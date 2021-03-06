---
title: Getwinfxpath — zadanie | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology: msbuild
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- getting the directory of the current .NET Framework runtime [WPF MSBuild]
- GetWinFXPath task [WPF MSBuild], parameters
- GetWinFXPath task [WPF MSBuild]
- obtaining the path to the current .NET Framework runtime [WPF MSBuild]
ms.assetid: b1dfb467-f3d3-47f3-83ef-af7b0e33a772
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: ace14a3238142be4d703b4d2e0fa457288b00458
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49852833"
---
# <a name="getwinfxpath-task"></a>Getwinfxpath — zadanie
<xref:Microsoft.Build.Tasks.Windows.GetWinFXPath> Zadanie zwraca katalogu bieżącego [!INCLUDE[TLA#tla_winfx](../msbuild/includes/tlasharptla_winfx_md.md)] środowiska uruchomieniowego.  
  
## <a name="task-parameters"></a>Parametry zadania  
  
| Parametr | Opis |
|-------------------| - |
| `WinFXPath` | Opcjonalnie **ciąg** parametr wyjściowy.<br /><br /> Określa ścieżkę rzeczywistych [!INCLUDE[TLA2#tla_winfx](../msbuild/includes/tla2sharptla_winfx_md.md)] środowiska uruchomieniowego. |
| `WinFXNativePath` | Wymagane **ciąg** parametru.<br /><br /> Określa ścieżkę do natywnych [!INCLUDE[TLA2#tla_titlewinfx](../msbuild/includes/tla2sharptla_titlewinfx_md.md)] środowiska uruchomieniowego. |
| `WinFXWowPath` | Wymagane **ciąg** parametru.<br /><br /> Określa ścieżkę do [!INCLUDE[TLA#tla_winfx](../msbuild/includes/tlasharptla_winfx_md.md)] zestawów w 32-bitowych **Windows na Windows** modułu w systemach 64-bitowych. |
  
## <a name="remarks"></a>Uwagi  
 Jeśli <xref:Microsoft.Build.Tasks.Windows.GetWinFXPath> zadanie jest wykonywane na 64-bitowy procesor, **WinFXPath** parametr ma wartość ścieżki, która jest przechowywana w **WinFXWowPath** parametru; w przeciwnym razie **WinFXPath**  parametr ma wartość ścieżki, która jest przechowywana w **WinFXNativePath** parametru.  
  
## <a name="example"></a>Przykład  
 Poniższy przykład pokazuje, jak używać **getwinfxpath —** zadanie, aby wykryć ścieżką natywną do [!INCLUDE[TLA2#tla_titlewinfx](../msbuild/includes/tla2sharptla_titlewinfx_md.md)] środowiska uruchomieniowego.  
  
```xml  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  <UsingTask   
    TaskName="Microsoft.Build.Tasks.Windows.GetWinFXPath"   
    AssemblyFile="C:\Program Files\Reference Assemblies\Microsoft\Framework\v3.0\PresentationBuildTasks.dll" />  
  <Target Name="GetWinFXPathTask">  
    <GetWinFXPath  
      WinFXNativePath="c:\WinFXNative"   
      WinFXWowPath="c:\WinFXWowNative" />  
  </Target>  
  <Import Project="$(MSBuildBinPath)\Microsoft.WinFX.targets" />  
</Project>  
```  
  
## <a name="see-also"></a>Zobacz także  
 [Odwołanie do WPF MSBuild](../msbuild/wpf-msbuild-reference.md)   
 [Odwołanie do zadania](../msbuild/wpf-msbuild-task-reference.md)   
 [Odwołanie do narzędzia MSBuild](../msbuild/msbuild-reference.md)   
 [Odwołanie do zadania](../msbuild/msbuild-task-reference.md)   
 [Tworzenie aplikacji WPF (WPF)](/dotnet/framework/wpf/app-development/building-a-wpf-application-wpf)