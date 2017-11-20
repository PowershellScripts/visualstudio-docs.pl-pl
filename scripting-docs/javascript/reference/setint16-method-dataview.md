---
title: "setInt16 — metoda (DataView) | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 01/18/2017
ms.prod: windows-client-threshold
ms.reviewer: 
ms.suite: 
ms.technology: devlang-javascript
ms.tgt_pltfrm: 
ms.topic: language-reference
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: 901c6cf5-63fb-45bd-9ea8-185c1d892060
caps.latest.revision: "5"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 04ea20079c217d1aeef8456e9c81996661fed356
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2017
---
# <a name="setint16-method-dataview"></a>setInt16 — Metoda (DataView)
Ustawia wartość Int16 na określone przesunięcie bajtów od początku widoku. Brak bez wyrównania ograniczenia; wartości wielobajtowego może być ustawiona na dowolnym przesunięcie.  
  
## <a name="syntax"></a>Składnia  
  
```  
dataView.setInt16(byteOffset, value, littleEndian);   
```  
  
## <a name="parameters"></a>Parametry  
 `byteOffset`  
 Miejsce w buforze, w którym ma być pobrana wartość.  
  
 `value`  
 Wartość do ustawienia.  
  
 `littleEndian`  
 Opcjonalny. Jeśli wartość false lub niezdefiniowany powinna być zapisana wartość big-endian, w przeciwnym razie wartość little endian mają być zapisywane.  
  
## <a name="remarks"></a>Uwagi  
 Te metody zgłosić wyjątek, jeśli zapisują poza koniec widoku.  
  
## <a name="example"></a>Przykład  
 Poniższy przykład pokazuje, jak ustawić pierwszy Int16 w widoku danych.  
  
```JavaScript  
var req = new XMLHttpRequest();  
    req.open('GET', "http://www.example.com");  
    req.responseType = "arraybuffer";  
    req.send();  
  
    req.onreadystatechange = function () {  
        if (req.readyState === 4) {  
            var buffer = req.response;  
            var dataView = new DataView(buffer);  
            dataView.setInt16(0, 9);  
        }  
    }  
  
```  
  
## <a name="requirements"></a>Wymagania  
 [!INCLUDE[jsv10](../../javascript/reference/includes/jsv10-md.md)]