---
title: IDebugEngine3 | Dokumentacja firmy Microsoft
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
- IDebugEngine3
helpviewer_keywords:
- IDebugEngine3 interface
ms.assetid: 8bdf4bb7-3b5d-4991-8981-772d4f6bb656
caps.latest.revision: 16
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: b316816c3e49d57cd4aa2d0229a00ad1e28173d0
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49222550"
---
# <a name="idebugengine3"></a>IDebugEngine3
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Reprezentuje aparat debugowania pojedynczego (DE), sterująca debugowanie jednego lub więcej modułów.  
  
## <a name="syntax"></a>Składnia  
  
```  
IDebugEngine3 : IDebugEngine2  
```  
  
## <a name="notes-for-implementers"></a>Uwagi dotyczące implementacji  
 Ten interfejs jest implementowany przez niestandardowe DE (jeśli ją obsługuje symbole) Aby włączyć stan JustMyCode. Ten interfejs muszą być zaimplementowane przez DE, jeśli obsługuje symboli i JustMyCode.  
  
## <a name="notes-for-callers"></a>Uwagi dotyczące wywoływania  
 Ten interfejs jest wywoływane przez Menedżer debugowania sesji (SDM) do przekazania na temat opcji użytkownika dla lokalizacji, z którego można załadować symboli. Jest również nazywany, aby ustawić identyfikator GUID aparatu, gdy zostanie uruchomiony (ten identyfikator GUID jest określane na podstawie od momentu rejestracji aparat). SDM wywołuje również tego interfejsu, aby ustawić stan JustMyCode oraz ustawić wszystkie wyjątki znane przez debuger do określonego stanu.  
  
## <a name="methods-in-vtable-order"></a>Metody w Vtable kolejności  
 Oprócz metod odziedziczone [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md), `IDebugEngine3` interfejsu udostępnia następujące metody.  
  
|Metoda|Opis|  
|------------|-----------------|  
|[SetSymbolPath](../../../extensibility/debugger/reference/idebugengine3-setsymbolpath.md)|Ustawia ścieżki lub ścieżek, które DE będzie używać do wyszukiwania symboli debugowania.|  
|[LoadSymbols](../../../extensibility/debugger/reference/idebugengine3-loadsymbols.md)|Ładuje symbole dla wszystkich modułów, których nie zainstalowano jeszcze symbole załadowane.|  
|[SetJustMyCodeState](../../../extensibility/debugger/reference/idebugengine3-setjustmycodestate.md)|Informuje DE o JustMyCode.|  
|[SetEngineGuid](../../../extensibility/debugger/reference/idebugengine3-setengineguid.md)|Określa identyfikator GUID DE od metryki.|  
|[SetAllExceptions](../../../extensibility/debugger/reference/idebugengine3-setallexceptions.md)|Ustaw wszystkie wyjątki jest aktualnie oczekujących do określonego stanu.|  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Zobacz też  
 [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)

