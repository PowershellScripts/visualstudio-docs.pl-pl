---
title: IPropertyProxyEESide::CreateReplacementObject | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IPropertyProxyEESide::CreateReplacementObject
helpviewer_keywords: IPropertyProxyEESide::CreateReplacementObject
ms.assetid: 0cfe79b8-c3f1-48b0-a225-e39dee2c92fe
caps.latest.revision: "11"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 0f0202f017004e69f356b31299f0ed28b55348aa
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="ipropertyproxyeesidecreatereplacementobject"></a>IPropertyProxyEESide::CreateReplacementObject
Tworzy kopię obiektu danych specyficznych dla ewaluatora wyrażenia (EE).  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT CreateReplacementObject(  
   IEEDataStorage*  dataIn,  
   IEEDataStorage** dataOut  
);  
```  
  
```csharp  
int CreateReplacementObject(  
   IEEDataStorage     dataIn,  
   out IEEDataStorage dataOut  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `dataIn`  
 [in] [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md) obiekt zawierający dane do skopiowania.  
  
 `dataOut`  
 [out] Zwraca nowy `IEEDataStorage` obiektu.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Ta metoda jest podana [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md) obiekt reprezentujący tablicę bajtów. Ten obiekt przychodzących danych zwykle nie jest zaimplementowana przez EE. Jednak obiektu zwróconego przez tę metodę zawsze jest implementowany przez EE, który umożliwia wdrożenie EE `IEEDataStorage` interfejs na potrzeby niezależnie od klasy.  
  
 Należy pamiętać, że dane dostarczone przez przychodzący `IEEDataStorage` obiekt musi być tych samych danych w wychodzącej `IEEDataStorage` obiektu.  
  
## <a name="see-also"></a>Zobacz też  
 [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md)   
 [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md)