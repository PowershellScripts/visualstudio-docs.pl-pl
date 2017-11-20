---
title: "Porady: Określanie zdarzeń kompilacji (Visual Basic) | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- pre-build events
- events [Visual Studio], builds
- post-build events
- build events [Visual Studio]
- builds [Visual Studio], events
ms.assetid: 40dc83bf-a7c5-4a14-816a-fa0980b6e4c3
caps.latest.revision: "26"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 78dc3c36a7513a04afd8f8e136996c3f896291e2
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-specify-build-events-visual-basic"></a>Porady: określanie zdarzeń kompilacji (Visual Basic)
Zdarzenia kompilacji w języku Visual Basic mogą służyć do uruchamiania skryptów, makr lub innych działań jako część procesu kompilacji. Zdarzenia prekompilacyjnego występują przed kompilacji; zdarzenia postkompilacyjnego występują po kompilacji.  
  
 Tworzenie zdarzenia są określone w **zdarzeń kompilacji** okno dialogowe, dostępne z **skompilować** strony **Projektant projektu**.  
  
> [!NOTE]
>  Visual Basic Express nie obsługuje zapisu zdarzeń kompilacji. Jest to obsługiwane tylko w pełną wersję programu Visual Studio.  
  
## <a name="how-to-specify-pre-build-and-post-build-events"></a>Jak określać zdarzenia Prekompilacyjnego i mające miejsce po kompilacji  
  
#### <a name="to-specify-a-build-event"></a>Aby określić zdarzenia kompilacji  
  
1.  Z projektem wybranym **Eksploratora rozwiązań**na **projektu** menu, kliknij przycisk **właściwości**.  
  
2.  Kliknij przycisk **skompilować** kartę.  
  
3.  Kliknij przycisk **zdarzeń kompilacji** przycisk, aby otworzyć **zdarzeń kompilacji** okno dialogowe.  
  
4.  Wprowadź argumenty wiersza polecenia dla akcji kompilacji przed lub po kompilacji, a następnie kliknij przycisk **OK**.  
  
    > [!NOTE]
    >  Dodaj `call` instrukcję przed wszystkie postkompilacyjnego polecenia, które uruchamiają pliki bat. Na przykład `call C:\MyFile.bat` lub `call C:\MyFile.bat call C:\MyFile2.bat`.  
  
    > [!NOTE]
    >  Jeśli Twoje zdarzenia prekompilacyjnego lub mające miejsce po kompilacji nie zakończy się pomyślnie, można zakończyć kompilacji przez akcję zdarzeń zamknąć przy użyciu kodu innego niż zero (0), wskazujący pomyślne akcji.  
  
## <a name="example-how-to-change-manifest-information-using-a-post-build-event"></a>Przykład: Jak zmienić manifestu informacji za pomocą zdarzenie mające miejsce po kompilacji  
 Poniższa procedura pokazuje, jak ustawić minimalnej wersji systemu operacyjnego w manifeście aplikacji za pomocą polecenia .exe wywoływana z zdarzenia postkompilacyjnego (. exe.manifest pliku w katalogu projektu). Minimalna wersja systemu operacyjnego jest liczbą czteroczęściową, takich jak 4.10.0.0. Aby to zrobić, zmieni polecenie `<dependentOS>` sekcji manifestu:  
  
```  
<dependentOS>  
   <osVersionInfo>  
      <os majorVersion="4" minorVersion="10" buildNumber="0" servicePackMajor="0" />  
   </osVersionInfo>  
</dependentOS>  
```  
  
#### <a name="to-create-an-exe-command-to-change-the-application-manifest"></a>Aby utworzyć polecenie .exe, aby zmienić manifest aplikacji  
  
1.  Utwórz aplikację konsoli dla polecenia. Z **pliku** menu, kliknij przycisk **nowy**, a następnie kliknij przycisk **projektu**.  
  
2.  W **nowy projekt** okna dialogowego, **Visual Basic** węzła, wybierz opcję **Windows** , a następnie **aplikacji konsoli** szablonu. Nazwij projekt `ChangeOSVersionVB`.  
  
3.  W Module1.vb, Dodaj następujący wiersz do drugiego `Imports` instrukcje w górnej części pliku:  
  
    ```  
    Imports System.Xml  
    ```  
  
4.  Dodaj następujący kod w `Sub Main`:  
  
    ```  
    Sub Main()  
       Dim applicationManifestPath As String  
       applicationManifestPath = My.Application.CommandLineArgs(0)  
       Console.WriteLine("Application Manifest Path: " & applicationManifestPath.ToString)  
  
       'Get version name  
       Dim osVersion As Version  
       If My.Application.CommandLineArgs.Count >= 2 Then  
          osVersion = New Version(My.Application.CommandLineArgs(1).ToString)  
       Else  
          Throw New ArgumentException("OS Version not specified.")  
       End If  
       Console.WriteLine("Desired OS Version: " & osVersion.ToString())  
  
       Dim document As XmlDocument  
       Dim namespaceManager As XmlNamespaceManager  
       namespaceManager = New XmlNamespaceManager(New NameTable())  
       With namespaceManager  
          .AddNamespace("asmv1", "urn:schemas-microsoft-com:asm.v1")  
          .AddNamespace("asmv2", "urn:schemas-microsoft-com:asm.v2")  
       End With  
  
       document = New XmlDocument()  
       document.Load(applicationManifestPath)  
  
       Dim baseXPath As String  
       baseXPath = "/asmv1:assembly/asmv2:dependency/asmv2:dependentOS/asmv2:osVersionInfo/asmv2:os"  
  
       'Change minimum required OS Version.  
       Dim node As XmlNode  
       node = document.SelectSingleNode(baseXPath, namespaceManager)  
       node.Attributes("majorVersion").Value = osVersion.Major.ToString()  
       node.Attributes("minorVersion").Value = osVersion.Minor.ToString()  
       node.Attributes("buildNumber").Value = osVersion.Build.ToString()  
       node.Attributes("servicePackMajor").Value = osVersion.Revision.ToString()  
  
       document.Save(applicationManifestPath)  
    End Sub  
    ```  
  
     Polecenie przyjmuje dwa argumenty. Pierwszy argument jest ścieżka do manifestu aplikacji (oznacza to, że folder w którym proces kompilacji tworzy manifestu, zwykle Projectname.publish). Drugi argument jest nowa wersja systemu operacyjnego.  
  
