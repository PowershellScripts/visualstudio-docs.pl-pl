---
title: 'Porady: Określanie zdarzeń kompilacji (C#)'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
- pre-build events
- events [Visual Studio], builds
- post-build events
- build events [Visual Studio]
- builds [Visual Studio], events
ms.assetid: b4ce1ad9-5215-4b6f-b6a2-798b249aa335
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: aa82c7f12b3932c1e9f5aac7392d6ef2b8e8a773
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49885857"
---
# <a name="how-to-specify-build-events-c"></a>Porady: Określanie zdarzeń kompilacji (C#)

Korzystanie ze zdarzeń kompilacji określić polecenia, które są uruchamiane przed rozpoczęciem kompilacji lub po zakończeniu kompilacji. Zdarzenia kompilacji są wykonywane tylko wtedy, gdy kompilacja pomyślnie osiągnie tych punktów w procesie kompilacji.

Podczas kompilowania projektu zdarzenia sprzed kompilacji są dodawane do pliku o nazwie *PreBuildEvent.bat* i zdarzenia mające miejsce po kompilacji zostaną dodane do pliku o nazwie *PostBuildEvent.bat*. Jeśli chcesz upewnić się, sprawdzanie błędów, należy dodać własne polecenia sprawdzania błędów do kroków kompilacji.

[!INCLUDE[note_settings_general](../data-tools/includes/note_settings_general_md.md)]

## <a name="how-to-specify-pre-build-and-post-build-events"></a>Jak określić zdarzenia sprzed kompilacji i po kompilacji

### <a name="to-specify-a-build-event"></a>Aby określić zdarzenia kompilacji

1.  W **Eksploratora rozwiązań**, wybierz projekt, dla którego chcesz określić zdarzeń kompilacji.

2.  Na **projektu** menu, kliknij przycisk **właściwości**.

3.  Wybierz **zdarzenia kompilacji** kartę.

4.  W **wiersz polecenia zdarzenia sprzed kompilacji** Określ składnia zdarzenia kompilacji.

    > [!NOTE]
    > Jeśli projekt jest aktualny, a nie kompilacja zostaje wyzwolona, nie należy uruchamiać zdarzenia prekompilacyjnego.

5.  W **wiersz polecenia zdarzenia po kompilacji** Określ składnia zdarzenia kompilacji.

    > [!NOTE]
    > Dodaj `call` instrukcji przed poleceniami wszystkich wykonywanych po kompilacji, które są uruchamiane *.bat* plików. Na przykład `call C:\MyFile.bat` lub `call C:\MyFile.bat call C:\MyFile2.bat`.

6.  W **Uruchom zdarzenie po kompilacji** należy określić, na jakich warunkach, aby uruchomić zdarzenie mające miejsce po kompilacji.

    > [!NOTE]
    > Aby dodać długiej składni lub wybrać dowolne makra z kompilacji [zdarzeń/po kompilacji — zdarzenia prekompilacyjnego wiersza polecenia, okno dialogowe](../ide/reference/pre-build-event-post-build-event-command-line-dialog-box.md), kliknij przycisk oznaczony wielokropkiem (**...** ) do wyświetlenia w polu edycji.

     Składnia zdarzenia kompilacji może zawierać dowolne polecenie, które jest prawidłowa, w wierszu polecenia lub w *.bat* pliku. Nazwa pliku wsadowego powinien być poprzedzony `call` aby upewnić się, że wszystkie kolejne polecenia są wykonywane.

    > [!NOTE]
    > Jeśli zdarzenia sprzed kompilacji lub po kompilacji nie zostanie ukończone pomyślnie, możesz zakończyć działanie kompilacji przez akcję zdarzenia zakończyć pracę z kodem niż zero (0), co oznacza pomyślne akcji.

## <a name="example-how-to-change-manifest-information-by-using-a-post-build-event"></a>Przykład: Jak zmienić informacje manifestu za pomocą zdarzenia postkompilacyjnego

