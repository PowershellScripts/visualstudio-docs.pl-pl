---
title: Modyfikowanie Visual Studio 2017 | Dokumentacja firmy Microsoft
description: "Dowiedz się, jak zmodyfikuj program Visual Studio, krok po kroku."
ms.custom: H1Hack27Feb2017
ms.date: 11/08/2017
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-install
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- modify Visual Studio
- change visual studio
- changing Visual Studio
- customize Visual Studio
ms.assetid: 3399ea7b-a291-4a9e-80a1-b861a21afa1d
author: TerryGLee
ms.author: tglee
manager: ghogen
ms.openlocfilehash: d35d3e5b58ad9aed66bd85f445f03b28a931a725
ms.sourcegitcommit: 26419ab0cccdc30d279c32d6a841758cfa903806
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/11/2017
---
# <a name="modify-visual-studio-2017-by-adding-or-removing-workloads-and-components"></a>Modyfikowanie Visual Studio 2017 przez dodanie lub usunięcie obciążeń i składniki
Nie tylko ma wprowadziliśmy łatwiej można spersonalizować Visual Studio, aby dopasować zadań, należy wykonać, wprowadziliśmy również go łatwiej zbyt Dostosowywanie programu Visual Studio. Nie więcej w Panelu sterowania, aby to zrobić; Zamiast tego należy uruchomić nowy Instalator programu Visual Studio i wprowadź żądane zmiany.

Poniżej przedstawiono sposób.  

## <a name="modify-workloads"></a>Modyfikowanie obciążeń  
 Obciążeń zawiera funkcje, które należy do programowania języka lub platformy, którego używasz. Zmodyfikować Visual Studio, dzięki czemu obsługuje pracę, którą chcesz wykonać, jeśli chcesz to zrobić za pomocą obciążeń.  

>[!IMPORTANT]
>Aby zainstalować, zaktualizować lub zmodyfikuj program Visual Studio, musisz zalogować się przy użyciu konta z uprawnieniami administracyjnymi. Aby uzyskać więcej informacji, zobacz [uprawnienia użytkownika i programu Visual Studio](../ide/user-permissions-and-visual-studio.md).

1.  Instalator programu Visual Studio odnaleźć na tym komputerze.  

     Na przykład na komputerze z systemem Windows 10 Anniversary Update, wybierz pozycję **Start**, a następnie przewiń do literę **V**, w którym znajduje się w **Instalator programu Visual Studio**.  

     ![Instalator programu Visual Studio](media/vs2017-locate-the-visual-studio-installer.PNG "zlokalizować Instalator programu Microsoft Visual Studio")

     >[!NOTE]
     Na niektórych komputerach, Instalator programu Visual Studio może być wyświetlany poniżej literę **"M"** jako **Microsoft Visual Studio Instalatora**.<br/><br/> Alternatywnie Instalator programu Visual Studio można znaleźć w następującej lokalizacji:`C:\Program Files (x86)\Microsoft Visual Studio\Installer\vs_installer.exe`

2.  Kliknij lub naciśnij, aby uruchomić Instalatora, a następnie wybierz **Modyfikuj**.  

     ![Uruchom lub zmodyfikuj program Visual Studio](media/vs2017-modify.PNG "zmodyfikować 2017 Visual Studio")  

3.  Z **obciążeń** ekranu, zaznacz lub odznacz obciążeń, które chcesz zainstalować lub odinstalować.  

    ![Okno dialogowe programu Visual Studio 2017 ustawienia](media/vs2017-modify-workloads.PNG "wybierz obciążenie w Visual Studio 2017 r.")

4. Kliknij lub naciśnij polecenie **Modyfikuj** ponownie.  

5. Po zainstalowaniu nowego obciążeń i składników, kliknij przycisk **uruchamianie**.

## <a name="modify-individual-components"></a>Zmodyfikować poszczególne składniki

Jeśli nie chcesz dostosować instalację programu Visual Studio, wybierz za pomocą funkcji przydatną obciążeń **pojedynczych składników** z Instalator programu Visual Studio, wybierz, co użytkownik ma, a następnie wykonaj monitów.  

## <a name="get-support"></a>Uzyskaj pomoc techniczną
Czasami może wystąpienia problemów. W przypadku niepowodzenia instalacji programu Visual Studio, zobacz [problemy dotyczące instalacji i uaktualniania Rozwiązywanie problemów z programu Visual Studio 2017](troubleshooting-installation-issues.md) stronę porady dotyczące rozwiązywania problemów. Jak również zgłosić problemy produktu z nami za pośrednictwem [zgłosić Problem](../ide/how-to-report-a-problem-with-visual-studio-2017.md) narzędzia w programie Visual Studio IDE lub udział sugestia z nami na [UserVoice](https://visualstudio.uservoice.com/forums/121579). Można śledzić problemy z produktu w [Visual Studio Developer Community](https://developercommunity.visualstudio.com/), zadawać pytania i odpowiedzi. Można również kontaktowaniu się z nami i innymi deweloperami Visual Studio za pomocą naszych [konwersacji programu Visual Studio w społeczności Gitter](https://gitter.im/Microsoft/VisualStudio) (wymaga [GitHub](https://github.com/) konta).

## <a name="see-also"></a>Zobacz także
* [Zainstaluj program Visual Studio 2017 r.](install-visual-studio.md)
* [Aktualizacja programu Visual Studio 2017 r.](update-visual-studio.md)
* [Odinstaluj program Visual Studio 2017 r.](uninstall-visual-studio.md)
* [Jak zgłosić Problem z programu Visual Studio 2017 r.](../ide/how-to-report-a-problem-with-visual-studio-2017.md)