---
title: Uproszczone osadzanie | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- editors [Visual Studio SDK], custom - simple view embedding
ms.assetid: f1292478-a57d-48ec-8c9e-88a23f04ffe5
caps.latest.revision: 17
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 3919e64e9ce8a3e343a9ebba997a178f4f4230e6
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49257507"
---
# <a name="simplified-embedding"></a>Uproszczone osadzanie
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Uproszczone osadzanie jest włączona w edytorze, po jego obiekt widoku dokumentu jest elementem nadrzędnym (czyli przeprowadzone elementu podrzędnego) [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]i <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowPane> interfejs jest implementowany jej okna poleceń. Uproszczone osadzanie edytory nie może obsługiwać aktywny formant. Obiekty, używany do tworzenia edytora za pomocą uproszczone osadzanie przedstawiono na poniższej ilustracji.  
  
 ![Uproszczone osadzanie w edytorze grafiki](../extensibility/media/vssimplifiedembeddingeditor.gif "vsSimplifiedEmbeddingEditor")  
Edytor z uproszczone osadzanie  
  
> [!NOTE]
>  Obiektów na tej ilustracji tylko `CYourEditorFactory` obiektu jest wymagana do utworzenia standardowy edytor opartych na plikach. Jeśli tworzysz niestandardowy edytor, nie należy implementować <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistDocData2>, ponieważ edytor prawdopodobnie będzie mieć własny mechanizm prywatnej trwałości. Dla innych niestandardowych edytorów jednak należy to zrobić.  
  
 Wszystkie interfejsy zaimplementowane do tworzenia edytora za pomocą uproszczone osadzanie są zawarte w `CYourEditorDocument` obiektu. Jednak do obsługi wielu widoków danych dokumentu, Podziel interfejsy na osobne dane i przeglądać obiekty zgodnie z instrukcjami w poniższej tabeli.  
  
|Interface|Lokalizacja interfejsu|Zastosowanie|  
|---------------|---------------------------|---------|  
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowPane>|Widok|Udostępnia połączenie do okna nadrzędnego.|  
|<xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget>|Widok|Obsługuje polecenia.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser>|Widok|Włącza aktualizacje paska stanu.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsToolboxUser>|Widok|Włącza **przybornika** elementów.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsFileChangeEvents>|Dane|Wysyła powiadomienia po zmianie pliku.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.IPersistFileFormat>|Dane|Włącza funkcję Zapisz jako dla typu pliku.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistDocData2>|Dane|Umożliwia utrwalanie w dokumencie.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsDocDataFileChangeControl>|Dane|Umożliwia pomijanie zdarzeń zmiany plików, takie jak wyzwolenie Załaduj ponownie.|

