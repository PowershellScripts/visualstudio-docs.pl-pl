---
title: "Projektant działań PickBranch | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: System.Activities.Statements.PickBranch.UI
ms.assetid: f523ad47-bbc0-4cda-a35c-41e67c4ba081
caps.latest.revision: "10"
author: ErikRe
ms.author: erikre
manager: erikre
ms.openlocfilehash: 9a77adbe5e2663ef11242d162b6ac718d88daea5
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2017
---
# <a name="pickbranch-activity-designer"></a>Projektant działań PickBranch
<xref:System.Activities.Statements.PickBranch> Zapewnia oparte na zdarzeniu ścieżkę wykonywania w <xref:System.Activities.Statements.Pick> działanie, które mogą być wyzwalane przez zdarzenia przychodzącego.  
  
## <a name="pickbranch"></a>PickBranch  
 <xref:System.Activities.Statements.PickBranch>obiekty są zawarte w <xref:System.Activities.Statements.Pick.Branches%2A> Kolekcja <xref:System.Activities.Statements.Pick> działania. Każdy <xref:System.Activities.Statements.PickBranch> znajduje się w gałęzi <xref:System.Activities.Statements.Pick> działania i mogą być wykonywane z powodu niektóre zdarzenia przychodzącego, która służy jako wyzwalacz. W ten sposób [!INCLUDE[wfd1](../workflow-designer/includes/wfd1_md.md)] udostępnia modelowanie przepływu sterowania opartego na zdarzeniach. Każdy <xref:System.Activities.Statements.PickBranch> zawiera <xref:System.Activities.Statements.PickBranch.Trigger%2A> i <xref:System.Activities.Statements.PickBranch.Action%2A>.  
  
### <a name="how-to-use-the-pick-activity-designer"></a>Jak używać Projektant działań pobrania  
 **PickBranch** designer znajduje się w **przepływ sterowania** kategorii **przybornika**, które jest dostępne po kliknięciu **przybornika** Karta na [!INCLUDE[wfd2](../workflow-designer/includes/wfd2_md.md)] (można także wybrać **narzędzi** z **widoku** menu lub CTRL + ALT + X).  
  
 Dwa puste <xref:System.Activities.Statements.PickBranch> obiekty o wyświetlić nazwy **Branch1** i **Branch2** jest tworzonych domyślnie jako elementy <xref:System.Activities.Statements.Pick> działania podczas **wybierz** Projektant działań początkowo jest przenoszony do [!INCLUDE[wfd2](../workflow-designer/includes/wfd2_md.md)]. Te odpowiednich <xref:System.Activities.Statements.PickBranch.DisplayName%2A> wartości właściwości mogą być edytowane w **PickBranch** projektanta nagłówka lub poziomu **właściwości** okna dla każdej gałęzi.  
  
 Istnieją dwa sposoby dodawania <xref:System.Activities.Statements.PickBranch> obiekty do kolekcji <xref:System.Activities.Statements.Pick> obiektu: przeciąganie i upuszczanie **PickBranch** projektanta z **przybornika** lub korzystając z menu kontekstowego w ramach **wybierz** powierzchni projektu:  
  
1.  **PickBranch** Projektant <xref:System.Activities.Statements.PickBranch> kiedy zostanie przeciągnięty z **przybornika** i upuścić na jednej z gałęzi **wybierz** Projektant działań na [!INCLUDE[wfd2](../workflow-designer/includes/wfd2_md.md)] powierzchni. Nowy <xref:System.Activities.Statements.PickBranch> obiekty mogą być umieszczony wewnątrz <xref:System.Activities.Statements.Pick> projektanta po lewej lub prawej wszelkie istniejące <xref:System.Activities.Statements.PickBranch> elementy znajdujące się już w kolekcji. Podczas przeciągania **PickBranch** projektanta na **wybierz** projektanta za pomocą myszy **wybierz** projektanta używa pionowy pasek szary blue wskaż, gdzie <xref:System.Activities.Statements.PickBranch> jest dodawany do położenia danej myszy.  
  
