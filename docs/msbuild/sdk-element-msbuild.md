---
title: Zestaw SDK, Element (MSBuild) | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 01/25/2018
ms.technology: msbuild
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#Project
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- Sdk element [MSBuild]
- <Sdk> element [MSBuild]
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 1069a22e700eebfd9d1e8c387af99cf4241ffbe0
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49834180"
---
# <a name="sdk-element-msbuild"></a>Zestaw SDK, element (MSBuild)
Odwołania [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] projekt zestawu SDK.  

 \<Project>  
 \<Sdk>  


## <a name="syntax"></a>Składnia  

```xml  
<Sdk Name="My.Custom.Sdk"
     Version="1.0.0" />  
```  

## <a name="attributes-and-elements"></a>Atrybuty i elementy  
 W poniższych sekcjach opisano atrybuty, elementy podrzędne i elementy nadrzędne.  

### <a name="attributes"></a>Atrybuty  

|Atrybut|Opis|  
|---------------|-----------------|  
|`Name`|Atrybut wymagany.<br /><br /> Nazwa zestawu SDK projektu.|  
|`Version`|Atrybut opcjonalny.<br /><br /> Wersja zestawu SDK projektu|  

### <a name="child-elements"></a>Elementy podrzędne  
 Brak.

### <a name="parent-elements"></a>Elementy nadrzędne  

| Element | Opis |
| - | - |
| [Project](../msbuild/project-element-msbuild.md) | Element główny wymagany [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] pliku projektu. |

## <a name="see-also"></a>Zobacz także  
 [Porady: odwołanie do zestawu SDK projektu MSBuild](../msbuild/how-to-use-project-sdk.md)   
 [Odwołanie do schematu pliku projektu](../msbuild/msbuild-project-file-schema-reference.md)   
 [MSBuild](../msbuild/msbuild.md)
