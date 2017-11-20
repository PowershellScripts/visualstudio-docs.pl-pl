---
title: 'Porady: czyszczenie kompilacji | Dokumentacja firmy Microsoft'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- Exec task [MSBuild]
- MSBuild, cleaning a build
- directories [.NET Framework], for output items
- output, removing items
ms.assetid: 999ba473-b0c4-45c7-930a-63ea7a510509
caps.latest.revision: "13"
author: kempb
ms.author: kempb
manager: ghogen
ms.openlocfilehash: 2b935e0d09bb80347ee17c796f83846cef02a39f
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-clean-a-build"></a>Porady: czyszczenie kompilacji
Podczas oczyszczania kompilacji wszystkich plików pośrednich i wynikowych są usuwane, pozostawiając tylko pliki projektów i składnika. Z plików projektu i składników nowe wystąpienia klasy obiektów i pliki wyjściowe mogą następnie zostać skompilowane. Biblioteka typowych zadań, które jest udostępniane z [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] obejmuje [Exec](../msbuild/exec-task.md) zadanie, które służy do uruchamiania polecenia systemowe. Aby uzyskać więcej informacji w bibliotece zadań, zobacz [odwołanie do zadania](../msbuild/msbuild-task-reference.md).  
  
## <a name="creating-a-directory-for-output-items"></a>Tworzenie katalogu do elementów wyjściowych  
 Domyślnie w tym samym katalogu co pliki projektu i źródła znajduje się plik .exe, który jest tworzony podczas kompilowania projektu. Zwykle jednak elementów wyjściowych są tworzone w oddzielnym katalogu.  
  
#### <a name="to-create-a-directory-for-output-items"></a>Aby utworzyć katalog do elementów wyjściowych  
  
1.  Użyj `Property` element, aby określić lokalizację i nazwę katalogu. Na przykład utworzyć katalog o nazwie `BuiltApp` w katalogu, który zawiera pliki projektu i źródła:  
  
     `<builtdir>BuiltApp</builtdir>`  
  
2.  Użyj [makedir —](../msbuild/makedir-task.md) zadań można utworzyć katalogu, jeśli katalog nie istnieje. Na przykład:  
  
     `<MakeDir Directories = "$(builtdir)"`  
  
     `Condition = "!Exists('$(builtdir)')" />`  
  
## <a name="removing-the-output-items"></a>Usuwanie elementów danych wyjściowych  
 Przed utworzeniem nowych wystąpień plików pośrednich i wynikowych, warto wyczyścić wszystkie poprzednie wystąpienie plików pośrednich i wynikowych. Użyj [removedir —](../msbuild/removedir-task.md) zadanie służy do usuwania z katalogu i wszystkich plików i katalogów, które zawiera z dysku.  
  
#### <a name="to-remove-a-directory-and-all-files-contained-in-the-directory"></a>Aby usunąć wszystkie pliki znajdujące się w katalogu i katalogu  
  
-   Użyj `RemoveDir` zadań w celu usunięcia katalogu. Na przykład:  
  
     `<RemoveDir Directories="$(builtdir)" />`  
  
## <a name="example"></a>Przykład  
 Poniższy kod przykładowy projekt zawiera nowy element docelowy `Clean`, która używa `RemoveDir` zadanie służy do usuwania z katalogu i wszystkich plików i katalogów, które zawiera. Również w tym przykładzie `Compile` docelowej tworzy oddzielny katalog dla elementów danych wyjściowych, które nie są usuwane podczas kompilacji jest czyszczona.  
  
 `Compile`jest zdefiniowany jako domyślnego obiektu docelowego i w związku z tym jest używana automatycznie, chyba że zostanie określony inny element docelowy lub miejsc docelowych. Należy użyć przełącznika wiersza polecenia **/target** Aby określić inny element docelowy. Na przykład:  
  
 `msbuild <file name>.proj /target:Clean`  
  
 **/Target** przełącznik może zostać skrócony do **/t** i można określić więcej niż jeden element docelowy. Na przykład, aby można było użyć obiektu docelowego `Clean` następnie docelowego `Compile`, wpisz:  
  
 `msbuild <file name>.proj /t:Clean;Compile`  
  
```xml  
<Project DefaultTargets = "Compile"  
    xmlns="http://schemas.microsoft.com/developer/msbuild/2003" >  
  
    <PropertyGroup>  
        <!-- Set the application name as a property -->  
        <name>HelloWorldCS</name>  
  
        <!-- Set the output folder as a property -->  
        <builtdir>BuiltApp</builtdir>  
    </PropertyGroup>  
  
    <ItemGroup>  
        <!-- Specify the inputs by type and file name -->  
        <CSFile Include = "consolehwcs1.cs"/>  
    </ItemGroup>  
  
    <Target Name = "Compile">  
        <!-- Check whether an output folder exists and create  
        one if necessary -->  
        <MakeDir Directories = "$(builtdir)"   
            Condition = "!Exists('$(builtdir)')" />  
  
        <!-- Run the Visual C# compiler -->  
        <CSC Sources = "@(CSFile)"   
            OutputAssembly = "$(BuiltDir)\$(appname).exe">  
            <Output TaskParameter = "OutputAssembly"  
                ItemName = "EXEFile" />  
        </CSC>  
  
        <!-- Log the file name of the output file -->  
        <Message Text="The output file is @(EXEFile)"/>  
    </Target>  
  
    <Target Name = "Clean">  
        <RemoveDir Directories="$(builtdir)" />  
    </Target>  
</Project>  
```  
  
## <a name="see-also"></a>Zobacz też  
 [Exec — zadanie](../msbuild/exec-task.md)   
 [Makedir — zadanie](../msbuild/makedir-task.md)   
 [Removedir — zadanie](../msbuild/removedir-task.md)   
 [CSC — zadanie](../msbuild/csc-task.md)   
 [Obiekty docelowe](../msbuild/msbuild-targets.md)