---
title: Funkcja SccBackgroundGet | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: SccBackgroundGet
helpviewer_keywords: SccBackgroundGet function
ms.assetid: 69817e52-b9ac-4f4d-820b-2cc9c384f0dc
caps.latest.revision: "13"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 85b700f0cb1e3a364cae69ff6c628151ea6a7bd3
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="sccbackgroundget-function"></a>Funkcja SccBackgroundGet
Ta funkcja pobiera z kontroli źródła każdego określonych plików bez interakcji użytkownika.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
SCCRTN SccBackgroundGet(  
   LPVOID  pContext,  
   LONG    nFiles,  
   LPCSTR* lpFileNames,  
   LONG    dwFlags,  
   LONG    dwBackgroundOperationID  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 pContext  
 [in] Wskaźnik kontekstu wtyczkę kontroli źródła.  
  
 To  
 [in] Liczba plików określonych w `lpFileNames` tablicy.  
  
 lpFileNames  
 [w, out] Tablica nazw plików, które mają zostać pobrane.  
  
> [!NOTE]
>  Nazwy musi być w pełni kwalifikowanej nazwy plików lokalnych.  
  
 wartość elementu dwFlags  
 [in] Polecenie flagi (`SCC_GET_ALL`, `SCC_GET_RECURSIVE`).  
  
 dwBackgroundOperationID  
 [in] Unikatowa wartość skojarzone z tą operacją.  
  
## <a name="return-value"></a>Wartość zwracana  
 Implementacja wtyczkę kontroli źródła tej funkcji może przywrócić jedną z następujących wartości:  
  
|Wartość|Opis|  
|-----------|-----------------|  
|SCC_OK|Operacja została ukończona pomyślnie.|  
|SCC_E_BACKGROUNDGETINPROGRESS|Pobieranie tła jest już w toku (wtyczkę kontroli źródła powinna zwracać to tylko wtedy, gdy nie obsługuje operacji wsadowych jednoczesnych).|  
|SCC_I_OPERATIONCANCELED|Operacja została anulowana przed kończone.|  
  
## <a name="remarks"></a>Uwagi  
 Ta funkcja jest wywoływana zawsze na wątku innego niż ten, który załadowano wtyczkę kontroli źródła. Ta funkcja nie powinien zwrócić, dopóki zakończy działania; jednak może ona zostać wywołana wiele razy przy użyciu wielu list plików, wszystkie w tym samym czasie.  
  
 Korzystanie z `dwFlags` argument jest taka sama jak [SccGet](../extensibility/sccget-function.md).  
  
## <a name="see-also"></a>Zobacz też  
 [Funkcje API wtyczkę kontroli źródła](../extensibility/source-control-plug-in-api-functions.md)   
 [SccGet](../extensibility/sccget-function.md)