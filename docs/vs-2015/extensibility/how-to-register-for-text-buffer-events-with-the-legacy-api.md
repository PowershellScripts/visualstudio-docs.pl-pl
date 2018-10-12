---
title: 'Porady: rejestrowanie zdarzeń buforu tekstu przy użyciu starszej wersji interfejsu API | Dokumentacja firmy Microsoft'
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
- editors [Visual Studio SDK], legacy - register for text buffer events
ms.assetid: 5fc00ced-882c-4b48-b46c-1fa5a2469f94
caps.latest.revision: 14
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 76b782e688c567eb3888b2dbc890a360d22e3014
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49232248"
---
# <a name="how-to-register-for-text-buffer-events-with-the-legacy-api"></a>Porady: rejestrowanie zdarzeń buforu tekstu przy użyciu starszej wersji interfejsu API
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Jeśli uzyskujesz dostęp do buforu tekstowego przy użyciu starszej wersji interfejsu API, należy zarejestrować dla zdarzenia buforu tekstu, jak pokazano w poniższej procedurze.  
  
### <a name="to-advise-text-buffer-events"></a>Aby importowali zdarzenia buforu tekstu  
  
1.  Ze wskaźnika do jednego z interfejsów na <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextBuffer>, wywołaj `QueryInterface` dla wskaźnika do <xref:Microsoft.VisualStudio.OLE.Interop.IConnectionPointContainer>.  
  
2.  Wywołaj <xref:Microsoft.VisualStudio.OLE.Interop.IConnectionPointContainer.FindConnectionPoint%2A> metody i przekaż identyfikator interfejsu zdarzenia, dla których chcesz zarejestrować.  
  
     Na przykład, jeśli chcesz zarejestrować <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLinesEvents>, należy przekazać w interfejsie identyfikator IID_IVsTextLinesEvents.  
  
     Bufor tekstowy zwraca wskaźnik do <xref:Microsoft.VisualStudio.OLE.Interop.IConnectionPoint> interfejs dla obiektu punktu połączenia.  
  
3.  Za pomocą tego wskaźnika, wywołaj <xref:Microsoft.VisualStudio.OLE.Interop.IConnectionPoint.Advise%2A> metody, przekazując wskaźnik do implementacji interfejsu zdarzenia, dla którego chcesz zarejestrować, na przykład `IVsTextLinesEvents` interfejsu.  
  
     Środowisko zwraca plik cookie, który można następnie przestawaj słuchać zdarzeń przez wywołanie metody <xref:Microsoft.VisualStudio.OLE.Interop.IConnectionPoint.Unadvise%2A> metody.  
  
## <a name="see-also"></a>Zobacz też  
 [Zdarzenia buforu tekstowego w starszym interfejsie API](../extensibility/text-buffer-events-in-the-legacy-api.md)

