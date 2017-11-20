---
Title: "Przypisywanie licencji do subskrypcji usługi Visual Studio"
Author: evanwindom
Ms.author: jaunger
Manager: evelynp
Ms.date: 10/3/2017
Ms.topic: Get-Started-Article
Description: "Dowiedz się, jak Administratorzy mogą przypisywać licencje do subskrybentów"
Ms.prod: vs-subscription
Ms.technology: vs-subscriptions
Searchscope: VS Subscription
ms.openlocfilehash: e2a32e911c85603b2d08adb0edad76bcfbc6d6ed
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2017
---
# <a name="assigning-licenses-in-the-visual-studio-subscriptions-administrator-portal"></a>Przypisywanie licencji w portalu administratora subskrypcji programu Visual Studio
## <a name="assigning-a-single-user"></a>Przypisywanie jednego użytkownika
Jeśli masz dostępnych licencji subskrypcji programu Visual Studio można przypisać do nowych użytkowników na ich ich zalety subskrypcji dostęp do tych licencji. 
1.  Aby przypisać jeden subskrybent Visual Studio, w górnej części tabeli, kliknij przycisk **Dodaj**.

![Dodaj subskrybenta](_img\assign-license-add\assign-license-add.png)

2.  Wprowadź informacje do pól formularza dla nowych subskrybentów. Jeśli organizacja korzysta z usługi Azure Active Directory, w tym polu działa jako funkcja wyszukiwania: wyszukiwanie osób w bieżącym katalogu, można wybrać użytkownika w wynikach wyszukiwania. Po wybraniu tej osoby ich nazw, logowania poczty e-mail i powiadomienie e-mail zostaną wypełnione automatycznie zgodnie z poniższą. 

Jeśli Twoja organizacja ma inny adres e-mail do odbierania wiadomości e-mail niż używanego do logowania, istnieje możliwość wprowadzania go tutaj. Wybierz hiperłącze, które wskazuje "Inny adres e-mail dla komunikacji niż logowania?". 

Jeśli chcesz, aby móc zalogować się do tego subskrybenta [Portal subskrypcji w usłudze Visual Studio](https:/my.visualstudio.com) i mają dostęp do modułu pobierania oprogramowania i innych subskrypcji usług oraz zasoby (w tym Microsoft Azure, programu Visual Studio Team Usługi Xamarin i szkolenia Pluralsight, pomocy technicznej i inne), upewnij się, że pole pliki do pobrania jest zaznaczone. Jeśli wybierzesz zaznaczenie tego pola wyboru, użytkownik nie ma dostępu do modułu pobierania oprogramowania, ale dostęp do innych korzyści zawarte w subskrypcji będzie to miało wpływu. Gdy wszystko będzie gotowe, kliknij przycisk **Dodaj**.

![Wprowadź informacje abonenta](_img\assign-license-add\add-subscriber-1.png)
![wprowadź informacje abonenta](_img\assign-license-add\add-subscriber-2.png)

3.  Po dodaniu subskrybenta, wiadomości E-mail przypisania będą automatycznie wysyłane do nowych subskrybentów z dalszymi instrukcjami. Możesz wysłać wiadomości E-mail przypisania w dowolnym momencie ponownie przez kliknięcie przycisku Wyślij ponownie w menu u góry.

![Subskrybent dodane](_img\assign-license-add\add-subscriber-complete.png)

## <a name="bulk-assignments"></a>Przydziały zbiorcze
1.  Aby dodać jednocześnie wiele subskrybentów, przejdź do karty subskrybentów. Na Wstążce u góry kliknij **Dodawanie zbiorcze**. 

![Dodawanie zbiorcze](_img\assign-license-add\bulk-assign-add.png)

2. Przypisz masowo używa szablonu programu Microsoft Excel można przekazać subskrybentów. W oknie dialogowym przekazać wielu subskrybentów, kliknij przycisk **Pobierz** można pobrać szablonu. Zawsze należy pobrać najnowszą wersję tego szablonu. Jeśli używasz starszej wersji zbiorczego przekazania może zakończyć się niepowodzeniem.
! Przekaż wiele Subscribers](_img\assign-license-add\bulk-assign-upload.png)
3.  W arkuszu kalkulacyjnym programu Excel Wypełnij pola o informacje dla użytkowników indywidualnych, które chcesz przypisać subskrypcje. Odwołanie pole jest opcjonalne. Jeśli wypełniony dowolnej części szablonu nieprawidłowo, powinien zostać wyświetlony komunikat o błędzie opisujący problem. Zapisz plik na dysku twardym, jeśli zostaną wykonane.
**W celu zapewnienia sprawnego przekazywania, należy stosować poniższe najlepsze rozwiązania:**
- Upewnij się, że żadne z pól formularza zawierać przecinków.
- Usuwaj odstępy przed i po pól formularza, takich jak nazwy użytkowników.
- Upewnij się, że nie zawierają dodatkowe spacje między nazwami pierwszego lub ostatniego dwuczęściowej nazwy użytkowników (np. dwuczęściową imię, takie jak "Może Maggie" należy nie wpisać jako "Może Maggie", ponieważ system nie będzie ograniczać dodatkowe miejsce)

![Zbiorcze Dodawanie szablonu](_img\assign-license-add\bulk-template.png)

4.  Powrócić do portalu Visual Studio subskrypcje administracyjnej i w oknie dialogowym przekazać wielu subskrybentów, kliknij przycisk **Przeglądaj**. Przejdź do pliku programu Excel został zapisany i kliknij **OK**. Na ekranie pojawi się postępu przekazywania. 

![Dodawanie zbiorcze przekazywania](_img\assign-license-add\bulk-assign-upload-2.png)

Jeśli szablon zawiera błędy, przekazywanie zakończy się niepowodzeniem i zostaną wyświetlone błędy można więc Popraw szablon i próbę przekazania zbiorczego.

![Przekazywanie błędów](_img\assign-license-add\bulk-assign-upload-fail.png)

Po pomyślnym zakończeniu operacji przekazywania, zobaczysz listę subskrybentów i komunikat potwierdzenia.

![Przesyłanie zakończone](_img\assign-license-add\bulk-assign-upload-complete.png)