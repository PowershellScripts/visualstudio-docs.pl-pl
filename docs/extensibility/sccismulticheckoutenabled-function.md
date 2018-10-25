---
title: Funkcja SccIsMultiCheckoutEnabled | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- SccIsMultiCheckoutEnabled
helpviewer_keywords:
- SccIsMultiCheckoutEnabled function
ms.assetid: 6721639d-e475-4766-81b5-ee40a280fc70
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: e4a71f839c2129bcfb699188dec09b02b18d4cd1
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49920121"
---
# <a name="sccismulticheckoutenabled-function"></a>SccIsMultiCheckoutEnabled, funkcja
Ta funkcja sprawdza, czy wtyczka do kontroli źródła zezwala na wiele operacji wyewidencjonowania w pliku.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
SCCRTN SccIsMultiCheckoutEnabled(  
   LPVOID pContext,  
   LPBOOL pbMultiCheckout  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 pContext  
 [in] Struktura kontekście wtyczki kontroli źródła.  
  
 pbMultiCheckout  
 [out] Określa, czy wiele operacji wyewidencjonowania są włączone dla tego projektu (obsługujące wiele operacji wyewidencjonowania oznacza wartość różną od zera).  
  
## <a name="return-value"></a>Wartość zwracana  
 Implementacja wtyczki kontroli źródła tej funkcji powinien zwrócić jedną z następujących wartości:  
  
|Wartość|Opis|  
|-----------|-----------------|  
|SCC_OK|Sprawdzanie zakończyło się pomyślnie.|  
|SCC_E_NONSPECIFICERROR<br /><br /> SCC_E_UNKNOWNERROR|Wystąpił nieokreślony błąd.|  
  
## <a name="remarks"></a>Uwagi  
 IDE ułatwia dwóch kontroli, aby określić, jeśli pliki mogą zostać wyewidencjonowane jednocześnie przez więcej niż jednego użytkownika. Po pierwsze system kontroli źródła musi obsługiwać wiele operacji wyewidencjonowania. Wtyczka do kontroli źródła można określić tę możliwość podczas inicjowania, określając `SCC_CAP_MULTICHECKOUT`. Następnie drugiego wyboru IDE wywołuje tę funkcję, aby określić, czy bieżący projekt obsługuje wiele operacji wyewidencjonowania. Jeśli wiele operacji wyewidencjonowania są obsługiwane dla wybranego projektu, wtyczka zwraca Powodzenie kodu i ustawia `pbMultiCheckout` na wartość różną od zera (`TRUE`) lub `FALSE`.  
  
## <a name="see-also"></a>Zobacz też  
 [Funkcje interfejsu API wtyczki kontroli źródła ](../extensibility/source-control-plug-in-api-functions.md)