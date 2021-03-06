---
title: Projektant przepływu pracy — InvokeDelegate
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
ms.technology: vs-workflow-designer
f1_keywords:
- InvokeDelegate Designer
- System.Activities.Statements.InvokeDelegate.UI
ms.assetid: 289a7498-5127-453f-beb5-05f05b80d26f
ms.author: gewarren
manager: douge
ms.workload:
- multiple
author: gewarren
ms.openlocfilehash: 1e1f91b88d686f3e9a6ddee9573824eb4191e2bf
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49927934"
---
# <a name="invokedelegate"></a>InvokeDelegate

**InvokeDelegate** projektanta jest używany do tworzenia i konfigurowania <xref:System.Activities.Statements.InvokeDelegate> działania.

## <a name="the-invokedelegate-activity"></a>Działanie InvokeDelegate

<xref:System.Activities.Statements.InvokeDelegate> Wywołuje Delegat publiczny.

### <a name="use-the-invokedelegate-activity-designer"></a>Użyj InvokeDelegate Projektant działań

Dostęp do **InvokeDelegate** projektanta działań w **podstawowych** kategorii **przybornika**. **InvokeDelegate** projektanta działań mogą być przeciągnięte z **przybornika** i porzucić do powierzchni projektanta przepływów pracy, gdzie odkąd działań są zazwyczaj umieszczane, takie jak wewnątrz <xref:System.Activities.Statements.Sequence>. Projektant działań porzucenie tworzy <xref:System.Activities.Statements.InvokeDelegate> działanie przy użyciu domyślnego <xref:System.Activities.Activity.DisplayName%2A> z InvokeDelegate. <xref:System.Activities.Activity.DisplayName%2A> Mogą być edytowane w nagłówku **InvokeDelegate** projektanta działań lub **DisplayName** pola siatki właściwości.

### <a name="the-invokedelegate-properties"></a>Właściwości InvokeDelegate

W poniższej tabeli przedstawiono <xref:System.Activities.Statements.InvokeDelegate> właściwości i w tym artykule opisano, jak są używane w projektancie. Te właściwości można edytować w siatce właściwości, a niektóre z nich mogą być edytowane na powierzchni projektanta przepływów pracy.

|Nazwa właściwości|Wymagane|Użycie|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|Przyjazna nazwa <xref:System.Activities.Statements.InvokeDelegate> działania. Wartość domyślna to InvokeDelegate.<br /><br /> Mimo że <xref:System.Activities.Activity.DisplayName%2A> nie jest ściśle wymagane, zaleca się go użyć.|
|<xref:System.Activities.Statements.InvokeDelegate.Delegate%2A>|True|Nazwa <xref:System.Activities.ActivityDelegate> wywoływana, gdy działanie wykonuje. Ta właściwość może być edytowany na powierzchni projektanta i jest wymagana.|
|<xref:System.Activities.Statements.InvokeDelegate.DelegateArguments%2A>|False|Kolekcja argument wywoływany delegat. Klucze są nazwy obiektów parametru na <xref:System.Activities.ActivityDelegate>, a ich wartości są argumenty, których wyrażenia są obliczane i przypisane do odpowiednich obiektów parametru. Aby wyświetlić **DelegateArguments** okna dialogowego, w którym można ustawić tę właściwość, kliknij przycisk wielokropka w **DelegateArguments** pola siatki właściwości. Kliknij przycisk **Utwórz Argument** pola w celu dodania argumenty.|

## <a name="see-also"></a>Zobacz także

- [Instrukcje: Definiowanie i stosowanie delegowania działania w Projektancie przepływu pracy](../workflow-designer/how-to-define-and-consume-activity-delegates-in-the-workflow-designer.md)