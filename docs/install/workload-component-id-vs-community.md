---
title: "Visual Studio Community 2017 obciążenia i składnik identyfikatorów | Dokumentacja firmy Microsoft"
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
ms.assetid: 58494fc3-12de-4761-bd4a-74b54f72bfb3
ms.openlocfilehash: 69b1e308f413e4e2abe28c646e9b1999cd1ffe4b
ms.sourcegitcommit: 2c7f48ad6073a81fa927568793633f26cc1f0b15
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/17/2017
---
# <a name="visual-studio-community-2017-workload-and-component-ids"></a>Visual Studio Community 2017 obciążenia i składnik identyfikatorów

Tabele na tej stronie listy identyfikatorów, w której można zainstalować program Visual Studio przy użyciu wiersza polecenia lub można określić jako zależności w manifeście VSIX. Należy pamiętać, że będą dodawane dodatkowe składniki jako wydania aktualizacji dla programu Visual Studio.

Należy również zauważyć następujące informacje o stronie:

* Każde obciążenie ma osobny rozdział następuje identyfikator obciążenia i spisu składników, które są dostępne dla obciążeń.
* Domyślnie **wymagane** składników zostanie zainstalowany po zainstalowaniu obciążenie. Jeśli zostanie wybrana, można także zainstalować **zalecane** i **opcjonalnie** składników.
* Dodaliśmy również sekcja, która zawiera listę dodatkowych składników, które nie są powiązane z dowolnym obciążeniu.

Po ustawieniu zależności w manifeście VSIX, należy określić tylko identyfikatory składników. Użyj tabel na tej stronie, aby określić naszych zależności minimalna składnika. W niektórych scenariuszach może to oznaczać, że możesz określić tylko jeden składnik od obciążenia. W innych sytuacjach może oznaczać, możesz określić wiele składników z pojedyncze obciążenie lub wielu składników z wiele obciążeń. Aby uzyskać więcej informacji, zobacz [porady: Migracja projektów rozszerzalności programu Visual Studio 2017](../extensibility/how-to-migrate-extensibility-projects-to-visual-studio-2017.md) strony.

Aby uzyskać więcej informacji na temat używania tych identyfikatorów, zobacz [użyć parametrów wiersza polecenia do zainstalowania programu Visual Studio 2017](use-command-line-parameters-to-install-visual-studio.md) strony. Oraz listę obciążenia i identyfikatory składników dla innych produktów, zobacz [obciążenia 2017 r w usłudze Visual Studio i identyfikatory składników](workload-and-component-ids.md) strony.

## <a name="visual-studio-core-editor-included-with-visual-studio-community-2017"></a>Visual Studio core edytora (dołączony do programu Visual Studio Community 2017)

**Identyfikator:** Microsoft.VisualStudio.Workload.CoreEditor

**Opis:** środowisko powłoki core Visual Studio, w tym kod obsługujący składni edycji, kontroli kodu źródłowego i elementu roboczego zarządzania.

### <a name="components-included-by-this-workload"></a>Składniki przez to obciążenie

Identyfikator składnika | Nazwa | Wersja | Typ zależności
--- | --- | --- | ---
Microsoft.VisualStudio.Component.CoreEditor | Edytor podstawowe usługi Visual Studio | 15.0.26606.0 | Wymagane


## <a name="azure-development"></a>Programowanie Azure

**Identyfikator:** Microsoft.VisualStudio.Workload.Azure

**Opis:** Azure SDK, narzędzia i projekty do tworzenia usług w chmurze, aplikacji i tworzenie zasobów.

### <a name="components-included-by-this-workload"></a>Składniki przez to obciążenie

Identyfikator składnika | Nazwa | Wersja | Typ zależności
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Usługi językowe razor | 15.0.26720.2 | Wymagane
Component.Microsoft.VisualStudio.Web.AzureFunctions | Narzędzia zadań Webjob platformy Microsoft Azure | 15.0.26720.2 | Wymagane
Component.WebSocket | WebSocket4Net | 15.0.26606.0 | Wymagane
Microsoft.Component.ClickOnce | Publikowanie ClickOnce | 15.0.26919.1 | Wymagane
Microsoft.Component.MSBuild | MSBuild | 15.0.26208.0 | Wymagane
Microsoft.Component.NetFX.Core.Runtime | Środowisko uruchomieniowe .NET core | 15.0.26208.0 | Wymagane
Microsoft.Net.Component.4.5.1.TargetingPack | Pakiet docelowy .NET framework 4.5.1 | 15.0.26621.2 | Wymagane
Microsoft.Net.Component.4.5.2.TargetingPack | Pakiet określania wartości docelowej platformy .NET framework 4.5.2 | 15.0.26621.2 | Wymagane
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 15.0.26621.2 | Wymagane
Microsoft.Net.Component.4.6.1.SDK | .NET framework 4.6.1 zestawu SDK | 15.0.26621.2 | Wymagane
Microsoft.Net.Component.4.6.1.TargetingPack | Pakiet określania wartości docelowej platformy .NET framework 4.6.1 | 15.0.26621.2 | Wymagane
Microsoft.Net.Component.4.6.TargetingPack | .NET framework 4.6 targeting pack | 15.0.26621.2 | Wymagane
Microsoft.Net.Component.4.TargetingPack | .NET framework 4 targeting pack | 15.0.26621.2 | Wymagane
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | Narzędzia do programowania .NET framework 4.6.1 | 15.0.26606.0 | Wymagane
Microsoft.Net.ComponentGroup.TargetingPacks.Common | Narzędzia deweloperskie programu .NET framework 4 — 4.6 | 15.0.26606.0 | Wymagane
Microsoft.Net.Core.Component.SDK | .NET podstawowe narzędzia do programowania 1.0 1.1 | 15.0.26606.0 | Wymagane
Microsoft.NetCore.ComponentGroup.DevelopmentTools | Narzędzia do programowania .NET core 2.0 | 15.0.26919.1 | Wymagane
Microsoft.NetCore.ComponentGroup.Web | Narzędzia do programowania .NET core 2.0 | 15.0.26919.1 | Wymagane
Microsoft.VisualStudio.Component.AppInsights.Tools | Narzędzia Developer Analytics tools | 15.0.26621.2 | Wymagane
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Azure Authoring Tools | 15.0.26621.2 | Wymagane
Microsoft.VisualStudio.Component.Azure.ClientLibs | Biblioteki Azure dla platformy .NET | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Emulator obliczeń platformy Azure | 15.0.26621.2 | Wymagane
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Emulator usługi Azure Storage | 15.0.26823.1 | Wymagane
Microsoft.VisualStudio.Component.Azure.Waverton | Azure podstawowe narzędzia usługi w chmurze | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.CloudExplorer | Eksplorator chmury | 15.0.26711.1 | Wymagane
Microsoft.VisualStudio.Component.Common.Azure.Tools | Narzędzia łączności i publikowanie | 1.10.50614.2 | Wymagane
Microsoft.VisualStudio.Component.IISExpress | Usługi IIS Express  | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | Diagnostyka JavaScript | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.JavaScript.TypeScript | Obsługa języka JavaScript i TypeScript | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Zarządzane podstawowe obciążenie pulpitu | 15.0.26419.1 | Wymagane
Microsoft.VisualStudio.Component.NuGet | Menedżer pakietów NuGet | 15.0.26621.2 | Wymagane
Microsoft.VisualStudio.Component.PortableLibrary | Biblioteka przenośna .NET targeting pack | 15.0.26208.0 | Wymagane
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
Microsoft.VisualStudio.Component.TypeScript.2.3 | TypeScript 2.3 zestawu SDK | 15.0.26621.2 | Wymagane
Microsoft.VisualStudio.Component.VisualStudioData | Źródła danych i odwołania do usług | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.Web | Narzędzia deweloperskie ASP.NET i sieć web | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.ComponentGroup.Azure.Prerequisites | Wymagania wstępne rozwoju platformy Azure | 15.0.26711.1 | Wymagane
Microsoft.VisualStudio.ComponentGroup.AzureFunctions | Narzędzia zadań Webjob platformy Microsoft Azure | 15.0.26720.2 | Wymagane
Microsoft.VisualStudio.ComponentGroup.Web | Narzędzia deweloperskie ASP.NET i sieć web | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET i sieć web development | 15.0.26606.0 | Wymagane
Microsoft.Component.Azure.DataLake.Tools | Usługa Azure Data Lake i narzędzia do analizy strumienia | 15.0.26823.1 | Zalecane
Microsoft.VisualStudio.Component.Azure.MobileAppsSdk | Azure SDK aplikacji mobilnych | 15.0.26504.0 | Zalecane
Microsoft.VisualStudio.Component.Azure.ResourceManager.Tools | Usługa Azure Resource Manager podstawowe narzędzia | 15.0.26906.1 | Zalecane
Microsoft.VisualStudio.Component.Azure.ServiceFabric.Tools | Narzędzia usługi Service Fabric | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.DiagnosticTools | Narzędzia profilowania platformy .NET | 15.0.26711.1 | Zalecane
Microsoft.VisualStudio.ComponentGroup.Azure.CloudServices | Narzędzia usługi w chmurze Azure | 15.0.26504.0 | Zalecane
Microsoft.VisualStudio.ComponentGroup.Azure.ResourceManager.Tools | Narzędzia Menedżera zasobów Azure | 15.0.26919.1 | Zalecane
Microsoft.Net.Component.4.6.2.SDK | .NET framework 4.6.2 zestawu SDK | 15.0.26208.0 | Optional
Microsoft.Net.Component.4.6.2.TargetingPack | .NET framework 4.6.2 docelowego pakietu | 15.0.26208.0 | Optional
Microsoft.Net.Component.4.7.SDK | .NET framework 4.7 zestawu SDK | 15.0.26419.1 | Optional
Microsoft.Net.Component.4.7.TargetingPack | .NET framework 4.7 targeting pack | 15.0.26621.2 | Optional
Microsoft.Net.ComponentGroup.4.6.2.DeveloperTools | Narzędzia do programowania .NET framework 4.6.2 | 15.0.26621.2 | Optional
Microsoft.Net.ComponentGroup.4.7.DeveloperTools | Narzędzia do programowania .NET framework 4.7 | 15.0.26606.0 | Optional
Microsoft.Net.Core.Component.SDK.1x | Oprogramowanie .NET core narzędzi programistycznych 1.0 1.1 dla komputerów typu Desktop | 15.0.26919.1 | Optional
Microsoft.NetCore.1x.ComponentGroup.Web | Oprogramowanie .NET core narzędzi programistycznych 1.0 1.1 dla sieci Web | 15.0.26919.1 | Optional
Microsoft.VisualStudio.Component.Azure.Storage.AzCopy | Narzędzie AzCopy magazynu Azure | 15.0.26906.1 | Optional
Microsoft.VisualStudio.Component.PowerShell.Tools | Narzędzia programu PowerShell | 3.0.552 | Optional
Microsoft.VisualStudio.Component.Wcf.Tooling | Windows Communication Foundation | 15.0.26606.0 | Optional


