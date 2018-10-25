---
title: Funkcja SccUninitialize | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- SccUninitialize
helpviewer_keywords:
- SccUninitialize function
ms.assetid: 17cf5337-d251-4422-bc96-93fe7d48f2ae
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: e9d992428dd6358cee2b6a46efc0816e7840c449
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49948034"
---
# <a name="sccuninitialize-function"></a>SccUninitialize, funkcja
Ta funkcja czyści wszystkie alokacje lub otwartych połączeń utworzonych przez poprzednie wywołanie [SccInitialize](../extensibility/sccinitialize-function.md) w ramach przygotowania do zamykania wtyczka do kontroli źródła.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
SCCRTN SccUninitialize (  
   LPVOID pvContext  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 pvContext  
 [in] Wskaźnik do struktury kontekście wtyczki kontroli źródła, utworzone w [SccInitialize](../extensibility/sccinitialize-function.md).  
  
## <a name="return-value"></a>Wartość zwracana  
 Implementacja wtyczki kontroli źródła tej funkcji powinien zwrócić jedną z następujących wartości:  
  
|Wartość|Opis|  
|-----------|-----------------|  
|SCC_OK|Oczyszczania została ukończona pomyślnie.|  
  
## <a name="remarks"></a>Uwagi  
 Wtyczka do kontroli źródła jest odpowiedzialny za przygotowywanie zamknięcie i zwalnianie pamięci, że wtyczka została przydzielona w strukturze kontekstu. Funkcja jest wywoływana raz dla każdego wystąpienia danego dodatku typu plug-in. Wywołanie [SccInitialize](../extensibility/sccinitialize-function.md) poprzedza tego wywołania. Brak projektów nadal może być otwarty w momencie wywołania `SccUninitialize`.  
  
## <a name="see-also"></a>Zobacz też  
 [Funkcje interfejsu API wtyczki kontroli źródła](../extensibility/source-control-plug-in-api-functions.md)   
 [SccInitialize](../extensibility/sccinitialize-function.md)