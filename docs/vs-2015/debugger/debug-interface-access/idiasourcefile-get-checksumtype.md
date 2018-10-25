---
title: Idiasourcefile::get_checksumtype — | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- IDiaSourceFile::get_checksumType method
ms.assetid: 4c363e61-a6a9-409a-9cc0-d06eb2bee645
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: e7fbc18256ad9bbc927cb003b7cea51e15f13751
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49919616"
---
# <a name="idiasourcefilegetchecksumtype"></a>IDiaSourceFile::get_checksumType
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Pobiera typ sumy kontrolnej.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
HRESULT get_checksumType (   
   DWORD* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pRetVal`  
 [out] Zwraca typ sumy kontrolnej.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Typ sumy kontrolnej to wartości, które mogą być mapowane do algorytmu sumy kontrolnej. Na przykład standardowy format pliku PDB zazwyczaj może mieć jedną z następujących wartości:  
  
|Typ sumy kontrolnej|Etykieta interfejsu CryptoAPI|Opis|  
|-------------------|---------------------|-----------------|  
|0|\<Brak >|Nie istnieje sumy kontrolnej.|  
|1|`CALG_MD5`|Suma kontrolna jest generowany przy użyciu algorytmu wyznaczania wartości skrótu MD5.|  
|2|`CALG_SHA1`|Suma kontrolna jest generowany przy użyciu algorytmu wyznaczania wartości skrótu SHA1.|  
  
 `CryptoAPI` Etykiety są z `ALG_ID` wyliczenia. Aby uzyskać więcej informacji na temat algorytmy wyznaczania wartości skrótu, zapoznaj się `CryptoAPI` sekcji Microsoft [!INCLUDE[winsdkshort](../../includes/winsdkshort-md.md)].  
  
 Aby uzyskać bajtów rzeczywista suma kontrolna pliku źródłowego, należy wywołać [idiasourcefile::get_checksum —](../../debugger/debug-interface-access/idiasourcefile-get-checksum.md) metody.  
  
## <a name="see-also"></a>Zobacz też  
 [Idiasourcefile —](../../debugger/debug-interface-access/idiasourcefile.md)   
 [IDiaSourceFile::get_checksum](../../debugger/debug-interface-access/idiasourcefile-get-checksum.md)



