---
title: IDebugPortSupplier3 | Dokumentacja firmy Microsoft
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
- IDebugPortSupplier3
helpviewer_keywords:
- IDebugPortSupplier3 interface
ms.assetid: e458cd02-2370-4435-8953-17d7a60ce152
caps.latest.revision: 9
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: ae9b1911d92c8fe2e9a55b7737c37db44aa9d441
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49284417"
---
# <a name="idebugportsupplier3"></a>IDebugPortSupplier3
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Ten interfejs umożliwia obiekt wywołujący określić, czy dostawcy portu można zachować portów (zapisując je na dysku) między wywołań debugera, a następnie Pobierz listę portów zachowanych.  
  
## <a name="syntax"></a>Składnia  
  
```  
IDebugPortSupplier3 : IDebugPortSupplier2  
```  
  
## <a name="notes-for-implementers"></a>Uwagi dotyczące implementacji  
 Dostawcy niestandardowego portu implementuje ten interfejs obsługuje przechowywanie ani portu informacje są zapisywane na dysku. Ten interfejs musi zostać wdrożone na tym samym obiekcie jako [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md) interfejsu.  
  
## <a name="notes-for-callers"></a>Uwagi dotyczące wywoływania  
 Wywołaj [QueryInterface](http://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) na `IDebugPortSupplier2` interfejsu w celu uzyskania tego interfejsu.  
  
## <a name="methods-in-vtable-order"></a>Metody w Vtable kolejności  
 Oprócz metod odziedziczone [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md) interfejs, ten interfejs obsługuje następujące czynności:  
  
|Metoda|Opis|  
|------------|-----------------|  
|[CanPersistPorts](../../../extensibility/debugger/reference/idebugportsupplier3-canpersistports.md)|Zwraca, czy dostawca portu można utrwalić portów (zapisując je na dysku) między wywołań debugera.|  
|[EnumPersistedPorts](../../../extensibility/debugger/reference/idebugportsupplier3-enumpersistedports.md)|Zwraca obiekt, który może służyć do wyliczenia za pośrednictwem wszystkich portów, które były zapisywane na dysku przez dostawcę tego portu.|  
  
## <a name="remarks"></a>Uwagi  
 Jeśli dostawcy portu można utrwalić porty różnych wywołań, powinien implementować ten interfejs. Porty powinien być ładowany podczas dostawcy portu jest tworzone i zapisywane na dysku, kiedy niszczony jest dostawcy portu.  
  
 Aparat debugowania zazwyczaj nie wchodzi w interakcję z dostawcą portu, a także będą ma być używana dla tego interfejsu.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Zobacz też  
 [Interfejsy podstawowe](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md)

