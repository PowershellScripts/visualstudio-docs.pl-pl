---
title: "Używanie PyLint z kodem języka Python w programie Visual Studio | Dokumentacja firmy Microsoft"
description: "Jak używać PyLint w programie Visual Studio do sprawdzenie problemów w kodzie języka Python."
ms.custom: 
ms.date: 07/12/2017
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-python
ms.devlang: python
ms.tgt_pltfrm: 
ms.topic: article
caps.latest.revision: 
author: kraigb
ms.author: kraigb
manager: ghogen
ms.workload:
- python
- data-science
ms.openlocfilehash: 426e61144462e2421d593d7b05b0d547093c7147
ms.sourcegitcommit: ba29e4d37db92ec784d4acf9c6e120cf0ea677e9
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/01/2018
---
# <a name="using-pylint-to-check-python-code"></a>Przy użyciu PyLint w celu sprawdzenia kodu języka Python

[PyLint](https://www.pylint.org/), powszechnie używane narzędzie, które sprawdza błędów w kodzie języka Python i zachęca dobrej Python kodowania wzorców, jest zintegrowany z programu Visual Studio dla projektów języka Python.

Po prostu kliknij prawym przyciskiem myszy projekt języka Python w Eksploratorze rozwiązań i wybierz **Python > Uruchom PyLint...** :

![Polecenie PyLint w menu kontekstowym dla projektów języka Python](media/code-pylint-command.png)

Za pomocą tego polecenia monit o zainstalowanie PyLint do środowiska active, jeśli nie jest już istnieje.

PyLint ostrzeżenia i błędy są wyświetlane w oknie Lista błędów:

![Lista błędów PyLint](media/code-pylint-error-list.png)

Dwukrotne kliknięcie błąd przejście bezpośrednio do kodu źródłowego, który wygenerował problem.

> [!Tip]
> Zobacz [PyLint funkcji odwołanie](https://pylint.readthedocs.io/en/latest/technical_reference/features.html) szczegółową listę wszystkich PyLint komunikaty wyjściowe.

## <a name="setting-pylint-command-line-options"></a>Ustawianie opcji wiersza polecenia PyLint

[Opcje wiersza polecenia](https://pylint.readthedocs.io/en/latest/user_guide/run.html#command-line-options) części dokumentacji PyLint zawiera opis sposobu kontrolowania zachowania PyLint firmy za pośrednictwem `.pylintrc` pliku konfiguracji. Tego pliku można umieścić w folderze głównym projektu języka Python w programie Visual Studio lub w innym miejscu w zależności od tego, jak bardzo ma tych ustawień (zobacz [opcje wiersza polecenia](https://pylint.readthedocs.io/en/latest/user_guide/run.html#command-line-options) szczegółowe informacje).

Na przykład w celu pominięcia ostrzeżenia "Brak docstring" pokazano na poprzedniej ilustracji z `.pylintrc` pliku w projekcie, wykonaj kroki:

1. W wierszu polecenia przejdź do katalogu głównym projektu (która zawiera Twoje `.pyproj` plików) i uruchom następujące polecenie, aby wygenerować plik konfiguracji komentarze:

   ```command
   pylint --generate-rcfile > .pylintrc
   ```

1. W Eksploratorze rozwiązań programu Visual Studio, kliknij prawym przyciskiem myszy projekt, wybierz **Dodaj > Kończenie elementu...** , przejdź do i wybierz nową `.pylintrc` pliku, a następnie wybierz **Dodaj**.

1. Otwórz plik do edycji, który zawiera różne ustawienia, którymi można pracować z. Aby wyłączyć ostrzeżenia, zlokalizuj `[MESSAGES CONTROL]` sekcji, a następnie zlokalizuj `disable` ustawienie w tej sekcji. Brak ciąg z określonymi komunikatami, do których można dołączyć niezależnie od tego ostrzeżenia, które chcesz. W tym przykładzie należy dołączyć `,missing-docstring` (w tym oddzielania przecinkami).

1. Zapisz `.pylintrc` pliku i uruchom PyLint ponownie, aby zobaczyć, że ostrzeżenia teraz są pomijane.

> [!Tip]
> Aby użyć `.pylintrc` pliku z udziału sieciowego, Utwórz zmienną środowiskową o nazwie `PYLINTRC` wartość nazwy pliku w sieci udostępnianie przy użyciu ścieżki UNC ani litery dysku zmapowanego. Na przykład `PYLINTRC=\\myshare\python\.pylintrc`.