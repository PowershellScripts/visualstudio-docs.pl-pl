---
title: IDebugProgramDestroyEventFlags2 | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: IDebugProgramDestroyEventFlags2 interface
ms.assetid: d384ff71-dc71-40b9-a871-801f8b6a3418
caps.latest.revision: "7"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: bee4fe04f22bd9afbff8e2d26ef9d699b0226241
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="idebugprogramdestroyeventflags2"></a>IDebugProgramDestroyEventFlags2
Umożliwia to aparat debugowania zastąpić domyślne zachowanie [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] interfejsu użytkownika podczas kończenia sesji debugowania.  
  
## <a name="syntax"></a>Składnia  
  
```  
IDebugProgramDestroyEventFlags2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uwagi dotyczące implementacji  
 Ten interfejs jest implementowany przez aparaty debugowania. Jest to przydatne w przypadku hostów, które może utworzyć i zniszcz wiele programów w okresie istnienia procesu.  
  
## <a name="methods"></a>Metody  
 W poniższej tabeli przedstawiono metody `IDebugProgramDestroyEventFlags2`.  
  
|Metoda|Opis|  
|------------|-----------------|  
|[GetFlags](../../../extensibility/debugger/reference/idebugprogramdestroyeventflags2-getflags.md)|Pobiera program zniszczyć flagi.|  
  
## <a name="remarks"></a>Uwagi  
 Domyślne zachowanie [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] interfejsu użytkownika jest konieczność powrotu do trybu projektowania po wszystkie programy zostały wysłane programu zniszczyć zdarzeń. Ten interfejs umożliwia aparat debugowania zmienić to zachowanie.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: Msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Zestaw: Microsoft.VisualStudio.Debugger.Interop.dll