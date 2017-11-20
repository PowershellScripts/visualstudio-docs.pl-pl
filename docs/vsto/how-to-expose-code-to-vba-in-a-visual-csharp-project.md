---
title: "Porady: udostępnianie kodu z VBA w projektach Visual C# | Dokumentacja firmy Microsoft"
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
helpviewer_keywords:
- Visual C# [Office development in Visual Studio], exposing code to VBA
- VBA [Office development in Visual Studio], exposing code in document-level customizations
- document-level customizations [Office development in Visual Studio], exposing code
- exposing code to VBA
ms.assetid: 56d5894b-4823-42f4-8c7e-d8739b859c52
caps.latest.revision: "25"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: a52060f1a1b2200109c5003321857915d95bd12a
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-expose-code-to-vba-in-a-visual-c-project"></a>Porady: udostępnianie kodu z VBA w projektach Visual C#
  Można udostępnianie kodu w projektach Visual C# na język Visual Basic dla kodu aplikacji (VBA), jeśli chcesz, aby dwa typy kodu do oddziaływać na siebie.  
  
 Proces Visual C# różni się od procesu Visual Basic. Aby uzyskać więcej informacji, zobacz [porady: udostępnianie kodu z VBA w projektach Visual Basic](../vsto/how-to-expose-code-to-vba-in-a-visual-basic-project.md).  
  
 [!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]  
  
## <a name="exposing-code-in-a-visual-c-project"></a>Udostępnianie kodu w projektach Visual C#  
 Aby włączyć kod VBA wywoływanie kodu w projektach Visual C#, należy zmodyfikować kod, tak aby widoczne dla modelu COM, a następnie ustaw **ReferenceAssemblyFromVbaProject** właściwości **True** w projektancie.  
  
 Aby uzyskać wskazówki, który demonstruje sposób wywołania metody w projektach Visual C# z kodu VBA, zobacz [wskazówki: Wywoływanie kodu z VBA w Visual C & 35; Projekt](../vsto/walkthrough-calling-code-from-vba-in-a-visual-csharp-project.md).  
  
#### <a name="to-expose-code-in-a-visual-c-project-to-vba"></a>Aby udostępnianie kodu w projektach Visual C# w VBA  
  
1.  Otwórz lub Utwórz projekt poziomie dokumentu, który jest oparty na dokument programu Word, skoroszyt programu Excel lub szablon programu Excel obsługującej makra i zawierający kod VBA.  
  
     Aby uzyskać więcej informacji na temat formatów plików dokumentów, które obsługuje makr zobacz [łączenie VBA i dostosowywanie na poziomie dokumentu](../vsto/combining-vba-and-document-level-customizations.md).  
  
    > [!NOTE]  
    >  Nie można użyć tej funkcji w projektach szablon programu Word.  
  
2.  Upewnij się, że kod VBA w dokumencie może działać bez monitowania użytkownika o włączenie makr. Zaufany kod VBA przez dodanie lokalizacji projektu pakietu Office do listy zaufanych lokalizacji w ustawieniach Centrum zaufania dla programu Word i Excel.  
  
3.  Dodaj element członkowski, który chcesz udostępnić VBA do publicznej klasy w projekcie ani deklarować nowy element członkowski jako **publicznego**.  
  
4.  Zastosuj następujące <xref:System.Runtime.InteropServices.ComVisibleAttribute> i <xref:System.Runtime.InteropServices.ClassInterfaceAttribute> atrybuty do klasy, która wyświetlasz VBA. Te atrybuty uwidaczniania klasy COM, ale bez generowania interfejsu klasy.  
  
    ```csharp  
    [System.Runtime.InteropServices.ComVisible(true)]  
    [System.Runtime.InteropServices.ClassInterface(  
        System.Runtime.InteropServices.ClassInterfaceType.None)]  
    ```  
  
