---
title: "Korzystanie z członków Microsoft.VisualStudio.TestTools.UnitTesting w testach jednostkowych | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-devops-test
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 0fa335fd-e442-448f-913f-25a19df90a93
caps.latest.revision: "6"
ms.author: douge
manager: douge
ms.openlocfilehash: 1a723104cdd350dcc2c5fac80eef4e98b178df4c
ms.sourcegitcommit: aadb9588877418b8b55a5612c1d3842d4520ca4c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2017
---
# <a name="using-microsoftvisualstudiotesttoolsunittesting-members-in-unit-tests"></a>Korzystanie z członków Microsoft.VisualStudio.TestTools.UnitTesting w testach jednostkowych
Framework testów jednostkowych obsługuje jednostki testowania w [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]. Użyj klas i członków w Microsoft.VisualStudio.TestPlatform.UnitTestFramework > przestrzenią nazw, gdy są kodowania testów jednostkowych. Można używać ich, gdy napisano jednostki przetestować od początku lub są uściślenie test jednostki, który został wygenerowany na podstawie kodu podczas testowania.  
  
## <a name="groups-of-elements"></a>Grupy elementów  
 Aby zapewnić lepszy przegląd Framework testów jednostkowych, w tej sekcji organizuje elementy obszaru nazw UnitTesting w grupy funkcje.  
  
> [!NOTE]
>  Atrybut elementów, których nazwy zawierają ciąg atrybutu, może służyć lub bez ciąg atrybutu. Na przykład następujący przykładowy kod dwóch działać tak samo:  
>   
>  `[TestClass()]`  
>   
>  `[TestClassAttribute()]`  
  
### <a name="elements-used-for-data-driven-testing"></a>Elementów używanych do testów opartych na danych  
 Następujące elementy umożliwia konfigurowanie testów jednostkowych opartych na danych. Aby uzyskać więcej informacji, zobacz [jak: tworzenie testu jednostkowego Data-driven](../test/how-to-create-a-data-driven-unit-test.md) i [wskazówki: Korzystanie z pliku konfiguracji do określania źródła danych](../test/walkthrough-using-a-configuration-file-to-define-a-data-source.md).  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.DataAccessMethod  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.DataSourceAttribute 
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.DataSourceElement  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.DataSourceElementCollection  
  
