---
title: IDebugModule3::LoadSymbols | Dokumentacja firmy Microsoft
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
- IDebugModule3::LoadSymbols
helpviewer_keywords:
- IDebugModule3::LoadSymbols
ms.assetid: 7548c8c1-cbc6-48aa-a845-19058d4a85bb
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 1c9eb4a3ec14b2af59ba5fb8a9983a97bd980a6e
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49257039"
---
# <a name="idebugmodule3loadsymbols"></a>IDebugModule3::LoadSymbols
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Ładuje symbole dla bieżącego modułu.  
  
## <a name="syntax"></a>Składnia  
  
```cpp#  
HRESULT LoadSymbols(  
   void  
);  
```  
  
```csharp  
int LoadSymbols();  
```  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli metoda się powiedzie, zwraca `S_OK`. Jeśli nie powiedzie się, zwraca kod błędu.  
  
## <a name="remarks"></a>Uwagi  
 Ta metoda ładuje symbole z bieżącą ścieżkę wyszukiwania (może być zmienione przez wywołanie metody [SetSymbolPath](../../../extensibility/debugger/reference/idebugengine3-setsymbolpath.md) metody).  
  
 Ta metoda jest preferowana nad [ReloadSymbols_Deprecated](../../../extensibility/debugger/reference/idebugmodule2-reloadsymbols-deprecated.md) metody.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugModule3](../../../extensibility/debugger/reference/idebugmodule3.md)   
 [SetSymbolPath](../../../extensibility/debugger/reference/idebugengine3-setsymbolpath.md)

