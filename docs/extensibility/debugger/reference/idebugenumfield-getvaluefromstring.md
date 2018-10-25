---
title: IDebugEnumField::GetValueFromString | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugEnumField::GetValueFromString
helpviewer_keywords:
- IDebugEnumField::GetValueFromString method
ms.assetid: 1ef8ac5e-a3e0-4078-b876-7f5615aedcbb
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 86cf8b1421769ac9a4b302e0da3676d826b9bea6
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49942234"
---
# <a name="idebugenumfieldgetvaluefromstring"></a>IDebugEnumField::GetValueFromString
Ta metoda zwraca wartość skojarzoną z nazwą stała wyliczenia.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT GetValueFromString(  
   LPCOLESTR  pszValue,  
   ULONGLONG* pvalue  
);  
```  
  
```csharp  
int GetValueFromString(  
   string    pszValue,  
   out ulong pValue  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pszValue`  
 [in] Ciąg określający nazwę, dla którego ma zostać pobrana wartość. Należy pamiętać, że dla języka C++, jest to ciąg znaku dwubajtowego.  
  
 `pValue`  
 [out] Zwraca wartość liczbową skojarzoną.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca `S_FALSE`, jeśli nazwa nie jest częścią wyliczenia lub kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Ta metoda jest rozróżniana wielkość liter. Użyj razie wyszukiwanie bez uwzględniania wielkości liter (na przykład w języku, takie jak Visual Basic, których nazwy nie są z uwzględnieniem wielkości liter) [GetValueFromStringCaseInsensitive](../../../extensibility/debugger/reference/idebugenumfield-getvaluefromstringcaseinsensitive.md).  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugEnumField](../../../extensibility/debugger/reference/idebugenumfield.md)   
 [GetValueFromStringCaseInsensitive](../../../extensibility/debugger/reference/idebugenumfield-getvaluefromstringcaseinsensitive.md)