---
title: IActiveScriptError::GetSourceLineText | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptError.GetSourceLineText
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptError_GetSourceLineText
ms.assetid: 64f7f37f-7288-4dbe-b626-a35d90897f36
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: bb886d5f40042313483dc3b298488d1291c30563
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2017
ms.locfileid: "24793303"
---
# <a name="iactivescripterrorgetsourcelinetext"></a>IActiveScriptError::GetSourceLineText
Pobiera wiersz w pliku źródłowym, w którym błąd wystąpił w trakcie aparat skryptów skryptu.  
  
## <a name="syntax"></a>Składnia  
  
```  
HRESULT GetSourceLineText(  
    BSTR *pbstrSourceLine  // address of buffer for source line  
);  
```  
  
## <a name="parameter"></a>Parametr  
 `pbstrSourceLine`  
 [out] Adres buforu, który odbiera wiersz kodu źródłowego, w którym wystąpił błąd.  
  
## <a name="return-value"></a>Wartość zwracana  
 Zwraca `S_OK` w przypadku powodzenia lub `E_FAIL` Jeśli wiersz w pliku źródłowym nie została pobrana.  
  
## <a name="see-also"></a>Zobacz też  
 [IActiveScriptError](../../winscript/reference/iactivescripterror.md)