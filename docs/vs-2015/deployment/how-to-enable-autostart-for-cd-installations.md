---
title: 'Porady: włączenie funkcji AutoStart dla instalacji z dysku CD | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-deployment
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- ClickOnce deployment, AutoStart
- ClickOnce deployment, installation on CD or DVD
- deploying applications [ClickOnce], installation on CD or DVD
ms.assetid: caaec619-900c-4790-90e3-8c91f5347635
caps.latest.revision: 19
author: mikejo5000
ms.author: mikejo
manager: wpickett
ms.openlocfilehash: 2fde610731ca5ec315b94d2e46f58edb2a7b56fa
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49273146"
---
# <a name="how-to-enable-autostart-for-cd-installations"></a>Porady: włączenie funkcji AutoStart dla instalacji z dysku CD
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

W przypadku wdrażania [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] aplikacji za pomocą nośników wymiennych, takich jak dysk CD-ROM lub DVD-ROM, aby umożliwić `AutoStart` tak, aby [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] aplikacja jest uruchamiana automatycznie, gdy nośnik zostanie wstawiona.  
  
 `AutoStart` można włączyć dla **Publikuj** strony **projektanta projektu**.  
  
### <a name="to-enable-autostart"></a>Aby włączyć automatyczne uruchamianie  
  
1.  Za pomocą projektu wybranego w **Eksploratora rozwiązań**na **projektu** kliknij menu **właściwości**.  
  
2.  Kliknij przycisk **Publikuj** kartę.  
  
3.  Kliknij przycisk **opcje** przycisku.  
  
     **Opcji publikowania** pojawi się okno dialogowe.  
  
4.  Kliknij przycisk **wdrożenia**.  
  
5.  Wybierz **dla instalacji z dysku CD, automatycznie Rozpocznij instalację po włożeniu dysku CD** pole wyboru.  
  
     Plik Autorun.inf zostaną skopiowane do lokalizacji publikowania, gdy aplikacja została opublikowana.  
  
## <a name="see-also"></a>Zobacz też  
 [Publikowanie aplikacji ClickOnce](../deployment/publishing-clickonce-applications.md)   
 [Instrukcje: publikowanie aplikacji ClickOnce za pomocą Kreatora publikacji](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)



