---
title: IDebugObject2::IsUserData | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugObject2::IsUserData
helpviewer_keywords:
- IDebugObject2::IsUserData method
ms.assetid: 6ffa0d0e-f742-496d-acc7-db74c248bc45
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 7fee6b88b33080221d619d40f797d0a976d5f495
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49849180"
---
# <a name="idebugobject2isuserdata"></a>IDebugObject2::IsUserData
Określa, czy obiekt reprezentuje dane użytkownika.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT IsUserData(  
   BOOL* pfUser  
);  
```  
  
```csharp  
int IsUserData(  
   out int pfUser  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pfUser`  
 [out] Zwraca wartość różną od zera (`TRUE`) obiekt reprezentuje dane użytkownika; wartość zero (`FALSE`) Jeśli nie jest.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca wartość S_OK; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Dane użytkownika są dowolnego obiektu, który jest częścią modułu wyznaczony jako JustMyCode (konfigurowanych przez użytkownika opcji oznaczający moduł jako kod użytkownika i dlatego są widoczne w śladzie stosu).  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugObject2](../../../extensibility/debugger/reference/idebugobject2.md)