---
title: 'Porady: Konfigurowanie analizy kodu dla aplikacji sieci Web programu ASP.NET | Dokumentacja firmy Microsoft'
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
- vs.codeanalysis.propertypages.asp
ms.assetid: b3000b31-fd9d-489e-81a2-a4bee49453ba
caps.latest.revision: 15
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: bf7450341dd166977d67639f4f3762fae6ef89c8
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49283910"
---
# <a name="how-to-configure-code-analysis-for-an-aspnet-web-application"></a>Porady: konfigurowanie analizy kodu dla aplikacji internetowej ASP.NET
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

W [!INCLUDE[vsPreShort](../includes/vspreshort-md.md)] i [!INCLUDE[vsUltShort](../includes/vsultshort-md.md)] można wybrać z listy analizy kodu *zestawów reguł* dotyczą [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] aplikacji sieci Web. Domyślny zestaw reguł jest reguł zalecanych minimalna firmy Microsoft. Możesz wybrać inny zestaw reguł, aby zastosować do witryny sieci Web.  
  
### <a name="to-configure-a-rule-set-for-an-aspnet-page-framework-project"></a>Aby skonfigurować zestaw reguł dla projektu architektura strony ASP.NET  
  
1.  Wybierz witrynę sieci Web w **Eksploratora rozwiązań**.  
  
2.  Na **analizy** menu, kliknij przycisk **Konfigurowanie analizy kodu dla witryny sieci Web**.  
  
3.  Jeśli rozwiązanie ma więcej niż jeden projekt zaznaczonego rozwiązanie, wybierz opcję kompilacji konfiguracji i docelowy system operacyjny z **konfiguracji** i **platformy** listy.  
  
4.  Dla każdego projektu w rozwiązaniu, kliknij przycisk **zestaw reguł** kolumny, a następnie kliknij przycisk, nazwa reguły jest ustawiony na uruchamianie.  
  
5.  Domyślnie analiza kodu jest uruchamiany na wszystkie projekty w rozwiązaniu. Aby wyłączyć lub włączyć analizy kodu dla konkretnego projektu, wykonaj następujące kroki:  
  
    1.  Kliknij prawym przyciskiem myszy nazwę projektu, a następnie kliknij polecenie Właściwości.  
  
    2.  Zaznacz lub wyczyść **Włącz analizę kodu** pole wyboru. Można również uruchomić analizę kodu ręcznie, wybierając **Uruchom analizę kodu dla witryny sieci Web** z **analizy** menu.  
  
6.  W **Uruchom ten zestaw reguł** listy rozwijanej listy, wykonaj następujące kroki:  
  
    -   Wybierz zestaw reguł, który chcesz użyć.  
  
    -   Wybierz  **\<Przeglądaj >** do określenia, ustaw istniejącej reguły niestandardowe, który nie jest na liście.  
  
    -   Definiowanie niestandardowego zestawu reguł. Aby uzyskać więcej informacji, zobacz [Tworzenie niestandardowych zestawów reguł](../code-quality/creating-custom-code-analysis-rule-sets.md).



