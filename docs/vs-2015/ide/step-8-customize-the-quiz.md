---
title: 'Krok 8: Dostosowywanie kwizu | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: dc8edb13-1b23-47d7-b859-8c6f7888c1a9
caps.latest.revision: 14
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 559bd2a1b908ab5b1590a2ec2dd71225020db79a
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49260146"
---
# <a name="step-8-customize-the-quiz"></a>Krok 8: Dostosowywanie kwizu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

W ostatniej części tego samouczka dowiesz się o kilka sposobów na dostosowywanie kwizu i rozszerzają co już znasz. Na przykład zastanów się, jak program stwarza problemy dzielenia losowych, w których odpowiedź jest nigdy nie ułamek. Aby dowiedzieć się więcej, należy wyłączyć `timeLabel` kontrolować różne kolory i przypisz quizu wskazówką.  
  
### <a name="to-customize-the-quiz"></a>Dostosowywanie kwizu  
  
-   Kiedy tylko pięć sekund pozostają w quizie, Włącz **timeLabel** kontrolować red przez ustawienie jego **BackColor** właściwości (`timeLabel.BackColor = Color.Red;`). Resetuj kolor po umieszczeniu quizu.  
  
-   Nadaj quizu wskazówką przez odtwarzanie dźwięku w momencie poprawną odpowiedź do formantu NumericUpDown. (Należy napisać program obsługi zdarzeń dla każdego formantu `ValueChanged()` zdarzenie, które są generowane w każdym przypadku, gdy osoba wypełniająca quiz zmienia wartość kontrolki.)  
  
### <a name="to-continue-or-review"></a>Aby kontynuować lub przeglądnąć  
  
-   Aby pobrać pełną wersję quizu, zobacz [przykładowy samouczek pełnej wersji quizu matematycznego](http://code.msdn.microsoft.com/Complete-Math-Quiz-8581813c).  
  
-   Aby przejść do następnego samouczka, zobacz [Tutorial 3: Create a Matching Game](../ide/tutorial-3-create-a-matching-game.md).  
  
-   Aby powrócić do poprzedniego kroku samouczka, zobacz [kroku 7: problemów dodawać mnożenia i dzielenia](../ide/step-7-add-multiplication-and-division-problems.md).



