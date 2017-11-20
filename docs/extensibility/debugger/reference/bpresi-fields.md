---
title: BPRESI_FIELDS | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: BPRESI_FIELDS
helpviewer_keywords: BPRESI_FIELDS enumeration
ms.assetid: 99f17b1e-3e67-4f85-89d6-5c6cf45c8008
caps.latest.revision: "11"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 90bd76940ea2b442d0f2aecdf28ebceb6e995ca1
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="bpresifields"></a>BPRESI_FIELDS
Określa informacje mają być pobrane informacje pomyślne rozpoznawanie punkt przerwania.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
enum enum_BPRESI_FIELDS {   
   BPRESI_BPRESLOCATION = 0x0001,  
   BPRESI_PROGRAM       = 0x0002,  
   BPRESI_THREAD        = 0x0004,  
   BPRESI_ALLFIELDS     = 0xffffffff  
};  
typedef DWORD BPRESI_FIELDS;  
```  
  
```csharp  
public enum enum_BPRESI_FIELDS {   
   BPRESI_BPRESLOCATION = 0x0001,  
   BPRESI_PROGRAM       = 0x0002,  
   BPRESI_THREAD        = 0x0004,  
   BPRESI_ALLFIELDS     = 0xffffffff  
};  
```  
  
## <a name="members"></a>Elementy członkowskie  
 BPRESI_BPRESLOCATION  
 Inicjowanie użycia `bpResLocation` pola (lokalizacji punktu przerwania rozpoznawania) [BP_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-resolution-info.md) struktury.  
  
 BPRESI_PROGRAM  
 Inicjowanie użycia `pProgram` pole `BP_RESOLUTION_INFO` struktury.  
  
 BPRESI_THREAD  
 Inicjowanie użycia `pThread` pole `BP_RESOLUTION_INFO` struktury.  
  
 BPRESI_ALLFIELDS  
 Określa wszystkie pola.  
  
## <a name="remarks"></a>Uwagi  
 Przekazany do [GetResolutionInfo](../../../extensibility/debugger/reference/idebugbreakpointresolution2-getresolutioninfo.md) metody, aby wskazać, które pola [BP_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-resolution-info.md) struktury mają być zainicjowany.  
  
 Te flagi są również używane w celu wskazania, które pola `BP_RESOLUTION_INFO` struktury są używane i prawidłowe, gdy jest zwracany tej struktury.  
  
 Te wartości mogą być łączone z bitowego `OR`.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Zestaw: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Wyliczenia](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [BP_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-resolution-info.md)   
 [GetResolutionInfo](../../../extensibility/debugger/reference/idebugbreakpointresolution2-getresolutioninfo.md)