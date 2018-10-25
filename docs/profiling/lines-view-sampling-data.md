---
title: Widok linii - dane próbkowania | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- Lines view
ms.assetid: 46497249-c797-42c5-a02c-3e4bb3b4ee60
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: cb965b9a93a278a4c51ea4661f683ebafc2838fd
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49914817"
---
# <a name="lines-view---sampling-data"></a>Widok linii — dane próbkowania
Uruchom wiersze widok pobierania próbek danych zawiera dane o wydajności dla instrukcji, które były wykonywane w chwili przykłady zostały zebranych podczas profilowania.  
  
> [!NOTE]
>  Ulepszone funkcje zabezpieczeń w systemie Windows 8 i Windows Server 2012 wymagają znaczących zmian w taki sposób, programu Visual Studio profiler zbiera dane na tych platformach. Aplikacje platformy uniwersalnej systemu Windows również wymagają nowych technik zbierania. Zobacz [narzędzia do oceny wydajności w aplikacjach systemu Windows 8 i Windows Server 2012](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).  
  
 W pliku źródłowym instrukcji może obejmować więcej niż jeden wiersz w pliku źródłowym, a jeden wiersz może zawierać więcej niż jedną instrukcję. Instrukcja jest identyfikowane przez następujące elementy:  
  
- Plik źródłowy, który zawiera deklarację funkcji.  
  
- Funkcja, która zawiera instrukcję.  
  
- Wiersza źródłowego, od której rozpoczyna się wykonywanie instrukcji.  
  
- Znak w wierszu źródłowym, w którym rozpoczyna się wykonywanie instrukcji.  
  
- Wiersza źródłowego, w którym kończy się instrukcji.  
  
- Znak w wierszu źródłowym, w którym kończy się instrukcji.  
  
  Kolumna Nazwa wiersza zawiera wzorzec sortowalnej łączenia danych identyfikator.  
  
  Zgodnie z definicją instrukcja wywołuje inne funkcje. W związku z tym są wyświetlane tylko wyłączne wartości.  
  
|Kolumny|Opis|  
|------------|-----------------|  
|**Identyfikator procesu**|Identyfikator procesu (PID) uruchomienia profilowania.|  
|**Nazwa procesu**|Nazwa procesu.|  
|**Nazwa modułu**|Nazwa modułu, który zawiera wiersz funkcji.|  
|**Ścieżka modułu**|Ścieżka modułu, który zawiera wiersz funkcji.|  
|**Plik źródłowy**|Plik źródłowy, zawierające następujący wiersz w funkcji.|  
|**Nazwa funkcji**|Nazwa funkcji.|  
|**Numer wiersza funkcji**|Numer wiersza początku tej funkcji w pliku źródłowym.|  
|**Adres funkcji**|Adres początkowy funkcji.|  
|**Początkowy wiersz w źródle**|Numer wiersza początkowego w pliku źródłowym, w którym zostały zebrane w tym przykładzie.|  
|**Końcowy wiersz w źródle**|Końcowy numer wiersza w pliku źródłowym, w którym zostały zebrane w tym przykładzie.|  
|**Początkowy znak w źródle**|Przesunięcie początkowy znak w wierszu pliku źródłowego, w którym zostały zebrane w tym przykładzie.|  
|**Końcowy znak w źródle**|Przesunięcie końcowy znak w wierszu pliku źródłowego, w którym zostały zebrane w tym przykładzie.|  
|**Nazwa wiersza**|Generowane przez program profilujący identyfikator wiersza przy użyciu następującej składni:`Source File`**; [**  `Line Number Start` **,**`Character Start`**] ->; [** `Line Number End`**,**`Character End`**]**|  
|**Próbki wyłączne**|Łączna liczba próbek, które zostały zebrane podczas wykonywania wiersza funkcji.|  
|**% Wyłącznych próbek**|Procent wszystkich przykładów podczas uruchomienia profilowania, które zostały zebrane podczas wykonywania wiersza funkcji.|  
  
## <a name="see-also"></a>Zobacz także  
 [Widok linii - próbkowanie](../profiling/lines-view-dotnet-memory-sampling-data.md)