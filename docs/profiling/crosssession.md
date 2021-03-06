---
title: CrossSession | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: b9fcb9c3-7903-478c-9b7c-dbd94092fcba
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 112983b543a602bca7105ad1b5b69c5995eadeb0
ms.sourcegitcommit: 6944ceb7193d410a2a913ecee6f40c6e87e8a54b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 09/05/2018
ms.locfileid: "43774622"
---
# <a name="crosssession"></a>CrossSession
*VSPerfCmd.exe* **CrossSession** opcja umożliwia profiler do zbierania danych z dowolnej sesji konsoli. **CrossSession** opcja musi być używany z **Start** opcji.  
  
 Można używać skrótu **CS** zamiast **CrossSession**.  
  
## <a name="syntax"></a>Składnia  
  
```cmd  
VSPerfCmd.exe /Start:Method /CrossSession [Options]  
```  
  
#### <a name="parameters"></a>Parametry  
 Brak  
  
## <a name="valid-options"></a>Prawidłowe opcje  
 Aby włączyć profilowanie w innej sesji **CrossSession** opcja musi być określona za pomocą **Start** opcji. **CrossSession** musi być także określona we wszystkich kolejnych **Dołącz narzędzia VSPerfCmd** i **Odłącz** poleceń.  
  
 **Początek:** `Method`  
 **Start** opcja inicjuje profiler do określonej metody profilowania.  
  
 **Dołącz:** _PID_[**,**_PID_]  
 Rozpoczyna się profilowanie określonych procesów.  
  
 **Odłącz**[**:**_PID_[,_PID_]]  
 Zatrzymuje profilowanie określonych procesów.  
  
## <a name="example"></a>Przykład  
 W tym przykładzie **CrossSession** opcja służy do dołączania do aplikacji, która została uruchomiona w innej sesji konsoli.  
  
```cmd  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp /CrossSession  
VSPerfCmd.exe /Attach:12345 /CS  
```  
  
## <a name="see-also"></a>Zobacz także  
 [Narzędzia VSPerfCmd](../profiling/vsperfcmd.md)   
 [Profil aplikacji autonomicznych](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [Aplikacje sieci web ASP.NET profilu](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Usługi profilowania](../profiling/command-line-profiling-of-services.md)