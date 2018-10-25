---
title: Oczekiwano obiektu wyliczenia | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-client-threshold
ms.reviewer: ''
ms.suite: ''
ms.technology:
- javascript
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- VS.WebClient.Help.SCRIPT5015
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: dc6e32c1-a6e6-4e12-ac99-e3f65f91c8d7
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 485e6e387f07fd3a54727f5f8e08c0a00743c6d9
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49935851"
---
# <a name="enumerator-object-expected"></a>Oczekiwano obiektu wyliczenia
Podjęto próbę wywołania **Enumerator.prototype.atEnd, Enumerator.prototype.item, Enumerator.prototype.moveFirst,** lub **Enumerator.prototype.moveNext** metody na obiekt typu innych niż `Enumerator`. Obiekt tego typu wywołania musi być typu `Enumerator`. Poniżej przedstawiono przykładowy kod, która narusza tę regułę:  
  
```JavaScript  
var o = new Object;  
o.f = Enumerator.prototype.atEnd;  
o.f();  
```  
  
### <a name="to-correct-this-error"></a>Aby poprawić ten błąd  
  
-   Tylko wywołania **Enumerator.prototype.atEnd**, **Enumerator.prototype.item**, **Enumerator.prototype.moveFirst**, lub  **Enumerator.prototype.moveNext** metod obiektów typu `Enumerator`. Aby sprawdzić, czy obiekt jest `Enumerator` obiektu, należy użyć:  
  
    ```  
    if(x instanceof Enumerator)  
    ```  
  
## <a name="see-also"></a>Zobacz też  
 [Enumerator, obiekt](../../javascript/reference/enumerator-object-javascript.md)