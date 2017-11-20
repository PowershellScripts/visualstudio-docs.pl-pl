---
title: "Odwołanie do schematu VSCT XML | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- Visual Studio command table configuration files (VSCT), XML schema
- VSCT XML schema elements
ms.assetid: 49e7efae-e713-4762-a824-96fdaf92cdc9
caps.latest.revision: "14"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 1fc82041f8ab2790c63c271f85d573a3105ab8b0
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="vsct-xml-schema-reference"></a>Odwołanie do schematu VSCT XML
Zapewnia tabeli elementów schematu kompilatora tabeli polecenie podrzędne dozwolone elementy i atrybuty dla każdego.  
  
 Plik konfiguracji (vsct) tabeli polecenia opartych na języku XML definiuje elementy polecenia, które zawiera pakiet VSPackage zintegrowane środowisko programistyczne (IDE). Te elementy zawierają elementy menu, menu, paski narzędzi i pola kombi.  
  
> [!NOTE]
>  Kompilator VSCT można uruchomić preprocesora w pliku vsct. Ponieważ jest to zwykle obejmuje preprocesora, można zdefiniować C++ i makra, które mają tej samej składni, który jest używany w plikach C++. To przykłady znajdują się w vsct pliku **nowy projekt** Kreator tworzy dla projektu pakiet VSPackage.  
  
## <a name="optional-elements"></a>Elementy opcjonalne  
 Niektóre elementy VSCT są opcjonalne. Jeśli `Parent` argument nie zostanie określony, Group_Undefined:0 będzie niejawnego. Jeśli `Icon` argument nie zostanie określony, guidOfficeIcon:msotcidNoIcon będzie niejawnego. Jeśli klawisz skrótu jest zdefiniowana, emulacji, która jest zwykle używana, jest opcjonalne.  
  
 Elementy mapy bitowej może być osadzony w czasie kompilacji, określając lokalizację paska mapy bitowej w `href` argumentu. Paska mapy bitowej jest skopiowanych podczas scalania zamiast wyodrębniony z biblioteki DLL zasobów. Gdy `href` podany argument `usedList` argument staje się opcjonalne, a wszystkie gniazda w paska mapy bitowej są traktowane jako używane.  
  
 Wszystkie wartości identyfikatora GUID i identyfikator musi być zdefiniowany za pomocą nazwy symbolicznej. Te nazwy może być zdefiniowana w nagłówku plików lub w VSCT \<symbole > sekcji. Nazwy symbolicznej musi określać elementy lokalne, uwzględnione za pośrednictwem \<Include > elementy, lub odwołuje się \<Extern > elementów. Nazwa symboliczna zostaną zaimportowane z pliku nagłówka, określonego w \<Extern > elementu, jeśli wynika z prostego wzorca z #define wartość symbolu. Wartość może być inny symbol, pod warunkiem, że symbol został uprzednio zdefiniowany. Definicje GUID musi występować po format OLE albo C++. Wartości Identyfikatora może być cyfr dziesiętnych lub cyfr szesnastkowych, które są poprzedzone 0 x, jak pokazano w poniższych wierszach:  
  
-   {6D484634-E53D-4a2c-ADCB-55145C9362C8}  
  
-   {0x6d484634, 0xe53d, 0x4a2c, {0xad, 0xcb, 0x55, 0x14, 0x5c, 0x93, 0x62, 0xc8}}  
  
 Komentarze XML mogą być używane, ale mogą je odrzucić obustronne narzędzi graficznego interfejsu użytkownika (GUI). Zawartość \<adnotacji > elementy dotrą do aktualizować niezależnie od formatu.  
  
## <a name="schema-hierarchy"></a>Schemat hierarchii  
 Pliku vsct ma następujące główne elementy.  
  
 [CommandTable Element](../extensibility/commandtable-element.md)  
  
 [Extern — Element](../extensibility/extern-element.md)  
  
 [Umieść Element](../extensibility/include-element.md)  
  
 [Zdefiniuj Element](../extensibility/define-element.md)  
  
 [Element poleceń](../extensibility/commands-element.md)  
  
 [CommandPlacements Element](../extensibility/commandplacements-element.md)  
  
 [VisibilityConstraints Element](../extensibility/visibilityconstraints-element.md)  
  
 [Element powiązania klawiszy](../extensibility/keybindings-element.md)  
  
 [UsedCommands Element](../extensibility/usedcommands-element.md)  
  
 [Element nadrzędny](../extensibility/parent-element.md)  
  
 [Icon — Element](../extensibility/icon-element.md)  
  
 [Element ciągów](../extensibility/strings-element.md)  
  
 [Polecenie flagi elementu](../extensibility/command-flag-element.md)  
  
 [Element symboli](../extensibility/symbols-element.md)  
  
 [Atrybuty warunkowe](../extensibility/vsct-xml-schema-conditional-attributes.md)  
  
## <a name="see-also"></a>Zobacz też  
 [Jak VSPackages dodać elementy interfejsu użytkownika](../extensibility/internals/how-vspackages-add-user-interface-elements.md)   
 [Routing poleceń w VSPackages](../extensibility/internals/command-routing-in-vspackages.md)