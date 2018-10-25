---
title: Analizowanie pokrycia kodu w testach weryfikacji kompilacji | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 59c07d15-511e-4fd0-b398-bde9d5ed00d9
caps.latest.revision: 10
ms.author: gewarren
manager: douge
ms.openlocfilehash: b67986e42a914c73dea99f97611967aa6ee24097
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49905457"
---
# <a name="analyzing-code-coverage-in-build-verification-tests"></a>Analiza pokrycia kodu w testach weryfikacji kompilacji
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Analiza pokrycia kodu w programie Microsoft Visual Studio dowiesz się, jaka część kodu jest są wykonywane przez testy automatyczne. Aby uzyskać więcej informacji, zobacz [przy użyciu pokrycia kodu, aby określić, jaka część kodu jest poddawana testom](../test/using-code-coverage-to-determine-how-much-code-is-being-tested.md).  
  
 Podczas sprawdzania kodu testy będą uruchamiane na serwerze kompilacji, razem z innymi testami pozostałych członków zespołu. (Jeśli jeszcze nie skonfigurowano już to, zobacz [Uruchom testy w procesie kompilacji](http://msdn.microsoft.com/library/d05743a1-c5cf-447e-bed9-bed3cb595e38).) Jest przydatne do analizy pokrycia kodu w usłudze kompilacji, ponieważ zapewniający najbardziej aktualny i wszechstronny obraz pokrycia całego projektu. Zawiera także automatyczne testy systemu i inne zakodowane testy, których zwykle nie uruchamia się na komputerach deweloperskich.  
  
1. W programie Team Explorer Otwórz **kompilacje**, a następnie dodaj lub Edytuj definicję kompilacji.  
  
2. Na **procesu** rozwiń **testy automatyczne**, **źródła testów**, **parametrów uruchomieniowych**. Ustaw **typu pliku parametrów uruchomieniowych** do **włączonym pokryciem kodu**.  
  
    Jeśli masz więcej niż jedną definicję źródła testów, powtórz ten krok dla każdej z nich.  
  
   - <em>Ale nie ma pola o nazwie **typ pliku ustawień uruchomienia</em>*. *  
  
      W obszarze **testy automatyczne**, wybierz opcję **zestawu testowego** i wybierz przycisk wielokropka **[...]**  na końcu wiersza. W **Dodaj/Edytuj przebieg testowy** dialogowego **Test Runner**, wybierz **Visual Studio Test Runner**.  
  
   ![Ustawienia definicji kompilacji, pokrycia kodu](../test/media/codecoverage-plaincc.png "CodeCoverage plainCC")  
  
   Po uruchomieniu kompilacji wyniki pokrycia kodu są wyświetlane w podsumowaniu kompilacji.  
  
## <a name="see-also"></a>Zobacz też  
 [Korzystanie z pokrycia kodu do określania, jaka część kodu jest poddawana testom](../test/using-code-coverage-to-determine-how-much-code-is-being-tested.md)



