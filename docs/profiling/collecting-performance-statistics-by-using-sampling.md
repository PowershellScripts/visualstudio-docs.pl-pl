---
title: "Zbieranie statystyk wydajności za pomocą metody pobierania próbek | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- Profiling Tools,sampling
- sampling profiling method
ms.assetid: 8e36361b-bb3d-40c6-b286-0e68c0ecb915
caps.latest.revision: "21"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 2e66566160f458a34c069d1025f9bab311a2f5ec
ms.sourcegitcommit: 26419ab0cccdc30d279c32d6a841758cfa903806
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/11/2017
---
# <a name="collecting-performance-statistics-by-using-sampling"></a>Zbieranie statystyk wydajności za pomocą metody pobierania próbek
Domyślnie [!INCLUDE[vsPreShort](../code-quality/includes/vspreshort_md.md)] metody próbkowania w narzędziach profilowania zbiera informacje dotyczące profilowania co 10 000 000 cykli procesora (około co setną sekundy na komputerze, 1 GHz). Metody pobierania próbek jest przydatne w przypadku znalezienia problemy dotyczące użycia procesora i Sugerowane metody uruchamiania większości dochodzenia wydajności.  
  
 **Wymagania**  
  
-   [!INCLUDE[vsUltLong](../code-quality/includes/vsultlong_md.md)], [!INCLUDE[vsPreLong](../code-quality/includes/vsprelong_md.md)], [!INCLUDE[vsPro](../code-quality/includes/vspro_md.md)]  
  
> [!NOTE]
>  Ulepszone funkcje zabezpieczeń w systemie Windows 8 i Windows Server 2012 wymagane znaczących zmian w sposobie profilera Visual Studio zbiera dane na tych platformach. Aplikacje platformy uniwersalnej systemu Windows wymagają również nowe techniki kolekcji. Zobacz [narzędzi wydajności w przypadku aplikacji systemu Windows 8 i Windows Server 2012](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).  
  
 Metoda pobierania próbek można określić za pomocą jednej z następujących procedur:  
  
-   Na pierwszej stronie kreatora profilowania, kliknij przycisk **próbkowania procesora CPU (zalecane)**.  
  
-   Na **Eksplorator wydajności** paska narzędzi w **metody** kliknij **próbkowania**.  
  
-   Na **ogólne** strony okna dialogowego właściwości sesji wydajności, kliknij przycisk **próbkowania**.  
  
## <a name="common-tasks"></a>Typowe zadania  
 Możesz określić dodatkowe opcje w *sesji wydajności***strony właściwości** okno dialogowe sesji wydajności. Aby otworzyć okno dialogowe:  
  
-   W **Eksplorator wydajności**, kliknij prawym przyciskiem myszy nazwę sesji wydajności, a następnie kliknij przycisk **właściwości**.  
  
 Zadania w poniższej tabeli opisano opcje, które można określić w *sesji wydajności***strony właściwości** okno dialogowe, gdy profilu przy użyciu metody pobierania próbek.  
  
|Zadanie|Zawartość pokrewna|  
|----------|---------------------|  
|Na **ogólne** strony, Dodaj alokacji pamięci .NET i zbieranie danych okres istnienia i określ szczegóły nazewnictwa profilowania wygenerowany plik danych (Vsp).|-   [Zbieranie alokacji pamięci .NET i okres istnienia obiektu](../profiling/collecting-dotnet-memory-allocation-and-lifetime-data.md)<br />-   [Porady: Ustawianie opcji nazwy pliku danych wydajności](../profiling/how-to-set-performance-data-file-name-options.md)|  
|Na **próbkowania** strony, zmienić częstotliwość próbkowania, Zmień zdarzenie próbkowania z cykli zegara procesora do innego licznika wydajności procesora lub zmienić jednocześnie.|-   [Porady: Wybieranie zdarzeń pobierania próbek](../profiling/how-to-choose-sampling-events.md)|  
|Na **uruchamianie** Określ aplikację do uruchomienia i rozpoczęcia zlecenia, jeśli masz wiele .exe projektów w rozwiązaniu kodu.|-   [Zbieranie danych o interakcji między warstwy](../profiling/collecting-tier-interaction-data.md)|  
|Na **interakcja warstwowa** Dodaj informacje o wywołaniach ADO.NET do danych zbieranych w theprofiling Uruchom.|-   [Zbieranie danych o interakcji między warstwy](../profiling/collecting-tier-interaction-data.md)|  
|Na **zdarzeń systemu Windows** Określ co najmniej jednego zdarzenia funkcji Śledzenie zdarzeń systemu Windows () do zbierania danych próbkowania.|-   [Porady: zbieranie zdarzeń śledzenia dla danych systemu Windows (ETW)](../profiling/how-to-collect-event-tracing-for-windows-etw-data.md)|  
|Na **liczników systemu Windows** strony, określ co najmniej jeden liczników wydajności systemu operacyjnego można dodać do danych profilowania jako znaczniki.|-   [Porady: zbieranie danych liczników systemu Windows](../profiling/how-to-collect-windows-counter-data.md)|  
|Na **zaawansowane** strony, określ wersję środowiska uruchomieniowego .NET Framework do profilowania, jeśli moduły aplikacji używać wielu wersji. Domyślnie jest profilowane pierwszej wersji załadowane.|-   [Porady: Określanie środowiska wykonawczego .NET Framework](../profiling/how-to-specify-the-dotnet-framework-runtime.md)|