## <a name="data-storage-and-processing"></a>Magazyn danych i przetwarzania

**Identyfikator:** Microsoft.VisualStudio.Workload.Data

**Opis:** Connect, opracowanie i przetestowanie rozwiązania danych przy użyciu programu SQL Server, usługi Azure Data Lake, Hadoop lub uczenie Maszynowe Azure.

### <a name="components-included-by-this-workload"></a>Składniki przez to obciążenie

Identyfikator składnika | Nazwa | Wersja | Typ zależności
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Usługi językowe razor | 15.0.26720.2 | Zalecane
Component.Redgate.SQLSearch.VSExtension | Redgate SQL Search | 2.4.2.1439 | Zalecane
Component.WebSocket | WebSocket4Net | 15.0.26606.0 | Zalecane
Microsoft.Component.Azure.DataLake.Tools | Usługa Azure Data Lake i narzędzia do analizy strumienia | 15.0.26823.1 | Zalecane
Microsoft.Component.ClickOnce | Publikowanie ClickOnce | 15.0.26919.1 | Zalecane
Microsoft.Component.MSBuild | MSBuild | 15.0.26208.0 | Zalecane
Microsoft.Net.Component.4.5.1.TargetingPack | Pakiet docelowy .NET framework 4.5.1 | 15.0.26621.2 | Zalecane
Microsoft.Net.Component.4.5.2.TargetingPack | Pakiet określania wartości docelowej platformy .NET framework 4.5.2 | 15.0.26621.2 | Zalecane
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 15.0.26621.2 | Zalecane
Microsoft.Net.Component.4.6.1.SDK | .NET framework 4.6.1 zestawu SDK | 15.0.26621.2 | Zalecane
Microsoft.Net.Component.4.6.1.TargetingPack | Pakiet określania wartości docelowej platformy .NET framework 4.6.1 | 15.0.26621.2 | Zalecane
Microsoft.Net.Component.4.6.TargetingPack | .NET framework 4.6 targeting pack | 15.0.26621.2 | Zalecane
Microsoft.Net.Component.4.TargetingPack | .NET framework 4 targeting pack | 15.0.26621.2 | Zalecane
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | Narzędzia do programowania .NET framework 4.6.1 | 15.0.26606.0 | Zalecane
Microsoft.Net.ComponentGroup.TargetingPacks.Common | Narzędzia deweloperskie programu .NET framework 4 — 4.6 | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.AppInsights.Tools | Narzędzia Developer Analytics tools | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Azure Authoring Tools | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.Azure.ClientLibs | Biblioteki Azure dla platformy .NET | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Emulator obliczeń platformy Azure | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Emulator usługi Azure Storage | 15.0.26823.1 | Zalecane
Microsoft.VisualStudio.Component.Azure.Waverton | Azure podstawowe narzędzia usługi w chmurze | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.CloudExplorer | Eksplorator chmury | 15.0.26711.1 | Zalecane
Microsoft.VisualStudio.Component.Common.Azure.Tools | Narzędzia łączności i publikowanie | 1.10.50614.2 | Zalecane
Microsoft.VisualStudio.Component.IISExpress | Usługi IIS Express  | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | Diagnostyka JavaScript | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.JavaScript.TypeScript | Obsługa języka JavaScript i TypeScript | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Zarządzane podstawowe obciążenie pulpitu | 15.0.26419.1 | Zalecane
Microsoft.VisualStudio.Component.NuGet | Menedżer pakietów NuGet | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.PortableLibrary | Biblioteka przenośna .NET targeting pack | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilatory języka C# i Visual Basic Roslyn | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# i Visual Basic | 15.0.26711.1 | Zalecane
Microsoft.VisualStudio.Component.SQL.ADAL | Środowisko uruchomieniowe programu SQL ADAL | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.SQL.CLR | Typy danych CLR dla programu SQL Server | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.SQL.CMDUtils | Narzędzia wiersza polecenia programu SQL Server | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.SQL.DataSources | Obsługuje źródeł danych dla programu SQL Server | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | Program SQL Server Express 2016 LocalDB | 15.0.26919.1 | Zalecane
Microsoft.VisualStudio.Component.SQL.NCLI | SQL Server Native Client | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Data Tools | 15.0.26906.1 | Zalecane
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Narzędzia do analizy statycznej | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.TextTemplating | Transformacji szablonu tekstowego | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.TypeScript.2.3 | TypeScript 2.3 zestawu SDK | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.VisualStudioData | Źródła danych i odwołania do usług | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.Web | Narzędzia deweloperskie ASP.NET i sieć web | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.ComponentGroup.Web | Narzędzia deweloperskie ASP.NET i sieć web | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET i sieć web development | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.FSharp | Obsługa języka F # | 15.0.26606.0 | Optional


## <a name="data-science-and-analytical-applications"></a>Nauki dane i aplikacje analitycznych

**Identyfikator:** Microsoft.VisualStudio.Workload.DataScience

**Opis:** języków i narzędzi do tworzenia aplikacji analizy danych, w tym Python, R i F #.

### <a name="components-included-by-this-workload"></a>Składniki przez to obciążenie

Identyfikator składnika | Nazwa | Wersja | Typ zależności
--- | --- | --- | ---
Component.Anaconda3.x64 | Anaconda3 64-bitowych (4.4.0) | 4.4.0 | Zalecane
Component.Microsoft.VisualStudio.RazorExtension | Usługi językowe razor | 15.0.26720.2 | Zalecane
Microsoft.Component.CookiecutterTools | Obsługa szablonów Cookiecutter | 15.0.26621.2 | Zalecane
Microsoft.Component.PythonTools | Obsługa języka Python | 15.0.26823.1 | Zalecane
Microsoft.Component.PythonTools.Web | Obsługa sieci web języka Python | 15.0.26606.0 | Zalecane
Microsoft.Component.VC.Runtime.UCRTSDK | Zestaw Windows Universal CRT SDK | 15.0.26208.0 | Zalecane
Microsoft.Net.Component.4.6.1.TargetingPack | Pakiet określania wartości docelowej platformy .NET framework 4.6.1 | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.Common.Azure.Tools | Narzędzia łączności i publikowanie | 1.10.50614.2 | Zalecane
Microsoft.VisualStudio.Component.FSharp | Obsługa języka F # | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.JavaScript.TypeScript | Obsługa języka JavaScript i TypeScript | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.NuGet | Menedżer pakietów NuGet | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.R.Open | Klient Microsoft R (3.3.2) | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.RHost | Obsługa środowiska uruchomieniowego dla narzędzi programistycznych R | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilatory języka C# i Visual Basic Roslyn | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# i Visual Basic | 15.0.26711.1 | Zalecane
Microsoft.VisualStudio.Component.RTools | Obsługa języków R | 15.0.26919.1 | Zalecane
Microsoft.VisualStudio.Component.SQL.CLR | Typy danych CLR dla programu SQL Server | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Narzędzia do analizy statycznej | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.TypeScript.2.3 | TypeScript 2.3 zestawu SDK | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.VisualStudioData | Źródła danych i odwołania do usług | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.Windows81SDK | Zestaw SDK systemu Windows 8.1 | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET i sieć web development | 15.0.26606.0 | Zalecane
Component.Anaconda2.x64 | Anaconda2 64-bitowych (4.4.0) | 4.4.0 | Optional
Component.Anaconda2.x86 | Anaconda2 32-bitowych (4.4.0) | 4.4.0 | Optional
Component.Anaconda3.x86 | Anaconda3 32-bitowych (4.4.0) | 4.4.0 | Optional
Microsoft.ComponentGroup.PythonTools.NativeDevelopment | Narzędzia deweloperskie macierzystego języka Python | 15.0.27004.2002 | Optional
Microsoft.VisualStudio.Component.Graphics.Tools | Grafika debugera i profilera procesora GPU programu DirectX | 15.0.26823.1 | Optional
Microsoft.VisualStudio.Component.Graphics.Win81 | Grafika narzędzi Windows 8.1 SDK | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.VC.140 | Zestaw narzędzi w wersji 140 2015.3 VC ++ dla komputerów typu desktop (x86, x64) | 15.0.26720.2 | Optional
Microsoft.VisualStudio.Component.VC.CoreIde | Visual Studio C++ podstawowe funkcje | 15.0.26606.0 | Optional
Microsoft.VisualStudio.Component.VC.DiagnosticTools | Narzędzia profilowania C++ | 15.0.26823.1 | Optional
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | Zestaw narzędzi v141 2017 VC ++ (x86, x64) | 15.0.26823.1 | Optional
Microsoft.VisualStudio.Component.Windows10SDK | Środowisko wykonawcze systemu Windows Universal C | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.16299.Desktop | Windows 10 SDK (10.0.16299.0) dla pulpitu C++ [x86 i x64] | 15.0.27004.2002 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP | Windows 10 SDK (10.0.16299.0) dla platformy uniwersalnej systemu Windows: C#, VB, JS | 15.0.27004.2002 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP.Native | Windows 10 SDK (10.0.16299.0) dla platformy uniwersalnej systemu Windows: C++ | 15.0.27004.2002 | Optional


## <a name="net-desktop-development"></a>.NET — rozwój pulpitu

**Identyfikator:** Microsoft.VisualStudio.Workload.ManagedDesktop

**Opis:** tworzenie WPF, formularze systemu Windows i aplikacje konsoli przy użyciu języka C#, VB i F #.

### <a name="components-included-by-this-workload"></a>Składniki przez to obciążenie

