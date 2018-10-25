---
title: IDebugProperty::EnumMembers | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugProperty.EnumMembers
apilocation:
- scrobj.dll
helpviewer_keywords:
- IDebugProperty::EnumMembers
ms.assetid: 8ce398a5-6452-4804-ae8f-5c54cd11c661
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 07ad47ee8d0232df5f528db659def421475e7b33
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49924248"
---
# <a name="idebugpropertyenummembers"></a>IDebugProperty::EnumMembers
Wylicza właściwości elementów członkowskich.  
  
## <a name="syntax"></a>Składnia  
  
```  
HRESULT EnumMembers (  
   DBGPROP_INFO_FLAGSdwFieldSpec,  
   UINTnRadix,  
   REFIIDrefiid,  
   IEnumDebugPropertyInfo**ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `dwFieldSpec`  
 [in] Określa `DBGPROP_INFO_FLAGS` stałych, które określają, pola, które w strukturach właściwości debugowania wyliczenia mają zostać wypełnione.  
  
 `nRadix`  
 [in] Podstawy do użycia w interpretacji wszelkie dane liczbowe.  
  
 `refiid`  
 [in] IID jest przekazywany do filtrowania modułu wyliczającego. Identyfikator IID jest jednym z `IDebugPropertyEnumType` interfejsów, które dziedziczą z `IDebugPropertyEnumType_All`.  
  
 `ppEnum`  
 [out] Zwraca `IEnumDebugPropertyInfo` interfejs, który wylicza właściwości elementu członkowskiego.  
  
## <a name="return-value"></a>Wartość zwracana  
 Zwraca prawidłową `HRESULT`, zazwyczaj `S_OK`.  
  
## <a name="see-also"></a>Zobacz też  
 [Interfejs IDebugProperty](../../winscript/reference/idebugproperty-interface.md)   
 [DBGPROP_INFO_FLAGS](../../winscript/reference/dbgprop-info-flags.md)   
 [Interfejs IDebugPropertyEnumType_All](../../winscript/reference/idebugpropertyenumtype-all-interface.md)   
 [IEnumDebugPropertyInfo, interfejs](../../winscript/reference/ienumdebugpropertyinfo-interface.md)