---
title: Tworzenie komentarzy JSDoc dla funkcji IntelliSense języka JavaScript | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: a0dadc81-3755-4a47-bcee-c1010819ff2a
caps.latest.revision: 8
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 9d338b2bece99f720670871a1b92c6b2a57c4280
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49908590"
---
# <a name="create-jsdoc-comments-for-javascript-intellisense"></a>Tworzenie komentarzy JSDoc na potrzeby funkcji IntelliSense języka JavaScript
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Funkcja IntelliSense w programie Visual Studio Wyświetla informacje, które można dodać do skryptu, używając standardowych komentarzy JSDoc. Komentarze JSDoc służy do dostarczania informacji dotyczących elementów kodu, takich jak functions, pól i zmiennych.  

## <a name="jsdoc-comment-tags"></a>Tagi komentarza JSDoc  
 Następujących standardowych tagów komentarzy JSDoc są używane przez funkcję IntelliSense, aby wyświetlić informacje o swoim kodzie.  


|  JSDoc tag   |                       Składnia                        |                                                     Uwagi                                                      |
|--------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| @deprecated  |              @deprecated *Opis elementu*              |                                   Określa zaniechanej funkcji lub metody.                                   |
| @description |             @description *Opis elementu*              |                              Określa opis funkcji lub metody.                               |
|    @param    | @param {*typu*} *parameterName*<em>opis</em> | Określa informacje dla parametru w funkcji lub metody.<br /><br /> Obsługuje również TypeScript @paramTag. |
|  @property   |          @property {*typu*} *propertyName*          |   Określa informacje, w tym opis, pola lub elementu członkowskiego, który jest zdefiniowany w obiekcie.    |
|   @returns   |                  @returns {*typu*}                  |           Określa wartość zwracaną.<br /><br /> TypeScript, można użyć @returnType zamiast @returns.           |
|   @summary   |               @summary *Opis elementu*                |                   Określa opis funkcji lub metody (taka sama jak @description).                   |
|    @type     |                   @type {*typu*}                    |                                Określa typ stałą lub zmienną.                                |
|   @typedef   |         @typedef {*typu*} *customTypeName*          |                                            Określa typ niestandardowy.                                            |

### <a name="examples"></a>Przykłady  
 Poniższy przykład pokazuje użycie @description, @param, i @return JSDoc tagów dla funkcji o nazwie `getArea`.  

```javascript  
/** @description Determines the area of a circle that has the specified radius parameter.  
 * @param {number} radius The radius of the circle.  
 * @return {number}  
 */  
function getArea(radius) {  
    var areaVal;  
    areaVal = Math.PI * radius * radius;  
    return areaVal;  
}  
```  

 W poprzednim przykładzie, funkcja IntelliSense wyświetla opis parametru i informacje zwrotne po wpisaniu nawiasu otwierającego dla `getArea`.  

 ![Informacje o technologii IntelliSense dla funkcji](../ide/media/js-intellisense-jsdoc-comments.png "JS_IntelliSense_JSDoc_Comments")  

 Poniższy przykład pokazuje, jak używać @typedef oznaczyć za pomocą @property tagu.  

```javascript  
/**  
  * @typedef {object} Weather  
  * @property {string} current The current weather.  
  */  
function getForecast(Weather) {  
}  

var w = new Weather();  
```  

 Poniższy przykład pokazuje użycie @type JSDoc tagów. Jak pokazano w tym przykładzie, pojedyncza gwiazdka (*), które należy wykonać parę początkowej gwiazdki (\*\*) nie są wymagane.  

```javascript  
/**  
    @type {string}  
*/  
const RED = 'FF0000';  

```  

 Poniższy przykład pokazuje, jak używać @deprecated JSDoc tag.  

```javascript  
/**  
 * @deprecated since version 2.0  
 */  
function old() {  
}  
```



