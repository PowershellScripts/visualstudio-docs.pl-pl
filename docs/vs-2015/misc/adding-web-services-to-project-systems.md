---
title: Dodawanie usług sieci Web do systemy projektu | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-csharp
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- project systems, adding Web services
- Web services, adding to VSPackage project systems
ms.assetid: 8efa078b-68b2-45a2-9be2-44f807bc0d7f
caps.latest.revision: 8
manager: douge
ms.openlocfilehash: 88966ee17567970d0807792c57c2483cadb22f63
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49280322"
---
# <a name="adding-web-services-to-project-systems"></a>Dodawanie usług sieci Web do systemów projektów
Ogólnie rzecz biorąc, usługi XML sieci Web są adresy URL zasobów, które zwracają informacje do systemu projektu przy użyciu protokołu SOAP (Simple Object Access Protocol). Można zintegrować usługi sieci Web do systemu projektu pakietu VSPackage przy użyciu <xref:Microsoft.VisualStudio.Shell.Interop.IVsAddProjectItemDlg2> interfejsu.  
  
### <a name="to-add-a-web-service-to-your-project-system"></a>Aby dodać usługę sieci Web do systemu projektu  
  
1.  Wywołaj `QueryService` dla <xref:Microsoft.VisualStudio.Shell.Interop.IVsAddProjectItemDlg2> interfejsu za pośrednictwem <xref:Microsoft.VisualStudio.Shell.Interop.SVsAddWebReferenceDlg> usługi.  
  
2.  Wywołaj <xref:Microsoft.VisualStudio.Shell.Interop.IVsAddWebReferenceDlg2.AddWebReferenceDlg%2A> metody. Jeśli przekażesz w `pDiscoverySession` jako parametr `NULL`sesji funkcji odnajdywania jest tworzona automatycznie i sesja jest buforowany, dzięki czemu jest dostępny do późniejszego użytku przez <xref:Microsoft.VisualStudio.Shell.Interop.IVsAddWebReferenceDlg2> interfejsu. <xref:Microsoft.VisualStudio.Shell.Interop.IVsAddWebReferenceDlg2.AddWebReferenceDlg%2A> Metoda zwraca wskaźnik do <xref:Microsoft.VisualStudio.Shell.Interop.IDiscoveryResult2>.  
  
3.  Wywołaj <xref:Microsoft.VisualStudio.Shell.Interop.IDiscoveryResult.AddWebReference%2A> metody. Przekaż obiekt automatyzacji dla folderu odwołania do usługi sieci Web jako `pUnkWebReferenceFolder` parametru. W środowisku Visual Studio sprawdzi, jeśli usługa sieci Web jest już obecny. Jeśli usługa sieci Web nie jest obecny, środowiska pobiera i dodaje usługę sieci Web do folderu i dodatkowe pliki węzłów podrzędnych folderu (na przykład pliki .wsdl).  
  
## <a name="see-also"></a>Zobacz też  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsAddWebReferenceDlg2>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IDiscoveryResult>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IDiscoverySession>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsDiscoveryService>