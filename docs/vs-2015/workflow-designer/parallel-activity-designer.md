---
title: Parallel, Projektant działań | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: .net-framework-4.6
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- System.Activities.Statements.Parallel.UI
ms.assetid: 0306dc3b-075a-4091-ac3a-96486fbabed5
caps.latest.revision: 10
author: gewarren
ms.author: gewarren
manager: erikre
ms.openlocfilehash: f557eb013cb313321b336fb22fd1299e51faaa82
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49221585"
---
# <a name="parallel-activity-designer"></a>Parallel, projektant działań
<xref:System.Activities.Statements.Parallel> Działanie jest wykonywane równocześnie zbiór działań podrzędnych.  
  
## <a name="the-parallel-activity"></a>Działanie równoległe  
 <xref:System.Activities.Statements.Parallel> Działania przechowuje działania podrzędne w <xref:System.Activities.Statements.Parallel.Branches%2A> kolekcji. Użyj <xref:System.Activities.Statements.Parallel> działania zamiast <xref:System.Activities.Statements.Sequence> działanie w przypadku niektórych działań podrzędnych może być bezczynny.  
  
 <xref:System.Activities.Statements.Parallel> Działanie ma <xref:System.Activities.Statements.Parallel.CompletionCondition%2A> właściwość, która zawiera określone przez użytkownika [!INCLUDE[vbprvb](../includes/vbprvb-md.md)] wyrażenia. <xref:System.Activities.Statements.Parallel> Działania daje w wyniku tej właściwości po zakończeniu każdej gałęzi. Jeśli daje w wyniku **True**, a następnie <xref:System.Activities.Statements.Parallel> działanie zakończy się bez wykonania innych działów. Jeśli <xref:System.Activities.Statements.Parallel.CompletionCondition%2A> nie można rozpoznać **True**, a następnie <xref:System.Activities.Statements.Parallel> ukończeniu działania, gdy wszystkie działania podrzędne zostały ukończone.  
  
### <a name="using-the-parallel-activity-designer"></a>Za pomocą Parallel, Projektant działań  
 **Równoległe** projektanta działań można znaleźć w **przepływ sterowania** kategorii **przybornika**, które jest dostępne po kliknięciu **przybornika**karty w lewej części [!INCLUDE[wfd2](../includes/wfd2-md.md)] (można także wybrać **narzędzi** z **widoku** menu lub klawiszy CTRL + ALT + X.)  
  
 **Równoległe** projektanta działań mogą być przeciągnięte z **przybornika** i porzuconych do [!INCLUDE[wfd2](../includes/wfd2-md.md)] powierzchni wszędzie tam, gdzie Projektanci działań są zazwyczaj umieszczone, na przykład wewnątrz **Sekwencji** projektanta działań. Po upuszczając go do [!INCLUDE[wfd2](../includes/wfd2-md.md)], tworzy on <xref:System.Activities.Statements.Parallel> działania, które domyślnie zawiera <xref:System.Activities.Activity.DisplayName%2A> z **równoległe**  
  
 Aby dodać działanie, aby <xref:System.Activities.Statements.Parallel.Branches%2A> kolekcji aktywności równoległej, przeciągnij niektóre projektanta działań z **przybornika** i upuść je na trójkąt wewnątrz **równoległe** Projektant działań. Trójkąty części bocznej działań zawartych w gałęzi. Można dodawać dodatkowe działania, powtarzając tej procedury. Działania można zmienić kolejności, przez przeciąganie i upuszczanie ich w ramach **równoległe** projektanta działań.  
  
### <a name="parallel-activity-properties-in-the-workflow-designer"></a>Właściwości działania równoległe w Projektancie przepływu pracy  
 Poniższa tabela pokazuje właściwości działań równoległych i w tym artykule opisano, jak są używane w projektancie.  
  
|Nazwa właściwości|Wymagane|Użycie|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|Określa przyjazną nazwę wyświetlaną projektanta działań w nagłówku. Wartość domyślna to **równoległe**. Wartość może być opcjonalnie edytować w **właściwości** siatki lub bezpośrednio w nagłówku projektanta działań.|  
|<xref:System.Activities.Statements.Parallel.Branches%2A>|True|Zawiera kolekcję działania podrzędne do wykonania.|  
|<xref:System.Activities.Statements.Parallel.CompletionCondition%2A>|False|Oceniane, po zakończeniu gałęzi. Jeśli daje w wyniku **True**, następnie zaplanowane oczekujące gałęzie zostały anulowane. Jeśli ta właściwość nie jest ustawiona lub daje w wyniku **False**, działanie zakończy się po zakończeniu wszystkich swoich działań podrzędnych. Wartość domyślna to **null**.|  
  
## <a name="see-also"></a>Zobacz też  
 [Sekwencja](../workflow-designer/sequence-activity-designer.md)   
 [ParallelForEach\<T >](../workflow-designer/parallelforeach-t-activity-designer.md)   
 [Przepływ sterowania](../workflow-designer/control-flow-activity-designers.md)