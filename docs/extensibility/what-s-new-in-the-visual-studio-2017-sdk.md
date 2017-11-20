---
title: Jaki &#39; s nowego w Visual Studio 2017 SDK | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 10/31/2017
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 9efcf0a3-dbde-4cab-8ed3-425826a48b2e
caps.latest.revision: "1"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 0be477d54ffeab52c415890c7d95447fa3f55ffc
ms.sourcegitcommit: fb751e41929f031d1a9247bc7c8727312539ad35
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 11/15/2017
---
# <a name="what39s-new-in-the-visual-studio-2017-sdk"></a>Jaki &#39; s nowego w Visual Studio 2017 SDK

Visual Studio SDK ma następujące nowe i zaktualizowane funkcje dla programu Visual Studio 2017 r.

## <a name="vsix-v3-format"></a>VSIX v3 format

Aby umożliwić obsługę nowych instalacji Visual Studio 2017 lekki, format manifestu rozszerzenia VSIX została zaktualizowana w wersji 3 (VSIX v3).

Nowy format ma obsługę:

* Jawne zadeklarowanie wymagania wstępne i instalowane przez VSIXInstaller.
* Zestawy Ngen'ing w instalacji rozszerzenia.
* Instalowanie zasobów poza głównym zwykle rozszerzenia.

Aby dowiedzieć się więcej o tych zmianach, zobacz następujące tematy:

* [Zmiany do rozszerzenia dla 2017](breaking-changes-2017.md)
* [Obsługa ngen w pliku VSIX w wersji 3](ngen-support.md)
* [Instalowanie znajduje się poza folderem rozszerzeń](set-install-root.md)
* [Często zadawane pytania dla rozszerzalności programu Visual Studio 2017 r.](faq-2017.md)

## <a name="migrating-extensibility-project-to-visual-studio-2017"></a>Migrowanie rozszerzalność projektu do programu Visual Studio 2017 r.

Aby dowiedzieć się, jak zaktualizować rozszerzalności projektów i ich manifestów VSIX do programu Visual Studio 2017, zobacz [porady: Migracja projektów rozszerzalności programu Visual Studio 2017](how-to-migrate-extensibility-projects-to-visual-studio-2017.md).

## <a name="custom-project-and-item-templates"></a>Niestandardowych szablonów projektów i elementów

Począwszy od programu Visual Studio 2017 skanowanie w poszukiwaniu szablony niestandardowe projektów i elementów zostaną już wykonane. Zamiast tego rozszerzenia, należy podać manifestu plików szablonów, które opisują lokalizację instalacji tych szablonów. Można użyć programu Visual Studio 2017 można zaktualizować rozszerzenia VSIX. W przypadku wdrożenia przy użyciu Instalatora MSI rozszerzenie, należy ręcznie wygenerować pliki manifestu szablonu. Aby uzyskać więcej informacji, zobacz [uaktualniania niestandardowe szablony projektów i elementów dla programu Visual Studio 2017](../extensibility/upgrading-custom-project-and-item-templates-for-visual-studio-2017.md). Schemat manifestu szablonu jest udokumentowany w [programu Visual Studio manifestu odwołanie do schematu szablonu](../extensibility/visual-studio-template-manifest-schema-reference.md).

## <a name="updated-extension-performance-guidelines"></a>Wskazówki dotyczące wydajności zaktualizowane rozszerzenia

Jest dostępna nowa [porady: diagnozowania wydajności rozszerzenia](how-to-diagnose-extension-performance.md) tematu w obszarze [Zarządzanie VSPackages](managing-vspackages.md) demonstrujące sposób wykrywania i analizować rozszerzenia wpływ na Visual Studio uruchamianie i rozwiązanie załadować razy.