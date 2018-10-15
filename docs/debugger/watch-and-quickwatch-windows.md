---
title: Ustawianie wyrażenia kontrolnego na zmiennych w programie Visual Studio | Dokumentacja firmy Microsoft
ms.custom: H1Hack27Feb2017
ms.date: 10/11/2018
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.watch
helpviewer_keywords:
- debugging [Visual Studio], Watch window
- expressions [debugger], evaluating
- variables [debugger], evaluating
- expression evaluation
- registers, evaluating
- debugging [Visual Studio], expression evaluation
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: ad08799c0dce3792e096291dfaf62d52e2515df4
ms.sourcegitcommit: 48bc8492973e93612e5afaba3b47d0f98aecf97c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/15/2018
ms.locfileid: "49325019"
---
# <a name="set-a-watch-on-variables-using-the-watch-and-quickwatch-windows-in-visual-studio"></a>Ustawianie wyrażenia kontrolnego na zmiennych używanie okien wyrażenie kontrolne i QuickWatch w programie Visual Studio

Podczas debugowania, można użyć **Obejrzyj** i **QuickWatch** systemu windows, aby obejrzeć zmiennych i wyrażeń.  Różnica jest to, że **Obejrzyj** można wyświetlić w oknie kilku zmiennych podczas **QuickWatch** okno wyświetla pojedynczą zmienną w czasie.

Systemu windows są dostępne tylko podczas sesji debugowania. Można otworzyć **Obejrzyj** oknie Wybierz **debugowania** > **Windows** > **Obejrzyj**, a następnie wybierz polecenie **Obejrzeć 1**, **Obejrzyj 2**, **Obejrzyj 3**, lub **Obejrzyj 4**. Aby otworzyć **QuickWatch** okna, albo kliknij prawym przyciskiem myszy zmienną i wybierz **QuickWatch**, lub po prostu wybierz **debugowania** > **QuickWatch** .

## <a name="observe-variables-with-the-watch-window"></a>Obserwuj zmienne okno czujki

Możesz obserwować więcej niż jedną zmienną z **Obejrzyj** okna. Na przykład, jeśli masz następujący kod:

```C++
int main()
{
    int a, b, c;
    a = 1;
    b = 2;
    c = 0;

    for (int i = 0; i < 10; i++)
    {
        a++;
        b *= 2;
        c = a + b;
    }

    return 0;
}

```

Dodaj wartości trzech zmiennych do **Obejrzyj** okna w następujący sposób:

1. Wybierz `c = a + b;` wiersza.

2. Ustaw punkt przerwania (wybierając **debugowania** > **Przełącz punkt przerwania** lub naciskając klawisz F9).

3. Rozpocznij debugowanie (F5). Zatrzymuje wykonywanie w punkcie przerwania.

4. Otwórz **Obejrzyj** okna (wybierając **debugowania** > **Windows** > **Obejrzyj**  >   **Czujka 1**, lub naciskając klawisze Ctrl + Alt + W, 1).

5. Wybierz pusty wiersz, a następnie wpisz zmienną `a`. Następnie te same czynności wykonasz zmiennych `b` i `c`.

   ![Obserwuj zmienne](../debugger/media/watchvariables.png "WatchVariables")

6. Kontynuuj, debugowanie, naciskając klawisz F11, zgodnie z potrzebami, aby przejść do debugera.

Powinien zostać wyświetlony wartości zmiennych zmieniają się wraz z iteracyjne przeglądanie `for` pętli.

Jeśli programowania używasz w kodzie macierzystym, czasami konieczne może być zakwalifikowanie kontekstu nazwy zmiennej lub wyrażenie, które ma nazwę zmiennej. Kontekst jest funkcja, plik źródłowy i moduł, w którym znajduje się zmienna. Jeśli ma być zakwalifikowanie kontekstu, można użyć składni operatora kontekstu. Aby uzyskać więcej informacji, zobacz [operator kontekstu (C++)](../debugger/context-operator-cpp.md).

## <a name="observe-expressions-with-the-watch-window"></a>Sprawdź wyrażenia w oknie czujki

Teraz Wypróbujmy użycie zamiast tego wyrażenia. Możesz dodać dowolne prawidłowe wyrażenie rozpoznawanym przez debuger.

Na przykład jeśli masz kod przedstawiony w poprzedniej sekcji, można uzyskać średnią z trzech wartości przy użyciu tego wyrażenia:

![Wyrażenie czujki](../debugger/media/watchexpression.png "WatchExpression")

