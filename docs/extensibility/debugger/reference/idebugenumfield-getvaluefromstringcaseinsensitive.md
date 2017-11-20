---
title: IDebugEnumField::GetValueFromStringCaseInsensitive | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugEnumField::GetValueFromStringCaseInsensitive
helpviewer_keywords: IDebugEnumField::GetValueFromStringCaseInsensitive method
ms.assetid: ef95b38e-d9b2-4fb5-a166-7c2e14641dc7
caps.latest.revision: "8"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 8f1ff74931ac5433ff22330bc6f218315ccaf259
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idebugenumfieldgetvaluefromstringcaseinsensitive"></a>IDebugEnumField::GetValueFromStringCaseInsensitive
Ta metoda używa wyszukiwania bez uwzględniania wielkości liter w celu zwrócenia wartości skojarzone z nazwą stała wyliczenia.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT GetValueFromStringCaseInsensitive(  
   LPCOLESTR  pszValue,  
   ULONGLONG* pvalue  
);  
```  
  
```csharp  
int GetValueFromStringCaseInsensitive(  
   string    pszValue,   
   out ulong pValue  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pszValue`  
 [in] Ciąg określający nazwę, dla którego można uzyskać wartość. Należy pamiętać, że dla języka C++, jest to ciąg znaków dwubajtowych.  
  
 `pValue`  
 [out] Zwraca wartość skojarzoną wartość liczbową.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca `S_FALSE`, jeśli nazwa nie jest częścią wyliczenia lub kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Ta metoda jest rozróżniana wielkość liter. Jeśli wyszukiwanie nie jest konieczne (na przykład w języku C++, na którym jest rozróżniana wielkość liter nazwy np.), użyj [GetValueFromString](../../../extensibility/debugger/reference/idebugenumfield-getvaluefromstring.md).  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugEnumField](../../../extensibility/debugger/reference/idebugenumfield.md)   
 [GetValueFromString](../../../extensibility/debugger/reference/idebugenumfield-getvaluefromstring.md)