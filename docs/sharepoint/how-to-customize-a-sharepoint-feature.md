---
title: 'Porady: dostosowywanie funkcji SharePoint | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
f1_keywords:
- VS.SharePointTools.RAD.FeatureDesigner.SwitchView
- VS.SharePointTools.RAD.featureDesigner.Manifest
- VS.SharePointTools.RAD.FeatureDesignerProperties
dev_langs:
- VB
- CSharp
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, features
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 9be9ba70bb94e743a788db11b55c188275bcad64
ms.sourcegitcommit: d9e4ea95d0ea70827de281754067309a517205a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/29/2018
ms.locfileid: "37120300"
---
# <a name="how-to-customize-a-sharepoint-feature"></a>Porady: dostosowywanie funkcji SharePoint
  Można tworzyć i dostosowywać funkcje programu SharePoint przy użyciu narzędzia Projektant Funkcji w programie Visual Studio. Na przykład można ustawić zakres funkcji i dodać inne funkcje jako zależności. Domyślnie Projektant Funkcji jest otwarty podczas dodawania nowych funkcji w Eksploratorze rozwiązań lub w Eksploratorze pakietu programu SharePoint.  
  
## <a name="opening-the-feature-designer"></a>Otwieranie Projektanta Funkcji  
 Można dodawać i usuwać elementy SharePoint do projektu funkcji przy użyciu narzędzia Projektanta Funkcji.  
  
#### <a name="to-open-the-feature-designer"></a>Aby otworzyć Projektanta Funkcji
  
1.  W **Eksploratorze rozwiązań**, rozwiń węzeł **funkcji**.  
  
2.  Kliknij dwukrotnie na element *Feature1*, lub Otwórz menu skrótów elementu *Feature1*, a następnie wybierz pozycję **Widok projektanta**.  
  
## <a name="view-the-packaged-manifest-file"></a>Wyświetl spakowany plik manifestu  
 Projektant funkcji może służyć do modyfikacji i generowania pliku manifestu spakowanych funkcji (*feature.xml*). Następnie można wyświetlić kod XML dla tego pliku w programie Visual Studio.  
  
#### <a name="to-view-the-packaged-manifest-file"></a>Aby wyświetlić spakowany pliku manifestu  
  
1.  W **Projektancie funkcji**, wybierz kartę **Manifest**.  
  
#### <a name="to-view-the-packaged-manifest-file-by-using-solution-explorer"></a>Aby wyświetlić spakowany plik manifestu za pomocą Eksploratora rozwiązań  
  
1.  W **Eksploratorze rozwiązań**, wybierz ikonę **Pokaż wszystkie pliki**.  
  
2.  Rozwiń węzeł funkcje, rozwiń NazwaFunkcji, rozwiń NazwaFunkcji.feature, a następnie otwórz plik *\<Nazwa_funkcji >. Template.XML*.  
  
    > [!NOTE]  
    >  Po otwarciu szablonu manifestu funkcji w formacie pliku XML, pliki zostaną automatycznie sprawdzone i można zignorować ostrzeżenia, które są wyświetlane w oknie Lista błędów.  
  
## <a name="change-the-manifest-template"></a>Zmień szablon manifestu  
 Można zmienić kod XML w edytorze XML programu Visual Studio lub w okienku manifestu szablonu pliku manifestu funkcji. Wszelkie zmiany w kodzie XML są scalane do spakowanego pliku manifestu funkcji. Na przykład można zmienić szablon manifestu, aby dostosować właściwość funkcji.  
  
#### <a name="to-change-the-manifest-template-by-using-the-xml-editor"></a>Zmień szablon manifestu za pomocą edytora XML  
  
1.  W **Projektancie Funkcji**, wybierz kartę **Manifest**, rozwiń węzeł **Edytuj opcje**, a następnie wybierz **Otwórz w edytorze XML**.  
  
     Zmiany w pliku XML są scalane w spakowanym pliku manifestu.  
  
#### <a name="to-change-the-manifest-template-by-using-the-manifest-template-pane"></a>Zmień szablon manifestu przy użyciu okna szablonu manifestu  
  
1.  W **Projektancie Funkcji**, wybierz kartę **Manifest**, rozwiń węzeł **Edytuj opcje**, a następnie zmień plik XML, który zostanie wyświetlony w okienku manifestu szablonu.  
  
     Zmiany w pliku XML są wyświetlane w oknie **Podgląd spakowanego manifestu**.  
  
## <a name="overwrite-the-packaged-manifest-file"></a>Zastąp spakowane pliki manifestu  
 Można wyłączyć Funkcję Projektanta i utworzyć *feature.xml* plik ręcznie. Po pierwszym wykonaniu bieżące ustawienia są zapisywane do pliku XML szablonu funkcji w Projektancie Funkcji. Następnie można zmodyfikować lub zastąpić kod XML.  
  
> [!NOTE]  
>  Jeśli dodasz lub usuniesz elementy projektu SharePoint w pliku XML, gdy Projektant Funkcji jest wyłączony, te elementy projektu nie są spakowane.  
  
#### <a name="to-overwrite-packaged-manifest-file-by-disabling-the-designer"></a>Zastąp spakowany plik manifestu poprzez wyłączenie Projektanta  
  
1.  W **Projektanta Funkcji**, wybierz kartę **Manifest**.  
  
2.  Rozwiń węzeł **Edytuj opcje**, wybierz łącze **Zastąp wygenerowany kod XML i edycja manifestu w edytorze XML**, a następnie wybierz przycisk **Tak**.  
  
     Szablon zostanie zaktualizowany o spakowany plik bieżącego manifestu.  
  
## <a name="enable-the-feature-designer"></a>Włącz Projektanta Funkcji  
 Można ponownie włączyć Projektanta Funkcji, aby dostosować plik *feature.xml*.  
  
#### <a name="to-re-enable-the-designer"></a>Aby ponownie włączyć Projektanta  
  
1.  W **Projektancie Funkcji**, wybierz łącze **Odrzuć zmiany manifestu i ponownie włącz Projektanta**, a następnie wybierz przycisk **Tak**.  
  
2.  Szablon zostanie odświeżony z początkowym tekstem, a zmiany wprowadzone w pliku XML zostaną utracone.  
  
## <a name="see-also"></a>Zobacz także
 [Pakiet i wdrażanie rozwiązań SharePoint](../sharepoint/packaging-and-deploying-sharepoint-solutions.md)  
  
