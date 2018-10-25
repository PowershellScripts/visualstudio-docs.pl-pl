---
title: Tworzenie niestandardowych Wizualizatorów danych | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 06/19/2017
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.visualizer.troubleshoot
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- debugger, visualizers
- visualizers
ms.assetid: c24c006f-f2ac-429f-89db-677fc0c6e1ea
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 859bf6493a06663a8977898ffa07d600b826d458
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49854315"
---
# <a name="create-custom-visualizers-of-data"></a>Tworzenie niestandardowych Wizualizatorów danych
 Wizualizatory są składnikami [!INCLUDE[vs_current_short](../code-quality/includes/vs_current_short_md.md)] interfejs użytkownika debugera. A *Wizualizator* tworzy okno dialogowe lub inny interfejs do wyświetlania zmiennej lub obiektu w sposób, który jest odpowiedni do jego typu danych. Na przykład wizualizatora HTML interpretuje ciąg HTML i wyświetla wynik, jak będzie wyglądał w oknie przeglądarki; Wizualizator mapy bitowej interpretuje strukturę mapy bitowej i wyświetla grafiki, którą reprezentuje. Niektóre wizualizatorów umożliwiają modyfikowanie, a także wyświetlić dane.

 [!INCLUDE[vs_current_short](../code-quality/includes/vs_current_short_md.md)] Debugera zawiera sześć wizualizatorów standardowych. Są to tekst, HTML, XML i JSON wizualizatorów, z których wszystkie pracować nad obiektów w postaci ciągów; z wizualizatora drzewa WPF, do wyświetlania właściwości WPF drzewa wizualnego w obiekcie; i Wizualizator zestawu danych, która działa w przypadku obiektów DataSet, DataView i DataTable. Dodatkowe wizualizatorów mogą być dostępne do pobrania firmy Microsoft Corporation w przyszłości i są dostępne w innych firm i społeczności. Ponadto możesz napisać własne wizualizatorów i zainstalować je w [!INCLUDE[vs_current_short](../code-quality/includes/vs_current_short_md.md)] debugera.

 > [!NOTE]
 > Aby utworzyć niestandardowego wizualizatora dla kodu natywnego, zobacz [uproszczony Wizualizator debugowania natywnego oprogramowania SQLite](https://github.com/Microsoft/VSSDK-Extensibility-Samples/tree/master/SqliteVisualizer) próbki. W aplikacjach platformy uniwersalnej systemu Windows i Windows 8.x wizualizatory niestandardowe nie są obsługiwane.

 W debugerze, wizualizatory są reprezentowane przez ikonę lupy ![VisualizerIcon](../debugger/media/dbg-tips-visualizer-icon.png "ikonę Wizualizator"). Po wyświetleniu ikoną lupy w **DataTip**, w oknie debugera, takie jak **Obejrzyj** oknie lub w **QuickWatch** okno dialogowe, możesz kliknąć ikonę lupy do Wybierz odpowiednie dla typu danych odpowiedniego obiektu wizualizatora.

## <a name="overview-of-custom-visualizers"></a>Omówienie wizualizatory niestandardowe

Możesz napisać niestandardowego wizualizatora obiektu klasy zarządzanej z wyjątkiem <xref:System.Object> lub <xref:System.Array>.  
  
 Architektura wizualizatora debuger ma dwie części:  
  
- *Debugera po stronie* jest uruchamiany w ramach debugera programu Visual Studio. Kod po stronie debugera tworzy i wyświetla interfejsu użytkownika dla usługi wizualizatora.  
  
- *Po stronie debugowanego obiektu* jest uruchamiany w ramach procesu programu Visual Studio debuguje ( *obiekt debugowany*).  
  
  Obiekt danych, które mają być wyświetlane (na przykład obiekt ciągu) istnieje w obiekcie debugowanym procesie. Dlatego po stronie debugowanego obiektu ma wysyłać ten obiekt danych po stronie debugera, który można następnie wyświetlać je za pomocą interfejsu użytkownika, które można utworzyć.  
  
  Po stronie debugera otrzyma ten obiekt danych, aby być wizualizowane z *dostawcy obiektów* implementującej <xref:Microsoft.VisualStudio.DebuggerVisualizers.IVisualizerObjectProvider> interfejsu. Po stronie debugowanego obiektu wysyła obiekt danych za pośrednictwem *źródła obiektu*, który pochodzi od <xref:Microsoft.VisualStudio.DebuggerVisualizers.VisualizerObjectSource>. Dostawcy obiektów można również wysyłać dane z powrotem do źródła obiektu, który umożliwia pisanie wizualizatora, który umożliwia edycję, a także wyświetla dane. Dostawcy obiektów może zostać zastąpiona w celu komunikować Ewaluator wyrażeń i dlatego źródła obiektu  
  
  Po stronie debugowanego obiektu i debuger komunikować się ze sobą za pośrednictwem <xref:System.IO.Stream>. Metody są dostarczane do serializacji obiektu danych do <xref:System.IO.Stream> i deserializacji <xref:System.IO.Stream> do obiektu danych.  
  
  Kod po stronie debugowanego obiektu jest określony za pomocą atrybutu DebuggerVisualizer (<xref:System.Diagnostics.DebuggerVisualizerAttribute>).  
  
  Do tworzenia interfejsu użytkownika wizualizatora po stronie debugera, należy utworzyć klasę, która dziedziczy po elemencie <xref:Microsoft.VisualStudio.DebuggerVisualizers.DialogDebuggerVisualizer> i zastąpić <xref:Microsoft.VisualStudio.DebuggerVisualizers.DialogDebuggerVisualizer.Show%2A?displayProperty=fullName> metodę w celu wyświetlenia interfejsu.  
  
  Możesz użyć <xref:Microsoft.VisualStudio.DebuggerVisualizers.IDialogVisualizerService> do wyświetlania formularzy Windows, okien dialogowych i formantów z Twojej wizualizatora.  
  
  Obsługa typów ogólnych jest ograniczona. Można napisać Wizualizator dla obiektu docelowego, który jest typem ogólnym, tylko wtedy, gdy typ ogólny jest typem otwartym. To ograniczenie jest taka sama jak wartość ograniczenia, korzystając z `DebuggerTypeProxy` atrybutu. Aby uzyskać więcej informacji, zobacz [przy użyciu atrybutu DebuggerTypeProxy](../debugger/using-debuggertypeproxy-attribute.md).  
  
  Wizualizatory niestandardowe mogą mieć zagadnienia związane z zabezpieczeniami. Zobacz [zagadnienia dotyczące zabezpieczeń internetowych](../debugger/visualizer-security-considerations.md).  
  
  Procedury opisane poniżej, zapewniają ogólny widok co należy zrobić, aby utworzyć wizualizatora. Aby uzyskać bardziej szczegółowy opis, zobacz [wskazówki: pisanie wizualizatora w języku C#](../debugger/walkthrough-writing-a-visualizer-in-csharp.md).  
  
### <a name="to-create-the-debugger-side"></a>Aby utworzyć po stronie debugera  
  
1.  Użyj <xref:Microsoft.VisualStudio.DebuggerVisualizers.IVisualizerObjectProvider> metody w celu uzyskania wizualizowanego obiektu po stronie debugera.  
  
2.  Utwórz klasę, która dziedziczy z <xref:Microsoft.VisualStudio.DebuggerVisualizers.DialogDebuggerVisualizer>.  
  
3.  Zastąp <xref:Microsoft.VisualStudio.DebuggerVisualizers.DialogDebuggerVisualizer.Show%2A?displayProperty=fullName> metodę w celu wyświetlenia interfejsu. Użyj <xref:Microsoft.VisualStudio.DebuggerVisualizers.IDialogVisualizerService> metody w celu wyświetlenia formularzy Windows, okien dialogowych i formantów w ramach interfejsu.  
  
4.  Zastosuj <xref:System.Diagnostics.DebuggerVisualizerAttribute>, nadając mu wizualizatora (<xref:Microsoft.VisualStudio.DebuggerVisualizers.DialogDebuggerVisualizer>).  
  
### <a name="to-create-the-debuggee-side"></a>Aby utworzyć po stronie debugowanego obiektu  
  
1.  Zastosuj <xref:System.Diagnostics.DebuggerVisualizerAttribute>, nadając mu wizualizatora (<xref:Microsoft.VisualStudio.DebuggerVisualizers.DialogDebuggerVisualizer>) i źródła obiektu (<xref:Microsoft.VisualStudio.DebuggerVisualizers.VisualizerObjectSource>). Jeżeli pominięto źródła obiektu, będą używane domyślne źródło obiektu  
  
2.  Jeśli chcesz, aby Twoje visualizer, aby można było edytować obiekty danych, również zgodnie z ich, wyświetlić należy zastąpić `TransferData` lub `CreateReplacementObject` metody z <xref:Microsoft.VisualStudio.DebuggerVisualizers.VisualizerObjectSource>.   
  
## <a name="in-this-section"></a>W tej sekcji
  
 [Przewodnik: pisanie wizualizatora w języku C#](../debugger/walkthrough-writing-a-visualizer-in-csharp.md)  

 [Przewodnik: pisanie wizualizatora w języku Visual Basic](../debugger/walkthrough-writing-a-visualizer-in-visual-basic.md)  
  
 [Instrukcje: instalowanie wizualizatora](../debugger/how-to-install-a-visualizer.md)  
  
 [Instrukcje: testowanie i debugowanie wizualizatora](../debugger/how-to-test-and-debug-a-visualizer.md)  
  
 [Interfejs API wizualizatora — dokumentacja](../debugger/visualizer-api-reference.md)  
  
## <a name="related-sections"></a>Sekcje pokrewne  
 [Wyświetlanie danych w debugerze](../debugger/viewing-data-in-the-debugger.md)