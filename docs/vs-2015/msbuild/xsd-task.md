---
title: XSD — zadanie | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vc.task.xsd
- VC.Project.VCXMLDataGeneratorTool.Namespace
- VC.Project.VCXMLDataGeneratorTool.GenerateFromSchema
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- XSD task (MSBuild (Visual C++))
- MSBuild (Visual C++), XSD task
ms.assetid: 15c99f5c-7124-4bbc-bc03-70c7bcce8893
caps.latest.revision: 16
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: cd1aed6537d4fb49bafa34ce09dcb191c9475357
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49182640"
---
# <a name="xsd-task"></a>XSD — Zadanie
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Opakowuje narzędzie definicji schematu XML (xsd.exe), które generuje pliki schematu lub klasy z lokalizacji źródłowej.  
  
## <a name="parameters"></a>Parametry  
 W poniższej tabeli opisano parametry **XSD** zadania.  
  
-   **AdditionalOptions**  
  
     Opcjonalnie **ciąg** parametru.  
  
     Lista opcji określonych w wierszu polecenia. Na przykład "*/option1 /option2 /option#*". Użyj tego parametru, aby określić opcje, które nie są reprezentowane przez inne **XSD** parametru zadania.  
  
-   **GenerateFromSchema**  
  
     Opcjonalnie **ciąg** parametru.  
  
     Określa typy, które są generowane na podstawie określonego schematu.  
  
     Określ jedną z następujących wartości, z których każdy odpowiada opcji XSD.  
  
    -   **classes** - **/classes**  
  
    -   **dataset** - **/dataset**  
  
-   **Język**  
  
     Opcjonalnie **ciąg** parametru.  
  
     Określa język programowania dla wygenerowanego kodu.  
  
     Wybierz z **CS** (C#, co jest ustawieniem domyślnym), **VB** (Visual Basic) lub **JS** (JScript). Można również określić w pełni kwalifikowaną nazwę klasy, która implementuje `System.CodeDom.Compiler.CodeDomProvider Class`.  
  
-   **Namespace**  
  
     Opcjonalnie **ciąg** parametru.  
  
     Określa przestrzeń nazw czasu wykonywania wygenerowany typów.  
  
-   **Źródła**  
  
     Wymagane `ITaskItem[]` parametru.  
  
     Określa tablicę elementów pliku źródłowego programu MSBuild, które mogą być używane i wyemitowane przez zadania.  
  
-   **SuppressStartupBanner**  
  
     Opcjonalnie **logiczna** parametru.  
  
     Jeśli `true`, uniemożliwia wyświetlanie wiadomości praw autorskich i wersji, podczas uruchamiania zadania.  
  
-   **Katalog TrackerLogDirectory**  
  
     Opcjonalnie **ciąg** parametru.  
  
     Określa katalog dziennika śledzenia.  
  
## <a name="see-also"></a>Zobacz też  
 [Odwołanie do zadania](../msbuild/msbuild-task-reference.md)



