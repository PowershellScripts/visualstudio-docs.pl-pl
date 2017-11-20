---
title: IDebugCustomAttributeQuery2 | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugCustomAttributeQuery2
helpviewer_keywords:
- IDebugCustomAttributeQuery interface
- IDebugCustomAttributeQuery2 interface
ms.assetid: 7cfa23e4-a05a-47a3-af6c-bd40c655014b
caps.latest.revision: "13"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 57e31ef81b9f03943597e32428cc97993aa30936
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idebugcustomattributequery2"></a>IDebugCustomAttributeQuery2
Określa istnienie atrybutu niestandardowego dla tego pola i, jeśli istnieje, zwraca informacje o atrybutach.  
  
## <a name="syntax"></a>Składnia  
  
```  
IDebugCustomAttributeQuery2 : IDebugCustomAttributeQuery  
```  
  
## <a name="notes-for-implementers"></a>Uwagi dotyczące implementacji  
 Dostawca symbol implementuje ten interfejs dla tego samego obiektu, który implementuje [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) w celu obsługi niestandardowych atrybutów.  
  
## <a name="notes-for-callers"></a>Uwagi dotyczące wywoływania  
 Użyj [QueryInterface](/cpp/atl/queryinterface) uzyskać ten interfejs z [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) interfejsu.  
  
## <a name="methods-in-vtable-order"></a>Metody w kolejności Vtable  
 W poniższej tabeli przedstawiono metody **IDebugCustomAttributeQuery** interfejsu.  
  
|Metoda|Opis|  
|------------|-----------------|  
|[IsCustomAttributeDefined](../../../extensibility/debugger/reference/idebugcustomattributequery2-iscustomattributedefined.md)|Określa, czy atrybut niestandardowy istnieje według nazwy.|  
|[GetCustomAttributeByName](../../../extensibility/debugger/reference/idebugcustomattributequery2-getcustomattributebyname.md)|Pobiera informacje o atrybutach dotyczące danego atrybutu niestandardowego.|  
  
 Oprócz **IDebugCustomAttributeQuery** metod `IDebugCustomAttributeQuery2` implementuje następującą metodę:  
  
|Metoda|Opis|  
|------------|-----------------|  
|[EnumCustomAttributes](../../../extensibility/debugger/reference/idebugcustomattributequery2-enumcustomattributes.md)|Pobiera moduł wyliczający dla wszystkich atrybutów niestandardowych dołączony do tego pola.|  
  
## <a name="remarks"></a>Uwagi  
 [IEnumDebugCustomAttributes](../../../extensibility/debugger/reference/ienumdebugcustomattributes.md) metoda może zwracać moduł wyliczający dla wszystkich atrybutów niestandardowych zdefiniowanych dla tego pola.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Zestaw: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Symbol dostawcy interfejsów](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)   
 [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)   
 [IEnumDebugCustomAttributes](../../../extensibility/debugger/reference/ienumdebugcustomattributes.md)