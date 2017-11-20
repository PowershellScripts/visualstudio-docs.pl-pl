---
title: "Parametry połączenia zawiera poświadczenia za pomocą hasła w postaci zwykłego tekstu, a nie korzysta ze zintegrowanych zabezpieczeń | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 501d85af-92e0-4471-b280-8a59c0688575
caps.latest.revision: "3"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.technology: vs-data-tools
ms.openlocfilehash: e9c03f6c864894d0dee9a0fade3137f1a7c50cda
ms.sourcegitcommit: ee42a8771f0248db93fd2e017a22e2506e0f9404
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/09/2017
---
# <a name="the-connection-string-contains-credentials-with-a-clear-text-password-and-is-not-using-integrated-security"></a>Parametry połączenia zawiera poświadczenia za pomocą hasła w postaci zwykłego tekstu, a nie korzysta ze zintegrowanych zabezpieczeń
Czy chcesz zapisać parametry połączenia w bieżącym pliku DBML i pliki konfiguracji aplikacji z tymi informacjami poufnymi?  Kliknij przycisk nie, aby zapisać parametry połączenia bez informacji poufnych.  
  
 Podczas pracy z połączeń danych, które zawierają poufne informacje (hasła, które znajdują się w parametrach połączenia), możesz skorzystać z opcji zapisywania parametry połączenia w pliku DBML projektu i pliku konfiguracji aplikacji lub bez poufne informacje.  
  
> [!WARNING]
>  Jawne ustawienie **połączenia** właściwości **ustawienia aplikacji** właściwości **False** spowoduje dodanie hasła do pliku DBML.  
  
### <a name="to-save-the-connection-string-with-the-sensitive-information-in-the-projects-application-settings"></a>Aby zapisać parametry połączenia z poufne informacje w ustawieniach aplikacji projektu  
  
-   Kliknij przycisk **Tak**.  
  
     Parametry połączenia są przechowywane jako ustawienie aplikacji. Parametry połączenia zawierają poufne informacje w postaci zwykłego tekstu. Za pomocą pliku DBML nie zawiera poufne informacje.  
  
### <a name="to-save-the-connection-string-without-the-sensitive-information-in-the-projects-application-settings"></a>Aby zapisać parametry połączenia bez informacji poufnych w ustawieniach aplikacji projektu  
  
-   Kliknij przycisk **nr**.  
  
     Parametry połączenia są przechowywane jako ustawienie aplikacji, ale hasło nie jest dołączony.  
  
## <a name="see-also"></a>Zobacz także
[Komunikaty Projektanta obiektów relacyjnych](../data-tools/o-r-designer-messages.md)  
[LINQ do SQL narzędzi w programie Visual Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md)