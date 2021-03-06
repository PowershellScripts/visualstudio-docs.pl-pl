---
title: Widok wskaźników instrukcji (IP) - dane próbkowania | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- Instruction Pointers view
ms.assetid: c7f647bb-c5a3-4708-9f9d-33c0fd6e2e96
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 2fdc7069ee0d422fd59b297b4b99a982d265e3a2
ms.sourcegitcommit: ce154aee5b403d5c1c41da42302b896ad3cf8d82
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/07/2018
ms.locfileid: "34844283"
---
# <a name="instruction-pointers-ips-view---sampling-data"></a>Widok wskaźników instrukcji (IP) - dane próbkowania
Widok IP dane wydajności wyświetla dane instrukcje zestawu, które były wykonywane bezpośrednio w chwili przykłady zostały zebrane w przebiegu profilowania próbkowania.  
  
> [!NOTE]
>  Ulepszone funkcje zabezpieczeń w systemie Windows 8 i Windows Server 2012 wymagane znaczących zmian w sposobie profilera Visual Studio zbiera dane na tych platformach. Aplikacje platformy uniwersalnej systemu Windows wymagają również nowe techniki kolekcji. Zobacz [narzędzi wydajności w przypadku aplikacji systemu Windows 8 i Windows Server 2012](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).  
  
|Kolumny|Opis|  
|------------|-----------------|  
|**Identyfikator procesu**|Identyfikator PID profilowania Uruchom proces.|  
|**Nazwa procesu**|Nazwa procesu.|  
|**Nazwa modułu**|Nazwa modułu, który zawiera instrukcję.|  
|**Ścieżka modułu**|Ścieżka moduł, który zawiera instrukcję.|  
|**Plik źródłowy**|Plik źródłowy, który zawiera instrukcję.|  
|**Nazwa funkcji**|Nazwa funkcji, która zawiera instrukcję.|  
|**Numer wiersza — funkcja**|Numer wiersza początku tej funkcji w pliku źródłowym.|  
|**Adres funkcji**|Początkowy adres pamięci funkcji w załadować dane binarne.|  
|**Początek wiersza źródłowego**|Numer wiersza początkowego w pliku źródłowym, w którym zostały zebrane w tym przykładzie.|  
|**Źródło końca wiersza**|Końcowy numer wiersza pliku źródłowego, w którym zostały zebrane w tym przykładzie.|  
|**Rozpocznij znaków źródła**|Przesunięcie początkowy znak w wiersza pliku źródłowego, w którym zostały zebrane w tym przykładzie.|  
|**Źródło znak końcowy**|Przesunięcie znak końcowy w wiersza pliku źródłowego, w którym zostały zebrane w tym przykładzie.|  
|**Adres instrukcji**|Adres instrukcji w załadowanych danych binarnych.|  
|**Wyłącznych próbek**|Łączna liczba próbek, które zostały zebrane podczas wykonywania instrukcji.|  
|**% Wyłącznych próbek**|Procent wszystkich próbek w przebiegu profilowania, które zostały zebrane podczas wykonywania instrukcji.|  
  
## <a name="see-also"></a>Zobacz także  
 [Wskaźników instrukcji (IP) View - próbkowanie](../profiling/instruction-pointers-ips-view-dotnet-memory-sampling-data.md)