Reguły dotyczące oceny wyrażenia w **Obejrzyj** są ogólnie takie same jak reguły oceny wyrażenia w języku programowania. Jeśli wyrażenie zawiera błąd składniowy, oczekiwać, że ten sam błąd kompilatora, które są widoczne w edytorze kodu. Oto przykład:

![Obejrzyj błąd wyrażenia](../debugger/media/watchexpressionerror.png "WatchExpressionError")

## <a name="bkmk_refreshWatch"></a> Odświeżanie wartości czujki, które są nieaktualne

Ikona odświeżania (strzałka cykliczne) mogą być wyświetlane, gdy wyrażenie jest obliczane w **Obejrzyj** okna. Jeśli zostały wyłączone oceny właściwości (wybierając **narzędzia** > **opcje** > **debugowanie**  >   **Ogólne**, następnie wyczyszczenie **Włącz obliczanie właściwości i inne niejawne wywołania funkcji**), a napisaniu poniższego kodu:

```csharp
static void Main(string[] args)
{
    List<string> list = new List<string>();
    list.Add("hello");
    list.Add("goodbye");
}

```

Powinien być podobny do poniższej ilustracji Jeśli wyrażenie kontrolne jest ustawiony na `Count` właściwości listy:

![RefreshWatch](../debugger/media/refreshwatch.png "RefreshWatch")

Na poprzedniej ilustracji przedstawiono błąd lub wartość, która jest nieaktualna. Wartość można ogólnie odświeżanie, wybierając ikonę, ale w niektórych przypadkach może nie chcesz odświeżać je. Najpierw musisz znać, dlaczego nie można obliczyć wartość.

Etykietka narzędzia zawiera informacje dotyczące Dlaczego nie można obliczyć wyrażenia, po wskazaniu ikony. Jeśli circling strzałki na liście, nie można obliczyć wyrażenia, dla jednego z następujących powodów:

- Wystąpił błąd, ponieważ obliczania wyrażenia. Na przykład limit czasu może wystąpić lub zmienną mogły być poza zakres tej asysty.

