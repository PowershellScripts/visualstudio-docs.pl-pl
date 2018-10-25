---
title: IDebugEnumField::GetStringFromValue | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugEnumField::GetStringFromValue
helpviewer_keywords:
- IDebugEnumField::GetStringFromValue method
ms.assetid: 5f95fd0c-fdce-497f-9f54-2ad8749494e9
caps.latest.revision: 6
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 08f518df68686e75ec1b1cc5141bfb24ea141183
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49819111"
---
# <a name="idebugenumfieldgetstringfromvalue"></a>IDebugEnumField::GetStringFromValue
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Ta metoda uzyskuje nazwę danego jej wartość stałej wyliczenia.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
HRESULT GetStringFromValue(  
   ULONGLONG value,  
   BSTR*     pbstrValue  
);  
```  
  
```csharp  
int GetStringFromValue(  
   ulong      value,  
   out string pbstrValue  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `value`  
 [in] Wartość, dla którego należy pobrać nazwę wyliczenia stałej.  
  
 `pbstrValue`  
 [out] Zwraca nazwę stała wyliczenia.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca `S_FALSE` Jeśli wartość nie ma skojarzonego nazwy lub zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Jeśli istnieje więcej niż jedną nazwę skojarzonej z taką samą wartość, zostanie zwrócony imię zdefiniowane w wyliczeniu.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugEnumField](../../../extensibility/debugger/reference/idebugenumfield.md)

