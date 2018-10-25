---
title: 'DA0008: Zebrano kilka próbek | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.performance.rules.DATooFewSamples
- vs.performance.8
- vs.performance.DA0008
- vs.performance.rules.DA0008
ms.assetid: 8a5b78aa-7b3d-476c-a47d-abfaff3fae7c
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 4f80f4f08be3c2af8444a41209a8d19909c94a8f
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49897904"
---
# <a name="da0008-few-samples-collected"></a>DA0008: Kilka zebranych przykładów

|||  
|-|-|  
|Identyfikator reguły|DA0008|  
|Kategoria|Użycie narzędzia profilowania|  
|Metoda profilowania|Próbkowania|  
|Komunikat|Zebrano tylko kilka przykładów. Należy wziąć pod uwagę dłużej przebiegu lub zwiększenie częstotliwości próbkowania dla uzyskania bardziej znaczących wyników.|  
|Typ reguły|Informacje|  

## <a name="cause"></a>Przyczyna  
 Kilka przykładów zostały zebrane podczas uruchomienia profilowania.  

## <a name="rule-description"></a>Opis reguły  
 Gdy używana jest metoda pobierania próbek, należy zbierać są statystycznie istotne liczba próbek, aby upewnić się, że dane reprezentują program rzeczywiste zachowanie. Aby zminimalizować błędy pobierania próbek, należy spróbować zbieranie co najmniej 1000 próbek zachowanie wykonania instrukcji programu. Jeśli nie zbieraj, wystarczająco dużo próbki, można możesz błąd podczas analizowania danych profilowania.  

## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Należy wziąć pod uwagę profilowania już wykonywania aplikacji lub za pomocą próbkowania szybciej uzyskać wyniki są statystycznie istotne. Aby dowiedzieć się, jak zmienić częstotliwość próbkowania w środowisku IDE programu Visual Studio, zobacz [porady: Wybieranie zdarzeń próbkowania](../profiling/how-to-choose-sampling-events.md). Aby uzyskać więcej informacji o tym, jak zmienić częstotliwość próbkowania, korzystając z wiersza polecenia Profiling Tools, zobacz [czasomierza](../profiling/timer.md) w [VSPerfCmd](../profiling/vsperfcmd.md) odwołania.