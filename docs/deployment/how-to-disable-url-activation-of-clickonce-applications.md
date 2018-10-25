---
title: 'Porady: wyłączanie aktywacji adresu URL aplikacji ClickOnce | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-deployment
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- disallowUrlActivation
- URL activation, ClickOnce applications
- ClickOnce deployment, URL activation
ms.assetid: db31a16b-960f-4264-91d7-c7c40f876068
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 9ab9204513c59d2c853c0a3738ef2363739d56c1
ms.sourcegitcommit: 551f13774e8bb0eb47cbd973745628a956e866aa
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/19/2018
ms.locfileid: "49459624"
---
# <a name="how-to-disable-url-activation-of-clickonce-applications"></a>Porady: wyłączanie aktywacji adresu URL aplikacji ClickOnce

Zazwyczaj [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] aplikacji zostanie automatycznie uruchomiony natychmiast, po zakończeniu instalacji z serwera sieci Web. Ze względów bezpieczeństwa może zdecydować wyłączyć to zachowanie i poinformuj użytkowników, aby uruchomić aplikację z **Start** menu zamiast tego. Poniższa procedura opisuje sposób wyłączanie aktywacji adresu URL.

Ta technika może zostać użyta tylko w przypadku [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] aplikacji zainstalowanych na komputerze użytkownika z serwera sieci Web. Nie można używać dla aplikacji tylko w trybie online, które można uruchamiać tylko przy użyciu swojego adresu URL. Aby uzyskać więcej informacji na temat różnią się tylko w trybie online i zainstalowanych aplikacji, zobacz [Wybieranie strategii wdrażania ClickOnce](../deployment/choosing-a-clickonce-deployment-strategy.md).

Ta procedura korzysta z narzędzia Windows Software Development Kit (SDK) MageUI.exe. Aby uzyskać więcej informacji na temat tego narzędzia, zobacz [MageUI.exe (Manifest Generation i graficzny klient Editing Tool)](/dotnet/framework/tools/mageui-exe-manifest-generation-and-editing-tool-graphical-client). Można również wykonać tę procedurę przy użyciu programu Visual Studio.

## <a name="procedure"></a>Procedura

### <a name="to-disable-url-activation-for-your-application"></a>Aby wyłączanie aktywacji adresu URL aplikacji

1.  Otwórz manifest wdrożenia w MageUI.exe. Jeśli użytkownik jeszcze nie utworzono jedną, wykonaj kroki opisane w [wskazówki: ręczne wdrażanie aplikacji ClickOnce](../deployment/walkthrough-manually-deploying-a-clickonce-application.md).

2.  Wybierz **opcje wdrażania** kartę.

3.  Wyczyść **automatycznie uruchomić aplikacji po zainstalowaniu** pole wyboru.

4.  Zapisz i podpisać manifest.

## <a name="see-also"></a>Zobacz także

- [Publikowanie aplikacji ClickOnce](../deployment/publishing-clickonce-applications.md)