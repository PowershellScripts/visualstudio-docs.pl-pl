---
title: Okno dialogowe Zaawansowane ustawienia (Concurrency Visualizer) | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.cv.settings
ms.assetid: bb3d90aa-5f08-4953-9be0-be6cea11633d
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 60f4a038056d326cfb184cc3bb6876c411263ca1
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49884007"
---
# <a name="advanced-settings-dialog-box-concurrency-visualizer"></a>Okno dialogowe Zaawansowane ustawienia (Concurrency Visualizer)
Za pomocą **Zaawansowane ustawienia** okno dialogowe w Wizualizatorze współbieżności można kontrolować, jak zbierane są dane śledzenia.  Okno dialogowe zawiera karty dla symboli, tylko mój kod, buforowanie, filtrowania, CLR zdarzenia, znaczniki, dostawców i plików.  
  
## <a name="symbols"></a>Symbole  
 Narzędzie Concurrency Visualizer używa tych samych ustawień symboli jako debugera programu Visual Studio. Wizualizator współbieżności używa ustawienia do rozpoznawania stosy wywołań, które są skojarzone z danymi wydajności.  Podczas przetwarzania śladów, Concurrency Visualizer uzyskuje dostęp do serwerów symboli, które są określone na stronie ustawień.  W przypadku tych danych jest dostępny za pośrednictwem sieci, śledzenia przetwarzania działa wolniej.  Aby zmniejszyć ilość czasu, które są wymagane do rozwiązania symboli, można buforować symbole lokalnie. Jeśli pobrano symbole, Visual Studio załaduje je z lokalnej pamięci podręcznej.  
  
## <a name="just-my-code"></a>Tylko mój kod  
 Domyślnie tylko mój kod jest zestaw. *exe* i. *Biblioteka DLL* pliki, które są skojarzone z bieżącego rozwiązania w programie Visual Studio. Narzędzie Concurrency Visualizer ocenia to zbiór plików, gdy używasz funkcji tylko mój kod do filtrowania stosy wywołań. Na karcie tylko mój kod możesz dodać katalogi, które zawierają. *exe* i. *Biblioteka DLL* pliki do lokalizacji, które narzędzie Concurrency Visualizer używa tylko mój kod.  
  
 Ścieżki. *exe* i. *Biblioteka DLL* pliki są przechowywane w pliku śledzenia podczas zbierania śladu.  Zmiana tego ustawienia nie wpływa na wszystkie wcześniej zebrane ślady.  
  
