---
title: Nie można zmodyfikować projektanta podczas debugowania | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 487dafe4-d57c-4be1-9e3a-bb0a8699b2fa
caps.latest.revision: 7
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 625e93fd32fb3349d5b425f5567c3878479c8fbb
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49172175"
---
# <a name="the-designer-cannot-be-modified-while-debugging"></a>Nie można zmodyfikować projektanta podczas debugowania
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Ten komunikat pojawia się, gdy podejmowana jest próba modyfikować elementy w Projektancie obiektów relacyjnych, gdy aplikacja jest uruchomiona w trybie debugowania. Gdy aplikacja jest uruchomiona w trybie debugowania, O/R Designer jest tylko do odczytu.  
  
### <a name="to-correct-this-error"></a>Aby poprawić ten błąd  
  
-   Kliknij przycisk **Zatrzymaj debugowanie** na **debugowania** menu.  
  
     Aplikacja zatrzymuje debugowanie i można modyfikować elementów w Projektancie obiektów relacyjnych.  
  
## <a name="see-also"></a>Zobacz też  
 [LINQ to SQL Tools w programie Visual Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md)   
 [Wskazówki: Tworzenie składnika LINQ to SQL klas (Projektant O-R)](http://msdn.microsoft.com/library/35aad4a4-2e8a-46e2-ae09-5fbfd333c233)   
 [LINQ to SQL](http://msdn.microsoft.com/library/73d13345-eece-471a-af40-4cc7a2f11655)

