---
title: 'Porady: pomijanie ostrzeżeń analizy kodu dla wygenerowanego kodu | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 3a96434e-d419-43a7-81ba-95cccac835b8
caps.latest.revision: 7
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 07858183af427e2b67e1e0f63d1f8889caf72fbe
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49293751"
---
# <a name="how-to-suppress-code-analysis-warnings-for-generated-code"></a>Porady: pomijanie ostrzeżeń analizy kodu dla wygenerowanego kodu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kompilatory kodu zarządzanego często generują kod, który jest dodawany do projektu w celu ułatwienia tworzenia kodu szybkiego. Ponadto deweloperzy często używają narzędzi innych firm ułatwia szybkie tworzenie aplikacji. Te narzędzia są również wygenerować kod, który jest dodawany do projektu.  
  
 Możesz chcieć wyświetlić naruszenia reguły, które analizy kodu, który umożliwia odnalezienie w wygenerowanym kodzie. Jednak możesz nie chcieć je wyświetlić, jeśli nie można wyświetlić i utrzymywać kod, który zawiera naruszenie.  
  
 **Pomijaj wyniki z wygenerowanego kodu** pole wyboru na stronie właściwości analizy kodu projektu umożliwia wybranie, czy mają być wyświetlane ostrzeżenia analizy kodu w kodzie wygenerowanym przez narzędzie innej firmy.  
  
> [!NOTE]
>  Ta opcja nie pomija błędy analizy kodu i ostrzeżenia z wygenerowanego kodu podczas błędy i ostrzeżenia są wyświetlane w formularzach i szablony. Można wyświetlać lub zachować kod źródłowy dla formularza lub szablonu.  
  
### <a name="to-suppress-warnings-for-generated-code-in-a-project"></a>Aby pominąć ostrzeżeń dla wygenerowanego kodu w projekcie  
  
1.  Kliknij prawym przyciskiem myszy projekt w Eksploratorze rozwiązań, a następnie kliknij przycisk **właściwości**.  
  
2.  Kliknij przycisk **analiza kodu**.  
  
3.  Wybierz **Pomijaj wyniki z wygenerowanego kodu** pole wyboru.



