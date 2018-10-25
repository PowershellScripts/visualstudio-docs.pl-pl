---
title: IDiaStackWalkHelper::pdataForVA | Dokumentacja firmy Microsoft
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
- IDiaStackWalkHelper2::pdataByVA method
ms.assetid: fafc38fe-74dc-4726-9a51-eebf3a673d7f
caps.latest.revision: 14
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 525a19a997d5902da5d69d5804281d472b5d6a26
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49906224"
---
# <a name="idiastackwalkhelperpdataforva"></a>IDiaStackWalkHelper::pdataForVA
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Zwraca skojarzony z wirtualnym adresem bloku danych PDATA.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
HRESULT pdataForVA(   
   ULONGLONG  va,  
   DWORD      cbData,  
   DWORD*     pcbData,  
   BYTE*      pbData  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `va`  
 [in] Określa adres wirtualny danych w celu uzyskania.  
  
 `cbData`  
 [in] Rozmiar danych w bajtach, aby uzyskać.  
  
 `pcbData`  
 [out] Zwraca rzeczywisty rozmiar danych w bajtach, które zostały pobrane.  
  
 `pbData`  
 [out w] Bufor, który jest wypełniane żądanych danych. Nie może być `NULL`.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`. Zwraca `S_FALSE` przypadku nie PDATA dla określonego adresu. W przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 PDATA (sekcja o nazwie ".pdata") compiland — zawiera informacje dotyczące obsługi funkcji wyjątków.  
  
 Obiekt wywołujący wie, jak dużo danych jest zwracane, więc nie trzeba zadać, jak dużo danych jest dostępna na obiekt wywołujący. Dlatego jest dopuszczalne związanych z implementacją tę metodę, aby zwrócić błąd, jeśli `pbData` parametr `NULL`.  
  
## <a name="see-also"></a>Zobacz też  
 [IDiaStackWalkHelper](../../debugger/debug-interface-access/idiastackwalkhelper.md)



