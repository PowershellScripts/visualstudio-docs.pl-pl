---
title: IDebugExpressionEvaluator::SetLocale | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugExpressionEvaluator::SetLocale
helpviewer_keywords:
- IDebugExpressionEvaluator::SetLocale method
ms.assetid: d3d2027d-74e2-4ae6-bcc7-59d12f873b7c
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: f9c5e1fc300a150b15acc48f12dc3b8c6c01e277
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49882650"
---
# <a name="idebugexpressionevaluatorsetlocale"></a>IDebugExpressionEvaluator::SetLocale
Ta metoda określa język na potrzeby tworzenia drukowalnych wyników.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT SetLocale(   
   WORD wLangID  
);  
```  
  
```csharp  
int SetLocale(  
   ushort wLangID  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `wLangID`  
 [in] Identyfikator języka.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Ta metoda może zostać wywołana wiele razy, gdy Ewaluator wyrażeń (EE) jest załadowane, więc EE musi mieć możliwość przełączać języków na bieżąco. EE używa tych ustawień regionalnych, aby zwracać komunikaty o błędach i ciągi w odpowiednim języku.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugExpressionEvaluator](../../../extensibility/debugger/reference/idebugexpressionevaluator.md)