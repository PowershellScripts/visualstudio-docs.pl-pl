---
title: IEEDataStorage::GetSize | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IEEDataStorage::GetSize
helpviewer_keywords:
- IEEDataStorage::GetSize
ms.assetid: 33d232c4-1239-4abc-922b-e1bc5b908169
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: f9ac01907015a58681ee5cacb5b5ae38d32c2896
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49820645"
---
# <a name="ieedatastoragegetsize"></a>IEEDataStorage::GetSize
Zwraca liczbę bajtów zawartych w tym obiekcie.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT GetSize(  
   ULONG* size  
);  
```  
  
```csharp  
int GetSize(  
   out uint size  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `size`  
 [out] Liczba bajtów zawartych w tym obiekcie.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Użyj [GetData](../../../extensibility/debugger/reference/ieedatastorage-getdata.md) metodę, która pobierze bajtów rzeczywistych danych.  
  
## <a name="see-also"></a>Zobacz też  
 [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md)   
 [GetData](../../../extensibility/debugger/reference/ieedatastorage-getdata.md)