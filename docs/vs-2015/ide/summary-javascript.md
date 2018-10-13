---
title: '&lt;Podsumowanie&gt; (JavaScript) | Dokumentacja firmy Microsoft'
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
- summary JavaScript XML tag
- <summary> JavaScript XML tag
ms.assetid: 6540582d-bdb3-42ec-ad2f-c176783e6f9c
caps.latest.revision: 15
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 8ee08ed1e2a5feb1f5a87f7d6337a4b5f1e47a22
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49252411"
---
# <a name="ltsummarygt-javascript"></a>&lt;Podsumowanie&gt; (JavaScript)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Określa opis funkcji lub metody.  
  
## <a name="syntax"></a>Składnia  
  
```  
<summary locid="descriptionID">description  
</summary>  
```  
  
#### <a name="parameters"></a>Parametry  
 `locid`  
 Opcjonalna. Identyfikator informacji o lokalizacji na temat funkcji lub metody. Identyfikator jest albo identyfikatorem elementu członkowskiego albo odpowiada wartości atrybutu `name` w wiązce wiadomości zdefiniowanej przez metadane OpenAjax. Identyfikator typu zależy od formatu określonego w [ \<lokalizacja >](../ide/loc-javascript.md) elementu.  
  
 `description`  
 Opcjonalna. Opis funkcji lub metody.  
  
## <a name="remarks"></a>Uwagi  
 Elementy adnotować funkcje, które obejmują [ \<podsumowania >](../ide/summary-javascript.md), [ \<param >](../ide/param-javascript.md), i [ \<zwraca >](../ide/returns-javascript.md), muszą być umieszczone w ciele funkcji przed wszystkimi instrukcjami.  
  
## <a name="example"></a>Przykład  
 Poniższy kod przedstawia sposób użycia `<summary>` elementu.  
  
```javascript  
function areaFunction(radiusParam)  
{  
    /// <summary>Determines the area of a circle when supplied a radius parameter.</summary>  
    /// <param name="radiusParam" type="Number">The radius of the circle.</param>  
    /// <returns type="Number">The area.</returns>  
    var areaVal;  
    areaVal = Math.PI * radiusParam * radiusParam;  
    return areaVal;  
}  
  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Komentarze dokumentacji XML](../ide/xml-documentation-comments-javascript.md)



