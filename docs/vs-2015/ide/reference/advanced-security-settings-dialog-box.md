---
title: Zaawansowane ustawienia zabezpieczeń — okno dialogowe | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.err.debug_in_zone_no_hostproc
- vs.err.debug_in_zone_no_hostproc:11310
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- Advanced Security Settings dialog box
ms.assetid: 2e7aefe9-6d20-4f3e-b257-aee1ebcc6f5d
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: ff49418b23317b590776c0f81d334480f460780a
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49233002"
---
# <a name="advanced-security-settings-dialog-box"></a>Zaawansowane ustawienia zabezpieczeń — Okno dialogowe
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
To okno dialogowe umożliwia określenie ustawień zabezpieczeń dotyczące debugowania w strefie.  
  
 Aby otworzyć to okno dialogowe, wybierz węzeł projektu w **Eksploratora rozwiązań**, a następnie na **projektu** menu, kliknij przycisk **właściwości**. Podczas **projektanta projektu** zostanie wyświetlona, kliknij przycisk **zabezpieczeń** kartę. Na **zabezpieczeń** wybierz opcję **włączenia ustawień zabezpieczeń technologii ClickOnce**, kliknij przycisk **to częściowo zaufanych aplikacji**, a następnie kliknij przycisk **zaawansowane**.  
  
## <a name="uielement-list"></a>Lista elementów UI  
 **Debuguj aplikację z wybranym zestawem uprawnień**  
 Jeśli wybierzesz to pole wyboru, zestaw uprawnień wybranej na **zabezpieczeń** strony jest używany podczas debugowania. Domyślnie ta opcja jest zaznaczona.  
  
 Debugowanie w strefie zabezpieczeń do pracy, ta opcja musi być włączone; Ponadto **włączyć procesu hostingu Visual Studio** opcji (dostępne na **debugowania** strony **projektanta projektu**) musi być włączona.  
  
 W przypadku projektów aplikacji przeglądarki sieci Web WPF **Debuguj aplikację z wybranym zestawem uprawnień** opcji jest zaznaczony i wyłączony.  
  
 **Przyznać aplikacji dostęp do witryny pochodzenia**  
 Jeśli wybierzesz to pole wyboru, aplikacji można uzyskać dostęp do witryny sieci Web lub udziału serwera, na którym została opublikowana. Domyślnie ta opcja jest zaznaczona.  
  
 **Debuguj aplikację tak, jakby zostały pobrane z następującego adresu URL**  
 Jeśli trzeba umożliwić aplikacji dostęp do witryny sieci Web lub udziału serwera odpowiadający **adres URL instalacji** określone na **Publikuj** stronie i wpisz poniżej tego adresu URL. Ta opcja jest dostępna tylko wtedy, gdy **przyznać aplikacji dostęp do witryny pochodzenia** jest zaznaczone.  
  
## <a name="see-also"></a>Zobacz też  
 [Strona zabezpieczeń, Projektant projektu](../../ide/reference/security-page-project-designer.md)



