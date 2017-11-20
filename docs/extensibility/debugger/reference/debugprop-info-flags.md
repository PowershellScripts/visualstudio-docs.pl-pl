---
title: DEBUGPROP_INFO_FLAGS | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: DEBUGPROP_INFO_FLAGS
helpviewer_keywords: DBGPROP_INFO_FLAGS enumeration
ms.assetid: 1c7fe777-615e-4929-9ed4-970d9fe0eb81
caps.latest.revision: "11"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 24b0208cdfd49ef07ba85803d03a1e2c4aa91553
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="debugpropinfoflags"></a>DEBUGPROP_INFO_FLAGS
Określa, jakie informacje do pobrania dotyczące obiektu właściwości debugowania.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
enum enum_DEBUGPROP_INFO_FLAGS {   
   DEBUGPROP_INFO_FULLNAME          = 0x00000001,  
   DEBUGPROP_INFO_NAME              = 0x00000002,  
   DEBUGPROP_INFO_TYPE              = 0x00000004,  
   DEBUGPROP_INFO_VALUE             = 0x00000008,  
   DEBUGPROP_INFO_ATTRIB            = 0x00000010,  
   DEBUGPROP_INFO_PROP              = 0x00000020,  
   DEBUGPROP_INFO_VALUE_AUTOEXPAND  = 0x00010000,  
   DEBUGPROP_INFO_VALUE_NOFUNCEVAL  = 0x00020000,  
   DEBUGPROP_INFO_VALUE_RAW         = 0x00040000,  
   DEBUGPROP_INFO_VALUE_NO_TOSTRING = 0x00080000  
   DEBUGPROP_INFO_NONE              = 0x00000000,  
   DEBUGPROP_INFO_STANDARD          = DEBUGPROP_INFO_ATTRIB |  
                                      DEBUGPROP_INFO_NAME |  
                                      DEBUGPROP_INFO_TYPE |  
                                      DEBUGPROP_INFO_VALUE,  
   DEBUGPROP_INFO_ALL               = 0xffffffff  
};  
typedef DWORD DEBUGPROP_INFO_FLAGS;  
```  
  
```csharp  
public enum enum_DEBUGPROP_INFO_FLAGS {   
   DEBUGPROP_INFO_FULLNAME          = 0x00000001,  
   DEBUGPROP_INFO_NAME              = 0x00000002,  
   DEBUGPROP_INFO_TYPE              = 0x00000004,  
   DEBUGPROP_INFO_VALUE             = 0x00000008,  
   DEBUGPROP_INFO_ATTRIB            = 0x00000010,  
   DEBUGPROP_INFO_PROP              = 0x00000020,  
   DEBUGPROP_INFO_VALUE_AUTOEXPAND  = 0x00010000,  
   DEBUGPROP_INFO_VALUE_NOFUNCEVAL  = 0x00020000,  
   DEBUGPROP_INFO_VALUE_RAW         = 0x00040000,  
   DEBUGPROP_INFO_VALUE_NO_TOSTRING = 0x00080000  
   DEBUGPROP_INFO_NONE              = 0x00000000,  
   DEBUGPROP_INFO_STANDARD          = DEBUGPROP_INFO_ATTRIB |  
                                      DEBUGPROP_INFO_NAME |  
                                      DEBUGPROP_INFO_TYPE |  
                                      DEBUGPROP_INFO_VALUE,  
   DEBUGPROP_INFO_ALL               = 0xffffffff  
};  
```  
  
## <a name="members"></a>Elementy członkowskie  
 DEBUGPROP_INFO_FULLNAME  
 Inicjowanie użycia `bstrFullName` pola.  
  
 DEBUGPROP_INFO_NAME  
 Inicjowanie użycia `bstrName` pola.  
  
 DEBUGPROP_INFO_TYPE  
 Inicjowanie użycia `bstrType` pola.  
  
 DEBUGPROP_INFO_VALUE  
 Inicjowanie użycia `bstrValue` pola.  
  
 DEBUGPROP_INFO_ATTRIB  
 Inicjowanie użycia `dwAttrib` pola.  
  
 DEBUGPROP_INFO_PROP,  
 Inicjowanie użycia `pProperty` pola, które zawiera [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) interfejsu.  
  
 DEBUGPROP_INFO_VALUE_AUTOEXPAND  
 Oznacza, że pole wartości może zawierać wartość rozwinięty automatycznie, jeśli jest dostępna dla tego typu obiektu.  
  
 DEBUGPROP_INFO_VALUE_NOFUNCEVAL  
 Przestarzałe.  
  
 DEBUGPROP_INFO_VALUE_RAW  
 Zwraca wszystkie wartości beautified lub elementy członkowskie (czyli bez formatowania wartości).  
  
 DEBUGPROP_INFO_VALUE_NO_TOSTRING  
 Nie zwraca żadnych specjalnych syntezatora wartości (na przykład nie należy wywoływać `ToString()` obiektu w celu utworzenia wartości).  
  
 DEBUGPROP_INFO_NONE  
 Określa, że ustawiono żadnych flag.  
  
 DEBUGPROP_INFO_STANDARD  
 Inicjowanie użycia `dwAttrib`, `bstrName`, `bstrType`, i `bstrValue` pól.  
  
 DEBUGPROP_INFO_All  
 Wskazuje maskę wszystkie flagi.  
  
## <a name="remarks"></a>Uwagi  
 Te wartości są przekazywane do [GetPropertyInfo](../../../extensibility/debugger/reference/idebugproperty2-getpropertyinfo.md), [EnumChildren](../../../extensibility/debugger/reference/idebugproperty2-enumchildren.md), i [EnumProperties](../../../extensibility/debugger/reference/idebugstackframe2-enumproperties.md) metod, aby określić pola, które mają zostać zainicjowany [ DEBUG_PROPERTY_INFO](../../../extensibility/debugger/reference/debug-property-info.md) struktury.  
  
 Te wartości są używane również do `dwFields` członkiem `DEBUG_PROPERTY_INFO` struktury, aby wskazać, które pola struktury są używane i prawidłowe, gdy struktura jest zwracany.  
  
 Te wartości mogą być łączone z bitowego `OR`.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Zestaw: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Wyliczenia](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)   
 [GetPropertyInfo](../../../extensibility/debugger/reference/idebugproperty2-getpropertyinfo.md)   
 [EnumChildren](../../../extensibility/debugger/reference/idebugproperty2-enumchildren.md)   
 [EnumProperties](../../../extensibility/debugger/reference/idebugstackframe2-enumproperties.md)   
 [DEBUG_PROPERTY_INFO](../../../extensibility/debugger/reference/debug-property-info.md)