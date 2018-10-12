---
title: IDebugExpressionContext2::GetName | Dokumentacja firmy Microsoft
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
- IDebugExpressionContext2::GetName
helpviewer_keywords:
- IDebugExpressionContext2::GetName
ms.assetid: c2b70d22-17af-4986-a7e3-930910367216
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 6f8caba6eaadb94dc51d0fe5c5bc71840fd5d865
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49215569"
---
# <a name="idebugexpressioncontext2getname"></a>IDebugExpressionContext2::GetName
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Pobiera nazwę kontekst oceny.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
HRESULT GetName(   
   BSTR* pbstrName  
);  
```  
  
```csharp  
int GetName(   
   out string pbstrName  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pbstrName`  
 [out] Zwraca nazwę kontekst oceny.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Nazwa jest opis tego kontekstu oceny. Zwykle jest coś, co może być analizowane przez ewaluatora wyrażeń, odwołujący się do tego kontekstu dokładną ocenę. Na przykład w języku C++ nazwa jest w następujący sposób:  
  
```  
"{ function-name, source-file-name, module-file-name }"  
```  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugExpressionContext2](../../../extensibility/debugger/reference/idebugexpressioncontext2.md)