Identyfikator składnika | Nazwa | Wersja | Typ zależności
--- | --- | --- | ---
Microsoft.Component.ClickOnce | Publikowanie ClickOnce | 15.0.26919.1 | Wymagane
Microsoft.Component.MSBuild | MSBuild | 15.0.26208.0 | Wymagane
Microsoft.Net.Component.4.6.1.SDK | .NET framework 4.6.1 zestawu SDK | 15.0.26621.2 | Wymagane
Microsoft.Net.Component.4.6.1.TargetingPack | Pakiet określania wartości docelowej platformy .NET framework 4.6.1 | 15.0.26621.2 | Wymagane
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | Narzędzia do programowania .NET framework 4.6.1 | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.Debugger.JustInTime | Debuger Just In Time | 15.0.26823.1 | Wymagane
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Zarządzane podstawowe obciążenie pulpitu | 15.0.26419.1 | Wymagane
Microsoft.VisualStudio.Component.ManagedDesktop.Prerequisites | Narzędzia do tworzenia klasycznych aplikacji .NET | 15.0.26906.1 | Wymagane
Microsoft.VisualStudio.Component.PortableLibrary | Biblioteka przenośna .NET targeting pack | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilatory języka C# i Visual Basic Roslyn | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# i Visual Basic | 15.0.26711.1 | Wymagane
Microsoft.VisualStudio.Component.SQL.CLR | Typy danych CLR dla programu SQL Server | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Narzędzia do analizy statycznej | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.TextTemplating | Transformacji szablonu tekstowego | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.VisualStudioData | Źródła danych i odwołania do usług | 15.0.26208.0 | Wymagane
Microsoft.ComponentGroup.Blend | Blend for Visual Studio | 15.0.26711.1 | Zalecane
Microsoft.Net.Component.4.5.1.TargetingPack | Pakiet docelowy .NET framework 4.5.1 | 15.0.26621.2 | Zalecane
Microsoft.Net.Component.4.5.2.TargetingPack | Pakiet określania wartości docelowej platformy .NET framework 4.5.2 | 15.0.26621.2 | Zalecane
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 15.0.26621.2 | Zalecane
Microsoft.Net.Component.4.6.TargetingPack | .NET framework 4.6 targeting pack | 15.0.26621.2 | Zalecane
Microsoft.Net.Component.4.TargetingPack | .NET framework 4 targeting pack | 15.0.26621.2 | Zalecane
Microsoft.Net.ComponentGroup.TargetingPacks.Common | Narzędzia deweloperskie programu .NET framework 4 — 4.6 | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.EntityFramework | Entity Framework 6 narzędzia | 15.0.26208.0 | Zalecane
Component.Dotfuscator | Ochrona cenią sobie wcześniejsze — Dotfuscator | 15.0.26208.0 | Optional
Microsoft.Net.Component.4.6.2.SDK | .NET framework 4.6.2 zestawu SDK | 15.0.26208.0 | Optional
Microsoft.Net.Component.4.6.2.TargetingPack | .NET framework 4.6.2 docelowego pakietu | 15.0.26208.0 | Optional
Microsoft.Net.Component.4.7.SDK | .NET framework 4.7 zestawu SDK | 15.0.26419.1 | Optional
Microsoft.Net.Component.4.7.TargetingPack | .NET framework 4.7 targeting pack | 15.0.26621.2 | Optional
Microsoft.Net.ComponentGroup.4.6.2.DeveloperTools | Narzędzia do programowania .NET framework 4.6.2 | 15.0.26621.2 | Optional
Microsoft.Net.ComponentGroup.4.7.DeveloperTools | Narzędzia do programowania .NET framework 4.7 | 15.0.26606.0 | Optional
Microsoft.Net.Core.Component.SDK | .NET podstawowe narzędzia do programowania 1.0 1.1 | 15.0.26606.0 | Optional
Microsoft.Net.Core.Component.SDK.1x | Oprogramowanie .NET core narzędzi programistycznych 1.0 1.1 dla komputerów typu Desktop | 15.0.26919.1 | Optional
Microsoft.NetCore.ComponentGroup.DevelopmentTools | Narzędzia do programowania .NET core 2.0 | 15.0.26919.1 | Optional
Microsoft.VisualStudio.Component.FSharp | Obsługa języka F # | 15.0.26606.0 | Optional
Microsoft.VisualStudio.Component.IISExpress | Usługi IIS Express  | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.NuGet | Menedżer pakietów NuGet | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | Program SQL Server Express 2016 LocalDB | 15.0.26919.1 | Optional
Microsoft.VisualStudio.Component.SQL.NCLI | SQL Server Native Client | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.Wcf.Tooling | Windows Communication Foundation | 15.0.26606.0 | Optional
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 15.0.26208.0 | Optional


## <a name="game-development-with-unity"></a>Tworzenie gier z Unity

**Identyfikator:** Microsoft.VisualStudio.Workload.ManagedGame

**Opis:** tworzenia gier 2W i 3W z Unity, wydajne i platform środowisko dla deweloperów.

### <a name="components-included-by-this-workload"></a>Składniki przez to obciążenie

Identyfikator składnika | Nazwa | Wersja | Typ zależności
--- | --- | --- | ---
Microsoft.Net.Component.3.5.DeveloperTools | Narzędzia do programowania .NET framework 3.5 | 15.0.26621.2 | Wymagane
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilatory języka C# i Visual Basic Roslyn | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# i Visual Basic | 15.0.26711.1 | Wymagane
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Narzędzia do analizy statycznej | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.Unity | Visual Studio Tools for Unity | 15.0.26823.1 | Wymagane
Component.UnityEngine.x64 | Edytor 64-bitowych Unity 2017.1 | 15.0.26919.1 | Zalecane
Component.UnityEngine.x86 | Edytor 32-bitowej platformy Unity 5.6 | 15.0.26919.1 | Zalecane


## <a name="linux-development-with-c"></a>Tworzenie Linux za pomocą języka C++

**Identyfikator:** Microsoft.VisualStudio.Workload.NativeCrossPlat

**Opis:** Utwórz i debugowania aplikacji w środowisku systemu Linux.

### <a name="components-included-by-this-workload"></a>Składniki przez to obciążenie

Identyfikator składnika | Nazwa | Wersja | Typ zależności
--- | --- | --- | ---
Component.MDD.Linux | Visual C++ dla rozwoju systemu Linux | 15.0.26711.1 | Wymagane
Microsoft.VisualStudio.Component.VC.CoreIde | Visual Studio C++ podstawowe funkcje | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.Windows10SDK | Środowisko wykonawcze systemu Windows Universal C | 15.0.26621.2 | Wymagane
Component.Linux.CMake | Narzędzia Visual C++ tools for CMake i Linux | 15.0.27004.2002 | Zalecane
Component.Microsoft.VisualStudio.RazorExtension | Usługi językowe razor | 15.0.26720.2 | Zalecane
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilatory języka C# i Visual Basic Roslyn | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# i Visual Basic | 15.0.26711.1 | Zalecane
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Narzędzia do analizy statycznej | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | Zestaw narzędzi v141 2017 VC ++ (x86, x64) | 15.0.26823.1 | Zalecane
Microsoft.VisualStudio.Component.Windows10SDK.16299.Desktop | Windows 10 SDK (10.0.16299.0) dla pulpitu C++ [x86 i x64] | 15.0.27004.2002 | Zalecane
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP | Windows 10 SDK (10.0.16299.0) dla platformy uniwersalnej systemu Windows: C#, VB, JS | 15.0.27004.2002 | Zalecane
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP.Native | Windows 10 SDK (10.0.16299.0) dla platformy uniwersalnej systemu Windows: C++ | 15.0.27004.2002 | Zalecane
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET i sieć web development | 15.0.26606.0 | Zalecane


## <a name="desktop-development-with-c"></a>Tworzenie pulpitu za pomocą języka C++

**Identyfikator:** Microsoft.VisualStudio.Workload.NativeDesktop

**Opis:** tworzenia klasycznych aplikacji opartych na systemie Windows przy użyciu zestawu narzędzi Visual C++ ATL i opcjonalne funkcje, takie jak MFC i C + +/ CLI.

### <a name="components-included-by-this-workload"></a>Składniki przez to obciążenie

Identyfikator składnika | Nazwa | Wersja | Typ zależności
--- | --- | --- | ---
Microsoft.Component.MSBuild | MSBuild | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.Debugger.JustInTime | Debuger Just In Time | 15.0.26823.1 | Wymagane
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilatory języka C# i Visual Basic Roslyn | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.TextTemplating | Transformacji szablonu tekstowego | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.VC.CoreIde | Visual Studio C++ podstawowe funkcje | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.VC.Redist.14.Latest | Aktualizacji pakietu redystrybucyjnego Visual C++ 2017 r. | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.ComponentGroup.NativeDesktop.Core | Visual C++ podstawowe pulpitu funkcje | 15.0.26621.2 | Wymagane
Component.Microsoft.VisualStudio.RazorExtension | Usługi językowe razor | 15.0.26720.2 | Zalecane
Microsoft.VisualStudio.Component.Graphics.Tools | Grafika debugera i profilera procesora GPU programu DirectX | 15.0.26823.1 | Zalecane
Microsoft.VisualStudio.Component.Graphics.Win81 | Grafika narzędzi Windows 8.1 SDK | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# i Visual Basic | 15.0.26711.1 | Zalecane
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Narzędzia do analizy statycznej | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.VC.CMake.Project | Narzędzia Visual C++ tools for CMake | 15.0.27004.2002 | Zalecane
Microsoft.VisualStudio.Component.VC.DiagnosticTools | Narzędzia profilowania C++ | 15.0.26823.1 | Zalecane
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | Zestaw narzędzi v141 2017 VC ++ (x86, x64) | 15.0.26823.1 | Zalecane
Microsoft.VisualStudio.Component.Windows10SDK.16299.Desktop | Windows 10 SDK (10.0.16299.0) dla pulpitu C++ [x86 i x64] | 15.0.27004.2002 | Zalecane
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP | Windows 10 SDK (10.0.16299.0) dla platformy uniwersalnej systemu Windows: C#, VB, JS | 15.0.27004.2002 | Zalecane
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP.Native | Windows 10 SDK (10.0.16299.0) dla platformy uniwersalnej systemu Windows: C++ | 15.0.27004.2002 | Zalecane
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET i sieć web development | 15.0.26606.0 | Zalecane
Component.Incredibuild | IncrediBuild - przyspieszenia kompilacji | 15.0.26919.1 | Optional
Component.IncredibuildMenu | IncrediBuildMenu | 1.5.0.1 | Optional
Microsoft.Component.VC.Runtime.UCRTSDK | Zestaw Windows Universal CRT SDK | 15.0.26208.0 | Optional
Microsoft.Net.Component.4.6.1.SDK | .NET framework 4.6.1 zestawu SDK | 15.0.26621.2 | Optional
Microsoft.Net.Component.4.6.1.TargetingPack | Pakiet określania wartości docelowej platformy .NET framework 4.6.1 | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.VC.140 | Zestaw narzędzi w wersji 140 2015.3 VC ++ dla komputerów typu desktop (x86, x64) | 15.0.26720.2 | Optional
Microsoft.VisualStudio.Component.VC.ATL | Visual C++ ATL — Obsługa | 15.0.26823.1 | Optional
Microsoft.VisualStudio.Component.VC.ATLMFC | Obsługa MFC i ATL (x86 i x64) | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.VC.ClangC2 | Clang/C2 (eksperymentalne) | 15.0.26823.1 | Optional
Microsoft.VisualStudio.Component.VC.CLI.Support | C + +/ CLI pomocy technicznej | 15.0.26823.1 | Optional
Microsoft.VisualStudio.Component.VC.Modules.x86.x64 | Moduły biblioteki standardowej (eksperymentalne) | 15.0.26720.2 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.10240 | Windows 10 SDK (10.0.10240.0) | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.10586 | Windows 10 SDK (10.0.10586.0) | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.14393 | Windows 10 SDK (10.0.14393.0) | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.15063.Desktop | Windows 10 SDK (10.0.15063.0) dla pulpitu C++ [x86 i x64] | 15.0.26929.2 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.15063.UWP | Windows 10 SDK (10.0.15063.0) dla platformy uniwersalnej systemu Windows: C#, VB, JS | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.15063.UWP.Native | Windows 10 SDK (10.0.15063.0) dla platformy uniwersalnej systemu Windows: C++ | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.Windows81SDK | Zestaw SDK systemu Windows 8.1 | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.WinXP | Obsługa systemu Windows XP dla języka C++ | 15.0.26208.0 | Optional
Microsoft.VisualStudio.ComponentGroup.NativeDesktop.Win81 | Windows 8.1 SDK i Biblioteka UCRT | 15.0.26208.0 | Optional
Microsoft.VisualStudio.ComponentGroup.NativeDesktop.WinXP | Obsługa systemu Windows XP dla języka C++ | 15.0.26208.0 | Optional