## <a name="buffering"></a>buforowanie  
 Narzędzie Concurrency Visualizer używa śledzenie zdarzeń dla Windows (ETW), gdy zbiera śledzenia.  ETW używa różnych buforów przechowuje zdarzenia.  Domyślne ustawienia bufora ETW. może nie być optymalny we wszystkich przypadkach, a w niektórych przypadkach, może spowodować problemy, takie jak zdarzenia utracone.  Karta buforowanie można skonfigurować ustawienia bufora ETW. Aby uzyskać więcej informacji, zobacz [śledzenie zdarzeń](http://go.microsoft.com/fwlink/?LinkId=234579) i [struktury EVENT_TRACE_PROPERTIES](http://go.microsoft.com/fwlink/?LinkId=234580).  
  
## <a name="filter"></a>Filtr  
 Na karcie Filtr można wybrać zestaw zdarzeń, które zbiera dane narzędzia Concurrency Visualizer. Wybranie podzbioru zdarzeń ogranicza typy danych, które są wyświetlane w raportach, zmniejsza rozmiar każdego śledzenia i skraca czas wymagany do przetwarzania śladów.  
  
### <a name="clr-events"></a>zdarzenia CLR  
 Zdarzenia generowane przez środowisko uruchomieniowe języka wspólnego (CLR) Włącz Concurrency Visualizer rozwiązać zarządzane stosy wywołań.  Po wyłączeniu zbierania zdarzeń CLR zmniejszy rozmiar śledzenia, ale niektóre stosy wywołań nie zostanie rozwiązany.  W rezultacie niektóre aktywności wątku procesora CPU może niepoprawnie pogrupowane.  
  
### <a name="collect-for-native-processes"></a>Zbierz dla natywnych procesów  
 Domyślnie zdarzenia CLR są zbierane tylko wtedy, gdy proces zarządzany jest profilowana, ponieważ są one zazwyczaj konieczne w przypadku natywnych procesów.  W niektórych przypadkach (na przykład, gdy macierzysty proces jest hostowany jest aparat CLR) może być służąca do gromadzenia zdarzeń CLR dla natywnych procesów.  Jeśli jest to możliwe, wybierz opcję **Zbierz dla natywnych procesów** pole wyboru.  
  
### <a name="disable-rundown-events"></a>Wyłącz zdarzenia uwalniania  
 Środowisko CLR generuje zdarzenia na podstawie dwóch dostawców: środowiska uruchomieniowego i podsumowania.  Jeśli chcesz zbierać zdarzenia środowiska uruchomieniowego CLR, ale chcemy uniknąć zbierania zdarzeń podsumowania, wybierz **wyłączyć zdarzenia podsumowania** pole wyboru.  Zmniejsza rozmiar pliku śledzenia, który jest generowany przez kolekcji, ale niektóre stosów może nie rozwiązać. Aby uzyskać więcej informacji, zobacz [dostawcy ETW CLR](/dotnet/framework/performance/clr-etw-providers)  
  
### <a name="sample-events"></a>Przykładowe zdarzenia  
 Zbieraj stosy wywołań, które są skojarzone z wykonywaniem wątków umożliwia próbkowane zdarzenia. Te zdarzenia są zbierane w około raz na milisekundę dla wątków, które są wykonywane w bieżącym procesie. Po wyłączeniu zbierania próbkowane zdarzenia zmniejszany jest rozmiar zbieranego śladu, ale nie można przeglądać wszystkie stosy wywołań, które są skojarzone z wykonywaniem wątków.  
  
### <a name="gpu-events"></a>Zdarzenia procesora GPU  
 Zdarzenia procesora GPU są zdarzeniami generowanymi przez DirectX. Jeśli wyłączysz zbieranie zdarzeń procesora GPU, zmniejszany jest rozmiar zbieranego śladu, ale nie można wyświetlić wszystkie aktywności procesora GPU w widok użycia lub aktywności aparatu DirectX w widoku wątków.  
  
### <a name="file-io-events"></a>Zdarzenia We/Wy plików  
 Zdarzenia We/Wy pliku reprezentują uzyskuje dostęp do dysku w imieniu bieżącego procesu.  Po wyłączeniu zdarzenia We/Wy pliku zmniejszany jest rozmiar śledzenia, ale Widok wątków ani zgłaszać żadnych informacji o dysku kanałów lub operacje dyskowe.  
  
## <a name="markers"></a>Znaczniki  
 Na **znaczniki** karcie, można skonfigurować zbiór dostawcy ETW, które są wyświetlane jako znaczników w Wizualizatorze współbieżności.  Można również filtrować kolekcji znaczników na podstawie poziomu ważności i kategorii funkcji ETW.  Jeśli używasz [SDK narzędzia Concurrency Visualizer](../profiling/concurrency-visualizer-sdk.md) się przy użyciu własnego dostawcę znaczników narzędzia, możesz ją tutaj zarejestrować tak, aby była wyświetlana w widoku wątków.  
  
### <a name="add-a-new-provider"></a>Dodaj nowego dostawcę  
 Jeśli kod używa [SDK narzędzia Concurrency Visualizer](../profiling/concurrency-visualizer-sdk.md) lub generuje zdarzenia ETW, które należy wykonać <xref:System.Diagnostics.Tracing.EventSource> Konwencji, można wyświetlić te zdarzenia w Wizualizatorze współbieżności, rejestrując je w oknie dialogowym.  
  
 W **nazwa** wprowadź nazwę, która opisuje typy zdarzeń, które są generowane przez dostawcę.  W **GUID** wprowadź identyfikator GUID, który jest skojarzony z tym dostawcą. (Identyfikator GUID jest skojarzony z każdego dostawcy funkcji ETW).  
  
 Opcjonalnie można określić, czy odfiltrowywać zdarzenia z tego dostawcy, w oparciu o kategorię lub poziom ważności.  Można użyć kategorii pola do filtrowania na podstawie SDK narzędzia Concurrency Visualizer kategorii.  Aby to zrobić, należy wprowadzić ciągów rozdzielanych przecinkami, kategorii lub zakresy kategorii.  To ustawienie określa kategorie zdarzeń w bieżącym dostawcy, aby pokazać.  W przypadku dodawania <xref:System.Diagnostics.Tracing.EventSource> dostawcy, można użyć pola kategorii do filtrowania według słów kluczowych funkcji ETW.  Ponieważ słowo kluczowe jest maską bitów, można użyć ciąg liczb całkowitych rozdzielonych przecinkami, aby określić, które bity maski są ustawione. Na przykład "1,2" ustawia bity pierwszego i drugiego, a przekłada się to 6 w zapisie dziesiętnym.  
  
 Lista poziom ważności można użyć do filtrowania zdarzeń, które mają znaczenie lub poziom funkcji ETW, która jest mniejsza niż określona wartość.  
  
### <a name="configure-an-existing-provider"></a>Konfigurowanie istniejącego dostawcy  
 Aby edytować ustawienia, które są skojarzone z istniejącego dostawcy, wybierz z listy, a następnie wybierz **dostawcy edycji** przycisku.  Można zmienić nazwę, identyfikator GUID i ustawienia filtrowania.  
  
### <a name="filter-marker-data-out-of-concurrency-visualizer-reports"></a>Filtruj dane znacznika poza raporty Concurrency Visualizer  
 Jeśli nie chcesz, aby dane dotyczące określonego dostawcy się pojawić w przyszłości śledzenia, wyczyść pole wyboru obok dostawcy, który chcesz usunąć.  
  
## <a name="files"></a>Pliki  
 Na **pliki** karcie, można określić katalog, w obszarze śledzenia pliki są przechowywane każdorazowo śledzenia są zbierane.  Narzędzie Concurrency Visualizer generuje cztery pliki do każdego śledzenia, które są zbierane:  
  
- Plik dziennika (ETL) śledzenia zdarzeń w trybie jądra (<em>.</em> Kernel.etl*)  
  
- Plik dziennika śledzenia zdarzeń tryb użytkownika (<em>.</em> User.etl*)  
  
- Plik dane narzędzia Concurrency Visualizer (<em>.</em> CVData*)  
  
- Plik śladu wizualizatora współbieżności (<em>.</em> CVTrace*)  
  
  Dwa pliki ETL przechowywanie danych pierwotnych śledzenia, a te dwa pliki narzędzia Concurrency Visualizer magazynowanie przetworzonych danych.  Nieprzetworzone pliki ETL zwykle nie są używane po przetworzeniu śledzenia.  Wybieranie **pliki usunąć zdarzenia śledzenia dziennika (ETL) po przeprowadzeniu analizy** pole wyboru pozwala na zmniejszenie ilości danych śledzenia, który jest przechowywany na dysku.  
  
## <a name="see-also"></a>Zobacz także  
 [Tylko mój kod](../profiling/just-my-code-threads-view.md)   
 [Znaczniki CONCURRENCY Visualizer](../profiling/concurrency-visualizer-markers.md)