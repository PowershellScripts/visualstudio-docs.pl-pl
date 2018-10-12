---
title: Zarządzanie pakietami VSPackage | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- VSPackages, autoloading
- VSPackages, delayed loading
- delay loading
- VSPackages, loading
ms.assetid: 386e0ce5-4107-4164-b0cd-1cf43eb5e7cf
caps.latest.revision: 36
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 5b68ad8fb8ce32c2a4a1210d38fb458518d28435
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49296351"
---
# <a name="managing-vspackages"></a>Zarządzanie pakietami VSPackage
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

W większości przypadków nie trzeba martwić się o zarządzaniu pakietami VSPackage, ponieważ szablony projektów i elementów Zarejestruj i automatycznie załadować pakietu. Jednak w niektórych sytuacjach konieczne może się nieco więcej, aby można było zarządzać pakietu.  
  
## <a name="using-the-experimental-instance"></a>Za pomocą wystąpienie eksperymentalne  
 Aby dowiedzieć się więcej na temat wystąpienia eksperymentalnego, zobacz [wystąpienie doświadczalne](../extensibility/the-experimental-instance.md).  
  
## <a name="registering-and-unregistering-vspackages"></a>Rejestrowanie i wyrejestrowywanie pakietów VSPackage  
 Aby dowiedzieć się, jak rejestrowanie i wyrejestrowywanie pakietów VSPackage i innych rodzajów rozszerzenia, zobacz [rejestrowanie i wyrejestrowywanie pakietów VSPackage](../extensibility/registering-and-unregistering-vspackages.md).  
  
## <a name="loading-a-vspackage"></a>Ładowanie pakietu VSPackage  
 Pakietów VSPackage, który można ustawić automatyczne ładowanie podczas określonego identyfikatora GUID CMDUICONTEXT jest włączone. Aby uzyskać więcej informacji, zobacz [ładowanie pakietów VSPackage](../extensibility/loading-vspackages.md).  
  
## <a name="using-asyncpackage-to-load-vspackages-in-the-background"></a>Za pomocą AsyncPackage do ładowania pakietów VSPackages w tle  
 Klasy AsyncPackage włącza pakiet ładowanie w wątku w tle dla szybsza reakcja interfejsu użytkownika w programie Visual Studio. Aby uzyskać więcej informacji, zobacz [porady: użycie AsyncPackage do ładowania VSPackages w tle](../extensibility/how-to-use-asyncpackage-to-load-vspackages-in-the-background.md).  
  
## <a name="rule-based-ui-context-for-extensions"></a>Oparty na regułach kontekstu interfejsu użytkownika dla rozszerzenia  
 Konteksty interfejsu użytkownika opartego na regułach umożliwia autorom rozszerzenia do definiowania dokładne warunki, na jakich kontekstu interfejsu użytkownika jest aktywowany, a następnie załadować skojarzonych pakietów VSPackage. Aby uzyskać więcej informacji, zobacz [jak: oparty na regułach Użyj kontekstu interfejsu użytkownika dla rozszerzenia programu Visual Studio](../extensibility/how-to-use-rule-based-ui-context-for-visual-studio-extensions.md).  
  
## <a name="troubleshooting-vspackages"></a>Rozwiązywanie problemów z pakietami VSPackage  
 Dowiedz się, techniki rozwiązywania problemów z pakietami VSPackage, które nie są ładowane lub występują błędy: [Rozwiązywanie problemów z pakietami VSPackage](../extensibility/troubleshooting-vspackages.md)  
  
## <a name="see-also"></a>Zobacz też  
 [Pakiety VSPackage](../extensibility/internals/vspackages.md)

