---
title: Zabezpieczenia a zlokalizowane zestawy satelickie | Dokumentacja firmy Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
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
caps.latest.revision: "8"
author: kempb
ms.author: kempb
manager: ghogen
ms.openlocfilehash: fc8579d18f1d3f0314bab99698024e463b51454b
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="security-and-localized-satellite-assemblies"></a>Zabezpieczenia a zlokalizowane zestawy satelickie
Jeśli Twoje główny zestaw używa silne nazwy, zestawów satelickich muszą być podpisane przy użyciu tego samego klucza prywatnego jako główny zestaw. Jeśli klucz publiczny i prywatny pary różni się od głównego i zestawy satelickie, zasobów nie zostanie załadowany. Aby uzyskać więcej informacji na zestawy podpisywania, zobacz [porady: podpisać zestaw o silnej nazwie](/dotnet/framework/app-domains/how-to-sign-an-assembly-with-a-strong-name).  
  
 Ogólnie rzecz biorąc należy do grupy podpisywania firmy lub organizacji zewnętrznych podpisywania, zaloguj się przy użyciu klucza prywatnego. Jest to spowodowane wrażliwych klucza prywatnego: dostęp do często jest ograniczony do kilku osób. Możesz użyć podpisywanie opóźnione podczas programowania. Aby uzyskać więcej informacji, zobacz [opóźnione podpisywanie zestawu](/dotnet/framework/app-domains/delay-sign-assembly).  
  
## <a name="see-also"></a>Zobacz też  
 [Zagadnienia dotyczące zabezpieczeń zestawów](/dotnet/framework/app-domains/assembly-security-considerations)   
 [Główne pojęcia dotyczące zabezpieczeń](/dotnet/standard/security/key-security-concepts)   
 [Wprowadzenie do aplikacji międzynarodowych oparte na programie .NET Framework](../ide/introduction-to-international-applications-based-on-the-dotnet-framework.md)   
 [Lokalizowanie aplikacji](../ide/localizing-applications.md)   
 [Globalizacja i lokalizacja aplikacji](../ide/globalizing-and-localizing-applications.md)