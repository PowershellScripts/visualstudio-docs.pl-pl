---
title: Uzyskiwanie dostępu do prywatnej chmury platformy Azure z programem Visual Studio | Dokumentacja firmy Microsoft
description: Dowiedz się, jak uzyskać dostęp do zasobów chmury prywatnej za pomocą programu Visual Studio.
author: ghogen
manager: douge
assetId: 9d733c8d-703b-44e7-a210-bb75874c45c8
ms.prod: visual-studio-dev15
ms.technology: vs-azure
ms.custom: vs-azure
ms.workload: azure-vs
ms.topic: conceptual
ms.date: 11/13/2017
ms.author: ghogen
ms.openlocfilehash: 23c9fa380238a489b59404e07eebdb80c6cb2ccc
ms.sourcegitcommit: e481d0055c0724d20003509000fd5f72fe9d1340
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/05/2018
ms.locfileid: "51000635"
---
# <a name="accessing-private-azure-clouds-with-visual-studio"></a>Uzyskiwanie dostępu do prywatnej chmury platformy Azure z programem Visual Studio

Domyślnie program Visual Studio obsługuje punkty końcowe REST platformy Azure w chmurze. W tym artykule dowiesz się, jak uzyskać dostęp i korzystać z chmury prywatnej w programie Visual Studio za pomocą certyfikatu chmury prywatnej.

1. W witrynie Azure portal w ramach chmury prywatnej Pobierz odpowiedni plik ustawień publikowania, lub skontaktuj się z administratorem, aby uzyskać plik ustawień publikowania. (Plik ma rozszerzenie `.publishsettings`.)

1. W programie Visual Studio **Eksploratora serwera**, kliknij prawym przyciskiem myszy **Azure** a następnie wybierz węzeł **subskrypcji filtru i Zarządzaj**.

    ![Zarządzanie subskrypcjami polecenia](./media/vs-azure-tools-access-private-azure-clouds-with-visual-studio/IC790778.png)

1. W **Zarządzanie subskrypcji platformy Microsoft Azure** okno dialogowe, wybierz opcję **certyfikaty** kartę, a następnie wybierz **importu**.

    ![Importowanie certyfikatów platformy Azure](./media/vs-azure-tools-access-private-azure-clouds-with-visual-studio/IC790779.png)

1. W **subskrypcji platformy Microsoft Azure Import** okno dialogowe, wybierz opcję **Przeglądaj**.

    ![Przeglądaj przycisk w oknie dialogowym Import subskrypcji platformy Microsoft Azure](./media/vs-azure-tools-access-private-azure-clouds-with-visual-studio/browse-button.png)

1. W **Otwórz** okno dialogowe, przejdź do katalogu, w którym został zapisany plik ustawień publikowania, wybierz plik, a następnie wybierz **Otwórz**.

    ![Wybierz plik ustawień publikowania](./media/vs-azure-tools-access-private-azure-clouds-with-visual-studio/select-publish-settings-file.png)

1. Po zwróceniu do **subskrypcji platformy Microsoft Azure Import** okno dialogowe, wybierz opcję **importu**.

    ![Importowanie pliku ustawień publikowania](./media/vs-azure-tools-access-private-azure-clouds-with-visual-studio/IC790780.png)

    Certyfikaty są zaimportowane z pliku ustawień publikowania w programie Visual Studio i możesz teraz wchodzić w interakcje z zasobami w chmurze prywatnej.

