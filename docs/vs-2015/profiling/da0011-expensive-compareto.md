---
title: 'DA0011: Kosztowna funkcja CompareTo | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.performance.DA0011
- vs.performance.rules.DAExpensiveCompareTo
- vs.performance.11
- vs.performance.rules.DA0011
ms.assetid: 239a381d-0d97-4367-8668-746c93f5af2c
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 0726ef4eb93d3e962e5fa39fe9cc7acbdbfbe8ca
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49210447"
---
# <a name="da0011-expensive-compareto"></a>DA0011: Expensive CompareTo
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Aby uzyskać najnowszą dokumentację programu Visual Studio 2017, zobacz [DA0011: kosztowna funkcja CompareTo](https://docs.microsoft.com/visualstudio/profiling/da0011-expensive-compareto) w witrynie docs.microsoft.com.  
  
|||  
|-|-|  
|Identyfikator reguły|DA0011|  
|Kategoria|Sposób użycia programu .NET framework|  
|Metod profilowania|Próbkowania<br /><br /> Pamięć .NET|  
|Komunikat|Funkcje CompareTo powinny być tanie i nie przydzielić wszystkie pamięci. Mniejsza złożoność funkcji CompareTo, jeśli jest to możliwe.|  
|Typ reguły|Ostrzeżenie|  
  
## <a name="cause"></a>Przyczyna  
 CompareTo — metoda tego typu jest kosztowne lub przydziela pamięć.  
  
## <a name="rule-description"></a>Opis reguły  
 Metody CompareTo powinny być skuteczne i nie należy przydzielić pamięci.  
  
## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Zmniejsz złożoność CompareTo — metoda.

