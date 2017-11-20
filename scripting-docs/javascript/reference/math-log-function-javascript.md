---
title: "Math.log — funkcja (JavaScript) | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 01/18/2017
ms.prod: windows-client-threshold
ms.reviewer: 
ms.suite: 
ms.technology: devlang-javascript
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords: log
dev_langs:
- JavaScript
- TypeScript
- DHTML
helpviewer_keywords:
- log method
- Math object
ms.assetid: 5d617fb5-4b27-404e-842f-eea5549a7c1a
caps.latest.revision: "9"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 62bfb6bf9bb95b541a51224af4484ded22ccb4e8
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2017
---
# <a name="mathlog-function-javascript"></a>Math.log — Funkcja (JavaScript)
Zwraca logarytm naturalny (podstawowy `e`) dla danej liczby.  
  
## <a name="syntax"></a>Składnia  
  
```  
Math.log(number)   
```  
  
#### <a name="parameters"></a>Parametry  
 liczba  
 Liczba.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli `number` jest dodatnia, funkcja zwraca logarytm naturalny liczby. Jeśli `number` jest ujemna, funkcja zwraca `NaN`. Jeśli `number` ma wartość 0, ta funkcja zwraca `-Infinity`.  
  
## <a name="example"></a>Przykład  
 Poniższy kod przedstawia sposób użycia tej funkcji.  
  
```JavaScript  
var numArr = [ 45.3, 69.0, 557.04, 0.222 ];  
  
for (i in numArr) {  
    document.write(Math.log(numArr[i]));  
    document.write("<br/>");  
}  
  
// Output:   
// 3.8133070324889884  
// 4.23410650459726  
// 6.322637050634291  
// -1.5050778971098575  
```  
  
## <a name="requirements"></a>Wymagania  
 [!INCLUDE[jsv1](../../javascript/misc/includes/jsv1-md.md)]  
  
 **Dotyczy**: [Math — obiekt](../../javascript/reference/math-object-javascript.md)  
  
## <a name="see-also"></a>Zobacz też  
 [Math.SQRT — funkcja](../../javascript/reference/math-sqrt-function-javascript.md)