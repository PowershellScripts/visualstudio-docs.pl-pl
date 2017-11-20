---
title: 'Porady: debugowanie aplikacji ClickOnce z ograniczonymi uprawnieniami | Dokumentacja firmy Microsoft'
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
- debugging [Visual Studio], ClickOnce applications
- ClickOnce deployment, debugging
- ClickOnce applications, debugging
ms.assetid: 6991ea91-5253-451b-923d-22273a3d38b1
caps.latest.revision: "10"
author: stevehoag
ms.author: shoag
manager: wpickett
ms.openlocfilehash: aa51d29a1d5703f4fd02ee023eb1180da8031ac4
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2017
---
# <a name="how-to-debug-a-clickonce-application-with-restricted-permissions"></a>Porady: debugowanie aplikacji ClickOnce przy użyciu ograniczonych uprawnień
Deweloperzy najprawdopodobniej działają komputerze dewelopera z uprawnień pełnego zaufania, nie zobaczysz tego samego wyjątki zabezpieczeń podczas debugowania aplikacji ClickOnce, której użytkownik końcowy może zostać wyświetlony podczas uruchamiania go z ograniczonymi uprawnieniami.  
  
 Aby przechwytywać tych wyjątków, trzeba debugowania aplikacji z takimi samymi uprawnieniami jak użytkownika końcowego. Debugowanie z ograniczonymi uprawnieniami można włączyć dla **zabezpieczeń** strony **projektanta projektu**.  
  
 Ponadto podczas opracowywania aplikacji, które wywołują usługi sieci Web, te usługi sieci Web często znajdują się na komputerze deweloperskim. Po wdrożeniu użytkownicy będą uzyskiwać dostęp do tych usług sieci Web z innego adresu URL. Aby emulować środowisko użytkownika końcowego podczas debugowania, należy określić, czy adres URL i debuger będzie traktować usług sieci Web tak, jakby była wywoływana z tego adresu URL.  
  
### <a name="to-enable-debugging-with-restricted-permissions"></a>Aby włączyć debugowanie z ograniczonymi uprawnieniami  
  
1.  Z projektem wybranym **Eksploratora rozwiązań**na **projektu** menu, kliknij przycisk **właściwości**.  
  
2.  W **projektanta projektu**, kliknij przycisk **zabezpieczeń** kartę.  
  
3.  Wybierz **włączyć ustawienie zabezpieczeń ClickOnce** pole wyboru, a następnie kliknij przycisk **jest częściowo zaufanych aplikacji** przycisk opcji.  
  
4.  Kliknij przycisk **zaawansowane** przycisku.  
  
5.  Wybierz **Debuguj aplikację z wybranym zestawem uprawnień** pole wyboru, a następnie kliknij przycisk **OK**.  
  
     Podczas debugowania aplikacji, wszelkie próby uprawnienia, które nie są częścią zestawu uprawnień dostępu zgłosi wyjątek zabezpieczeń.  
  
### <a name="to-specify-a-url-for-debugging"></a>Aby określić adres URL do debugowania  
  
1.  Z projektem wybranym **Eksploratora rozwiązań**na **projektu** menu, kliknij przycisk **właściwości**.  
  
2.  W **projektanta projektu**, kliknij przycisk **zabezpieczeń** kartę.  
  
3.  Wybierz **włączyć ustawienie zabezpieczeń ClickOnce** pole wyboru, a następnie kliknij przycisk **jest częściowo zaufanych aplikacji** przycisk opcji.  
  
4.  Kliknij przycisk **zaawansowane** przycisku.  
  
5.  Wybierz **Debuguj aplikację z wybranym zestawem uprawnień** pole wyboru, a następnie kliknij przycisk **OK**.  
  
6.  W **Debuguj aplikację tak, jakby była pobrana z następującego adresu URL** polu tekstowym wprowadź adres URL lub ścieżka sieciowa.  
  
## <a name="see-also"></a>Zobacz też  
 [Porady: ustawienie uprawnień niestandardowych dla aplikacji ClickOnce](../deployment/how-to-set-custom-permissions-for-a-clickonce-application.md)   
 [Zabezpieczanie aplikacji ClickOnce](../deployment/securing-clickonce-applications.md)   
 [Zabezpieczenia dostępu kodu dla aplikacji ClickOnce](../deployment/code-access-security-for-clickonce-applications.md)   
 [Zabezpieczanie aplikacji ClickOnce](../deployment/securing-clickonce-applications.md)