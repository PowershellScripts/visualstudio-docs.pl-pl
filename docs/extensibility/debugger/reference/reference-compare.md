---
title: REFERENCE_COMPARE | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: REFERENCE_COMPARE
helpviewer_keywords: REFERENCE_COMPARE enumeration
ms.assetid: e31cdc78-f621-498b-9ca4-aefa790b9f6f
caps.latest.revision: "8"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 07d8b5ade6e80c0629d4f0c3eedee2941f9b95a5
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="referencecompare"></a>REFERENCE_COMPARE
Określa typ porównania dla odwołania.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
enum enum_REFERENCE_COMPARE {   
   REF_COMPARE_EQUAL        = 0x0001,  
   REF_COMPARE_LESS_THAN    = 0x0002,  
   REF_COMPARE_GREATER_THAN = 0x0003  
};  
typedef DWORD REFERENCE_COMPARE;  
```  
  
```csharp  
public enum enum_REFERENCE_COMPARE {   
   REF_COMPARE_EQUAL        = 0x0001,  
   REF_COMPARE_LESS_THAN    = 0x0002,  
   REF_COMPARE_GREATER_THAN = 0x0003  
};  
```  
  
## <a name="members"></a>Elementy członkowskie  
 REF_COMPARE_EQUAL  
 Określa porównanie równości.  
  
 REF_COMPARE_LESS_THAN  
 Określa mniej-niż porównania.  
  
 REF_COMPARE_GREATER_THAN  
 Określa większy-niż porównania.  
  
## <a name="remarks"></a>Uwagi  
 Przekazany jako argument [porównania](../../../extensibility/debugger/reference/idebugreference2-compare.md) metody.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Zestaw: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Wyliczenia](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [Porównaj](../../../extensibility/debugger/reference/idebugreference2-compare.md)