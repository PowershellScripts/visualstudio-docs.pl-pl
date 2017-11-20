---
title: "Odwołanie do zadania MSBuild WPF | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- WPF MSBuild task reference [WPF MSBuild], term/definition table
- build tasks [WPF MSBuild], Microsoft build engine
- build tasks using the Microsoft build engine [WPF MSBuild], compile markup and process resources
- WPF MSBuild task reference [WPF MSBuild]
ms.assetid: 96df0370-e50f-4ffc-9771-b12fb8721143
caps.latest.revision: "4"
author: kempb
ms.author: kempb
manager: ghogen
ms.openlocfilehash: bdf6da409d3b7e87e95c8eb08f6ce730e3c1b1cc
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="wpf-msbuild-task-reference"></a>Odwołanie do zadania WPF MSBuild
Proces kompilacji systemu Windows Presentation Foundation (WPF) rozszerza Microsoft build engine (MSBuild) za sprawą dodatkowego zestawu zadania kompilacji, w tym na kompilowanie zakładek i zasobów procesowych zadań.  
  
## <a name="in-this-section"></a>W tej sekcji  
 [Fileclassifier —](../msbuild/fileclassifier-task.md)  
 Klasyfikuje zestaw zasobów źródła jako te, które zostaną osadzone w zestawie. Jeśli zasób nie jest Lokalizowalny, jest osadzony w zestawie aplikacji głównej; w przeciwnym razie jest osadzony w zestawie satelickim.  
  
 [Generatetemporarytargetassembly —](../msbuild/generatetemporarytargetassembly-task.md)  
 Generuje zestawu, jeśli co najmniej jeden [!INCLUDE[TLA#tla_xaml](../msbuild/includes/tlasharptla_xaml_md.md)] strony w projekcie odwołuje się do typu, która jest zadeklarowana jako lokalnie w tym projekcie. Wygenerowanym zestawie zostaną usunięte po ukończeniu procesu kompilacji, czy Proces kompilacji nie powiedzie się.  
  
 [Getwinfxpath —](../msbuild/getwinfxpath-task.md)  
 Zwraca katalogu bieżącego [!INCLUDE[TLA#tla_winfx](../msbuild/includes/tlasharptla_winfx_md.md)] środowiska wykonawczego.  
  
 [Markupcompilepass1 —](../msbuild/markupcompilepass1-task.md)  
 Konwertuje niemożliwe do zlokalizowania [!INCLUDE[TLA#tla_xaml](../msbuild/includes/tlasharptla_xaml_md.md)] pliki na skompilowany format binarny projektu.  
  
 [Markupcompilepass2 —](../msbuild/markupcompilepass2-task.md)  
 Wykonuje oznaczenia w drugim przebiegu kompilacji na [!INCLUDE[TLA#tla_xaml](../msbuild/includes/tlasharptla_xaml_md.md)] pliki, które odwołują się do typów w tym samym projekcie.  
  
 [Mergelocalizationdirectives —](../msbuild/mergelocalizationdirectives-task.md)  
 Scala atrybuty lokalizacji i komentarze co najmniej jednego [!INCLUDE[TLA2#tla_xaml](../msbuild/includes/tla2sharptla_xaml_md.md)] plików binarnych w jednym pliku dla całego zestawu.  
  
 [Resourcesgenerator —](../msbuild/resourcesgenerator-task.md)  
 Osadza co najmniej jeden zasób (.ico jpg, bmp, [!INCLUDE[TLA2#tla_xaml](../msbuild/includes/tla2sharptla_xaml_md.md)] w formacie binarnym, a inne typy rozszerzeń) w plik .resources.  
  
 [Uidmanager —](../msbuild/uidmanager-task.md)  
 Sprawdza, aktualizuje lub usuwa unikatowe identyfikatory (UID), aby zlokalizować wszystkie [!INCLUDE[TLA#tla_xaml](../msbuild/includes/tlasharptla_xaml_md.md)] elementów zawartych w źródle [!INCLUDE[TLA2#tla_xaml](../msbuild/includes/tla2sharptla_xaml_md.md)] plików.  
  
 [Updatemanifestforbrowserapplication —](../msbuild/updatemanifestforbrowserapplication-task.md)  
 Dodaje  **\<hostinbrowser — / >** element do manifestu aplikacji (*projectname*. exe.manifest) podczas [!INCLUDE[TLA#tla_xbap](../msbuild/includes/tlasharptla_xbap_md.md)] skompilować projekt.  
  
## <a name="see-also"></a>Zobacz też  
 [MSBuild](../msbuild/msbuild.md)