---
title: Wdrażanie typów projektów | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- projects [Visual Studio SDK], managed-code
- projects [Visual Studio SDK], aggregator
ms.assetid: 7f132f67-8589-464c-90dc-0d57ae02aa8f
caps.latest.revision: 13
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: b54250a32c8c3a24232d2b6a654aeb87fa9a727b
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49188254"
---
# <a name="deploying-project-types"></a>Wdrażanie typów projektów
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

[!INCLUDE[vsipsdk](../../includes/vsipsdk-md.md)] instaluje nowy typ projektu agregatora (ProjectAggregator2.dll), a także pakiet Instalatora Windows do ponownej dystrybucji (ProjectAggregator2.msi). Dla typów projektów kodu zarządzanego, należy użyć nowego agregatora. ProjectAggregator2 działa ograniczenia arounds [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] projektu agregator, który uniemożliwić poprawne działanie w typach projektów kodu zarządzanego. Poniżej opisano sposób zmiany Twojego pakietu VSPackage, aby użyć nowego agregatora.  
  
1.  Usunięcie projektu NativeHierarchyWrapper z rozwiązania.  
  
2.  Usuń wszystkie pliki binarne NativeHierarchyWrapper z konfiguracji.  
  
3.  Dodaj ProjectAggregator2.msi do konfiguracji.

