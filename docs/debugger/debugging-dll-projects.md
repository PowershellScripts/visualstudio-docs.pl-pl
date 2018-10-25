---
title: Debugowanie projektów DLL | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 05/23/2017
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging DLLs
- templates, debugging DLLs
- DLLs, debugging
- debugging [Visual Studio], DLLs
ms.assetid: 433cab30-d191-460b-96f7-90d2530ca243
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 04ffdd5d0256ae0fc42b89dfa850fb0ae2d36748
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49818669"
---
# <a name="debugging-dll-projects-from-visual-studio"></a>Debugowanie projektów DLL w programie Visual Studio
Poniższe szablony programu Visual Studio tworzą biblioteki DLL:  
  
-   (C++, C# i Visual Basic) Biblioteka klas   

-   (C++): projekt DLL konsoli Win32
  
     Aby uzyskać więcej informacji, zobacz [techniki testowania MFC](../debugger/mfc-debugging-techniques.md).

-   (C++, C# i Visual Basic): Biblioteka formantów Windows Forms
  
     Debugowanie Biblioteka kontrolek formularzy Windows jest podobne do debugowania projektu biblioteki klas. W większości przypadków będzie wywoływać kontrolki Windows z innego projektu. Podczas debugowania projektu wywołującego można wkroczyć do kodu kontrolki Windows, ustawić punkty przerwania i wykonywać inne operacje debugowania. Aby uzyskać więcej informacji, zobacz [kontrolek formularzy Windows Forms](/dotnet/framework/winforms/controls/index).  

  
##  <a name="vxtskdebuggingdllprojectsbuildingadebugversion"></a> Tworzenie wersji debugowania  
 Niezależnie od tego, jak rozpocząć debugowanie upewnij się, najpierw Tworzenie wersji debugowania biblioteki DLL, a następnie upewnij się, że wersja do debugowania znajduje się w lokalizacji, gdzie jej szuka go znaleźć. To może wydawać się oczywiste, ale Jeśli zapomnisz tego kroku, aplikacja może znaleźć inną wersję biblioteki DLL i ją załadować. Następnie program będzie kontynuował zastanawiasz się, dlaczego nigdy nie został osiągnięty punkt przerwania. Podczas debugowania, możesz sprawdzić, które biblioteki DLL program załadował, przez otwarcie debugera **modułów** okna. **Modułów** okno zawiera listę każdego pliku DLL lub EXE załadowana w debugowanym procesie. Aby uzyskać więcej informacji, zobacz [porady: Korzystanie z okna modułów](../debugger/how-to-use-the-modules-window.md).  
 Aby debuger dołączał do kodu napisanego w języku C++, kod musi wysyłać właściwość `DebuggableAttribute`. Można dodać to w kodzie automatycznie przez powiązanie z [/assemblydebug](/cpp/build/reference/assemblydebug-add-debuggableattribute) — opcja konsolidatora.  
  
##  <a name="vxtskdebuggingdllprojectsmixedmodedebugging"></a> Debugowanie w trybie mieszanym  
 Aplikacja wywołująca, która wywołuje bibliotekę DLL można pisać w kodzie zarządzanym lub kodzie natywnym. Jeśli zarządzana biblioteka DLL jest wywoływana przez kod macierzysty i chcesz debugować oba, zarządzane i natywne debugery należy włączyć. Można wybrać w  **\<Projekt > strony właściwości** lub oknie dialogowym. Jak to zrobić, zależy od tego, czy rozpoczynasz debugowanie z projektu DLL lub wywoływania projektu aplikacji. Aby uzyskać więcej informacji, zobacz [porady: debugowanie w trybie mieszanym](../debugger/how-to-debug-in-mixed-mode.md).  
  
##  <a name="vxtskdebuggingdllprojectschangingdefaultconfigurations"></a> Zmiana konfiguracji domyślnych  
 Po utworzeniu projektu aplikacji konsolowej przy użyciu szablonu projektu [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] automatycznie tworzy wymagane ustawienia konfiguracji Debug i Release. Jeśli to konieczne, możesz zmienić te ustawienia. Aby uzyskać więcej informacji, zobacz [ustawienia projektu dla konfiguracji debugowania języka C++](../debugger/project-settings-for-a-cpp-debug-configuration.md), [ustawienia projektu dla języka C# Debuguj konfiguracje](../debugger/project-settings-for-csharp-debug-configurations.md), [ustawienia projektu dla konfiguracji debugowania języka Visual Basic ](../debugger/project-settings-for-a-visual-basic-debug-configuration.md), i [jak: Ustaw wartość Debug i Release konfiguracje](../debugger/how-to-set-debug-and-release-configurations.md).  
  
##  <a name="vxtskdebuggingdllprojectswaystodebugthedll"></a> Sposoby debugowania DLL  
 Każdy z projektów w tej sekcji tworzy bibliotekę DLL. Nie można uruchomić biblioteki DLL bezpośrednio; musi zostać wywołany przez aplikację, zwykle EXE. Aby uzyskać więcej informacji, zobacz [tworzenie i zarządzanie projekty języka Visual C++](/cpp/ide/creating-and-managing-visual-cpp-projects). Aplikacja wywołująca może spełniać dowolne spośród następujących kryteriów:  
  
- Aplikacja utworzona w innym projekcie, w tym samym [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] rozwiązanie, które zawiera bibliotekę klas.  
  
- Istniejącą aplikację już wdrożona na komputerze testowym lub produkcyjnym.  
  
- Znajduje się w sieci Web i dostępne za pośrednictwem adresu URL.  
  
- Aplikacja sieci Web zawierającą stronę sieci Web, która osadza biblioteki DLL.  
  
###  <a name="vxtskdebuggingdllprojectsthecallingapplication"></a> Debugowanie aplikacji wywołującej  
Aby debugować bibliotekę DLL, należy uruchomić debugowanie aplikacji wywołującej, zazwyczaj pliku EXE albo aplikacji sieci Web. Istnieje kilka sposobów jej debugowania.  
  
- Jeśli masz projekt dla aplikacji wywołującej, możesz otworzyć ten projekt i rozpocząć wykonywanie z **debugowania** menu. Aby uzyskać więcej informacji, zobacz [wprowadzenie do debugera](../debugger/getting-started-with-the-debugger.md).  
  
- Jeśli aplikacja wywołująca jest istniejący program już wdrożona na komputerze testowym lub produkcyjnym i działa już można dołączyć do niego. Użyj tej metody, jeśli biblioteka DLL jest formantem obsługiwanym przez program Internet Explorer lub formantem na stronie sieci Web. Aby uzyskać więcej informacji, zobacz [porady: dołączanie do procesu uruchamiania](../debugger/attach-to-running-processes-with-the-visual-studio-debugger.md).  
  
- Można to debugować z projektu DLL. Aby uzyskać więcej informacji, zobacz [porady: debugowanie z projektu DLL](../debugger/how-to-debug-from-a-dll-project.md).  
  
- Można to debugować z [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] [bezpośrednim](#vxtskdebuggingdllprojectstheimmediatewindow). W tym przypadku **bezpośrednie** okna odgrywa rolę aplikacji.  
  
Przed rozpoczęciem debugowania aplikacji wywołującej, zazwyczaj można ustawić punkt przerwania w bibliotece klas. Aby uzyskać więcej informacji, zobacz [przy użyciu punktów przerwania](../debugger/using-breakpoints.md). Po osiągnięciu punktu przerwania można przechodzić przez kod, obserwując działanie w każdym wierszu, dopóki nie można ustalić przyczynę problemu. Aby uzyskać więcej informacji, zobacz [Przechodzenie do kodu w debugerze](../debugger/navigating-through-code-with-the-debugger.md).
  
###  <a name="vxtskdebuggingdllprojectstheimmediatewindow"></a> Okno bezpośrednie  
 Będziesz w stanie ocenić funkcje lub metody w DLL bez wywoływana aplikacji. Możesz zrobić, debugowanie w czasie projektowania i używasz **bezpośrednie** okna. Aby debugować w ten sposób, wykonaj następujące kroki, podczas gdy projekt DLL jest otwarty:  
  
1.  Otwórz narzędzie Debugger **bezpośrednie** okna.  
  
2.  Aby przetestować metodę o nazwie `Test` w klasie `Class1`, tworzenia wystąpienia obiektu typu `Class1` , wpisując następujący kod C# w oknie bezpośrednim. Ten kod zarządzany działa dla języka Visual Basic i C++ po odpowiednich zmianach składni:  
  
    ```cpp
    Class1 obj = new Class1();  
    ```  
  
     W języku C# wszystkie nazwy muszą być w pełni kwalifikowana. Ponadto wszelkie metody lub zmienne muszą być w bieżącym zakresie i kontekście sesji debugowania.  
  
3.  Przy założeniu, że `Test` ma jedną `int` parametru oceny `Test` przy użyciu **bezpośrednie** okna:  
  
    ```cpp
    ?obj.Test(10)  
    ```  
  
     Wynik zostanie wydrukowany w **bezpośrednie** okna.  
  
4.  Można kontynuować debugowanie `Test` umieszczając znajdującym się w nim punkt przerwania, a następnie ponownie oceniając funkcję:  
  
    ```cpp
    ?obj.Test(10);  
    ```  
  
     Punkt przerwania zostanie osiągnięty i będzie można krokowo `Test`. Po zakończeniu realizacji `Test`, debuger będzie ponownie w trybie projektowania.

## <a name="vxtskdebuggingdllprojectsexternal"></a> Debugowanie zewnętrznej biblioteki DLL z projektu w języku C++

Jeśli projekt jest debugowany zewnętrznej biblioteki DLL, zależy od funkcji debugowania (takich jak krokowe wykonywanie kodu) [konfiguracji debugowania biblioteki dll](#vxtskdebuggingdllprojectsbuildingadebugversion) została skompilowana i czy [plik .pdb](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md) i inne wymagane pliki dla biblioteki DLL są dostępne.

Projekt, trzeba będzie mógł odnaleźć biblioteki DLL i pliku .pdb używana do debugowania. Można utworzyć zadanie niestandardowej kompilacji, aby skopiować te pliki  **\<folderu projektu > \Debug** folderu wyjściowego, lub skopiować pliki do folderu wyjściowego ręcznie.

Łatwo można ustawić lokalizacje plików nagłówkowych i <em>pliki .lib na stronach właściwości (kliknij prawym przyciskiem myszy projekt C++, a następnie wybierz ** Właściwości widoku</em><em>, a następnie wybierz pozycję **wszystkie konfiguracje</em>* ) bez konieczności skopiuj je do folderu wyjściowego:

- Folder C/C++ (Kategoria Ogólne) — określ folder zawierający pliki nagłówków w **dodatkowe katalogi dołączenia** pola.
- Folder łączący (Kategoria Ogólne) — określ folder zawierający plik .lib w **dodatkowe katalogi bibliotek** pola. 
- Folder łączący (kategoria danych wejściowych) — określ pełną ścieżkę i nazwę pliku .lib w **dodatkowe zależności** pola.

Jeśli konfiguracja jest prawidłowa, możesz debugować poprzez uruchomienie wykonywanie z **debugowania** menu.

Aby uzyskać więcej informacji na temat ustawień projektu, zobacz [strony właściwości (Visual C++)](/cpp/ide/property-pages-visual-cpp).
  
## <a name="see-also"></a>Zobacz też  
 [Debugowanie zarządzanego kodu](../debugger/debugging-managed-code.md)   
 [Typy projektów Visual C++](../debugger/debugging-preparation-visual-cpp-project-types.md)   
 [C#, F # i typów projektów języka Visual Basic](../debugger/debugging-preparation-csharp-f-hash-and-visual-basic-project-types.md)   
 [Ustawienia projektu dla konfiguracji debugowania języka C++](../debugger/project-settings-for-a-cpp-debug-configuration.md)   
 [Ustawienia projektu dla języka C# konfiguracji debugowania](../debugger/project-settings-for-csharp-debug-configurations.md)   
 [Ustawienia projektu dla języka Visual Basic konfiguracji debugowania](../debugger/project-settings-for-a-visual-basic-debug-configuration.md)   
 [Zabezpieczenia debugera](../debugger/debugger-security.md)
