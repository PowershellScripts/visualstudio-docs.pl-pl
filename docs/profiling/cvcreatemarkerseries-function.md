---
title: "Cvcreatemarkerseries — funkcja | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- cvmarkers/CvCreateMarkerSeriesA
- cvmarkers/CvCreateMarkerSeriesW
helpviewer_keywords:
- CvCreateMarkerSeriesA method
- CvCreateMarkerSeriesW method
ms.assetid: e280530b-137a-43a7-8643-aa514ab86ed7
caps.latest.revision: "3"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 5eccac7a0b139b830121add61518c23fa055ca23
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="cvcreatemarkerseries-function"></a>CvCreateMarkerSeries — Funkcja
Tworzy serię znacznika dla podanego dostawcy.  
  
## <a name="syntax"></a>Składnia  
  
```  
_Check_return_ HRESULT CvCreateMarkerSeriesW(  
    _In_ PCV_PROVIDER  pProvider,  
    _In_ LPCWSTR pSeriesName,  
    _Out_ PCV_MARKERSERIES* ppMarkerSeries);  
  
_Check_return_ HRESULT CvCreateMarkerSeriesA(  
    _In_ PCV_PROVIDER  pProvider,  
    _In_ LPCSTR pSeriesName,  
    _Out_ PCV_MARKERSERIES* ppMarkerSeries);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pProvider`  
 Obiekt dostawcy poprzednio inicjowany przez CvInitProvider. Nie może mieć wartości NULL.  
  
 `pSeriesName`  
 Nazwa serii znacznika. Nie może mieć wartości NULL, ale może być ciągiem pustym.  
  
 `ppMarkerSeries`  
 Adres zmiennej danych wyjściowych, która zapisze w kontekście serii znacznika. Nie może mieć wartości NULL.  
  
## <a name="return-value"></a>Wartość zwracana  
 S_OK serii znacznika został utworzony pomyślnie lub kod błędu w przypadku zostały wszystkie błędy. Użyj makra powiodło się/nie powiodło się, aby sprawdzić warunku błędu.  
  
## <a name="requirements"></a>Wymagania  
 **Nagłówek:** cvmarkers.h  
  
 **Unicode:** CvCreateMarkerSeriesW  
  
 **ANSI:** CvCreateMarkerSeriesA  
  
## <a name="see-also"></a>Zobacz też  
 [Odwołanie do biblioteki C++](../profiling/cpp-library-reference.md)