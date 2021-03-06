---
title: Projektant przepływu pracy — TransactedReceiveScope, Projektant działań
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
ms.technology: vs-workflow-designer
f1_keywords:
- System.ServiceModel.Activities.TransactedReceiveScope.UI
ms.assetid: 7ca93aad-4e83-4d81-90f4-998ee114d9b6
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: a42c1cc9dac8e71bfe71f684232fdbf67fadb710
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49929546"
---
# <a name="transactedreceivescope-activity-designer"></a>TransactedReceiveScope, projektant działań

**TransactedReceiveScope** projektanta jest używany do tworzenia i konfigurowania <xref:System.ServiceModel.Activities.TransactedReceiveScope> działania.

## <a name="the-transactedreceivescope-activity"></a>Działanie TransactedReceiveScope

<xref:System.ServiceModel.Activities.TransactedReceiveScope> Działanie umożliwia przepływu transakcji na serwerze transakcji utworzone przez przepływ pracy lub dyspozytora.

### <a name="using-the-transactedreceivescope-activity-designer"></a>Za pomocą TransactedReceiveScope, Projektant działań

Dostęp do **TransactedReceiveScope** projektanta działań w **komunikatów** kategorii **przybornika**. **TransactedReceiveScope** projektanta działań mogą być przeciągnięte z **przybornika** i porzucić do powierzchni projektanta przepływów pracy wszędzie tam, gdzie działań są zazwyczaj umieszczone. Spowoduje to utworzenie <xref:System.ServiceModel.Activities.TransactedReceiveScope> działanie przy użyciu domyślnego **DisplayName** transactedreceivescope. <xref:System.Activities.Activity.DisplayName%2A> Mogą być edytowane w nagłówku **TransactedReceiveScope** projektanta działań lub **DisplayName** pola siatki właściwości.

**TransactedReceiveScope** Projektant zawiera **żądania** i **treści** pola. Są one używane do konfigurowania <xref:System.ServiceModel.Activities.TransactedReceiveScope.Request%2A> właściwość, która określa <xref:System.ServiceModel.Activities.Receive> działania i <xref:System.ServiceModel.Activities.TransactedReceiveScope.Body%2A> właściwość, która określa niektóre inne <xref:System.Activities.Activity>. <xref:System.ServiceModel.Activities.TransactedReceiveScope.Request%2A> Tworzy transakcji. Następnie transakcja ma zostać otoczenia w zakresie <xref:System.ServiceModel.Activities.TransactedReceiveScope.Body%2A> tak, aby wszystkie działania w tym zakresie wykonuje wewnątrz tej transakcji.

### <a name="the-transactedreceivescope-properties"></a>Właściwości TransactedReceiveScope

W poniższej tabeli przedstawiono <xref:System.ServiceModel.Activities.TransactedReceiveScope> właściwości i w tym artykule opisano, jak są używane w projektancie. Te <xref:System.Activities.Activity.DisplayName%2A> właściwości można edytować w siatce właściwości lub na powierzchni projektanta przepływów pracy, ale inne muszą być edytowane na powierzchni projektowej.

|Nazwa właściwości|Wymagane|Użycie|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|False|Opcjonalna nazwa przyjazna <xref:System.ServiceModel.Activities.TransactedReceiveScope> działania. Wartość domyślna to TransactedReceiveScope.<br /><br /> Mimo że <xref:System.Activities.Activity.DisplayName%2A> nazwa nie jest bezwzględnie konieczne, jest najlepszym rozwiązaniem, aby użyć nazwy wyświetlanej.|
|<xref:System.ServiceModel.Activities.TransactedReceiveScope.Request%2A>|True|Spadnie <xref:System.ServiceModel.Activities.Receive> działanie do **żądania** bloku na powierzchni projektanta działań.|
|<xref:System.ServiceModel.Activities.TransactedReceiveScope.Body%2A>|False|Spadnie <xref:System.Activities.Activity> do **treści** bloku na powierzchni projektanta działań.|

## <a name="see-also"></a>Zobacz także

- [CorrelationScope](../workflow-designer/correlationscope-activity-designer.md)
- [InitializeCorrelation](../workflow-designer/initializecorrelation-activity-designer.md)
- [Receive](../workflow-designer/receive-activity-designer.md)
- [ReceiveAndSendReply](../workflow-designer/receiveandsendreply-template-designer.md)
- [Send](../workflow-designer/send-activity-designer.md)
- [SendAndReceiveReply](../workflow-designer/sendandreceivereply-template-designer.md)