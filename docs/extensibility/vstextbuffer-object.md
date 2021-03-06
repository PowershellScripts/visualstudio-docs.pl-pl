---
title: Obiekt VSTextBuffer | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- VSTextBuffer
helpviewer_keywords:
- VSTextBuffer object, reference
- views [Visual Studio SDK], VSTextBuffer object
ms.assetid: c5f94b45-7249-4e1f-a53d-1d2a1c61e0ef
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 587a0193dea0f4a8d16ea0555cf5788cd1ead1d5
ms.sourcegitcommit: 9765b3fcf89375ca499afd9fc42cf4645b66a8a2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/20/2018
ms.locfileid: "46495352"
---
# <a name="vstextbuffer-object"></a>Obiekt VSTextBuffer
Obiekt bufor tekstowy przedstawia strumień tekst Unicode, który jest zazwyczaj skojarzone z plikiem. A <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextBuffer> obiekt może być używany poza kontekstem podstawowy edytor, tak jak kreatora.  
  
 W poniższej tabeli przedstawiono interfejsy `VSTextBuffer`.  
  
|Metoda|Opis|  
|------------|-----------------|  
|[IOleCommandTarget](/windows/desktop/api/docobj/nn-docobj-iolecommandtarget)|Standardowy interfejs OLE. Używane do obsługi w buforze Cofnij/Ponów.|  
|[IPersistFile](/windows/desktop/api/objidl/nn-objidl-ipersistfile)|Standardowy interfejs OLE.|  
|[IPersistStream](/windows/desktop/api/objidl/nn-objidl-ipersiststream)|Standardowy interfejs OLE.|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsCompoundAction>|Umożliwia tworzenie akcji związki (czyli akcje, które są grupowane w jednostce pojedynczego Cofnij/ponów).|  
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistDocData>|Włącza trwałość danych dokumentu zarządzanych przez bufor tekstowy.|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextBuffer>|Oferuje podstawowe usługi; używane przez wielu klientów.|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextFind>|Służy do wyszukiwania buforu.|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLines>|Umożliwia odczytywanie i zapisywanie funkcji przy użyciu dwuwymiarowe współrzędne. Dziedziczy `IVsTextBuffer`.|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextStream>|Umożliwia odczytywanie i zapisywanie funkcji przy użyciu współrzędnych jednowymiarowa. Dziedziczy `IVsTextBuffer`.|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextScanner>|Udostępnia szybką, zorientowane na strumień, sekwencyjnych tekstu w buforze.|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsUserData>|Zapewnia dostęp do ogólnego zbiór właściwości. Najważniejsze właściwości jest nazwa lub krótkiej nazwy buforu. Losowe dane można przechowywać w buforze z tym interfejsem, tworząc identyfikator GUID i używać go jako klucza.|  
|<xref:Microsoft.VisualStudio.OLE.Interop.IConnectionPointContainer>|Obsługuje punkty połączenia dla zdarzeń.|  
  
## <a name="remarks"></a>Uwagi  
 `VSTextBuffer` Znajduje się zwykle przez `QueryInterface` wywołanie na `IVsTextBuffer`. Aby uzyskać więcej informacji, zobacz [bufor tekstowy](../extensibility/accessing-the-text-buffer-by-using-the-legacy-api.md).  
  
## <a name="see-also"></a>Zobacz także  
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextBuffer>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextView>   
 [Edytuj dane](https://www.microsoft.com/download/details.aspx?id=55984)