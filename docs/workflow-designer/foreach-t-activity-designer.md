---
title: Projektant przepływu pracy — ForEach&lt;T&gt; Projektant działań
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
ms.technology: vs-workflow-designer
f1_keywords:
- System.Activities.Statements.ForEach`1.UI
ms.assetid: 67097b3a-fcf5-4a72-beb1-2c7784151a86
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 99531f690e9dcbd1b35453acd17f1c52b8afb1d2
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49836219"
---
# <a name="foreachlttgt-activity-designer"></a>Instrukcja ForEach&lt;T&gt; Projektant działań

<xref:System.Activities.Statements.ForEach%601> Działanie wykonuje działania zawarte w jego <xref:System.Activities.Statements.ForEach%601.Body%2A> dla każdego elementu w określonej <xref:System.Activities.Statements.ForEach%601.Values%2A> kolekcji.

## <a name="foreacht-properties-in-the-workflow-designer"></a>Instrukcja ForEach < T\> właściwości w Projektancie przepływu pracy

W poniższej tabeli przedstawiono najbardziej przydatne <xref:System.Activities.Statements.ForEach%601> właściwości działań i informacje dotyczące używania ich w projektancie.

|Nazwa właściwości|Wymagane|Użycie|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|Przyjazna nazwa <xref:System.Activities.Statements.ForEach%601> działania. Wartość domyślna to ForEach < Int32\>. Mimo że <xref:System.Activities.Activity.DisplayName%2A> wartość nie jest bezwzględnie konieczne, jest najlepszym rozwiązaniem, aby użyć jednego.|
|<xref:System.Activities.Statements.ForEach%601.Values%2A>|True|Kolekcja elementów do iteracji. Aby ustawić <xref:System.Activities.Statements.ForEach%601.Values%2A>, wpisz wyrażenie języka Visual Basic w **wartości** polu na **ForEach < T\>**  działanie projektanta lub w siatce właściwości.|
|*TypeArgument*|True|Typ elementów w <xref:System.Activities.Statements.ForEach%601.Values%2A> kolekcji określonej przez parametr ogólny *T*. Domyślnie *elementu typeargument w języku* ustawiono **Int32**. Aby zmienić typ, zmień wartość *elementu typeargument w języku* pola kombi w siatce właściwości.|

Domyślnie, nosi nazwę iteratora pętli **elementu**. Można zmienić nazwy zmiennej iteratora w <xref:System.Activities.Statements.ForEach%601> projektanta działań. Iteratora pętli można używać w wyrażeniach w elementy podrzędne <xref:System.Activities.Statements.ForEach%601> działania.

## <a name="see-also"></a>Zobacz także

- [ParallelForEach\<T>](../workflow-designer/parallelforeach-t-activity-designer.md)
- [Przepływ sterowania](../workflow-designer/control-flow-activity-designers.md)