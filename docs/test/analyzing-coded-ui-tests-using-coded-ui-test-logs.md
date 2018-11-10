---
title: Analizowanie kodowanych testów interfejsu użytkownika przy użyciu dzienników testu kodowanego interfejsu użytkownika w programie Visual Studio
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-test
ms.topic: conceptual
ms.author: gewarren
manager: douge
ms.workload:
- multiple
author: gewarren
ms.openlocfilehash: 7d743dd11b67c3883bad815b26234717f377ff57
ms.sourcegitcommit: 0a8ac5f2a685270d9ca79bb39d26fd90099bfa29
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/09/2018
ms.locfileid: "51295998"
---
# <a name="analyzing-coded-ui-tests-using-coded-ui-test-logs"></a>Analizowanie coded UI kodowanych testów przy użyciu dzienników testu interfejsu użytkownika

Kodowane filtr dzienników testu interfejsu użytkownika i rekord, który uruchamia ważne informacje dotyczące Twojego kodowanego testu interfejsu użytkownika. Dzienniki są prezentowane w formacie, który umożliwia szybkie debugowanie problemów.

## <a name="step-1-enable-logging"></a>Krok 1: Włączanie rejestrowania

Zależnie od scenariusza należy użyć jednej z następujących metod Aby włączyć dziennik:

- Docelowy .NET Framework w wersji 4, na których nie *App.config* plik istnieje w projekcie testu:

   1. Otwórz *QTAgent32_40.exe.config* pliku. Domyślnie ten plik znajduje się w *% ProgramFiles (x86) %\Microsoft Visual Studio\2017\Enterprise\Common7\IDE*.

   2. Na poziom dziennika, który ma, należy zmodyfikować wartość EqtTraceLevel.

   3. Zapisz plik.

- Docelowy .NET Framework w wersji 4.5 bez *App.config* plik istnieje w projekcie testu:

   1. Otwórz *QTAgent32.exe.config* pliku. Domyślnie ten plik znajduje się w *% ProgramFiles (x86) %\Microsoft Visual Studio\2017\Enterprise\Common7\IDE*.

   2. Zmień wartość EqtTraceLevel na poziom dziennika, który ma.

   3. Zapisz plik.

- *App.config* plik znajduje się w projekcie testu:

    - Otwórz *App.config* plik w projekcie, a następnie dodaj następujący kod w węźle Konfiguracja:

      ```xml
      <system.diagnostics>
        <switches>
          <add name="EqtTraceLevel" value="4" />
        </switches>
      </system.diagnostics>`
      ```

- Włączanie rejestrowania z sam kod testu:

   <xref:Microsoft.VisualStudio.TestTools.UITesting.PlaybackSettings.LoggerOverrideState%2A> = HtmlLoggerState.AllActionSnapshot;

## <a name="step-2-run-your-coded-ui-test-and-view-the-log"></a>Krok 2: Uruchamianie kodowanego testu interfejsu użytkownika i Wyświetl dziennik

Po uruchomieniu kodowanego testu interfejsu użytkownika ze zmianami do *QTAgent32.exe.config* pliku w miejscu, zobacz dane wyjściowe link **Eksploratora testów** wyników. Pliki dziennika są tworzone, nie tylko w przypadku, gdy test zakończy się niepowodzeniem, ale także w przypadku udanych testów, gdy poziom śledzenia jest ustawiona na "pełne."

1.  Na **testu** menu, wybierz **Windows** , a następnie wybierz **Eksplorator testów**.

2.  Na **kompilacji** menu, wybierz **Kompiluj rozwiązanie**.

3.  W **Eksploratora testów**, wybierz kodowanego testu interfejsu użytkownika, aby uruchomić, otwórz jego menu skrótów, a następnie wybierz **Uruchom wybrane testy**.

     Testy automatyczne uruchamianie i wskazują one powodzeniem lub niepowodzeniem.

    > [!TIP]
    > Aby wyświetlić **Eksplorator testów**, wybierz **testu** > **Windows**, a następnie wybierz **Eksplorator testów**.

4.  Wybierz **dane wyjściowe** łącze w **Eksplorator testów** wyników.

     ![Link danych wyjściowych w Eksploratorze testów](../test/media/cuit_htmlactionlog1.png)

     Spowoduje to wyświetlenie danych wyjściowych dla testu, który zawiera łącze do dziennika akcji.

     ![Wyniki i łącza danych wyjściowych z kodowanego testu interfejsu użytkownika](../test/media/cuit_htmlactionlog2.png)

5.  Wybierz *UITestActionLog.html* łącza.

     Dziennik jest wyświetlany w przeglądarce sieci web.

     ![Plik dziennika w kodowanych testów interfejsu użytkownika](../test/media/cuit_htmlactionlog3.png)

## <a name="see-also"></a>Zobacz także

- [Używanie automatyzacji interfejsu użytkownika do testowania kodu](../test/use-ui-automation-to-test-your-code.md)
- [Porady: Uruchamianie testów z programu Microsoft Visual Studio](https://msdn.microsoft.com/Library/1a1207a9-2a33-4a1e-a1e3-ddf0181b1046)