---
title: "Visual Studio Desktop Express 2017 obciążenia i składnik identyfikatorów | Dokumentacja firmy Microsoft"
description: "Użyj obciążenia i identyfikatory składników, aby zainstalować program Visual Studio przy użyciu wiersza polecenia lub określić jako zależności w manifeście VSIX"
keywords: 
author: TerryGLee
ms.author: tglee
manager: ghogen
ms.date: 10/09/2017
ms.topic: article
helpviewer_keywords:
- workload ID, Visual Studio
- component ID, Visual Studio
- install Visual Studio, administrator guide
ms.service: 
ms.technology:
- vs-ide-install
- vs-ide-sdk
ms.assetid: a3c0cc76-e3ce-435c-a1af-a6318b5a4dbe
ms.openlocfilehash: 7a69153f0df6ba6f7da19f5e2a0046209fffdaf6
ms.sourcegitcommit: 2c7f48ad6073a81fa927568793633f26cc1f0b15
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/17/2017
---
# <a name="visual-studio-desktop-express-2017-workload-and-component-ids"></a>Visual Studio Desktop Express 2017 obciążenia i składnik identyfikatorów

Tabele na tej stronie listy identyfikatorów, w której można zainstalować program Visual Studio przy użyciu wiersza polecenia lub można określić jako zależności w manifeście VSIX. Należy pamiętać, że będą dodawane dodatkowe składniki jako wydania aktualizacji dla programu Visual Studio.

Należy również zauważyć następujące informacje o stronie:

* Każde obciążenie ma osobny rozdział następuje identyfikator obciążenia i spisu składników, które są dostępne dla obciążeń.
* Domyślnie **wymagane** składników zostanie zainstalowany po zainstalowaniu obciążenie. Jeśli zostanie wybrana, można także zainstalować **zalecane** i **opcjonalnie** składników.
* Dodaliśmy również sekcja, która zawiera listę dodatkowych składników, które nie są powiązane z dowolnym obciążeniu.

Po ustawieniu zależności w manifeście VSIX, należy określić tylko identyfikatory składników. Użyj tabel na tej stronie, aby określić naszych zależności minimalna składnika. W niektórych scenariuszach może to oznaczać, że możesz określić tylko jeden składnik od obciążenia. W innych sytuacjach może oznaczać, możesz określić wiele składników z pojedyncze obciążenie lub wielu składników z wiele obciążeń. Aby uzyskać więcej informacji, zobacz [porady: Migracja projektów rozszerzalności programu Visual Studio 2017](../extensibility/how-to-migrate-extensibility-projects-to-visual-studio-2017.md) strony.

Aby uzyskać więcej informacji na temat używania tych identyfikatorów, zobacz [użyć parametrów wiersza polecenia do zainstalowania programu Visual Studio 2017](use-command-line-parameters-to-install-visual-studio.md) strony. Oraz listę obciążenia i identyfikatory składników dla innych produktów, zobacz [obciążenia 2017 r w usłudze Visual Studio i identyfikatory składników](workload-and-component-ids.md) strony.

## <a name="express-for-windows-desktop"></a>Express for Windows Desktop

**Identyfikator:** Microsoft.VisualStudio.Workload.WDExpress

**Opis:** tworzyć aplikacje natywne i zarządzane jak WPF, WinForms i Win32 kod obsługujący składni edycji kontroli kodu źródłowego, a elementu roboczego zarządzania. Obsługuje C#, Visual Basic i Visual C++.

### <a name="components-included-by-this-workload"></a>Składniki przez to obciążenie

