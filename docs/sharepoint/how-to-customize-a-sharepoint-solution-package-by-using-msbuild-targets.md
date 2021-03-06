---
title: 'Porady: Dostosowywanie pakietu rozwiązania SharePoint przy użyciu docelowych elementów MSBuild | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, packages
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 434d673c62d0b26efa1559db7d7d98747146fd2d
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49889692"
---
# <a name="how-to-customize-a-sharepoint-solution-package-by-using-msbuild-targets"></a>Porady: Dostosowywanie pakietu rozwiązania SharePoint przy użyciu docelowych elementów MSBuild
  Przy użyciu docelowych elementów MSBuild w wierszu polecenia, można dostosować, jak program Visual Studio tworzy pliki pakietu programu SharePoint (*.wsp*). Na przykład można dostosować właściwości programu MSBuild, aby zmienić katalog pośredni pakowania i grup elementów MSBuild, określających wyliczany plików.  
  
## <a name="customize-and-run-msbuild-targets"></a>Dostosowywanie i uruchamianie elementów docelowych MSBuild  
 Możesz dostosować BeforeLayout i AfterLayout obiekty docelowe, po wykonaniu zadań przed układu pakietu, takie jak dodawanie, usuwanie lub modyfikowanie plików, które zostanie umieszczony w pakiecie.  
  
#### <a name="to-customize-the-beforelayout-target"></a>Aby dostosować docelowej BeforeLayout  
  
1. Otwórz edytora, takiego jak Notatnik, a następnie dodaj następujący kod.  
  
   ```xml  
   <Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
     <Target Name="BeforeLayout">  
       <Message Importance="high" Text="In the BeforeLayout Target"></Message>  
     </Target>  
   </Project>  
   ```  
  
    W tym przykładzie wyświetla komunikat przed opakowanie ten element docelowy.  
  
2. Nadaj plikowi nazwę **CustomLayout.SharePoint.targets**, a następnie zapisz go w folderze projektu programu SharePoint.  
  
3. Otwórz projekt, otwórz jego menu skrótów, a następnie wybierz **Zwolnij projekt**.  
  
4. W **Eksploratora rozwiązań**, otwórz menu skrótów dla projektu, a następnie wybierz **Edytuj**  *\<nazwa_projektu > .vbproj* lub **Edytuj**  *\<Nazwa_projektu > .csproj*.  
  
5. Po `Import` wiersz w pobliżu końca pliku projektu, Dodaj następujący wiersz.  
  
   ```xml  
   <Import Project="CustomLayout.SharePoint.targets" />  
   ```  
  
6. Zapisz i zamknij plik projektu.  
  
7. W **Eksploratora rozwiązań**, otwórz menu skrótów dla projektu, a następnie wybierz **Załaduj ponownie projekt**.  
  
   Podczas publikowania projektu, zostanie wyświetlony komunikat w danych wyjściowych przed rozpoczęciem tworzenia pakietów.  
  
#### <a name="to-customize-the-afterlayout-target"></a>Aby dostosować docelowej AfterLayout  
  
1. Na pasku menu wybierz **pliku** > **Otwórz** > **pliku**.  
  
2. W **Otwórz plik** okno dialogowe, przejdź do folderu projektu, wybierz plik CustomLayout.target, a następnie wybierz **Otwórz** przycisku.  
  
3. Tuż przed `</Project>` tag, Dodaj następujący kod:  
  
   ```xml  
   <Target Name="AfterLayout">  
     <Message Importance="high" Text="In the AfterLayout Target"></Message>  
   </Target>  
   ```  
  
    W tym przykładzie wyświetla komunikat po ten element docelowy jest spakowany.  
  
4. Zapisz i zamknij plik elementów docelowych.  
  
5. Uruchom ponownie program Visual Studio, a następnie otwórz projekt.  
  
   Podczas publikowania projektu, pojawi się komunikat BeforeLayout przed rozpoczęciem tworzenia pakietów, a AfterLayout komunikat jest wyświetlany po zakończeniu tworzenia pakietów.  
  
## <a name="see-also"></a>Zobacz także
 [Pakowanie i wdrażanie rozwiązań SharePoint](../sharepoint/packaging-and-deploying-sharepoint-solutions.md)  
  
