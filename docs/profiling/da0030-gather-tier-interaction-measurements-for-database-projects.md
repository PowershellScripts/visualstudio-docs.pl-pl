---
title: 'DA0030: Zbieraj pomiary interakcji warstw dla projektów bazy danych | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.performance.DA0030
- vs.performance.rules.DA0030
- vs.performance.30
ms.assetid: 42b2f69d-0cfa-4854-82c4-589c3d8b4557
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 0d0fb38348a901582182bdfaec2d7d775ec195f7
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49814015"
---
# <a name="da0030-gather-tier-interaction-measurements-for-database-projects"></a>DA0030: Gromadzenie pomiarów interakcji warstwy dla projektów bazy danych

|||  
|-|-|  
|Identyfikator reguły|DA0030|  
|Kategoria|Użycie narzędzia profilowania|  
|Metoda profilowania|Próbkowania|  
|Komunikat|Zebranie pomiarów interakcji dla aplikacji wielowarstwowych będzie pomagają zrozumieć wzorców użycia baz danych i danych klucza dostępu opóźnienia. Spróbuj ponownie sprofilować aplikację z włączoną opcją profilowania interakcji między warstwami.|  
|Typ reguły|Informacje|  

## <a name="cause"></a>Przyczyna  
 Wywołania <xref:System.Data> metody są znaczna część danych profilowania, a nie zostaną zebrane dane interakcji między warstwami podczas uruchomienia profilowania. Należy wziąć pod uwagę profilowanie ponownie i dodawanie danych o interakcji między warstwami.  

## <a name="rule-description"></a>Opis reguły  
 Ta reguła jest uruchamiana zawsze wtedy, gdy istnieje znaczne działanie funkcji, które znajdują się w przestrzeniach nazw System.Data, w tym <xref:System.Data.Linq> <xref:System.Data.Linq>.  

 Wielowarstwowe aplikacje za pomocą warstwy usług dla ich warstwy prezentacji i danych. Często Warstwa danych jest oddzielny proces uruchamiany system zarządzania bazami danych, takich jak Microsoft SQL Server. Warstwa danych może być uruchomiony na osobnym komputerze nawet od pozostałej części aplikacji. Profile próbkowania zapewniają mały wgląd w funkcje i usługi uruchomione spoza procesu lub zdalnie.  

 Narzędzia profilowania można zbierać informacji chronometrażu dla aplikacji wielowarstwowych, które wchodzą w interakcje z warstwy danych programu Microsoft SQL Server przy użyciu wywołań asynchronicznych do usług ADO.NET. Musisz jawnie włączyć profilowanie interakcji między warstwami. Go nie jest włączona domyślnie.  

## <a name="how-to-fix-violations"></a>Jak naprawić naruszenia  
 Ta reguła jest wyłącznie w celach informacyjnych i może nie wymagać działań korygujących.  

 Aby uzyskać informacje dotyczące sposobu dodawania danych o interakcji między warstwami do danych profilowania ze środowiska IDE programu Visual Studio, zobacz [zbierania danych o interakcji między warstwami](../profiling/collecting-tier-interaction-data.md). Aby uzyskać informacje dotyczące sposobu dodawania danych o interakcji między warstwami z wiersza polecenia, zobacz [zbierania danych o interakcji między warstwami](../profiling/adding-tier-interaction-data-from-the-command-line.md).