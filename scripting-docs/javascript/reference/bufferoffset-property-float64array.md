---
title: "bufferOffset właściwość (Float64Array) | Dokumentacja firmy Microsoft"
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
ms.assetid: 9b566ec9-97d1-4a54-96cd-c1608f0ed330
caps.latest.revision: "7"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a2d64af7d1f7aeb9f4f42ee1854c5a6a93ad5505
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2017
---
# <a name="bufferoffset-property-float64array"></a>bufferOffset Właściwość (Float64Array)
Tylko do odczytu. Ustalone podczas tworzenia przesunięcie (w bajtach) tej tablicy od początku jej ArrayBuffer.  
  
## <a name="syntax"></a>Składnia  
  
```JavaScript  
var arrayOffset = float64Array.byteOffset;  
```  
  
## <a name="example"></a>Przykład  
 Poniższy przykład pokazuje, jak pobrać przesunięcie tablicy.  
  
```JavaScript  
var req = new XMLHttpRequest();  
    req.open('GET', "http://www.example.com");  
    req.responseType = "arraybuffer";  
    req.send();  
  
    req.onreadystatechange = function () {  
        if (req.readyState === 4) {  
            var buffer = req.response;  
            var dataView = new DataView(buffer);  
            var floatArr = new Float64Array(buffer.byteLength / 8);  
            alert(floatArr.byteOffset);  
        }  
    }  
  
```  
  
## <a name="requirements"></a>Wymagania  
 [!INCLUDE[jsv10](../../javascript/reference/includes/jsv10-md.md)]