---
title: "Tworzenie w trybie Offline instalację programu Visual Studio | Dokumentacja firmy Microsoft"
description: "Dowiedz się, jak zainstalować program Visual Studio w trybie offline."
ms.custom: 
ms.date: 08/30/2017
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-install
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- offline installation [Visual Studio]
- offline install [Visual Studio]
- layout [Visual Studio]
ms.assetid: f8625d5e-f6ea-4db0-83c0-619b77fab3cf
author: TerryGLee
ms.author: tglee
manager: ghogen
ms.openlocfilehash: 8b0902c7e2d3c2b51ecd915647a3e8a03e49c641
ms.sourcegitcommit: 26419ab0cccdc30d279c32d6a841758cfa903806
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/11/2017
---
# <a name="create-an-offline-installation-of-visual-studio-2017"></a>Tworzenie w trybie offline instalację programu Visual Studio 2017 r.

Firma Microsoft zaprojektowane Instalator Visual Studio 2017 działają poprawnie w różnych warunków, sieci i komputera.

- Nowy model oparte na obciążeniu oznacza, że należy pobrać daleko mniejszej niż w poprzednich wersjach programu Visual Studio: małego 300 MB do najmniejszego instalacji;
- W porównaniu do ogólnego "ISO" lub plik zip, możemy pobrać tylko pakiety, które są potrzebne dla maszyny. Na przykład firma Microsoft nie pobieraj plików 64-bitowych, jeśli nie są potrzebne;
- W procesie instalacji spróbujemy trzy technologie różnych pobierania (WebClient, Usługa BITS i WinInet) aby zminimalizować zakłócenia oprogramowania antywirusowego i serwera proxy;
- Pliki, musisz zainstalować program Visual Studio są dystrybuowane w sieci dostarczania globalnych, dlatego firma Microsoft może udostępnić je użytkownikom z lokalnego serwera.

Zalecamy wypróbowanie [Instalator sieci web programu Visual Studio](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocsOL)&mdash;naszym zdaniem znajdziesz ją dobrej obsługi.

 > [!div class="button"]
 > [Pobierz program Visual Studio 2017 r.](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocsOL)
<br/>

Jeśli chcesz zainstalować w trybie offline, ponieważ połączenie z Internetem jest niedostępne lub zawodnych, patrz [zainstalować program Visual Studio 2017 o niskiej przepustowości lub zawodnych w środowiskach sieci](../install/install-vs-inconsistent-quality-network.md). Polecenie umożliwia utworzenie lokalnej pamięci podręcznej plików trzeba wykonać instalację w trybie offline. Ten proces zastępuje pliki ISO dostępne w poprzednich wersjach.

> [!NOTE]
> Jeśli jesteś administratorem przedsiębiorstwa, który chce wykonać wdrożenie programu Visual Studio 2017 klienckich stacjach roboczych, które są zaporą z siecią Internet, zobacz nasze [Tworzenie instalacji sieciowej programu Visual Studio 2017](../install/create-a-network-installation-of-visual-studio.md) i [Uwagi dotyczące instalowania programu Visual Studio w środowisku offline](../install/install-visual-studio-in-offline-environment.md) stron.

## <a name="get-support"></a>Uzyskaj pomoc techniczną
Czasami może wystąpienia problemów. W przypadku niepowodzenia instalacji programu Visual Studio, zobacz [problemy dotyczące instalacji i uaktualniania Rozwiązywanie problemów z programu Visual Studio 2017](troubleshooting-installation-issues.md) stronę porady dotyczące rozwiązywania problemów. Jak również zgłosić problemy produktu z nami za pośrednictwem [zgłosić Problem](../ide/how-to-report-a-problem-with-visual-studio-2017.md) narzędzia w programie Visual Studio IDE lub udział sugestia z nami na [UserVoice](https://visualstudio.uservoice.com/forums/121579). Można śledzić problemy z produktu w [Visual Studio Developer Community](https://developercommunity.visualstudio.com/), zadawać pytania i odpowiedzi. Można również kontaktowaniu się z nami i innymi deweloperami Visual Studio za pomocą naszych [konwersacji programu Visual Studio w społeczności Gitter](https://gitter.im/Microsoft/VisualStudio) (wymaga [GitHub](https://github.com/) konta).