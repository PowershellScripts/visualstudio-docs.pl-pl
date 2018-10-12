---
title: Kontrolowanie koloru, stylu linii i innych właściwości kształtu | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: c06d0066-24aa-4c65-b91c-c2089b81ec8d
caps.latest.revision: 4
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: b5694e81721bcc16b13c1857a07072fcaef00a08
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49285483"
---
# <a name="controlling-color-line-style-and-other-shape-properties"></a>Kontrolowanie koloru, stylu linii i innych właściwości kształtu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Niektóre właściwości kształtu, takich jak kolor może być "widoczne" — oznacza to, połączony z właściwością domeny kształtu. Inne muszą być kontrolowane bezpośrednio.  
  
## <a name="exposing-a-property"></a>Udostępnianie właściwości  
 Niektóre właściwości kształtu, np. kolor można połączyć wartości właściwości domeny.  
  
 W definicji DSL wybierz kształt, łącznika lub diagramu klasy. W jego menu kontekstowym wybierz **Dodaj udostępniane**, a następnie wybierz polecenie Właściwości ma, takich jak kolor wypełnienia.  
  
 Kształt ma teraz właściwość domeny, którego można ustawić w kodzie programu, ani jako użytkownik.  
  
## <a name="dynamically-updating-an-exposed-property"></a>Dynamiczne aktualizowanie narażonych właściwości  
 Zazwyczaj mają być narażone właściwość zależna od innej właściwości. Można na przykład kształt na czerwony, zawsze wtedy, gdy właściwość określonej domeny jest mniejsza od zera. Aby wprowadzić tę zależność, należy utworzyć [reguły](../modeling/rules-propagate-changes-within-the-model.md). Na przykład:  
  
```csharp  
using System;  
using System.Collections.Generic;  
using System.Linq;  
using Microsoft.VisualStudio.Modeling;  
using Microsoft.VisualStudio.Modeling.Diagrams;  
namespace ExampleNamespace  
{  
 // Attribute associates the rule with class:  
 [RuleOn(typeof(CarShape), FireTime = TimeToFire.TopLevelCommit)]  
 // The rule is a class derived from one of the abstract rules:  
 class CarShapeAddRule : AddRule  
 {  
 // Override the abstract method:  
 public override void ElementAdded(ElementAddedEventArgs e)  
 {  
 base.ElementAdded(e);  
 CarShape shape = e.ModelElement as CarShape;  
 Store store = shape.Store;  
 // Ignore this call if we're currently loading a model:  
 if (store.TransactionManager.CurrentTransaction.IsSerializing)   
  return;  
 Car car = shape.ModelElement as Car;  
 // Code here propagates change as required - for example:  
 shape.FillColor = car.Somebool ? System.Drawing.Color.Red : System.Drawing.Color.Green;   
 }  
}  
 // The rule must be registered:  
 public partial class ExampleDomainModel  
 {  
 protected override Type[] GetCustomDomainModelTypes()  
 {  
  List<Type> types = new List<Type>(base.GetCustomDomainModelTypes());  
  types.Add(typeof(CarShapeAddRule));  
  // If you add more rules, list them here.   
  return types.ToArray();  
 }  
 }  
}  
```



