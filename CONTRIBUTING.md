# <a name="contributing"></a>Współtworzenie

Dziękujemy za zainteresowanie Współtworzenie dokumentacji programu Visual Studio!

W tym temacie zobaczysz podstawowy proces dodawania i aktualizowania zawartości w [witrynie dokumentacji programu Visual Studio](https://docs.microsoft.com/visualstudio).

W tym temacie omówiono:

* [Proces przekazywania](#process-for-contributing)
* [Lista kontrolna wskazówki](#guidance-checklist)
* [Tworzenie witryny docs](#building-the-docs)
* [Współtworzenie przykłady](#contributing-to-samples)
* [Umowę licencyjną współautora](#contributor-license-agreement)

## <a name="process-for-contributing"></a>Proces przekazywania

**Krok 1:** Otwórz problem zawierająca opis artykułu, aby zapisać i jak on odnosi się do istniejącej zawartości.
Zawartość wewnątrz **docs** folderu jest podzielona na sekcje, które są zorganizowane według obszaru zawartości (np. debuger). Spróbuj ustalić poprawnego folderu do nowej zawartości. Uzyskiwanie opinii na temat swojej propozycji. 

Możesz pominąć ten pierwszy krok w przypadku niewielkich zmian.

**Krok 2:** rozwidlenia `MicrosoftDocs/visualstudio-docs` repozytorium.

**Krok 3:** Utwórz `branch` artykułu.

**Krok 4:** Napisz artykuł.

Jeśli jest to nowy temat, możesz użyć tej funkcji [plik szablonu](./styleguide/template.md) jako punktu początkowego. Zawiera wskazówki dotyczące pisania i wyjaśniono również metadane wymagane dla każdego artykułu, takie jak informacje o autorze.

Przejdź do folderu, który odnosi się do lokalizacji spisu treści dla artykułu w kroku 1.
Ten folder zawiera pliki Markdown wszystkie artykuły w tej sekcji. Jeśli to konieczne, Utwórz nowy folder do umieszczenia plików zawartości.

Obrazy i inne zasoby statyczne, dodaj je do podfolderu o nazwie **media**. Jeśli tworzysz nowy folder na potrzeby zawartości, należy dodać folder multimediów do nowego folderu.

Pamiętaj wykonać poprawnej składni języka Markdown. Zobacz [przewodnik stylistyczny](./styleguide/template.md) Aby uzyskać więcej informacji.

### <a name="example-structure"></a>Przykład struktury

    docs
      /debugger
          debugging-installed-app-package.md
          /media
              debugging-installed-app-package.png

**Krok 5:** przesłać ściągnięcia żądania (PR) z gałęzi `MicrosoftDocs/visualstudio-docs/master`.

Jeśli żądanie Ściągnięcia jest adresowanie istniejący problem, Dodaj `Fixes #Issue_Number` — słowo kluczowe komunikat dotyczący zatwierdzenia lub opis żądania Ściągnięcia, więc ten problem może automatycznie zamknięte po scaleniu żądania Ściągnięcia. Aby uzyskać więcej informacji, zobacz [zamyka problemy za pośrednictwem wiadomości z zatwierdzeń](https://help.github.com/articles/closing-issues-via-commit-messages/).

Zespół programu Visual Studio przejrzy żądanie Ściągnięcia i informacją o tym, czy zmiana wygląda dobrze, czy są niezbędne, aby można było zatwierdzić innych aktualizacji/zmian.

**Krok 6:** wprowadź wymagane zmiany w gałęzi, zgodnie z opisem z zespołem.

Maintainers spowoduje scalenie żądania Ściągnięcia z gałęzią główną, po zastosowaniu opinii i zmiany wygląda dobrze.

W erze przesuwamy wszystkich zatwierdzeń z głównej gałęzi do gałęzi aktywnej, a następnie będzie można wyświetlić Twój wkład Konferencję https://docs.microsoft.com/visualstudio/.

## <a name="dos-and-donts"></a>Zalecenia i zakazy

Poniżej przedstawiono krótką listę przeprowadzi reguł, które należy mieć na uwadze, gdy wprowadzasz zmiany w dokumentacji platformy .NET.

- **Nie** zaskakującymi nam za pomocą żądań ściągnięcia big Data. Zamiast tego należy zgłosić problem i Rozpocznij dyskusję, dzięki czemu można firma Microsoft zobowiązuje się w kierunku, zanim inwestować dużą ilość czasu.
- **CZY** odczytu [przewodnik stylistyczny](./styleguide/template.md) i [połączeń głosowych i ton](./styleguide/voice-tone.md) wytycznych.
- **CZY** użyj [szablonu](./styleguide/template.md) pliku jako punktu początkowego swoją pracę.
- **CZY** tworzenie oddzielnej gałęzi w rozwidleniu przed rozpoczęciem pracy w artykułach.
- **CZY** wykonaj [przepływu pracy przepływu usługi GitHub](https://guides.github.com/introduction/flow/).
- **CZY** blogu i tweet (lub niezależnie od rodzaju) o współtworzeniu, często!

> [!NOTE]
> Można zauważyć niektóre tematy są obecnie następujące wszystkie wskazówki, które są określone w tym miejscu i na [przewodnik stylistyczny](./styleguide/template.md) także. Pracujemy nad do osiągnięcia spójności w całej lokacji. Sprawdź listę [zgłaszanie problemów](https://github.com/dotnet/docs/issues?q=is%3Aissue+is%3Aopen+label%3Aguidelines-adherence) firma Microsoft obecnie śledzonych dla tego określonego celu.

## <a name="building-the-docs"></a>Tworzenie witryny docs

Dokumentacja jest zapisywany [GitHub Flavored Markdown](https://help.github.com/categories/writing-on-github/) i opracowano z użyciem [DocFX](https://dotnet.github.io/docfx/) i inne narzędzia do publikowania/budynek wewnętrznego. Jest ona hostowana na [docs.microsoft.com](https://docs.microsoft.com/dotnet).

Jeśli chcesz tworzyć dokumentację lokalnie, musisz zainstalować [DocFX](https://dotnet.github.io/docfx/); najnowsze wersje są najlepsze.

Istnieje kilka sposobów, aby użyć DocFX, a większość z nich są objęte [DocFX przewodnik wprowadzenie](https://dotnet.github.io/docfx/tutorial/docfx_getting_started.html).
Poniższe instrukcje opisują korzystanie z [wiersza polecenia na podstawie](https://dotnet.github.io/docfx/tutorial/docfx_getting_started.html#2-use-docfx-as-a-command-line-tool) wersję narzędzia.
Jeśli masz doświadczenia z innymi sposobami powyższe łącze na liście, możesz je wykorzystać.

**Uwaga:** obecnie DocFX wymaga programu .NET Framework na Windows lub platformy Mono (dla systemu Linux lub macOS). Mamy nadzieję, że w przyszłości przenieść go do programu .NET Core.

Można tworzyć i wynikowy lokacji lokalnie przy użyciu serwera sieci web wbudowanego w wersji zapoznawczej. Przejdź do folderu dokumentacji core na komputerze i wpisz następujące polecenie:

```
docfx -t default --serve
```

To jest uruchamiany w podglądzie lokalnym [localhost: 8080](http://localhost:8080). Można wyświetlić zmiany, przechodząc do `http://localhost:8080/[path]`, takich jak http://localhost:8080/articles/welcome.html.

**Uwaga:** podglądzie lokalnym aktualnie nie zawiera żadnych motywów w tej chwili, wygląd i działanie będą takie same jak w witrynie dokumentacji. Pracujemy nad do ustalania środowiska.

# <a name="contributing-to-samples"></a>Współtworzenie przykłady

Teraz zawierać wymagane przykładowego kodu jako wbudowane bloki kodu w swoim artykule. Repozytorium zawiera codesnippets folder, ale nie jest gotowy do publicznego dodawania zawartości.
