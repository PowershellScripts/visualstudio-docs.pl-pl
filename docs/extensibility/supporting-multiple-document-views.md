---
title: Obsługa wielu widoków dokumentu | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], custom - multiple document views
ms.assetid: c7ec2366-91c4-477f-908d-e89068bdb3e3
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 5a2fafdaaa2d54cd445017ebd9120d8648bf7067
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49942351"
---
# <a name="supporting-multiple-document-views"></a>Obsługa wielu widoków dokumentu
Możesz podać więcej niż jeden widok dokumentu, tworząc oddzielny dokument dane i obiekty widoku dokumentu dla edytora. Czasami, w których będzie przydatny widok dokumentu dodatkowe są następujące:  
  
- Nowe okno obsługi: ma tego edytora, aby zapewnić co najmniej dwa widoki tego samego typu, aby użytkownik, który jest już otwarte w edytorze okna można otworzyć nowe okno, wybierając **nowe okno** polecenia **okna** menu.  
  
- Formularz i kodu umożliwia wyświetlenie pomocy technicznej: ma tego edytora, aby zawierają widoki różnych typów. [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)], na przykład zawiera widok formularza i widoku kodu.  
  
  Aby uzyskać więcej informacji na ten temat zobacz procedurę CreateEditorInstance w pliku EditorFactory.cs w projekcie niestandardowy edytor, utworzona przez szablon pakietu Visual Studio. Aby uzyskać więcej informacji na temat tego projektu, zobacz [wskazówki: Tworzenie niestandardowego edytora](../extensibility/walkthrough-creating-a-custom-editor.md).  
  
## <a name="synchronizing-views"></a>Synchronizowanie widoków  
 Podczas implementowania wielu widoków dokumentu obiekt danych jest musi zachować wszystkie widoki zsynchronizowane z danymi. Można użyć obsługi interfejsy na zdarzeń <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextBuffer> do synchronizowania wielu widoków z danymi.  
  
 Jeśli nie używasz <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextBuffer> obiekt, aby zsynchronizować wiele widoków, a następnie należy zaimplementować własny system zdarzeń do obsługi zmiany wprowadzone do obiektu danych dokumentu. Różne poziomy szczegółowości umożliwia aktualizowanie wielu widoków. Ustawienie maksymalnej szczegółowości, podczas wpisywania w jednym widoku inne widoki zostaną zaktualizowane od razu. Za pomocą minimalna szczegółowość innych widoków nie są aktualizowane, dopóki ich aktywacji.  
  
## <a name="determining-whether-document-data-is-already-open"></a>Określanie, czy dane dokumentu jest już otwarty  
 Uruchamianie tabeli dokumentu (Normalizacją) w zintegrowanym środowisku programistycznym (IDE) pomaga śledzić, czy dane dla dokumentu jest jeszcze otwarty, jak pokazano na poniższym diagramie.  
  
 ![DocDataView — grafika](../extensibility/media/docdataview.gif "DocDataView —")  
Wiele widoków  
  
 Domyślnie każdego widoku (obiekt widoku dokumentu) znajduje się w jego własnej ramki okna (<xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowFrame>). Jak już wspomniano, jednak dokumentu dane mogą być wyświetlane w wielu widoków. Aby włączyć tę opcję, Visual Studio sprawdza Normalizacją, aby ustalić, czy danego dokumentu jest już otwarty w edytorze. Kiedy wywołuje IDE <xref:Microsoft.VisualStudio.Shell.Interop.IVsEditorFactory.CreateEditorInstance%2A> do tworzenia edytora, zwracane wartości innej niż NULL, w `punkDocDataExisting` parametr wskazuje, czy dokument jest już otwarty w innym edytorze. Aby uzyskać więcej informacji na temat funkcji Normalizacją, zobacz [uruchamianie tabeli dokumentu](../extensibility/internals/running-document-table.md).  
  
 W swojej <xref:Microsoft.VisualStudio.Shell.Interop.IVsEditorFactory> implementacji, sprawdź obiekt danych dokumentu, które są zwracane w `punkDocDataExisting` ustalenie, czy dane dokumentu są odpowiednie dla Twojego edytora. (Na przykład HTML wyświetlone tylko dane powinny przez edytor HTML.) Jeśli jest to odpowiednie, fabryką Edytor powinien zapewniają drugi widok danych. Jeśli `punkDocDataExisting` parametr nie jest `NULL`, istnieje możliwość, albo czy obiekt danych dokument jest otwarty w innym edytorze, a bardziej prawdopodobne, dane dokumentu jest już otwarty w innym widoku z tym samym edytora. Jeśli dane dokumentu jest otwarty w innej edytor, który nie obsługuje usługi fabryka edytora, Visual Studio nie można otworzyć usługi fabryka edytora. Aby uzyskać więcej informacji, zobacz [porady: dołączanie widoków do danych dokumentu](../extensibility/how-to-attach-views-to-document-data.md).