2.  Kliknij prawym przyciskiem myszy **wybierz** Projektant działań (, ale nie do wewnątrz **PickBranch** designer) uzyskać menu kontekstowe i wybierz **utwórz gałąź** Aby dodać nowy <xref:System.Activities.Statements.PickBranch>. Zwróć uwagę, że nowe <xref:System.Activities.Statements.PickBranch> jest dodawany do prawej istniejącej <xref:System.Activities.Statements.PickBranch> obiekty w **wybierz** projektanta.  
  
 **PickBranch** projektanta można rozszerzyć, aby ujawnić **wyzwalacza** i **akcji** pola lub zwinięte, klikając podwójne daszka po prawej stronie ich nagłówki. Edytuj <xref:System.Activities.Statements.PickBranch.Trigger%2A> i <xref:System.Activities.Statements.PickBranch.Action%2A> każdego <xref:System.Activities.Statements.PickBranch> upuszczając działań do **wyzwalacza** i **akcji** pola ich projektantów.  
  
 <xref:System.Activities.Statements.PickBranch> Obiekty w <xref:System.Activities.Statements.Pick.Branches%2A> Kolekcja <xref:System.Activities.Statements.Pick> obiektów, można zmienić kolejności przez przeciąganie i upuszczanie je do nowej lokalizacji w ramach **wybierz** projektanta. **Wybierz** projektanta używa pionowy pasek szary blue wskaż, gdzie <xref:System.Activities.Statements.PickBranch> jest dodawany do umieszczenia danego myszy.  
  
 Istnieją dwa sposoby, aby usunąć <xref:System.Activities.Statements.PickBranch>:  
  
1.  Wybierz **PickBranch** projektanta i usuń go.  
  
2.  Wybierz **PickBranch** projektanta, kliknij prawym przyciskiem myszy uzyskać menu kontekstowe i wybierz **usunąć**.  
  
 Należy wybrać **PickBranch** projektanta, jak wybrać jedną z działań wewnątrz jego **wyzwalacza** lub **akcji** pola przez pomyłkę usuwa jeden z tych działań i nie <xref:System.Activities.Statements.PickBranch> obiektu.  
  
### <a name="pickbranch-properties-in-the-workflow-designer"></a>Właściwości PickBranch w Projektancie przepływów pracy  
 W poniższej tabeli przedstawiono najbardziej przydatne <xref:System.Activities.Statements.PickBranch> właściwości oraz opis sposobu korzystania z nich w [!INCLUDE[wfd2](../workflow-designer/includes/wfd2_md.md)].  
  
|Nazwa właściwości|Wymagane|Użycie|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Statements.PickBranch.DisplayName%2A>|False|Przyjazna nazwa wyświetlana w nagłówku **PickBranch** projektanta. Wartość domyślna to gałęzi.<br /><br /> Mimo że <xref:System.Activities.Activity.DisplayName%2A> nie jest ścisłym wymogiem jest najlepszym rozwiązaniem jej użyć.|  
|<xref:System.Activities.Statements.PickBranch.Trigger%2A>|Wartość true|Każdy <xref:System.Activities.Statements.PickBranch> zawiera <xref:System.Activities.Statements.PickBranch.Trigger%2A> akcji, które może wywołać <xref:System.Activities.Statements.PickBranch.Action%2A>.|  
|<xref:System.Activities.Statements.PickBranch.Action%2A>|False|Każdy <xref:System.Activities.Statements.PickBranch> zawiera <xref:System.Activities.Statements.PickBranch.Action%2A> wykonaniu Jeśli wyzwolone.|  
  
## <a name="see-also"></a>Zobacz też  
 [Przepływ sterowania](../workflow-designer/control-flow-activity-designers.md)   
 [Wybierz działanie](/dotnet/framework/windows-workflow-foundation/pick-activity)   
 [Przy użyciu działaniu wybierz](/dotnet/framework/windows-workflow-foundation/samples/using-the-pick-activity)