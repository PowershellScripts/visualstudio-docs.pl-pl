---
title: Obsługa ustawień użytkowników | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- Custom Settings Points
- user settings [Visual Studio SDK], registering persistence support
- persistence, registering settings
ms.assetid: ad9beac3-4f8d-4093-ad0e-6fb00444a709
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 8ea4d5bd890c28721539fa9528df72446fedc126
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49948996"
---
# <a name="support-for-user-settings"></a>Pomoc techniczna dotycząca ustawień użytkownika
Pakietu VSPackage może zdefiniować co najmniej jednej kategorii ustawienia, które są zmienne stanu, które utrzymują się, gdy użytkownik wybierze **importu/eksportu ustawień** polecenie **narzędzia** menu. Aby włączyć ten stan trwały, użyj ustawienia interfejsów API w [!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)].  

 Wpis rejestru, który jest określany jako punkt ustawienia niestandardowe i identyfikator GUID definiuje kategorię ustawień pakietu VSPackage. Pakietu VSPackage może obsługiwać wiele kategorii ustawienia, każdy zdefiniowany przez punkt ustawienia niestandardowe.  

-   Implementacje ustawienia, które są oparte na zestawy międzyoperacyjne (przy użyciu <xref:Microsoft.VisualStudio.Shell.Interop.IVsUserSettings> interfejsu) należy utworzyć niestandardowe ustawienia punktu przez edycję rejestru lub za pomocą skryptu rejestratora (pliku .rgs). Aby uzyskać więcej informacji, zobacz [tworzenie skryptów rejestratora](/cpp/atl/creating-registrar-scripts).  

-   Kod, który używa Framework pakietu zarządzanego (MPF) należy utworzyć niestandardowe ustawienia punktów, dołączając <xref:Microsoft.VisualStudio.Shell.ProvideProfileAttribute> do pakietu VSPackage dla każdego punktu ustawienia niestandardowe.  

     Jeśli jednego pakietu VSPackage obsługuje kilka punktów ustawienia niestandardowe, w każdym punkcie ustawienia niestandardowego jest implementowany przez osobnej klasy, a każdy zostanie zarejestrowany przez unikatowego wystąpienia <xref:Microsoft.VisualStudio.Shell.ProvideProfileAttribute> klasy. W związku z tym ustawienia z implementacji klasy może obsługiwać więcej niż jednej kategorii ustawień.  

## <a name="custom-settings-point-registry-entry-details"></a>Szczegóły wpisu rejestru punktu ustawień niestandardowych  
 Niestandardowe ustawienia punkty są tworzone we wpisie rejestru w następującej lokalizacji: HKLM\Software\Microsoft\VisualStudio\\*\<wersji >* \UserSettings\\`<CSPName>`, gdzie `<CSPName>` nazywa się punkt ustawienia niestandardowe obsługuje pakietu VSPackage i  *\<wersji >* jest wersją [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)], na przykład 8.0.  

> [!NOTE]
>  Ścieżka katalogu głównego HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\VisualStudio\\*\<wersji >* może zostać zastąpiona przez alternatywne główne, kiedy [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] jest zintegrowanym środowisku programistycznym (IDE) zainicjowane. Aby uzyskać więcej informacji, zobacz [przełączniki wiersza polecenia](../../extensibility/command-line-switches-visual-studio-sdk.md).  

 Poniżej przedstawiono strukturę wpis rejestru:  

 HKLM\Software\Microsoft\VisualStudio\\*\<wersji >* \UserSettings\  

 `<CSPName`> = "#12345" s  

 Pakiet = "{XXXXXX XXXX XXXX XXXX XXXXXXXXX}"  

 Kategoria = "{YYYY RRRRRR rrrr rrrr YYYYYYYYY}"  

 ResourcePackage = "{ZZZZZZ ZZZZ ZZZZ ZZZZ ZZZZZZZZZ}"  

 AlternateParent = CategoryName  


| Nazwa | Typ | Dane | Opis |
|-----------------|--------| - | - |
| (Domyślnie) | REG_SZ | Nazwa punktu ustawienia niestandardowe | Nazwy kluczy `<CSPName`>, nazywa się Niezlokalizowany punktu ustawienia niestandardowe.<br /><br /> W oparciu o MPF implementacji nazwy kluczy są uzyskiwane przez łączenie `categoryName` i `objectName` argumenty <xref:Microsoft.VisualStudio.Shell.ProvideProfileAttribute> konstruktora do `categoryName_objectName`.<br /><br /> Klucz może być pusta lub może on zawierać identyfikator odwołania do zlokalizowanych ciągów w towarzyszącej bibliotece DLL. Ta wartość jest uzyskiwana z `objectNameResourceID` argument <xref:Microsoft.VisualStudio.Shell.ProvideProfileAttribute> konstruktora. |
| Package | REG_SZ | Identyfikator GUID | Identyfikator GUID pakietu VSPackage, który implementuje punkt ustawienia niestandardowe.<br /><br /> Implementacje opierają się na użyciu MPF <xref:Microsoft.VisualStudio.Shell.ProvideProfileAttribute> klasy, należy użyć konstruktora `objectType` argument zawierający VSPackage <xref:System.Type> i odbicia, aby uzyskać tę wartość. |
| Kategoria | REG_SZ | Identyfikator GUID | Identyfikator GUID kategorii ustawień.<br /><br /> Implementacje, w oparciu o zestawy międzyoperacyjne, ta wartość może być dowolnie wybrany identyfikator GUID, który [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] IDE przekazuje do <xref:Microsoft.VisualStudio.Shell.Interop.IVsUserSettings.ExportSettings%2A> i <xref:Microsoft.VisualStudio.Shell.Interop.IVsUserSettings.ImportSettings%2A> metody. Wszystkich implementacjach te dwie metody, należy sprawdzić ich argumentów identyfikatora GUID.<br /><br /> W oparciu o MPF implementacji tego identyfikatora GUID jest uzyskiwana przez <xref:System.Type> implementacji klasy [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] mechanizm ustawienia. |
| ResourcePackage | REG_SZ | Identyfikator GUID | Opcjonalna.<br /><br /> Ścieżka do satelitarne biblioteki DLL zawierających zlokalizowanych ciągów Jeśli implementującej pakietu VSPackage nie dostarcza je.<br /><br /> MPF używa odbicia w celu uzyskania odpowiedniego zasobu pakietu VSPackage, więc <xref:Microsoft.VisualStudio.Shell.ProvideProfileAttribute> klasy nie ustawia tego argumentu. |
| AlternateParent | REG_SZ | Nazwa folderu, w obszarze strony Opcje narzędzi zawierające ten punkt ustawienia niestandardowe. | Opcjonalna.<br /><br /> Należy ustawić tę wartość, tylko wtedy, gdy implementacja ustawienia obsługuje **opcje narzędzi** stron korzystających z mechanizmu stanu trwałego w [!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)] zamiast mechanizmu w modelu automatyzacji, który ma być zapisany stan.<br /><br /> W takich przypadkach jest wartością w kluczu AlternateParent `topic` części `topic.sub-topic` ciąg używany do identyfikowania danej **ToolsOptions** strony. Na przykład w przypadku **ToolsOptions** strony `"TextEditor.Basic"` wartość AlternateParent będzie `"TextEditor"`.<br /><br /> Gdy <xref:Microsoft.VisualStudio.Shell.ProvideProfileAttribute> generuje punkt ustawienia niestandardowe, jest taka sama jak nazwa kategorii. |

