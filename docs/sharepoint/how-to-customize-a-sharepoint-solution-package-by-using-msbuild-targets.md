---
title: "Porady: Dostosowywanie pakietu rozwiązania SharePoint przy użyciu docelowych elementów MSBuild | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 02/02/2017
ms.reviewer: 
ms.suite: 
ms.technology: office-development
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
- VB
- CSharp
helpviewer_keywords: SharePoint development in Visual Studio, packages
ms.assetid: 7fa6a276-04c8-463e-be95-57c2c6240d76
caps.latest.revision: "15"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 758cf3e62621c22f3f97dc62b70c745afb860b8a
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-customize-a-sharepoint-solution-package-by-using-msbuild-targets"></a>Wskazówki: Dostosowywanie pakietu rozwiązania SharePoint przy użyciu docelowych elementów MSBuild
  Przy użyciu docelowych elementów MSBuild w wierszu polecenia, można dostosować, jak program Visual Studio tworzy pliki pakietu programu SharePoint (wsp). Na przykład można dostosować właściwości programu MSBuild, aby zmienić katalog pośredni pakowania i grup elementów MSBuild określające wyliczany plików.  
  
## <a name="customizing-and-running-msbuild-targets"></a>Dostosowywanie i uruchamianie docelowych elementów MSBuild  
 W przypadku dostosowania BeforeLayout i AfterLayout obiekty docelowe, można wykonać zadania przed układu pakietu, takich jak dodawanie, usuwanie lub modyfikowanie plików, które zostaną dodane do pakietu.  
  
#### <a name="to-customize-the-beforelayout-target"></a>Aby dostosować docelowej BeforeLayout  
  
1.  Otwórz Edytor, takiego jak Notatnik, a następnie dodaj poniższy kod.  
  
    ```  
    <Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
      <Target Name="BeforeLayout">  
        <Message Importance="high" Text="In the BeforeLayout Target"></Message>  
      </Target>  
    </Project>  
    ```  
  
     W tym przykładzie wyświetla komunikat przed opakowywanie ten element docelowy.  
  
2.  Nadaj nazwę plikowi **CustomLayout.SharePoint.targets**, a następnie zapisz go w folderze projektu programu SharePoint.  
  
3.  Otwórz projekt, otwórz menu skrótów, a następnie wybierz **Zwolnij projekt**.  
  
4.  W **Eksploratora rozwiązań**, otwórz menu skrótów projektu, a następnie wybierz **Edytuj***ProjectName***vbproj** lub **Edytować***ProjectName***.csproj**.  
  
5.  Po `Import` wiersz pod koniec pliku projektu, Dodaj następujący wiersz.  
  
    ```  
    <Import Project="CustomLayout.SharePoint.targets" />  
    ```  
  
6.  Zapisz i zamknij plik projektu.  
  
7.  W **Eksploratora rozwiązań**, otwórz menu skrótów projektu, a następnie wybierz **Załaduj ponownie projekt**.  
  
 Podczas publikowania projektu, komunikat zostanie wyświetlony w danych wyjściowych, przed rozpoczęciem tworzenia pakietów.  
  
#### <a name="to-customize-the-afterlayout-target"></a>Aby dostosować docelowy AfterLayout  
  
1.  Na pasku menu wybierz **pliku**, **Otwórz**, **pliku**.  
  
2.  W **Otwórz plik** okno dialogowe, przejdź do folderu projektu, wybierz plik CustomLayout.target, a następnie wybierz **Otwórz** przycisku.  
  
3.  Tuż przed `</Project>` tagów, Dodaj następujący kod:  
  
    ```  
    <Target Name="AfterLayout">  
      <Message Importance="high" Text="In the AfterLayout Target"></Message>  
    </Target>  
    ```  
  
     W tym przykładzie wyświetla komunikat po spakowaniu ten element docelowy.  
  
4.  Zapisz i zamknij plik elementów docelowych.  
  
5.  Uruchom ponownie program Visual Studio, a następnie otworzyć projekt.  
  
 Podczas publikowania projektu, zostanie wyświetlony komunikat BeforeLayout przed rozpoczęciem tworzenia pakietów i AfterLayout pojawi się po zakończeniu tworzenia pakietów.  
  
## <a name="see-also"></a>Zobacz też  
 [Pakowanie i wdrażanie rozwiązań SharePoint](../sharepoint/packaging-and-deploying-sharepoint-solutions.md)  
  
  