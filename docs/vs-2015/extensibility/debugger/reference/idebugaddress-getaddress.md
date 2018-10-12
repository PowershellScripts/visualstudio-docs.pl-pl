---
title: IDebugAddress::GetAddress | Dokumentacja firmy Microsoft
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
- IDebugAddress::GetAddress
helpviewer_keywords:
- IDebugAddress:GetAddress method
ms.assetid: 2590387b-5d36-4116-9a75-737957b8898e
caps.latest.revision: 7
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: ddb3b6e3d8055dd9a5b6304cf57a355986706b0d
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49186767"
---
# <a name="idebugaddressgetaddress"></a>IDebugAddress::GetAddress
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Zwraca strukturę opisujący obiekt i jego lokalizację w jego zakres lub kontenera.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT GetAddress (  
   DEBUG_ADDRESS * pAddress  
);  
```  
  
```csharp  
int GetAddress(  
   DEBUG_ADDRESS[] pAddress  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pAddress`  
 [out w] A [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md) strukturę, która jest wypełniane przez tę metodę.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca wartość S_OK; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md) struktury jest przekazywany do tej metody, która wypełnia go przy użyciu odpowiednich informacji. Interpretacji tych informacji, zależy od rodzaju informacje zwrócone i symbol program obsługi. Zobacz [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md) Aby uzyskać więcej informacji.  
  
## <a name="see-also"></a>Zobacz też  
 [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md)

