---
title: 'Przykładowe rozszerzenie programu Excel: Klasa PropertyProvider | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 075d9b8d-8658-4fca-8711-08304dbac1c5
caps.latest.revision: 11
ms.author: gewarren
manager: douge
ms.openlocfilehash: 513d54fd9779bb4148e00d0839ef75b1a4637545
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49203661"
---
# <a name="sample-excel-extension-propertyprovider-class"></a>Przykładowe rozszerzenie programu Excel: klasa PropertyProvider
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Klasa wewnętrznego rozszerza <xref:Microsoft.VisualStudio.TestTools.UITesting.UITestPropertyProvider> klasy i zapewnia właściwości dla [!INCLUDE[ofprexcel](../includes/ofprexcel-md.md)] elementy, aby nagrywać i odtwarzać testy interfejsu użytkownika.  
  
## <a name="getcontrolsupportlevel-method"></a>Metoda GetControlSupportLevel  
 <xref:Microsoft.VisualStudio.TestTools.UITesting.UITestPropertyProvider.GetControlSupportLevel%2A> Metoda zwraca liczbę, która wskazuje poziom pomocy technicznej, które może zaoferować Dostawca właściwości, dla podanego formantu. Im większa wartość zwrócona więcej właściwości dostawcy może obsługiwać formant. W tym przypadku metoda sprawdza wartość <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.IUITechnologyElement.TechnologyName%2A> właściwość podanego formantu. Jeśli wartość to "Programu Excel" i <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.IUITechnologyElement.ControlTypeName%2A> wskazuje jest `CellElement`, metoda zwraca najwyższą wartość; w przeciwnym razie zwraca wartość zero, co oznacza, że nie jest obsługiwana.  
  
## <a name="getpropertynames-method"></a>Metoda GetPropertyNames  
 Zwraca słownik nazw właściwości i deskryptorów właściwości obsługiwanych właściwości kontrolkę komórki programu Excel.  
  
## <a name="getpropertydescriptor-method"></a>Metoda GetPropertyDescriptor  
 Ta metoda jest wywoływana przez strukturę testowania można uzyskać deskryptora właściwości wstępnie zdefiniowanych podana nazwa właściwości.  
  
## <a name="getpropertyvalue-and-setpropertyvalue-methods"></a>GetPropertyValue i metod SetPropertyValue  
 `GetPropertyValue` Metoda używa `Communicator` klasy to rozszerzenie, aby zwrócić wartości właściwości z programu Excel. `SetPropertyValue` Metoda używa <xref:Microsoft.VisualStudio.TestTools.UITesting.Keyboard> klasy i `Communicator` składnik, aby ustawić wartości właściwości. Te metody są wywoływane przez platformę testowania.  
  
## <a name="code-generation-customization-methods"></a>Metody dostosowywania generowania kodu  
 Te metody nie są zaimplementowane dla tego rozszerzenia. W związku z tym, albo zwracają `null` lub zgłosić <xref:System.NotImplementedException>.  
  
## <a name="see-also"></a>Zobacz też  
 <xref:Microsoft.VisualStudio.TestTools.UITesting.UITestPropertyProvider>   
 <xref:Microsoft.VisualStudio.TestTools.UITesting.Keyboard>   
 [Rozszerzanie kodowanych testów interfejsu użytkownika i rejestrowanie akcji obsługujących program Microsoft Excel](../test/extending-coded-ui-tests-and-action-recordings-to-support-microsoft-excel.md)



