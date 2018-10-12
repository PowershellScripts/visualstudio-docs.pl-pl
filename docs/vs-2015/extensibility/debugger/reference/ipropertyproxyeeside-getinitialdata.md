---
title: IPropertyProxyEESide::GetInitialData | Dokumentacja firmy Microsoft
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
- IPropertyProxyEESide::GetInitialData
helpviewer_keywords:
- IPropertyProxyEESide::GetInitialData
ms.assetid: 36cceb19-2604-4ef9-b42b-5dd30cbe24b1
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 654d971ca09ff0a4a69e476810077a43035dfae2
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49209875"
---
# <a name="ipropertyproxyeesidegetinitialdata"></a>IPropertyProxyEESide::GetInitialData
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Zwraca dane początkowe dla tego obiektu.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
HRESULT GetInitialData(  
   IEEDataStorage** dataOut  
);  
```  
  
```csharp  
int GetInitialData(  
   out IEEDataStorage dataOut  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `dataOut`  
 [out] Zwraca [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md) obiekt zawierający dane pierwotne tego obiektu.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="see-also"></a>Zobacz też  
 [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md)   
 [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md)

