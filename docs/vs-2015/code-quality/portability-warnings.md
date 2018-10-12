---
title: Ostrzeżenia przenośności | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.codeanalysis.PortabilityRules
helpviewer_keywords:
- portability warnings
- managed code analysis warnings, portability warnings
- warnings, portability
ms.assetid: 902e859a-2153-4970-baaa-8a5b4a11806f
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 3b7c38f8380fc8e52707b9c4817880b1ce86b4b9
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49173085"
---
# <a name="portability-warnings"></a>Ostrzeżenia przenośności
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Ostrzeżenia przenośności obsługuje przenośności w różnych systemach operacyjnych.  
  
## <a name="in-this-section"></a>W tej sekcji  
  
|Reguła|Opis|  
|----------|-----------------|  
|[CA1900: Pola typu wartości powinny być przenośne](../code-quality/ca1900-value-type-fields-should-be-portable.md)|Ta reguła sprawdza, czy struktury, które są zadeklarowane za pomocą atrybutu jawnego układu, zostaną prawidłowo wyrównane podczas przekazywania do kodu niezarządzanego w 64-bitowych systemach operacyjnych.|  
|[CA1901: Deklaracje P/Invoke powinny być przenośne](../code-quality/ca1901-p-invoke-declarations-should-be-portable.md)|Ta reguła oblicza rozmiar każdego parametru oraz wartość zwracaną metody P/Invoke i sprawdza, czy ich rozmiar jest poprawny podczas przekazywania do kodu niezarządzanego w 32-bitowych i 64-bitowych systemach operacyjnych.|  
|[CA1903: Używaj tylko interfejsu API platformy docelowej](../code-quality/ca1903-use-only-api-from-targeted-framework.md)|Element członkowski lub typ używa elementu członkowskiego lub typu wprowadzonego w dodatku Service Pack, który nie został uwzględniony razem ze wskazanym środowiskiem docelowym projektu.|



