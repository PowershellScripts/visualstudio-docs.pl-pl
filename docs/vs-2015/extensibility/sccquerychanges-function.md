---
title: Funkcja SccQueryChanges | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- SccQueryChanges
helpviewer_keywords:
- SccQueryChanges function
ms.assetid: 4cd58eb3-6952-49b1-9620-8682e3eaa604
caps.latest.revision: 14
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 8dea3152dcebeff667df99f52f05f2ac39a50aa6
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49848647"
---
# <a name="sccquerychanges-function"></a>SccQueryChanges, funkcja
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Ta funkcja wylicza danej listy plików, przekazywania informacji na temat zmiany nazwy dla każdego pliku za pomocą funkcji wywołania zwrotnego.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
SCCRTN SccQueryChanges(  
   LPVOID           pContext,  
   LONG             nFiles,  
   LPCSTR*          lpFileNames,  
   QUERYCHANGESFUNC pfnCallback,  
   LPVOID           pvCallerData  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 pContext  
 [in] Wskaźnik kontekście wtyczki kontroli źródła.  
  
 Niepowodzeń  
 [in] Liczba plików w `lpFileNames` tablicy.  
  
 lpFileNames  
 [in] Tablica nazw plików, aby uzyskać informacje na.  
  
 pfnCallback  
 [in] Funkcja wywołania zwrotnego do wywołania dla każdej nazwy pliku na liście (patrz [QUERYCHANGESFUNC](../extensibility/querychangesfunc.md) Aby uzyskać szczegółowe informacje).  
  
 pvCallerData  
 [in] Niezmieniona wartość, które zostaną przekazane do funkcji wywołania zwrotnego.  
  
## <a name="return-value"></a>Wartość zwracana  
 Implementacja wtyczki kontroli źródła tej funkcji powinien zwrócić jedną z następujących wartości:  
  
|Wartość|Opis|  
|-----------|-----------------|  
|SCC_OK|Proces wykonywania zapytania, zostało ukończone pomyślnie.|  
|SCC_E_PROJNOTOPEN|Projekt nie został otwarty w kontroli źródła.|  
|SCC_E_ACCESSFAILURE|Wystąpił problem podczas uzyskiwania dostępu do systemu kontroli źródła, prawdopodobnie z powodu problemów z siecią lub rywalizacji o zasoby.|  
|SCC_E_NONSPECIFICERROR|Wystąpił nieokreślony lub ogólny błąd.|  
  
## <a name="remarks"></a>Uwagi  
 Odpytywane dla zmiany są do przestrzeni nazw: ściślej mówiąc, zmiana nazwy, dodawania i usuwania pliku.  
  
## <a name="see-also"></a>Zobacz też  
 [Funkcje interfejsu API wtyczki kontroli źródła](../extensibility/source-control-plug-in-api-functions.md)   
 [QUERYCHANGESFUNC](../extensibility/querychangesfunc.md)   
 [Kody błędów](../extensibility/error-codes.md)

