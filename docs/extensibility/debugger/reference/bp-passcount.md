---
title: BP_PASSCOUNT | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- BP_PASSCOUNT
helpviewer_keywords:
- BP_PASSCOUNT structure
ms.assetid: 791ac175-b897-4c70-873e-240da7e0ac89
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 105c6668c50d690bcc0016f888ce1f241130d1eb
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49883123"
---
# <a name="bppasscount"></a>BP_PASSCOUNT
W tym artykule opisano, liczbę i warunki, na których jest uruchamiany warunkowego punktu przerwania.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
typedef struct _BP_PASSCOUNT {   
   DWORD              dwPassCount;  
   BP_PASSCOUNT_STYLE stylePassCount;  
} BP_PASSCOUNT;  
```  
  
```csharp  
public struct BP_PASSCOUNT {   
   public uint dwPassCount;  
   public uint stylePassCount;  
};  
```  
  
## <a name="members"></a>Elementy członkowskie  
 `dwPassCount`  
 Liczba razy, aby przekazać za pośrednictwem punktu przerwania przed wyzwoleniem go.  
  
 `stylePassCount`  
 Wartość z zakresu od [BP_PASSCOUNT_STYLE](../../../extensibility/debugger/reference/bp-passcount-style.md) Liczba przebiegów wyliczenie, które określa styl punkt przerwania.  
  
## <a name="remarks"></a>Uwagi  
 Ta struktura jest elementem członkowskim [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md) struktury.  
  
 Ta struktura również jest przekazywany jako parametr do[SetPassCount](../../../extensibility/debugger/reference/idebugboundbreakpoint2-setpasscount.md) i[SetPassCount](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-setpasscount.md) metody.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Struktur i Unii](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md)   
 [SetPassCount](../../../extensibility/debugger/reference/idebugboundbreakpoint2-setpasscount.md)   
 [SetPassCount](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-setpasscount.md)   
 [BP_PASSCOUNT_STYLE](../../../extensibility/debugger/reference/bp-passcount-style.md)