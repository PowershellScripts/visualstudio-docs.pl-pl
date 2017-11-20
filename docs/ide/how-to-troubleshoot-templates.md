---
title: "Porady: Rozwiązywanie problemów z szablonami | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: Visual Studio templates, troubleshooting
ms.assetid: 3e577ad2-f725-4c11-93b3-477f2404ec81
caps.latest.revision: "10"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: af00efbeb759bfc41d12e0ab814ecadd4bbc7799
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-troubleshoot-templates"></a>Porady: rozwiązywanie problemów z szablonami
Jeśli szablon nie może załadować w środowisku programistycznym, istnieje kilka sposobów, aby zlokalizować ten problem.  
  
## <a name="validating-the-vstemplate-file"></a>Sprawdzanie poprawności pliku .vstemplate  
 Jeśli plik .vstemplate w szablonie nie pasuje do [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] schematu szablonu szablonu nie może występować w **nowy projekt** okno dialogowe.  
  
#### <a name="to-validate-the-vstemplate-file"></a>Aby sprawdzić poprawność pliku .vstemplate  
  
1.  Zlokalizuj plik zip, który zawiera szablon.  
  
2.  Wyodrębnij plik zip.  
  
3.  Na **pliku** w menu [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)], kliknij przycisk **Otwórz**, a następnie kliknij przycisk **pliku**.  
  
4.  Wybierz plik .vstemplate szablonu, a następnie kliknij przycisk **Otwórz**.  
  
5.  Sprawdź, czy kod XML w pliku .vstemplate działa zgodnie z [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] schematu szablonu. Aby uzyskać więcej informacji o schemacie .vstemplate, zobacz [odwołanie do schematu szablonu Visual Studio](../extensibility/visual-studio-template-schema-reference.md).  
  
    > [!NOTE]
    >  Aby uzyskać pomoc techniczną IntelliSense podczas tworzenia pliku .vstemplate, Dodaj `xmlns` atrybutu `VSTemplate` element i przypisz jej wartość http://schemas.microsoft.com/developer/vstemplate/2005.  
  
6.  Zapisz i zamknij plik .vstemplate.  
  
7.  Wybierz pliki zawarte w szablonie, kliknij prawym przyciskiem myszy, wybierz opcję **Wyślij do**i kliknij przycisk **skompresowany Folder (zip)**. Wybrane pliki są kompresowane do pliku zip.  
  
8.  Umieść nowy plik zip, w tym samym katalogu co stary plik zip.  
  
9. Usuń pliki szablonów wyodrębnionego i stary plik zip szablonu.  
  
## <a name="monitoring-the-event-log"></a>Monitorowanie dziennika zdarzeń  
 [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]dzienniki błędów napotkanych podczas przetwarzania plików zip szablonu. Jeśli szablon nie jest wyświetlany w **nowy projekt** oczekiwano okno dialogowe jako, można użyć **Podgląd zdarzeń** Aby rozwiązać ten problem.  
  
#### <a name="to-locate-template-errors-in-event-viewer"></a>Aby znaleźć błędy szablonu w Podglądzie zdarzeń  
  
1.  W systemie Windows, kliknij przycisk **Start**, kliknij przycisk **Panelu sterowania**, kliknij dwukrotnie **narzędzia administracyjne**, a następnie kliknij dwukrotnie **Podgląd zdarzeń**.  
  
2.  W okienku po lewej stronie kliknij **aplikacji**.  
  
3.  Poszukaj zdarzeń z **źródła** wartość `Visual Studio - VsTemplate`.  
  
4.  Kliknij dwukrotnie zdarzenie szablonu, aby wyświetlić ten błąd.  
  
## <a name="see-also"></a>Zobacz też  
 [Dostosowywanie szablonów](../ide/customizing-project-and-item-templates.md)   
 [Tworzenie szablony projektów i elementów](../ide/creating-project-and-item-templates.md)   
 [Odwołanie do schematu szablonu Visual Studio](../extensibility/visual-studio-template-schema-reference.md)