---
title: 'Porady: aplikacje Office docelowej przy użyciu podstawowych zestawów międzyoperacyjnych'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- assemblies [Office development in Visual Studio], PIA references
- primary interop assemblies [Office development in Visual Studio], adding references to
- Office primary interop assemblies in Visual Studio, adding references to
- Office applications [Office development in Visual Studio], automating
- application development [Office development in Visual Studio], automating
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 576d26f039005dac3d494652f1e5127c39092a00
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49863753"
---
# <a name="how-to-target-office-applications-through-primary-interop-assemblies"></a>Porady: aplikacje Office docelowej przy użyciu podstawowych zestawów międzyoperacyjnych
  Podczas tworzenia nowego projektu pakietu Office, Visual Studio automatycznie dodaje odwołania do programu Microsoft Office podstawowe zestawy międzyoperacyjne (PIA), które są wymagane do kompilowania projektu. Należy dodać odwołania do innych zestawów PIA w następujących scenariuszach:  
  
- Chcesz korzystać z funkcji innych aplikacji pakietu Microsoft Office w projekcie. Na przykład można używać funkcji programu Microsoft Office Excel w projekcie dla programu Microsoft Office Word.  
  
- Chcesz zautomatyzować aplikacji Microsoft Office, które nie mają dedykowanych projektów w programie Visual Studio, takich jak Microsoft Office Access.  
  
  [!INCLUDE[appliesto_all](../vsto/includes/appliesto-all-md.md)]  
  
  [!INCLUDE[note_settings_general](../sharepoint/includes/note-settings-general-md.md)]  
  
## <a name="to-add-a-reference-to-a-primary-interop-assembly"></a>Aby dodać odwołanie do podstawowego zestawu międzyoperacyjnego  
  
1.  Otwórz projekt pakietu Office i wybierz nazwę projektu w **Eksploratora rozwiązań**.  
  
2.  Na **projektu** menu, kliknij przycisk **Dodaj odwołanie**.  
  
3.  Na **Framework** , a następnie wybierz PIA w **nazwa składnika** listy. Aby uzyskać więcej informacji na temat dostępnych podstawowych zestawów międzyoperacyjnych programu Microsoft Office, zobacz [podstawowe zestawy międzyoperacyjne pakietu Office](../vsto/office-primary-interop-assemblies.md).  
  
     Jeśli projekt jest ukierunkowany [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] lub nowszym, **Osadź typy współdziałania** dla odwołania do zestawu jest właściwością **True** domyślnie. Za pomocą tego ustawienia, rozwiązanie nie wymaga PIA na komputerach użytkowników końcowych. Aby uzyskać więcej informacji, zobacz [projektowania i tworzenia rozwiązań dla pakietu Office](../vsto/designing-and-creating-office-solutions.md).  
  
    > [!NOTE]  
    >  W projektach pakietu Office, zawsze dodać odwołania do zestawów PIA pakietu Office za pomocą **.NET** karcie **Dodaj odwołanie** okna dialogowego, a nie od **COM** kartę. Aby uzyskać więcej informacji, zobacz [podstawowe zestawy międzyoperacyjne pakietu Office](../vsto/office-primary-interop-assemblies.md).  
  
4.  Kliknij przycisk **OK**.  
  
     Nazwa zestawu, który pojawia się w **odwołania** folderu **Eksploratora rozwiązań**.  
  
## <a name="see-also"></a>Zobacz także  
 [Podstawowe zestawy międzyoperacyjne pakietu Office](../vsto/office-primary-interop-assemblies.md)   
 [Pisanie kodu w rozwiązaniach pakietu Office](../vsto/writing-code-in-office-solutions.md)   
 [Opracowywania rozwiązań pakietu Office](../vsto/developing-office-solutions.md)   
 [Porady: podstawowe zestawy międzyoperacyjne pakietu Office instalacji](../vsto/how-to-install-office-primary-interop-assemblies.md)  
  
  