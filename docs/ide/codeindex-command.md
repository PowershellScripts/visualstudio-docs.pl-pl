---
title: Polecenie CodeIndex
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
helpviewer_keywords:
- command-line tools [Team Foundation Server]
- TFSConfig
- CodeIndex command [Team Foundation Server]
ms.assetid: b79568d4-6a64-4ca9-a1ee-3e57f92a9c5c
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 3f1169ff5bc9487fc062ab7cbc6e2adb01151a19
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49926153"
---
# <a name="codeindex-command"></a>Polecenie CodeIndex

Użyj **CodeIndex** polecenia do zarządzania indeksowaniem kodu na serwerze Team Foundation Server. Na przykład można zresetować indeks, aby naprawić informacje narzędzia CodeLens, lub wyłączyć indeksowanie, aby zbadać problemy z wydajnością serwera.

## <a name="required-permissions"></a>Wymagane uprawnienia

Aby użyć **CodeIndex** polecenia, musi być członkiem **Administratorzy Team Foundation** grupy zabezpieczeń. Zobacz [uprawnień i grup zdefiniowanych dla usługom DevOps platformy Azure i TFS](/azure/devops/organizations/security/permissions?view=vsts).

> [!NOTE]
> Nawet wtedy, gdy użytkownik loguje się przy użyciu poświadczeń administracyjnych, należy otworzyć podwyższone okno Wiersz polecenia, aby uruchomić to polecenie. Należy także uruchomić to polecenie z warstwy aplikacji programu Team Foundation.

## <a name="syntax"></a>Składnia

```cmd
TFSConfig CodeIndex /indexingStatus | /setIndexing:[ on | off | keepupOnly ] | /ignoreList:[ add | remove | removeAll | view ] ServerPath | /listLargeFiles [/fileCount:FileCount] [/minSize:MinSize] | /reindexAll | /destroyCodeIndex [/noPrompt] | /temporaryDataSizeLimit:[ view | <SizeInGBs> | disable ] | /indexHistoryPeriod:[ view | all | <NumberOfMonths> ] [/collectionName:CollectionName | /collectionId:CollectionId]
```

### <a name="parameters"></a>Parametry

|**Argument**|**Opis**|
|------------------| - |
|`CollectionName`|Określa nazwę kolekcji projektu. Jeśli nazwa zawiera spacje, należy ją ująć w cudzysłów, na przykład "Fabrikam Website".|
|`CollectionId`|Określa numer identyfikujący kolekcji projektu.|
|`ServerPath`|Określa ścieżkę do pliku kodu.|

