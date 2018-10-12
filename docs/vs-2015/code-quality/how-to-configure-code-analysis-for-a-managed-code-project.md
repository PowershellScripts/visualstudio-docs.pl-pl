---
title: 'Porady: Konfigurowanie analizy kodu dla projektu kodu zarządzanego | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.codeanalysis.propertypages.csvb
helpviewer_keywords:
- code analysis, selecting rule sets
- code analysis, rule sets
ms.assetid: 618f6ff3-db0e-46cb-b08d-dfa35e62c9e7
caps.latest.revision: 35
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 98f3d14b73b0219d0fcec4312648bf613f37378e
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49239190"
---
# <a name="how-to-configure-code-analysis-for-a-managed-code-project"></a>Porady: konfigurowanie analizy kodu dla projektu zarządzanego kodu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

W [!INCLUDE[vsUltLong](../includes/vsultlong-md.md)], [!INCLUDE[vsPreLong](../includes/vsprelong-md.md)] i [!INCLUDE[vsPro](../includes/vspro-md.md)], można wybrać z listy analizy kodu *zestawów reguł* do zastosowania do projektu kodu zarządzanego. Domyślny zestaw reguł jest reguł zalecanych Minimum firmy Microsoft. Można stosować inną regułę ustawiony jako projekt lub dla wszystkich projektów w rozwiązaniu.  
  
> [!NOTE]
>  Aby uzyskać informacje o sposobie konfigurowania zestawu reguł dla aplikacji sieci Web ASP.NET, zobacz [porady: Konfigurowanie analizy kodu dla aplikacji sieci Web ASP.NET](../code-quality/how-to-configure-code-analysis-for-an-aspnet-web-application.md).  
  
### <a name="to-configure-a-rule-set-for-a-net-framework-project"></a>Aby skonfigurować zestaw reguł dla projektu .NET Framework  
  
1.  W **Eksploratora rozwiązań**, kliknij projekt.  
  
2.  Na **analizy** menu, kliknij przycisk **Konfigurowanie analizy kodu dla** *ProjectName*.  
  
3.  W **konfiguracji** i **platformy** listy, kliknij przycisk platformę kompilacji konfiguracji i docelowej.  
  
4.  Aby uruchomić analizę kodu, za każdym razem, gdy projekt jest kompilowany przy użyciu wybranej konfiguracji, zaznacz **Włącz analizę kodu podczas kompilacji (definiuje stałą CODE_ANALYSIS)** pole wyboru. Można również uruchomić analizę kodu ręcznie, otwierając **analizy** menu i klikając **Uruchom analizę kodu dla** *ProjectName*.  
  
5.  Domyślnie program analizy kodu nie raportuje ostrzeżenia z kodu, który jest generowany automatycznie przez narzędzia zewnętrzne. Aby wyświetlić ostrzeżenia z wygenerowanego kodu, należy wyczyścić **Pomijaj wyniki z wygenerowanego kodu** pole wyboru.  
  
    > [!NOTE]
    >  Ta opcja nie pomija błędy analizy kodu i ostrzeżenia z wygenerowanego kodu podczas błędy i ostrzeżenia są wyświetlane w formularzach i szablony. Można wyświetlać lub zachować kod źródłowy dla formularza lub szablonu.  
  
6.  W **Uruchom ten zestaw reguł** listy, wykonaj jedną z następujących czynności:  
  
    -   Kliknij zestaw reguł, który chcesz użyć.  
  
    -   Kliknij przycisk  **\<Przeglądaj … >** do określenia, ustaw istniejącej reguły niestandardowe, który nie jest na liście.  
  
    -   Definiowanie niestandardowego zestawu reguł.  
  
         Aby uzyskać więcej informacji, zobacz [Tworzenie niestandardowych zestawów reguł](../code-quality/creating-custom-code-analysis-rule-sets.md).  
  
## <a name="see-also"></a>Zobacz też  
 [Przewodnik: Konfigurowanie niestandardowego zestawu reguł i korzystanie z niego](../code-quality/walkthrough-configuring-and-using-a-custom-rule-set.md)



