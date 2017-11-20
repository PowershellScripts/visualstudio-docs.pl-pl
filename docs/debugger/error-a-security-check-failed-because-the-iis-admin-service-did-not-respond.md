---
title: "Błąd: Sprawdzanie zabezpieczeń nie powiodło się, ponieważ usługa administratora usług IIS nie odpowiada. | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vs.debug.error.iis_not_responding
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords: debugger, Web application errors
ms.assetid: 6060e94e-71dc-49f2-bb59-2584216eadbf
caps.latest.revision: "10"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 5bc147c979357934d68692ea863c665422c84b34
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="error-a-security-check-failed-because-the-iis-admin-service-did-not-respond"></a>Błąd: Sprawdzanie zabezpieczeń nie powiodło się ponieważ usługa administratora nie odpowiada
Ten błąd występuje, gdy administrator usług IIS nie odpowiada. Zwykle oznacza to, że jest problem z instalacją usług IIS. Po pierwsze sprawdzenie, czy usługa jest uruchomiona za pomocą **usług** narzędzia z **narzędzia administracyjne**.  
  
### <a name="to-correct-this-error"></a>Aby poprawić ten błąd  
  
-   Ponownie zainstaluj usługi IIS, za pomocą **Dodaj lub usuń programy** Panelu sterowania.  
  
-   —lub—  
  
-   Usuwanie usług IIS z komputera, za pomocą apletu Dodaj lub usuń programy w Panelu sterowania. Jeśli usunięto usług IIS i nadal występują problemy, sprawdź w rejestrze i upewnij się, że ten klucz już istnieje:  
  
    ```  
    HKEY_CLASSES_ROOT\CLSID\{A9E69610-B80D-11D0-B9B9-00A0C922E750}  
    ```  
  
     —lub—  
  
-   Wyłącz usługę administratora usług IIS przy użyciu narzędzia administracyjne w Panelu sterowania. Spowoduje to wyłączenie usług IIS na tym komputerze.  
  
     Po wykonaniu któregokolwiek te trzy kroki, uruchom ponownie komputer.  
  
     Aby uzyskać dodatkowe informacje Zobacz dokumentację usług IIS.  
  
## <a name="see-also"></a>Zobacz też  
 [Debugowanie aplikacji sieci Web: Błędy i rozwiązywanie problemów](../debugger/debugging-web-applications-errors-and-troubleshooting.md)