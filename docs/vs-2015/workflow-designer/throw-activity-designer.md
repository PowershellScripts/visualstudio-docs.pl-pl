---
title: Throw, Projektant działań | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: .net-framework-4.6
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- System.Activities.Statements.Throw.UI
ms.assetid: 5e97c947-be39-4a1f-af04-000e2e09528a
caps.latest.revision: 4
author: gewarren
ms.author: gewarren
manager: erikre
ms.openlocfilehash: 335601a40b21400e77aad5c493788db6e7146acd
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49275681"
---
# <a name="throw-activity-designer"></a>Throw, projektant działań
**Throw** projektanta działań służy do tworzenia i konfigurowania <xref:System.Activities.Statements.Throw> działania.  
  
## <a name="the-throw-activity"></a>Działanie Throw  
 <xref:System.Activities.Statements.Throw> Działanie zgłasza wyjątek.  
  
### <a name="using-the-throw-activity-designer"></a>Za pomocą projektanta działań Throw  
 **Throw** projektanta działań można znaleźć w **obsługę błędów** kategorii **przybornika**, które jest dostępne po kliknięciu **przybornika**karty w lewej części [!INCLUDE[wfd2](../includes/wfd2-md.md)] (można także wybrać **narzędzi** z **widoku** menu lub klawiszy CTRL + ALT + X.)  
  
 **Throw** projektanta działań mogą być przeciągnięte z **przybornika** i porzuconych do [!INCLUDE[wfd2](../includes/wfd2-md.md)] powierzchni wszędzie tam, gdzie działań są zwyczajowo umieszczane, takie jak wewnątrz <xref:System.Activities.Statements.Sequence>. Spowoduje to utworzenie <xref:System.Activities.Statements.Throw> działanie przy użyciu domyślnego **DisplayName** z Throw. <xref:System.Activities.Activity.DisplayName%2A> Wartość może być edytowana w nagłówku **Throw** projektanta działań lub **DisplayName** pola siatki właściwości. <xref:System.Activities.Statements.Throw.Exception%2A> Można edytować właściwości, w siatce właściwości.  
  
### <a name="the-throw-properties"></a>Właściwości Throw  
 W poniższej tabeli przedstawiono <xref:System.Activities.Statements.Throw> właściwości i w tym artykule opisano, jak są używane w projektancie.  
  
|Nazwa właściwości|Wymagane|Użycie|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|Określa opcjonalny przyjazna nazwa <xref:System.Activities.Statements.Throw> działania. Wartość domyślna to Throw.|  
|<xref:System.Activities.Statements.Throw.Exception%2A>|True|Wyjątek do zgłoszenia. Ten wyjątek musi pochodzić od klasy <xref:System.Exception>. Aby określić wyjątek, wpisz wyrażenie języka Visual Basic w siatce właściwości.|  
  
## <a name="see-also"></a>Zobacz też  
 [Kolekcja](../workflow-designer/collection-activity-designers.md)   
 [Zgłoś ponownie](../workflow-designer/rethrow-activity-designer.md)   
 [Throw, Projektant działań](../workflow-designer/throw-activity-designer.md)   
 [TryCatch](../workflow-designer/trycatch-activity-designer.md)