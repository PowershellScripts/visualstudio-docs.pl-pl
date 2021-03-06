---
title: Rejestrowanie zleceń dla rozszerzeń nazw plików | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- verbs, registering
ms.assetid: 81a58e40-7cd0-4ef4-a475-c4e1e84d6e06
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: dd42bc89eb853a5d65f8e15eab3fdf2cd054f278
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49927804"
---
# <a name="register-verbs-for-file-name-extensions"></a>Rejestrowanie zleceń dla rozszerzeń nazw plików
Skojarzenie rozszerzenia nazwy pliku z aplikacją zazwyczaj ma preferowanego akcję, która występuje po dwukrotnym kliknięciu pliku. Preferowane to, że akcja jest połączony z czasownika, na przykład otwarty, która odnosi się do akcji.  
  
 Możesz zarejestrować zlecenia, które są skojarzone z identyfikator programowy (ProgID) dla rozszerzenia za pomocą klucza powłoki znajdujących się w **HKEY_CLASSES_ROOT\{progid} \shell**. Aby uzyskać więcej informacji, zobacz [typy plików](/windows/desktop/shell/fa-file-types).  
  
## <a name="register-standard-verbs"></a>Rejestrowanie zleceń standardowych  
 System operacyjny rozpoznaje następujących zleceń standardowych:  
  
- Otwarcie  
  
- Edytowanie  
  
- Odtwarzanie  
  
- Drukuj  
  
- Wersja zapoznawcza  
  
  Jeśli to możliwe, należy zarejestrować standardowy czasownika. Najbardziej typowe to Open zlecenie. Czasownik edycji należy użyć tylko wtedy, gdy istnieje wyraźna różnica pomiędzy otwierania pliku i edytowania pliku. Na przykład, otwierając *.htm* pliku wyświetla go w przeglądarce, natomiast edycji *.htm* rozpocznie edytora HTML. Zleceń standardowych są lokalizowane za pomocą ustawień regionalnych systemu operacyjnego.  
  
> [!NOTE]
>  Podczas rejestrowania zleceń standardowych, nie należy ustawiać wartość domyślna dla otworzyć klucza. Wartość domyślna zawiera ciąg wyświetlany w menu. System operacyjny dostarcza ten ciąg dla zleceń standardowych.  
  
 Pliki projektu powinien być zarejestrowany w Uruchom nowe wystąpienie klasy [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] po użytkownik otwiera plik. W poniższym przykładzie pokazano standardowy czasownika rejestracja [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] projektu.  
  
```  
[HKEY_CLASSES_ROOT\.csproj]  
@="VisualStudio.csproj.8.0"  
  
[HKEY_CLASSES_ROOT\.csproj\OpenWithList]  
[HKEY_CLASSES_ROOT\.csproj\OpenWithList\VSLauncher.exe]  
@=""  
  
[HKEY_CLASSES_ROOT\.csproj\OpenWithProgids]  
"VisualStudio.csproj.8.0"=""  
  
[HKEY_CLASSES_ROOT\Applications\VSLauncher.exe]  
[HKEY_CLASSES_ROOT\Applications\VSLauncher.exe\Shell]  
[HKEY_CLASSES_ROOT\Applications\VSLauncher.exe\Shell\Open]  
[HKEY_CLASSES_ROOT\Applications\VSLauncher.exe\Shell\Open\Command]  
@="C:\\Program Files\\Common Files\\Microsoft Shared\\MSEnv\\VSLauncher.exe \"%1\""  
  
[HKEY_CLASSES_ROOT\VisualStudio.csproj.8.0]  
@="C# Project file"  
  
[HKEY_CLASSES_ROOT\VisualStudio.csproj.8.0\DefaultIcon]  
@="C:\\VisualStudioPath\\VC#\\VCSPackages\\csproj.dll,0"  
  
[HKEY_CLASSES_ROOT\VisualStudio.csproj.8.0\shell]  
[HKEY_CLASSES_ROOT\VisualStudio.csproj.8.0\shell\Open]  
[HKEY_CLASSES_ROOT\VisualStudio.csproj.8.0\shell\Open\Command]  
@="\"C:\\Program Files\\Common Files\\Microsoft Shared\\MSEnv\\VSLauncher.exe\" \"%1\""  
```  
  
 Aby otworzyć plik w istniejącym wystąpieniu programu [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)], zarejestruj DDEEXEC klucza. W poniższym przykładzie pokazano standardowy czasownika rejestracja [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] *.cs* pliku.  
  
```  
[HKEY_CLASSES_ROOT\.cs]  
@="VisualStudio.cs.8.0"  
  
[HKEY_CLASSES_ROOT\.cs\OpenWithList]  
[HKEY_CLASSES_ROOT\.cs\OpenWithList\devenv.exe]  
@=""  
  
[HKEY_CLASSES_ROOT\.cs\OpenWithProgids]  
"VisualStudio.cs.8.0"=""  
  
[HKEY_CLASSES_ROOT\VisualStudio.cs.8.0]  
@="C# Source file"  
  
[HKEY_CLASSES_ROOT\VisualStudio.cs.8.0\DefaultIcon]  
@="C:\\VisualStudioPath\\VC#\\VCSPackages\\csproj.dll,1"  
  
[HKEY_CLASSES_ROOT\VisualStudio.cs.8.0\shell]  
[HKEY_CLASSES_ROOT\VisualStudio.cs.8.0\shell\Open]  
[HKEY_CLASSES_ROOT\VisualStudio.cs.8.0\shell\Open\Command]  
@="\"C:\\VisualStudioPath\\Common7\\IDE\\devenv.exe\" /dde \"%1\""  
  
[HKEY_CLASSES_ROOT\VisualStudio.cs.8.0\shell\Open\ddeexec]  
@="Open(\"%1\")"  
  
[HKEY_CLASSES_ROOT\VisualStudio.cs.8.0\shell\Open\ddeexec\Application]  
@="VisualStudio.8.0"  
  
[HKEY_CLASSES_ROOT\VisualStudio.cs.8.0\shell\Open\ddeexec\Topic]  
@="system"  
```  
  
## <a name="set-the-default-verb"></a>Ustaw zlecenie domyślne  
 Polecenie domyślne jest akcja, która jest wykonywana po dwukrotnym kliknięciu pliku w Eksploratorze Windows. Polecenie domyślne jest zlecenie, określony jako wartość domyślna dla **HKEY_CLASSES_ROOT\\*progid*\Shell** klucza. Jeśli wartość nie zostanie określona, polecenie domyślne jest określone w pierwszym zlecenie **HKEY_CLASSES_ROOT\\*progid*\Shell** listy kluczy.  
  
> [!NOTE]
>  Jeśli zamierzasz zmienić domyślne zlecenie rozszerzenia w ramach wdrożenia side-by-side, należy wziąć pod uwagę wpływ na instalacji i usuwania. Podczas instalacji zostanie zastąpiona oryginalna wartość domyślną.  
  
## <a name="see-also"></a>Zobacz także  
 [Zarządzaj skojarzeniami plików side-by-side](../extensibility/managing-side-by-side-file-associations.md)
