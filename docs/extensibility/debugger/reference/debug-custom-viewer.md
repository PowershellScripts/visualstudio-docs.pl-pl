---
title: DEBUG_CUSTOM_VIEWER | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- DEBUG_CUSTOM_VIEWER
helpviewer_keywords:
- DEBUG_CUSTOM_VIEWER structure
ms.assetid: 8e0ef3f0-0107-48e8-a037-6e52b4c4ed9d
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: e86cae45298b3f137e2ebca65fa8c531c6d86457
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49908447"
---
# <a name="debugcustomviewer"></a>DEBUG_CUSTOM_VIEWER
Struktura, która identyfikuje podglądu niestandardowego lub typu wizualizatora.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
typedef struct tagDEBUG_CUSTOM_VIEWER {  
   DWORD dwID;  
   BSTR  bstrMenuName;  
   BSTR  bstrDescription;  
   GUID  guidLang;  
   GUID  guidVendor;  
   BSTR  bstrMetric;  
} DEBUG_CUSTOM_VIEWER;  
```  
  
```csharp  
public struct DEBUG_CUSTOM_VIEWER {  
   public uint   dwID;  
   public string bstrMenuName;  
   public string bstrDescription;  
   public Guid   guidLang;  
   public Guid   guidVendor;  
   public string bstrMetric;  
};  
```  
  
## <a name="members"></a>Elementy członkowskie  
 dwID  
 Identyfikator, aby odróżnić wiele osób przeglądających lub wizualizatorów implementowane za pomocą jednej `GUID`.  
  
 bstrMenuName  
 Tekst, który będzie wyświetlany w menu rozwijanym.  
  
 bstrDescription  
 Opis podglądu niestandardowego lub Wizualizator typów (musi być wartością null Jeśli nie są używane).  
  
 guidLang  
 Język dostarczanie Ewaluator wyrażeń.  
  
 guidVendor  
 Dostawca dostarczanie Ewaluator wyrażeń.  
  
 bstrMetric  
 Metryki w ramach której przeglądarka niestandardowa lub typu wizualizatora `CLSID` są przechowywane.  
  
## <a name="remarks"></a>Uwagi  
 Lista ta struktura jest zwracany przez wywołanie [GetCustomViewerList](../../../extensibility/debugger/reference/idebugproperty3-getcustomviewerlist.md) — metoda (a w konsekwencji, [GetCustomViewerList](../../../extensibility/debugger/reference/ieevisualizerservice-getcustomviewerlist.md) metody).  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Struktur i Unii](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [GetCustomViewerList](../../../extensibility/debugger/reference/idebugproperty3-getcustomviewerlist.md)   
 [GetCustomViewerList](../../../extensibility/debugger/reference/ieevisualizerservice-getcustomviewerlist.md)