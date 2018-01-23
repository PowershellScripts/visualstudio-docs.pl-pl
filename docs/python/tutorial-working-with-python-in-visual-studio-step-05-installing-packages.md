---
title: "Praca z języka Python w programie Visual Studio w kroku 5, instalowanie pakietów | Dokumentacja firmy Microsoft"
description: "Krok 5 podstawowy samouczek do pracy z języka Python w programie Visual Studio, prezentacja programu Visual Studio funkcje zarządzania pakietami w środowisku Python."
ms.custom: 
ms.date: 01/16/2018
ms.reviewer: 
ms.suite: 
ms.technology: devlang-python
ms.devlang: python
ms.tgt_pltfrm: 
ms.topic: get-started-article
caps.latest.revision: "1"
author: kraigb
ms.author: kraigb
manager: ghogen
ms.workload:
- python
- data-science
ms.openlocfilehash: 4e7779b1ad7ee2725d92874756230ff04e633fee
ms.sourcegitcommit: bd16e764134c436d2d2f46490f51234d5246ee50
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/22/2018
---
# <a name="step-5-installing-packages-in-your-python-environment"></a>Krok 5: Instalowanie pakietów w środowisku Python

**Poprzedni krok: [uruchamianie kodu w debugerze](tutorial-working-with-python-in-visual-studio-step-04-debugging.md)**

Społeczność deweloperów języka Python ma wyprodukowanych tysiące przydatne pakiety, które można zastosować do własnych projektów. Program Visual Studio udostępnia interfejs użytkownika w zakresie zarządzania pakietami w Twoim środowisku Python.

1. Wybierz **Widok > inne okna > środowiska Python** polecenia menu. **Środowiska Python** okno otwiera jako element równorzędny do Eksploratora rozwiązań i przedstawia różnych środowiskach dostępne dla Ciebie. Lista zawiera obu środowiskach, które zostały zainstalowane za pomocą Instalatora programu Visual Studio i tych, które należy zainstalować osobno. Środowisko pogrubione to domyślnego środowiska, który jest używany dla nowych projektów.

  ![Okno środowiska Python](media/environments-default-view-blue.png)

1. W środowisku **omówienie** kartę zapewnia szybki dostęp do interaktywnego okna dla tego środowiska wraz z folderu instalacji i tłumaczy w środowisku. Na przykład wybierz **Otwórz okno interaktywne** i interaktywnego okna dla tego w danym środowisku jest wyświetlana w programie Visual Studio.

1. Wybierz **pakiety** kartę i można wyświetlić listę pakietów, które są aktualnie zainstalowane w środowisku.

  ![Pakiety zainstalowane w środowisku](media/environments-installed-packages-blue.png)

1. Zainstaluj `matplotlib` wprowadzając jej nazwę w polu wyszukiwania, następnie wybierz pozycję`pip install`

  ![Instalowanie matplotlib w środowisku](media/environments-add-matplotlib1.png)

1. Jeśli zostanie wyświetlony monit, w tym celu należy wyrazić zgodę na podniesienia uprawnień.
 
1. Po zainstalowaniu pakietu zostanie wyświetlony w oknie środowiska Python. **X** z prawej strony pakietu odinstalowuje go. 

  ![Ukończenie instalacji matplotlib w środowisku](media/environments-add-matplotlib2.png)

  Pasek postępu małych poniżej środowiska wskazuje, że program Visual Studio tworzy bazę danych IntelliSense dla nowo zainstalowany pakiet. **IntelliSense** karta zawiera także szczegółowe informacje. Należy pamiętać, że przed zakończeniem tej bazy danych, funkcje IntelliSense, takie jak automatyczne uzupełnianie i sprawdzanie składni nie będzie aktywny w edytor dla tego pakietu.

1. Utwórz nowy projekt z **Plik > Nowy > Projekt**, wybierając szablon "Python aplikacji". W pliku kodu, który pojawia się Wklej następujący kod, który tworzy wave cosinus, takich jak poprzednich kroków samouczka tylko tym kreślone graficznie:

    ```python
    import numpy as np     # installed with matplotlib
    import matplotlib.pyplot as plt
    from math import radians

    def main():
        x = np.arange(0, radians(1800), radians(12))
        plt.plot(x, np.cos(x), 'b')
        plt.show()

    main()
    ```

1. Uruchom program z (F5) lub bez debugera (Ctrl + F5), aby wyświetlić dane wyjściowe:

  ![Dane wyjściowe przykład matplotlib](media/environments-add-matplotlib3.png)

## <a name="next-steps"></a>Następne kroki

> [!div class="nextstepaction"]
> [Praca z usługą Git](tutorial-working-with-python-in-visual-studio-step-06-working-with-git.md)

### <a name="going-deeper"></a>Przechodząc głębiej

- [Środowiska Python](managing-python-environments-in-visual-studio.md)