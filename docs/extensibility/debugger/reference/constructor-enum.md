---
title: CONSTRUCTOR_ENUM | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- CONSTRUCTOR_ENUM
helpviewer_keywords:
- CONSTRUCTOR_ENUM enumeration
ms.assetid: 6d335b2c-66bc-460c-a4a6-4f3f1b697c2c
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 5a8302d89bb90902f2a31a81545f14dd233bbe1f
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49820541"
---
# <a name="constructorenum"></a>CONSTRUCTOR_ENUM
Zaznacza różne rodzaje konstruktorów.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
typedef enum ConstructorMatchOptions {   
   crAll       = 0,  
   crNonStatic = 1,  
   crStatic    = 2  
} CONSTRUCTOR_ENUM;  
```  
  
```csharp  
public enum ConstructorMatchOptions {   
   crAll       = 0,  
   crNonStatic = 1,  
   crStatic    = 2  
};  
```  
  
## <a name="members"></a>Elementy członkowskie  
 crAll  
 Wybiera wszystkie konstruktory.  
  
 crNonStatic  
 Wybiera niestatycznych konstruktorów.  
  
 crStatic  
 Wybiera konstruktorów statycznych.  
  
## <a name="remarks"></a>Uwagi  
 Przekazywany jako argument do [EnumConstructors](../../../extensibility/debugger/reference/idebugclassfield-enumconstructors.md) metody.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Wyliczenia](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [GetReason](../../../extensibility/debugger/reference/idebugcanstopevent2-getreason.md)