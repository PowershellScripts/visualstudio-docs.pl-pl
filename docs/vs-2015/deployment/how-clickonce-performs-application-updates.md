---
title: Jak technologia ClickOnce wykonuje aktualizacje aplikacji | Dokumentacja firmy Microsoft
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
- updates, ClickOnce
- ClickOnce deployment, updates
- deploying applications [ClickOnce], application updates
ms.assetid: d54313c2-cf0c-420d-b151-99953a95f0bb
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: wpickett
ms.openlocfilehash: 5c2e135a2b872ecd389149626ac09caf02734f40
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49298028"
---
# <a name="how-clickonce-performs-application-updates"></a>Jak technologia ClickOnce wykonuje aktualizacje aplikacji
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Technologia ClickOnce używa informacji o wersjach plików, które zostały określone w manifeście wdrożenia aplikacji, aby zdecydować, czy można zaktualizować pliki aplikacji. Po rozpoczęciu aktualizacji, technologia ClickOnce używa technikę o nazwie *plików poprawek* w celu uniknięcia nadmiarowe pobieranie plików aplikacji.  
  
## <a name="file-patching"></a>Poprawianie plików  
 Podczas aktualizowania aplikacji ClickOnce nie pobiera wszystkie pliki do nowej wersji aplikacji, chyba, że pliki zostały zmienione. Zamiast tego porównuje sygnatury skrótu pliki określone w manifeście aplikacji dla bieżącej aplikacji przed podpisów w manifeście dla nowej wersji. W przypadku różnych podpisów plików ClickOnce pliki do pobrania nowej wersji. Jeśli podpisy są zgodne, plik nie zmienił się z jednej wersji do następnego. W tym przypadku ClickOnce kopiuje istniejący plik i używa go w nowej wersji aplikacji. To podejście zapobiega konieczności pobierania ponownie całej aplikacji, nawet jeśli tylko jeden lub dwa pliki zostały zmienione ClickOnce.  
  
 Poprawianie plików działa także dla zestawów, które zostały pobrane na żądanie przy użyciu <xref:System.Deployment.Application.ApplicationDeployment.DownloadFileGroup%2A> i <xref:System.Deployment.Application.ApplicationDeployment.DownloadFileGroupAsync%2A> metody.  
  
 Jeśli używasz programu Visual Studio do kompilowania aplikacji generuje on nowe sygnatury skrótu dla wszystkich plików w każdym przypadku, gdy należy ponownie skompilować cały projekt. W tym przypadku wszystkie zestawy zostaną pobrane do klienta, mimo że tylko kilka zestawów, które mogły ulec zmianie.  
  
 Plik poprawki nie działa dla plików, które są oznaczone jako dane i przechowywane w katalogu danych. Są one zawsze pobierane niezależnie od tego, sygnatury skrótu pliku. Aby uzyskać więcej informacji o katalogu danych, zobacz [Accessing Local and Remote Data in ClickOnce Applications](../deployment/accessing-local-and-remote-data-in-clickonce-applications.md).  
  
## <a name="see-also"></a>Zobacz też  
 [Wybieranie strategii aktualizacji ClickOnce](../deployment/choosing-a-clickonce-update-strategy.md)   
 [Wybieranie strategii wdrażania ClickOnce](../deployment/choosing-a-clickonce-deployment-strategy.md)



