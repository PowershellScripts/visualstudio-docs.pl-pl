---
title: IDebugPendingBreakpoint2::Virtualize | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- IDebugPendingBreakpoint2::Virtualize
helpviewer_keywords:
- Virtualize method
- IDebugPendingBreakpoint2::Virtualize method
ms.assetid: 58c8e9a5-4494-47c2-bddb-56f628da6a2d
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: eb2e66378b2a7b906b6bf9e0efe4e718316ade54
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49948294"
---
# <a name="idebugpendingbreakpoint2virtualize"></a>IDebugPendingBreakpoint2::Virtualize
Włącza/wyłącza zwirtualizowane stan to oczekujące punktu przerwania. Jeśli oczekujący punkt przerwania zostaje zwirtualizowany, aparat debugowania będzie podejmować próby powiązać go za każdym razem, gdy nowy kod ładuje się do programu.  
  
## <a name="syntax"></a>Składnia  
  
```cpp  
HRESULT Virtualize(   
   BOOL fVirtualize  
);  
```  
  
```cpp  
int Virtualize(   
   int fVirtualize  
);  
```  
  
#### <a name="parameters"></a>Parametry  
 `fVirtualize`  
 [in] Ustaw na wartość różną od zera (`TRUE`) do wirtualizacji oczekujący punkt przerwania lub równą zero (`FALSE`) Aby wyłączyć wirtualizacji.  
  
## <a name="return-value"></a>Wartość zwracana  
 Jeśli operacja się powiedzie, zwraca `S_OK`; w przeciwnym razie zwraca kod błędu. Zwraca `E_BP_DELETED` Jeśli punkt przerwania został usunięty.  
  
## <a name="remarks"></a>Uwagi  
 Zwirtualizowane punkt przerwania jest powiązany za każdym razem, gdy kod jest ładowany.  
  
## <a name="example"></a>Przykład  
 Poniższy przykład pokazuje, jak zaimplementować tę metodę dla prostego `CPendingBreakpoint` obiekt ujawniający [IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md) interfejsu.  
  
```cpp  
HRESULT CPendingBreakpoint::Virtualize(BOOL fVirtualize)    
{    
   HRESULT hr;    
  
   // Verify that the pending breakpoint has not been deleted. If deleted,   
   // then return hr = E_BP_DELETED.    
   if (m_state.state != PBPS_DELETED)    
   {    
      if (fVirtualize)    
      {    
         // Set the PBPSF_VIRTUALIZED flag in the PENDING_BP_STATE_FLAGS   
         // structure.    
         SetFlag(m_state.flags, PBPSF_VIRTUALIZED);    
      }    
      else    
      {    
         // Clear the PBPSF_VIRTUALIZED flag in the PENDING_BP_STATE_FLAGS   
         // structure.    
         ClearFlag(m_state.flags, PBPSF_VIRTUALIZED);    
      }    
      hr = S_OK;    
   }    
   else    
   {    
      hr = E_BP_DELETED;    
   }    
  
   return hr;    
}    
```  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md)