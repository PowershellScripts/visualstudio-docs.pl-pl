---
title: BP_COND_STYLE | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- BP_COND_STYLE
helpviewer_keywords:
- BP_COND_STYLE enumeration
ms.assetid: a93b1412-f447-48a1-af9d-38f3dbb3092f
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 8ff46d6cae842d258aab8fb03409ff263670c410
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49939777"
---
# <a name="bpcondstyle"></a>BP_COND_STYLE
Określa styl warunku punktu przerwania dla oczekujące i powiązane punkty przerwania.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
enum enum_BP_COND_STYLE {   
   BP_COND_NONE         = 0x0000,  
   BP_COND_WHEN_TRUE    = 0x0001,  
   BP_COND_WHEN_CHANGED = 0x0002  
};  
typedef DWORD BP_COND_STYLE;  
```  
  
```csharp  
public enum enum_BP_COND_STYLE {   
   BP_COND_NONE         = 0x0000,  
   BP_COND_WHEN_TRUE    = 0x0001,  
   BP_COND_WHEN_CHANGED = 0x0002  
};  
```  
  
## <a name="members"></a>Elementy członkowskie  
 BP_COND_NONE  
 Uruchamia punkt przerwania, po osiągnięciu punktu przerwania pozycji. Nie określono warunek punktu przerwania.  
  
 BP_COND_WHEN_TRUE  
 Uruchamia punkt przerwania, tylko jeśli wyrażenie warunkowe skojarzony punkt przerwania daje w wyniku `true`.  
  
 BP_COND_WHEN_CHANGED  
 Uruchamiany punkt przerwania tylko wtedy, gdy wartość wyrażenia warunkowego skojarzony punkt przerwania został zmieniony z jego poprzedniej oceny.  
  
## <a name="remarks"></a>Uwagi  
 Używany do `styleCondition` członkiem [BP_CONDITION](../../../extensibility/debugger/reference/bp-condition.md) struktury.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Wyliczenia](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [BP_CONDITION](../../../extensibility/debugger/reference/bp-condition.md)