Identyfikator składnika | Nazwa | Wersja | Typ zależności
--- | --- | --- | ---
Microsoft.Component.ClickOnce | Publikowanie ClickOnce | 15.0.26919.1 | Wymagane
Microsoft.Component.HelpViewer | Podgląd pomocy | 15.0.26711.1 | Wymagane
Microsoft.Component.MSBuild | MSBuild | 15.0.26208.0 | Wymagane
Microsoft.Component.VC.Runtime.OSSupport | Środowiska uruchomieniowego Visual C++ dla platformy uniwersalnej systemu Windows | 15.0.26621.2 | Wymagane
Microsoft.Net.Component.4.5.1.TargetingPack | Pakiet docelowy .NET framework 4.5.1 | 15.0.26621.2 | Wymagane
Microsoft.Net.Component.4.5.2.TargetingPack | Pakiet określania wartości docelowej platformy .NET framework 4.5.2 | 15.0.26621.2 | Wymagane
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 15.0.26621.2 | Wymagane
Microsoft.Net.Component.4.6.1.SDK | .NET framework 4.6.1 zestawu SDK | 15.0.26621.2 | Wymagane
Microsoft.Net.Component.4.6.1.TargetingPack | Pakiet określania wartości docelowej platformy .NET framework 4.6.1 | 15.0.26621.2 | Wymagane
Microsoft.Net.Component.4.6.TargetingPack | .NET framework 4.6 targeting pack | 15.0.26621.2 | Wymagane
Microsoft.Net.Component.4.TargetingPack | .NET framework 4 targeting pack | 15.0.26621.2 | Wymagane
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | Narzędzia do programowania .NET framework 4.6.1 | 15.0.26606.0 | Wymagane
Microsoft.Net.ComponentGroup.TargetingPacks.Common | Narzędzia deweloperskie programu .NET framework 4 — 4.6 | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.Common.Azure.Tools | Narzędzia łączności i publikowanie | 1.10.50614.2 | Wymagane
Microsoft.VisualStudio.Component.CoreEditor | Edytor podstawowe usługi Visual Studio | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.EntityFramework | Entity Framework 6 narzędzia | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.NuGet | Menedżer pakietów NuGet | 15.0.26621.2 | Wymagane
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilatory języka C# i Visual Basic Roslyn | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# i Visual Basic | 15.0.26711.1 | Wymagane
Microsoft.VisualStudio.Component.SQL.ADAL | Środowisko uruchomieniowe programu SQL ADAL | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.SQL.CLR | Typy danych CLR dla programu SQL Server | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.SQL.CMDUtils | Narzędzia wiersza polecenia programu SQL Server | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.SQL.DataSources | Obsługuje źródeł danych dla programu SQL Server | 15.0.26621.2 | Wymagane
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | Program SQL Server Express 2016 LocalDB | 15.0.26919.1 | Wymagane
Microsoft.VisualStudio.Component.SQL.NCLI | SQL Server Native Client | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Data Tools | 15.0.26906.1 | Wymagane
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Narzędzia do analizy statycznej | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.TextTemplating | Transformacji szablonu tekstowego | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.VC.CLI.Support | C + +/ CLI pomocy technicznej | 15.0.26823.1 | Wymagane
Microsoft.VisualStudio.Component.VC.Tools.ARM | Kompilatory w programie Visual C++ i bibliotek dla ARM | 15.0.26906.1 | Wymagane
Microsoft.VisualStudio.Component.VC.Tools.ARM64 | Kompilatory w programie Visual C++ i bibliotek dla ARM64 | 15.0.26906.1 | Wymagane
Microsoft.VisualStudio.Component.VisualStudioData | Źródła danych i odwołania do usług | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.Windows10SDK.14393 | Windows 10 SDK (10.0.14393.0) | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.Windows10SDK.16299.Desktop | Windows 10 SDK (10.0.16299.0) dla pulpitu C++ [x86 i x64] | 15.0.27004.2002 | Wymagane
Microsoft.VisualStudio.Component.Windows10SDK.16299.Desktop.arm | Windows 10 SDK (10.0.16299.0) dla pulpitu C++ [ARM i ARM64] | 15.0.27004.2002 | Wymagane
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP | Windows 10 SDK (10.0.16299.0) dla platformy uniwersalnej systemu Windows: C#, VB, JS | 15.0.27004.2002 | Wymagane
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP.Native | Windows 10 SDK (10.0.16299.0) dla platformy uniwersalnej systemu Windows: C++ | 15.0.27004.2002 | Wymagane

## <a name="unaffiliated-components"></a>Odłączony składników

Są to składniki, które nie są dołączone każde obciążenie, ale można wybrać jako poszczególnych składników.

Identyfikator składnika | Nazwa | Wersja
--- | --- | ---
n/d | n/d | n/d

## <a name="get-support"></a>Uzyskaj pomoc techniczną
Czasami może wystąpienia problemów. W przypadku niepowodzenia instalacji programu Visual Studio, zobacz [problemy dotyczące instalacji i uaktualniania Rozwiązywanie problemów z programu Visual Studio 2017](troubleshooting-installation-issues.md) stronę porady dotyczące rozwiązywania problemów. Jak również zgłosić problemy produktu z nami za pośrednictwem [zgłosić Problem](../ide/how-to-report-a-problem-with-visual-studio-2017.md) narzędzia w programie Visual Studio IDE lub udział sugestia z nami na [UserVoice](https://visualstudio.uservoice.com/forums/121579). Można śledzić problemy z produktu w [Visual Studio Developer Community](https://developercommunity.visualstudio.com/), zadawać pytania i odpowiedzi. Można również kontaktowaniu się z nami i innymi deweloperami Visual Studio za pomocą naszych [konwersacji programu Visual Studio w społeczności Gitter](https://gitter.im/Microsoft/VisualStudio) (wymaga [GitHub](https://github.com/) konta).

## <a name="see-also"></a>Zobacz także

* [Visual Studio obciążenia i składnik identyfikatorów](workload-and-component-ids.md)
* [Przewodnik administratora w usłudze Visual Studio](visual-studio-administrator-guide.md)
* [Korzystanie z parametrów wiersza polecenia do zainstalowania programu Visual Studio](use-command-line-parameters-to-install-visual-studio.md)
  * [Przykłady parametru wiersza polecenia](command-line-parameter-examples.md)
* [Tworzenie w trybie offline instalację programu Visual Studio](create-an-offline-installation-of-visual-studio.md)