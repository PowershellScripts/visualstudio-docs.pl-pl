---
title: IDebugProcess2::EnumPrograms | Dokumentacja firmy Microsoft
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
- IDebugProcess2::EnumPrograms
helpviewer_keywords:
- IDebugProcess2::EnumPrograms
ms.assetid: f5b7295d-487d-464f-a4c6-d54175b07705
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 589a60b4eb484e8dc02ce4a8cf2765505fc7316a
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49232992"
---
# <a name="idebugprocess2enumprograms"></a>IDebugProcess2::EnumPrograms
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Pobiera listę wszystkich programów, które są zawarte w tym procesie.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
HRESULT EnumPrograms(   
   IEnumDebugPrograms2** ppEnum  
);  
```  
  
```csharp  
int EnumPrograms(   
   out IEnumDebugPrograms2 ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `ppEnum`  
 [out] Zwraca [IEnumDebugPrograms2](../../../extensibility/debugger/reference/ienumdebugprograms2.md) obiekt, który zawiera listę wszystkich programów w procesie.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)   
 [IEnumDebugPrograms2](../../../extensibility/debugger/reference/ienumdebugprograms2.md)

