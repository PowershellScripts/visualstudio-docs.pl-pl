---
title: 'Porady: ustawienie ClickOnce wersji publikacji | Dokumentacja firmy Microsoft'
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
- ClickOnce deployment, setting publish version
- publishing, ClickOnce
- Publish Version property
ms.assetid: 06f15504-6385-40a6-b01d-cd90ca36dc73
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: wpickett
ms.openlocfilehash: b3965e9600fa3ef6a091ae8e32439e8e4f420668
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49271716"
---
# <a name="how-to-set-the-clickonce-publish-version"></a>Porady: ustawienie wersji publikacji technologii ClickOnce
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

[!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] `Publish Version` Właściwość określa, czy w przypadku publikowania aplikacji będzie traktowane jako aktualizację. Każda wersja czasu jest zwiększana, aplikacja zostanie opublikowana jako aktualizację.  
  
 `Publish Version` Właściwość można ustawić na **Publikuj** strony **projektanta projektu**.  
  
> [!NOTE]
>  Brak opcji projektu, który automatycznie powoduje zwiększenie `Publish Version` właściwość każdorazowo aplikacja została opublikowana; ta opcja jest włączona domyślnie. Aby uzyskać więcej informacji, zobacz [porady: automatyczne zwiększenie wersji publikowania ClickOnce](../deployment/how-to-automatically-increment-the-clickonce-publish-version.md).  
  
### <a name="to-change-the-publish-version"></a>Aby zmienić wersję publikowania  
  
1.  Za pomocą projektu wybranego w **Eksploratora rozwiązań**na **projektu** kliknij menu **właściwości**.  
  
2.  Kliknij przycisk **Publikuj** kartę.  
  
3.  W **opublikować wersję** pola, Zwiększ **głównych**, **pomocnicza**, **kompilacji**, lub **poprawki** wersji liczby.  
  
    > [!NOTE]
    >  Nigdy nie należy zmniejszyć numeru wersji; wykonanie tej tak może spowodować aktualizacji nieprzewidywalne zachowanie.  
  
## <a name="see-also"></a>Zobacz też  
 [Wybieranie strategii aktualizacji ClickOnce](../deployment/choosing-a-clickonce-update-strategy.md)   
 [Porady: automatyczne zwiększenie ClickOnce wersji publikacji](../deployment/how-to-automatically-increment-the-clickonce-publish-version.md)   
 [Publikowanie aplikacji ClickOnce](../deployment/publishing-clickonce-applications.md)   
 [Instrukcje: publikowanie aplikacji ClickOnce za pomocą Kreatora publikacji](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)



