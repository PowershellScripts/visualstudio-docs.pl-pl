---
title: Tworzenie Portable profilowania pliki danych z poziomu wiersza polecenia | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 2ceb63a7-b835-4988-b756-2afc3fcc4808
caps.latest.revision: "6"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f222856d16033cba5ae089c19081efeefe744aa5
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="creating-portable-profiling-data-files-from-the-command-line"></a>Tworzenie przenośnych plików danych profilowania z wiersza polecenia
Aby udostępnianie danych profilowania, można użyć [VSPerfReport](../profiling/vsperfreport.md) narzędzia wiersza polecenia, aby osadzić symboli dla profilowania do pliku Vsp.  
  
 Można także utworzyć wstępnie przeanalizowane plik danych (vsps) profilowania jest mniejszy, który jest szybsze do obciążenia w środowisku IDE.  
  
> [!NOTE]
>  Upewnij się, że pliki symboli (.pdb) są dostępne dla **VSPerfReport**. Aby uzyskać więcej informacji, zobacz [porady: Określanie lokalizacji plików symboli z wiersza polecenia](../profiling/how-to-specify-symbol-file-locations-from-the-command-line.md).  
>   
>  Aby uzyskać informacje o ścieżce do **VSReport**, zobacz [Określanie ścieżki do narzędzi wiersza polecenia](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md).  
>   
>  Nie można filtrować dane profilowania w pliku vsps.  
  
### <a name="to-embed-the-symbols-for-a-profiling-run-into-a-profiling-data-vsp-file"></a>Aby osadzić symboli dla profilowania do profilowania plik danych (Vsp)  
  
-   W oknie wiersza polecenia wpisz następujące polecenie:  
  
     \<Ścieżka >**VSPerfReport \<** pliku VSP > **/PackSymbols**  
  
     Domyślnie plik vsps nosi nazwę o nazwie podstawowej pliku Vsp. Można określić nazwę alternatywną, za pomocą **dane wyjściowe** opcji.  
  
### <a name="to-create-a-summary-profiling-data-file"></a>Aby utworzyć plik podsumowania danych profilowania  
  
-   W oknie wiersza polecenia wpisz następujące polecenie:  
  
     \<Ścieżka >**VSPerfReport \<** pliku VSP > **/SummaryFile** [**/Output:**\<nazwa pliku >]  
  
     Domyślnie plik vsps nosi nazwę o nazwie podstawowej pliku Vsp. Można określić nazwę alternatywną, za pomocą **dane wyjściowe** opcji.