---
title: Zabezpieczenia szablonów tekstowych | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- text templates, security
ms.assetid: 567a2383-7d43-4acc-af4a-cd70b7a0151e
caps.latest.revision: 25
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: 65b4b6616921dae0abb0bb54316d8b8262d1f652
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49214685"
---
# <a name="security-of-text-templates"></a>Zabezpieczenia szablonów tekstowych
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Szablony tekstowe mają następujące problemy dotyczące zabezpieczeń:  
  
-   Szablony tekstowe są narażone na wstawienia dowolnego kodu.  
  
-   Jeśli mechanizm używany przez hosta można znaleźć procesor dyrektywy nie jest bezpieczne, można uruchomić złośliwe procesora dyrektywy.  
  
## <a name="arbitrary-code"></a>Dowolnego kodu  
 Podczas pisania szablonu można umieścić dowolny kod w ramach \<## > tagów. Umożliwia to dowolnego kodu do wykonania z w ramach szablonu tekstu.  
  
 Upewnij się, że można uzyskać szablony z zaufanych źródeł. Upewnij się ostrzec użytkowników końcowych w aplikacji nie można wykonać szablonów, które nie pochodzą z zaufanych źródeł.  
  
## <a name="malicious-directive-processor"></a>Złośliwy procesora dyrektywy  
 Aparat szablonów tekstu współdziała z hosta przekształcania i co najmniej jeden procesor dyrektywy do przekształcania szablonu tekstu do pliku wyjściowego. Aby uzyskać więcej informacji, zobacz [proces przekształcania szablonu tekstowego](../modeling/the-text-template-transformation-process.md).  
  
 Jeśli mechanizm używany przez hosta można znaleźć procesor dyrektywy nie jest bezpieczne, uruchamia ryzyko uruchomienia złośliwych procesora dyrektywy. Złośliwy procesor dyrektywy może dostarczyć kod, który jest uruchamiany w `FullTrust` tryb uruchamiania szablonu. Jeśli utworzono hosta przekształcania szablonu niestandardowego tekstu, należy użyć mechanizm bezpiecznego, takich jak rejestr, aparat do zlokalizowania procesory dyrektyw.