## <a name="game-development-with-c"></a>Tworzenie gier z C++

**Identyfikator:** Microsoft.VisualStudio.Workload.NativeGame

**Opis:** umożliwia tworzenie profesjonalnych gry obsługiwane przez usługę programu DirectX, niezr lub Cocos2d pełną moc C++.

### <a name="components-included-by-this-workload"></a>Składniki przez to obciążenie

Identyfikator składnika | Nazwa | Wersja | Typ zależności
--- | --- | --- | ---
Microsoft.VisualStudio.Component.VC.Redist.14.Latest | Aktualizacji pakietu redystrybucyjnego Visual C++ 2017 r. | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.Graphics.Tools | Grafika debugera i profilera procesora GPU programu DirectX | 15.0.26823.1 | Zalecane
Microsoft.VisualStudio.Component.Graphics.Win81 | Grafika narzędzi Windows 8.1 SDK | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Narzędzia do analizy statycznej | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.VC.CoreIde | Visual Studio C++ podstawowe funkcje | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.VC.DiagnosticTools | Narzędzia profilowania C++ | 15.0.26823.1 | Zalecane
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | Zestaw narzędzi v141 2017 VC ++ (x86, x64) | 15.0.26823.1 | Zalecane
Microsoft.VisualStudio.Component.Windows10SDK.16299.Desktop | Windows 10 SDK (10.0.16299.0) dla pulpitu C++ [x86 i x64] | 15.0.27004.2002 | Zalecane
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP | Windows 10 SDK (10.0.16299.0) dla platformy uniwersalnej systemu Windows: C#, VB, JS | 15.0.27004.2002 | Zalecane
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP.Native | Windows 10 SDK (10.0.16299.0) dla platformy uniwersalnej systemu Windows: C++ | 15.0.27004.2002 | Zalecane
Component.Android.NDK.R12B | Zestawu NDK systemu android (R12B) | 12.1.9 | Optional
Component.Android.SDK23.Private | Instalacja zestawu SDK systemu android (interfejs API na poziomie 23) (lokalnej instalacji) | 15.0.26906.1 | Optional
Component.Ant | Apache Ant (1.9.3) | 1.9.3.7 | Optional
Component.Cocos | Cocos | 15.0.26906.1 | Optional
Component.Incredibuild | IncrediBuild - przyspieszenia kompilacji | 15.0.26919.1 | Optional
Component.IncredibuildMenu | IncrediBuildMenu | 1.5.0.1 | Optional
Component.JavaJDK | Zestaw Java SE Development Kit (8.0.1120.15) | 15.0.26403.0 | Optional
Component.MDD.Android | Narzędzia deweloperskie dla systemu Android w języku C++ | 15.0.26606.0 | Optional
Component.Unreal | Instalator aparatu unreal | 15.0.26621.2 | Optional
Component.Unreal.Android | Visual Studio dla systemu Android obsługę aparatu Unreal Engine | 15.0.26919.1 | Optional
Microsoft.Component.VC.Runtime.UCRTSDK | Zestaw Windows Universal CRT SDK | 15.0.26208.0 | Optional
Microsoft.Net.Component.4.5.1.TargetingPack | Pakiet docelowy .NET framework 4.5.1 | 15.0.26621.2 | Optional
Microsoft.Net.Component.4.5.2.TargetingPack | Pakiet określania wartości docelowej platformy .NET framework 4.5.2 | 15.0.26621.2 | Optional
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 15.0.26621.2 | Optional
Microsoft.Net.Component.4.6.1.SDK | .NET framework 4.6.1 zestawu SDK | 15.0.26621.2 | Optional
Microsoft.Net.Component.4.6.1.TargetingPack | Pakiet określania wartości docelowej platformy .NET framework 4.6.1 | 15.0.26621.2 | Optional
Microsoft.Net.Component.4.6.TargetingPack | .NET framework 4.6 targeting pack | 15.0.26621.2 | Optional
Microsoft.Net.Component.4.TargetingPack | .NET framework 4 targeting pack | 15.0.26621.2 | Optional
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | Narzędzia do programowania .NET framework 4.6.1 | 15.0.26606.0 | Optional
Microsoft.Net.ComponentGroup.TargetingPacks.Common | Narzędzia deweloperskie programu .NET framework 4 — 4.6 | 15.0.26606.0 | Optional
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilatory języka C# i Visual Basic Roslyn | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# i Visual Basic | 15.0.26711.1 | Optional
Microsoft.VisualStudio.Component.Windows10SDK | Środowisko wykonawcze systemu Windows Universal C | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.10240 | Windows 10 SDK (10.0.10240.0) | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.10586 | Windows 10 SDK (10.0.10586.0) | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.14393 | Windows 10 SDK (10.0.14393.0) | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.15063.Desktop | Windows 10 SDK (10.0.15063.0) dla pulpitu C++ [x86 i x64] | 15.0.26929.2 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.15063.UWP | Windows 10 SDK (10.0.15063.0) dla platformy uniwersalnej systemu Windows: C#, VB, JS | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.15063.UWP.Native | Windows 10 SDK (10.0.15063.0) dla platformy uniwersalnej systemu Windows: C++ | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.Windows81SDK | Zestaw SDK systemu Windows 8.1 | 15.0.26208.0 | Optional
Microsoft.VisualStudio.ComponentGroup.NativeDesktop.Win81 | Windows 8.1 SDK i Biblioteka UCRT | 15.0.26208.0 | Optional


## <a name="mobile-development-with-c"></a>Tworzenie przenośnych za pomocą języka C++

**Identyfikator:** Microsoft.VisualStudio.Workload.NativeMobile

**Opis:** tworzenie wieloplatformowych aplikacji dla systemu iOS, Android i Windows za pomocą języka C++.

### <a name="components-included-by-this-workload"></a>Składniki przez to obciążenie

Identyfikator składnika | Nazwa | Wersja | Typ zależności
--- | --- | --- | ---
Microsoft.VisualStudio.Component.VC.CoreIde | Visual Studio C++ podstawowe funkcje | 15.0.26606.0 | Wymagane
Component.Android.NDK.R13B | Zestawu NDK systemu android (R13B) | 13.1.6 | Zalecane
Component.Android.SDK19 | Instalacja zestawu SDK systemu android (poziom interfejsu API 19 i 21) | 15.0.26621.2 | Zalecane
Component.Android.SDK22 | Instalacja zestawu SDK systemu android (interfejs API na poziomie 22) | 15.0.26208.0 | Zalecane
Component.Android.SDK25 | Instalacja zestawu SDK systemu android (interfejs API na poziomie 25) | 15.0.26919.1 | Zalecane
Component.Ant | Apache Ant (1.9.3) | 1.9.3.7 | Zalecane
Component.MDD.Android | Narzędzia deweloperskie dla systemu Android w języku C++ | 15.0.26606.0 | Zalecane
Component.Android.NDK.R12B | Zestawu NDK systemu android (R12B) | 12.1.9 | Optional
Component.Android.NDK.R12B_3264 | Zestawu NDK systemu android (R12B) (32-bitowe) | 12.1.10 | Optional
Component.Android.NDK.R13B_3264 | Zestawu NDK systemu android (R13B) (32-bitowe) | 13.1.7 | Optional
Component.Android.SDK23 | Instalacja zestawu SDK systemu android (interfejs API na poziomie 23) (Instalacja globalne) | 15.0.26906.1 | Optional
Component.Google.Android.Emulator.API23.V2 | Emulator systemu Google Android (interfejs API poziomie 23) (Instalacja globalne) | 15.0.26906.1 | Optional
Component.HAXM | Intel sprzętu przyspieszyć wykonywanie Menedżera (HAXM) (Instalacja globalne) | 15.0.26919.1 | Optional
Component.Incredibuild | IncrediBuild - przyspieszenia kompilacji | 15.0.26919.1 | Optional
Component.IncredibuildMenu | IncrediBuildMenu | 1.5.0.1 | Optional
Component.JavaJDK | Zestaw Java SE Development Kit (8.0.1120.15) | 15.0.26403.0 | Optional
Component.MDD.IOS | Narzędzia deweloperskie dla systemu iOS C++ | 15.0.26621.2 | Optional


## <a name="net-core-cross-platform-development"></a>Programowanie wieloplatformowych .NET core

**Identyfikator:** Microsoft.VisualStudio.Workload.NetCoreTools

**Opis:** tworzenie wieloplatformowych aplikacji za pomocą narzędzia do programowania .NET Core, platformy ASP.NET Core, HTML, JavaScript i kontenera.

### <a name="components-included-by-this-workload"></a>Składniki przez to obciążenie

