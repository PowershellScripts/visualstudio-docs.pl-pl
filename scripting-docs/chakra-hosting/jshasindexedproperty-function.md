---
title: "Jshasindexedproperty — funkcja | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 01/18/2017
ms.prod: windows-client-threshold
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: jsrt/JsHasIndexedProperty
helpviewer_keywords: JsHasIndexedProperty function
ms.assetid: 30436a3d-fda0-407e-aba2-142be2310372
caps.latest.revision: "12"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 786be053ee501f60c633cd4b93f7b73acaa9b68d
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2017
---
# <a name="jshasindexedproperty-function"></a>JsHasIndexedProperty — Funkcja
Sprawdza, czy obiekt ma wartość o określonym indeksie.  
  
## <a name="syntax"></a>Składnia  
  
```  
STDAPI_(JsErrorCode) JsHasIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _Out_ bool *result  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `object`  
 Obiekt do działania na.  
  
 `index`  
 Indeks do testowania.  
  
 `result`  
 Określa, czy obiekt ma wartość o określonym indeksie.  
  
## <a name="return-value"></a>Wartość zwracana  
 Kod `JsNoError` Jeśli operacja powiodła się, kod błędu w przeciwnym razie wartość.  
  
## <a name="remarks"></a>Uwagi  
 Wymaga kontekstu aktywnego skryptu.  
  
## <a name="requirements"></a>Wymagania  
 **Nagłówek:** jsrt.h  
  
## <a name="see-also"></a>Zobacz też  
 [Odwołanie (środowisko uruchomieniowe JavaScript)](../chakra-hosting/reference-javascript-runtime.md)