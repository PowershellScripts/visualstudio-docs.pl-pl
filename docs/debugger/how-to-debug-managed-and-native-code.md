---
title: 'Samouczek: Debugowanie kodu zarządzanego i natywnego (tryb mieszany)'
description: Dowiedz się, jak można debugować natywną bibliotekę DLL z aplikacji platformy .NET Core lub .NET Framework za pomocą debugowania w trybie mieszanym
ms.custom: ''
ms.date: 10/24/2018
ms.technology: vs-ide-debug
ms.topic: tutorial
dev_langs:
- CSharp
- C++
helpviewer_keywords:
- mixed mode debugging
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- dotnet
- cplusplus
ms.openlocfilehash: 97ad3b6e112a05db817f7a522c3865893d439fd7
ms.sourcegitcommit: 12d6398c02e818de4fbcb4371bae9e5db6cf9509
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/25/2018
ms.locfileid: "50050329"
---
# <a name="tutorial-debug-managed-and-native-code-in-the-same-debugging-session"></a>Samouczek: Debugowanie kodu zarządzanego i natywnego w tej samej sesji debugowania

Program Visual Studio umożliwia włączenie więcej niż jeden typ debugera przy debugowaniu, która jest wywoływana, debugowanie w trybie mieszanym. W tym samouczku, można ustawić opcje debugowania kodu zarządzanego i natywnego w jednej sesji debugowania. W tym samouczku pokazano, jak można debugować kodu natywnego z zarządzanej aplikacji, ale można również wykonać odwrotna i [debugować kodu zarządzanego z aplikacji natywnej](../debugger/how-to-debug-in-mixed-mode.md). Debuger obsługuje również debugowanie w trybie mieszanym, takich jak debugowanie innych typów [języka Python i kodu natywnego](../python/debugging-mixed-mode-c-cpp-python-in-visual-studio.md) i w typach aplikacji, takich jak ASP.NET przy użyciu debugera skryptów.

W tym samouczku wykonasz następujące czynności:

> [!div class="checklist"]
> * Tworzenie prostego natywnej biblioteki DLL
> * Utwórz prostą aplikację platformy .NET Core lub .NET Framework do wywoływania biblioteki DLL
> * Uruchom debuger
> * Trafiony punkt przerwania w aplikacji zarządzanej
> * Wejdź do kodu natywnego

## <a name="prerequisites"></a>Wymagania wstępne

* Konieczne jest posiadanie zainstalowanego programu Visual Studio i **programowanie aplikacji klasycznych w języku C++** obciążenia.

    Jeśli jeszcze nie zainstalowano programu Visual Studio, przejdź do strony [program Visual Studio pobiera](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) strony, aby zainstalować go za darmo.

    Jeśli musisz zainstalować obciążenie, ale już program Visual Studio, kliknij przycisk **Otwórz Instalator programu Visual Studio** łącze w okienku po lewej stronie **nowy projekt** okno dialogowe. Uruchamia Instalatora programu Visual Studio. Wybierz **programowanie aplikacji klasycznych w języku C++** obciążenia, wybierz **Modyfikuj**.

* Musisz również posiadać albo **programowanie aplikacji klasycznych dla platformy .NET** obciążenia lub **platformy .NET Core programowanie wieloplatformowych** zainstalowanym obciążeniem, w zależności od typu aplikacji, która ma zostać utworzony.

## <a name="create-a-simple-native-dll"></a>Tworzenie prostego natywnej biblioteki DLL

1. W programie Visual Studio, wybierz **pliku** > **New** > **projektu**.

1. W **nowy projekt** okna dialogowego wybierz **Visual C++**, **innych** z sekcji zainstalowanych szablonów, a następnie w środkowym okienku wybierz **pusty projekt** .

1. W **nazwa** wpisz **Mixed_Mode_Debugging** i kliknij przycisk **OK**.

    Program Visual Studio tworzy pusty projekt, który jest wyświetlany w Eksploratorze rozwiązań, w okienku po prawej stronie.

1. W Eksploratorze rozwiązań kliknij prawym przyciskiem myszy **pliki źródłowe** węzła w C++ projektu, a następnie wybierz **Dodaj** > **nowy element**, a następnie wybierz pozycję **języka C++ plik (.cpp)**. Nadaj plikowi nazwę **Mixed_Mode.cpp**i wybierz polecenie **Dodaj**.

    Visual Studio dodaje nowy plik w języku C++.

1. Skopiuj następujący kod do *Mixed_Mode.cpp*:

    ```cpp
    #include "Mixed_Mode.h"
    ```
1. W Eksploratorze rozwiązań kliknij prawym przyciskiem myszy **pliki nagłówkowe** węzła w C++ projektu, a następnie wybierz **Dodaj** > **nowy element**, a następnie wybierz pozycję  **Plik nagłówka (.h)**. Nadaj plikowi nazwę **Mixed_Mode.h**i wybierz polecenie **Dodaj**.

    Visual Studio dodaje nowy plik nagłówkowy.

