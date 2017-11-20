---
title: Funkcja SccAddFilesFromSCC | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: SccAddFilesFromSCC
helpviewer_keywords: SccAddFilesFromSCC function
ms.assetid: f21a3500-ade8-4dd8-8647-10e2179be9c1
caps.latest.revision: "17"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 1764bfc503e25860326b1910c432edcf95c8f21c
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="sccaddfilesfromscc-function"></a>Funkcja SccAddFilesFromSCC
Ta funkcja dodaje listę plików z kontroli źródła do aktualnie otwartego projektu.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
SCCRTN SccAddFilesFromSCC(  
   LPVOID  pContext,  
   HWND    hWnd,  
   LPSTR   lpUser,  
   LPSTR   lpAuxProjPath,  
   LONG    cFiles,  
   LPCSTR* lpFilePaths,  
   LPCSTR  lpDestination,  
   LPCSTR  lpComment,  
   LPBOOL  pbResults  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 pContext  
 [in] Wskaźnik kontekstu wtyczkę kontroli źródła.  
  
 Właściwość hWnd  
 [in] Dojście do okna IDE, które wtyczka do kontroli źródła można używać jako elementu nadrzędnego wszystkie okna dialogowe, które zawiera.  
  
 lpUser  
 [w, out] Nazwa użytkownika (do SCC_USER_SIZE, włącznie z terminatorem null).  
  
 lpAuxProjPath  
 [w, out] Pomocnicze ciąg identyfikujący projektu (maksymalnie `SCC_PRJPATH_`rozmiar, włącznie z terminatorem null).  
  
 cFiles  
 [in] Liczba plików przez `lpFilePaths`.  
  
 lpFilePaths  
 [w, out] Tablica nazw plików do dodania do bieżącego projektu.  
  
 lpDestination  
 [in] Ścieżka docelowa, gdzie są pliki do zapisania.  
  
 lpComment  
 [in] Komentarz, który ma zostać zastosowany do wszystkich przekazywanych plików.  
  
 pbResults  
 [w, out] Tablica flag, które są zestawu, informując o powodzeniu (różną od zera lub TRUE) lub Niepowodzenie (zero lub wartość FAŁSZ) dla każdego pliku (rozmiar tablicy musi wynosić co najmniej `cFiles` długa).  
  
## <a name="return-value"></a>Wartość zwracana  
 Implementacja wtyczkę kontroli źródła tej funkcji może przywrócić jedną z następujących wartości:  
  
|Wartość|Opis|  
|-----------|-----------------|  
|SCC_E_PROJNOTOPEN|Projekt nie jest otwarty.|  
|SCC_E_OPNOTPERFORMED|Połączenie nie jest w tym samym projekcie określony przez`lpAuxProjPath.`|  
|SCC_E_NOTAUTHORIZED|Użytkownik nie ma uprawnień do aktualizacji bazy danych.|  
|SCC_E_NONSPECIFICERROR|Wystąpił nieznany błąd.|  
|SCC_I_RELOADFILE|Plik lub projekt musi zostać ponownie załadowana.|  
  
## <a name="see-also"></a>Zobacz też  
 [Funkcje API wtyczkę kontroli źródła](../extensibility/source-control-plug-in-api-functions.md)