---
title: "Narzędzia XML w Visual Studio | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vb.xmldesigner
helpviewer_keywords:
- XML [Visual Studio], resources
- Enterprise Templates, XML and
- discovery files, XML
- server controls, XML and
- Web server controls, XML
- XSL
- XML [Visual Studio], data sources
- XML schemas
- XML [Visual Studio], SGML relationship to
- CSS, style sheets for XML
- XML [Visual Studio], .NET Framework classes
- data [Visual Studio], XML
- classes [Visual Studio], XML
- style sheets, for XML
- Web services
- SGML, XML
- XML [Visual Studio]
- datasets [Visual Basic], XML Schemas
- XSD schemas
- XSL, style sheets
- XMLDataDocument class
ms.assetid: 1fd5de47-2d61-4180-9539-c2c4bf9ab768
caps.latest.revision: "21"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 3786e74f9913400e7a95d962c8512d2263d6ae39
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="xml-tools-in-visual-studio"></a>Narzędzia XML w Visual Studio
*Extensible Markup Language (XML)* to język zapewniający format opisu danych. To ułatwia dokładniejsze deklarowanie zawartości i uzyskiwanie bardziej znaczących wyników na wielu platformach. Ponadto XML umożliwia rozdzielenie prezentacji danych. Na przykład w języku HTML umożliwia tagi przeglądarka, aby wyświetlić dane jako pogrubieniem lub kursywą; w kodzie XML używaj tagów wyłącznie w celu określenia dane, takie jak nazwę miejscowości, temperatury i barometryczne wykorzystania. W kodzie XML umożliwia arkusze stylów, takich jak arkusza stylów języka XSL (Extensible) i kaskadowych arkuszy stylów (CSS) przedstawiają dane w przeglądarce. XML oddziela dane od prezentacji i procesu. Dzięki temu można wyświetlić i przetwarzania danych, które mają być, stosując arkusze stylów różnych i aplikacji.  
  
 Kod XML jest podzbiorem SGML jest zoptymalizowany pod kątem dostarczania w sieci Web. Jest on zdefiniowany w sieci World Wide Web konsorcjum W3C. Tej normalizacji gwarantuje, że dane strukturalne będzie uniform i niezależnie od aplikacji lub dostawców.  
  
 Kod XML jest fundament wiele funkcji [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] i [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)]. Na poniższej liście tematu nazwy narzędzia i funkcje związane z XML, które są oferowane w [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] i [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)].  
  
 Aby uzyskać więcej informacji, zobacz [Centrum deweloperów języka XML](http://go.microsoft.com/fwlink/?LinkID=100176), który zawiera najnowszą dokumentację, informacje techniczne, pliki do pobrania, grupy dyskusyjne i inne zasoby dla deweloperów XML.  
  
## <a name="in-this-section"></a>W tej sekcji  
 [Praca z danych XML](../xml-tools/working-with-xml-data.md)  
 W tym artykule omówiono rolę XML w sposobie obsługi danych w [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].  
  
 [Profilowanie XSLT](../xml-tools/debugging-xslt.md)  
 Zawiera łącza do innych tematów dotyczących za pomocą debugera programu Visual Studio do debugowania XSLT.  
  
## <a name="reference"></a>Tematy pomocy  
 [Microsoft.VisualStudio.XmlEditor](http://go.microsoft.com/fwlink/?LinkID=165699)  
 Przedstawia [edytora XML](http://go.microsoft.com/fwlink/?LinkId=228249) drzewo za pomocą analizy [System.Xml.Linq](http://go.microsoft.com/fwlink/?LinkId=228250) dla wszystkich dokumentów XML.  
  
 [Odwołanie XML standardów](http://msdn.microsoft.com/en-us/79c78508-c9d0-423a-a00f-672e855de401)  
 Informacje na temat technologii XML, w tym XML, definicja typu dokumentu (DTD) języka definicji schematu XML (XSD) i XSLT.  
  
 <xref:System.Xml?displayProperty=fullName>  
 Zawiera opis klas i inne elementy wchodzące w skład <xref:System.Xml> przestrzeni nazw i łącza do bardziej szczegółowych informacji na temat każdego elementu.  
  
 <xref:System.Xml.Serialization?displayProperty=fullName>  
 Zawiera opis klas i inne elementy wchodzące w skład <xref:System.Xml.Serialization> przestrzeni nazw i linki do bardziej szczegółowych informacji o każdym elemencie.  
  
## <a name="related-sections"></a>Sekcje pokrewne  
 [Modelu obiektu dokumentu XML modelu DOM)](/dotnet/standard/data/xml/xml-document-object-model-dom)  
 Opisuje sposób <xref:System.Xml.XmlDocument> i W3C Document Object Model (podstawowe), poziom 1 i poziom 2 przestrzeń nazw pomocy technicznej specyfikacji wykonania jego skojarzonych klas.  
  
 [Odczyt XML z element XmlReader](http://msdn.microsoft.com/en-us/3029834c-a27e-4331-b7aa-711924062182)  
 Opisuje sposób <xref:System.Xml.XmlReader> udostępnia niebuforowany, do przodu tylko, tylko do odczytu do danych XML w strumieniu XML.  
  
 [Zapisywanie XML z Element XmlWriter](http://msdn.microsoft.com/en-us/ea41f72c-e1d3-4e0a-ab0f-f0eb1c27ab86)  
 Opisuje sposób <xref:System.Xml.XmlWriter> zapewnia niebuforowany, przekazywania, sposób generowania strumieni XML i ułatwia tworzenie dokumentów XML, które są zgodne ze standardem W3C.  
  
 [Przekształcenia XSLT](/dotnet/standard/data/xml/xslt-transformations)  
 Opisuje sposób <xref:System.Xml.Xsl.XslCompiledTransform> klasa implementuje zalecenie XSLT 1.0.  
  
 [Przetwarzania danych XML przy użyciu modelu danych XPath](/dotnet/standard/data/xml/process-xml-data-using-the-xpath-data-model)  
 Opisuje sposób <xref:System.Xml.XPath.XPathNavigator> klasy może przetwarzać dane XML przechowywane w <xref:System.Xml.XPath.XPathDocument> lub <xref:System.Xml.XmlDocument> obiektu. <xref:System.Xml.XPath.XPathNavigator> Klasy jest oparta na XQuery 1.0 i XPath 2.0 Model danych i może służyć do nawigowania i edytowanie danych XML.  
  
 [Model obiektu schematu XML (SOM)](/dotnet/standard/data/xml/xml-schema-object-model-som)  
 W tym artykule opisano klasy używane do tworzenia i manipulowania schematów XML, zapewniając <xref:System.Xml.Schema.XmlSchema> klasy obciążenia i Edytuj schematu.