1. Skopiuj następujący kod do *Mixed_Mode.h*:

    ```cpp
    #ifndef MIXED_MODE_MULTIPLY_HPP
    #define MIXED_MODE_MULTIPLY_HPP

    extern "C"
    {
        __declspec(dllexport) int __stdcall mixed_mode_multiply(int a, int b) {
            return a * b;
        }
    }
    #endif
    ```

1. Na pasku narzędzi debugowania wybierz **debugowania** konfiguracji i **x86** lub **x64** jako platformę (dla platformy .NET Core, która zawsze działa w trybie 64-bitowym, wybierz **x64**  jako platformę).

1. W Eksploratorze rozwiązań kliknij prawym przyciskiem myszy węzeł projektu (**Mixed_Mode_Debugging**) i wybierz polecenie **właściwości**.

    > [!IMPORTANT]
    > Konfiguracja właściwości dla języka C++ jest poszczególnych platform. Tak Jeśli zaczniesz od jednej do innych (x86 do x64 lub vice versa), można również ustawić właściwości dla nowej konfiguracji. (Na stronie właściwości sprawdź **x64** lub **Win32** jest ustawiony jako platformę w górnej części strony.)

1. W **właściwości** wybierz **właściwości konfiguracji** > **konsolidatora** > **zaawansowane**, i następnie w **punkt wejścia nie** listy rozwijanej liście, upewnij się, że **nie** jest zaznaczone. Jeśli musisz zmienić ustawienie, aby **nie**, następnie wybierz **Zastosuj**.

1. W **właściwości** wybierz **właściwości konfiguracji** > **ogólne**, a następnie wybierz pozycję **Biblioteka dynamiczna (dll)** z **typu konfiguracji** pola. Następnie Zastosuj ustawienia.

    ![Przełącz się do macierzystych bibliotek DLL](../debugger/media/mixed-mode-set-as-native-dll.png)

1. Kliknij prawym przyciskiem myszy projekt i wybierz polecenie **kompilacji**.

    Projekt powinien być kompilowany bez błędów.

## <a name="create-a-simple-net-framework-or-net-core-app-to-call-the-dll"></a>Tworzenie prostej aplikacji .NET Framework lub .NET Core do wywoływania biblioteki DLL

1. W programie Visual Studio, wybierz **pliku** > **New** > **projektu**.

    > [!NOTE]
    > Mimo że można również dodać nowy projekt zarządzanych do rozwiązania projektu C++, zamiast tworzenia nowego rozwiązania nie Radzimy sobie, w tym miejscu umożliwiają większy zestaw scenariuszy debugowania.

1. Wybierz szablon dla kodu aplikacji.

    Dla programu .NET Framework w **nowy projekt** okna dialogowego wybierz **Visual C#**, **pulpitu Windows** z sekcji zainstalowanych szablonów, a następnie w środkowym okienku wybierz  **Aplikacja konsoli (.NET Framework)**.

    Dla platformy .NET Core w **nowy projekt** okna dialogowego wybierz **Visual C#**, **platformy .NET Core** z sekcji zainstalowanych szablonów, a następnie w środkowym okienku wybierz  **Aplikacja (.NET Core) konsoli**.

1. W **nazwa** wpisz **Mixed_Mode_Calling_App** i kliknij przycisk **OK**.

    Program Visual Studio tworzy projekt konsoli, która jest wyświetlana w Eksploratorze rozwiązań w okienku po prawej stronie.

1. W *Program.cs*, Zastąp domyślny kod następującym kodem:

    ```csharp
    using System;
    using System.Runtime.InteropServices;

    namespace Mixed_Mode_Calling_App
    {
        public class Program
        {
            // Replace the file path shown here with the
            // file path on your computer. For .NET Core, the typical (default) path
            // for a 64-bit DLL might look like this:
            // C:\Users\username\source\repos\Mixed_Mode_Debugging\x64\Debug\Mixed_Mode_Debugging.dll
            // Here, we show a typical path for a DLL targeting the **x86** option.
            [DllImport(@"C:\Users\username\source\repos\Mixed_Mode_Debugging\Debug\Mixed_Mode_Debugging.dll", EntryPoint =
            "mixed_mode_multiply", CallingConvention = CallingConvention.StdCall)]
            public static extern int Multiply(int x, int y);
            public static void Main(string[] args)
            {
                int result = Multiply(7, 7);
                Console.WriteLine("The answer is {0}", result);
                Console.ReadKey();
            }
        }
    }
    ```

1. W nowym kodzie należy zaktualizować ścieżkę pliku do ścieżki biblioteki dll, która została wcześniej utworzona (zobacz komentarze w kodzie). Upewnij się, Zastąp *username* symbol zastępczy.