Poniższa procedura pokazuje, jak ustawić wersję minimalną wersję systemu operacyjnego w manifeście aplikacji przy użyciu *.exe* polecenia, która jest wywoływana z zdarzenia postkompilacyjnego ( *. exe.manifest* w pliku katalog projektu). Wersja minimalna wersja systemu operacyjnego jest Czteroczęściowy numer, takich jak 4.10.0.0. Aby to zrobić, polecenia zmieni `<dependentOS>` sekcji manifestu:

```xml
<dependentOS>
   <osVersionInfo>
      <os majorVersion="4" minorVersion="10" buildNumber="0" servicePackMajor="0" />
   </osVersionInfo>
</dependentOS>
```

### <a name="to-create-an-exe-command-to-change-the-application-manifest"></a>Aby utworzyć polecenie .exe, aby zmienić manifest aplikacji

1. Utwórz aplikację konsolową dla polecenia. Z **pliku** menu wskaż **New**, a następnie kliknij przycisk **projektu**.

2. W **nowy projekt** okna dialogowego rozwiń **Visual C#**, kliknij przycisk **Windows**, a następnie kliknij przycisk **aplikację Konsolową** szablonu. Nadaj projektowi nazwę `ChangeOSVersionCS`.

3. W *Program.cs*, Dodaj następujący wiersz do drugiego `using` instrukcji w górnej części pliku:

   ```csharp
   using System.Xml;
   ```

4. W `ChangeOSVersionCS` przestrzeni nazw, Zastąp `Program` Implementacja klasy z następującym kodem:

   ```csharp
   class Program
   {
      /// <summary>
      /// This function will set the minimum operating system version for a ClickOnce application.
      /// </summary>
      /// <param name="args">
      /// Command Line Arguments:
      /// 0 - Path to application manifest (.exe.manifest).
      /// 1 - Version of OS
      ///</param>
      static void Main(string[] args)
      {
         string applicationManifestPath = args[0];
         Console.WriteLine("Application Manifest Path: " + applicationManifestPath);

         // Get version name.
         Version osVersion = null;
         if (args.Length >=2 ){
            osVersion = new Version(args[1]);
         }else{
            throw new ArgumentException("OS Version not specified.");
         }
         Console.WriteLine("Desired OS Version: " + osVersion.ToString());

         XmlDocument document;
         XmlNamespaceManager namespaceManager;
         namespaceManager = new XmlNamespaceManager(new NameTable());
         namespaceManager.AddNamespace("asmv1", "urn:schemas-microsoft-com:asm.v1");
         namespaceManager.AddNamespace("asmv2", "urn:schemas-microsoft-com:asm.v2");

         document = new XmlDocument();
         document.Load(applicationManifestPath);

         string baseXPath;
         baseXPath = "/asmv1:assembly/asmv2:dependency/asmv2:dependentOS/asmv2:osVersionInfo/asmv2:os";

         // Change minimum required operating system version.
         XmlNode node;
         node = document.SelectSingleNode(baseXPath, namespaceManager);
         node.Attributes["majorVersion"].Value = osVersion.Major.ToString();
         node.Attributes["minorVersion"].Value = osVersion.Minor.ToString();
         node.Attributes["buildNumber"].Value = osVersion.Build.ToString();
         node.Attributes["servicePackMajor"].Value = osVersion.Revision.ToString();

         document.Save(applicationManifestPath);
      }
   }
   ```

    Polecenie przyjmuje dwa argumenty: ścieżkę manifestu aplikacji (czyli folderu, w którym proces kompilacji tworzy manifest, zwykle *Projectname.publish*), a nową wersję systemu operacyjnego.

5. Skompiluj projekt. Na **kompilacji** menu, kliknij przycisk **Kompiluj rozwiązanie**.

