---
title: 'Porady: Określanie nazwy Menu Start dla aplikacji ClickOnce | Dokumentacja firmy Microsoft'
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
- Start menu resource name
- Start menu name
- ClickOnce deployment, Start menu name
ms.assetid: 4b5183b2-2fd4-4433-9310-4a73bb12c4e3
caps.latest.revision: 19
author: mikejo5000
ms.author: mikejo
manager: wpickett
ms.openlocfilehash: 98554ef2dc9b1f5bdd3ef1879f32b2c2319a7a1b
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49277784"
---
# <a name="how-to-specify-a-start-menu-name-for-a-clickonce-application"></a>Porady: określanie nazwy menu Start dla aplikacji ClickOnce
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Gdy [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] instalacji aplikacji do użytku w trybie online i offline, wpis jest dodawany do **Start** menu i **apletu Dodaj lub usuń programy** listy. Domyślnie nazwa wyświetlana jest taka sama jak nazwa zestawu aplikacji, ale można zmienić nazwę wyświetlaną, ustawiając **nazwa produktu** w **opcji publikowania** okno dialogowe.  
  
 **Nazwa produktu** będą wyświetlane na stronie publish.htm; dla zainstalowanej aplikacji w trybie offline, będzie on nazwę wpisu w **Start** menu, a będzie również nazwę, która zawiera w **Dodawanie lub usuwanie Programy**.  
  
 **Nazwa wydawcy** będą wyświetlane na stronie publish.htm powyżej **nazwa produktu**, a dla zainstalowanej aplikacji w trybie offline, konieczne będzie również nazwę folderu, który zawiera ikonę aplikacji w **Start**  menu.  
  
 Możesz ustawić **nazwa produktu** i **nazwę wydawcy** właściwości w **opcji publikowania** okno dialogowe, dostępne na **Publikuj** strony z **Projektant projektu**.  
  
### <a name="to-specify-a-start-menu-name"></a>Aby określić nazwy menu Start  
  
1.  Za pomocą projektu wybranego w **Eksploratora rozwiązań**na **projektu** menu, kliknij przycisk **właściwości**.  
  
2.  Kliknij przycisk **Publikuj** kartę.  
  
3.  Kliknij przycisk **opcje** przycisk, aby otworzyć **opcji publikowania** okno dialogowe.  
  
4.  Kliknij przycisk **opis**.  
  
5.  W **opcji publikowania** okna dialogowego wprowadź nazwę, aby wyświetlić **nazwa produktu**.  
  
6.  Opcjonalnie można wprowadzić nazwę wydawcy w **nazwę wydawcy**.  
  
## <a name="see-also"></a>Zobacz też  
 [Publikowanie aplikacji ClickOnce](../deployment/publishing-clickonce-applications.md)   
 [Instrukcje: publikowanie aplikacji ClickOnce za pomocą Kreatora publikacji](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)



