---
title: Opcje, edytor tekstu, C#, zaawansowane
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Text_Editor.CSharp.Outlining
- VS.ToolsOptionsPages.Text_Editor.CSharp.Advanced
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: 16c92111fc29071447d4af5e736b881fa7c7a769
ms.sourcegitcommit: e680e8ac675f003ebcc8f8c86e27f54ff38da662
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/16/2018
ms.locfileid: "49356746"
---
# <a name="options-text-editor-c-advanced"></a>Opcje, edytor tekstu, C#, zaawansowane

Użyj **zaawansowane** Strona opcji, aby modyfikować ustawienia formatowania edytora, refaktoryzacji kodu i komentarze dokumentacji XML dla języka C#. Dostępu do tej opcji strony, wybierz **narzędzia** > **opcje**, a następnie wybierz **edytora tekstów** > **C#**  >  **Zaawansowane**.

> [!NOTE]
> Nie wszystkie opcje mogą być wymienione w tym miejscu.

## <a name="analysis"></a>Analiza

- Włączanie pełnej analizy rozwiązania

   Włącza analizę kodu dla wszystkich plików w rozwiązaniu, nie wystarczy otworzyć plików kodu. Aby uzyskać więcej informacji, zobacz [pełnej analizy rozwiązania](../../code-quality/how-to-enable-and-disable-full-solution-analysis-for-managed-code.md).

## <a name="using-directives"></a>Dyrektywy Using

- Umieść najpierw dyrektywy "System" podczas sortowania deklaracji Using

   Po wybraniu **Usuń i Sortuj wyrażenia Using** w sortuje menu kliknij prawym przyciskiem myszy polecenie `using` dyrektywy i miejsc przestrzeni nazw "System" w górnej części listy

   Przed rozpoczęciem sortowania:

   ```csharp
   using AutoMapper;
   using FluentValidation;
   using System.Collections.Generic;
   using System.Linq;
   using Newtonsoft.Json;
   using System;
   ```
   
   Po sortowaniu:

   ```csharp
   using System;
   using System.Collections.Generic;
   using System.Linq;
   using AutoMapper;
   using FluentValidation;
   using Newtonsoft.Json;
   ```
   
- Oddziel grupy dyrektywy using

   Po wybraniu **Usuń i Sortuj wyrażenia Using** oddziela polecenia w menu kliknij prawym przyciskiem myszy `using` dyrektyw, wstawiając pusty wiersz między grupami dyrektyw, które mają ten sam głównej przestrzeni nazw.

   Przed rozpoczęciem sortowania:

   ```csharp
   using AutoMapper;
   using FluentValidation;
   using System.Collections.Generic;
   using System.Linq;
   using Newtonsoft.Json;
   using System;
   ```
   
   Po sortowaniu:
   
   ```csharp
   using AutoMapper;
   
   using FluentValidation;
   
   using Newtonsoft.Json;
   
   using System;
   using System.Collections.Generic;
   using System.Linq;
   ```
   
- Dodaj dyrektywy Using dla typów odwołań do zestawów i pakietów NuGet 

   Po wybraniu [szybka akcja](../quick-actions.md) jest dostępna zainstalować pakiet NuGet i dodać `using` dyrektywy dla typów bez odwołań.

   ![Szybkie działanie, aby zainstalować pakiet NuGet w programie Visual Studio](media/nuget-lightbulb.png)
  
## <a name="highlighting"></a>Wyróżnianie

- Wyróżnij odwołania do symbolu pod kursorem

   Gdy kursor znajduje się wewnątrz symbolu lub po kliknięciu symbolu, zostały wyróżnione wszystkich wystąpień symbolu w pliku kodu.

## <a name="outlining"></a>Tworzenie konspektu

- Przejdź do trybu konspektu po otwarciu plików

   Po wybraniu automatycznie przedstawia plik kodu, który tworzy zwijany bloków kodu. Przy pierwszym otwarciu pliku #regions bloków i bloków nieaktywnego kodu Zwiń.

## <a name="editor-help"></a>Pomoc Edytora

- Generowanie komentarzy dokumentacji XML dla / / /

   Po wybraniu Wstawia elementy XML dla komentarzy dokumentacji XML po wpisaniu `///` wprowadzenie komentarza. Aby uzyskać więcej informacji na temat dokumentacji XML, zobacz [komentarze dokumentacji XML (C# Programming Guide)](/dotnet/csharp/programming-guide/xmldoc/xml-documentation-comments).

## <a name="see-also"></a>Zobacz także

- [Porady: wstawianie komentarzy XML do generowania dokumentacji](../../ide/reference/generate-xml-documentation-comments.md)
- [Komentarze dokumentacji XML (C# Programming Guide)](/dotnet/csharp/programming-guide/xmldoc/xml-documentation-comments)
- [Dokumentowanie kodu przy użyciu komentarzy XML (Przewodnik C#)](/dotnet/csharp/codedoc)
- [Ustawianie opcji edytora specyficznych dla języka](../../ide/reference/setting-language-specific-editor-options.md)
- [C# IntelliSense](../../ide/visual-csharp-intellisense.md)