6. Kopiuj *.exe* plik do katalogu, takie jak *C:\TEMP\ChangeOSVersionVB.exe*.

   Następnie wywołaj to polecenie zdarzenie po kompilacji, aby zmodyfikować manifest aplikacji.

### <a name="to-invoke-a-post-build-event-to-modify-the-application-manifest"></a>Aby wywołać zdarzenie po kompilacji, aby zmodyfikować manifest aplikacji

1.  Tworzenie aplikacji Windows dla projektu, które mają zostać opublikowane. Z **pliku** menu wskaż **New**, a następnie kliknij przycisk **projektu**.

2.  W **nowy projekt** okna dialogowego rozwiń **Visual C#** , kliknij przycisk **pulpitu Windows**, a następnie kliknij przycisk **Windows Forms App** szablon. Nadaj projektowi nazwę `CSWinApp`.

3.  Za pomocą projektu wybranego w **Eksploratora rozwiązań**na **projektu** menu, kliknij przycisk **właściwości**.

4.  W **projektanta projektu**, zlokalizuj **Publikuj** strony, a następnie ustaw **publikowania lokalizacji** do *C:\TEMP*.

5.  Opublikuj projekt, klikając **Publikuj teraz**.

     Plik manifestu zostanie utworzone i umieścić w *C:\TEMP\CSWinApp_1_0_0_0\CSWinApp.exe.manifest*. Aby wyświetlić manifest, kliknij prawym przyciskiem myszy plik, kliknij przycisk **Otwórz za pomocą**, wybierz opcję **wybierz program, z listy**, a następnie kliknij przycisk **Notatnik**.

     Wyszukaj w pliku `<osVersionInfo>` elementu. Na przykład może być wersji:

    ```xml
    <os majorVersion="4" minorVersion="10" buildNumber="0" servicePackMajor="0" />
    ```

6.  W **projektanta projektu**, kliknij przycisk **zdarzenia kompilacji** kartę, a następnie kliknij przycisk **edytować po kompilacji** przycisku.

7.  W **wiersz polecenia zdarzenia po kompilacji** wpisz następujące polecenie:

     `C:\TEMP\ChangeOSVersionCS.exe "$(TargetPath).manifest" 5.1.2600.0`

     Podczas tworzenia projektu, to polecenie zmieni się w manifeście aplikacji wersja minimalna wersja systemu operacyjnego na 5.1.2600.0.

     Ponieważ `$(TargetPath)` — makro określa pełną ścieżkę do pliku wykonywalnego, trwa tworzenie `$(TargetPath)` *.manifest* określą manifestem aplikacji utworzonym w *bin* katalogu. Publikowanie skopiuje tego manifestu do lokalizacji publikowania, które zostały ustawione wcześniej.

8.  Opublikuj projekt ponownie. Przejdź do **Publikuj** strony, a następnie kliknij przycisk **Publikuj teraz**.

     Ponownie wyświetlić manifest. Aby wyświetlić manifest, otwórz katalog publikacji, kliknij prawym przyciskiem myszy plik, kliknij przycisk **otwierających**, wybierz opcję **wybierz program, z listy**, a następnie kliknij przycisk **Notatnik**.

     Wersja powinien mieć teraz treść:

    ```xml
    <os majorVersion="5" minorVersion="1" buildNumber="2600" servicePackMajor="0" />
    ```

## <a name="see-also"></a>Zobacz także

- [Strona zdarzenia, Projektant projektu kompilacji (C#)](../ide/reference/build-events-page-project-designer-csharp.md)
- [Okno dialogowe wiersz polecenia zdarzenia/po kompilacji — zdarzenie prekompilacyjne](../ide/reference/pre-build-event-post-build-event-command-line-dialog-box.md)
- [Porady: Określanie Tworzenie zdarzenia (Visual Basic)](../ide/how-to-specify-build-events-visual-basic.md)
- [Kompilowanie i tworzenie kompilacji](../ide/compiling-and-building-in-visual-studio.md)