- Wyrażenie zawiera wywołanie funkcji, który może wywołać efekt uboczny, w aplikacji (zobacz [efekty uboczne i wyrażenia](#bkmk_sideEffects) sekcji).

- Wyłączeniu automatycznej oceny właściwości i niejawne funkcja wywołuje przez debuger (wybierając **narzędzia** > **opcje** > **debugowanie**  >  **Ogólne**, następnie wyczyszczenie **Włącz obliczanie właściwości i inne niejawne wywołania funkcji**). Nie można automatycznie obliczyć wyrażenia następnie.

Aby odświeżyć wartości, wybierz ikonę odświeżania lub naciśnij klawisz spacji. Debuger próbuje ponownie oceń wyrażenie. Ikona odświeżania może pojawić się, ponieważ automatycznej oceny właściwości i inne niejawne wywołania funkcji zostało wyłączone. W tym przypadku debugera można obliczyć wyrażenia.

Ikona może zostać wyświetlony jest koło z dwóch falistych linii, które przypominają wątków. Ta ikona oznacza, że debuger nie szacuje wyrażenia ze względu na potencjalne zależności między wątkami. Innymi słowy obliczenie kodu wymaga innych wątków w aplikacji w celu tymczasowego uruchomienia. Podczas pracy w trybie przerwania, wszystkie wątki w aplikacji zwykle są zatrzymywane. Zezwolenie tymczasowego uruchomienia innych wątków może mieć nieoczekiwane wpływ na stan programu i powoduje, że debuger Ignoruj zdarzenia, takie jak punkty przerwania i wyjątków zgłaszanych na te wątki.

## <a name="bkmk_sideEffects"></a> Efekty uboczne i wyrażenia

Obliczenie niektórych wyrażeń może zmienić wartość zmiennej lub inaczej wpłynąć na stan programu. Na przykład obliczenie następującego wyrażenia zmienia wartość `var1`:

```csharp
var1 = var2
```

Ten kod może spowodować, że [efekt uboczny](https://en.wikipedia.org/wiki/Side_effect_\(computer_science\)). Efekty uboczne może utrudnić debugowanie bardziej przez zmianę sposobu działania programu.

Wyrażenie ma efekty uboczne, jest oceniane tylko raz, po przejściu go. Dalsze oceny są wyłączone. Można ręcznie przezwyciężyć takie działanie, wybierając ikonę aktualizacji, który pojawia się obok wartości.

Jest jednym ze sposobów, aby uniknąć ze wszystkimi efektami ubocznymi, aby wyłączyć funkcję automatycznej oceny (wybierając **narzędzia** > **opcje** > **debugowanie**  >  **Ogólne**, następnie wyczyszczenie **Włącz obliczanie właściwości i inne niejawne wywołania funkcji**).

Podczas oceny właściwości i niejawne wywołania funkcji jest wyłączone, możesz wymusić oceny za pomocą **ac** format modyfikator (tylko język C#). Zobacz [Specyfikatory w języku C# formatu](../debugger/format-specifiers-in-csharp.md).

## <a name="bkmk_objectIds"></a> Użyj identyfikatorów obiektów w oknie czujki (C# i Visual Basic)

Czasami możesz chcieć przyjrzeć się zachowaniu określonego obiektu. Na przykład można śledzić obiekt określony przez zmienną lokalną przeszedł do tej zmiennej poza zakres tej asysty. W języku C# i Visual Basic, możesz tworzyć identyfikatory obiektów dla konkretnych wystąpień typów referencyjnych i używać ich w **Obejrzyj** okna w warunków punktu przerwania. Identyfikator obiektu jest generowany przez środowisko uruchomieniowe języka wspólnego (CLR) debugowanie usług i powiązane z obiektem.

> [!NOTE]
> Identyfikatory obiektów Utwórz uszkodzonymi odwołaniami, które nie uniemożliwiają jako elementu bezużytecznego zbierane przez obiekt. Są one prawidłowe tylko dla bieżącej sesji debugowania.

Poniższy kod tworzy jedną metodę `Person` przy użyciu zmiennej lokalnej, ale chcesz dowiedzieć się, jakie `Person`jego nazwa jest w innej metodzie:

```csharp
class Person
{
    public Person(string name)
    {
        Name = name;
    }
    public string Name { get; set; }
}

public class Program
{
    static List<Person> _people = new List<Person>();
    public static void Main(string[] args)
    {
        MakePerson();
        DoSomething();
    }

    private static void MakePerson()
    {
        var p = new Person("Bob");
        _people.Add(p);
    }

    private static void DoSomething()
    {
        // more processing
         Console.WriteLine("done");
    }
}

```

Można dodać odwołanie do tego `Person` obiektu **Obejrzyj** okna w następujący sposób:

1. Zaznacz wiersz w kodzie, który występuje, że obiekt został utworzony.

2. Ustaw punkt przerwania (wybierając **debugowania** > **Przełącz punkt przerwania** lub naciskając klawisz F9).

3. Rozpocznij debugowanie.

4. Po zatrzymaniu w punkcie przerwania wykonywania Otwórz **zmiennych lokalnych** okna (wybierając **debugowania** > **Windows** > **zmiennychlokalnych**), kliknij prawym przyciskiem myszy zmienną i wybierz **wprowadzić identyfikator obiektu**.

   Powinien zostać wyświetlony znak dolara (**$**) oraz liczbą **lokalne** okno, które jest identyfikator obiektu.

   > [!NOTE]
   > Jeśli chcesz wyświetlić właściwości tego obiektu, takie jak `Person.Name`, należy włączyć oceny właściwości, wybierając **narzędzia** > **opcje**  >   **Debugowanie** > **ogólne**, następnie ustawiając **Włącz obliczanie właściwości i inne niejawne wywołania funkcji**.

5. Dodaj identyfikator obiektu do **Obejrzyj** okien przez kliknięcie prawym przyciskiem myszy dolara i numer, a następnie wybierając **Dodaj czujkę**.

6. Ustaw punkt przerwania, w którym chcesz obserwować zachowanie obiektu.  W poprzednim kodzie, który będzie mieć `DoSomething()` metody.

7. Kontynuuj, debugowanie. Gdy zatrzyma wykonywanie `DoSomething()` metody **Obejrzyj** jest wyświetlana w oknie `Person` obiektu.

## <a name="use-registers-in-the-watch-window-c-only"></a>Użyj rejestruje się w oknie czujki (tylko C++)

Można dodać rejestru nazwy i nazwy zmiennych, przy użyciu  **$ \<zarejestrować&nbsp;nazwa >** lub  **@ \<zarejestrować&nbsp;name >** podczas debugowania kodu macierzystego. Aby uzyskać więcej informacji, zobacz [Pseudozmienne](../debugger/pseudovariables.md).

## <a name="dynamic-view-and-the-watch-window"></a>Dynamiczny widok i w oknie czujki

Niektóre języki skryptów (na przykład, JavaScript lub Python) Użyj dynamicznych lub [kaczka wpisując](https://en.wikipedia.org/wiki/Duck_typing), i językami .NET (w wersji 4.0 lub nowszy) obsługuje obiekty, które są trudne do obserwowania przy użyciu normalnych debugowania systemu windows, ponieważ ich może to być środowiska uruchomieniowego, właściwości i metody, które nie mogą być wyświetlane.

**Obejrzyj** okno może być wyświetlany obiekt dynamiczny jest tworzony z typu, który implementuje <xref:System.Dynamic.IDynamicMetaObjectProvider> interfejsu. Po wyświetleniu tego obiektu jest debugera dodaje specjalny **dynamiczny widok** węzeł podrzędny o nazwie obiektu po otwarciu **Autos** okna (wybierając **debugowania**  >  **Windows** > **Autos**). Ten węzeł Wyświetla dynamiczne elementy członkowskie obiektu dynamicznych, ale nie zezwala na edytowanie wartości elementów członkowskich.

Aby wstawić nowe wyrażenie kontrolne zmiennej, rzutuje obiekt dynamiczny obiektu:

1. Kliknij prawym przyciskiem myszy dowolnego podrzędnym **dynamiczny widok**.
2. Wybierz **Dodaj wyrażenie kontrolne**. Następnie `object.name` staje się `((dynamic) object).name`.

Ocena członków **dynamiczny widok** mogą mieć skutki uboczne. Opis efekty uboczne są znaleźć [efekty uboczne i wyrażenia](#bkmk_sideEffects) sekcji. Dla języka C# debuger nie automatycznie to ponowne ocenienie wartości widocznych na **dynamiczny widok** po kroku do nowego wiersza kodu. Dla języka Visual Basic wyrażeń dodane za pomocą **dynamiczny widok** są automatycznie odświeżane.

Aby uzyskać instrukcje dotyczące sposobu odświeżania **dynamiczny widok** wartości, zobacz [wartości Odśwież wyrażenie kontrolne, które są nieaktualne](#bkmk_refreshWatch) sekcji.

Jeśli chcesz wyświetlić tylko **dynamiczny widok** dla obiektu, możesz użyć **dynamiczne** specyfikatora w formatu **Obejrzyj** okna:

- C#: `ObjectName, dynamic`
- Visual Basic: `$dynamic, ObjectName`

**Dynamiczny widok** również poprawia środowisko debugowania dla obiektów COM. Gdy debuger pobiera zapakowane w obiekt COM **.__ComObject**, dodaje **dynamiczny widok** węzła dla obiektu.

## <a name="observe-a-single-variable-or-expression-with-quickwatch"></a>Obserwuj pojedynczej zmiennej lub wyrażenia w QuickWatch

Możesz użyć **QuickWatch** okna, aby obserwować w pojedynczej zmiennej. Na przykład, jeśli masz następujący kod:

```csharp
static void Main(string[] args)
{
    int a, b;
    a = 1;
    b = 2;
    for (int i = 0; i < 10; i++)
    {
        a = a + b;
    }
}
```

Możesz obserwować zmiennej w **QuickWatch** okna w następujący sposób:

1. Ustaw punkt przerwania na `a = a + b;` wiersza.

2. Rozpocznij debugowanie. Zatrzymuje wykonywanie w punkcie przerwania.

3. Wybierz zmienną `a`.

4. Wybierz opcję **debugowania** > **QuickWatch** lub naciśnij **Shift + F9**. **QuickWatch** zostanie wyświetlone okno. W **wartość** polu `a` zmienna jest widoczna o wartości 1.

   ![Zmienna QuickWatch](../debugger/media/quickwatchvariable.png "QuickWatchVariable")

   Aby szacować wyrażenia za pomocą zmiennej, wpisz wyrażenie takich jak `a + b` do **wyrażenie** pole, a następnie kliknij przycisk **to ponowne ocenienie**.

   ![Wyrażenie w QuickWatch](../debugger/media/quickwatchexpression.png "QuickWatchExpression")

   Aby dodać zmiennej lub wyrażenia, aby **Obejrzyj** w oknie **QuickWatch**, wybierz **Dodaj czujkę**.

   > [!NOTE]
   > **QuickWatch** okno jest oknem modalne okno dialogowe, więc nie można kontynuować debugowanie tak długo, jak jest otwarty.

5. Zamknij **QuickWatch** okna. Teraz można kontynuować debugowanie podczas obserwowania wartość w **Obejrzyj** okna.

## <a name="see-also"></a>Zobacz także

[Okna debugera](../debugger/debugger-windows.md)
