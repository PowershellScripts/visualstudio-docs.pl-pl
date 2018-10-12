---
title: Ukrywanie właściwości, które mają właściwości podrzędnej | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-csharp
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- properties [Visual Studio SDK], hiding
- Properties window, hiding properties that have child properties
ms.assetid: 6003607e-fc19-4bf9-a299-9f6adf8e92eb
caps.latest.revision: 13
manager: douge
ms.openlocfilehash: 76ef9c093bb91bc3cc22df7b56c4d5d69dbc41a5
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49196524"
---
# <a name="hiding-properties-that-have-child-properties"></a>Ukrywanie właściwości, które mają właściwości podrzędnej
Czy chcesz ukryć właściwości, które mają właściwości podrzędnej:  
  
-   Jeśli masz zagnieżdżonych projektów, gdzie projekt nadrzędny programowo określa niektóre aspekty projekt podrzędny.  
  
-   Jeśli możesz użyć formantu przy użyciu wyspecjalizowanego projektanta i nie chcesz dają deweloperom pełny dostęp do wszystkich właściwości formantu.  
  
-   Jeśli masz zakresie własności obiektu i chce ograniczyć widoku właściwości.  
  
### <a name="to-hide-properties-that-have-child-properties"></a>Aby ukryć właściwości, które mają właściwości podrzędnej  
  
1.  Ustaw `pfDisplay` parametru w <xref:Microsoft.VisualStudio.Shell.Interop.IVsPerPropertyBrowsing.DisplayChildProperties%2A> do `FALSE`.  
  
2.  Ustaw `pfHide` parametru w <xref:Microsoft.VisualStudio.Shell.Interop.IVsPerPropertyBrowsing.HideProperty%2A> do `TRUE`.  
  
## <a name="see-also"></a>Zobacz też  
 [Siatka wyświetlania właściwości](../extensibility/internals/properties-display-grid.md)