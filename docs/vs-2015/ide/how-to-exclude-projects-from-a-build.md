---
title: 'Porady: wykluczanie projektów z kompilacji | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 17a837ca-5db9-46cd-b5a7-b14ad1d2c47d
caps.latest.revision: 8
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 6419d2aa216f625aaf82087f0dc8f453e0d0d475
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49941844"
---
# <a name="how-to-exclude-projects-from-a-build"></a>Poradnik: Wykluczanie projektów z kompilacji
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Możesz tworzyć rozwiązania, bez konieczności tworzenia wszystkie projekty, które zawiera. Może na przykład wykluczyć projekt, który przerywa kompilację. Można następnie utworzyć projekt po badania i adres problemy.  
  
 Projekt może wyłączyć, korzystając z następujących metod:  
  
- Usunięcie go tymczasowo z aktywnej konfiguracji rozwiązania.  
  
- Tworzenie konfiguracji rozwiązania, które nie obejmują projektu.  
  
  Aby uzyskać więcej informacji, zobacz [ogólne informacje o konfiguracjach kompilacji](../ide/understanding-build-configurations.md).  
  
### <a name="to-temporarily-remove-a-project-from-the-active-solution-configuration"></a>Aby tymczasowo usunięcie projektu z aktywnej konfiguracji rozwiązania  
  
1.  Na pasku menu wybierz **kompilacji**, **programu Configuration Manager**.  
  
2.  W **projektu kontekstów** tabeli, Znajdź projekt, które chcesz wykluczyć z kompilacji.  
  
3.  W **kompilacji** kolumny dla projektu, usuń zaznaczenie pola wyboru.  
  
4.  Wybierz **Zamknij** przycisk, a następnie ponownie skompiluj rozwiązanie.  
  
### <a name="to-create-a-solution-configuration-that-excludes-a-project"></a>Umożliwia utworzenie konfiguracji rozwiązania, który wyklucza projektu  
  
1.  Na pasku menu wybierz **kompilacji**, **programu Configuration Manager**.  
  
2.  W **Konfiguracja rozwiązania aktywnego** wybierz  **\<nowy >**.  
  
3.  W **nazwa** wprowadź nazwę dla konfiguracji rozwiązania.  
  
4.  W **Kopiuj ustawienia** wybierz konfiguracji rozwiązania, na którym chcesz utworzyć nową konfigurację (na przykład **debugowania**), a następnie wybierz **OK** przycisku .  
  
5.  W **programu Configuration Manager** okno dialogowe, wyczyść pole wyboru w **kompilacji** kolumny dla projektu, który chcesz wykluczyć, a następnie wybierz **Zamknij** przycisku.  
  
6.  Na **standardowa** narzędzi, sprawdź, czy nowa konfiguracja rozwiązania jest aktywna konfiguracja w **konfiguracje rozwiązania** pole.  
  
7.  Na pasku menu wybierz **kompilacji**, **Kompiluj rozwiązanie**.  
  
## <a name="see-also"></a>Zobacz też  
 [Ogólne informacje o konfiguracjach kompilacji](../ide/understanding-build-configurations.md)   
 [Porady: tworzenie i edytowanie konfiguracji](../ide/how-to-create-and-edit-configurations.md)   
 [Instrukcje: Równoczesne kompilowanie wielu konfiguracji](../ide/how-to-build-multiple-configurations-simultaneously.md)



