---
title: 'Porady: automatyczne zwiększenie ClickOnce wersji publikacji | Dokumentacja firmy Microsoft'
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
- deploying applications [ClickOnce], incrementing publish version automatically
- Publish Version property, incrementing
- ClickOnce deployment, incrementing publish version automatically
- publishing, ClickOnce
ms.assetid: 686ab88a-6305-4914-a05b-fe269cc0ae1e
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: wpickett
ms.openlocfilehash: ac5b4e67c0bbebba7586715e4ba491bf11bacc4a
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49300225"
---
# <a name="how-to-automatically-increment-the-clickonce-publish-version"></a>Porady: automatyczne zwiększenie wersji publikacji ClickOnce
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Podczas publikowania [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] aplikację, zmieniając `Publish Version` właściwości powoduje, że aplikacja opublikowana jako aktualizację. Domyślnie, Visual Studio automatycznie zwiększa `Revision` liczby `Publish Version` każdorazowo, możesz opublikować aplikację.  
  
 To zachowanie można wyłączyć na **Publikuj** strony **projektanta projektu**.  
  
> [!NOTE]
>  Okna dialogowe i polecenia menu mogą się różnić od tych opisanych w Pomocy, w zależności od ustawień aktywnych lub wydania. Aby zmienić swoje ustawienia, wybierz opcję **Import i eksport ustawień** na **narzędzia** menu. Aby uzyskać więcej informacji, zobacz [Dostosowywanie ustawień środowiska deweloperskiego, w programie Visual Studio](http://msdn.microsoft.com/en-us/22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
### <a name="to-disable-automatically-incrementing-the-publish-version"></a>Aby wyłączyć automatyczne zwiększenie wersji publikowania  
  
1.  Za pomocą projektu wybranego w **Eksploratora rozwiązań**na **projektu** menu, kliknij przycisk **właściwości**.  
  
2.  Kliknij przycisk **Publikuj** kartę.  
  
3.  W **opublikować wersję** sekcji wyczyść **automatycznie zwiększ numer poprawki przy każdym wydaniu** pole wyboru.  
  
## <a name="see-also"></a>Zobacz też  
 [Porady: ustawienie ClickOnce wersji publikacji](../deployment/how-to-set-the-clickonce-publish-version.md)   
 [Publikowanie aplikacji ClickOnce](../deployment/publishing-clickonce-applications.md)   
 [Instrukcje: publikowanie aplikacji ClickOnce za pomocą Kreatora publikacji](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)



