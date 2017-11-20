---
title: "Formatowanie kodu języka Python w programie Visual Studio | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 07/12/2017
ms.reviewer: 
ms.suite: 
ms.technology: devlang-python
ms.devlang: python
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 3d0f1631-360b-45d4-a0cb-01c3c10d25f2
caps.latest.revision: "1"
author: kraigb
ms.author: kraigb
manager: ghogen
ms.openlocfilehash: 8d693278eb9d60d690e797d4e14163495239cd31
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="formatting-python-code"></a>Formatowanie kodu języka Python

Visual Studio umożliwia sformatowanie szybki kod do dopasowania wstępnie skonfigurowane opcje formatowania.

- Aby sformatować zaznaczenia: Wybierz **Edytuj > Zaawansowane > Wybieranie formatu** lub naciśnij klawisze Ctrl + E, F.
- Aby sformatować cały plik: Wybierz **Edytuj > Zaawansowane > dokumentu w formacie** lub naciśnij klawisze Ctrl + E, D.

Opcje są ustawiane za pomocą **Narzędzia > Opcje > Edytor tekstu > Python > Formatowanie** i jego zagnieżdżonych karty i domyślnie są ustawione odpowiadające podzbiorem [8 program ten przewodnik po stylu](http://www.python.org/dev/peps/pep-0008/). **Ogólne** kartę Określa, kiedy stosowane jest formatowanie; trzy karty ustawienia zostały opisane w tym temacie.

[Python obsługi w programie Visual Studio](installation.md) dodaje również przydatne [wypełnienia akapitu komentarz](#fill-comment-paragraph-command) polecenie **Edytuj > Zaawansowane** menu zgodnie z opisem poniżej.

## <a name="spacing"></a>Odstępy

**Odstępy** kontrolki, w którym spacje są wstawiane lub usunąć wokół różnych konstrukcji języka. Każda opcja charakteryzuje się trzema możliwymi wartościami:

- Zaznaczony: gwarantuje, że zastosowano odstępów.
- Wyczyszczone: usuwa wszystkie odstęp.
- Nieokreślony: pozostawia oryginalne formatowanie miejscowej.

W poniższych tabelach znajdują się przykłady dla różnych opcji:

| Opcja definicji klasy | Zaznaczone | Wyczyszczone |
| --- | --- | --- | 
| Wstaw odstęp między nazwy deklaracji klasy oraz listę typów podstawowych | `class X (object): pass` | `class X(object): pass` | 
| Wstaw spację wewnątrz nawiasów listy zasad | `class X( object ): pass` | `class X(object): pass` |
| Wstaw spację wewnątrz nawiasów listy baz pusty | `class X( ): pass` | `class X(): pass` |

<br/>

| Definicje funkcji-opcja | Zaznaczone | Wyczyszczone |
| --- | --- | --- |
| Wstaw spację między nazwę deklaracji funkcji i listy parametrów | `def X (): pass` | `def X(): pass` | 
| Wstaw spację wewnątrz nawiasów listy parametrów | `def X( a, b ): pass` | `def X(a, b): pass` |
| Wstaw spację wewnątrz nawiasów pustej listy parametrów | `def X( ): pass` | `def X(): pass` |
| Wstawiaj odstępy dookoła "=" w wartości domyślne parametrów | `includes X(a = 42): pass` | `includes X(a=42): pass` |
| Wstaw spację przed i po operatorach adnotacji zwracanego | `includes X() -> 42: pass` | `includes X()->42: pass` |

<br/>

| Opcja operatory | Zaznaczone | Wyczyszczone |
| --- | --- | --- |
| Wstawiaj odstępy dookoła operatorów dwuargumentowych | `a + b` | `a+b` |
| Wstawiaj odstępy dookoła przypisania | `a = b` | `a=b` |

<br/>

| Opcja Odstępy wyrażenia | Zaznaczone | Wyczyszczone |
| --- | --- | --- |
| Wstaw spację między nazwę wywołanie funkcji i listy argumentów | `X ()` | `X()` |
| Wstaw spację wewnątrz nawiasów pustej listy argumentów | `X( )` | `X()` |
| Wstaw spację wewnątrz nawiasów listy argumentów | `X( a, b )` | `X(a, b)` |
| Wstaw spację wewnątrz nawiasów wyrażenia | `( a )` | `(a)` |
| Wstaw spację wewnątrz nawiasów pusty spójnej kolekcji. | `( )` | `()` |
| Wstaw spację wewnątrz nawiasów spójnej kolekcji | `( a, b )` | `(a, b)` |
| Wstaw spację wewnątrz pustych nawiasów kwadratowych | `[ ]` | `[]` |
| Wstaw spacje wewnątrz nawiasów kwadratowych list | `[ a, b ]` | `[a, b]` |
| Wstaw spację przed otwierającym nawiasem kwadratowym | `x [i]` | `x[i]` |
| Wstaw spację wewnątrz nawiasów kwadratowych | `x[ i ]` | `x[i]` |

<br/>

## <a name="statements"></a>Instrukcje

**Instrukcje** opcje umożliwiają kontrolowanie automatyczne ponowne zapisywanie różnych instrukcji w formularzach Pythonic więcej.

| Opcja | Przed formatowania | Po sformatowaniu |
| --- | --- | --- |
| Umieść zaimportowanych modułów w nowym wierszu | `import sys, pickle` | `import sys`<br/>`import pickle` |
| Usuń zbędne średnikami | `x = 42;` | `x = 42` |
| Umieść użycie wielu instrukcji w nowych wierszy | `x = 42; y = 100` | `x = 42`<br/>`y = 100` |


## <a name="wrapping"></a>Zawijanie

**Zawijanie** umożliwia ustawisz **maksymalna szerokość komentarz** (wartość domyślna to 80). Jeśli **zawijać komentarze, które są zbyt szerokie** opcja jest ustawiona, komentarze, aby nie przekroczyć tego maksymalną szerokość formatuje Visual Studio.

```python
# Wrapped to 40 columns
# There should be one-- and preferably
# only one --obvious way to do it.
```

```python
# Not-wrapped:
# There should be one-- and preferably only one --obvious way to do it.
```



## <a name="fill-comment-paragraph-command"></a>Wypełnij polecenie Akapit komentarza

**Edytuj > Zaawansowane > wypełnienia akapitu komentarz** (Ctrl + E, P) i który formatów komentarz tekstu, łączenie krótkich wierszy ze sobą i podzielenie długo z nich.

Na przykład:

```python
# foo 
# bar
# baz
```

zmiany:

```python
# foo bar baz
```

```python
# This is a very long long long long long long long long long long long long long long long long long long long comment
```

zmiany:

```python
# This is a very long long long long long long long long long long long long
# long long long long long long long comment
```