## <a name="attributes-used-to-establish-a-calling-order"></a>Atrybuty używany do ustanawiania kolejności wywoływania  
 Element kodu ozdobione jedną z następujących atrybutów jest wywoływana w tej chwili, które określisz. Aby uzyskać więcej informacji, zobacz [anatomia testu jednostkowego](http://msdn.microsoft.com/en-us/a03d1ee7-9999-4e7c-85df-7d9073976144).  
  
### <a name="for-assemblies"></a>Dla zestawów  
 AssemblyInitialize i AssemblyCleanup są nazywane prawo po załadowaniu używanemu zestawowi oraz prawo przed używanemu zestawowi zostanie zwolniona.  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.AssemblyInitializeAttribute  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.AssemblyCleanupAttribute  
  
### <a name="for-classes"></a>Dla klas  
 ClassInitialize i ClassCleanup są nazywane prawo po załadowaniu klasy i w prawo przed klasy zostanie zwolniona.  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.ClassInitializeAttribute  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.ClassCleanupAttribute  
  
### <a name="for-test-methods"></a>Dla metody testowe  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.TestInitializeAttribute  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.TestCleanupAttribute  
  
## <a name="attributes-used-to-identify-test-classes-and-methods"></a>Atrybuty używane do identyfikowania testu klasy i metody  
 Każda klasa testu musi mieć atrybut TestClass i każdej metody testu musi mieć atrybut TestMethod. Aby uzyskać więcej informacji, zobacz [anatomia testu jednostkowego](http://msdn.microsoft.com/en-us/a03d1ee7-9999-4e7c-85df-7d9073976144).  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.TestClassAttribute  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.TestMethodAttribute  
  
## <a name="assert-classes-and-related-exceptions"></a>Assert klasy i powiązanych wyjątków  
 Testy jednostkowe sprawdzić zachowanie określonych aplikacji przez ich użycie różnych rodzajów instrukcje Assert, wyjątków i atrybutów. Aby uzyskać więcej informacji, zobacz [korzystanie z klas potwierdzeń](../test/using-the-assert-classes.md).  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.Assert 
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.CollectionAssert  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.StringAssert  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.AssertFailedException  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.AssertInconclusiveException  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.UnitTestAssertException  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.ExpectedExceptionAttribute  
  
## <a name="the-testcontext-class"></a>Klasa TestContext  
 Następujące atrybuty i wartości do nich przypisane są wyświetlane w [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] okna właściwości dla określonej metody. Te atrybuty nie mają być dostępne za pośrednictwem kod testu jednostkowego. Zamiast tego mają wpływ na sposób testu jednostkowego jest używany lub Uruchom, albo przez użytkownika za pomocą środowiska IDE programu [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)], lub [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] aparatu testów. Na przykład niektóre z tych atrybutów są wyświetlane jako kolumny w oknie Test Manager, a okno wyników testu, które oznacza, że można używać ich do grupy i sortować testy i wyniki testu. Jeden taki atrybut jest TestPropertyAttribute, które umożliwia dodanie dowolnego metadanych do testów jednostkowych. Na przykład użytkownik może służyć do przechowywania nazwy przebiegu testowego, które obejmuje ten test, przez oznaczenie testu jednostkowego z `[TestProperty("TestPass", "Accessibility")]`. Lub może być używany do przechowywania wskaźnika typu testu jest: `[TestProperty("TestKind", "Localization")]`. Właściwości tworzenia za pomocą tego atrybutu, a wartość właściwości przypisania, zarówno wyświetlanych w [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] okna właściwości pod nagłówkiem **konkretnego testu**.  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.OwnerAttribute  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.DeploymentItemAttribute  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.DescriptionAttribute  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.HostTypeAttribute  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.IgnoreAttribute  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.PriorityAttribute  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.TestPropertyAttribute  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.WorkItemAttribute  
  
## <a name="test-configuration-classes"></a>Klasy konfiguracji testu  
  
-   Microsoft.TeamFoundation.TestManagement.Client.ObjectTypes >  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.TestConfigurationSection  
  
## <a name="attributes-used-for-generating-reports"></a>Atrybuty używane do generowania raportów  
 Atrybuty w tej sekcji dotyczą metody testowej, która ich dekoracji dla jednostek w hierarchii projektu [!INCLUDE[esprtfs](../code-quality/includes/esprtfs_md.md)] projektu zespołowego.  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.CssIterationAttribute  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.CssProjectStructureAttribute  
  
## <a name="classes-used-with-private-accessors"></a>Klasy używane z prywatnej metody dostępu  
 Zgodnie z opisem w [przy użyciu Publicize można utworzyć prywatnego akcesora](http://msdn.microsoft.com/en-us/2056c6a7-6672-42a7-8f53-fead33c56deb), można wygenerować testu jednostkowego dla metody prywatnej. Tej generacji tworzy klasie prywatnego akcesora, która tworzy wystąpienie obiektu PrivateObject klasy. Klasa PrivateObject jest klasa otoki umożliwiająca używa jako część procesu prywatnego akcesora odbicia. Klasa PrivateType jest podobny, ale jest używana do wywoływania prywatnych metod statycznych, zamiast wywoływania metod prywatnych wystąpienia.  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.PrivateObject  
  
-   Microsoft.VisualStudio.TestPlatform.UnitTestFramework.PrivateType  
  
## <a name="see-also"></a>Zobacz też  
 Microsoft.VisualStudio.TestPlatform.UnitTestFramework