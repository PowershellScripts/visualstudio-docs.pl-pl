---
title: "Przetwarzanie szablonów tekstowych przy użyciu hosta niestandardowego | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- text templates, in application or VS extension
- text templates, custom directive hosts
ms.assetid: affa3296-854d-47d6-9685-285f6d9ba5dc
caps.latest.revision: "33"
author: alancameronwills
ms.author: awills
manager: douge
ms.openlocfilehash: ea51f2b4b11680c07d9e7344d097b954a57d3f4d
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2017
---
# <a name="processing-text-templates-by-using-a-custom-host"></a>Przetwarzanie szablonów tekstowych przy użyciu hosta niestandardowego
*Transformacji szablonu tekstowego* przetworzyć przyjmuje *szablonu tekstowego* pliku jako dane wejściowe i tworzy plik tekstowy jako dane wyjściowe. Możesz wywołać aparat przekształcania tekstu z [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] rozszerzenia, lub z poziomu aplikacji autonomicznej uruchomiona na komputerze, na którym [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] jest zainstalowany. Jednak należy podać *hosta tworzenia szablonów tekstowych*. Ta klasa łączy szablon ze środowiskiem, znajdując zasoby, takie jak zestawy i dołączane pliki, oraz zajmując się obsługą danych wyjściowych i komunikatów o błędach.  
  
> [!TIP]
>  Jeśli piszesz pakietu lub rozszerzenia, które zostanie uruchomione w ramach [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)], należy wziąć pod uwagę przy użyciu usługi tworzenia szablonów tekstowych, zamiast zapisywania własnych hosta. Aby uzyskać więcej informacji, zobacz [wywoływanie transformacji tekstu w rozszerzeniu VS](../modeling/invoking-text-transformation-in-a-vs-extension.md).  
  
> [!NOTE]
>  Nie zaleca się używania przekształceń szablonu tekstu w aplikacjach serwerowych. Zaleca się używanie przekształceń szablonu tekstu tylko w pojedynczych wątkach. Jest to spowodowane tym, że aparat szablonów tekstowych ponownie używa pojedynczego elementu AppDomain do tłumaczenia, skompilowania i wykonania szablonów. Przetłumaczony kod nie jest odporny na wielowątkowość. Aparat jest przeznaczona do przetworzenia plików pojedynczo, ponieważ są one [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] projektu w czasie projektowania.  
>   
>  W przypadku aplikacji środowiska wykonawczego, należy wziąć pod uwagę przy użyciu szablonów tekstowych wstępnie przetworzonych: zobacz [Generowanie tekstu czasu wykonywania z szablonów tekstowych T4](../modeling/run-time-text-generation-with-t4-text-templates.md).  
  
 Jeśli aplikacja używa zestawu szablonów, które są ustalane w czasie kompilacji, łatwiej jest używać wstępnie przetworzonych szablonów tekstowych. Można również użyć tego podejścia, jeśli aplikacja jest uruchamiana na komputerze, na którym [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] nie jest zainstalowany. Aby uzyskać więcej informacji, zobacz [Generowanie tekstu czasu wykonywania z szablonów tekstowych T4](../modeling/run-time-text-generation-with-t4-text-templates.md).  
  
## <a name="executing-a-text-template-in-your-application"></a>Wykonywanie szablonu tekstu w aplikacji  
 Do wykonania szablonu tekstowego, należy wywołać metodę ProcessTemplate <xref:Microsoft.VisualStudio.TextTemplating.Engine?displayProperty=fullName>:  
  
```  
using Microsoft.VisualStudio.TextTemplating;  
...  
Engine engine = new Engine();  
string output = engine.ProcessTemplate(templateString, host);  
```  
  
 Aplikacja musi znaleźć i dostarczyć szablon oraz musi obsłużyć dane wyjściowe.  
  
 W `host` parametru, należy podać klasę, która implementuje <xref:Microsoft.VisualStudio.TextTemplating.ITextTemplatingEngineHost>. Jest to wywoływane zwrotnie przez aparat.  
  
 Host musi mieć możliwość rejestrowania błędów, rozpoznawania odwołań do zestawu i dołączania plików, podawania domeny aplikacji, w której można wykonać szablon, a także wywoływania odpowiednich procesorów dla każdej dyrektywy.  
  
 <xref:Microsoft.VisualStudio.TextTemplating.Engine?displayProperty=fullName>jest zdefiniowany w **Microsoft.VisualStudio.TextTemplating.\*. 0 biblioteki dll**, i <xref:Microsoft.VisualStudio.TextTemplating.ITextTemplatingEngineHost> jest zdefiniowany w **Microsoft.VisualStudio.TextTemplating.Interfaces.\*. 0 biblioteki dll**.  
  
## <a name="in-this-section"></a>W tej sekcji  
 [Wskazówki: Tworzenie niestandardowego hosta szablonu tekstowego](../modeling/walkthrough-creating-a-custom-text-template-host.md)  
 Przedstawiono sposób tworzenia niestandardowego hosta szablonu tekstowego, która sprawia, że tekst szablonu funkcji dostępnych poza [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].  
  
## <a name="reference"></a>Tematy pomocy  
 <xref:Microsoft.VisualStudio.TextTemplating.ITextTemplatingEngineHost>  
  
## <a name="related-sections"></a>Sekcje pokrewne  
 [Proces transformacji szablonu tekstowego](../modeling/the-text-template-transformation-process.md)  
 W tym artykule opisano, jak działa transformacja tekstu i które części można dostosować.  
  
 [Tworzenie procesory dyrektywy szablonu tekstowego T4 niestandardowych](../modeling/creating-custom-t4-text-template-directive-processors.md)  
 Zawiera omówienie procesorów dyrektyw szablonu tekstu.