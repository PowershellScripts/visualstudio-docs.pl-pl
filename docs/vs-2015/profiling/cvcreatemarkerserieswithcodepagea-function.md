---
title: Funkcja CvCreateMarkerSeriesWithCodePageA | Dokumentacja firmy Microsoft
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
- cvmakers/CvCreateMarkerSeriesWithCodePageA
helpviewer_keywords:
- CvCreateMarkerSeriesWithCodePageA method
ms.assetid: 3d7ed601-2222-4be9-a557-f217db008753
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: fda15e064c4a8d14ebb2d145ba9f2fa5c050ce2e
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49239047"
---
# <a name="cvcreatemarkerserieswithcodepagea-function"></a>CvCreateMarkerSeriesWithCodePageA — Funkcja
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Tworzy serię znacznika dla danego dostawcy i określona strona kodowa. Ta funkcja może służyć do określenia strony kodowej jawnie dla tekstu, napisanych przez funkcje API ANSI znacznika. Ustawianie strony kodowej może być przydatne w przypadku, gdy śledzenie jest przechwycony i następnie analizowane na różnych maszynach, za pomocą różnych ustawień regionalnych/języków. Domyślnie używany jest zwrócona przez funkcję GetACP() strony kodowej.  
  
## <a name="syntax"></a>Składnia  
  
```  
HRESULT CvCreateMarkerSeriesWithCodePageA(  
   _In_ PCV_PROVIDER pProvider,  
   _In_ LPCSTR pSeriesName,  
   _In_ UINT nTextCodePage,  
   _Out_ PCV_MARKERSERIES* ppMarkerSeries  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pProvider`  
 Poprzednio inicjowany przez cvinitprovider — obiekt dostawcy. Nie może mieć wartości NULL.  
  
 `pSeriesName`  
 Nazwa serii znacznika. Nie może mieć wartości NULL, ale dozwolone jest pustym ciągiem.  
  
 `nTextCodePage`  
 Prawidłowy kod strony.  
  
 `ppMarkerSeries`  
 Adres zmiennej danych wyjściowych, który będzie przechowywał znaczników serii kontekstu. Nie może mieć wartości NULL.  
  
## <a name="return-value"></a>Wartość zwracana  
 S_OK znaczników serii został pomyślnie utworzony lub kod błędu w przypadku zostały wszystkie błędy. Aby sprawdzić, czy warunek błędu, należy użyć makra Powodzenie/niepowodzenie.  
  
## <a name="requirements"></a>Wymagania  
 **Nagłówek:** cvmarkers.h  
  
## <a name="see-also"></a>Zobacz też  
 [Odwołanie do biblioteki języka C++](../profiling/cpp-library-reference.md)