Identyfikator składnika | Nazwa | Wersja | Typ zależności
--- | --- | --- | ---
Microsoft.Net.Core.Component.SDK | .NET podstawowe narzędzia do programowania 1.0 1.1 | 15.0.26606.0 | Wymagane
Microsoft.NetCore.ComponentGroup.DevelopmentTools | Narzędzia do programowania .NET core 2.0 | 15.0.26919.1 | Wymagane
Microsoft.NetCore.ComponentGroup.Web | Narzędzia do programowania .NET core 2.0 | 15.0.26919.1 | Wymagane
Component.Microsoft.VisualStudio.RazorExtension | Usługi językowe razor | 15.0.26720.2 | Zalecane
Component.WebSocket | WebSocket4Net | 15.0.26606.0 | Zalecane
Microsoft.Component.ClickOnce | Publikowanie ClickOnce | 15.0.26919.1 | Zalecane
Microsoft.Component.MSBuild | MSBuild | 15.0.26208.0 | Zalecane
Microsoft.Net.Component.4.5.1.TargetingPack | Pakiet docelowy .NET framework 4.5.1 | 15.0.26621.2 | Zalecane
Microsoft.Net.Component.4.5.2.TargetingPack | Pakiet określania wartości docelowej platformy .NET framework 4.5.2 | 15.0.26621.2 | Zalecane
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 15.0.26621.2 | Zalecane
Microsoft.Net.Component.4.6.1.SDK | .NET framework 4.6.1 zestawu SDK | 15.0.26621.2 | Zalecane
Microsoft.Net.Component.4.6.1.TargetingPack | Pakiet określania wartości docelowej platformy .NET framework 4.6.1 | 15.0.26621.2 | Zalecane
Microsoft.Net.Component.4.6.TargetingPack | .NET framework 4.6 targeting pack | 15.0.26621.2 | Zalecane
Microsoft.Net.Component.4.TargetingPack | .NET framework 4 targeting pack | 15.0.26621.2 | Zalecane
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | Narzędzia do programowania .NET framework 4.6.1 | 15.0.26606.0 | Zalecane
Microsoft.Net.ComponentGroup.TargetingPacks.Common | Narzędzia deweloperskie programu .NET framework 4 — 4.6 | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.AppInsights.Tools | Narzędzia Developer Analytics tools | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Azure Authoring Tools | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.Azure.ClientLibs | Biblioteki Azure dla platformy .NET | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Emulator obliczeń platformy Azure | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Emulator usługi Azure Storage | 15.0.26823.1 | Zalecane
Microsoft.VisualStudio.Component.Azure.Waverton | Azure podstawowe narzędzia usługi w chmurze | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.CloudExplorer | Eksplorator chmury | 15.0.26711.1 | Zalecane
Microsoft.VisualStudio.Component.Common.Azure.Tools | Narzędzia łączności i publikowanie | 1.10.50614.2 | Zalecane
Microsoft.VisualStudio.Component.DiagnosticTools | Narzędzia profilowania platformy .NET | 15.0.26711.1 | Zalecane
Microsoft.VisualStudio.Component.DockerTools | Narzędzia programistyczne dla kontenerów | 15.0.26724.1 | Zalecane
Microsoft.VisualStudio.Component.IISExpress | Usługi IIS Express  | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | Diagnostyka JavaScript | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.JavaScript.TypeScript | Obsługa języka JavaScript i TypeScript | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Zarządzane podstawowe obciążenie pulpitu | 15.0.26419.1 | Zalecane
Microsoft.VisualStudio.Component.NuGet | Menedżer pakietów NuGet | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.PortableLibrary | Biblioteka przenośna .NET targeting pack | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilatory języka C# i Visual Basic Roslyn | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# i Visual Basic | 15.0.26711.1 | Zalecane
Microsoft.VisualStudio.Component.SQL.ADAL | Środowisko uruchomieniowe programu SQL ADAL | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.SQL.CLR | Typy danych CLR dla programu SQL Server | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.SQL.CMDUtils | Narzędzia wiersza polecenia programu SQL Server | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.SQL.DataSources | Obsługuje źródeł danych dla programu SQL Server | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | Program SQL Server Express 2016 LocalDB | 15.0.26919.1 | Zalecane
Microsoft.VisualStudio.Component.SQL.NCLI | SQL Server Native Client | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Data Tools | 15.0.26906.1 | Zalecane
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Narzędzia do analizy statycznej | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.TextTemplating | Transformacji szablonu tekstowego | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.TypeScript.2.3 | TypeScript 2.3 zestawu SDK | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.VisualStudioData | Źródła danych i odwołania do usług | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.Web | Narzędzia deweloperskie ASP.NET i sieć web | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.ComponentGroup.Web | Narzędzia deweloperskie ASP.NET i sieć web | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET i sieć web development | 15.0.26606.0 | Zalecane
Microsoft.Net.Core.Component.SDK.1x | Oprogramowanie .NET core narzędzi programistycznych 1.0 1.1 dla komputerów typu Desktop | 15.0.26919.1 | Optional
Microsoft.NetCore.1x.ComponentGroup.Web | Oprogramowanie .NET core narzędzi programistycznych 1.0 1.1 dla sieci Web | 15.0.26919.1 | Optional
Microsoft.VisualStudio.ComponentGroup.IISDevelopment | Programowanie czasu obsługi usług IIS | 15.0.26720.2 | Optional


## <a name="mobile-development-with-net"></a>Programowanie przenośnych z platformą .NET

**Identyfikator:** Microsoft.VisualStudio.Workload.NetCrossPlat

**Opis:** tworzenie wieloplatformowych aplikacji dla systemu iOS, Android i Windows za pomocą platformy Xamarin.

### <a name="components-included-by-this-workload"></a>Składniki przez to obciążenie

Identyfikator składnika | Nazwa | Wersja | Typ zależności
--- | --- | --- | ---
Component.Android.SDK25 | Instalacja zestawu SDK systemu android (interfejs API na poziomie 25) | 15.0.26919.1 | Wymagane
Component.Google.Android.Emulator.API25 | Emulator systemu Google Android (interfejs API na poziomie 25) | 15.0.26929.2 | Wymagane
Component.HAXM | Intel sprzętu przyspieszyć wykonywanie Menedżera (HAXM) (Instalacja globalne) | 15.0.26919.1 | Wymagane
Component.JavaJDK | Zestaw Java SE Development Kit (8.0.1120.15) | 15.0.26403.0 | Wymagane
Microsoft.Net.Component.4.6.1.SDK | .NET framework 4.6.1 zestawu SDK | 15.0.26621.2 | Wymagane
Microsoft.Net.Component.4.6.1.TargetingPack | Pakiet określania wartości docelowej platformy .NET framework 4.6.1 | 15.0.26621.2 | Wymagane
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | Narzędzia do programowania .NET framework 4.6.1 | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.PortableLibrary | Biblioteka przenośna .NET targeting pack | 15.0.26208.0 | Wymagane
Component.Android.NDK.R13B | Zestawu NDK systemu android (R13B) | 13.1.6 | Zalecane
Component.Xamarin | Xamarin | 15.0.26711.1 | Zalecane
Component.Xamarin.Inspector | Skoroszyty Xamarin | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.FSharp | Obsługa języka F # | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.Merq | Popularne narzędzia wewnętrzny Xamarin | 15.0.26720.2 | Zalecane
Microsoft.VisualStudio.Component.MonoDebugger | Debuger mono | 15.0.26720.2 | Zalecane
Microsoft.VisualStudio.Component.NuGet | Menedżer pakietów NuGet | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilatory języka C# i Visual Basic Roslyn | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# i Visual Basic | 15.0.26711.1 | Zalecane
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Narzędzia do analizy statycznej | 15.0.26208.0 | Zalecane
Microsoft.Component.ClickOnce | Publikowanie ClickOnce | 15.0.26919.1 | Optional
Microsoft.Component.NetFX.Native | Architektura .NET Native | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.AppInsights.Tools | Narzędzia Developer Analytics tools | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.DiagnosticTools | Narzędzia profilowania platformy .NET | 15.0.26711.1 | Optional
Microsoft.VisualStudio.Component.Graphics | Edytory modelu obrazu i 3W | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.Phone.Emulator.15063 | Emulatorze przenośnym z systemem Windows 10 (twórców aktualizacja) | 15.0.26711.1 | Optional
Microsoft.VisualStudio.Component.SQL.CLR | Typy danych CLR dla programu SQL Server | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.VisualStudioData | Źródła danych i odwołania do usług | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP | Windows 10 SDK (10.0.16299.0) dla platformy uniwersalnej systemu Windows: C#, VB, JS | 15.0.27004.2002 | Optional
Microsoft.VisualStudio.ComponentGroup.UWP.Xamarin | Narzędzia uniwersalnych platformy systemu Windows dla platformy Xamarin | 15.0.27004.2002 | Optional


## <a name="aspnet-and-web-development"></a>ASP.NET i sieć web development

**Identyfikator:** Microsoft.VisualStudio.Workload.NetWeb

**Opis:** tworzenie aplikacji sieci web przy użyciu narzędzi programistycznych platformy ASP.NET, platformy ASP.NET Core, HTML, JavaScript i kontenera.

### <a name="components-included-by-this-workload"></a>Składniki przez to obciążenie

Identyfikator składnika | Nazwa | Wersja | Typ zależności
--- | --- | --- | ---
Microsoft.Net.Core.Component.SDK | .NET podstawowe narzędzia do programowania 1.0 1.1 | 15.0.26606.0 | Wymagane
Microsoft.NetCore.ComponentGroup.DevelopmentTools | Narzędzia do programowania .NET core 2.0 | 15.0.26919.1 | Wymagane
Microsoft.NetCore.ComponentGroup.Web | Narzędzia do programowania .NET core 2.0 | 15.0.26919.1 | Wymagane
Component.Microsoft.VisualStudio.RazorExtension | Usługi językowe razor | 15.0.26720.2 | Zalecane
Component.WebSocket | WebSocket4Net | 15.0.26606.0 | Zalecane
Microsoft.Component.ClickOnce | Publikowanie ClickOnce | 15.0.26919.1 | Zalecane
Microsoft.Component.MSBuild | MSBuild | 15.0.26208.0 | Zalecane
Microsoft.Net.Component.4.5.1.TargetingPack | Pakiet docelowy .NET framework 4.5.1 | 15.0.26621.2 | Zalecane
Microsoft.Net.Component.4.5.2.TargetingPack | Pakiet określania wartości docelowej platformy .NET framework 4.5.2 | 15.0.26621.2 | Zalecane
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 15.0.26621.2 | Zalecane
Microsoft.Net.Component.4.6.1.SDK | .NET framework 4.6.1 zestawu SDK | 15.0.26621.2 | Zalecane
Microsoft.Net.Component.4.6.1.TargetingPack | Pakiet określania wartości docelowej platformy .NET framework 4.6.1 | 15.0.26621.2 | Zalecane
Microsoft.Net.Component.4.6.TargetingPack | .NET framework 4.6 targeting pack | 15.0.26621.2 | Zalecane
Microsoft.Net.Component.4.TargetingPack | .NET framework 4 targeting pack | 15.0.26621.2 | Zalecane
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | Narzędzia do programowania .NET framework 4.6.1 | 15.0.26606.0 | Zalecane
Microsoft.Net.ComponentGroup.TargetingPacks.Common | Narzędzia deweloperskie programu .NET framework 4 — 4.6 | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.AppInsights.Tools | Narzędzia Developer Analytics tools | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Azure Authoring Tools | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.Azure.ClientLibs | Biblioteki Azure dla platformy .NET | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Emulator obliczeń platformy Azure | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Emulator usługi Azure Storage | 15.0.26823.1 | Zalecane
Microsoft.VisualStudio.Component.Azure.Waverton | Azure podstawowe narzędzia usługi w chmurze | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.CloudExplorer | Eksplorator chmury | 15.0.26711.1 | Zalecane
Microsoft.VisualStudio.Component.Common.Azure.Tools | Narzędzia łączności i publikowanie | 1.10.50614.2 | Zalecane
Microsoft.VisualStudio.Component.DiagnosticTools | Narzędzia profilowania platformy .NET | 15.0.26711.1 | Zalecane
Microsoft.VisualStudio.Component.DockerTools | Narzędzia programistyczne dla kontenerów | 15.0.26724.1 | Zalecane
Microsoft.VisualStudio.Component.EntityFramework | Entity Framework 6 narzędzia | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.IISExpress | Usługi IIS Express  | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | Diagnostyka JavaScript | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.JavaScript.TypeScript | Obsługa języka JavaScript i TypeScript | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Zarządzane podstawowe obciążenie pulpitu | 15.0.26419.1 | Zalecane
Microsoft.VisualStudio.Component.NuGet | Menedżer pakietów NuGet | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.PortableLibrary | Biblioteka przenośna .NET targeting pack | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilatory języka C# i Visual Basic Roslyn | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# i Visual Basic | 15.0.26711.1 | Zalecane
Microsoft.VisualStudio.Component.SQL.ADAL | Środowisko uruchomieniowe programu SQL ADAL | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.SQL.CLR | Typy danych CLR dla programu SQL Server | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.SQL.CMDUtils | Narzędzia wiersza polecenia programu SQL Server | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.SQL.DataSources | Obsługuje źródeł danych dla programu SQL Server | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | Program SQL Server Express 2016 LocalDB | 15.0.26919.1 | Zalecane
Microsoft.VisualStudio.Component.SQL.NCLI | SQL Server Native Client | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Data Tools | 15.0.26906.1 | Zalecane
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Narzędzia do analizy statycznej | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.TextTemplating | Transformacji szablonu tekstowego | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.TypeScript.2.3 | TypeScript 2.3 zestawu SDK | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.VisualStudioData | Źródła danych i odwołania do usług | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.Wcf.Tooling | Windows Communication Foundation | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.Web | Narzędzia deweloperskie ASP.NET i sieć web | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.ComponentGroup.Web | Narzędzia deweloperskie ASP.NET i sieć web | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET i sieć web development | 15.0.26606.0 | Zalecane
Microsoft.Net.Component.4.6.2.SDK | .NET framework 4.6.2 zestawu SDK | 15.0.26208.0 | Optional
Microsoft.Net.Component.4.6.2.TargetingPack | .NET framework 4.6.2 docelowego pakietu | 15.0.26208.0 | Optional
Microsoft.Net.Component.4.7.SDK | .NET framework 4.7 zestawu SDK | 15.0.26419.1 | Optional
Microsoft.Net.Component.4.7.TargetingPack | .NET framework 4.7 targeting pack | 15.0.26621.2 | Optional
Microsoft.Net.ComponentGroup.4.6.2.DeveloperTools | Narzędzia do programowania .NET framework 4.6.2 | 15.0.26621.2 | Optional
Microsoft.Net.ComponentGroup.4.7.DeveloperTools | Narzędzia do programowania .NET framework 4.7 | 15.0.26606.0 | Optional
Microsoft.Net.Core.Component.SDK.1x | Oprogramowanie .NET core narzędzi programistycznych 1.0 1.1 dla komputerów typu Desktop | 15.0.26919.1 | Optional
Microsoft.NetCore.1x.ComponentGroup.Web | Oprogramowanie .NET core narzędzi programistycznych 1.0 1.1 dla sieci Web | 15.0.26919.1 | Optional
Microsoft.VisualStudio.Component.FSharp | Obsługa języka F # | 15.0.26606.0 | Optional
Microsoft.VisualStudio.ComponentGroup.IISDevelopment | Programowanie czasu obsługi usług IIS | 15.0.26720.2 | Optional
Microsoft.VisualStudio.Web.Mvc4.ComponentGroup | ASP.NET MVC 4 | 15.0.26606.0 | Optional