5.  Na **kompilacji** menu, kliknij przycisk **Kompiluj rozwiązanie**.  
  
6.  Skopiuj plik .exe do katalogu, takie jak `C:\TEMP\ChangeOSVersionVB.exe`.  
  
 Następnie wywołaj tego polecenia zdarzenia po kompilacji, aby zmienić manifest aplikacji.  
  
#### <a name="to-invoke-a-post-build-event-to-change-the-application-manifest"></a>Aby wywołać zdarzenie mające miejsce po kompilacji, aby zmienić manifest aplikacji  
  
1.  Tworzenie aplikacji systemu Windows dla projektu do opublikowania. Z **pliku** menu, kliknij przycisk **nowy**, a następnie kliknij przycisk **projektu**.  
  
2.  W **nowy projekt** okna dialogowego, **Visual Basic** węzła, wybierz opcję **klasycznego pulpitu systemu Windows** , a następnie **aplikacji formularzy systemu Windows** szablon. Nazwij projekt `VBWinApp`.  
  
3.  W projekcie wybrana w **Eksploratora rozwiązań**na **projektu** menu, kliknij przycisk **właściwości**.  
  
4.  W Projektancie projektu, przejdź do **publikowania** strony i ustaw **publikowania lokalizacji** do `C:\TEMP\`.  
  
5.  Publikowanie projektu, klikając **opublikować teraz**.  
  
     Plik manifestu zostanie utworzony i umieścić w `C:\TEMP\VBWinApp_1_0_0_0\VBWinApp.exe.manifest`. Aby wyświetlić plik manifestu, kliknij prawym przyciskiem myszy plik, a następnie kliknij przycisk **Otwórz za pomocą**, następnie kliknij przycisk **wybierz program z listy**, a następnie kliknij przycisk **Notatnik**.  
  
     Wyszukaj w pliku `<osVersionInfo>` elementu. Na przykład może być wersji:  
  
    ```  
    <os majorVersion="4" minorVersion="10" buildNumber="0" servicePackMajor="0" />  
    ```  
  
6.  W Projektancie projektu, przejdź do **skompilować** i kliknij polecenie **zdarzeń kompilacji** przycisk, aby otworzyć **zdarzeń kompilacji** okno dialogowe.  
  
7.  W **wiersz polecenia zdarzenia po kompilacji** wprowadź następujące polecenie:  
  
     `C:\TEMP\ChangeOSVersionVB.exe "$(TargetPath).manifest" 5.1.2600.0`  
  
     Podczas tworzenia projektu, to polecenie spowoduje zmianę minimalnej wersji systemu operacyjnego w manifeście aplikacji na 5.1.2600.0.  
  
     `$(TargetPath)` Makro wyraża pełnej ścieżki pliku wykonywalnego tworzona. W związku z tym $(TargetPath) manifest określa manifest aplikacji utworzony w katalogu bin. Publikowanie skopiuje tego manifestu ustawionych wcześniej lokalizację publikowania.  
  
8.  Ponownie opublikować projekt. Przejdź do **publikowania** i kliknij przycisk **opublikować teraz**.  
  
     Ponownie wyświetlić manifestu. Aby wyświetlić manifestu, przejdź do katalogu publikowania, kliknij prawym przyciskiem myszy plik, a następnie kliknij przycisk **Otwórz za pomocą** , a następnie **wybierz program z listy**, a następnie kliknij przycisk **Notatnik**.  
  
     Teraz należy odczytać wersji:  
  
    ```  
    <os majorVersion="5" minorVersion="1" buildNumber="2600" servicePackMajor="0" />  
    ```  
  
## <a name="see-also"></a>Zobacz też  
 [Zarządzanie właściwościami kompilacji](http://msdn.microsoft.com/en-us/94308881-f10f-4caf-a729-f1028e596a2c)   
 [Strona kompilowania, Projektant projektu (Visual Basic)](../ide/reference/compile-page-project-designer-visual-basic.md)   
 [Strona publikowania, Projektant projektu](../ide/reference/publish-page-project-designer.md)   
 [Okno dialogowe wiersza polecenia zdarzenia/po kompilacji — zdarzenia prekompilacyjnego](../ide/reference/pre-build-event-post-build-event-command-line-dialog-box.md)   
 [Porady: Określanie zdarzeń kompilacji (C#)](../ide/how-to-specify-build-events-csharp.md)