## <a name="configure-mixed-mode-debugging-net-framework"></a>Konfigurowanie trybu mieszanego debugowania (.NET Framework)

1. W Eksploratorze rozwiązań kliknij prawym przyciskiem myszy zarządzanej **Mixed_Mode_Calling_App** projektu, a następnie wybierz **Ustaw jako projekt startowy**.

1. Kliknij prawym przyciskiem myszy zarządzanej **Mixed_Mode_Calling_App** projektu, a następnie wybierz **właściwości**, a następnie wybierz **debugowania** w okienku po lewej stronie. Wybierz **Włącz debugowanie kodu natywnego**, a następnie zamknij stronę właściwości, aby zapisać zmiany.

    ![Włącz debugowanie w trybie mieszanym](../debugger/media/mixed-mode-enable-native-code-debugging.png)

## <a name="configure-mixed-mode-debugging-net-core"></a>Konfigurowanie trybu mieszanego debugowania (.NET Core)

W większości wersji programu Visual Studio 2017, musisz włączyć debugowanie w trybie mieszanym dla kodu natywnego w aplikacji platformy .NET Core przy użyciu *launchSettings.json* pliku zamiast **właściwości** strony. Aby śledzić aktualizacje interfejsu użytkownika dla tej funkcji, zobacz ten [problem w usłudze GitHub](https://github.com/dotnet/project-system/issues/1125).

1. Otwórz *launchSettings.json* w pliku *właściwości* folderu. Domyślnie plik znajduje się w tej lokalizacji.

    *C:\Users\<username > \source\repos\Mixed_Mode_Calling_App\Properties*

    Jeśli plik nie jest obecny, otwórz właściwości projektu (kliknij prawym przyciskiem myszy zarządzanej **Mixed_Mode_Calling_App** projektu w Eksploratorze rozwiązań, a następnie wybierz **właściwości**). Tymczasowe zmiany w **debugowania** kartę i skompiluj projekt. Cofnąć zmiany, które zostały wprowadzone.

1. W *lauchsettings.json* plików, dodaj następującą właściwość:

    ```csharp
    "nativeDebugging": true
    ```

    Tak na przykład plik może wyglądać następująco:

    ```csharp
    {
      "profiles": {
        "Mixed_Mode_Calling_App": {
          "commandName": "Project",
          "nativeDebugging": true
        }
      }
    }
    ```

## <a name="set-a-breakpoint-and-start-the-debugger"></a>Ustaw punkt przerwania i uruchomić debuger

1. W C# otwarty projekt *Program.cs* i ustaw punkt przerwania w następujący wiersz kodu, klikając w lewy margines:

    ```csharp
    int result = Multiply(7, 7);
    ```

    Czerwony okrąg pojawia się na lewym marginesie, aby wskazać, że ustawiono punkt przerwania.

1. Naciśnij klawisz **F5** (**debugowania** > **Rozpocznij debugowanie**) można uruchomić debugera.

    Debuger zatrzymuje się na punkcie przerwania, który został ustawiony. Żółta strzałka wskazuje, gdzie debuger jest obecnie wstrzymana.

## <a name="step-into-native-code"></a>Wejdź do kodu natywnego

1. Podczas wstrzymania w aplikacji zarządzanej, naciśnij klawisz **F11** (**debugowania** > **Step Into**).

    Plik nagłówka z kodem natywnym otwiera się i zostanie wyświetlona żółta strzałka, gdy debuger jest wstrzymana.

    ![Wejdź do kodu natywnego](../debugger/media/mixed-mode-step-into-native-code.png)

    Teraz można wykonywać następujące czynności dla zestawu i identyfikować punkty przerwania i sprawdzanie zmiennych.

1. Umieść kursor nad zmienne, aby zobaczyć ich wartości.

1. Przyjrzyj się **Autos** i **lokalne** systemu windows, aby zobaczyć zmiennej i ich wartości.

    Wstrzymaniu w debugerze, ale można używać innych funkcji debugera taki jak **Obejrzyj** okna i **stos wywołań** okna.

1. Naciśnij klawisz **F11** ponownie w celu przechodzenia debugera jeden wiersz.

1. Naciśnij klawisz **Shift + F11** (**debugowania** > **Step Out**) aby kontynuować wykonywanie aplikacji, a następnie ponownie wstrzymać w aplikacji zarządzanej.

1. Naciśnij klawisz **F5** kontynuowanie działania aplikacji.

    Gratulacje! Ukończono samouczek na temat debugowania w trybie mieszanym.

## <a name="next-steps"></a>Następne kroki

W tym samouczku przedstawiono sposób debugowania kodu macierzystego z zarządzanej aplikacji, należy włączyć debugowanie w trybie mieszanym. Aby uzyskać przegląd innych funkcji debugera zobacz następujący artykuł:

> [!div class="nextstepaction"]
> [Pierwsze spojrzenie na debugera](../debugger/debugger-feature-tour.md)
