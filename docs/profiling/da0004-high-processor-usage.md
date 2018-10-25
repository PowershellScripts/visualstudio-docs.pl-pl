---
title: 'DA0004: Znaczące wykorzystanie czasu procesora | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.performance.rules.DAHighProcessorUsage
- vs.performance.rules.DA0004
- vs.performance.DA0004
- vs.performance.4
ms.assetid: 2c4fb569-929e-4f1d-8c50-b590ee371351
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 87f418c8f145d13dee575c9d45d192a59547e6a0
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49920888"
---
# <a name="da0004-high-processor-usage"></a>DA0004: Znaczące wykorzystanie czasu procesora

|||  
|-|-|  
|Identyfikator reguły|DA0004|  
|Kategoria|Użycie narzędzia profilowania|  
|Metod profilowania|Oprzyrządowanie<br /><br /> Próbkowania|  
|Komunikat|Użycie procesora jest stale powyżej 75%. Należy rozważyć użycie trybu próbkowania dla aplikacji zależne od Procesora CPU.|  
|Typ reguły|Informacje|  

 Podczas profilowania za pomocą próbkowania pamięci platformy .NET i metod rywalizacji zasobów musi zebrać co najmniej 10 próbek do wyzwolenia tej reguły.  

## <a name="cause"></a>Przyczyna  
 Użycie procesora (CPU) był wysoko w danych, które zostały zebrane przy użyciu metody Instrumentacji profilowania. Należy wziąć pod uwagę przy użyciu metody próbkowania, metoda profilowania, gdy profilowanie Procesora powiązana aplikacja.  

## <a name="rule-description"></a>Opis reguły  
 Podczas tego uruchomienia profilowania procesora (czy procesory) był zajęty, spójne. Wysokie wykorzystanie procesora CPU można wskazać aplikacji zależne od Procesora CPU. Instrumentowane profile nie są najbardziej efektywny sposób Badaj scenariusze użycia procesora CPU. Próbkowanie jest bardziej efektywne w przypadku profilowania aplikacji, które spędzają większość czasu wykonywania instrukcji na procesorze.  

## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Należy wziąć pod uwagę profilowania aplikację ponownie przy użyciu metody próbkowania zamiast metody instrumentacji, o ile nie wymagają funkcji chronometrażu lub interesuje Cię bardziej opis wejścia/wyjścia niż wąskich gardeł.