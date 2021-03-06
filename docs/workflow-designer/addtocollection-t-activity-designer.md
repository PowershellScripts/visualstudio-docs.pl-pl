---
title: Projektant przepływu pracy — AddToCollection<T> Projektant działań
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
ms.technology: vs-workflow-designer
f1_keywords:
- System.Activities.Statements.AddToCollection`1.UI
ms.assetid: f7fc0702-164e-4370-8946-bb2f9f9384b7
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: f6b260ca798befbbf45ba198f919f84ffc976262
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49869850"
---
# <a name="addtocollectiont-activity-designer"></a>AddToCollection\<T > Projektant działań

**AddToCollection\<T >** projektanta działań służy do tworzenia i konfigurowania <xref:System.Activities.Statements.AddToCollection%601> działania.

## <a name="the-addtocollectiont-activity"></a>AddToCollection\<T > działania

<xref:System.Activities.Statements.AddToCollection%601> Działania dodaje element do kolekcji.

### <a name="using-the-addtocollectiont-activity-designer"></a>Za pomocą AddToCollection\<T > Projektant działań

**AddToCollection\<T >** projektanta działań można znaleźć w **kolekcji** kategorii **przybornika**, które jest dostępne po kliknięciu  **Przybornik** kartę projektanta przepływów pracy. Można także wybrać **przybornika** z **widoku** menu lub naciśnij klawisz **Ctrl**+**Alt** + **X**.

**AddToCollection\<T >** projektanta działań mogą być przeciągnięte z **przybornika** i porzucić do powierzchni projektanta przepływów pracy wszędzie tam, gdzie działań są umieszczone, takie jak wewnątrz <xref:System.Activities.Statements.Sequence>. Upuszczanie **AddToCollection\<T >** tworzy projektanta działań <xref:System.Activities.Statements.AddToCollection%601> działanie przy użyciu domyślnego <xref:System.Activities.Activity.DisplayName%2A> z AddToCollection < Int32\>. (Domyślnie *elementu typeargument w języku* jest **Int32**. Elementu typeargument w języku można zmienić w siatce właściwości.) <xref:System.Activities.Activity.DisplayName%2A> Wartość może być edytowana w nagłówku **AddToCollection < T\>**  projektanta działań lub **DisplayName** pola siatki właściwości. W siatce właściwości, należy edytować inne właściwości.

### <a name="the-addtocollectiont-properties"></a>AddToCollection\<T > Właściwości

W poniższej tabeli przedstawiono <xref:System.Activities.Statements.AddToCollection%601> właściwości i w tym artykule opisano, jak są używane w projektancie.

|Nazwa właściwości|Wymagane|Użycie|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|Przyjazna nazwa <xref:System.Activities.Statements.AddToCollection%601> działania. Wartość domyślna to AddToCollection < Int32\>. Mimo że <xref:System.Activities.Activity.DisplayName%2A> wartość nie jest bezwzględnie konieczne, jest najlepszym rozwiązaniem, aby użyć jednego.|
|<xref:System.Activities.Statements.AddToCollection%601.Item%2A>|True|Element do dodania do kolekcji\<T >. Ten element jest typu *T*, która jest typu *elementu typeargument w języku*. Aby określić element, wpisz wyrażenie języka Visual Basic w siatce właściwości.|
|<xref:System.Activities.Statements.AddToCollection%601.Collection%2A>|True|Kolekcja, do którego ma zostać dodany element. Ta kolekcja jest typu **ICollection < elementu typeargument w języku\>**. Aby określić kolekcję, wpisz wyrażenie języka Visual Basic w siatce właściwości.|
|*TypeArgument*|True|Typu T z elementów znajdujących się w <xref:System.Collections.Generic.ICollection%601>. Domyślnie to *elementu typeargument w języku* ustawiono typ **Int32**. Aby zmienić typ, zmień wartość *elementu typeargument w języku* w polu kombi w siatce właściwości.|

## <a name="see-also"></a>Zobacz także

- [Kolekcja](../workflow-designer/collection-activity-designers.md)
- [AddToCollection\<T > Projektant działań](../workflow-designer/addtocollection-t-activity-designer.md)
- [ClearCollection\<T >](../workflow-designer/clearcollection-t-activity-designer.md)
- [ExistsInCollection\<T >](../workflow-designer/existsincollection-t-activity-designer.md)
- [RemoveFromCollection\<T >](../workflow-designer/removefromcollection-t-activity-designer.md)