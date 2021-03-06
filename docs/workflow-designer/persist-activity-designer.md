---
title: Projektant przepływu pracy — Persist, Projektant działań
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
ms.technology: vs-workflow-designer
f1_keywords:
- System.Activities.Statements.Persist.UI
ms.assetid: be8648dd-3eb9-4a50-8ec1-57a8be804692
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 51f74b5348c7e99824659ee713171bd71c5f522e
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49831345"
---
# <a name="persist-activity-designer"></a>Persist, projektant działań

**Utrwalanie** projektanta działań służy do tworzenia i konfigurowania <xref:System.Activities.Statements.Persist> działania.

## <a name="the-persist-activity"></a>Utrwalanie działania

<xref:System.Activities.Statements.Persist> Działanie zapisuje przepływ pracy na dysku, jeśli jest to możliwe. <xref:System.Activities.Statements.Persist> Działania nie można wykonać w strefie bez trwałości, jak na przykład w ramach <xref:System.Activities.Statements.TransactionScope> działania. Jeśli używasz <xref:System.Activities.Statements.Persist> działań w zakresie bez trwałości, zgłaszany jest wyjątek w czasie wykonywania.

### <a name="using-the-persist-activity-designer"></a>Za pomocą Persist, Projektant działań

**Utrwalanie** projektanta działań można znaleźć w **środowiska uruchomieniowego** kategorii **przybornika**, które jest dostępne po kliknięciu **przybornika** Karta (można także wybrać **przybornika** z **widoku** menu lub klawiszy CTRL + ALT + X.)

**Utrwalanie** projektanta działań mogą być przeciągnięte z **przybornika** i porzucić do powierzchni projektanta przepływów pracy wszędzie tam, gdzie działań są zazwyczaj umieszczane, takie jak wewnątrz <xref:System.Activities.Statements.Sequence>. Spowoduje to utworzenie <xref:System.Activities.Statements.Persist> działanie przy użyciu domyślnego **DisplayName** z utrwalanie. <xref:System.Activities.Activity.DisplayName%2A> Mogą być edytowane w nagłówku **utrwalanie** projektanta działań lub **DisplayName** pola siatki właściwości.

### <a name="the-persist-properties"></a>Utrwalanie właściwości

W poniższej tabeli przedstawiono <xref:System.Activities.Statements.Persist> właściwości i w tym artykule opisano, jak są używane w projektancie. Te właściwości można edytować w siatce właściwości, a niektóre z nich mogą być edytowane na powierzchni projektanta przepływów pracy.

|Nazwa właściwości|Wymagane|Użycie|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|Przyjazna nazwa <xref:System.Activities.Statements.Persist> działania. Wartość domyślna to utrwalanie. Chociaż nazwa wyświetlana nie jest bezwzględnie konieczne, jest najlepszym rozwiązaniem, aby użyć nazwy wyświetlanej.|

## <a name="see-also"></a>Zobacz także

- [Środowisko uruchomieniowe](../workflow-designer/runtime-activity-designers.md)
- [TerminateWorkflow](../workflow-designer/terminateworkflow-activity-designer.md)