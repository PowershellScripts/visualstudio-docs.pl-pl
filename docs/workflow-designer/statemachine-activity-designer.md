---
title: "Projektant działań StateMachine | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- StateMachine Designer
- System.Activities.Statements.StateMachine.UI
ms.assetid: 474d5fb3-1049-4b3f-bc6b-7524dbbe1672
caps.latest.revision: "5"
ms.author: sdanie
manager: erikre
ms.openlocfilehash: b6b4d2e2d2327fdb045eca78f2a322bdc4d69868
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2017
---
# <a name="statemachine-activity-designer"></a>Obiekt StateMachine Projektant działań
<xref:System.Activities.Statements.StateMachine> Działanie zawiera kolekcję stanów i modele przepływów pracy za pomocą modelu maszyny znanego stanu.  
  
## <a name="using-the-statemachine-activity-designer"></a>Przy użyciu narzędzia Projektant działań StateMachine  
 Aby dodać <xref:System.Activities.Statements.StateMachine> działania, przeciągnij **StateMachine** Projektant działań z **automatu stanów** sekcji **przybornika** i upuść ją na do [!INCLUDE[wfd1](../workflow-designer/includes/wfd1_md.md)] powierzchni. Aby dodać stan podrzędnych do tego <xref:System.Activities.Statements.StateMachine> działania, przeciągnij <xref:System.Activities.Statements.State> lub <xref:System.Activities.Core.Presentation.FinalState> z **przybornika** i upuść ją na **StateMachine**.  
  
### <a name="statemachine-activity-properties-in-the-workflow-designer"></a>Obiekt StateMachine właściwości działania w Projektancie przepływów pracy  
 W poniższej tabeli przedstawiono <xref:System.Activities.Statements.StateMachine> właściwości, które można ustawić za pomocą projektanta przepływów pracy i w tym artykule opisano, jak są używane w projektancie. Te właściwości można edytować w siatce właściwości i niektóre można edytowane na powierzchnię projektanta.  
  
|Nazwa właściwości|Wymagane|Użycie|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|Określa przyjazną nazwę <xref:System.Activities.Statements.StateMachine> Projektant działań w nagłówku. Wartość domyślna to **StateMachine**. Wartość można edytować w siatce właściwości lub bezpośrednio w nagłówku Projektant działań. <xref:System.Activities.Activity.DisplayName%2A> Jest używany w nadrzędnych, który jest wyświetlany w górnej części projektanta przepływów pracy.<br /><br /> Mimo że <xref:System.Activities.Activity.DisplayName%2A> nie jest ścisłym wymogiem jest najlepszym rozwiązaniem jej użyć.|  
  
## <a name="see-also"></a>Zobacz też  
 [Schemat blokowy](../workflow-designer/flowchart-activity-designer.md)   
 [Przepływ sterowania](../workflow-designer/control-flow-activity-designers.md)