## <a name="nodejs-development"></a>Programowanie node.js

**Identyfikator:** Microsoft.VisualStudio.Workload.Node

**Opis:** tworzyć aplikacje skalowalne sieci przy użyciu środowiska Node.js, asynchroniczne sterowane zdarzeniami środowiska wykonawczego języka JavaScript.

### <a name="components-included-by-this-workload"></a>Składniki przez to obciążenie

Identyfikator składnika | Nazwa | Wersja | Typ zależności
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Usługi językowe razor | 15.0.26720.2 | Wymagane
Component.WebSocket | WebSocket4Net | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | Diagnostyka JavaScript | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.JavaScript.TypeScript | Obsługa języka JavaScript i TypeScript | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.Node.Tools | Obsługa środowiska node.js | 15.0.26823.1 | Wymagane
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilatory języka C# i Visual Basic Roslyn | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# i Visual Basic | 15.0.26711.1 | Wymagane
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Narzędzia do analizy statycznej | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.TypeScript.2.3 | TypeScript 2.3 zestawu SDK | 15.0.26621.2 | Wymagane
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET i sieć web development | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.Common.Azure.Tools | Narzędzia łączności i publikowanie | 1.10.50614.2 | Zalecane
Microsoft.VisualStudio.Component.Git | Git dla systemu Windows | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.AppInsights.Tools | Narzędzia Developer Analytics tools | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.DiagnosticTools | Narzędzia profilowania platformy .NET | 15.0.26711.1 | Optional
Microsoft.VisualStudio.Component.VC.CoreIde | Visual Studio C++ podstawowe funkcje | 15.0.26606.0 | Optional
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | Zestaw narzędzi v141 2017 VC ++ (x86, x64) | 15.0.26823.1 | Optional


## <a name="officesharepoint-development"></a>Programowanie Office i SharePoint

**Identyfikator:** Microsoft.VisualStudio.Workload.Office

**Opis:** dodatków VSTO dodatki Tworzenie pakietu Office i programu SharePoint oraz rozwiązań programu SharePoint przy użyciu języka C#, VB i JavaScript.

### <a name="components-included-by-this-workload"></a>Składniki przez to obciążenie

Identyfikator składnika | Nazwa | Wersja | Typ zależności
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Usługi językowe razor | 15.0.26720.2 | Wymagane
Component.WebSocket | WebSocket4Net | 15.0.26606.0 | Wymagane
Microsoft.Component.ClickOnce | Publikowanie ClickOnce | 15.0.26919.1 | Wymagane
Microsoft.Component.MSBuild | MSBuild | 15.0.26208.0 | Wymagane
Microsoft.Net.Component.4.5.2.TargetingPack | Pakiet określania wartości docelowej platformy .NET framework 4.5.2 | 15.0.26621.2 | Wymagane
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 15.0.26621.2 | Wymagane
Microsoft.Net.Component.4.6.1.SDK | .NET framework 4.6.1 zestawu SDK | 15.0.26621.2 | Wymagane
Microsoft.Net.Component.4.6.1.TargetingPack | Pakiet określania wartości docelowej platformy .NET framework 4.6.1 | 15.0.26621.2 | Wymagane
Microsoft.Net.Component.4.TargetingPack | .NET framework 4 targeting pack | 15.0.26621.2 | Wymagane
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | Narzędzia do programowania .NET framework 4.6.1 | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.AppInsights.Tools | Narzędzia Developer Analytics tools | 15.0.26621.2 | Wymagane
Microsoft.VisualStudio.Component.Common.Azure.Tools | Narzędzia łączności i publikowanie | 1.10.50614.2 | Wymagane
Microsoft.VisualStudio.Component.Debugger.JustInTime | Debuger Just In Time | 15.0.26823.1 | Wymagane
Microsoft.VisualStudio.Component.IISExpress | Usługi IIS Express  | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | Diagnostyka JavaScript | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.JavaScript.TypeScript | Obsługa języka JavaScript i TypeScript | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Zarządzane podstawowe obciążenie pulpitu | 15.0.26419.1 | Wymagane
Microsoft.VisualStudio.Component.ManagedDesktop.Prerequisites | Narzędzia do tworzenia klasycznych aplikacji .NET | 15.0.26906.1 | Wymagane
Microsoft.VisualStudio.Component.NuGet | Menedżer pakietów NuGet | 15.0.26621.2 | Wymagane
Microsoft.VisualStudio.Component.PortableLibrary | Biblioteka przenośna .NET targeting pack | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilatory języka C# i Visual Basic Roslyn | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# i Visual Basic | 15.0.26711.1 | Wymagane
Microsoft.VisualStudio.Component.Sharepoint.Tools | Office Developer Tools for Visual Studio | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.SQL.ADAL | Środowisko uruchomieniowe programu SQL ADAL | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.SQL.CLR | Typy danych CLR dla programu SQL Server | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.SQL.CMDUtils | Narzędzia wiersza polecenia programu SQL Server | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.SQL.DataSources | Obsługuje źródeł danych dla programu SQL Server | 15.0.26621.2 | Wymagane
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | Program SQL Server Express 2016 LocalDB | 15.0.26919.1 | Wymagane
Microsoft.VisualStudio.Component.SQL.NCLI | SQL Server Native Client | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Data Tools | 15.0.26906.1 | Wymagane
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Narzędzia do analizy statycznej | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.TextTemplating | Transformacji szablonu tekstowego | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.TypeScript.2.3 | TypeScript 2.3 zestawu SDK | 15.0.26621.2 | Wymagane
Microsoft.VisualStudio.Component.VisualStudioData | Źródła danych i odwołania do usług | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.Wcf.Tooling | Windows Communication Foundation | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.Web | Narzędzia deweloperskie ASP.NET i sieć web | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.Workflow | Windows Workflow Foundation | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.ComponentGroup.Web | Narzędzia deweloperskie ASP.NET i sieć web | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET i sieć web development | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.TeamOffice | Visual Studio Tools dla pakietu Office (środowisko VSTO) | 15.0.26606.0 | Zalecane


## <a name="python-development"></a>Tworzenie Python

**Identyfikator:** Microsoft.VisualStudio.Workload.Python

**Opis:** edytowanie, debugowanie, sterowania interaktywnego rozwoju i źródła dla języka Python.

### <a name="components-included-by-this-workload"></a>Składniki przez to obciążenie

