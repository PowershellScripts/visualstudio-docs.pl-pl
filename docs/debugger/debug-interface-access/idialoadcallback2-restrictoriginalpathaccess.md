---
title: IDiaLoadCallback2::RestrictOriginalPathAccess | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: IDiaLoadCallback2::RestrictOriginalPathAccess method
ms.assetid: 31fde3af-2824-4b0f-8d0d-cee6046596f6
caps.latest.revision: "8"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 826cebba9d4eaf8e2bcf6d055a2ce524e1cf17d0
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idialoadcallback2restrictoriginalpathaccess"></a>IDiaLoadCallback2::RestrictOriginalPathAccess
Określa, czy można wyszukać plik PDB w oryginalnym katalogu debugowania.  
  
## <a name="syntax"></a>Składnia  
  
```C++  
HRESULT RestrictOriginalPathAccess ();  
```  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Inne niż powrotnych kodu `S_OK` uniemożliwia szuka pliku PDB w oryginalnym katalogu debugowania. Oryginalny katalog debugowania jest ścieżka do pliku symboli skompilowany do pliku wykonywalnego, gdy włączone jest debugowanie. Ta ścieżka nie jest zawsze taka sama jak ścieżka, w której istnieje plik wykonywalny.  
  
## <a name="see-also"></a>Zobacz też  
 [Idialoadcallback2 —](../../debugger/debug-interface-access/idialoadcallback2.md)