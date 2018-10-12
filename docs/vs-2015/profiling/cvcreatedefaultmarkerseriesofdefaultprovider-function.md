---
title: Funkcja CvCreateDefaultMarkerSeriesOfDefaultProvider | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- cvmarkers/CvCreateDefaultMarkerSeriesOfDefaultProvider
helpviewer_keywords:
- CvCreateDefaultMarkerSeriesOfDefaultProvider method
ms.assetid: 24eb80f8-8fca-4c47-93b5-bb1eb8ffdffd
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: e9d899bde342f61d3d10afca204527526197d2ac
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49190661"
---
# <a name="cvcreatedefaultmarkerseriesofdefaultprovider-function"></a>CvCreateDefaultMarkerSeriesOfDefaultProvider — Funkcja
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Tworzy domyślny znaczników serii domyślnego dostawcę.  
  
## <a name="syntax"></a>Składnia  
  
```  
HRESULT CvCreateDefaultMarkerSeriesOfDefaultProvider(  
   _Out_ PCV_PROVIDER* ppProvider,  
   _Out_ PCV_MARKERSERIES* ppMarkerSeries  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppProvider`  
 Adres dostawcy zmiennej obiektu. Adres nie może mieć wartości NULL, zmienna może mieć dowolną wartość.  
  
 `ppMarkerSeries`  
 Adres zmiennej obiektu serii znacznika. Adres nie może mieć wartości NULL, zmienna może mieć dowolną wartość.  
  
## <a name="return-value"></a>Wartość zwracana  
 S_OK, gdy zarówno dostawca, jak i znaczników serii zostały utworzone pomyślnie lub kod błędu w przypadku zostały wszystkie błędy. Aby sprawdzić, czy warunek błędu, należy użyć makra Powodzenie/niepowodzenie.  
  
## <a name="requirements"></a>Wymagania  
 **Nagłówek:** cvmarkers.h  
  
## <a name="see-also"></a>Zobacz też  
 [Odwołanie do biblioteki języka C++](../profiling/cpp-library-reference.md)



