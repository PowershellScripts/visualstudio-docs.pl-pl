---
title: IDebugEnumField::GetValueFromString | Dokumentacja firmy Microsoft
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
- IDebugEnumField::GetValueFromString
helpviewer_keywords:
- IDebugEnumField::GetValueFromString method
ms.assetid: 1ef8ac5e-a3e0-4078-b876-7f5615aedcbb
caps.latest.revision: 8
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: c99c163eef122de65a15a43b5244ac2644f7618c
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49277010"
---
# <a name="idebugenumfieldgetvaluefromstring"></a>IDebugEnumField::GetValueFromString
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Ta metoda zwraca wartość skojarzoną z nazwą stała wyliczenia.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
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

