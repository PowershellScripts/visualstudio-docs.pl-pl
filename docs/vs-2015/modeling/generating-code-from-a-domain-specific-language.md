---
title: Generowanie kodu z języka specyficznego dla domeny | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: e3706cc9-2afd-456a-a879-68425a248ebc
caps.latest.revision: 15
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: 5edc6e267957f08837399ae5c2e56bce3cc26cce
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49232001"
---
# <a name="generating-code-from-a-domain-specific-language"></a>Generowanie kodu z języka specyficznego dla domeny
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Microsoft [!INCLUDE[dsl](../includes/dsl-md.md)] oferują zaawansowane możliwości do generowania kodu, dokumenty, pliki konfiguracji i innych artefaktów z danych reprezentowanych w modelach. Za pomocą [!INCLUDE[dsl](../includes/dsl-md.md)], można utworzyć zestaw klas, które reprezentują dane, można napisać szablony tekstowe w klasach których nazwy i właściwości odzwierciedlenia tych danych.  
  
 Na przykład firma Fabrikam ma plik XML nazw klienta i adresy e-mail. Ich deweloperom tworzenie modelu, w którym klient jest klasę o nazwie właściwości i wiadomości e-mail. Napisz ich kilka szablonów tekstu do przetwarzania danych, w tym ten fragment, który tworzy spis wszystkich klientów jako część strony HTML:  
  
```  
<table>  
<# foreach (Customer c in ContactList) {  #>  
  <tr><td> <#= c.FullName #> </td>   
      <td> <#= c.EmailAddress #> </td> </tr>  
<# } #>  </table>  
```  
  
 Podczas przetwarzania bazy danych klientów w pliku XML jest do odczytu do magazynu modeli. A *procesora dyrektywy*utworzony za pomocą [!INCLUDE[dsl](../includes/dsl-md.md)], udostępnia klasy klienta do kodu w szablonie tekstowym. Wiele szablonów tekstowych mogą być uruchamiane na tym samym magazynie.  
  
 Szablony tekstowe są istotne dla [!INCLUDE[dsl](../includes/dsl-md.md)]. Są one używane do generowania kodu źródłowego dla elementów modelu domeny, jak również pakietu VSPackage i formanty, które są używane do Zintegruj odpowiednie narzędzia, za pomocą [!INCLUDE[vsprvs](../includes/vsprvs-md.md)].  
  
 W tej sekcji omówiono niektóre sposoby tworzenia, modyfikacji i szablony tekstowe używane w debugowania [!INCLUDE[dsl](../includes/dsl-md.md)].  
  
## <a name="in-this-section"></a>W tej sekcji  
 [Uzyskiwanie dostępu do modeli z poziomu szablonów tekstu](../modeling/accessing-models-from-text-templates.md)  
  
 Zawiera podstawowe informacje o odwoływaniu się do języka specyficznego dla domeny w szablonach tekstowych.  
  
 [Przewodnik: Debugowanie szablonu tekstowego uzyskującego dostęp do modelu](../modeling/walkthrough-debugging-a-text-template-that-accesses-a-model.md)  
  
 W tym artykule opisano, jak to zrobić, rozwiązywanie problemów i debugowanie szablonu tekstu, który odwołuje się do języka specyficznego dla domeny.  
  
 [Przewodnik: Łączenie hosta z generowanym procesorem dyrektywy](../modeling/walkthrough-connecting-a-host-to-a-generated-directive-processor.md)  
  
 W tym artykule opisano sposób łączenia niestandardowego hosta z generowanym procesorem dyrektywy.  
  
 [Polecenie DslTextTransform](../modeling/the-dsltexttransform-command.md)  
  
 W tym artykule opisano pliku polecenia, który jest wykonywany TextTransform plik wykonywalny w wierszu polecenia dla szablonów tekstowych, które odwołują się języki specyficzne dla domeny.  
  
## <a name="reference"></a>Tematy pomocy  
 [Pisanie szablonu tekstowego T4](../modeling/writing-a-t4-text-template.md)  
  
 Udostępnia składnia dyrektyw szablonu tekstu i bloki sterujące.  
  
## <a name="related-sections"></a>Sekcje pokrewne  
 [Generowanie kodu czasu projektowania przy użyciu szablonów tekstowych T4](../modeling/design-time-code-generation-by-using-t4-text-templates.md)  
  
 Wyjaśniono proces przekształcania szablonu tekstu.  
  
 [Generowanie kodu w procesie kompilacji](../modeling/code-generation-in-a-build-process.md)  
  
 Ten temat jest generowanie plików z DSL na serwerze kompilacji.



