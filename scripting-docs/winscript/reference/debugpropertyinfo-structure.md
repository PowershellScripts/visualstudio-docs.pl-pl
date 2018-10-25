---
title: Struktura DebugPropertyInfo | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- DebugPropertyInfo
apilocation:
- scrobj.dll
helpviewer_keywords:
- DebugPropertyInfo structure
ms.assetid: 3246efbc-c212-4024-8f07-6414c2f85e75
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 0dca3dac5c2e55e512bd4f798ca4a9bce82f7e00
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49874192"
---
# <a name="debugpropertyinfo-structure"></a>Struktura DebugPropertyInfo
Opisuje obiekt hierarchiczny charakter, który ma nazwę, typ i wartość. Służy do opisywania właściwości debugowania zmiennych lokalnych, parametrów, obejrzyj zmiennych i wyrażeń i rejestruje.  
  
## <a name="syntax"></a>Składnia  
  
```  
typedef struct DebugPropertyInfo{  
   DBGPROP_INFO_FLAGS  dwValidFields;  
   BSTR  bstrName;  
   BSTR  bstrType;  
   BSTR  bstrValue;  
   BSTR  bstrFullName;  
   DBGPROP_ATTRIB_FLAGS  dwAttrib;  
   IDebugProperty*  pDebugProp;  
};  
```  
  
## <a name="members"></a>Elementy członkowskie  
 dwValidFields  
 Wyliczany typ danych używany do określenia, które pola są inicjowane.  
  
 bstrName  
 Nazwa właściwości w kontekście.  
  
 bstrType  
 Typ właściwości jako sformatowany ciąg.  
  
 bstrValue  
 Wartość właściwości jako sformatowany ciąg.  
  
 bstrFullName  
 Pełna nazwa właściwości.  
  
 dwAttrib  
 Wyliczenie, które określa flagi dla atrybutów właściwości debugowania.  
  
 pDebugProp  
 `IDebugProperty` Opisanego przez informacje zawarte w tym `DebugPropertyInfo` struktury.  
  
## <a name="see-also"></a>Zobacz też  
 [Interfejs IDebugProperty](../../winscript/reference/idebugproperty-interface.md)   
 [DBGPROP_ATTRIB_FLAGS](../../winscript/reference/dbgprop-attrib-flags.md)   
 [DBGPROP_INFO_FLAGS](../../winscript/reference/dbgprop-info-flags.md)