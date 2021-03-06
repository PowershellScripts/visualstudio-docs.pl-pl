---
title: '&lt;Pakiet&gt; — Element (program inicjujący) | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-deployment
ms.topic: conceptual
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- <package> element [bootstrapper]
ms.assetid: ecd06658-ad02-4440-bccd-88437b7fb816
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 49867ddc897a9c1a1241a891a3ba3de866d84688
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49899243"
---
# <a name="ltpackagegt-element-bootstrapper"></a>&lt;Pakiet&gt; — element (program inicjujący)
`Package` Element jest elementem XML najwyższego poziomu w pliku pakietu.  

## <a name="syntax"></a>Składnia  

```xml  
<Package  
    Culture  
    Name  
    LicenseAgreement  
>  
    <InstallChecks>  
        <AssemblyCheck   
            Property  
            Name  
            PublicKeyToken  
            Version  
            Language  
            ProcessorArchitecture  
        />  
        <RegistryCheck  
            Property  
            Key  
            Value  
        />  
        <ExternalCheck   
            PackageFile  
            Property  
            Arguments  
            Log  
        />  
        <FileCheck   
            Property  
            FileName  
            SearchPath  
            SpecialFolder  
            SearchDepth  
        />  
        <MsiProductCheck   
            Property  
            Product  
            Feature  
        />  
        <RegistryFileCheck   
            Property  
            Key  
            Value  
            File  
            SearchDepth  
        />  
    </InstallChecks>  

    <Commands  
        Reboot  
    >  
        <Command  
            PackageFile  
            Arguments  
            EstimatedInstallSeconds  
            EstimatedDiskBytes  
            EstimatedTempBytes  
            Log  
        >  
            <InstallConditions>  
                <BypassIf   
                    Property  
                    Compare  
                    Value  
                    Schedule  
                />  
                <FailIf   
                    Property  
                    Compare  
                    Value  
                    String  
                    Schedule  
                />  
            </InstallConditions>  
            <ExitCodes>  
                <ExitCode   
                    Value  
                    Result  
                    String  
                />  
            </ExitCodes>  
        </Command>  
    </Commands>  

    <PackageFiles  
        CopyAllComponents  
    >  
        <PackageFile   
            Name  
            Path  
            HomeSite  
            PublicKey  
        />  
    </PackageFiles>  

    <Strings>  
        <String  
            Name  
        >  
        </String>  
    </Strings>  

    <Schedules>  
        <Schedule  
            Name  
        >  
           <BuildList />  
           <BeforePackage />  
           <AfterPackage />  
        </Schedule>  
    </Schedules>  
</Package>  
```  

## <a name="elements-and-attributes"></a>Atrybuty i elementy  
 `Package` Element jest wymagany. Ma następujące atrybuty.  


| Atrybut | Opis |
|--------------------| - |
| `Culture` | Wymagana. Określa kulturę używaną do tego pakietu, która określa język, który ma być używany. Ten atrybut jest kluczem do `Strings` element, który wyświetla ciągi dla kultury dla nazw produktów i komunikaty o błędach podczas instalacji. |
| `Name` | Wymagana. Nazwa pakietu, takich jak wyświetlany dla deweloperów w narzędziu [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]. Ten atrybut jest kluczem do `Strings` element, który powinien zawierać `String` element z `Name` i `Culture` ustawić właściwości, aby dopasować `Name` i `Culture` właściwości `Package`. |
| `LicenseAgreement` | Opcjonalna. Określa nazwę pliku pakietu dystrybucji, który zawiera umowy licencyjnej użytkownika oprogramowania (EULA).  Ten plik może być zwykły tekst (*.txt*) lub w formacie. (*.rtf*) |

## <a name="example"></a>Przykład  
 Poniższy przykład kodu pokazuje plik kompletny pakiet dla redystrybucji [!INCLUDE[dnprdnlong](../code-quality/includes/dnprdnlong_md.md)].  

```xml  
<?xml version="1.0" encoding="utf-8" ?>  

<Package  
  xmlns="http://schemas.microsoft.com/developer/2004/01/bootstrapper"  
  Name="DisplayName"  
  Culture="Culture"  
  LicenseAgreement="eula.rtf"  
>  

    <PackageFiles>  
        <PackageFile Name="eula.rtf"/>  
    </PackageFiles>  

    <!-- Defines a localizable string table for error messages-->  
    <Strings>  
        <String Name="DisplayName">.NET Framework 2.0</String>  
        <String Name="Culture">en</String>  
        <String Name="AdminRequired">Administrator permissions are required to install the .NET Framework 2.0. Contact your administrator.</String>  
        <String Name="InvalidPlatformWin9x">Installation of the .NET Framework 2.0 is not supported on Windows 95. Contact your application vendor.</String>  
        <String Name="InvalidPlatformWinNT">Installation of the .NET Framework 2.0 is not supported on Windows NT 4.0. Contact your application vendor.</String>  
        <String Name="InvalidPlatformIE">Installation of the .NET Framework 2.0 requires Internet Explorer 5.01 or greater. Contact your application vendor.</String>  
        <String Name="InvalidPlatformArchitecture">This version of the .NET Framework 2.0 is not supported on a 64-bit operating system. Contact your application vendor.</String>  
        <String Name="WindowsInstallerImproperInstall">Due to an error with Windows Installer, the installation of the .NET Framework 2.0 cannot proceed.</String>  
        <String Name="AnotherInstanceRunning">Another instance of setup is already running. The running instance must complete before this setup can proceed.</String>  
        <String Name="BetaNDPFailure">A beta version of the .NET Framework was detected on the computer. Uninstall any previous beta versions of .NET Framework before continuing.</String>  
        <String Name="GeneralFailure">A failure occurred attempting to install the .NET Framework 2.0.</String>  
        <String Name="DotNetFXExe">http://go.microsoft.com/fwlink/?LinkId=37283</String>  
        <String Name="InstMsiAExe">http://go.microsoft.com/fwlink/?LinkId=37285</String>  
        <String Name="Msi30Exe">http://go.microsoft.com/fwlink/?LinkId=37287</String>  
    </Strings>  

</Package>  
```  

## <a name="see-also"></a>Zobacz także  
 [Odwołanie do schematu produktu i pakietu](../deployment/product-and-package-schema-reference.md)