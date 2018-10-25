---
title: IDebugProperty::GetExtendedInfo | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugProperty.GetExtendedInfo
apilocation:
- scrobj.dll
helpviewer_keywords:
- IDebugProperty::GetExtendedInfo
ms.assetid: a989ade5-16d5-4ee6-8d8a-8dcbfad24034
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c66ea53bde17f2936567cd93ae0be166f35382ed
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49925545"
---
# <a name="idebugpropertygetextendedinfo"></a>IDebugProperty::GetExtendedInfo
Pobiera rozszerzone informacje dla właściwości.  
  
## <a name="syntax"></a>Składnia  
  
```  
HRESULT GetExtendedInfo (  
   ULONG  cInfos,  
   GUID*  rgguidExtendedInfo,  
   VARIANT* pExtendedInfo  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `cInfos`  
 [in] Liczba obiektów rozszerzonych informacji.  
  
 `rgguidExtendedInfo`  
 [in] Tablica `GUID`s jest przekazywana tak, aby wiele elementów rozszerzone informacje mogą być pobierane, w tym samym czasie.  
  
 `pExtendedInfo`  
 [out] Zwraca tablicę `VARIANT`s, którego można pobrać informacji o właściwości rozszerzonej.  
  
## <a name="return-value"></a>Wartość zwracana  
 Zwraca prawidłową `HRESULT`, zazwyczaj `S_OK`.  
  
## <a name="remarks"></a>Uwagi  
 Ten interfejs pobiera rozszerzone informacje dla tego obiektu. Interfejs API istnieje wyłącznie na potrzeby pobierania informacji, które nie jest przystosowany do pobierania przy użyciu `IDebugProperty::GetPropertyInfo`).  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugProperty, interfejs](../../winscript/reference/idebugproperty-interface.md)