---
title: Parametry połączenia zawierają poświadczenia z hasła w postaci zwykłego tekstu, a nie korzysta ze zintegrowanych zabezpieczeń | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 501d85af-92e0-4471-b280-8a59c0688575
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: f1ec13cab1b8c41225cb1934740b8dd3e7f59ac0
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49230878"
---
# <a name="the-connection-string-contains-credentials-with-a-clear-text-password-and-is-not-using-integrated-security"></a>Parametry połączenia zawierają poświadczenia z hasłem w postaci zwykłego tekstu i nie korzystają ze zintegrowanych zabezpieczeń
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Czy chcesz zapisać parametry połączenia w bieżącym pliku DBML i pliki konfiguracyjne aplikacji z tymi informacjami poufnymi?  Kliknij przycisk nie, aby zapisać parametry połączenia bez informacji poufnych.  
  
 Podczas pracy z połączeniami danych, zawierające informacje poufne (hasła, które znajdują się w parametrach połączenia), możesz skorzystać z opcji zapisanie parametrów połączenia w pliku DBML projektu i pliku konfiguracji aplikacji z użyciem lub bez poufne informacje.  
  
> [!WARNING]
>  Jawne ustawianie **połączenia** właściwości **ustawienia aplikacji** właściwości **False** spowoduje dodanie hasła do pliku DBML.  
  
### <a name="to-save-the-connection-string-with-the-sensitive-information-in-the-projects-application-settings"></a>Aby zapisać parametry połączenia z poufnych informacji w ustawieniach aplikacji projektu  
  
-   Kliknij przycisk **Tak**.  
  
     Parametry połączenia są przechowywane jako ustawienie aplikacji. Parametry połączenia zawierają poufne informacje w postaci zwykłego tekstu. Za pomocą pliku DBML nie zawiera poufne informacje.  
  
### <a name="to-save-the-connection-string-without-the-sensitive-information-in-the-projects-application-settings"></a>Aby zapisać parametry połączenia bez informacji poufnych w ustawieniach aplikacji projektu  
  
-   Kliknij przycisk **nie**.  
  
     Parametry połączenia są przechowywane jako ustawienie aplikacji, ale hasło nie jest dołączony.  
  
## <a name="see-also"></a>Zobacz też  
 [Narzędzia LINQ to SQL Tools w programie Visual Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md)

