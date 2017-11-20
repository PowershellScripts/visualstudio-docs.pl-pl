---
title: Zainstaluj program Visual Studio za serwerem zapory lub serwera proxy | Dokumentacja firmy Microsoft
description: 
ms.custom: 
ms.date: 08/01/2017
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-install
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- network installation, Visual Studio
- administrator guide, Visual Studio
- installing Visual Studio, administrator guide
- list of domains, locations, URLs
ms.assetid: 
author: TerryGLee
ms.author: tglee
manager: ghogen
ms.openlocfilehash: 4b203bbc3512ebc59a73a4e1420388a28fdf166b
ms.sourcegitcommit: 26419ab0cccdc30d279c32d6a841758cfa903806
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/11/2017
---
# <a name="install-visual-studio-behind-a-firewall-or-proxy-server"></a>Zainstaluj program Visual Studio za serwerem zapory lub serwera proxy

Instalator programu Visual Studio pobiera pliki z różnych domen i serwerów ich pobierania. Ta strona zawiera listę adresów URL domen, które możesz chcieć "dozwolone" jako zaufane w skryptach wdrożenia.

Jeśli to możliwe w danym środowisku, należy rozważyć dodanie następujących domen z protokołów HTTP i HTTPS.

## <a name="microsoft-domains"></a>Domeny firmy Microsoft
| Domain | Cel |
| ------ | ------- |
| go.microsoft.com | Rozpoznawanie adresu URL instalacji |
| aka.MS | Rozpoznawanie adresu URL instalacji |
| Download.VisualStudio.microsoft.com | Ustawienia lokalizacji pobierania pakietów |
| witrynie Download.microsoft.com | Ustawienia lokalizacji pobierania pakietów |
| Download.VisualStudio.com | Ustawienia lokalizacji pobierania pakietów |
| DL.xamarin.com | Ustawienia lokalizacji pobierania pakietów |
| visualstudiogallery.msdn.microsoft.com | Lokalizacja pobierania rozszerzenia programu Visual Studio |
| www.VisualStudio.com | Lokalizacja dokumentacji |
| docs.microsoft.com | Lokalizacja dokumentacji |
| MSDN.microsoft.com | Lokalizacja dokumentacji |
| www.microsoft.com | Lokalizacja dokumentacji |
| *.windows.net | Zaloguj się w lokalizacji |
| *.microsoftonline.com | Zaloguj się w lokalizacji |
| *.live.com | Zaloguj się w lokalizacji |


## <a name="non-microsoft-domains"></a>Domeny inne niż firmy Microsoft
| Domain | Instaluje te obciążenia |
| ------ | ------- |
| Archive.apache.org |  Tworzenie przenośnych za pomocą języka JavaScript <br />(Cordova) |
| cocos2d x.org | Tworzenie gier z C++ <br />(Cocos) |
| Download.epicgames.com | Tworzenie gier z C++ <br />(Aparatu unreal Engine) |
| Download.Oracle.com | Tworzenie przenośnych za pomocą języka JavaScript <br />(Java SDK) <br /><br />Programowanie przenośnych z platformą .NET <br />(Java SDK) |
| Download.unity3d.com | Tworzenie gier z Unity <br />(Unity) |
| netstorage.unity3d.com | Tworzenie gier z Unity <br /> (Unity) |
| DL.Google.com | Tworzenie przenośnych za pomocą języka JavaScript <br />(Zestaw SDK systemu android i zestawu NDK, Emulator) <br /><br />Programowanie przenośnych z platformą .NET <br />(Zestaw SDK systemu android i zestawu NDK, Emulator) |
| www.incredibuild.com | Tworzenie gier z C++ <br />(IncrediBuild) |
| incredibuildvs2017i.azureedge.NET | Tworzenie gier z C++ <br />(IncrediBuild) |
| www.Python.org | Tworzenie Python <br />(Python) <br /><br />Nauki dane i aplikacje analitycznych <br />(Python) |

## <a name="get-support"></a>Uzyskaj pomoc techniczną
Czasami może wystąpienia problemów. W przypadku niepowodzenia instalacji programu Visual Studio, zobacz [problemy dotyczące instalacji i uaktualniania Rozwiązywanie problemów z programu Visual Studio 2017](troubleshooting-installation-issues.md) stronę porady dotyczące rozwiązywania problemów. Jak również zgłosić problemy produktu z nami za pośrednictwem [zgłosić Problem](../ide/how-to-report-a-problem-with-visual-studio-2017.md) narzędzia w programie Visual Studio IDE lub udział sugestia z nami na [UserVoice](https://visualstudio.uservoice.com/forums/121579). Można śledzić problemy z produktu w [Visual Studio Developer Community](https://developercommunity.visualstudio.com/), zadawać pytania i odpowiedzi. Można również kontaktowaniu się z nami i innymi deweloperami Visual Studio za pomocą naszych [konwersacji programu Visual Studio w społeczności Gitter](https://gitter.im/Microsoft/VisualStudio) (wymaga [GitHub](https://github.com/) konta).

## <a name="see-also"></a>Zobacz także
* [Zainstaluj program Visual Studio 2017 r.](install-visual-studio.md)
* [Korzystanie z parametrów wiersza polecenia do zainstalowania programu Visual Studio 2017 r.](use-command-line-parameters-to-install-visual-studio.md)
  * [Przykłady parametru wiersza polecenia](command-line-parameter-examples.md)
  * [Obciążenie i identyfikator składnika odwołania](workload-and-component-ids.md)
* [Utwórz oparte na sieci instalację programu Visual Studio 2017 r.](create-a-network-installation-of-visual-studio.md)
  * [Zainstaluj certyfikaty wymagane do instalacji w trybie offline program Visual Studio](install-certificates-for-visual-studio-offline.md)
* [Proces instalacji programu Visual Studio przy użyciu pliku odpowiedzi](automated-installation-with-response-file.md)
* [Automatyczne stosowanie kluczy produktów podczas wdrażania programu Visual Studio](automatically-apply-product-keys-when-deploying-visual-studio.md)
* [Określ ustawienia domyślne dla wdrożeń w przedsiębiorstwie programu Visual Studio 2017 r.](set-defaults-for-enterprise-deployments.md)
* [Wyłącz lub Przenieś pamięć podręczną pakietów](disable-or-move-the-package-cache.md)
* [Aktualizacja Instalacja oparta na sieci programu Visual Studio](update-a-network-installation-of-visual-studio.md)
* [Aktualizacje kontroli wdrożeń programu Visual Studio 2017 r.](controlling-updates-to-visual-studio-deployments.md)
* [Narzędzia do wykrywania i Zarządzanie wystąpieniami programu Visual Studio](tools-for-managing-visual-studio-instances.md)