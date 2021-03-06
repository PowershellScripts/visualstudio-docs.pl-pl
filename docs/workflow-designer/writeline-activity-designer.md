---
title: Projektant przepływu pracy — WriteLine, Projektant działań
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
ms.technology: vs-workflow-designer
f1_keywords:
- System.Activities.Statements.WriteLine.UI
ms.assetid: 1b5f29a8-b7fd-477e-949e-2f689cae3c96
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: a512288d141823115361bf8eacfd179a74a1da1b
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49876714"
---
# <a name="writeline-activity-designer"></a>WriteLine, projektant działań

**WriteLine** projektanta działań służy do tworzenia i konfigurowania <xref:System.Activities.Statements.WriteLine> działania.

## <a name="the-writeline-activity"></a>Działanie WriteLine

<xref:System.Activities.Statements.WriteLine> Działanie zapisuje tekst na określony <xref:System.IO.TextWriter> obiektu. Jeśli nie <xref:System.IO.TextWriter> jest określony, <xref:System.Activities.Statements.WriteLine> zapisuje tekst w konsoli.

### <a name="using-the-writeline-activity-designer"></a>Za pomocą WriteLine, Projektant działań

Dostęp do **WriteLine** projektanta działań w **podstawowych** kategorii **przybornika**. **WriteLine** projektanta działań mogą być przeciągnięte z **przybornika** i porzucić do powierzchni projektanta przepływów pracy wszędzie tam, gdzie działań są zazwyczaj umieszczane, takie jak wewnątrz <xref:System.Activities.Statements.Sequence>. Spowoduje to utworzenie <xref:System.Activities.Statements.WriteLine> działanie przy użyciu domyślnego <xref:System.Activities.Activity.DisplayName%2A> z WriteLine. <xref:System.Activities.Activity.DisplayName%2A> Mogą być edytowane w nagłówku **WriteLine** projektanta działań lub **DisplayName** pola siatki właściwości.

### <a name="the-writeline-properties"></a>Właściwości WriteLine

W poniższej tabeli przedstawiono <xref:System.Activities.Statements.WriteLine> właściwości i w tym artykule opisano, jak są używane w projektancie. Te właściwości można edytować w siatce właściwości, a niektóre z nich mogą być edytowane na powierzchni projektanta przepływów pracy.

|Nazwa właściwości|Wymagane|Użycie|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|Przyjazna nazwa <xref:System.Activities.Statements.WriteLine> działania. Wartość domyślna to WriteLine. Mimo że <xref:System.Activities.Activity.DisplayName%2A> nie jest bezwzględnie konieczne jest najlepszym rozwiązaniem jest użycie jednego.|
|<xref:System.Activities.Statements.WriteLine.Text%2A>|False|Tekst do zapisu. Aby ustawić właściwości, wpisz wyrażenie języka Visual Basic w **tekstu** polu na **WriteLine** działanie projektanta lub w siatce właściwości.|
|<xref:System.Activities.Statements.WriteLine.TextWriter%2A>|False|<xref:System.IO.TextWriter> Do której <xref:System.Activities.Statements.WriteLine> zapisuje <xref:System.Activities.Statements.WriteLine.Text%2A>. Wartość domyślna to konsoli.|

## <a name="see-also"></a>Zobacz także

- [Typy pierwotne](../workflow-designer/primitives-activity-designers.md)
- [Assign](../workflow-designer/assign-activity-designer.md)
- [Delay](../workflow-designer/delay-activity-designer.md)
- [InvokeMethod](../workflow-designer/invokemethod-activity-designer.md)