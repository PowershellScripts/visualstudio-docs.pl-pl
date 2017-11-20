---
title: "Porady: określanie strony publikowania dla aplikacji ClickOnce | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-deployment
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- deploying applications [ClickOnce], specifying publish page
- Publish Page property
- publishing, ClickOnce
- ClickOnce deployment, specifying publish page
ms.assetid: 9d70eebb-bdee-4b42-8e7e-7a07e199bdf7
caps.latest.revision: "18"
author: stevehoag
ms.author: shoag
manager: wpickett
ms.openlocfilehash: e05718d2a00df76d2c78e16c5b4473ab48d43a39
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2017
---
# <a name="how-to-specify-a-publish-page-for-a-clickonce-application"></a>Porady: określanie strony publikowania dla aplikacji ClickOnce
Podczas publikowania [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] aplikacji domyślnej strony sieci Web (publish.htm) zostaną wygenerowane i opublikowane wraz z aplikacji. Ta strona zawiera nazwę aplikacji, łącze do zainstalowania aplikacji i/lub wymagań wstępnych i link do tematu Pomocy zawierająca opis [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)]. **Opublikuj stronę** właściwości projektu można określić nazwę strony sieci Web dla Twojego [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] aplikacji.  
  
 Po stronie publikacji został określony, przy następnym możesz opublikować go zostaną skopiowane do lokalizacji publikacji; nie zostaną zastąpione w przypadku publikowania ponownie. Jeśli chcesz dostosować wygląd strony, możesz to zrobić bez obaw o utratę danych. Aby uzyskać więcej informacji, zobacz [porady: Dostosowywanie strony sieci Web technologii ClickOnce domyślne](../deployment/how-to-customize-the-default-web-page-for-a-clickonce-application.md).  
  
 **Opublikuj stronę** właściwości można ustawić w **opcji publikowania** okno dialogowe, dostępne z **publikowania** okienku **projektanta projektu**.  
  
### <a name="to-specify-a-custom-web-page-for-a-clickonce-application"></a>Aby określić niestandardowe strony sieci Web dla aplikacji ClickOnce  
  
1.  Z projektem wybranym **Eksploratora rozwiązań**na **projektu** kliknij menu **właściwości**.  
  
2.  Wybierz **publikowania** okienka.  
  
3.  Kliknij przycisk **opcje** przycisk, aby otworzyć **opcji publikowania** okno dialogowe.  
  
4.  Kliknij przycisk **wdrożenia**.  
  
5.  W **opcji publikowania** okna dialogowego upewnij się, że **opublikować stronę sieci web Otwórz wdrożenia po** jest zaznaczone pole wyboru (ona powinny zostać wybrana domyślnie).  
  
6.  W **stronę sieci web wdrożenia:** , wprowadź nazwę dla strony sieci Web, a następnie kliknij **OK**.  
  
### <a name="to-prevent-the-publish-page-from-launching-each-time-you-publish"></a>Aby zapobiec uruchamianiu zawsze, gdy opublikujesz strony publikowania  
  
1.  Z projektem wybranym **Eksploratora rozwiązań**na **projektu** kliknij menu **właściwości**.  
  
2.  Wybierz **publikowania** okienka.  
  
3.  Kliknij przycisk **opcje** przycisk, aby otworzyć **opcji publikowania** okno dialogowe.  
  
4.  Kliknij przycisk **wdrożenia**.  
  
5.  W **opcji publikowania** okno dialogowe, usuń zaznaczenie **opublikować stronę sieci web Otwórz wdrożenia po** pole wyboru.  
  
## <a name="see-also"></a>Zobacz też  
 [Publikowanie aplikacji ClickOnce](../deployment/publishing-clickonce-applications.md)   
 [Porady: publikowanie aplikacji ClickOnce za pomocą Kreatora publikacji](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)   
 [Porady: dostosowywanie ClickOnce domyślnej strony sieci Web](../deployment/how-to-customize-the-default-web-page-for-a-clickonce-application.md)