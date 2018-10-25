---
title: 'Porady: ignorowanie błędów w zadaniach | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: msbuild - "vs-ide-sdk"
ms.topic: conceptual
helpviewer_keywords:
- MSBuild, ignoring errors
- ContinueOnError attribute [MSBuild]
ms.assetid: e2f1ca4f-787b-44bd-bc64-81a036025e96
author: mikejo5000
ms.author: mikejo
manager: douge
ms.openlocfilehash: 3df3a3b40dd67f12bac19f4e69f5293c85bb85f3
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49940037"
---
# <a name="how-to-ignore-errors-in-tasks"></a>Porady: ignorowanie błędów w zadaniach
Czasami chcesz być odporne na błędy w wykonywaniu pewnych zadań kompilacji. Jeśli te krytyczne zadania nie powiedzie się, które mają kompilacji, aby kontynuować, ponieważ nadal może utworzyć wymagane dane wyjściowe. Na przykład, jeśli projekt używa `SendMail` zadanie, aby wysłać wiadomość e-mail po utworzeniu każdego składnika, warto rozważyć je dopuszczalny dla kompilacji przejść do ukończenia, nawet wtedy, gdy serwery poczty są niedostępne i nie można wysłać komunikaty o stanie. Lub, na przykład, jeśli pliki pośrednie zwykle są usuwane podczas kompilacji, można rozważyć jej dopuszczalny dla kompilacji przejść do ukończenia, nawet wtedy, gdy nie można usunąć tych plików.  
  
## <a name="use-the-continueonerror-attribute"></a>Użyj ContinueOnError — atrybut  
 `ContinueOnError` Atrybutu `Task` element kontroluje, czy kompilacja zatrzymuje się lub być kontynuowana po wystąpieniu awarii zadań. Ten atrybut określa również, czy błędy są traktowane jako błędy lub ostrzeżenia, gdy kontynuuje kompilację.  
  
 `ContinueOnError` Atrybut może zawierać jedną z następujących wartości:  
  
- **WarnAndContinue** lub **true**. Jeśli zadanie nie powiedzie się, kolejne zadania w [docelowej](../msbuild/target-element-msbuild.md) elementu i kompilacja będą wykonywane, a wszystkie błędy z zadania są traktowane jako ostrzeżenia.  
  
- **ErrorAndContinue**. Jeśli zadanie nie powiedzie się, kolejne zadania w `Target` elementu i kompilacja będą wykonywane, a wszystkie błędy z zadania są traktowane jako błędy.  
  
- **ErrorAndStop** lub **false** (ustawienie domyślne). Jeśli zadanie nie powiedzie się, kolejnych zadań na `Target` elementu i kompilacja nie są wykonywane i całą `Target` elementu i kompilacja jest uważany za nie powiodło się.  
  
  Wersje programu .NET Framework przed 4.5 obsługiwane tylko `true` i `false` wartości.  
  
  Wartość domyślna `ContinueOnError` jest `ErrorAndStop`. Jeśli ten atrybut zostanie ustawiony `ErrorAndStop`, wprowadzeniu zachowanie jawne dla każdego, kto czyta pliku projektu.  
  
#### <a name="to-ignore-an-error-in-a-task"></a>Ignorowanie błędu w zadaniu  
  
-   Użyj `ContinueOnError` atrybut zadania. Na przykład:  
  
     `<Delete Files="@(Files)" ContinueOnError="WarnAndContinue"/>`  
  
## <a name="example"></a>Przykład  
 Poniższy przykład kodu pokazuje, że `Build` docelowej nadal działa i kompilacja, jest uznawany za sukces, nawet jeśli `Delete` zadań kończy się niepowodzeniem.  
  
```xml  
<Project DefaultTargets="FakeBuild"  
    xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
    <ItemGroup>  
        <Files Include="*.obj"/>  
    </ItemGroup>  
    <Target Name="Clean">  
        <Delete Files="@(Files)" ContinueOnError="WarnAndContinue"/>  
    </Target>  
  
    <Target Name="FakeBuild" DependsOnTargets="Clean">  
        <Message Text="Building after cleaning..."/>  
    </Target>  
</Project>  
```  
  
## <a name="see-also"></a>Zobacz także
[MSBuild](../msbuild/msbuild.md)  
[Odwołanie do zadania](../msbuild/msbuild-task-reference.md)   
[Zadania](../msbuild/msbuild-tasks.md)