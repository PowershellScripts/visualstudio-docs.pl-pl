---
title: IDebugProcessQueryProperties::QueryProperties | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: IDebugProcessQueryProperties::QueryProperties
ms.assetid: 976a9962-b689-45bb-afb6-16b2c5dbc3b8
caps.latest.revision: "5"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: c73cd73283a700d1e47ff5909d6c4ce7ec198714
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idebugprocessquerypropertiesqueryproperties"></a>IDebugProcessQueryProperties::QueryProperties
Ta — metoda zapytania dla określonej wartości debugowania procesu.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT QueryProperties(  
   ULONG                  celt,  
   PROCESS_PROPERTY_TYPE *rgdwPropTypes,  
   VARIANT               *rgtPropValues);  
```  
  
```csharp  
int QueryProperties(  
   uint                       celt,  
   enum_PROCESS_PROPERTY_TYPE rgdwPropTypes,  
   out object[ ]              rgtPropValues);  
```  
  
#### <a name="parameters"></a>Parametry  
 `celt`  
 [in] Rozmiar tablic zawierających definicji właściwości i wartości właściwości.  
  
 `dwPropType`  
 [in] Tablica zawiera definicje właściwości, którego dotyczy kwerenda. Możliwe wartości to:  
  
-   PROCESS_PROPERTY_COMMAND_LINE = 1  
  
-   PROCESS_PROPERTY_CURRENT_DIRECTORY = 2  
  
-   PROCESS_PROPERTY_ENVIRONMENT_VARIABLES = 3  
  
 `pvarPropValue`  
 [out] Tablica zawierająca wartości właściwości.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Ta metoda jest rzadko używana.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugProcessQueryProperties](../../../extensibility/debugger/reference/idebugprocessqueryproperties.md)