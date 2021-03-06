---
title: Parametry kontekstu | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- wizards, context parameters
- context parameters
ms.assetid: 1a062dcb-8a8f-40dd-bea9-3d10f9448966
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: d595bcc99cbacabd55c8e85775e1d691e917a41c
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49875843"
---
# <a name="context-parameters"></a>Parametry kontekstu
W [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] zintegrowanym środowisku programistycznym (IDE), możesz dodać kreatorów, aby **nowy projekt**, **Dodaj nowy element**, lub **Dodaj projekt Sub** okien dialogowych. Dodano kreatorów są dostępne na **pliku** menu lub klikając prawym przyciskiem myszy projekt w **Eksploratora rozwiązań**. IDE przekazuje parametry kontekstu wykonania kreatora. Parametry kontekstu Definiowanie stanu projektu, gdy IDE wywołuje kreatora.  
  
 IDE rozpoczyna kreatory, ustawiając <xref:Microsoft.VisualStudio.Shell.Interop.VSADDITEMOPERATION> flagi w wywołaniu IDE <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject3.AddItem%2A> metody dla projektu. Po ustawieniu projektu mogą powodować `IVsExtensibility::RunWizardFile` metodę można wykonać przy użyciu nazwy zarejestrowanych kreatora lub identyfikator GUID i innych parametrów kontekstu, które IDE przekazuje do niego.  
  
## <a name="context-parameters-for-new-project"></a>Parametry kontekstu dla nowego projektu  
  
| Parametr | Opis |
|-------------------------| - |
| `WizardType` | Zarejestrowany typ kreatora (<xref:EnvDTE.Constants.vsWizardNewProject>) lub identyfikator GUID, który wskazuje na typ kreatora. W [!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)] {0F90E1D0-4999-11D1-B6D1-00A0C90F2744} jest implementacja, identyfikator GUID dla kreatora. |
| `ProjectName` | Ciąg, który jest unikatowy [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] nazwy projektu. |
| `LocalDirectory` | Lokalizacja lokalne pliki projektu pracy. |
| `InstallationDirectory` | Ścieżka katalogu [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] jest instalacja. |
| `FExclusive` | Flaga wartości logicznej, która wskazuje, czy projekt powinien zostać zamknięty otwarte rozwiązania. |
| `SolutionName` | Nazwa pliku rozwiązania bez katalogu części lub *.sln* rozszerzenia. *.Suo* nazwa pliku jest tworzona przy użyciu `SolutionName`. Jeśli ten argument nie jest ciągiem pustym, kreator używa <xref:EnvDTE._Solution.Create%2A> przed dodaniem projektu z <xref:EnvDTE._Solution.AddFromTemplate%2A>. Jeśli ta nazwa jest ciągiem pustym, użyj <xref:EnvDTE._Solution.AddFromTemplate%2A> bez wywoływania <xref:EnvDTE._Solution.Create%2A>. |
| `Silent` | Wartość logiczna wskazująca, czy kreator powinien pracować w trybie dyskretnym tak, jakby **Zakończ** kliknięty (`TRUE`). |
  
## <a name="context-parameters-for-add-new-item"></a>Parametry kontekstu Dodaj nowy element  
  
| Parametr | Opis |
|-------------------------| - |
| `WizardType` | Zarejestrowany typ kreatora (<xref:EnvDTE.Constants.vsWizardAddItem>) lub identyfikator GUID, który wskazuje na typ kreatora. W [!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)] {0F90E1D1-4999-11D1-B6D1-00A0C90F2744} jest implementacja, identyfikator GUID dla kreatora. |
| `ProjectName` | Ciąg, który jest unikatowy [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] nazwy projektu. |
| `ProjectItems` | Lokalizacja lokalna, który zawiera pliki projektu pracy. |
| `ItemName` | Nazwa elementu, który ma zostać dodany. Ta nazwa jest domyślna nazwa pliku lub nazwę pliku, wpisywany przez użytkownika z **Dodaj elementy** okno dialogowe. Nazwa opiera się na flagi, które są ustawiane w *.vsdir* pliku. Nazwa może zawierać wartości null. |
| `InstallationDirectory` | Ścieżka katalogu [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] jest instalacja. |
| `Silent` | Wartość logiczna wskazująca, czy kreator powinien pracować w trybie dyskretnym tak, jakby **Zakończ** kliknięty (`TRUE`). |
  
## <a name="context-parameters-for-add-sub-project"></a>Parametry kontekstu Dodawanie projektu podrzędnego  
  
| Parametr | Opis |
|-------------------------| - |
| `WizardType` | Zarejestrowany typ kreatora (<xref:EnvDTE.Constants.vsWizardAddSubProject>) lub identyfikator GUID, który wskazuje na typ kreatora. W [!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)] {0F90E1D2-4999-11D1-B6D1-00A0C90F2744} jest implementacja, identyfikator GUID dla kreatora. |
| `ProjectName` | Ciąg, który jest unikatowy [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] nazwy projektu. |
| `ProjectItems` | Wskaźnik do `ProjectItems` kolekcji, na którym działa Kreator. This, wskaźnik jest przekazywana do kreatora na podstawie pozycji wybranej hierarchii projektu. Użytkownik zwykle wybiera folder, w której ma zostać umieszczony element, a następnie wywołuje projektu **elementu Dodawanie** okno dialogowe. |
| `LocalDirectory` | Lokalizacja lokalne pliki projektu pracy. |
| `ItemName` | Nazwa elementu, który ma zostać dodany. Ta nazwa jest domyślna nazwa pliku lub nazwę pliku, wpisywany przez użytkownika z **Dodaj elementy** okno dialogowe. Nazwa opiera się na flagi, które są ustawiane w *.vsdir* pliku. Nazwa może zawierać wartości null. |
| `InstallationDirectory` | Ścieżka katalogu [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] instalacji. |
| `Silent` | Wartość logiczna wskazująca, czy kreator powinien pracować w trybie dyskretnym tak, jakby **Zakończ** kliknięty (`TRUE`). |
  
## <a name="see-also"></a>Zobacz też  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject2>   
 [Parametry niestandardowe](../../extensibility/internals/custom-parameters.md)   
 [Kreatorzy](../../extensibility/internals/wizards.md)   
 [Plik kreatora (vsz)](../../extensibility/internals/wizard-dot-vsz-file.md)   
 [Parametry kontekstu uruchomiania kreatorów](https://msdn.microsoft.com/Library/051a10f4-9e45-4604-b344-123044f33a24)