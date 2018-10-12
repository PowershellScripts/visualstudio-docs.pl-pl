---
title: 'Porady: Implementowanie Znajdź i Zamień mechanizm | Dokumentacja firmy Microsoft'
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
- editors [Visual Studio SDK], legacy - find and replace
ms.assetid: bbd348db-3d19-42eb-99a2-3e808528c0ca
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: d4ec48a1392efa67f17432f071c9bf4894c35e87
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49304021"
---
# <a name="how-to-implement-the-find-and-replace-mechanism"></a>Porady: Implementowanie Znajdź i Zamień mechanizm
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Program Visual Studio udostępnia dwa sposoby wdrażania Znajdź/Zamień. Jednym ze sposobów jest przekazać obraz tekstu do powłoki i pozwól mu obsługę wyszukiwania, wyróżniania i zastępowanie tekstu. Dzięki temu użytkownicy mogą określić wiele zakresów tekstu. Alternatywnie Twoje pakietu VSPackage można kontrolować ta sama funkcja. W obu przypadkach należy powiadomić powłoki o bieżący element docelowy i elementy docelowe wszystkie otwarte dokumenty.  
  
### <a name="to-implement-findreplace"></a>Aby zaimplementować Znajdź i Zamień  
  
1.  Implementowanie <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget> interfejsu na jednym z obiektów zwróconych przez właściwości ramki <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID> lub <xref:Microsoft.VisualStudio.Shell.Interop.__VSFPROPID>. Jeśli tworzysz niestandardowy edytor, powinien implementować ten interfejs jako część klasy edytora niestandardowego.  
  
2.  Użyj <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.GetCapabilities%2A> metody, aby określić opcje, które obsługuje edytora i, aby wskazać, czy implementuje wyszukiwanie obrazów tekstu.  
  
     Jeśli Edytor obsługuje wyszukiwanie obrazów tekstu, należy zaimplementować <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.GetSearchImage%2A>.  
  
     W przeciwnym razie zaimplementować <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Find%2A> i <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Replace%2A>.  
  
3.  W przypadku zaimplementowania <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Find%2A> i <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Replace%2A> metody, można ułatwić wyszukiwanie zadań, wywołując <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindHelper> interfejsu.  
  
## <a name="see-also"></a>Zobacz też  
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindHelper>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Find%2A>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.GetSearchImage%2A>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsFindTarget.Replace%2A>   
 <xref:Microsoft.VisualStudio.Shell.Interop.__VSPROPID>

