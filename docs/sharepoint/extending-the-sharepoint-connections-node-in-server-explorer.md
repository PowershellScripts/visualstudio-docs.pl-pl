---
title: Rozszerzanie węzła połączeń SharePoint w Eksploratorze serwera | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint Connections [SharePoint development in Visual Studio], extending a node
- SharePoint development in Visual Studio, extending SharePoint Connections node in Server Explorer
- SharePoint Connections [SharePoint development in Visual Studio], creating a new node type
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: f7211d31b8e57a88d3f6a5a585e912dd267cf943
ms.sourcegitcommit: e6b13898cfbd89449f786c2e8f3e3e7377afcf25
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/22/2018
ms.locfileid: "36325589"
---
# <a name="extend-the-sharepoint-connections-node-in-server-explorer"></a>Rozszerzanie węzła połączeń SharePoint w Eksploratorze serwera
  W programie Visual Studio można nawiązać lokalnych witryn programu SharePoint na komputerze dewelopera przy użyciu **połączeń SharePoint** w węźle **Eksploratora serwera** okna. Ten węzeł Wyświetla wielu składników lokalnych witryn programu SharePoint w hierarchicznym widoku drzewa. Na przykład można wyświetlić listy, biblioteki dokumentów i typy zawartości w lokacji lokalnej. Aby uzyskać więcej informacji o korzystaniu z **Eksploratora serwera** nawiązać lokalnych witryn programu SharePoint, zobacz [połączeń SharePoint Przeglądaj za pomocą Eksploratora serwera](../sharepoint/browsing-sharepoint-connections-using-server-explorer.md).  
  
 Można rozszerzyć **połączeń SharePoint** węzła przez tworzenie rozszerzeń dla istniejących węzłów lub przez tworzenie niestandardowego typu i dodanie go do hierarchii z węzłów.  
  
## <a name="tasks-for-extending-the-sharepoint-connections-node"></a>Zadania dla rozszerzanie węzła połączeń SharePoint
 Aby rozszerzyć istniejący węzeł, tworzenia rozszerzenia programu Visual Studio, który implementuje <xref:Microsoft.VisualStudio.SharePoint.Explorer.IExplorerNodeTypeExtension> interfejsu. Podczas rozszerzania węzła do węzła, takie jak własne elementy menu skrótów lub właściwości niestandardowe można dodać funkcji. Aby uzyskać więcej informacji, zobacz [porady: rozszerzanie węzła SharePoint w Eksploratorze serwera](../sharepoint/how-to-extend-a-sharepoint-node-in-server-explorer.md).  
  
 Do utworzenia typu niestandardowego, tworzenia rozszerzenia programu Visual Studio, który implementuje <xref:Microsoft.VisualStudio.SharePoint.Explorer.IExplorerNodeTypeProvider> interfejsu. Tworzenie niestandardowego węzła, jeśli chcesz wyświetlić składniki witryny programu SharePoint, które nie są wyświetlane w **Eksploratora serwera** domyślnie. Na przykład **Eksploratora serwera** jest nie wyświetlania galerii składników Web Part w witrynie programu SharePoint przez domyślny, ale można dodać niestandardowe węzła, w tym. Aby uzyskać więcej informacji, zobacz [porady: Dodawanie niestandardowego węzła SharePoint do Eksploratora serwera](../sharepoint/how-to-add-a-custom-sharepoint-node-to-server-explorer.md) i [wskazówki: rozszerzanie Eksploratora serwera do części sieci Web wyświetlaną](../sharepoint/walkthrough-extending-server-explorer-to-display-web-parts.md).  
  
## <a name="add-custom-properties-to-nodes"></a>Dodawanie właściwości niestandardowych do węzłów
 Rozszerzanie węzła lub utworzenie typu niestandardowego, można dodać właściwości niestandardowe do węzła. Właściwości są wyświetlane w **właściwości** okna po wybraniu węzła.  
  
 Istnieją dwa typy właściwości niestandardowe, które można dodać do węzła:  
  
-   Właściwości, które wyświetlić zestaw danych tylko do odczytu z witryny programu SharePoint. Dane w tym artykule opisano składnik programu SharePoint, która reprezentuje węzeł. Aby uzyskać wskazówki, które pokazuje, jak to zrobić, zobacz [wskazówki: rozszerzanie Eksploratora serwera do wyświetlania elementów sieci web](../sharepoint/walkthrough-extending-server-explorer-to-display-web-parts.md).  
  
-   Właściwości wyświetlanych danych niestandardowych odczytu/zapisu. Na przykład kodu, który pokazuje, jak to zrobić, zobacz [porady: rozszerzanie węzła SharePoint w Eksploratorze serwera](../sharepoint/how-to-extend-a-sharepoint-node-in-server-explorer.md).  
  
