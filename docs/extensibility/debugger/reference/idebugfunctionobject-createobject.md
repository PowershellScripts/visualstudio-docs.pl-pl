---
title: IDebugFunctionObject::CreateObject | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugFunctionObject::CreateObject
helpviewer_keywords:
- IDebugFunctionObject::CreateObject method
ms.assetid: c4c99dd5-609a-4e7c-8f29-eb728f57e995
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: d0af1607d8352b158c28248fc4bd85ed0fbaf7b3
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49908644"
---
# <a name="idebugfunctionobjectcreateobject"></a>IDebugFunctionObject::CreateObject
Tworzy obiekt przy użyciu konstruktora.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT CreateObject(   
   IDebugFunctionObject* pConstructor,  
   DWORD                 dwArgs,  
   IDebugObject*         pArgs[],  
   IDebugObject**        ppObject  
);  
```  
  
```csharp  
int CreateObject(  
   IDebugFunctionObject pConstructor,   
   uint                 dwArgs,   
   IDebugObject[]       pArgs,   
   out IDebugObject     ppObject  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pConstructor`  
 [in] [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md) obiekt reprezentujący konstruktora obiektu, który ma zostać utworzony.  
  
 `dwArgs`  
 [in] Liczba parametrów w `pArg` tablicy. Reprezentuje liczbę parametrów przekazanych do konstruktora.  
  
 `pArg`  
 [in] Tablica [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) obiekty reprezentujące parametry przekazywane do konstruktora.  
  
 `ppObject`  
 [out] Zwraca `IDebugObject` reprezentujący nowo utworzony obiekt.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca wartość S_OK; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Wywołaj tę metodę, aby utworzyć obiekt, który reprezentuje wystąpienie klasy (lub inne typ złożony, który wymaga konstruktora) oznacza to parametr do funkcji, która jest reprezentowana przez [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md) interfejsu.  
  
 Jeśli parametr obiektu, nie wymaga konstruktora, wywołaj [CreateObjectNoConstructor](../../../extensibility/debugger/reference/idebugfunctionobject-createobjectnoconstructor.md) metody.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md)   
 [CreateObjectNoConstructor](../../../extensibility/debugger/reference/idebugfunctionobject-createobjectnoconstructor.md)