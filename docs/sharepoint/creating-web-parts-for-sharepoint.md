---
title: "Tworzenie składników Web Part dla SharePoint | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 02/02/2017
ms.reviewer: 
ms.suite: 
ms.technology: office-development
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- Microsoft.SharePoint.WebControls.DateTimeControl
- Microsoft.SharePoint.WebControls.CssLink
- Microsoft.SharePoint.WebControls.RssLink
- Microsoft.SharePoint.WebControls.Theme
- Microsoft.SharePoint.WebControls.AspMenu
- Microsoft.SharePoint.WebControls.ListProperty
- Microsoft.SharePoint.WebControls.ProjectProperty
- Microsoft.SharePoint.WebControls.FormsDigest
- Microsoft.SharePoint.WebControls.ScriptLink
dev_langs:
- VB
- CSharp
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, Web Parts
- Web Parts [SharePoint development in Visual Studio], designing
ms.assetid: a6349e85-45cf-4766-b856-e25c9f1ffd34
caps.latest.revision: "42"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 5bba3f2e5f645b6b97fb43b22e7dfc1028a01ab0
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="creating-web-parts-for-sharepoint"></a>Tworzenie części sieciowych dla SharePoint
  Przy użyciu składników web Part, można zmodyfikować zawartość, wyglądu i zachowania stron witryny programu SharePoint za pomocą przeglądarki. Formanty po stronie serwera, które są uruchamiane wewnątrz strony sieci web są składniki Web Part: są blokami konstrukcyjnymi stron, które znajdują się w witrynie programu SharePoint. Zobacz [bloków konstrukcyjnych: składnikami Web Part](http://go.microsoft.com/fwlink/?LinkID=182097).  
  
 Można tworzyć i debugować części sieci web w witrynie programu SharePoint przy użyciu szablonów w programie Visual Studio.  
  
## <a name="creating-a-web-part-in-visual-studio"></a>Tworzenie składnika Web Part w programie Visual Studio  
 Tworzenie składnika web part, dodając **składnika Web Part** element do żadnego projektu programu SharePoint. Można użyć **składnika Web Part** elementu w trybie piaskownicy rozwiązania lub rozwiązaniu farmy.  
  
 Jeśli chcesz wizualnie projektowania składnika web part za pomocą projektanta, należy utworzyć **wizualnego składnika Web Part** lub Dodaj **wizualnego składnika Web Part** element do żadnego projektu programu SharePoint. Można użyć **wizualnego składnika Web Part** elementu w rozwiązaniu farmy.  
  
### <a name="web-part-item"></a>Element składnika Web Part  
 A **składnika Web Part** elementu zawiera pliki używane do projektowania składnika web part w witrynie programu SharePoint. Po dodaniu **składnika Web Part** elementu, Visual Studio tworzy folder w projekcie, a następnie dodaje kilka plików do folderu. W poniższej tabeli opisano każdego pliku.  
  
|Plik|Opis|  
|----------|-----------------|  
|Elements.XML|Zawiera informacje, które używa pliku definicji funkcji w projekcie, aby wdrożyć składnik web part.|  
|plik .webpart|Udostępnia informacje wymagające do wyświetlania składnika web part w galerii składników web part programu SharePoint.|  
|Plik kodu|Zawiera metody, która dodawanie formantów do składnika web part i który Generowanie niestandardowych zawartości w ramach składnika web part.|  
  
 Aby uzyskać więcej informacji, zobacz [porady: Tworzenie składnika Web Part programu SharePoint](../sharepoint/how-to-create-a-sharepoint-web-part.md).  
  
### <a name="visual-web-part-item"></a>Element wizualnego składnika Web Part  
 Wizualny składnik web part jest składnik web part, który utworzono przy użyciu narzędzia Projektant Visual Web Developer w programie Visual Studio. Wizualny składnik web part działa tak samo, jak inne części sieci web. Aby dodać formanty, takie jak przycisków i pola tekstowe do składnika web part, Dodaj kod do pliku XML. Jednak dodawanie formantów do wizualnego składnika web part przeciągając lub skopiować je do składnika web part z programu Visual Studio **przybornika**. Projektant następnie generuje kod wymagany w pliku XML. Zobacz [porady: tworzenie SharePoint Web Part za pomocą projektanta](../sharepoint/how-to-create-a-sharepoint-web-part-by-using-a-designer.md).  
  
## <a name="sharepoint-controls"></a>Formanty programu SharePoint  
 Program Visual Studio udostępnia niektóre formanty do tworzenia strony programu SharePoint, takich jak strony aplikacji. Formanty te są wyświetlane w **przybornika** w obszarze **formanty programu SharePoint**. Funkcja tych kontrolek pochodną [Microsoft.SharePoint.WebControls](http://go.microsoft.com/fwlink/?LinkId=235315) przestrzeni nazw, który zawiera formanty serwera ASP.NET, które są używane na stronach witryny i listy programu SharePoint.  
  
|Nazwa formantu|Opis|  
|------------------|-----------------|  
|[AspMenu](http://go.microsoft.com/fwlink/?LinkId=235307)|Wstawia menu ASP. Aby uzyskać więcej informacji, zobacz [informacje o formancie Menu](http://go.microsoft.com/fwlink/?LinkId=235316).|  
|[CssLink](http://go.microsoft.com/fwlink/?LinkId=235308)|Wstawia **łącze** elementu do strony aspx i stosuje co najmniej jednego zewnętrznego arkusza stylów zdefiniowanych przez **CssRegistration**.|  
|[DateTimeControl](http://go.microsoft.com/fwlink/?LinkId=235306)|Wstawia formantu daty i godziny do strony .aspx.|  
|[FormDigest](http://go.microsoft.com/fwlink/?LinkId=235309)|Wstawia walidacji zabezpieczeń na stronę .aspx|  
|[ListProperty](http://go.microsoft.com/fwlink/?LinkId=235310)|Zwraca właściwości określonej listy.|  
|[ProjectProperty](http://go.microsoft.com/fwlink/?LinkId=235311)|Zwraca globalnych właściwości bieżącej witryny sieci Web.|  
|[RssLink](http://go.microsoft.com/fwlink/?LinkId=235312)|Wstawia link do źródła danych RSS do strony .aspx.|  
|[Łącza](http://go.microsoft.com/fwlink/?LinkId=235313)|Udostępnia właściwości i metody do rejestrowania zasoby, takie jak skrypty, na stronie, dzięki czemu mogą być żądane podczas renderowania strony.|  
|[Motyw](http://go.microsoft.com/fwlink/?LinkId=235314)|Stosuje motyw do strony .aspx.|  
  
## <a name="debugging-a-web-part"></a>Debugowanie składnika Web Part  
 Można debugować projekt programu SharePoint, który zawiera składnik web part, tak jak będzie debugowania innych projektów programu Visual Studio. Po uruchomieniu debugera programu Visual Studio Visual Studio otworzy w witrynie programu SharePoint.  
  
 Aby rozpocząć debugowanie kodu, należy dodać składnik web part do strony sieci web w programie SharePoint.  
  
 Aby uzyskać więcej informacji na temat debugowania projektów SharePoint, zobacz [Rozwiązywanie problemów z rozwiązań SharePoint](../sharepoint/troubleshooting-sharepoint-solutions.md).  
  
## <a name="visual-web-part-limitations"></a>Ograniczenia wizualnego składnika Web Part  
 Począwszy od programu Visual Studio, można dodać części sieci web visual do rozwiązania programu SharePoint w trybie piaskownicy oraz rozwiązaniami farmy. Jednak części sieci web visual mają następujące ograniczenia:  
  
-   Parametry wymienne części sieci web Visual nie jest obsługiwane. Aby uzyskać więcej informacji, zobacz [parametry wymienne](../sharepoint/replaceable-parameters.md).  
  
-   Kontrolki użytkownika lub części programu visual web nie można przeciągnąć i porzucony lub skopiować na części sieci web programu visual. Ta akcja powoduje błąd kompilacji.  
  
-   Części sieci web Visual bezpośrednio nie obsługują tokenów serwera programu SharePoint, takich jak $SPUrl. Aby uzyskać więcej informacji, zobacz "Token ograniczenia w trybie piaskownicy Visual składników Web Part" w temacie [Rozwiązywanie problemów z rozwiązań SharePoint](../sharepoint/troubleshooting-sharepoint-solutions.md).  
  
-   Części sieci web Visual w trybie piaskownicy rozwiązania czasami komunikat o błędzie, "żądania wykonania kodu w trybie piaskownicy zostało odrzucone, ponieważ był zbyt zajęty, aby obsłużyć żądania usługi hosta kodu w trybie piaskownicy." Aby uzyskać więcej informacji na temat tego błędu, zobacz ten wpis w [Blog zespołu programu SharePoint Developer](http://go.microsoft.com/fwlink/?LinkId=225932).  
  
-   Debugowanie JavaScript po stronie serwera nie jest obsługiwany w programie Visual Studio, ale debugowanie JavaScript po stronie klienta jest obsługiwane.  
  
     Mimo że wbudowanego JavaScript można dodać do pliku znaczników po stronie serwera, debugowanie nie jest obsługiwana przez dodane znaczników punktów przerwania. Debugowanie JavaScript, odwołania zewnętrznego pliku JavaScript w pliku znaczników, a następnie ustaw punkty przerwania w pliku JavaScript.  
  
-   Debugowanie wbudowanego [!INCLUDE[vstecasp](../sharepoint/includes/vstecasp-md.md)] należy przeprowadzić kod w wygenerowanym pliku kodu zamiast w pliku znaczników.  
  
-   Części sieci web Visual nie obsługują `<@ Assembly Src=` dyrektywy.  
  
-   SharePoint sieci web, kontrolek, a niektóre [!INCLUDE[vstecasp](../sharepoint/includes/vstecasp-md.md)] formanty nie są obsługiwane w środowisku trybie piaskownicy programu SharePoint. Jeśli używane są nieobsługiwane formanty na wizualny składnik web part w trybie piaskownicy rozwiązania, błąd, zostanie wyświetlony "Nazwy typu lub przestrzeni nazw 'Motyw' nie istnieje w przestrzeni nazw"Microsoft.SharePoint.WebControls"".  
  
 Aby uzyskać więcej informacji o rozwiązaniach w trybie piaskownicy, zobacz [różnice między rozwiązaniami w trybie piaskownicy oraz rozwiązaniami farmy](../sharepoint/differences-between-sandboxed-and-farm-solutions.md).  
  
## <a name="creating-older-style-sharepoint-based-web-parts"></a>Tworzenie składników Web Part starszego stylu w oparciu o program SharePoint  
 Szablony programu Visual Studio służy do tworzenia niestandardowych [!INCLUDE[vstecasplong](../sharepoint/includes/vstecasplong-md.md)] web Part programu SharePoint. [!INCLUDE[vstecasplong](../sharepoint/includes/vstecasplong-md.md)]części sieci Web są tworzone nad [!INCLUDE[vstecasp](../sharepoint/includes/vstecasp-md.md)] infrastruktura składników web part i są zalecane typu dla nowych projektów.  
  
 W bardzo mało przypadków może być konieczne tworzenie składnika web part za pomocą starszej stylu oparty na programie SharePoint składnik web part. Visual Studio umożliwia tworzenie tych typów części sieci web, ale Visual Studio nie zapewnia żadnych szablonów, które są zaprojektowane specjalnie, aby można je utworzyć.  
  
 Aby uzyskać więcej informacji na temat po warto utworzyć starsze styl oparty na programie SharePoint składnik web part, zobacz [infrastruktury części sieci Web w programie Windows SharePoint Services](http://go.microsoft.com/fwlink/?LinkId=169290). Aby uzyskać więcej informacji na temat tworzenia składnika web part za pomocą starszej stylu oparty na programie SharePoint składnik web part, zobacz [wskazówki Tworzenie podstawowego składnika Web Part programu SharePoint](http://go.microsoft.com/fwlink/?LinkId=169288).  
  
## <a name="related-topics"></a>Tematy pokrewne  
  
|Tytuł|Opis|  
|-----------|-----------------|  
|[Porady: tworzenie SharePoint Web Part](../sharepoint/how-to-create-a-sharepoint-web-part.md)|Pokazuje, jak utworzyć części sieci web dla strony programu SharePoint.|  
|[Porady: tworzenie SharePoint Web Part za pomocą projektanta](../sharepoint/how-to-create-a-sharepoint-web-part-by-using-a-designer.md)|Przedstawiono sposób tworzenia składników web Part dla SharePoint za pomocą powierzchni projektu visual.|  
|[Porady: Tworzenie formantu użytkownika dla strony aplikacji SharePoint lub składnik Web Part](../sharepoint/how-to-create-a-user-control-for-a-sharepoint-application-page-or-web-part.md)|Pokazuje, jak utworzyć niestandardowe kontrolki do ponownego użycia, które mogą być używane przez stron aplikacji i składników web Part, które są uruchamiane w programie SharePoint.|  
|[Wskazówki: Tworzenie składnika Web Part dla SharePoint](../sharepoint/walkthrough-creating-a-web-part-for-sharepoint.md)|Opisuje sposób projektowania składnika web part programu SharePoint.|  
|[Wskazówki: Tworzenie składnika Web Part dla SharePoint za pomocą projektanta](../sharepoint/walkthrough-creating-a-web-part-for-sharepoint-by-using-a-designer.md)|Opisuje sposób projektowania składnika web part dla SharePoint przeciągając formanty powierzchnię projektu visual.|  
|[Wskazówki: Tworzenie składnika Web Part Silverlight wyświetlającego dane OData dla programu SharePoint](../sharepoint/walkthrough-creating-a-silverlight-web-part-that-displays-odata-for-sharepoint.md)|Opisuje sposób projektowania składnika web part programu SharePoint, która obsługuje aplikację Silverlight i wyświetla dane z listy programu SharePoint.|  
  
  