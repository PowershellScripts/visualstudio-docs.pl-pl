---
title: IDebugProviderProgramNode2::UnmarshalDebuggeeInterface | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugProviderProgramNode2::UnmarshalDebuggeeInterface
helpviewer_keywords: IDebugProviderProgramNode2::UnmarshalDebuggeeInterface
ms.assetid: 2e4653c5-10f1-493c-9973-f31d266c5d48
caps.latest.revision: "10"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: bb918c66e1b4b1b83a4919dd710f00c835f26045
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idebugproviderprogramnode2unmarshaldebuggeeinterface"></a>IDebugProviderProgramNode2::UnmarshalDebuggeeInterface
Pobiera określonego interfejsu przez granice procesu.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT UnmarshalDebuggeeInterface(  
   REFIID riid,  
   void** ppvObject  
);  
```  
  
```csharp  
int UnmarshalDebuggeeInterface(  
   ref Guid   riid,  
   out IntPtr ppvObject  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `riid`  
 [in] Identyfikator GUID interfejsu do uzyskania.  
  
 `ppvObject`  
 [out] Zwraca obiekt zawierający implementację żądanego interfejsu. [C++] to mogą być rzutowane bezpośrednio do typu żądanego interfejsu. C# użyj <xref:System.Runtime.InteropServices.Marshal.GetObjectForIUnknown%2A> metodę, aby uzyskać żądanego interfejsu.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli to się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Ta metoda jest używana, gdy aparat debugowania jest uruchomiony w [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] przestrzeni procesu i debugowany program działa w jego własnej przestrzeni procesu.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugProviderProgramNode2](../../../extensibility/debugger/reference/idebugproviderprogramnode2.md)