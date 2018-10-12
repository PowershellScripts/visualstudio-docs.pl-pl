---
title: IDebugPortRequest2::GetPortName | Dokumentacja firmy Microsoft
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
- IDebugPortRequest2::GetPortName
helpviewer_keywords:
- IDebugPortRequest2::GetPortName
ms.assetid: 53e2a3a4-bb34-4a02-a983-6bd84ea70587
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 11097133a3f37058e71ed81a1dd73b71480f27e0
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49185448"
---
# <a name="idebugportrequest2getportname"></a>IDebugPortRequest2::GetPortName
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Pobiera nazwę portu.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
HRESULT GetPortName(   
   BSTR* pbstrPortName  
);  
```  
  
```csharp  
int GetPortName(   
   out string pbstrPortName  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pbstrPortName`  
 [out] Zwraca nazwę portu.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 [IDebugPortRequest2](../../../extensibility/debugger/reference/idebugportrequest2.md) interfejsu jest zwykle przekazywany z pakietu debugowania (klienta) do dostawcy portu (serwera), można uzyskać połączenia do portu. Zarówno pakietu debugowania, jak i dostawcy portu sobie sprawę z możliwych opcji dla portu. Jeśli prosty ciąg opisujący portu, a następnie `IDebugPortRequest2::GetPortName` metoda ma za mało informacji do nawiązania połączenia. W przeciwnym razie można podać dodatkowe interfejsy przez klienta, który można uzyskać za pomocą serwera `IDebugPortRequest2::QueryInterface`.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugPortRequest2](../../../extensibility/debugger/reference/idebugportrequest2.md)