## <a name="get-data-for-built-in-nodes"></a>Pobieranie danych dla wbudowanego węzłów
 Obejmują wszystkie węzły wbudowanych dostarczane przez program Visual Studio niektóre dane dotyczące składnik programu SharePoint, które reprezentują. Węzeł, który reprezentuje listę w witrynie programu SharePoint umożliwia na przykład niektóre dane dotyczące listy, takie jak tytuł i adres URL domyślny widok listy.  
  
 Aby uzyskać dostęp do tych danych, należy pobrać obiekt danych z <xref:Microsoft.VisualStudio.SharePoint.IAnnotatedObject.Annotations%2A> właściwość <xref:Microsoft.VisualStudio.SharePoint.Explorer.IExplorerNode> obiekt, który reprezentuje węzeł planuje się. Typ obiektu danych zależy od typu węzła.  
  
 Poniższy przykład kodu pokazuje, jak można pobrać obiektu danych dla węzła listy. Aby wyświetlić ten przykład w kontekście większego przykładu, zobacz [porady: pobieranie danych dla wbudowanego węzła SharePoint w Eksploratorze serwera](../sharepoint/how-to-get-data-for-a-built-in-sharepoint-node-in-server-explorer.md).  
  
 [!code-vb[SPExtensibility.ProjectSystemExtension.General#11](../sharepoint/codesnippet/VisualBasic/projectsystemexamples/extension/serverexplorerextensionnodeinfo.vb#11)]
 [!code-csharp[SPExtensibility.ProjectSystemExtension.General#11](../sharepoint/codesnippet/CSharp/projectsystemexamples/extension/serverexplorerextensionnodeinfo.cs#11)]  
  
 W poniższej tabeli wymieniono typy obiektów danych dla każdego typu wbudowanego węzła.  
  
|Typ węzła|Typ obiektu danych|  
|---------------|----------------------|  
|Węzeł witryny programu SharePoint|<xref:Microsoft.VisualStudio.SharePoint.Explorer.IExplorerSiteNodeInfo>|  
|Typ zawartości|<xref:Microsoft.VisualStudio.SharePoint.Explorer.Extensions.IContentTypeNodeInfo>|  
|Funkcja|<xref:Microsoft.VisualStudio.SharePoint.Explorer.Extensions.IFeatureNodeInfo>|  
|Pole|<xref:Microsoft.VisualStudio.SharePoint.Explorer.Extensions.IFieldNodeInfo>|  
|Lista|<xref:Microsoft.VisualStudio.SharePoint.Explorer.Extensions.IListNodeInfo>|  
|Szablon listy|<xref:Microsoft.VisualStudio.SharePoint.Explorer.Extensions.IListTemplateNodeInfo>|  
|Widok listy (Microsoft.SharePoint.SPView)|<xref:Microsoft.VisualStudio.SharePoint.Explorer.Extensions.IListViewNodeInfo>|  
|Skojarzenia przepływu pracy|<xref:Microsoft.VisualStudio.SharePoint.Explorer.Extensions.IWorkflowAssociationNodeInfo>|  
|Szablon przepływu pracy|<xref:Microsoft.VisualStudio.SharePoint.Explorer.Extensions.IWorkflowTemplateNodeInfo>|  
  
 Aby uzyskać więcej informacji o korzystaniu z <xref:Microsoft.VisualStudio.SharePoint.IAnnotatedObject.Annotations%2A> właściwości, zobacz [rozszerzeń narzędzi kojarzenie danych niestandardowych z programem SharePoint](../sharepoint/associating-custom-data-with-sharepoint-tools-extensions.md).  
  
## <a name="see-also"></a>Zobacz także
 [Wskazówki: Rozszerzanie Eksploratora serwera do wyświetlania elementów sieci web](../sharepoint/walkthrough-extending-server-explorer-to-display-web-parts.md)   
 [Porady: rozszerzanie węzła SharePoint w Eksploratorze serwera](../sharepoint/how-to-extend-a-sharepoint-node-in-server-explorer.md)   
 [Porady: Dodawanie niestandardowego węzła SharePoint do Eksploratora serwera](../sharepoint/how-to-add-a-custom-sharepoint-node-to-server-explorer.md)   
 [Porady: pobieranie danych dla wbudowanego węzła SharePoint w Eksploratorze serwera](../sharepoint/how-to-get-data-for-a-built-in-sharepoint-node-in-server-explorer.md)   
 [Kojarzenie danych niestandardowych z rozszerzeniami narzędzi SharePoint](../sharepoint/associating-custom-data-with-sharepoint-tools-extensions.md)   
 [Przeglądanie połączeń SharePoint za pomocą Eksploratora serwera](../sharepoint/browsing-sharepoint-connections-using-server-explorer.md)   
 [Rozszerzanie narzędzi SharePoint w Visual Studio](../sharepoint/extending-the-sharepoint-tools-in-visual-studio.md)  
  
  