Identyfikator składnika | Nazwa | Wersja | Typ zależności
--- | --- | --- | ---
Component.CPython3.x64 | Python 3 64-bitowych (3.6.2) | 3.6.2 | Zalecane
Component.Microsoft.VisualStudio.RazorExtension | Usługi językowe razor | 15.0.26720.2 | Zalecane
Microsoft.Component.CookiecutterTools | Obsługa szablonów Cookiecutter | 15.0.26621.2 | Zalecane
Microsoft.Component.PythonTools | Obsługa języka Python | 15.0.26823.1 | Zalecane
Microsoft.Component.PythonTools.Web | Obsługa sieci web języka Python | 15.0.26606.0 | Zalecane
Microsoft.Component.VC.Runtime.UCRTSDK | Zestaw Windows Universal CRT SDK | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.Common.Azure.Tools | Narzędzia łączności i publikowanie | 1.10.50614.2 | Zalecane
Microsoft.VisualStudio.Component.JavaScript.TypeScript | Obsługa języka JavaScript i TypeScript | 15.0.26606.0 | Zalecane
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilatory języka C# i Visual Basic Roslyn | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# i Visual Basic | 15.0.26711.1 | Zalecane
Microsoft.VisualStudio.Component.SQL.CLR | Typy danych CLR dla programu SQL Server | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Narzędzia do analizy statycznej | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.TypeScript.2.3 | TypeScript 2.3 zestawu SDK | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.VisualStudioData | Źródła danych i odwołania do usług | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.Component.Windows81SDK | Zestaw SDK systemu Windows 8.1 | 15.0.26208.0 | Zalecane
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET i sieć web development | 15.0.26606.0 | Zalecane
Component.Anaconda2.x64 | Anaconda2 64-bitowych (4.4.0) | 4.4.0 | Optional
Component.Anaconda2.x86 | Anaconda2 32-bitowych (4.4.0) | 4.4.0 | Optional
Component.Anaconda3.x64 | Anaconda3 64-bitowych (4.4.0) | 4.4.0 | Optional
Component.Anaconda3.x86 | Anaconda3 32-bitowych (4.4.0) | 4.4.0 | Optional
Component.CPython2.x64 | Python 2 64-bitowych (2.7.13) | 2.7.13 | Optional
Component.CPython2.x86 | Python 2 32-bitowych (2.7.13) | 2.7.13 | Optional
Component.CPython3.x86 | Python 3 32-bitowych (3.6.2) | 3.6.2 | Optional
Component.WebSocket | WebSocket4Net | 15.0.26606.0 | Optional
Microsoft.Component.ClickOnce | Publikowanie ClickOnce | 15.0.26919.1 | Optional
Microsoft.Component.MSBuild | MSBuild | 15.0.26208.0 | Optional
Microsoft.Component.NetFX.Native | Architektura .NET Native | 15.0.26208.0 | Optional
Microsoft.Component.PythonTools.UWP | Obsługa języka Python IoT | 15.0.26606.0 | Optional
Microsoft.ComponentGroup.PythonTools.NativeDevelopment | Narzędzia deweloperskie macierzystego języka Python | 15.0.27004.2002 | Optional
Microsoft.Net.Component.4.5.1.TargetingPack | Pakiet docelowy .NET framework 4.5.1 | 15.0.26621.2 | Optional
Microsoft.Net.Component.4.5.2.TargetingPack | Pakiet określania wartości docelowej platformy .NET framework 4.5.2 | 15.0.26621.2 | Optional
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 15.0.26621.2 | Optional
Microsoft.Net.Component.4.6.1.SDK | .NET framework 4.6.1 zestawu SDK | 15.0.26621.2 | Optional
Microsoft.Net.Component.4.6.1.TargetingPack | Pakiet określania wartości docelowej platformy .NET framework 4.6.1 | 15.0.26621.2 | Optional
Microsoft.Net.Component.4.6.TargetingPack | .NET framework 4.6 targeting pack | 15.0.26621.2 | Optional
Microsoft.Net.Component.4.TargetingPack | .NET framework 4 targeting pack | 15.0.26621.2 | Optional
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | Narzędzia do programowania .NET framework 4.6.1 | 15.0.26606.0 | Optional
Microsoft.Net.ComponentGroup.TargetingPacks.Common | Narzędzia deweloperskie programu .NET framework 4 — 4.6 | 15.0.26606.0 | Optional
Microsoft.VisualStudio.Component.AppInsights.Tools | Narzędzia Developer Analytics tools | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Azure Authoring Tools | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.Azure.ClientLibs | Biblioteki Azure dla platformy .NET | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Emulator obliczeń platformy Azure | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Emulator usługi Azure Storage | 15.0.26823.1 | Optional
Microsoft.VisualStudio.Component.Azure.Waverton | Azure podstawowe narzędzia usługi w chmurze | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.ClassDesigner | Projektant klas | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.DiagnosticTools | Narzędzia profilowania platformy .NET | 15.0.26711.1 | Optional
Microsoft.VisualStudio.Component.Graphics | Edytory modelu obrazu i 3W | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.Graphics.Tools | Grafika debugera i profilera procesora GPU programu DirectX | 15.0.26823.1 | Optional
Microsoft.VisualStudio.Component.Graphics.Win81 | Grafika narzędzi Windows 8.1 SDK | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.IISExpress | Usługi IIS Express  | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | Diagnostyka JavaScript | 15.0.26606.0 | Optional
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Zarządzane podstawowe obciążenie pulpitu | 15.0.26419.1 | Optional
Microsoft.VisualStudio.Component.NuGet | Menedżer pakietów NuGet | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.PortableLibrary | Biblioteka przenośna .NET targeting pack | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.SQL.ADAL | Środowisko uruchomieniowe programu SQL ADAL | 15.0.26606.0 | Optional
Microsoft.VisualStudio.Component.SQL.CMDUtils | Narzędzia wiersza polecenia programu SQL Server | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.SQL.DataSources | Obsługuje źródeł danych dla programu SQL Server | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | Program SQL Server Express 2016 LocalDB | 15.0.26919.1 | Optional
Microsoft.VisualStudio.Component.SQL.NCLI | SQL Server Native Client | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Data Tools | 15.0.26906.1 | Optional
Microsoft.VisualStudio.Component.TextTemplating | Transformacji szablonu tekstowego | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.VC.140 | Zestaw narzędzi w wersji 140 2015.3 VC ++ dla komputerów typu desktop (x86, x64) | 15.0.26720.2 | Optional
Microsoft.VisualStudio.Component.VC.CoreIde | Visual Studio C++ podstawowe funkcje | 15.0.26606.0 | Optional
Microsoft.VisualStudio.Component.VC.DiagnosticTools | Narzędzia profilowania C++ | 15.0.26823.1 | Optional
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | Zestaw narzędzi v141 2017 VC ++ (x86, x64) | 15.0.26823.1 | Optional
Microsoft.VisualStudio.Component.Web | Narzędzia deweloperskie ASP.NET i sieć web | 15.0.26606.0 | Optional
Microsoft.VisualStudio.Component.Windows10SDK | Środowisko wykonawcze systemu Windows Universal C | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.10586 | Windows 10 SDK (10.0.10586.0) | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.16299.Desktop | Windows 10 SDK (10.0.16299.0) dla pulpitu C++ [x86 i x64] | 15.0.27004.2002 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP | Windows 10 SDK (10.0.16299.0) dla platformy uniwersalnej systemu Windows: C#, VB, JS | 15.0.27004.2002 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP.Native | Windows 10 SDK (10.0.16299.0) dla platformy uniwersalnej systemu Windows: C++ | 15.0.27004.2002 | Optional
Microsoft.VisualStudio.ComponentGroup.Web | Narzędzia deweloperskie ASP.NET i sieć web | 15.0.26606.0 | Optional


## <a name="universal-windows-platform-development"></a>Tworzenie uniwersalnych platformy systemu Windows

**Identyfikator:** Microsoft.VisualStudio.Workload.Universal

**Opis:** tworzenie aplikacji dla platformy uniwersalnej systemu Windows za pomocą języka C#, VB, JavaScript i opcjonalnie C++.

### <a name="components-included-by-this-workload"></a>Składniki przez to obciążenie

Identyfikator składnika | Nazwa | Wersja | Typ zależności
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Usługi językowe razor | 15.0.26720.2 | Wymagane
Component.WebSocket | WebSocket4Net | 15.0.26606.0 | Wymagane
Microsoft.Component.ClickOnce | Publikowanie ClickOnce | 15.0.26919.1 | Wymagane
Microsoft.Component.NetFX.Native | Architektura .NET Native | 15.0.26208.0 | Wymagane
Microsoft.ComponentGroup.Blend | Blend for Visual Studio | 15.0.26711.1 | Wymagane
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 15.0.26621.2 | Wymagane
Microsoft.Net.Component.4.6.1.SDK | .NET framework 4.6.1 zestawu SDK | 15.0.26621.2 | Wymagane
Microsoft.VisualStudio.Component.AppInsights.Tools | Narzędzia Developer Analytics tools | 15.0.26621.2 | Wymagane
Microsoft.VisualStudio.Component.DiagnosticTools | Narzędzia profilowania platformy .NET | 15.0.26711.1 | Wymagane
Microsoft.VisualStudio.Component.Graphics | Edytory modelu obrazu i 3W | 15.0.26621.2 | Wymagane
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | Diagnostyka JavaScript | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.JavaScript.TypeScript | Obsługa języka JavaScript i TypeScript | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.NuGet | Menedżer pakietów NuGet | 15.0.26621.2 | Wymagane
Microsoft.VisualStudio.Component.PortableLibrary | Biblioteka przenośna .NET targeting pack | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilatory języka C# i Visual Basic Roslyn | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# i Visual Basic | 15.0.26711.1 | Wymagane
Microsoft.VisualStudio.Component.SQL.CLR | Typy danych CLR dla programu SQL Server | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Narzędzia do analizy statycznej | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.TypeScript.2.3 | TypeScript 2.3 zestawu SDK | 15.0.26621.2 | Wymagane
Microsoft.VisualStudio.Component.UWP.Support | Narzędzia do uniwersalnych platformy systemu Windows | 15.0.26906.1 | Wymagane
Microsoft.VisualStudio.Component.VisualStudioData | Źródła danych i odwołania do usług | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP | Windows 10 SDK (10.0.16299.0) dla platformy uniwersalnej systemu Windows: C#, VB, JS | 15.0.27004.2002 | Wymagane
Microsoft.VisualStudio.ComponentGroup.UWP.Cordova | Narzędzia uniwersalnych platformy systemu Windows dla oprogramowania Cordova | 15.0.27004.2002 | Wymagane
Microsoft.VisualStudio.ComponentGroup.UWP.Xamarin | Narzędzia uniwersalnych platformy systemu Windows dla platformy Xamarin | 15.0.27004.2002 | Wymagane
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET i sieć web development | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.Windows10SDK.15063.UWP | Windows 10 SDK (10.0.15063.0) dla platformy uniwersalnej systemu Windows: C#, VB, JS | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.Component.Windows10SDK.15063.UWP.Native | Windows 10 SDK (10.0.15063.0) dla platformy uniwersalnej systemu Windows: C++ | 15.0.26621.2 | Zalecane
Microsoft.VisualStudio.ComponentGroup.Win10SDK_10.0.15063.UWP.All | Windows 10 SDK (10.0.15063.0) dla platformy uniwersalnej systemu Windows | 15.0.27004.2002 | Zalecane
Microsoft.Component.VC.Runtime.OSSupport | Środowiska uruchomieniowego Visual C++ dla platformy uniwersalnej systemu Windows | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.Graphics.Tools | Grafika debugera i profilera procesora GPU programu DirectX | 15.0.26823.1 | Optional
Microsoft.VisualStudio.Component.Graphics.Win81 | Grafika narzędzi Windows 8.1 SDK | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.Phone.Emulator.15063 | Emulatorze przenośnym z systemem Windows 10 (twórców aktualizacja) | 15.0.26711.1 | Optional
Microsoft.VisualStudio.Component.VC.CoreIde | Visual Studio C++ podstawowe funkcje | 15.0.26606.0 | Optional
Microsoft.VisualStudio.Component.VC.Tools.ARM | Kompilatory w programie Visual C++ i bibliotek dla ARM | 15.0.26906.1 | Optional
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | Zestaw narzędzi v141 2017 VC ++ (x86, x64) | 15.0.26823.1 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.10240 | Windows 10 SDK (10.0.10240.0) | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.10586 | Windows 10 SDK (10.0.10586.0) | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.14393 | Windows 10 SDK (10.0.14393.0) | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP.Native | Windows 10 SDK (10.0.16299.0) dla platformy uniwersalnej systemu Windows: C++ | 15.0.27004.2002 | Optional
Microsoft.VisualStudio.ComponentGroup.UWP.VC | Narzędzia platformy uniwersalnej systemu Windows C++ | 15.0.27004.2002 | Optional


