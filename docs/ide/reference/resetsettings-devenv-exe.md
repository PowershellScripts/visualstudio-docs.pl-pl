---
title: -ResetSettings (devenv.exe)
ms.date: 11/16/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
helpviewer_keywords:
- Devenv, /ResetSettings switch
- ResetSettings switch
- /ResetSettings Devenv switch
ms.assetid: 1d41021c-6f58-4bd5-b122-d1c995812192
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 568a829ff10cbee535729361b7c95dd7db6814f5
ms.sourcegitcommit: 54c65f81a138fc1e8ff1826f7bd9dcec710618cc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/19/2018
ms.locfileid: "51948072"
---
# <a name="resetsettings-devenvexe"></a>/ResetSettings (devenv.exe)

Przywraca ustawienia domyślne programu Visual Studio i automatycznie uruchamia IDE programu Visual Studio. Opcjonalnie resetuje ustawienia do określonego *vssettings* pliku.

Ustawienia domyślne są określane przez profil, który został wybrany, gdy program Visual Studio najpierw została uruchomiona.

> [!TIP]
> Aby dowiedzieć się, jak zresetować ustawienia za pomocą zintegrowanego środowiska programistycznego (IDE), zobacz [zresetować ustawienia](../synchronized-settings-in-visual-studio.md#reset-settings).

## <a name="syntax"></a>Składnia

```cmd
Devenv /ResetSettings SettingsFile
```

## <a name="arguments"></a>Argumenty

`SettingsFile`

Pełna ścieżka i nazwa *vssettings* pliku, aby zastosować do programu Visual Studio.

Aby przywrócić profil ogólne ustawienia projektowe, użyj `General`.

## <a name="remarks"></a>Uwagi

Jeśli nie `SettingsFile` jest określona, zostanie wyświetlony monit o wybór domyślnej kolekcji ustawień przy następnym uruchomieniu programu Visual Studio.

## <a name="example"></a>Przykład

Następujący wiersz polecenia powoduje zastosowanie ustawień przechowywanych w pliku `MySettings.vssettings`.

```cmd
Devenv.exe /ResetSettings "C:\My Files\MySettings.vssettings"
```

## <a name="see-also"></a>Zobacz także

- [Resetuj ustawienia](../synchronized-settings-in-visual-studio.md#reset-settings)
- [Personalizowanie środowiska IDE programu Visual Studio](../../ide/personalizing-the-visual-studio-ide.md)
- [Przełączniki wiersza polecenia Devenv](../../ide/reference/devenv-command-line-switches.md)