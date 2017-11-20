---
title: IDebugCoreServer3::EnableAutoAttach | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugCoreServer3::EnableAutoAttach
helpviewer_keywords: IDebugCoreServer3::EnableAutoAttach
ms.assetid: 06aa633b-263b-4e08-8844-9a52d5120b94
caps.latest.revision: "9"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 23c7faed077b8af442d81593808f9360995ba246
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idebugcoreserver3enableautoattach"></a>IDebugCoreServer3::EnableAutoAttach
Umożliwia automatyczne dołączanie aparatów określonego debugowania.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT EnableAutoAttach(  
   GUID*     rgguidSpecificEngines,  
   DWORD     celtSpecificEngines,  
   LPCOLESTR pszStartPageUrl,  
   BSTR*     pbstrSessionId  
);  
```  
  
```csharp  
int EnableAutoAttach(  
   Guid[]     rgguidSpecificEngines,  
   uint       celtSpecificEngines,  
   string     pszStartPageUrl,  
   out string pbstrSessionId  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `rgguidSpecificEngines`  
 [in] Tablica identyfikatory GUID dla każdego aparatu debugowania można oznaczyć jako dołączanie automatycznie.  
  
 `celtSpecificEngines`  
 [in] Liczba aparatów określone w `rgguidSpecificEngines`.  
  
 `pszStartPageUrl`  
 [in] Początkowy adres URL do użycia podczas podłączania automatycznie.  
  
 `pbstrSessionID`  
 [out] Identyfikator sesji, który był dołączony automatycznie.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu. Jeden kod błędu: `E_AUTO_ATTACH_NOT_REGISTERED`, co oznacza, że fabryka klas auto-attach nie został zarejestrowany.  
  
## <a name="remarks"></a>Uwagi  
 Po uruchomieniu program skojarzony z określonym adresem URL aparatami debugowania określonego zostaną automatycznie uruchomione i dołączony.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugCoreServer3](../../../extensibility/debugger/reference/idebugcoreserver3.md)