---
title: "Porady: zbieranie danych liczników systemu Windows | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- vs.performance.property.syscounter
- vs.performance.property.wincounter
helpviewer_keywords:
- windows counters
- performance tools, using windows counters
- profiling tools, using windows counters
ms.assetid: db4fbac2-bea5-4558-aa8b-160fcccf4b33
caps.latest.revision: "13"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d5b16cf6260932f11c9d4fd33f2eb5662327355a
ms.sourcegitcommit: 26419ab0cccdc30d279c32d6a841758cfa903806
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/11/2017
---
# <a name="how-to-collect-windows-counter-data"></a>Porady: zbieranie danych liczników systemu Windows
Liczniki systemu Windows to liczniki wydajności systemu, które mogą być zbierane w ustalonych odstępach czasu podczas profilowania. W widoku raportu narzędzi profilowania znaki, jest oznaczony wiersz **AutoMark** dla każdego interwału zbierania. Wiersz zawiera kolumny, które opisano w tym interwał wartości licznika wydajności. Aby ograniczyć analizę do okresu czasu między dwoma określonymi znacznikami, wybierz znaczniki, kliknij prawym przyciskiem myszy, a następnie wybierz **filtru przez** ->  **znaczniki** z menu skrótów.  
  
 **Wymagania**  
  
-   [!INCLUDE[vsUltLong](../code-quality/includes/vsultlong_md.md)], [!INCLUDE[vsPreLong](../code-quality/includes/vsprelong_md.md)], [!INCLUDE[vsPro](../code-quality/includes/vspro_md.md)]  
  
> [!NOTE]
>  Ulepszone funkcje zabezpieczeń w systemie Windows 8 i Windows Server 2012 wymagane znaczących zmian w sposobie profilera Visual Studio zbiera dane na tych platformach. Aplikacje platformy uniwersalnej systemu Windows wymagają również nowe techniki kolekcji. Zobacz [narzędzi wydajności w przypadku aplikacji systemu Windows 8 i Windows Server 2012](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).  
  
### <a name="to-collect-windows-counter-data"></a>Aby zebrać dane z systemem Windows  
  
1.  W Eksploratorze wydajności, kliknij prawym przyciskiem myszy sesji, dla której chcesz skonfigurować liczniki systemu Windows i wybierz **właściwości**.  
  
2.  W **strony właściwości**, kliknij przycisk **liczników systemu Windows**.  
  
3.  Wybierz **zbierania liczników systemu Windows** pole wyboru.  
  
4.  W **interwał zbierania (MS)** tekstu wpisz przedział czasu.  
  
5.  Wybierz kategorię z **kategorii licznika** listy rozwijanej.  
  
6.  Wybierz wystąpienie z **wystąpienia** listy rozwijanej.  
  
7.  Wybierz liczniki, które ma być używany, gdy w profilu aplikacji.  
  
8.  Kliknij przycisk **zastosowania.**  
  
## <a name="see-also"></a>Zobacz też  
 [Konfigurowanie sesji wydajności](../profiling/configuring-performance-sessions.md)   
 [Właściwości sesji wydajności](../profiling/performance-session-properties.md)   
 [Procesor CPU i liczniki systemu Windows](../profiling/cpu-and-windows-counters.md)