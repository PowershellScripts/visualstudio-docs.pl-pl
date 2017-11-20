---
title: "Format — właściwość (Intl.NumberFormat) | Dokumentacja firmy Microsoft"
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
ms.assetid: 68c3223a-023c-4fa0-aa99-d049a7a0e26a
caps.latest.revision: "5"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: be40f8e94220ad7504dd3b9736e71b3416bb3d2a
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2017
---
# <a name="format-property-intlnumberformat"></a>format — Właściwość (Intl.NumberFormat)
Zwraca funkcję, która formatuje liczbę ustawień regionalnych przy użyciu określonego numeru ustawień programu formatującego.  
  
## <a name="syntax"></a>Składnia  
  
```  
numberFormatObj.format  
```  
  
#### <a name="parameters"></a>Parametry  
 `numberFormatObj`  
 Wymagany. Nazwa `NumberFormat` obiekt ma być używany jako elementu formatującego.  
  
## <a name="remarks"></a>Uwagi  
 Funkcja zwrócony przez `format` właściwość przyjmuje jeden argument `value`i zwraca ciąg reprezentujący liczbę zlokalizowanych przy użyciu określonego w opcji `NumberFormat` obiektu. Jeśli `value` nie zostanie podana, funkcja zwraca `NaN` (nie liczba).  
  
## <a name="example"></a>Przykład  
 W poniższym przykładzie użyto `NumberFormat` obiekt, aby utworzyć numer zlokalizowane.  
  
```JavaScript  
var nf = new Intl.NumberFormat(["en-US"], {  
    style: "currency",  
    currency: "CNY",  
    currencyDisplay: "symbol",  
    maximumFractionDigit: 1  
})  
  
if (console && console.log) {  
    console.log(nf.format(100)); // "¥100.00"  
}  
  
```  
  
## <a name="requirements"></a>Wymagania  
 [!INCLUDE[jsv11](../../javascript/reference/includes/jsv11-md.md)]  
  
## <a name="see-also"></a>Zobacz też  
 [Intl.numberformat — obiekt](../../javascript/reference/intl-numberformat-object-javascript.md)