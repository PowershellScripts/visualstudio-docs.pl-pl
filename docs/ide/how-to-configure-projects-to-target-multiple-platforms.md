---
title: 'Porady: Konfigurowanie projektów pod kątem wielu platform docelowych'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-compile
ms.topic: conceptual
helpviewer_keywords:
- projects [Visual Studio], targeting platforms
- platforms, changing target platforms
ms.assetid: affa2392-7aed-45ac-9ffa-1d8e0496d590
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 308858941d03f6341cf3d22af074be45d790e16b
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49930222"
---
# <a name="how-to-configure-projects-to-target-multiple-platforms"></a>Porady: Konfigurowanie projektów pod kątem wielu platform docelowych

Program Visual Studio umożliwia rozwiązanie pod kątem kilku innej architektury procesora CPU lub platformami, jednocześnie. Właściwości, aby ustawić te są dostępne za pośrednictwem **programu Configuration Manager** okno dialogowe.

## <a name="target-a-platform"></a>Docelowa platforma

**Programu Configuration Manager** okno dialogowe pozwala utworzyć i ustawić konfiguracje rozwiązania i na poziomie projektu i platformy. Każdej kombinacji konfiguracji na poziomie rozwiązania i elementy docelowe może mieć unikatowe zbiory właściwości skojarzonych z nią, dzięki czemu można łatwo przełączać się między, na przykład konfiguracja wydania przeznaczonego [!INCLUDE[vcprx64](../extensibility/internals/includes/vcprx64_md.md)] platforma, konfiguracja wydania który jest przeznaczony dla x86 platformy i konfiguracji debugowania, który jest przeznaczony dla x86 platformy.

1.  Na **kompilacji** menu, kliknij przycisk **programu Configuration Manager**.

2.  W **pole platforma rozwiązania aktywnego**, wybierz platformę rozwiązania do obiektu docelowego, lub wybierz  **\<nowy >** do utworzenia nowej platformie. Visual Studio będzie kompilować aplikację pod kątem platformy, który jest ustawiony jako aktywnej platformy w **programu Configuration Manager** okno dialogowe.

## <a name="remove-a-platform"></a>Usuń to platforma

Jeśli okazuje się, że użytkownik nie ma potrzeby dla platformy, możesz usunąć go za pomocą **programu Configuration Manager** okno dialogowe. Spowoduje to usunięcie wszystkich ustawień rozwiązania i projektu, skonfigurowane dla tej kombinacji konfiguracji i docelowej.

1.  Na **kompilacji** menu, kliknij przycisk **programu Configuration Manager**.

2.  W **pole platforma rozwiązania aktywnego**, wybierz opcję  **\<Edytuj >**. **Edytuj platformy rozwiązań** zostanie otwarte okno dialogowe.

3.  Kliknij platformy, aby usunąć, a następnie kliknij przycisk **Usuń**.

## <a name="target-multiple-platforms-with-one-solution"></a>Dla wielu platform za pomocą jednego rozwiązania

Ponieważ istnieje możliwość zmiany ustawień, oparte na kombinacji konfiguracji i ustawień platformy, można skonfigurować rozwiązanie, które mogą kierować więcej niż jedną platformę.

### <a name="to-target-multiple-platforms"></a>Do wielu platform docelowych

1.  Użyj **programu Configuration Manager** można dodać co najmniej dwóch platform dla rozwiązania.

2.  Wybierz platformę docelową z **aktywną platformą rozwiązania** listy.

3.  Skompiluj rozwiązanie.

### <a name="to-build-multiple-solution-configurations-at-once"></a>Aby od razu kompilowanie wielu konfiguracji rozwiązania

1. Użyj **programu Configuration Manager** można dodać co najmniej dwóch platform dla rozwiązania.

2. Użyj **tworzenie partii** okna, aby jednocześnie utworzyć kilka konfiguracji rozwiązania.

   Można mieć platformę rozwiązanie na poziomie zestawu, na przykład [!INCLUDE[vcprx64](../extensibility/internals/includes/vcprx64_md.md)], i mieć żadnych projektów w ramach tego rozwiązania przeznaczone dla tej samej platformy. Istnieje również możliwość ma wiele projektów w rozwiązaniu, każdy przeznaczonych dla różnych platform. Zalecane jest, jeśli masz jedną z tych sytuacji, utworzenie nowej konfiguracji za pomocą opisową nazwę, aby uniknąć mylenia go.

## <a name="see-also"></a>Zobacz także

- [Porady: tworzenie i edytowanie konfiguracji](../ide/how-to-create-and-edit-configurations.md)
- [O konfiguracjach kompilacji](../ide/understanding-build-configurations.md)
- [Kompilowanie i czyszczenie projektów i rozwiązań w programie Visual Studio](../ide/building-and-cleaning-projects-and-solutions-in-visual-studio.md)
