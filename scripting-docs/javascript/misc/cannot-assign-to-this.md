---
title: Nie można przypisać do &#39;to&#39; | Dokumentacja firmy Microsoft
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
- VS.WebClient.Help.SCRIPT5000
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: ba2b0a2b-f0f8-4698-b335-a4ab6c166671
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 47e55d39e85675b37d2ac9741d1207a9e81d369e
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49856655"
---
# <a name="cannot-assign-to-39this39"></a>Nie można przypisać do &#39;to&#39;
Próba przypisania wartości do **to**. **to** jest [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] — słowo kluczowe, która odwołuje się do albo:

- Obiekt metody, w trakcie wykonywania

- Obiekt globalny, jeśli nie istnieje metoda bieżącego (lub metoda nie należy do żadnego innego obiektu).

Metoda jest [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] funkcję wywoływaną za pomocą obiektu. Wewnątrz metody **to** — słowo kluczowe jest odwołanie do obiektu, metoda została wywołana przy użyciu (które akurat jest obiekt utworzony przez wywołanie konstruktora klasy za pomocą **nowe** operator).

Wewnątrz metody, można użyć **to** do odwoływania się do bieżącego obiektu, ale nie można przypisać nową wartość do **to**.

## <a name="to-correct-this-error"></a>Aby poprawić ten błąd

- Nie należy przypisywać **to**. Aby uzyskać dostęp do właściwości lub metody wystąpień obiektu, należy użyć operatora kropka (np. **circle.radius**).

  > [!NOTE]
  > Nie można nazwać zmienną użytkownik utworzył **to**; jest [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] słowa zarezerwowanego.

## <a name="see-also"></a>Zobacz też

- [this, instrukcja](../../javascript/reference/this-statement-javascript.md)
- [Rozwiązywanie problemów ze skryptami](../../javascript/advanced/troubleshooting-your-scripts-javascript.md)