|**Option**|**Opis**|
|----------------| - |
|**/indexingStatus**|Pokazuje stan i konfigurację usługi indeksowania kodu.|
|**/setIndexing:**[na &#124; poza &#124; keepupOnly]|-   **na**: Uruchom indeksowanie wszystkich zestawów zmian.<br />-   **Wyłącz**: Zatrzymaj indeksowanie wszystkich zestawów zmian.<br />-   **keepupOnly**: Zatrzymaj indeksowanie wcześniej utworzonych zestawów zmian i Rozpocznij indeksowanie tylko nowych zestawów zmian.|
|**/ignoreList:**[Dodaj &#124; Usuń &#124; removeAll &#124; view] `ServerPath`<br /><br /> Można użyć znaku wieloznacznego (*) na początku, zakończenia lub obu końcach ścieżki serwera.|Określa listę plików kodu i ich ścieżek, które nie mają być indeksowane.<br /><br /> -   **Dodaj**: Dodawanie pliku, który ma nie być indeksowany do listy plików ignorowanych.<br />-   **Usuń**: Usuń plik, który ma indeksowane z listy plików ignorowanych.<br />-   **removeAll**: Wyczyść listę ignorowanych plików i Rozpocznij indeksowanie wszystkich plików.<br />-   **Widok**: Zobacz wszystkie pliki, które nie są indeksowane.|
|**/listLargeFiles [/ fileCount:** `FileCount` **/minSize:** `MinSize`]|Przedstawia określoną liczbę plików, która przekracza określony rozmiar w KB. Następnie można użyć **/ignoreList** opcji, aby wykluczyć te pliki z indeksowania.|
|**/reindexAll**|Wyczyść wcześniej zaindeksowane dane i ponownie uruchom indeksowanie.|
|**/destroyCodeIndex [/noPrompt]**|Usuń indeks kodu i wszystkie indeksowane dane. Nie wymaga potwierdzenia, jeśli używasz **/noprompt** opcji.|
|**/temporaryDataSizeLimit**: [widok &#124; <`SizeInGBs`> &#124; wyłączone]|Kontrolowanie ile tymczasowe dane CodeLens tworzy podczas przetwarzania zmian. Domyślny limit wynosi 2 GB.<br /><br /> -   **Widok**: Pokaż bieżący limit rozmiaru.<br />-   `SizeInGBs`: Zmień limit rozmiaru.<br />-   **Wyłącz**: Usuń limit rozmiaru.<br /><br /> Ten limit jest sprawdzany przed CodeLens przetwarza nowy zestaw zmian. Jeśli dane tymczasowe przekracza ten limit, CodeLens spowoduje wstrzymanie przetwarzania ostatnie zestawy zmian, nie nowe. Funkcja CodeLens spowoduje ponowne uruchomienie przetwarzania po danych jest wyczyszczone, a spadnie poniżej tego limitu. Czyszczenie jest uruchamiany automatycznie raz dziennie. Oznacza to, że dane tymczasowe może przekroczyć tego limitu, dopóki oczyszczania zacznie działać.|
|**/indexHistoryPeriod**: [widok &#124; wszystkich &#124; <`NumberOfMonths`>]|Formant, jak długo indeksu historię zmian. Dotyczy to, ile historii CodeLens pokazuje. Domyślny limit to 12 miesięcy. Oznacza to rozwiązanie CodeLens Pokazuje historię zmian z ostatnich 12 miesięcy tylko.<br /><br /> -   **Widok**: Pokaż bieżącą liczbę miesięcy.<br />-   **wszystkie**: indeks cała historia zmian.<br />-   `NumberOfMonths`: Zmień liczbę miesięcy, używany do historii zmian indeksu.|
|**/collectionName:** `CollectionName`|Określa nazwę kolekcji projektu, na którym ma być uruchamiany **CodeIndex** polecenia. Wymagane, jeśli nie używasz **/CollectionId**.|
|**/collectionId:** `CollectionId`|Określa numer identyfikujący kolekcji projektu, na którym ma być uruchamiany **CodeIndex** polecenia. Wymagane, jeśli nie używasz **/CollectionName**.|

## <a name="examples"></a>Przykłady

> [!NOTE]
> Przykładowe firmy, organizacje, produkty, nazwy domen, adresy e-mail, logo, osoby, miejsca i zdarzenia wymienione w niniejszym dokumencie są fikcyjne.  Wszelkie rzeczywistą firmą, organizacji, produktu, nazwy domeny, adres e-mail, logo, osoby, miejsca lub zdarzeń jest przeznaczone i powinno być wnioskowane.

 Aby zobaczyć status indeksowania kodu i konfiguracji:

```cmd
TFSConfig CodeIndex /indexingStatus /collectionName:"Fabrikam Website"
```

 Aby rozpocząć indeksowanie wszystkich zestawów zmian:

```cmd
TFSConfig CodeIndex /setIndexing:on /collectionName:"Fabrikam Website"
```

 Aby zatrzymać indeksowanie wcześniej utworzonych zestawów zmian i Rozpocznij indeksowanie tylko nowych zestawów zmian:

```cmd
TFSConfig CodeIndex /setIndexing:keepupOnly /collectionName:"Fabrikam Website"
```

 Aby znaleźć do 50 plików, które są większe niż 10 KB:

```cmd
TFSConfig CodeIndex /listLargeFiles /fileCount:50 /minSize:10 /collectionName:"Fabrikam Website"
```

 Aby wykluczyć określony plik z indeksowania i dodać go do listy plików ignorowanych:

```cmd
TFSConfig CodeIndex /ignoreList:add "$/Fabrikam Website/Catalog.cs" /collectionName:"Fabrikam Website"
```

 Aby wyświetlić wszystkie pliki, które nie są indeksowane:

```cmd
TFSConfig CodeIndex /ignoreList:view
```

 Aby wyczyścić wcześniej indeksowane dane i ponownie uruchomić indeksowanie:

```cmd
TFSConfig CodeIndex /reindexAll /collectionName:"Fabrikam Website"
```

 Aby zapisać całą historię zmian:

```cmd
TFSConfig CodeIndex /indexHistoryPeriod:all /collectionName:"Fabrikam Website"
```

 Aby usunąć limit rozmiaru danych tymczasowych CodeLens i kontynuować indeksowanie niezależnie od rozmiaru danych tymczasowych:

```cmd
TFSConfig CodeIndex /temporaryDataSizeLimit:disable /collectionName:"Fabrikam Website"
```

 Aby usunąć indeks kodu z potwierdzeniem:

```cmd
TFSConfig CodeIndex /destroyCodeIndex /collectionName:"Fabrikam Website"
```

## <a name="see-also"></a>Zobacz także

- [Znajdowanie zmian w kodzie i innych elementów historii za pomocą wskaźników CodeLens](../ide/find-code-changes-and-other-history-with-codelens.md)
- [Zarządzanie konfiguracją serwera za pomocą TFSConfig](/tfs/server/ref/command-line/tfsconfig-cmd)