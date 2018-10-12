---
title: Rozwiązywanie problemów z fragmentów kodu | Dokumentacja firmy Microsoft
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
- IntelliSense Code Snippets, troubleshooting
- troubleshooting IntelliSense Code Snippets
- troubleshooting Visual Basic, IntelliSense Code Snippets
ms.assetid: 7b6dd40e-2f78-4b50-8e68-41fac1bcb81e
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 4fff2767c962cf6899840e54bff798bae1f9e202
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49304814"
---
# <a name="troubleshooting-snippets"></a>Rozwiązywanie problemów z wstawkami kodu programu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Problemy z fragmenty kodu IntelliSense są zazwyczaj spowodowane dwa problemy: plik fragmentu w uszkodzona lub zły zawartość pliku fragmentu kodu.  
  
## <a name="common-problems"></a>Typowe problemy  
  
### <a name="the-snippet-cannot-be-dragged-from-file-explorer-to-a-visual-studio-source-file"></a>Fragment kodu nie można przeciągnąć z Eksploratora plików do pliku źródłowego programu Visual Studio  
  
-   Kod XML w pliku fragmentu kodu może być uszkodzony. **Edytora XML** w [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] mogą zlokalizować problemów w strukturze XML.  
  
-   Plik fragmentu kodu nie może być zgodny ze schematem fragmentu kodu. **Edytora XML** w [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] mogą zlokalizować problemów w strukturze XML.  
  
### <a name="the-code-has-compiler-errors-that-are-not-highlighted"></a>Kod ma błędy kompilatora, które nie są wyróżnione  
  
-   Być może brakuje odwołania projektu. Sprawdź dokumentację dotyczącą fragmentu kodu. Odwołanie nie zostanie znaleziony na komputerze, należy go zainstalować. Wstawianie fragmentu należy dodać do projektu wszystkie odwołania potrzebne. Jeżeli ten fragment kodu brakuje zawiera informacje, które mogą zostać zgłoszone do autora fragmentu kodu jako błąd.  
  
-   Zmienna może być niezdefiniowana. Powinien być wyróżniony niezdefiniowane zmienne we fragmencie. Jeśli nie, które mogą zostać zgłoszone do autora fragmentu kodu jako błąd.  
  
## <a name="see-also"></a>Zobacz też  
 [Fragmenty kodu](../ide/code-snippets.md)



