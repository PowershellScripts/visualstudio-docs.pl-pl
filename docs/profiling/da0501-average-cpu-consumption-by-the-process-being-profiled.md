---
title: "DA0501: Średnie wykorzystanie CPU przez proces poddawany profilowaniu. | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- vs.performance.rules.DA0501
- vs.performance.DA0501
- vs.performance.501
ms.assetid: b01946b4-75e3-47d5-a1a1-cebfae66a3af
caps.latest.revision: "7"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 5de803a82110720a78b5b80cada7dad1c39c46c1
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="da0501-average-cpu-consumption-by-the-process-being-profiled"></a>DA0501: Średnie wykorzystanie CPU przez proces poddawany profilowaniu.
|||  
|-|-|  
|Identyfikator reguły|DA501|  
|Kategoria|Monitorowanie zasobów|  
|Metoda profilowania|Wszystkie|  
|Komunikat|Średnie użycie Procesora przez profilowany proces.|  
|Typ reguły|Informacje|  
  
 Gdy profilu można za pomocą próbkowania, pamięci platformy .NET lub metody kontencji zasobów, należy zebrać co najmniej 10 próbek do wyzwolenia tej reguły.  
  
## <a name="rule-description"></a>Opis reguły  
 Ten komunikat raporty procent czasu, który procesor był zajęty wykonywaniem instrukcji z aplikacji. Podanej wartości jest średnią we wszystkich interwałach pomiarowych, w których był aktywny PROFILOWANEGO procesu. Wartość może być większa niż 100% na maszynie z więcej niż jeden procesor.  
  
## <a name="how-to-use-rule-data"></a>Jak używać danych reguły  
 Porównanie wydajności z różnych wersji lub kompilacji programu lub zrozumieć wydajność aplikacji w scenariuszach różnych testu, należy użyć wartości reguły.