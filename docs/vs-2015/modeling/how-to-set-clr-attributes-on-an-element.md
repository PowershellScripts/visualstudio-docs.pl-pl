---
title: 'Porady: ustawienie atrybutów CLR w elemencie | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.dsltools.EditAttributesDialog
helpviewer_keywords:
- Domain-Specific Language, custom attrributes
ms.assetid: b3db3c74-920c-4701-9544-6f75cbe8b7c9
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: b77e0f1f31c0f617e80a27de4e1d0ab1d0b3d2eb
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49264031"
---
# <a name="how-to-set-clr-attributes-on-an-element"></a>Porady: ustawienie atrybutów CLR w elemencie
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Atrybuty niestandardowe są specjalne atrybuty, które mogą być dodawane do elementy domeny, kształty, łączników i diagramy. Możesz dodać dowolny atrybut, który dziedziczy z `System.Attribute` klasy.  
  
### <a name="to-add-a-custom-attribute"></a>Aby dodać atrybut niestandardowy  
  
1.  W **Eksplorator DSL**, wybierz element, do którego chcesz dodać atrybut niestandardowy.  
  
2.  W **właściwości** okna, obok **atrybuty niestandardowe** właściwości, kliknij przycisk Przeglądaj (**...** ) ikona.  
  
     **Edycja atrybutów** zostanie otwarte okno dialogowe.  
  
3.  W **nazwa** kolumny, kliknij przycisk  **\<Dodaj atrybut >** i wpisz nazwę swojej atrybutu. Naciśnij klawisz ENTER.  
  
4.  Wiersz pod nazwą atrybutu zawiera nawiasy. W tym wierszu typu parametru atrybutu (na przykład `string`), a następnie naciśnij klawisz ENTER.  
  
5.  W **właściwości Name** kolumny, wpisz odpowiednią nazwę, na przykład `MyString`.  
  
6.  Kliknij przycisk **OK**.  
  
     **Atrybuty niestandardowe** właściwości wyświetla teraz atrybutu w następującym formacie:  
  
     `[` *AttributeName* `(` *ParameterName* `=` *typu* `)]`  
  
## <a name="see-also"></a>Zobacz też  
 [Słownik narzędzi języka specyficznego dla domeny](http://msdn.microsoft.com/en-us/ca5e84cb-a315-465c-be24-76aa3df276aa)



