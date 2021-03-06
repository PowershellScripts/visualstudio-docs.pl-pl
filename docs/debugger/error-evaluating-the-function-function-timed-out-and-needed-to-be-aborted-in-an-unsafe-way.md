---
title: 'Błąd: Obliczenie funkcji &#39;funkcja&#39; przekroczyła limit czasu i konieczne było przerwanie procesu w niebezpieczny sposób | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/04/2016
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.unsafe_func_eval_abort
ms.technology: vs-ide-debug
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 1f36e56b2870d5f099a3b8ed95265fe7e2d688ff
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49934447"
---
# <a name="error-evaluating-the-function-39function39-timed-out-and-needed-to-be-aborted-in-an-unsafe-way"></a>Błąd: Obliczenie funkcji &#39;funkcja&#39; przekroczyła limit czasu i konieczne było przerwanie procesu w niebezpieczny sposób

Pełny tekst komunikatu: obliczania funkcji "function" przekroczyła limit czasu i konieczne było przerwanie procesu w niebezpieczny sposób. Może to uszkodzenia procesu docelowego. 

Aby ułatwić sprawdzić stan obiektów platformy .NET, debuger automatycznie wymusi debugowanego procesu do uruchomienia dodatkowych kodu (zwykle metody pobierającej właściwości i funkcji ToString). W większości przypadków wszystkie te funkcje są wykonywane szybko i znacznie ułatwia debugowanie. Debuger nie uruchamiać aplikację w piaskownicy. W rezultacie metoda pobierająca właściwości lub metody ToString, który wywołuje w funkcji natywnej, która jest używana z może prowadzić do długie limity czasu, który może nie być możliwe do odzyskania. Jeśli napotkasz ten komunikat o błędzie, ten błąd wystąpił.
 
Jednym z najczęstszych przyczyn tego problemu jest gdy debuger ocenia właściwością, tylko możliwość wątku poddawana do wykonania. Więc jeśli właściwość oczekuje na inne wątki były uruchomione w debugowanym aplikacji i oczekuje ono w taki sposób, że środowisko uruchomieniowe platformy .NET nie jest w stanie przerwania, ten problem będzie się zdarzyć.
 
## <a name="to-correct-this-error"></a>Aby poprawić ten błąd
 
Istnieją trzy możliwe rozwiązania tego problemu.
 
### <a name="solution-1-prevent-the-debugger-from-calling-the-getter-property-or-tostring-method"></a>Rozwiązanie #1: Zapobiega debuger wywołanie metody pobierającej właściwości lub metody ToString
 
Komunikat o błędzie informuje o nazwę funkcji, w której debuger próbował wywołać. Jeśli zmodyfikujesz tę funkcję, można uniemożliwić wywołanie metody pobierającej właściwości lub metody ToString debugera. Wypróbuj jedną z następujących czynności:
 
* Zmienić metodę na inny rodzaj kodu oprócz pobierającą właściwość lub metoda ToString i problem znikną.
    —lub—
* (W przypadku ToString) Zdefiniuj atrybut DebuggerDisplay od typu, i może mieć debugera coś innego niż ToString oceny.
    —lub—
* (Dla metody pobierającej właściwości) Umieść `[System.Diagnostics.DebuggerBrowsable(DebuggerBrowsableState.Never)]` atrybutu dla właściwości. Może to być przydatne, jeśli masz metodę, która musi znajdować się właściwości interfejsu API ze względu na zgodność, ale należy go tak naprawdę metody.
 
### <a name="solution-2-have-the-target-code-ask-the-debugger-to-abort-the-evaluation"></a>Rozwiązanie #2: Mieć kod docelowej, poproś debugera, aby przerwać oceny
 
Komunikat o błędzie informuje o nazwę funkcji, w której debuger próbował wywołać. Jeśli metoda pobierająca właściwości lub metody ToString niepowodzenia by działała poprawnie, szczególnie w sytuacjach, gdy ten problem, które jest kod wymaga innego wątku, aby uruchomić kod, a następnie wywołać funkcję implementacji `System.Diagnostics.Debugger.NotifyOfCrossThreadDependency` poprosić debugera do przerwania funkcji Ocena. Za pomocą tego rozwiązania jest nadal możliwe jawnie ocenić tych funkcji, ale domyślne zachowanie to, zatrzyma wykonywanie po wystąpieniu wywołania NotifyOfCrossThreadDependency.
 
### <a name="solution-3-disable-all-implicit-evaluation"></a>Rozwiązanie #3: Wyłącz wszystkie bezwarunkowa ocena
 
Jeśli poprzednie rozwiązania nie rozwiązują problemu, przejdź do strony *narzędzia* > *opcje*i usuń zaznaczenie opcji *debugowanie*  >   *Ogólne* > *Włącz obliczanie właściwości i inne niejawne wywołania funkcji*. To spowoduje wyłączenie większość Obliczanie funkcji niejawnie i powinno rozwiązać problem.



  
