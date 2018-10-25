---
title: Interfejs IActiveScriptProfilerCallback2 | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IActiveScriptProfilerCallback2 interface
ms.assetid: 8f2e62e4-c232-4dc3-a2c0-54dd06298306
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6109e028dfc51a88314ce597a67847e95f7eaaed
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49815705"
---
# <a name="iactivescriptprofilercallback2-interface"></a>Interfejs IActiveScriptProfilerCallback2
Udostępnia metody, które są używane przez silnik wykonywania skryptów, aby powiadomić obiekt profiler, po wystąpieniu zdarzenia modelu DOM (Document Object). Ten interfejs jest implementowany przez obiekt profiler.  
  
## <a name="methods"></a>Metody  
  
|Metoda|Opis|  
|------------|-----------------|  
|[IActiveScriptProfilerCallback2::OnFunctionEnterByName](../../winscript/reference/iactivescriptprofilercallback2-onfunctionenterbyname.md)|Powiadamia obiekt profiler, który silnik wykonywania skryptów przechodzi do uruchomienia wywołania funkcji DOM w LICZBIE.|  
|[IActiveScriptProfilerCallback2::OnFunctionExitByName](../../winscript/reference/iactivescriptprofilercallback2-onfunctionexitbyname.md)|Powiadamia program profilujący, że obiekt, który aparat skryptów Zakończono DOM wywołania funkcji.|  
  
## <a name="remarks"></a>Uwagi  
 `IActiveScriptProfilerCallback2` Interfejsu najpierw wydane za pomocą programu Internet Explorer 9.  
  
 Powiadomienie o wywołania funkcji, które nie są wywołania do modelu DOM są dostarczane przez [interfejs IActiveScriptProfilerCallback](../../winscript/reference/iactivescriptprofilercallback-interface.md).  
  
> [!NOTE]
>  Dodanie możliwości do uruchamiania i zatrzymywania profilowania, gdy skrypt jest uruchamiany, wywołaj następujące metody. Korzystając z tych metod, można uzyskać pełny stos wywołań, jeśli [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)] jest uruchomiona, uruchomienie lub zatrzymanie profilowania.  
> 
> - Wywołaj [IActiveScriptProfilerControl2::CompleteProfilerStart](../../winscript/reference/iactivescriptprofilercontrol2-completeprofilerstart.md) powiadomić profiler rozpoczęto profilowanie.  
>   -   Wywołaj [IActiveScriptProfilerControl2::PrepareProfilerStop](../../winscript/reference/iactivescriptprofilercontrol2-prepareprofilerstop.md) powiadomić profiler zostanie wkrótce zatrzymania profilowania.  
  
## <a name="see-also"></a>Zobacz też  
 [Interfejsy profilera aktywnego skryptu](../../winscript/reference/active-script-profiler-interfaces.md)