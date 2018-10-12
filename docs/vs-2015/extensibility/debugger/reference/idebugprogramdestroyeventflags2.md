---
title: IDebugProgramDestroyEventFlags2 | Dokumentacja firmy Microsoft
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
- IDebugProgramDestroyEventFlags2 interface
ms.assetid: d384ff71-dc71-40b9-a871-801f8b6a3418
caps.latest.revision: 8
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 9afc8a810468733661abb2a71e609e3cbe303d51
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49223616"
---
# <a name="idebugprogramdestroyeventflags2"></a>IDebugProgramDestroyEventFlags2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Umożliwia to aparat debugowania zastąpić domyślne zachowanie [!INCLUDE[vsprvs](../../../includes/vsprvs-md.md)] interfejsu użytkownika podczas kończenia sesji debugowania.  
  
## <a name="syntax"></a>Składnia  
  
```  
IDebugProgramDestroyEventFlags2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uwagi dotyczące implementacji  
 Ten interfejs jest implementowany przez aparaty debugowania. Jest to przydatne dla hostów, które mogą tworzyć i zniszcz wielu programów w okresie istnienia procesu.  
  
## <a name="methods"></a>Metody  
 W poniższej tabeli przedstawiono metody `IDebugProgramDestroyEventFlags2`.  
  
|Metoda|Opis|  
|------------|-----------------|  
|[GetFlags](../../../extensibility/debugger/reference/idebugprogramdestroyeventflags2-getflags.md)|Pobiera program zniszczyć flag.|  
  
## <a name="remarks"></a>Uwagi  
 Domyślne zachowanie [!INCLUDE[vsprvs](../../../includes/vsprvs-md.md)] interfejsu użytkownika, to aby powrócić do trybu projektowania po wszystkich programów wysłały program Zdarzenie niszczenia. Ten interfejs umożliwia aparat debugowania zmienić to zachowanie.  
  
## <a name="requirements"></a>Wymagania  
 Nagłówek: Msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll

