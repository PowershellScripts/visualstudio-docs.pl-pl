---
title: IEEDataStorage::GetData | Dokumentacja firmy Microsoft
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
- IEEDataStorage::GetData
helpviewer_keywords:
- IEEDataStorage::GetData
ms.assetid: 4d384039-73d4-40b4-ace6-a2474c546397
caps.latest.revision: 8
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: be6b411ae5881dbcfcfc51de98d5b67cd57e8048
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49188134"
---
# <a name="ieedatastoragegetdata"></a>IEEDataStorage::GetData
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Pobiera określoną liczbę bajtów z obiektu.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
HRESULT GetData(  
   ULONG  dataSize,  
   ULONG* sizeGotten,  
   BYTE*  data  
);  
```  
  
```csharp  
int GetData(  
   uint     dataSize,  
   out uint sizeGotten,  
   byte[]   data  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `dataSize`  
 [in] Liczba bajtów do pobrania ( `data` tablicy musi posiadać co najmniej tej liczby bajtów).  
  
 `sizeGotten`  
 [out] Zwraca liczbę bajtów, które rzeczywiście zostały pobrane.  
  
 `data`  
 [out w] Tablica do wypełniona żądanych danych.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Zalecane użycie tej metody jest do pobrania wszystkich bajtów danych do lokalnej tablicy, ponieważ nie istnieje żaden sposób na pominięcie nad bajtów w procesie pobierania. W tym przypadku parametr `dataSize` powinien mieć wartość zwracana przez [getsize —](../../../extensibility/debugger/reference/ieedatastorage-getsize.md) metody.  
  
## <a name="see-also"></a>Zobacz też  
 [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md)   
 [GetSize](../../../extensibility/debugger/reference/ieedatastorage-getsize.md)

