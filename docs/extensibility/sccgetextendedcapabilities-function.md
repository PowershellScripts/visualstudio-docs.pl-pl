---
title: Funkcja SccGetExtendedCapabilities | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: SccGetExtendedCapabilities
helpviewer_keywords: SccGetExtendedCapabilities function
ms.assetid: 588c6a92-2147-4d8b-a357-96ca7da0a092
caps.latest.revision: "16"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: d5134116a9d6a8d7872692e88ecd8adf60e9c02e
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="sccgetextendedcapabilities-function"></a>Funkcja SccGetExtendedCapabilities
Ta funkcja zwraca dodatkowe funkcje obsługiwane przez wtyczkę kontroli źródła.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
SCCRTN SccGetExtendedCapabilities(  
   LPVOID pContext,  
   LONG lSccExCaps,  
   LPBOOL pbSupported  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 pContext  
 [in] Wskaźnik kontekstu wtyczkę kontroli źródła.  
  
 lSccExCaps  
 [in] Flagi Określanie rozszerzone możliwości, do których chcesz przetestować (znajdują się w tabeli rozszerzonego kodu możliwości [flagi możliwości](../extensibility/capability-flags.md) flag możliwe).  
  
 pbSupported  
 [out] Zwraca wartość inną niż zero (`TRUE`), jeśli określona funkcja jest obsługiwana; w przeciwnym wypadku zwraca wartość zero (`FALSE`).  
  
## <a name="return-value"></a>Wartość zwracana  
 Implementacja wtyczkę kontroli źródła tej funkcji może przywrócić jedną z następujących wartości:  
  
|Wartość|Opis|  
|-----------|-----------------|  
|SCC_OK|Pomyślnie ukończono operację możliwości get.|  
|SCC_E_UNKNOWNERROR<br /><br /> SCC_E_NONSPECIFICERROR|Wystąpił nieznany lub nieokreślony błąd.|  
  
## <a name="remarks"></a>Uwagi  
 Ta metoda jest wywoływana na żądanie; oznacza to, gdy możliwości należy zbadać, ta metoda jest wywoływana w celu określenia, czy obsługiwaną możliwości. Określono tylko jedną flagę naraz.  
  
## <a name="see-also"></a>Zobacz też  
 [Funkcje API wtyczkę kontroli źródła](../extensibility/source-control-plug-in-api-functions.md)   
 [Kody błędów](../extensibility/error-codes.md)   
 [Flagi możliwości](../extensibility/capability-flags.md)