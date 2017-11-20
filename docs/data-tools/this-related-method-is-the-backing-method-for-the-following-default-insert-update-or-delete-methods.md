---
title: "Ta powiązana metoda to metoda pomocnicza następujących domyślne metod wstawiania, aktualizacji lub usuń | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 62afa6da-97cf-48b9-8de3-33e4d72a0377
caps.latest.revision: "3"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.technology: vs-data-tools
ms.openlocfilehash: 3f8a31f886548d03f7acac58d392713ced297b42
ms.sourcegitcommit: ee42a8771f0248db93fd2e017a22e2506e0f9404
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/09/2017
---
# <a name="this-related-method-is-the-backing-method-for-the-following-default-insert-update-or-delete-methods"></a>Ta metoda powiązane jest metoda pomocnicza następujące domyślne insert, update lub metody delete
Ta metoda powiązane jest metoda pomocnicza następujące domyślne insert, update lub metody delete. Jeśli zostanie usunięta, te metody także zostaną usunięte. Czy chcesz kontynuować?  
  
 Wybrane `DataContext` metody jest obecnie używana jako jedną z metod Insert, Update lub Delete dla jednej z klas jednostek w Projektancie obiektów relacyjnych. Usunięcie wybranej metody powodują klasę jednostki, która była za pomocą tej metody można powrócić do domyślne zachowanie środowiska wykonawczego do operacji Insert, Update, lub usunąć w trakcie aktualizacji.  
  
### <a name="to-delete-the-selected-method-causing-the-entity-class-to-use-runtime-updates"></a>Aby usunąć wybranej metody, powodując klasy jednostki do korzystania z aktualizacji środowiska uruchomieniowego  
  
-   Kliknij przycisk **Tak**.  
  
     Wybrane metody zostaną usunięte i wszystkie klasy, które użyć tej metody dla zastępowanie zachowania aktualizacji są przywracane do przy użyciu domyślnego LINQ do SQL zachowania w czasie wykonywania.  
  
### <a name="to-close-the-message-box-leaving-the-selected-method-unchanged"></a>Aby zamknąć okno komunikatu, pozostawiając wybranej metody bez zmian  
  
-   Kliknij przycisk **nr**.  
  
     Zamyka okno komunikatu i nie zostały zmienione.  
  
## <a name="see-also"></a>Zobacz także
[Komunikaty Projektanta obiektów relacyjnych](../data-tools/o-r-designer-messages.md)  
[LINQ do SQL narzędzi w programie Visual Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md)