---
title: Opcje sesji wydajności ogólnej ustawienie | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.performance.property.general
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: d6c44435f69b5a94433081a518be14f8ffd1756e
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49834230"
---
# <a name="set-general-performance-session-options"></a>Ustawianie opcji sesji wydajności ogólnej

Można ustawić metod zbierania i profilowanie danych konwencje nazewnictwa dla sesji wydajności programu Visual Studio Profiling Tools **ogólne** strony okna dialogowego właściwości sesji wydajności. Aby otworzyć to okno dialogowe z **Eksplorator wydajności**, kliknij prawym przyciskiem myszy sesję wydajności, a następnie kliknij **właściwości**.

## <a name="choosing-data-collection-methods"></a>Wybieranie metody zbierania danych

Ustawianie metody podstawowej kolekcji, wybierając jedną z opcji w obszarze **kolekcja profilowania**. Opcje te są opisane, zgodnie z poniższą tabelą:

|||
|-|-|
|**Próbkowanie**. Metoda pobierania próbek zbiera informacje dotyczące profilowania w regularnych odstępach czasu. Ta metoda jest przydatna do znajdowania problemy dotyczące użycia procesora i jest metodą sugerowane na uruchamianie większości badania wydajności.|- [Zbieranie statystyk wydajności za pomocą metody pobierania próbek](../profiling/collecting-performance-statistics-by-using-sampling.md)|
|**Instrumentacja**. Metoda Instrumentacja wprowadza do kopii modułu profilowania kodu, który rejestruje każdego wpisu, zakończenia i wywołanie funkcji funkcje w module podczas uruchomienia profilowania. Ta metoda jest przydatne do zbierania informacji chronometrażu o sekcji kodu i zrozumienie wpływu na operacje wejścia i wyjścia na wydajność aplikacji.|- [Zbieranie szczegółowych danych o chronometrażu przy użyciu Instrumentacji](../profiling/collecting-detailed-timing-data-by-using-instrumentation.md)|
|**Współbieżność**. Metody współbieżności zbiera dane dla każdego zdarzenia, że bloki wykonywania kodu, takie jak kiedy wątek czeka na zablokowany dostęp do zasobu aplikacji ma zostać zwolniony. Ta metoda jest przydatna do analizowania aplikacji wielowątkowych.|- [Zbieranie danych współbieżności procesu i wątku](../profiling/collecting-thread-and-process-concurrency-data.md)|

 Może zbierać dane pamięci platformy .NET przy użyciu metody próbkowania i instrumentacji. Wybierz typ danych w ramach **profilowania pamięci środowiska .NET**.

|||
|-|-|
|**Zbierz informacje dotyczące alokacji obiektów platformy .NET**. Domyślnie dane obejmują liczbę i rozmiar istnienia przydzielonych obiektów. Zaznacz lub wyczyść to pole wyboru, aby włączyć lub wyłączyć zbieranie danych pamięci .NET. |- [Zbieranie alokacji pamięci .NET i okres istnienia obiektu](../profiling/collecting-dotnet-memory-allocation-and-lifetime-data.md)|
|**Również zbierać informacje dotyczące okresu istnienia obiektu platformy .NET**. Zaznacz to pole wyboru, aby dołączyć dane dotyczące generacje kolekcji wyrzucania elementów, które zostały użyte do odzyskania obiektów pamięci.|- [Zbieranie alokacji pamięci .NET i okres istnienia obiektu](../profiling/collecting-dotnet-memory-allocation-and-lifetime-data.md) |

 Stroną sesji profilowania pojawia się po uruchomieniu profil aplikacji, którym można wstrzymać, wznowić i zatrzymanie profilowania.

 ![Stronie sesji profilowania](../profiling/media/prof_profilingsessionpage.png "PROF_ProfilingSessionPage")

## <a name="set-profiling-data-file-options"></a>Ustawianie opcji pliku danych profilowania

|||
|-|-|
|**Raport**. Domyślnie plik profilowania (.vsp) danych o nazwie profilowanej aplikacji i znajduje się w folderze rozwiązania lub projektu. Ciąg daty jest również dołączana do nazwy, a zwiększona liczba jest dodawany do plików danych, które w przeciwnym razie byłyby takich samych nazwach. Te opcje można zmienić.|- [Porady: Ustawianie opcji nazwy pliku danych wydajności](../profiling/how-to-set-performance-data-file-name-options.md)|