---
title: IDebugFunctionObject::CreateObject | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugFunctionObject::CreateObject
helpviewer_keywords: IDebugFunctionObject::CreateObject method
ms.assetid: c4c99dd5-609a-4e7c-8f29-eb728f57e995
caps.latest.revision: "9"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 9ba06089624a585688f481719b2ce51397653cd1
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
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
 [in] [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md) obiekt reprezentujący Konstruktor obiektu, który ma zostać utworzony.  
  
 `dwArgs`  
 [in] Liczba parametrów w `pArg` tablicy. Przedstawia liczbę parametrów przekazanych do konstruktora.  
  
 `pArg`  
 [in] Tablica [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) obiekty reprezentujące parametry przekazany do konstruktora.  
  
 `ppObject`  
 [out] Zwraca `IDebugObject` reprezentujący nowo utworzony obiekt.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca wartość S_OK; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Wywołanie tej metody, aby utworzyć obiekt, który reprezentuje wystąpienie klasy (lub inne typ złożony, który wymaga konstruktora) czyli parametr do funkcji, która jest reprezentowana przez [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md) interfejsu.  
  
 Jeśli parametr obiektu nie wymaga konstruktora, wywołanie [CreateObjectNoConstructor](../../../extensibility/debugger/reference/idebugfunctionobject-createobjectnoconstructor.md) metody.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md)   
 [CreateObjectNoConstructor](../../../extensibility/debugger/reference/idebugfunctionobject-createobjectnoconstructor.md)