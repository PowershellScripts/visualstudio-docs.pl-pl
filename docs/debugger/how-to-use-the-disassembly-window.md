---
title: Wyświetlanie kodu dezasemblacji w debugerze programu Visual Studio | Dokumentacja firmy Microsoft
ms.custom: H1Hack27Feb2017
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.disassembly
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- assembly language, debugging inline assembly code
- breakpoints, Disassembly window
- Disassembly window
- machine code
ms.assetid: eaf84dd0-c82d-481b-af51-690b74e7794c
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 9b4d9eb1b9484206d3a7d880ec13378693930a63
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49917326"
---
# <a name="view-disassembly-code-in-the-visual-studio-debugger"></a>Wyświetlanie kodu dezasemblacji w debugerze programu Visual Studio
Ta funkcja jest dostępna tylko wtedy, gdy włączone jest debugowanie na poziomie adresów **opcje** okno dialogowe **debugowanie** węzła. Nie jest dostępna do debugowania skryptów lub SQL.  
  
 **Dezasemblacji** okno pokazuje kod zestawu odpowiadający instrukcjom utworzonym przez kompilator. Jeśli debugujesz kod zarządzany w instrukcjach zestawu odnoszą się do kodu macierzystego, utworzony przez kompilator Just-in-Time (JIT), a nie języka Microsoft intermediate language (MSIL) generowany przez kompilator programu Visual Studio.  
  
 Oprócz instrukcje montażu **dezasemblacji** okna można wyświetlić następujące informacje opcjonalne:  
  
- Adres pamięci, w którym znajduje się każdą instrukcję. Dla natywnych aplikacji jest to adres pamięci rzeczywistych. W przypadku języka Visual Basic, C# lub kodu zarządzanego jest przesunięcie od początku funkcji.  
  
- Kod źródłowy, z którego pochodzi kod zestawu.  
  
- Bajty kodu — bajtów reprezentujących rzeczywistą lub instrukcji MSIL.  
  
- Nazwy symboli dla adresów pamięci.  
  
- Numery wierszy odpowiadających do kodu źródłowego.  
  
  Instrukcje języka asemblera składają się z klawiszy skrótu skrótów dla instrukcji nazwy i symbole, które reprezentują zmiennych, rejestrów i stałe. Każdą instrukcję języka maszyny jest reprezentowany przez jeden język asemblera skrót klawiszowy, zwykle następuje jeden lub więcej zmiennych, rejestrów lub stałe.  
  
  Jeśli nie można odczytać języka asembler i chcesz w pełni korzystać z okna dezasemblacji, zapoznaj się z dobrej książki na programowania języka asemblera. Język asemblera programowania jest poza zakres, w jaki firma Microsoft adres, w tym krótkie wprowadzenie do okna dezasemblacji.  
  
  Ponieważ kod zestawu rolę odgrywa w rejestrach procesora lub, w przypadku kodu zarządzanego, rejestruje środowiska uruchomieniowego języka wspólnego, użytkownik będzie często przydatne może użyć okna dezasemblacji w połączeniu z okna rejestrów, dzięki czemu można zbadać rejestr zawartość.  
  
  Prawdopodobnie będzie nigdy nie masz pragnienie lub konieczne wyświetlenie kodu maszynowego instrukcje w ich pierwotne, numerycznego formularza, a nie języka asemblera. Jednak jeśli chcesz to zrobić, możesz użyć okna pamięci, w tym celu lub wybrać bajty kodu z menu skrótów w oknie demontażu.  
  
> [!NOTE]
>  Okna dialogowe i polecenia menu mogą się różnić od tych opisanych w Pomocy, w zależności od ustawień aktywnych lub wydania. Aby zmienić swoje ustawienia, wybierz opcję **Import i eksport ustawień** na **narzędzia** menu. Aby uzyskać więcej informacji, zobacz [personalizowanie środowiska IDE programu Visual Studio](../ide/personalizing-the-visual-studio-ide.md).  
  
### <a name="to-display-the-disassembly-window"></a>Aby wyświetlić okno dezasemblacji  
  
-   Podczas debugowania, wybierz **Debuguj > Windows** a następnie kliknij przycisk **dezasemblacji**.
  
### <a name="to-turn-optional-information-on-or-off"></a>Aby włączyć informacje opcjonalne lub wyłączyć  
  
-   Kliknij prawym przyciskiem myszy **dezasemblacji** oknie i ustawić lub wyczyścić odpowiednie opcje w menu skrótów.  
  
     Żółta strzałka na lewym marginesie oznacza lokalizację bieżący punkt wykonania. Dla kodu natywnego odpowiada to licznik programu procesora CPU. Ta lokalizacja zawiera następnej instrukcji, która zostanie wykonana w programach.  
  
     Aby uzyskać więcej informacji, zobacz [stronicowanie w górę lub w dół w pamięci](../debugger/how-to-page-up-or-down-in-memory.md).  
  
## <a name="see-also"></a>Zobacz też  
 [Wyświetlanie danych w debugerze](../debugger/viewing-data-in-the-debugger.md)   
 [Instrukcje: korzystanie z okna rejestrów](../debugger/how-to-use-the-registers-window.md)