5.  Zastąpienie **GetAutomationObject** metody klasy elementu hosta w projekcie można zwrócić wystąpienia klasy, która wyświetlasz VBA:  
  
    -   Jeśli wyświetlasz klasy elementu obsługującej VBA zastępują **GetAutomationObject** metodę, która należy do tej klasy, a następnie wróć bieżące wystąpienie klasy.  
  
        ```csharp  
        protected override object GetAutomationObject()  
        {  
            return this;  
        }  
        ```  
  
    -   Jeśli wyświetlasz klasę, która nie jest elementem hosta VBA zastępują **GetAutomationObject** metoda dowolnego hosta elementu w projekcie i zwrócić wystąpienia klasy elementu-host. Na przykład następujący kod przyjęto założenie, że wyświetlasz klasę o nazwie `DocumentUtilities` VBA.  
  
        ```csharp  
        protected override object GetAutomationObject()  
        {  
            return new DocumentUtilities();  
        }  
        ```  
  
     Aby uzyskać informacje o obiektach hosta, zobacz [elementów hosta i informacje o formantach hosta](../vsto/host-items-and-host-controls-overview.md).  
  
6.  Wyodrębnij interfejs z klasy, która wyświetlasz VBA. W **wyodrębniania interfejsu** oknie dialogowym Wybierz publiczne elementy członkowskie, które chcesz uwzględnić w deklaracji interfejsu. Aby uzyskać więcej informacji, zobacz [wyodrębnić refaktoryzacji interfejsu &#40; K & 35; &#41; ](/visualstudio/csharp-ide/extract-interface-refactoring-csharp).  
  
7.  Dodaj **publicznego** — słowo kluczowe do deklaracji interfejsu.  
  
8.  Udostępnienie interfejs dla modelu COM przez dodanie poniższego <xref:System.Runtime.InteropServices.ComVisibleAttribute> do interfejsu.  
  
    ```csharp  
    [System.Runtime.InteropServices.ComVisible(true)]  
    ```  
  
9. Otwórz dokument (dla programu Word) lub arkusz (dla programu Excel) w projektancie w [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)].  
  
10. W **właściwości** wybierz **ReferenceAssemblyFromVbaProject** właściwości i zmień wartość na **True**.  
  
    > [!NOTE]  
    >  Jeśli skoroszytu lub dokument nie zawiera kodu VBA lub jeśli kod VBA w dokumencie nie jest zaufany do uruchomienia, zostanie wyświetlony komunikat o błędzie w przypadku ustawienia **ReferenceAssemblyFromVbaProject** właściwości **True**. Jest to spowodowane Visual Studio nie może modyfikować projektu VBA w dokumencie w takiej sytuacji.  
  
11. Kliknij przycisk **OK** w komunikacie, który jest wyświetlany. Ten komunikat przypomina o tym, że jeśli dodasz VBA kodu do skoroszytu lub dokumentu podczas uruchamiania projektu z [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)], kod VBA zostaną utracone przy następnym uruchomieniu skompilować projekt. Jest to spowodowane dokumentu w kompilacji output się, że folder zostanie zastąpiony zawsze skompilować projekt.  
  
     W tym momencie program Visual Studio konfiguruje projekt tak, aby projekt VBA można wywołać w zestawie. Visual Studio również dodaje metodę o nazwie `GetManagedClass` do projektu języka VBA. Tę metodę można wywołać z dowolnego miejsca w projekcie VBA dostępu do tej klasy, która narażonych na VBA.  
  
12. Skompiluj projekt.  
  
## <a name="see-also"></a>Zobacz też  
 [Porady: tworzenie projektów Office w Visual Studio](../vsto/how-to-create-office-projects-in-visual-studio.md)   
 [Projektowanie i tworzenie rozwiązań pakietu Office](../vsto/designing-and-creating-office-solutions.md)   
 [Łączenie VBA i dostosowywanie na poziomie dokumentu](../vsto/combining-vba-and-document-level-customizations.md)   
 [Wskazówki: Wywoływanie kodu z VBA w Visual C & 35; Projekt](../vsto/walkthrough-calling-code-from-vba-in-a-visual-csharp-project.md)   
 [Porady: udostępnianie kodu z VBA w projektach Visual Basic](../vsto/how-to-expose-code-to-vba-in-a-visual-basic-project.md)  
  
  