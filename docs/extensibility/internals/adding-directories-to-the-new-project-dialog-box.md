---
title: "Dodawanie katalogów do okna dialogowego Nowy projekt | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: New Project dialog box, extending
ms.assetid: 53b328f5-20bb-49a3-bf9e-1818f4fbdf50
caps.latest.revision: "13"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: f24fd3c3a0ffb537c63346ef867a2a43481acfa9
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="adding-directories-to-the-new-project-dialog-box"></a>Dodawanie katalogów do okna dialogowego Nowy projekt
Podczas tworzenia nowych typów projektów, możesz również zarejestrować nowy katalog w **nowy projekt** się okno dialogowe zawierające je do użycia jako szablon. W poniższym przykładzie wyjaśniono, jak zarejestrować nowego katalogu, znanej także jako węzeł. W tym przykładzie szablony udostępniane przez pakiet VSPackage CLSID_Package są rejestrowane. W rezultacie, z lewej strony **nowy projekt** okno dialogowe oferuje dodanego węzła o nazwie ustaleniami Folder_Label_ResID zasobów. Ten zasób jest ładowany z pakiet VSPackage satelitarnej biblioteki DLL.  
  
 **Folderu** wartość reprezentuje identyfikator GUID folderu, w którym jest wyświetlany w węźle Folder_Label_ResID. W tym przykładzie reprezentuje identyfikator GUID **inne projekty** folderu w **typów projektów** okienku **nowy projekt** okno dialogowe. Jeśli **inne projekty** wartość jest nieobecny, etykiecie znajduje się na najwyższym poziomie.  
  
 Wartość TemplatesDir Określa pełną ścieżkę katalogu, który zawiera szablony projektów. Te pliki mogą być pliki .vsz lub pliki szablonów typowe w klonowania.  
  
 Jeśli określisz TemplatesLocalizedSubDir, musi ona identyfikator zasobu ciągu nazwy podkatalogu TemplatesDir, który zawiera zlokalizowane szablony. Ponieważ [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] ładuje zasobu ciągu z satelitarnej biblioteki DLL Jeśli istnieje, każdy satelitarnej biblioteki DLL może zawierać podkatalogu inną nazwę. Wartość SortPriority określa priorytet sortowania.  
  
```  
NoRemove NewProjectTemplates  
{  
    NoRemove TemplateDirs  
  {  
    ForceRemove %CLSID_Package%  
    {  
      ForceRemove /1 = s '#%Folder_Label_ResID%'  
      {  
        val Folder = s '{DCF2A94A-45B0-11D1-ADBF-00C04FB6BE4C}'  
        val TemplatesDir = s '%Template_Path%'  
        val TemplatesLocalizedSubDir = s '#100'  
        val SortPriority = d 1000  
      }  
    }  
  }  
}  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Rejestrowanie szablony projektów i elementów](../../extensibility/internals/registering-project-and-item-templates.md)   
 [Dodawanie elementów do Dodaj nowy element okien dialogowych](../../extensibility/internals/adding-items-to-the-add-new-item-dialog-boxes.md)   
 [Dodawanie katalogów do dodania okno dialogowe Nowy element](../../extensibility/internals/adding-directories-to-the-add-new-item-dialog-box.md)