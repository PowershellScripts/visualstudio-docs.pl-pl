---
title: Szablon zasad i okno właściwości | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- Properties window, template policy
ms.assetid: 1d8019d3-5e57-47ba-b358-526b0796a63b
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 8cf24f6f769ea9344d2a7716856e3c84fdf122de
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49816329"
---
# <a name="template-policy-and-the-properties-window"></a>Szablon zasad i okno właściwości
Gdy projekt znajduje się wewnątrz szablonu projektu w przedsiębiorstwie, tego szablonu projektu przedsiębiorstwa mogą wymusić zasady. Szablon zasad staje się ograniczający system, który może służyć do ustawiania wartości domyślnej właściwości, Ukryj właściwości, dodać właściwości i tak dalej.  
  
 Za pomocą zasad szablonu do sterowania wyświetlaniem informacje zawarte w **właściwości** okna różni się od wykonania <xref:Microsoft.VisualStudio.Shell.Interop.IVsPerPropertyBrowsing>. <xref:Microsoft.VisualStudio.Shell.Interop.IVsPerPropertyBrowsing> szablon zasad można zastosować, aby ograniczyć właściwości obiektów na poziomie rozwiązania lub projektu, obsługuje właściwości obiektów na poziomie składnika. Innymi słowy  
  
- Implementowanie metod na <xref:Microsoft.VisualStudio.Shell.Interop.IVsPerPropertyBrowsing> Aby ustalić, co jest wyświetlane w **właściwości** okna dla określonych obiektów  
  
- Użyj szablonu zasad na poziomie rozwiązania i projektu Aby ustalić, co jest wyświetlane w **właściwości** okno wcześniej określone obiekty  
  
  Przy użyciu szablonu zasad selektywne ograniczenie właściwości określone w **właściwości** wybrano okna, jeśli element projektu o określonym typie **Eksploratora rozwiązań** może być korzystne, aby wszystkie elementy członkowskie pracujesz nad projektem zespołu programistycznego. Na przykład za pomocą szablonu zasad, można skonfigurować wszystkie parametry połączenia informacje w bazie danych dla deweloperów i wprowadzić parametry połączenia tylko do odczytu. W ten sposób można określić prosty sposób zapewnić, że każdy Deweloper używa poprawną ścieżkę dostępu do danych.  
  
## <a name="see-also"></a>Zobacz też  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsPerPropertyBrowsing>   
 [Rozszerzanie właściwości](../../extensibility/internals/extending-properties.md)