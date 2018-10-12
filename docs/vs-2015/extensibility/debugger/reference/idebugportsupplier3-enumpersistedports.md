---
title: IDebugPortSupplier3::EnumPersistedPorts | Dokumentacja firmy Microsoft
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
- IDebugPortSupplier3::EnumPersistedPorts
helpviewer_keywords:
- IDebugPortSupplier3::EnumPersistedPorts
ms.assetid: 1c3dead3-5d6c-4067-8418-4015f0b0dd07
caps.latest.revision: 13
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: d77f11665fdca0b3fa75cbf93c9ab28c76f5044d
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49210739"
---
# <a name="idebugportsupplier3enumpersistedports"></a>IDebugPortSupplier3::EnumPersistedPorts
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Ta metoda pobiera obiekt, który umożliwia wyliczenie listę portów utrwalonych.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT EnumPersistedPorts(  
   BSTR_ARRAY         PortNames,  
   IEnumDebugPorts2** ppEnum  
);  
```  
  
```csharp  
int EnumPersistedPorts(  
   BSTR_ARRAY           PortNames,  
   out IEnumDebugPorts2 ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `PortNames`  
 [in] A [BSTR_ARRAY](../../../extensibility/debugger/reference/bstr-array.md) strukturę, która zawiera listę nazw portu odnajdujący i zwracający między utrwalonych portów. Zostaną zwrócone tylko tych utrwalonych portów przy użyciu tych nazw.  
  
 `ppEnum`  
 [out] Obiekt, który implementuje [IEnumDebugPorts2](../../../extensibility/debugger/reference/ienumdebugports2.md) interfejsu.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Utrwalonych porty są ładowane, gdy dostawcy portu jest tworzone i zapisywane, kiedy niszczony jest dostawcy portu.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugPortSupplier3](../../../extensibility/debugger/reference/idebugportsupplier3.md)   
 [IEnumDebugPorts2](../../../extensibility/debugger/reference/ienumdebugports2.md)   
 [BSTR_ARRAY](../../../extensibility/debugger/reference/bstr-array.md)

