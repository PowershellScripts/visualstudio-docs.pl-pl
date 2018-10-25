---
title: 'CA1601: Nie używaj czasomierzy, które uniemożliwiają zmianę stanu zasilania'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1601
- DoNotUseTimersThatPreventPowerStateChanges
helpviewer_keywords:
- CA1601
- DoNotUseTimersThatPreventPowerStateChanges
ms.assetid: b8028c92-0696-4c54-9773-0028f29bda9a
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 9ae36ae1f4af7281c8f32af57fd08cdda6145ba0
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49917340"
---
# <a name="ca1601-do-not-use-timers-that-prevent-power-state-changes"></a>CA1601: Nie używaj czasomierzy, które uniemożliwiają zmianę stanu zasilania

|||
|-|-|
|TypeName|DoNotUseTimersThatPreventPowerStateChanges|
|CheckId|CA1601|
|Kategoria|Microsoft.Mobility|
|Zmiana kluczowa|Kluczowa|

## <a name="cause"></a>Przyczyna
 Czasomierz został interwał występuje więcej niż jeden raz na sekundę.

## <a name="rule-description"></a>Opis reguły
 Nie częściej niż jeden raz na sekundę lub użyj czasomierzy, które występować częściej niż jeden sondowania czas na sekundę. Wyższa częstotliwość działań okresowych sprawi, że procesor będzie zajęty, co zakłóci działanie czasomierzy bezczynności oszczędzających energię, które wyłączają ekran i dyski twarde.

## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia
 Ustaw czasomierz interwałów występuje mniej niż jeden raz na sekundę.

## <a name="when-to-suppress-warnings"></a>Kiedy pominąć ostrzeżenia
 Ta reguła ma być pomijana, tylko wtedy, gdy wyzwalania czasomierza więcej niż jeden raz na sekundę jest wymagany i zagadnienia dotyczące mobilności można bezpiecznie zignorować.