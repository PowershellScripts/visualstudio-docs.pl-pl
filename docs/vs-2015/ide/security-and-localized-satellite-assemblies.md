---
title: Zabezpieczenia a zlokalizowane zestawy satelickie | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- key pairs for strong-named assemblies
- strong-named assemblies, security considerations
- satellite assemblies, localized
- code signing, assemblies
- security [Visual Studio], assemblies
- strong-named assemblies, localized
- assemblies [Visual Studio], security
- localization, satellite assemblies
ms.assetid: 6d953840-b301-47d5-8d34-30c1b29b5071
caps.latest.revision: 9
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: d817569a5f6709794b452fb5efe38d584669033f
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49218650"
---
# <a name="security-and-localized-satellite-assemblies"></a>Zabezpieczenia a zlokalizowane zestawy satelickie
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Jeśli zestaw głównych używa, silne nazwy, zestawy satelickie muszą być podpisane przy użyciu tego samego klucza prywatnego jako zestawu głównego. Jeśli klucz publiczny/prywatny, które pary jest niezgodny między głównym i zestawy satelickie, zasoby nie będą ładowane. Aby uzyskać więcej informacji na temat podpisywania zestawów, zobacz [porady: podpisywanie zestawu za pomocą silnej nazwy](http://msdn.microsoft.com/library/2c30799a-a826-46b4-a25d-c584027a6c67).  
  
 Ogólnie rzecz biorąc może być konieczne podpisywania grupy w organizacji lub zewnętrznego organizacji podpisywania, zaloguj się przy użyciu klucza prywatnego. Jest to spowodowane wrażliwych klucza prywatnego: dostęp do często jest ograniczony do kilku osób. Możesz użyć opóźnionego podpisywania w czasie projektowania. Aby uzyskać więcej informacji, zobacz [opóźnienie podpisywania zestawu](http://msdn.microsoft.com/library/9d300e17-5bf1-4360-97da-2aa55efd9070).  
  
## <a name="see-also"></a>Zobacz też  
 [Zagadnienia dotyczące zabezpieczeń zestawów](http://msdn.microsoft.com/library/1b5439c1-f3d5-4529-bd69-01814703d067)   
 [Główne pojęcia dotyczące zabezpieczeń](http://msdn.microsoft.com/library/3cfced4f-ea02-4e66-ae98-d69286363e98)   
 [Wprowadzenie do aplikacji międzynarodowych opartych na programie .NET Framework](../ide/introduction-to-international-applications-based-on-the-dotnet-framework.md)   
 [Lokalizowanie aplikacji](../ide/localizing-applications.md)   
 [Globalizowanie i lokalizowanie aplikacji](../ide/globalizing-and-localizing-applications.md)

