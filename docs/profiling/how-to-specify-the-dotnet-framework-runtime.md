---
title: 'Porady: Określanie środowiska wykonawczego .NET Framework | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- Profiling Tools, .NET Framework versions
- .NET Framework versions,profililng
ms.assetid: d39f3579-719a-4f47-a97d-5b4232fe4c64
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: e85e1c571ecb900d5ce7ffdecf8e85b8c367de5c
ms.sourcegitcommit: ce154aee5b403d5c1c41da42302b896ad3cf8d82
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/07/2018
ms.locfileid: "34844137"
---
# <a name="how-to-specify-the-net-framework-runtime"></a>Porady: Określanie środowiska uruchomieniowego .NET Framework

Wraz z wydaniem [!INCLUDE[net_v40_long](../code-quality/includes/net_v40_long_md.md)], aplikacje mogą być składane modułów, które zostały utworzone przy użyciu różnych wersji [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] środowiska wykonawczego. Domyślnie program Visual Studio Profiling Tools profilu pierwszy środowiska uruchomieniowego, który jest ładowany przez aplikację. Można określić czasu wykonywania do profilowania podczas uruchamiania aplikacji z profilerem i dołączanie profilera do aplikacji już uruchomione.

## <a name="to-specify-the-net-framework-run-time-to-profile-when-starting-an-application-with-the-profiler"></a>Aby określić środowiska wykonawczego .NET Framework do profilu, podczas uruchamiania aplikacji przy użyciu profilera

1. W **Eksplorator wydajności**, kliknij prawym przyciskiem myszy sesję wydajności, kliknij przycisk **właściwości**, a następnie kliknij przycisk **zaawansowane**.

     **Docelowa wersja środowiska CLR** liście wyświetlane są **automatyczne** i wersje [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] środowisko uruchomieniowe, które są zainstalowane na komputerze.

2. Wykonaj jedną z następujących czynności:

    - Kliknij wersję środowiska CLR, który ma zostać profilu.

    - Kliknij przycisk **automatyczne** do profilowania pierwszej wersji, który jest ładowany przez aplikację.

## <a name="to-specify-the-net-framework-run-time-to-profile-when-attaching-the-profiler-to-an-application"></a>Aby określić środowiska wykonawczego .NET Framework do profilu, kiedy dołączanie profilera do aplikacji

1. Na **Analizuj** menu wskaż **profilera**, następnie kliknij przycisk **Attach/Detach**.

2. Na **Dołącz Profiler do procesu** okna dialogowego kliknij proces, który ma być profilu.

     **Docelowa wersja środowiska CLR** pole listy s **automatyczne** i wersje [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] środowisko uruchomieniowe, które są zainstalowane na komputerze.

3. Wykonaj jedną z następujących czynności:

    - Kliknij wersję środowiska CLR, który ma zostać profilu.

    - Kliknij przycisk **automatyczne** do profilowania wersji, który jest ładowany podczas dołączenie profilera do aplikacji.