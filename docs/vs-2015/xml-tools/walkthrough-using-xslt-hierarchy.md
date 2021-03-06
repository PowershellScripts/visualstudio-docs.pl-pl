---
title: 'Wskazówki: Korzystanie z hierarchii XSLT | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 5e60c8ec-cd05-4597-b856-55038218acf4
caps.latest.revision: 8
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 5b94a958a915ad7858575e093cae525df17cc23e
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49280965"
---
# <a name="walkthrough-using-xslt-hierarchy"></a>Przewodnik: używanie hierarchii XSLT
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Narzędzie hierarchii XSLT upraszcza wiele zadań programistycznych XML. Arkusz stylów XSLT często używa `includes` i `imports` instrukcje. Kompilacja zaczyna się od arkusza stylów jednostki, ale gdy zostanie wyświetlony błąd w wyniku kompilacji arkusz stylów XSLT błędu mogą pochodzić z innego źródła niż arkusza stylów podmiotu zabezpieczeń. Naprawianie błędu lub edytowania arkusza stylów mogą wymagać dostępu do arkuszy stylów dołączanego lub importowanego. Krokowego wykonywania arkusza stylów w debugerze mogą otwierać arkusze stylów dołączone i importowanie i chcesz dodać punkt przerwania w pewnym momencie w co najmniej jednej arkusze stylów dołączone.  
  
 Inny scenariusz, w którym narzędzie hierarchii XSLT może być przydatne jest umieszczenie punktów przerwania w regułach wbudowany szablon. Szablon reguły są specjalne szablony generowane dla każdego trybu arkusza stylów i wywoływane przez `xsl:apply-templates` gdy szablon nie pasuje do węzła. Aby zaimplementować profilowanie wbudowanych szablonów reguł, debuger XSLT generuje plik z zasadami w folderze tymczasowym i kompiluje je wraz z arkusza stylów podmiotu zabezpieczeń. Bez Przechodzenie do kodu z niektórych `xsl:apply-template`, może być trudno znaleźć arkuszy stylów, które zostały uwzględnione w arkuszu stylów podmiotu zabezpieczeń lub znaleźć i otworzyć arkusz stylów za pomocą wbudowanego szablonu reguły.  
  
 W przykładzie w tym temacie pokazano, debugowanie w arkuszu stylów odwołania.  
  
### <a name="procedure-title"></a>Tytuł procedury  
  
1.  Otwórz dokument XML w programie Visual Studio. W tym przykładzie użyto następujących `collection.xml` dokumentu.  
  
    ```  
    <?xml version="1.0" encoding="utf-8"?>  
    <?xml-stylesheet type="text/xsl" href="xslinclude.xsl"?>  
    <COLLECTION>  
      <BOOK>  
        <TITLE>Lover Birds</TITLE>  
        <AUTHOR>Cynthia Randall</AUTHOR>  
        <PUBLISHER>Lucerne Publishing</PUBLISHER>  
      </BOOK>  
      <BOOK>  
        <TITLE>The Sundered Grail</TITLE>  
        <AUTHOR>Eva Corets</AUTHOR>  
        <PUBLISHER>Lucerne Publishing</PUBLISHER>  
      </BOOK>  
      <BOOK>  
        <TITLE>Splish Splash</TITLE>  
        <AUTHOR>Paula Thurman</AUTHOR>  
        <PUBLISHER>Scootney</PUBLISHER>  
      </BOOK>  
    </COLLECTION>  
    ```  
  
2.  Dodaj następujący kod `xslincludefile.xsl`:  
  
    ```  
    <?xml version='1.0'?>  
    <xsl:stylesheet version="1.0"  
          xmlns:xsl="http://www.w3.org/1999/XSL/Transform"  
          xml:space="preserve">  
  
    <xsl:template match="TITLE">  
       Title - <xsl:value-of select="."/><BR/>  
    </xsl:template>  
  
    <xsl:template match="AUTHOR">  
       Author - <xsl:value-of select="."/><BR/>  
    </xsl:template>  
  
    <xsl:template match="PUBLISHER">  
       Publisher - <xsl:value-of select="."/><BR/><!-- removed second <BR/> -->  
    </xsl:template>  
  
    </xsl:stylesheet>  
    ```  
  
3.  Dodaj następujący kod `xslinclude.xsl` pliku:  
  
    ```  
    <?xml version='1.0'?>  
    <xsl:stylesheet version="1.0"  
          xmlns:xsl="http://www.w3.org/1999/XSL/Transform">  
  
      <xsl:output method="xml" omit-xml-declaration="yes"/>  
  
      <xsl:template match="/">  
        <xsl:for-each select="COLLECTION/BOOK">  
          <xsl:apply-templates select="TITLE"/>  
          <xsl:apply-templates select="AUTHOR"/>  
          <xsl:apply-templates select="PUBLISHER"/>  
          <BR/>  
          <!-- add this -->  
        </xsl:for-each>  
      </xsl:template>  
  
      <!-- The following template rule will not be called,  
      because the related template in the including stylesheet  
      is called. If we move this template so that  
      it follows the xsl:include instruction, this one  
      will be called instead.-->  
      <xsl:template match="TITLE">  
        <DIV STYLE="color:blue">  
          Title: <xsl:value-of select="."/>  
        </DIV>  
      </xsl:template>  
  
      <xsl:include href="xslincludefile.xsl" />  
    </xsl:stylesheet>  
    ```  
  
4.  Dodaj punkt przerwania w instrukcji: `<xsl:include href="xslincludefile.xsl" />`  
  
5.  Rozpocznij debugowanie.  
  
6.  Gdy debuger zatrzymuje się w instrukcji `<xsl:include href="xslincludefile.xsl" />`, naciśnij klawisz Wkrocz do przycisku. Należy pamiętać, że debugowanie może być kontynuowane w arkuszu stylów odwołania. Hierarchia jest widoczna i Projektant wyświetla prawidłową ścieżkę.  
  
## <a name="see-also"></a>Zobacz też  
 [Przewodnik: Profiler XSLT](../xml-tools/walkthrough-xslt-profiler.md)



