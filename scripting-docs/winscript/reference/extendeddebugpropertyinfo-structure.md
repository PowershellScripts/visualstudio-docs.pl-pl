---
title: Struktura ExtendedDebugPropertyInfo | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- ExtendedDebugPropertyInfo
apilocation:
- scrobj.dll
helpviewer_keywords:
- ExtendedDebugPropertyInfo structure
ms.assetid: f2cf6477-454b-4d13-95da-ae4c90daa175
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 62b9f3b5877f7919a57e9747355276e438240796
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49888908"
---
# <a name="extendeddebugpropertyinfo-structure"></a>Struktura ExtendedDebugPropertyInfo
Rozszerza `DebugPropertyInfo` strukturę dodatkowe elementy członkowskie w celu scharakteryzowania właściwości rozszerzonej.  
  
## <a name="syntax"></a>Składnia  
  
```  
typedef struct ExtendedDebugPropertyInfo{  
   DBGPROP_INFO_FLAGS  dwValidFields;  
   LPOLESTR  bstrName;  
   LPOLESTR  bstrType;  
   LPOLESTR  bstrValue;  
   LPOLESTR  bstrFullName;  
   DBGPROP_ATTRIB_FLAGS  dwAttrib;  
   IDebugProperty*  pDebugProp;  
   DWORD  nDISPID;  
   DWORD  nType;  
   VARIANT  varValue;  
   ILockBytes*  plbValue;  
   IDebugExtendedProperty*  pDebugExtProp;  
};  
```  
  
## <a name="members"></a>Elementy członkowskie  
 `dwValidFields`  
 Wyliczany typ danych używany do określenia, które pola są inicjowane.  
  
 `bstrName`  
 Nazwa właściwości w kontekście.  
  
 `bstrType`  
 Typ właściwości jako sformatowany ciąg.  
  
 `bstrValue`  
 Wartość właściwości jako ciąg formatowania.  
  
 `bstrFullName`  
 Pełna nazwa właściwości.  
  
 `dwAttrib`  
 Wyliczenie, które określa flagi dla atrybutów właściwości debugowania.  
  
 `pDebugProp`  
 `IDebugProperty` Obiekt odpowiadający to `ExtendedDebugPropertyInfo`.  
  
 `nDISPID`  
 Identyfikator wysyłki.  
  
 `nType`  
 Typ właściwości rozszerzonej.  
  
 `varValue`  
 Wartość właściwości rozszerzonej, jeśli zmieści się w WARIANCIE.  
  
 `plbValue`  
 Bajty danych rzeczywistych wartości właściwości.  
  
 `pDebugExtProp`  
 `IDebugExtendedProperty` Obiekt odpowiadający to `ExtendedDebugPropertyInfo`.  
  
## <a name="see-also"></a>Zobacz też  
 [Struktura DebugPropertyInfo](../../winscript/reference/debugpropertyinfo-structure.md)   
 [Interfejs IDebugProperty](../../winscript/reference/idebugproperty-interface.md)   
 [Interfejs IDebugExtendedProperty](../../winscript/reference/idebugextendedproperty-interface.md)   
 [DBGPROP_ATTRIB_FLAGS](../../winscript/reference/dbgprop-attrib-flags.md)   
 [DBGPROP_INFO_FLAGS](../../winscript/reference/dbgprop-info-flags.md)