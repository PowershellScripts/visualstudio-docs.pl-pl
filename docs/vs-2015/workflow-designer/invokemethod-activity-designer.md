---
title: InvokeMethod, Projektant działań | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: .net-framework-4.6
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- System.Activities.Statements.InvokeMethod.UI
ms.assetid: 15e6efdc-52ca-46d8-9c5e-063f7c8265a6
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: erikre
ms.openlocfilehash: a3fa1c07bbb32bc1da963a0d2f0a91ae6c193a30
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49863688"
---
# <a name="invokemethod-activity-designer"></a>InvokeMethod, projektant działań
**InvokeMethod** projektanta jest używany do tworzenia i konfigurowania <xref:System.Activities.Statements.InvokeMethod> działania.  
  
## <a name="the-invokemethod-activity"></a>Działania InvokeMethod  
 <xref:System.Activities.Statements.InvokeMethod> Wywołuje metodę publicznych określonego obiektu lub typu.  
  
### <a name="using-the-invokemethod-activity-designer"></a>Za pomocą InvokeMethod, Projektant działań  
 **InvokeMethod** projektanta działań można znaleźć w **podstawowych** kategorii **przybornika**, które jest dostępne po kliknięciu **przybornika** kartę [!INCLUDE[wfd2](../includes/wfd2-md.md)] (można także wybrać **narzędzi** z **widoku** menu lub klawiszy CTRL + ALT + X.)  
  
 **InvokeMethod** projektanta działań mogą być przeciągnięte z **przybornika** i porzuconych do [!INCLUDE[wfd2](../includes/wfd2-md.md)] powierzchni gdziekolwiek działań są zwyczajowo umieszczane, takie jak wewnątrz <xref:System.Activities.Statements.Sequence>. Spowoduje to utworzenie <xref:System.Activities.Statements.InvokeMethod> działanie przy użyciu domyślnego <xref:System.Activities.Activity.DisplayName%2A> z InvokeMethod. <xref:System.Activities.Activity.DisplayName%2A> Mogą być edytowane w nagłówku **InvokeMethod** projektanta działań lub **DisplayName** pola siatki właściwości.  
  
### <a name="the-invokemethod-properties"></a>Właściwości InvokeMethod  
 W poniższej tabeli przedstawiono <xref:System.Activities.Statements.InvokeMethod> właściwości i w tym artykule opisano, jak są używane w projektancie. Te właściwości można edytować w siatce właściwości, a niektóre mogą być edytowane [!INCLUDE[wfd2](../includes/wfd2-md.md)]powierzchni projektowej.  
  
|Nazwa właściwości|Wymagane|Użycie|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|Przyjazna nazwa <xref:System.Activities.Statements.InvokeMethod> działania. Wartość domyślna to InvokeMethod.<br /><br /> Mimo że <xref:System.Activities.Activity.DisplayName%2A> nie jest bezwzględnie konieczne jest najlepszym rozwiązaniem, aby użyć jednego.|  
|<xref:System.Activities.Statements.InvokeMethod.MethodName%2A>|True|Nazwa metody do wywołania, gdy działanie wykonuje. Metoda wywoływana musi być zadeklarowany jako **publicznych**. Tej właściwości można edytować na powierzchni projektowej. To jest obowiązkowa.|  
|<xref:System.Activities.Statements.InvokeMethod.Parameters%2A>|False|Kolekcja parametrów wywoływanej metody. Parametry muszą zostać dodane do kolekcji w tej samej kolejności, które są wyświetlane w podpisie metody. W siatce właściwości kliknij przycisk z wielokropkiem w **parametry** pola, wyświetla **parametry** okno dialogowe pozwala ustawić tę właściwość. Kliknij przycisk **Utwórz Argument** przycisk, aby dodać parametry.|  
|<xref:System.Activities.Statements.InvokeMethod.Result%2A>|False|Wartość zwracaną przez wywołanie metody.|  
|<xref:System.Activities.Statements.InvokeMethod.RunAsynchronously%2A>|True|Określa, czy metoda jest wywoływana asynchronicznie. Wartość domyślna to **False**.|  
|<xref:System.Activities.Statements.InvokeMethod.TargetObject%2A>|False|Obiekt, który zawiera metodę do wywołania. Tej właściwości można edytować na powierzchni projektowej.<br /><br /> Albo <xref:System.Activities.Statements.InvokeMethod.TargetObject%2A> lub <xref:System.Activities.Statements.InvokeMethod.TargetType%2A> jest wymagany do skonfigurowania.|  
|<xref:System.Activities.Statements.InvokeMethod.TargetType%2A>|False|Typ <xref:System.Activities.Statements.InvokeMethod.TargetObject%2A>. Tej właściwości można edytować na powierzchni projektowej. Ta właściwość musi można ustawić tylko, gdy wywoływana metoda jest statyczna.|  
  
 Do przekazania parametrów jak język C# **się** parametrów (na przykład `Method1(out myParam)),` należy używać **OutArgument** zamiast **InOutArgument**  
  
 Metody z argumentami o nazwie **TargetObject** lub **wynik** nie można wywołać za pomocą <xref:System.Activities.Statements.InvokeMethod> działania. Jest to spowodowane tym, że <xref:System.Activities.Statements.InvokeMethod> rejestruje działanie <xref:System.Activities.Statements.InvokeMethod.GenericTypeArguments%2A>, <xref:System.Activities.Statements.InvokeMethod.TargetObject%2A> i <xref:System.Activities.Statements.InvokeMethod.Result%2A> w <xref:System.Activities.Activity.CacheMetadata%2A>.  
  
 Algorytm parametry w rejestrowaniu <xref:System.Activities.Activity.CacheMetadata%2A> jest wyświetlany na poniższej liście:  
  
1. Zarejestruj <xref:System.Activities.Statements.InvokeMethod.TargetObject%2A> argumentu.  
  
2. Zarejestruj <xref:System.Activities.Statements.InvokeMethod.Result%2A> argumentu.  
  
3. Iteracyjne przeglądanie <xref:System.Activities.Statements.InvokeMethod.Parameters%2A> kolekcji i zarejestrować każdy argument.  
  
   Wyjątek wynikowa jest typu <xref:System.Activities.InvalidWorkflowException> z następującym komunikatem: "InvokeMethod": zmienna RuntimeArgument lub DelegateArgument już istnieje o nazwie "TargetObject". Nazwy muszą być unikatowe w obrębie zakresu środowiska.  
  
   To ograniczenie nie dotyczy <xref:System.Activities.Statements.InvokeMethod.TargetType%2A> i <xref:System.Activities.Statements.InvokeMethod.RunAsynchronously%2A> ponieważ nie są argumentami przepływu pracy i dlatego nie są zarejestrowane w <xref:System.Activities.Statements.InvokeMethod.GenericTypeArguments%2A> zbiór <xref:System.Activities.Statements.InvokeMethod> działania w <xref:System.Activities.Activity.CacheMetadata%2A> metody.  
  
## <a name="see-also"></a>Zobacz też  
 [Elementy podstawowe](../workflow-designer/primitives-activity-designers.md)   
 [Przypisz](../workflow-designer/assign-activity-designer.md)   
 [Opóźnienie](../workflow-designer/delay-activity-designer.md)   
 [WriteLine](../workflow-designer/writeline-activity-designer.md)