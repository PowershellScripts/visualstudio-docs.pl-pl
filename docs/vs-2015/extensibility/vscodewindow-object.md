---
title: Obiekt VSCodeWindow | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- VSCodeWindow
helpviewer_keywords:
- views [Visual Studio SDK], VSCodeWindow object
- VsCodeWindow object
ms.assetid: cf5fe926-e784-4098-bc01-cac49c7c55c6
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 12752b015bc8e3f69002fd8732622fc11eface65
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49259381"
---
# <a name="vscodewindow-object"></a>VSCodeWindow, obiekt
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Okno kodu jest okno dokumentu specjalistyczne, który może zawierać jeden lub więcej widoków tekstu, zwykle <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextView> obiektu.  
  
 Pod względem architektury w oknie Kod jest okno dokumentu, który znajduje się w ramki okna. Funkcjonalnie okna kodu jest po prostu okno dokumentu z dodatkowych funkcji. W trybie interfejsu wielu dokumentów (MDI) w oknie Kod jest podrzędna ramka MDI. Aby uzyskać więcej informacji, zobacz [Dostosowywanie Windows kodu za pomocą starszej wersji interfejsu API](../extensibility/customizing-code-windows-by-using-the-legacy-api.md).  
  
 Poniższa tabela zawiera interfejsy w <xref:Microsoft.VisualStudio.TextManager.Interop.VsCodeWindow> obiektu.  
  
|Metoda|Opis|  
|------------|-----------------|  
|<xref:Microsoft.VisualStudio.OLE.Interop.IServiceProvider>|Dostarcza mechanizm ogólnego dostępu do lokalizowania usługi, która identyfikuje Unikatowy identyfikator globalny (GUID).|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsCodeWindow>|Reprezentuje wiele podrzędnych interfejsu (MDI) dokumentu zawierającego jeden lub więcej widoków kodu.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowPane>|Wypełnia ramki okna.|  
  
## <a name="see-also"></a>Zobacz też  
 <xref:Microsoft.VisualStudio.OLE.Interop.IServiceProvider>   
 [Edytuj dane](http://msdn.microsoft.com/en-us/f08872bd-fd9c-4e36-8cf2-a2a2622ef986)

