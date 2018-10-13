---
title: Obliczanie wyrażenia w trybie przerwania | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- break mode, expression evaluation
- debugging [Debugging SDK], expression evaluation
- expression evaluation, break mode
ms.assetid: 34fe5b58-15d5-4387-a266-72120f90a4b6
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 03be07a19ac95eaec64fbdec73f92742c02ad191
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49239523"
---
# <a name="expression-evaluation-in-break-mode"></a>Ocena wyrażeń w trybie przerwania
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Poniżej opisano proces, który występuje, gdy debuger jest w trybie przerwania, a także musi przeprowadzić obliczenia wyrażenia.  
  
## <a name="expression-evaluation-process"></a>Proces oceny wyrażenia  
 Poniżej przedstawiono podstawowe etapy obliczenia wyrażenia:  
  
1.  Menedżer debugowania sesji (SDM) wywołuje [IDebugStackFrame2::GetExpressionContext](../../extensibility/debugger/reference/idebugstackframe2-getexpressioncontext.md) można uzyskać interfejsu kontekście wyrażenia [IDebugExpressionContext2](../../extensibility/debugger/reference/idebugexpressioncontext2.md).  
  
2.  Następnie wywołuje SDM [IDebugExpressionContext2::ParseText](../../extensibility/debugger/reference/idebugexpressioncontext2-parsetext.md) ciąg, który ma być analizowany.  
  
3.  Jeśli ParseText nie zwróci S_OK, zwracany jest przyczyną tego błędu.  
  
     — w przeciwnym-  
  
     Jeśli ParseText zwróci S_OK, SDM następnie wywołać albo [IDebugExpression2::EvaluateSync](../../extensibility/debugger/reference/idebugexpression2-evaluatesync.md) lub [IDebugExpression2::EvaluateAsync](../../extensibility/debugger/reference/idebugexpression2-evaluateasync.md) uzyskać końcowa wartość wyrażenia przeanalizowany.  
  
    -   W przypadku przy użyciu `IDebugExpression2::EvaluateSync`, interfejs danego wywołania zwrotnego jest używany do komunikacji ciągły proces oceny. Końcowa wartość jest zwracana w [IDebugProperty2](../../extensibility/debugger/reference/idebugproperty2.md) interfejsu.  
  
    -   W przypadku przy użyciu `IDebugExpression2::EvaluateAsync`, interfejs danego wywołania zwrotnego jest używany do komunikacji ciągły proces oceny. Po zakończeniu oceny EvaluateAsync wysyła [IDebugExpressionEvaluationCompleteEvent2](../../extensibility/debugger/reference/idebugexpressionevaluationcompleteevent2.md) interfejs za pomocą wywołania zwrotnego. Z tym interfejsem zdarzeń końcowa wartość można uzyskać za pomocą [GetResult](../../extensibility/debugger/reference/idebugexpressionevaluationcompleteevent2-getresult.md).  
  
## <a name="see-also"></a>Zobacz też  
 [Wywoływanie zdarzeń debugera](../../extensibility/debugger/calling-debugger-events.md)

