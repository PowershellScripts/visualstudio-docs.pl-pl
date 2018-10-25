---
title: Można&#39;ma &#39;podziału&#39; poza pętlą | Dokumentacja firmy Microsoft
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
- VS.WebClient.Help.SCRIPT1019
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: 11d02172-2a78-4705-a730-d21111db5f42
caps.latest.revision: 6
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: bb23f1bc3de087515cad9ba4910cf2ebaf640353
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49928558"
---
# <a name="can39t-have-39break39-outside-of-loop"></a>Można&#39;ma &#39;podziału&#39; poza pętlą
Podjęto próbę użycia **podziału** — słowo kluczowe poza pętlą. **Podziału** słowo kluczowe jest używane do zakończenia pętli lub `switch` instrukcji. Muszą być osadzone w treści pętli lub `switch` instrukcji. Jednak **etykiety** wykonać break — słowo kluczowe.  
  
```  
break labelname;  
```  
  
 Wystarczy etykietami formie **podziału** — słowo kluczowe podczas korzystania z zagnieżdżonej pętli lub `switch` instrukcji i potrzeb dotyczących zerwać pętlę, która nie jest to najbardziej.  
  
### <a name="to-correct-this-error"></a>Aby poprawić ten błąd  
  
-   Upewnij się, że **podziału** — słowo kluczowe pojawia się wewnątrz instrukcji otaczającej pętli lub przełącznika.  
  
## <a name="see-also"></a>Zobacz też  
 [BREAK — instrukcja](../../javascript/reference/break-statement-javascript.md)   
 [Sterowanie przepływem programu](../../javascript/controlling-program-flow-javascript.md)   
 [Rozwiązywanie problemów ze skryptami](../../javascript/advanced/troubleshooting-your-scripts-javascript.md)