## <a name="visual-studio-extension-development"></a>Programowanie rozszerzenia usługi Visual Studio

**Identyfikator:** Microsoft.VisualStudio.Workload.VisualStudioExtension

**Opis:** Utwórz dodatki i rozszerzenia programu Visual Studio, w tym nowe polecenia kodu analizatory i narzędzia systemu windows.

### <a name="components-included-by-this-workload"></a>Składniki przez to obciążenie

Identyfikator składnika | Nazwa | Wersja | Typ zależności
--- | --- | --- | ---
Microsoft.Component.ClickOnce | Publikowanie ClickOnce | 15.0.26919.1 | Wymagane
Microsoft.Net.Component.4.6.1.SDK | .NET framework 4.6.1 zestawu SDK | 15.0.26621.2 | Wymagane
Microsoft.Net.Component.4.6.1.TargetingPack | Pakiet określania wartości docelowej platformy .NET framework 4.6.1 | 15.0.26621.2 | Wymagane
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | Narzędzia do programowania .NET framework 4.6.1 | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.PortableLibrary | Biblioteka przenośna .NET targeting pack | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.ComponentGroup.VisualStudioExtension.Prerequisites | Wymagania wstępne programu Visual Studio rozszerzenia programowanie | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.DiagnosticTools | Narzędzia profilowania platformy .NET | 15.0.26711.1 | Zalecane
Component.Dotfuscator | Ochrona cenią sobie wcześniejsze — Dotfuscator | 15.0.26208.0 | Optional
Microsoft.Component.MSBuild | MSBuild | 15.0.26208.0 | Optional
Microsoft.Component.VC.Runtime.OSSupport | Środowiska uruchomieniowego Visual C++ dla platformy uniwersalnej systemu Windows | 15.0.26621.2 | Optional
Microsoft.Net.Component.4.6.TargetingPack | .NET framework 4.6 targeting pack | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.AppInsights.Tools | Narzędzia Developer Analytics tools | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.ClassDesigner | Projektant klas | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.DslTools | Modelowanie zestawu SDK | 15.0.26711.1 | Optional
Microsoft.VisualStudio.Component.NuGet | Menedżer pakietów NuGet | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilatory języka C# i Visual Basic Roslyn | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# i Visual Basic | 15.0.26711.1 | Optional
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Narzędzia do analizy statycznej | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.TextTemplating | Transformacji szablonu tekstowego | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.VC.ATL | Visual C++ ATL — Obsługa | 15.0.26823.1 | Optional
Microsoft.VisualStudio.Component.VC.ATLMFC | Obsługa MFC i ATL (x86 i x64) | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.VC.CoreIde | Visual Studio C++ podstawowe funkcje | 15.0.26606.0 | Optional
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | Zestaw narzędzi v141 2017 VC ++ (x86, x64) | 15.0.26823.1 | Optional
Microsoft.VisualStudio.Component.VSSDK | Visual Studio SDK | 15.0.26919.1 | Optional


## <a name="mobile-development-with-javascript"></a>Tworzenie przenośnych za pomocą języka JavaScript

**Identyfikator:** Microsoft.VisualStudio.Workload.WebCrossPlat

**Opis:** tworzenie aplikacji systemu Android, iOS i platformy uniwersalnej systemu Windows za pomocą narzędzi dla oprogramowania Apache Cordova.

### <a name="components-included-by-this-workload"></a>Składniki przez to obciążenie

Identyfikator składnika | Nazwa | Wersja | Typ zależności
--- | --- | --- | ---
Component.CordovaToolset.6.3.1 | Zestaw narzędzi oprogramowania Cordova 6.3.1 | 15.0.26504.0 | Wymagane
Component.Microsoft.VisualStudio.RazorExtension | Usługi językowe razor | 15.0.26720.2 | Wymagane
Component.WebSocket | WebSocket4Net | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.Cordova | Tworzenie przenośnych za pomocą języka JavaScript podstawowe funkcje | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | Diagnostyka JavaScript | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.JavaScript.ProjectSystem | JavaScript ProjectSystem i narzędzia udostępnionego | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.JavaScript.TypeScript | Obsługa języka JavaScript i TypeScript | 15.0.26606.0 | Wymagane
Microsoft.VisualStudio.Component.Roslyn.Compiler | Kompilatory języka C# i Visual Basic Roslyn | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# i Visual Basic | 15.0.26711.1 | Wymagane
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Narzędzia do analizy statycznej | 15.0.26208.0 | Wymagane
Microsoft.VisualStudio.Component.TypeScript.2.3 | TypeScript 2.3 zestawu SDK | 15.0.26621.2 | Wymagane
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET i sieć web development | 15.0.26606.0 | Wymagane
Component.Android.SDK23.Private | Instalacja zestawu SDK systemu android (interfejs API na poziomie 23) (lokalnej instalacji) | 15.0.26906.1 | Optional
Component.Google.Android.Emulator.API23.Private | Emulator systemu Google Android (interfejs API poziomie 23) (instalacji lokalnej) | 15.0.26906.1 | Optional
Component.HAXM.Private | Intel sprzętu przyspieszyć wykonywanie Menedżera (HAXM) (lokalnej instalacji) | 15.0.26919.1 | Optional
Component.JavaJDK | Zestaw Java SE Development Kit (8.0.1120.15) | 15.0.26403.0 | Optional
Microsoft.Component.ClickOnce | Publikowanie ClickOnce | 15.0.26919.1 | Optional
Microsoft.Component.NetFX.Native | Architektura .NET Native | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.AppInsights.Tools | Narzędzia Developer Analytics tools | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.DiagnosticTools | Narzędzia profilowania platformy .NET | 15.0.26711.1 | Optional
Microsoft.VisualStudio.Component.Git | Git dla systemu Windows | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.Graphics | Edytory modelu obrazu i 3W | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.Phone.Emulator.15063 | Emulatorze przenośnym z systemem Windows 10 (twórców aktualizacja) | 15.0.26711.1 | Optional
Microsoft.VisualStudio.Component.SQL.CLR | Typy danych CLR dla programu SQL Server | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.VisualStudioData | Źródła danych i odwołania do usług | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP | Windows 10 SDK (10.0.16299.0) dla platformy uniwersalnej systemu Windows: C#, VB, JS | 15.0.27004.2002 | Optional
Microsoft.VisualStudio.ComponentGroup.UWP.Cordova | Narzędzia uniwersalnych platformy systemu Windows dla oprogramowania Cordova | 15.0.27004.2002 | Optional


## <a name="unaffiliated-components"></a>Odłączony składników

Są to składniki, które nie są dołączone każde obciążenie, ale można wybrać jako poszczególnych składników.

Identyfikator składnika | Nazwa | Wersja
--- | --- | ---
Component.Android.Emulator | Emulator programu Visual Studio dla systemu Android | 15.0.26711.1
Component.Android.NDK.R11C | Zestawu NDK systemu android (R11C) | 11.3.13
Component.Android.NDK.R11C_3264 | Zestawu NDK systemu android (R11C) (32-bitowe) | 11.3.15
Component.GitHub.VisualStudio | Rozszerzenie GitHub dla programu Visual Studio | 2.2.0.10
Microsoft.Component.Blend.SDK.WPF | Program Blend for Visual Studio SDK dla platformy .NET | 15.0.26929.2
Microsoft.Component.HelpViewer | Podgląd pomocy | 15.0.26711.1
Microsoft.VisualStudio.Component.DependencyValidation.Community | Sprawdzanie poprawności zależności | 15.0.26208.0
Microsoft.VisualStudio.Component.GraphDocument | Edytor DGML | 15.0.26906.1
Microsoft.VisualStudio.Component.LinqToSql | LINQ do SQL narzędzia | 15.0.26208.0
Microsoft.VisualStudio.Component.Phone.Emulator | Emulatorze przenośnym z systemem Windows 10 (Anniversary Edition) | 15.0.26711.1
Microsoft.VisualStudio.Component.TestTools.Core | Funkcje podstawowe narzędzia do testowania | 15.0.26606.0
Microsoft.VisualStudio.Component.TypeScript.2.0 | TypeScript 2.0 SDK | 15.0.26504.0
Microsoft.VisualStudio.Component.TypeScript.2.1 | TypeScript 2.1 zestawu SDK | 15.0.26208.0
Microsoft.VisualStudio.Component.TypeScript.2.2 | TypeScript 2.2 zestawu SDK | 15.0.26504.0
Microsoft.VisualStudio.Component.VC.Tools.ARM64 | Kompilatory w programie Visual C++ i bibliotek dla ARM64 | 15.0.26906.1
Microsoft.VisualStudio.Component.Windows10SDK.16299.Desktop.arm | Windows 10 SDK (10.0.16299.0) dla pulpitu C++ [ARM i ARM64] | 15.0.27004.2002

## <a name="get-support"></a>Uzyskaj pomoc techniczną
Czasami może wystąpienia problemów. W przypadku niepowodzenia instalacji programu Visual Studio, zobacz [problemy dotyczące instalacji i uaktualniania Rozwiązywanie problemów z programu Visual Studio 2017](troubleshooting-installation-issues.md) stronę porady dotyczące rozwiązywania problemów. Jak również zgłosić problemy produktu z nami za pośrednictwem [zgłosić Problem](../ide/how-to-report-a-problem-with-visual-studio-2017.md) narzędzia w programie Visual Studio IDE lub udział sugestia z nami na [UserVoice](https://visualstudio.uservoice.com/forums/121579). Można śledzić problemy z produktu w [Visual Studio Developer Community](https://developercommunity.visualstudio.com/), zadawać pytania i odpowiedzi. Można również kontaktowaniu się z nami i innymi deweloperami Visual Studio za pomocą naszych [konwersacji programu Visual Studio w społeczności Gitter](https://gitter.im/Microsoft/VisualStudio) (wymaga [GitHub](https://github.com/) konta).

## <a name="see-also"></a>Zobacz także

* [Visual Studio obciążenia i składnik identyfikatorów](workload-and-component-ids.md)
* [Przewodnik administratora w usłudze Visual Studio](visual-studio-administrator-guide.md)
* [Korzystanie z parametrów wiersza polecenia do zainstalowania programu Visual Studio](use-command-line-parameters-to-install-visual-studio.md)
  * [Przykłady parametru wiersza polecenia](command-line-parameter-examples.md)
* [Tworzenie w trybie offline instalację programu Visual Studio](create-an-offline-installation-of-visual-studio.md)