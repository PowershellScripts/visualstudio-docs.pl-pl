---
title: Zgodność wersji dla zasad ewidencjonowania analizy kodu | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- version compatibility, code analysis check-in policy
- check-in policies, version compatibility for code analysis
ms.assetid: 1af376e3-3be7-4445-803b-76a858567a5b
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 840a12e7f4c0e3853e885a803dea5a92e05a5a27
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49261485"
---
# <a name="version-compatibility-for-code-analysis-check-in-policies"></a>Kompatybilność wersji dla zasad ewidencjonowania analizy kodu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Jeśli musisz ocenić i tworzyć przy użyciu różnych wersji zasad ewidencjonowania dla analizy kodu [!INCLUDE[esprtfc](../includes/esprtfc-md.md)], musisz wiedzieć, że różnice w sposób [!INCLUDE[vstsTfsOrcasLong](../includes/vststfsorcaslong-md.md)] i [!INCLUDE[vstsTfsRosarioShort](../includes/vststfsrosarioshort-md.md)] oceń zasady ewidencjonowania.  
  
## <a name="version-compatibility-for-evaluating-check-in-policies"></a>Kompatybilność wersji dla oceny zasad ewidencjonowania  
  
-   Jeśli zasady ewidencjonowania analizy kodu są obliczane w [!INCLUDE[vstsTfsOrcasShort](../includes/vststfsorcasshort-md.md)], wszystkich reguł, które istniały w [!INCLUDE[vstsTfsRosarioShort](../includes/vststfsrosarioshort-md.md)] , ale nie istnieją w [!INCLUDE[vstsTfsOrcasShort](../includes/vststfsorcasshort-md.md)] są ignorowane.  
  
-   Jeśli zasady ewidencjonowania analizy kodu są obliczane w [!INCLUDE[vstsTfsRosarioShort](../includes/vststfsrosarioshort-md.md)], wszystkie nowe reguły, które należą wyłącznie do [!INCLUDE[vstsTfsOrcasShort](../includes/vststfsorcasshort-md.md)] są ignorowane.  
  
-   Jeśli zasady analizy kodu ewidencjonowania Określa zestawy reguł [!INCLUDE[vstsTfsOrcasShort](../includes/vststfsorcasshort-md.md)] ignoruje wszystkie reguły, które są określone przez zestawy nie rozpoznaje.  
  
-   Jeśli zasady analizy kodu ewidencjonowania Określa zestawy reguł, [!INCLUDE[vstsTfsRosarioShort](../includes/vststfsrosarioshort-md.md)] nie rozpozna, zostanie wyświetlony komunikat.  
  
## <a name="version-compatibility-for-authoring-check-in-policies"></a>Zgodność wersji do tworzenia zasad ewidencjonowania  
  
-   Jeśli zasady analizy kodu ewidencjonowania utworzone przy użyciu [!INCLUDE[vstsTfsOrcasShort](../includes/vststfsorcasshort-md.md)] wersję [!INCLUDE[esprtfc](../includes/esprtfc-md.md)], nie można użyć [!INCLUDE[vstsTfsRosarioShort](../includes/vststfsrosarioshort-md.md)] wersję [!INCLUDE[esprtfc](../includes/esprtfc-md.md)] go zmodyfikować. A także [!INCLUDE[vstsTfsRosarioShort](../includes/vststfsrosarioshort-md.md)] nie można obliczyć zasad.  
  
-   Jeśli zasady analizy kodu ewidencjonowania utworzone przy użyciu [!INCLUDE[esprtfc](../includes/esprtfc-md.md)] w [!INCLUDE[vstsTfsRosarioShort](../includes/vststfsrosarioshort-md.md)], można użyć [!INCLUDE[esprtfc](../includes/esprtfc-md.md)] w [!INCLUDE[vstsTfsOrcasShort](../includes/vststfsorcasshort-md.md)] do zmodyfikowania, a także zasady również może zostać oceniony przez [!INCLUDE[vstsTfsOrcasShort](../includes/vststfsorcasshort-md.md)]. Po zmodyfikowaniu zasad za pomocą [!INCLUDE[esprtfc](../includes/esprtfc-md.md)] w [!INCLUDE[vstsTfsOrcasShort](../includes/vststfsorcasshort-md.md)], nie będzie można edytować zasad za pomocą [!INCLUDE[esprtfc](../includes/esprtfc-md.md)] w [!INCLUDE[vstsTfsRosarioShort](../includes/vststfsrosarioshort-md.md)]. [!INCLUDE[vstsTfsRosarioShort](../includes/vststfsrosarioshort-md.md)] może służyć do oceny zasad bez problemów z niezgodnymi silne nazwy.  
  
-   Aby utworzyć zasady analizy kodu ewidencjonowania za pomocą ustawienia reguł, które są stosowane dla obu [!INCLUDE[vstsTfsRosarioShort](../includes/vststfsrosarioshort-md.md)] i [!INCLUDE[vstsTfsOrcasShort](../includes/vststfsorcasshort-md.md)], musisz utworzyć zasady w [!INCLUDE[vstsTfsRosarioShort](../includes/vststfsrosarioshort-md.md)], wprowadzać wszelkie zmiany, które są potrzebne i zapisać zasady. Jeśli zmiany zasad istnieje tylko w [!INCLUDE[vstsTfsOrcasShort](../includes/vststfsorcasshort-md.md)], zmodyfikuj i zapisz ją w [!INCLUDE[vstsTfsOrcasShort](../includes/vststfsorcasshort-md.md)].  
  
     Po zapisaniu zasad w [!INCLUDE[vstsTfsOrcasShort](../includes/vststfsorcasshort-md.md)], nie może zmienić ustawienia dla reguł, które istnieją w [!INCLUDE[vstsTfsRosarioShort](../includes/vststfsrosarioshort-md.md)] tylko.



