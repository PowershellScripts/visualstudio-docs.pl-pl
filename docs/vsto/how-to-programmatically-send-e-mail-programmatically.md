---
title: "Porady: programowane wysyłanie wiadomości E-Mail | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 02/02/2017
ms.reviewer: 
ms.suite: 
ms.technology: office-development
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- mail items [Office development in Visual Studio], sending e-mail
- Outlook [Office development in Visual Studio], creating e-mail
- Outlook [Office development in Visual Studio], sending e-mail
- e-mail [Office development in Visual Studio], sending
ms.assetid: 4fa0e1b5-2caf-4a11-8626-df643b23f5f0
caps.latest.revision: "18"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 98b0eefafa86fdaf8f7a664ac75a2f7c71a43549
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-programmatically-send-e-mail"></a>Porady: programowane wysyłanie wiadomości E-Mail  
  W tym przykładzie wysyła wiadomość e-mail do kontaktów, które mają nazwy domeny **example.com** w ich adresów e-mail.  
  
 [!INCLUDE[appliesto_olkallapp](../vsto/includes/appliesto-olkallapp-md.md)]  
  
## <a name="example"></a>Przykład  
 [!code-csharp[Trin_OL_ProgramEmail#1](../vsto/codesnippet/CSharp/Trin_OL_ProgramEMail/thisaddin.cs#1)]  
  
## <a name="compiling-the-code"></a>Kompilowanie kodu  
 Ten przykład wymaga:  
  
-   Kontakty, które mają nazwy domeny **example.com** w ich adresów e-mail.  
  
## <a name="robust-programming"></a>Niezawodne programowanie  
 Nie usuwaj kod filtru, która szuka nazwy domeny **example.com**. Rozwiązanie będzie wysyłać wiadomości e-mail do wszystkich kontaktów, po usunięciu filtru.  
  
## <a name="see-also"></a>Zobacz też  
 [Praca z elementami poczty](../vsto/working-with-mail-items.md)   
 [Porady: programowane Tworzenie elementu poczty E-Mail](../vsto/how-to-programmatically-create-an-e-mail-item.md)   
 [Porady: programowane dostęp do kontaktów programu Outlook](../vsto/how-to-programmatically-access-outlook-contacts.md)   
 [Porady: programowane wykonywanie akcji po odebraniu wiadomości E-Mail](../vsto/how-to-programmatically-perform-actions-when-an-e-mail-message-is-received.md)  
  
  