---
title: Rozwiązywanie problemów związanych z metrykami kodów
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: troubleshooting
ms.assetid: f2fdb995-4888-4246-85dc-7bacadd45968
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: ef7078b09b1bf2382e1c91878995772d80bfa625
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49853965"
---
# <a name="troubleshooting-code-metrics-issues"></a>Rozwiązywanie problemów związanych z metrykami kodów
Niektóre następujące problemy mogą występować w przypadku zbierać metryki kodu:

-   [Zmiany w obliczeniach złożoności kodu programu Visual Studio 2010](#Changes_in_Visual_Studio_2010_code_complexity_calculations)

##  <a name="Changes_in_Visual_Studio_2010_code_complexity_calculations"></a> Zmiany w obliczeniach złożoności kodu programu Visual Studio 2010
 Dla tej samej funkcji metryki złożoności kodu są obliczane w [!INCLUDE[vs_dev10_long](../code-quality/includes/vs_dev10_long_md.md)] może różnić się od metryki obliczana na podstawie wcześniejszych wersjach [!INCLUDE[vs_current_short](../code-quality/includes/vs_current_short_md.md)] w następujących sytuacjach:

- Funkcja zawiera jeden lub więcej bloki catch. W poprzednich wersjach [!INCLUDE[vs_current_short](../code-quality/includes/vs_current_short_md.md)], catch bloki nie zostały uwzględnione w obliczeniach. W [!INCLUDE[vs_dev10_long](../code-quality/includes/vs_dev10_long_md.md)], złożoność każdego bloku catch zostanie dodany do złożoność funkcji.

- Funkcja zawiera instrukcję switch (Select Case w języku Visual Basic). Kompilator różnice między [!INCLUDE[vs_dev10_long](../code-quality/includes/vs_dev10_long_md.md)] i wcześniejszych wersji może generować niektóre instrukcje switch, zawierające przypadków należą do różnych kod MSIL.

## <a name="see-also"></a>Zobacz też
 [Mierzenie złożoności i poziomu łatwości konserwacji kodu zarządzanego](../code-quality/measuring-complexity-and-maintainability-of-managed-code.md)