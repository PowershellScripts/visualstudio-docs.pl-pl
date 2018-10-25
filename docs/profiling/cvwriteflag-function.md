---
title: Funkcja CvWriteFlag | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- cvmarkers/CvWriteFlagExVA
- cvmarkers/CvWriteFlagExW
- cvmarkers/CvWriteFlagExVW
- cvmarkers/CvWriteFlagExA
helpviewer_keywords:
- CvWriteFlagExW method
- CvWriteFlagExVA method
- CvWriteFlagExA method
- CvWriteFlagExVW method
ms.assetid: ee9da1e2-7b34-4cba-81e2-215d25d32e4d
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 371be943dc062c5c3b5aac7f59493aa5f4f53002
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49897153"
---
# <a name="cvwriteflag-function"></a>Cvwriteflag — funkcja
Zapisuje plik śledzenia Concurrency Visualizer flagę.  
  
## <a name="syntax"></a>Składnia  
  
```C  
HRESULT CvWriteFlagExW(  
    _In_reads_bytes_(16) PCV_MARKERSERIES pMarkerSeries,  
    _In_ CV_IMPORTANCE level,  
    _In_ int category,  
    _In_ PCWSTR pMessage,  
    ...  
    );  
  
HRESULT CvWriteFlagExA(  
    _In_reads_bytes_(16) PCV_MARKERSERIES pMarkerSeries,  
    _In_ CV_IMPORTANCE level,  
    _In_ int category,  
    _In_ PCSTR pMessage,  
    ...  
    );  
  
HRESULT CvWriteFlagExVW(  
    _In_reads_bytes_(16) PCV_MARKERSERIES pMarkerSeries,  
    _In_ CV_IMPORTANCE level,  
    _In_ int category,  
    _In_ PCWSTR pMessage,  
    _In_ va_list argList);  
  
HRESULT CvWriteFlagExVA(  
    _In_reads_bytes_(16) PCV_MARKERSERIES pMarkerSeries,  
    _In_ CV_IMPORTANCE level,  
    _In_ int category,  
    _In_ PCSTR pMessage,  
    _In_ va_list argList);  
```  
  
#### <a name="parameters"></a>Parametry  
 `argList`  
 Lista argumentów.  
  
 `category`  
 Kategoria.  
  
 `level`  
 Poziom ważności.  
  
 `pMarkerSeries`  
 Kontekst serii prawidłowe znacznika. Nie może mieć wartości NULL.  
  
 `pMessage`  
 Ciąg formatu komunikatów. Nie może mieć wartości NULL.  
  
## <a name="return-value"></a>Wartość zwracana  
 S_OK, gdy komunikat jest pomyślnie zapisane. Kod błędu w przypadku, gdy było żadnych błędów. Aby sprawdzić, czy warunek błędu, należy użyć makra Powodzenie/niepowodzenie.  
  
## <a name="requirements"></a>Wymagania  
 **Nagłówek:** *cvmarkers.h*  
  
 **Unicode:** cvwriteflagexw —, cvwriteflagexvw —  
  
 <strong>ANSI:</strong>cvwriteflagexa —, cvwriteflagexva —  
  
## <a name="see-also"></a>Zobacz także  
 [Odwołanie do biblioteki języka C++](../profiling/cpp-library-reference.md)