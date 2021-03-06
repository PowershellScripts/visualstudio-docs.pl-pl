---
title: CancellationScope, Projektant działań | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: .net-framework-4.6
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- System.Activities.Statements.CancellationScope.UI
ms.assetid: 2c85d663-b219-4142-9866-7693ffd46379
caps.latest.revision: 8
author: gewarren
ms.author: gewarren
manager: erikre
ms.openlocfilehash: 125e9fd934ce40d2a6633daa62b817628306daa3
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49229895"
---
# <a name="cancellationscope-activity-designer"></a>CancellationScope, projektant działań
**CancellationScope** projektanta działań służy do tworzenia i konfigurowania <xref:System.Activities.Statements.CancellationScope> działania.  
  
## <a name="the-cancellationscope-activity"></a>Działania CancellationScope  
 <xref:System.Activities.Statements.CancellationScope> Działanie umożliwia określenie działania wykonywania i anulowania logiki dla tego działania.  
  
### <a name="using-the-cancellationscope-activity-designer"></a>Za pomocą CancellationScope, Projektant działań  
 **CancellationScope** projektanta działań można znaleźć w **transakcji** kategorii **przybornika**, które jest dostępne po kliknięciu **przybornika**  karcie [!INCLUDE[wfd2](../includes/wfd2-md.md)] (można także wybrać **narzędzi** z **widoku** menu lub klawiszy CTRL + ALT + X.)  
  
 **CancellationScope** projektanta działań mogą być przeciągnięte z **przybornika** i porzuconych do [!INCLUDE[wfd2](../includes/wfd2-md.md)] powierzchni wszędzie tam, gdzie działań są zwyczajowo umieszczane, takie jak wewnątrz <xref:System.Activities.Statements.Sequence>. Spowoduje to utworzenie <xref:System.Activities.Statements.CancellationScope> działanie przy użyciu domyślnego <xref:System.Activities.Activity.DisplayName%2A> z CancellationScope. <xref:System.Activities.Activity.DisplayName%2A> Wartość może być edytowana w nagłówku **CancellationScope** projektanta działań lub **DisplayName** pola siatki właściwości.  
  
### <a name="the-cancellationscope-properties"></a>Właściwości działania CancellationScope  
 W poniższej tabeli przedstawiono <xref:System.Activities.Statements.CancellationScope> właściwości i w tym artykule opisano, jak są używane w projektancie. <xref:System.Activities.Activity.DisplayName%2A> Właściwości można edytować w siatce właściwości, ale inne właściwości, należy edytować na [!INCLUDE[wfd2](../includes/wfd2-md.md)] powierzchni.  
  
|Nazwa właściwości|Wymagane|Użycie|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|Opcjonalna nazwa przyjazna <xref:System.Activities.Statements.CancellationScope> działania. Wartość domyślna to CancellationScope. Mimo że <xref:System.Activities.Activity.DisplayName%2A> wartość nie jest bezwzględnie konieczne, jest najlepszym rozwiązaniem, aby użyć jednego.|  
|<xref:System.Activities.Statements.CancellationScope.Body%2A>|True|Określa działanie anulowania, który znajduje się logiki. Można dodać <xref:System.Activities.Statements.CancellationScope.Body%2A> działania, listy działanie z **przybornika** do **treści** polu na **CancellationScope** projektanta działań z tekst wskazówki "listy Działanie tutaj".|  
|<xref:System.Activities.Statements.CancellationScope.CancellationHandler%2A>|True|Określa działania, który jest wykonywany w przypadku anulowania. Można dodać <xref:System.Activities.Statements.CancellationScope.CancellationHandler%2A> działania, listy działanie z **przybornika** do **CancellationHandler** polu na **CancellationScope** projektanta działań ze wskazówką tekst "Upuść działanie tutaj".|  
  
## <a name="see-also"></a>Zobacz też  
 [Transakcji](../workflow-designer/transaction-activity-designers.md)   
 [CompensableActivity](../workflow-designer/compensableactivity-activity-designer.md)   
 [Wyrównania](../workflow-designer/compensate-activity-designer.md)   
 [Upewnij się](../workflow-designer/confirm-activity-designer.md)   
 [TransactionScope](../workflow-designer/transactionscope-activity-designer.md)