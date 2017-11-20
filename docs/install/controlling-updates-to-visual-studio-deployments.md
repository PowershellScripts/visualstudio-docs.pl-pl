---
title: "Kontrolowanie aktualizacji do wdrożenia programu Visual Studio | Dokumentacja firmy Microsoft"
description: "{{SYMBOL ZASTĘPCZY}}"
ms.date: 08/14/2017
ms.reviewer: tims
ms.suite: 
ms.technology: vs-ide-install
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- '{{PLACEHOLDER}}'
- '{{PLACEHOLDER}}'
ms.assetid: 35C7AB05-07D5-4B38-BCAC-AB88444E7368
author: timsneath
ms.author: tglee
manager: ghogen
ms.openlocfilehash: 72e217f8543b6b150cc0587c36fac692e150179d
ms.sourcegitcommit: 26419ab0cccdc30d279c32d6a841758cfa903806
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/11/2017
---
# <a name="control-updates-to-network-based-visual-studio-deployments"></a>Formant aktualizacje do wdrożenia oparte na sieci programu Visual Studio

Administratorzy przedsiębiorstwa często Utwórz układ i udostępnić go w sieciowym udziale plików do wdrożenia na ich użytkowników końcowych.

## <a name="controlling-where-visual-studio-looks-for-updates"></a>Kontrolowanie, których wyszukuje aktualizacje programu Visual Studio
Domyślnie program Visual Studio w dalszym ciągu wyszukiwania w trybie online aktualizacje, nawet jeśli instalacja została wdrożona z udziału sieciowego. Jeśli jest dostępna aktualizacja, użytkownik może go zainstalować. Zaktualizowanej zawartości, która nie znajduje się w układzie w trybie offline jest pobierana z sieci web.

Jeśli ma bezpośrednią kontrolę nad którym wyszukuje aktualizacje programu Visual Studio, można zmodyfikować lokalizacji, w którym wygląda. Można też kontrolować wersję, z której użytkownicy są aktualizowane w celu. Aby to zrobić, wykonaj następujące kroki:

 1. Utwórz układ w trybie offline:
    ```
    vs_enterprise.exe --layout C:\vs2017offline --lang en-US
    ```
 2. Skopiuj go do udziału plików, w którym chcesz udostępnić go:
    ```
    xcopy /e C:\vs2017offline \\server\share\VS2017
    ```
 3. Modyfikowanie pliku response.json układ i zmiana `channelUri` wartość, aby wskazać kopię channelManifest.json, która kontroluje, administrator.

  Pamiętaj wprowadzić ukośników odwrotnych w wartości, jak w poniższym przykładzie:

  ```json
    "channelUri":"\\\\server\\share\\VS2017\\ChannelManifest.json"
  ```

 Teraz użytkownicy końcowi mogą uruchomić Instalatora z tego udziału, aby zainstalować program Visual Studio.
    ```
    \\server\share\VS2017\vs_enterprise.exe
    ```

Gdy administrator przedsiębiorstwa określa nadszedł czas na rzecz własnych użytkowników zaktualizować do nowszej wersji programu Visual Studio, mogą one [zaktualizować lokalizację układu](update-a-network-installation-of-visual-studio.md) uwzględnienie zaktualizowane pliki w następujący sposób.

 1. Polecenie, które jest podobny do następującego polecenia:
    ```
    vs_enterprise.exe --layout \\server\share\VS2017 --lang en-US
    ```
 2. Sprawdź, czy plik response.json w układzie zaktualizowane nadal zawiera dostosowania, w szczególności modyfikacji channelUri w następujący sposób:
    ```json
    "channelUri":"\\\\server\\share\\VS2017\\ChannelManifest.json"
    ```
 Istniejące Visual Studio instaluje plik z tego układu Wyszukaj aktualizacje w `\\server\share\VS2017\ChannelManifest.json`. Jeśli channelManifest.json jest nowsza niż co użytkownik zainstalował, Visual Studio informuje użytkownika, że dostępna jest aktualizacja.

 Instaluje nowy automatycznie zainstalować zaktualizowaną wersję programu Visual Studio bezpośrednio z układu.

## <a name="controlling-notifications-in-the-visual-studio-ide"></a>Kontrolowanie powiadomień w programie Visual Studio IDE
Visual Studio sprawdza lokalizacji, w którym został zainstalowany, takich jak udziału sieciowego lub Internetu, aby zobaczyć, czy są dostępne aktualizacje, zgodnie z wcześniejszym opisem. Po udostępnieniu aktualizacji programu Visual Studio powiadamia użytkownika przy użyciu flagi powiadomienia w prawym górnym rogu okna.

 ![Flaga powiadomienia aktualizacji](media/notification-flag.png)

Jeśli nie chcesz, aby użytkownicy końcowi, aby otrzymywać powiadomienia o aktualizacjach, można wyłączyć powiadomień. (Na przykład możesz wyłączyć powiadomienia, jeśli dostarczania aktualizacji za pomocą mechanizmu dystrybucji oprogramowania centralnej.)

Ponieważ program Visual Studio 2017 [są przechowywane wpisy rejestru w rejestrze prywatnej](tools-for-managing-visual-studio-instances.md#editing-the-registry-for-a-visual-studio-instance), nie bezpośredniego edytowania rejestru w typowy sposób. Jednak program Visual Studio obejmuje `vsregedit.exe` narzędzie, które służy do zmiany ustawienia programu Visual Studio. Można wyłączyć powiadomień za pomocą następującego polecenia:

```cmd
vsregedit.exe set "C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise" HKCU ExtensionManager AutomaticallyCheckForUpdates2Override dword 0
```
(Upewnij się zastąpić katalogu, aby dopasować zainstalowane wystąpienie, które chcesz edytować.)

> [!TIP]
> Użyj [vswhere.exe](tools-for-managing-visual-studio-instances.md#detecting-existing-visual-studio-instances) można znaleźć określonego wystąpienia programu Visual Studio na stacji roboczej klienta.

## <a name="get-support"></a>Uzyskaj pomoc techniczną
Czasami może wystąpienia problemów. W przypadku niepowodzenia instalacji programu Visual Studio, zobacz [problemy dotyczące instalacji i uaktualniania Rozwiązywanie problemów z programu Visual Studio 2017](troubleshooting-installation-issues.md) stronę porady dotyczące rozwiązywania problemów. Jak również zgłosić problemy produktu z nami za pośrednictwem [zgłosić Problem](../ide/how-to-report-a-problem-with-visual-studio-2017.md) narzędzia w programie Visual Studio IDE lub udział sugestia z nami na [UserVoice](https://visualstudio.uservoice.com/forums/121579). Można śledzić problemy z produktu w [Visual Studio Developer Community](https://developercommunity.visualstudio.com/), zadawać pytania i odpowiedzi. Można również kontaktowaniu się z nami i innymi deweloperami Visual Studio za pomocą naszych [konwersacji programu Visual Studio w społeczności Gitter](https://gitter.im/Microsoft/VisualStudio) (wymaga [GitHub](https://github.com/) konta).

## <a name="see-also"></a>Zobacz także
* [Zainstaluj program Visual Studio](install-visual-studio.md)
* [Przewodnik administratora w usłudze Visual Studio](visual-studio-administrator-guide.md)
* [Korzystanie z parametrów wiersza polecenia do zainstalowania programu Visual Studio](use-command-line-parameters-to-install-visual-studio.md)
* [Narzędzia do zarządzania wystąpieniami programu Visual Studio](tools-for-managing-visual-studio-instances.md)