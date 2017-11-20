---
title: IDebugProcess2::GetAttachedSessionName | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: IDebugProcess2::GetAttachedSessionName
helpviewer_keywords: IDebugProcess2::GetAttachedSessionName
ms.assetid: 7e5e116f-2c0c-4bc8-ad3f-e9fd2318a7e4
caps.latest.revision: "13"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 553141f01211389308978e80d22220634625c940
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idebugprocess2getattachedsessionname"></a>IDebugProcess2::GetAttachedSessionName
Pobiera nazwę sesji, która jest debugowanie tego procesu. IDE można wyświetlić te informacje użytkownikowi, który jest debugowanie określonego procesu na określonym komputerze.  
  
> [!NOTE]
>  Ta metoda jest przestarzała i jej wdrożenia należy zawsze zwracają `E_NOTIMPL`.  
  
## <a name="syntax"></a>Składnia  
  
```  
HRESULT GetAttachedSessionName(  
   BSTR* pbstrSessionName  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `pbstrSessionName`  
  
## <a name="return-value"></a>Wartość zwracana  
 Ta metoda zawsze powinna zwrócić `E_NOTIMPL`.  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)