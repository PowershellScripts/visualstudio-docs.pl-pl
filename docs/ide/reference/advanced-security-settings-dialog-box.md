---
title: Zaawansowane ustawienia zabezpieczeń — Okno dialogowe
ms.date: 06/27/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- vs.err.debug_in_zone_no_hostproc
helpviewer_keywords:
- Advanced Security Settings dialog box
ms.assetid: 2e7aefe9-6d20-4f3e-b257-aee1ebcc6f5d
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: dce482f53f9f3e6dd0b57d6cb905f97cdfaa601a
ms.sourcegitcommit: 5b767247b3d819a99deb0dbce729a0562b9654ba
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/20/2018
ms.locfileid: "39180519"
---
# <a name="advanced-security-settings-dialog-box"></a>Zaawansowane ustawienia zabezpieczeń — Okno dialogowe

To okno dialogowe umożliwia określenie ustawień zabezpieczeń dotyczące debugowania w strefie.

![Okno dialogowe Zaawansowane ustawienia zabezpieczeń w programie Visual Studio](../media/advanced-security-settings.png)

Aby otworzyć to okno dialogowe, wybierz węzeł projektu w **Eksploratora rozwiązań**, a następnie na **projektu** menu, kliknij przycisk **właściwości**. Podczas **projektanta projektu** zostanie wyświetlona, kliknij przycisk **zabezpieczeń** kartę. Na **zabezpieczeń** wybierz opcję **włączenia ustawień zabezpieczeń technologii ClickOnce**, kliknij przycisk **to częściowo zaufanych aplikacji**, a następnie kliknij przycisk **zaawansowane**.

## <a name="uielement-list"></a>Lista elementów interfejsu użytkownika

**Przyznać aplikacji dostęp do witryny pochodzenia**

Jeśli wybierzesz to pole wyboru, aplikacja może wykorzystywać udziału witryny sieci Web lub serwera, na którym została opublikowana. Domyślnie ta opcja jest zaznaczona.

**Debuguj aplikację tak, jakby zostały pobrane z następującego adresu URL**

Jeśli trzeba umożliwić aplikacji dostęp do witryny sieci Web lub serwera udziału odpowiadający **adres URL instalacji** określone na **Publikuj** wpisz tutaj tego adresu URL. Ta opcja jest dostępna tylko wtedy, gdy **przyznać aplikacji dostęp do witryny pochodzenia** jest zaznaczone.

## <a name="see-also"></a>Zobacz także

- [Strona zabezpieczeń, Projektant projektu](../../ide/reference/security-page-project-designer.md)