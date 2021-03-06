---
title: 'Porady: programowane Zmienianie formatowania w wierszach arkusza zawierających zaznaczone komórki'
ms.custom: ''
ms.date: 02/02/2017
ms.technology:
- office-development
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- rows [Office development in Visual Studio]
- formatting [Office development in Visual Studio]
- worksheets, changing formatting
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: a74f610d596a991512f7f3ba5061da6db862f0c3
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49891287"
---
# <a name="how-to-programmatically-change-formatting-in-worksheet-rows-containing-selected-cells"></a>Porady: programowane Zmienianie formatowania w wierszach arkusza zawierających zaznaczone komórki
  Możesz zmienić czcionkę cały wiersz, który zawiera zaznaczonej komórki, dlatego, że tekst jest pogrubiony.  
  
 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]  
  
## <a name="to-make-the-current-row-bold-and-the-previously-bolded-row-normal"></a>Aby pogrubić bieżący wiersz i wcześniej pogrubiony wiersz normalnego  
  
1. Zadeklaruj zmienną statyczną, aby śledzić wcześniej wybrany wiersz.  
  
    [!code-csharp[Trin_VstcoreExcelAutomation#37](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#37)]
    [!code-vb[Trin_VstcoreExcelAutomation#37](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#37)]  
  
2. Pobierz odwołanie do bieżącej komórki za pomocą <xref:Microsoft.Office.Interop.Excel._Application.ActiveCell%2A> właściwości.  
  
    [!code-csharp[Trin_VstcoreExcelAutomation#38](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#38)]
    [!code-vb[Trin_VstcoreExcelAutomation#38](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#38)]  
  
3. Styl do bieżącego wiersza bold przy użyciu <xref:Microsoft.Office.Interop.Excel.Range.EntireRow%2A> właściwość aktywną komórką.  
  
    [!code-csharp[Trin_VstcoreExcelAutomation#39](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#39)]
    [!code-vb[Trin_VstcoreExcelAutomation#39](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#39)]  
  
4. Upewnij się, że bieżąca wartość `previousRow` jest różna od 0. 0 (zero) oznacza, że jest po raz pierwszy przy użyciu tego kodu.  
  
    [!code-csharp[Trin_VstcoreExcelAutomation#40](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#40)]
    [!code-vb[Trin_VstcoreExcelAutomation#40](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#40)]  
  
5. Upewnij się, że bieżący wiersz różni się od poprzedniego wiersza.  
  
    [!code-csharp[Trin_VstcoreExcelAutomation#41](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#41)]
    [!code-vb[Trin_VstcoreExcelAutomation#41](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#41)]  
  
6. Pobieranie, a odwołanie do zakresu, który reprezentuje wiersz, który wcześniej został wybrany, a zestaw wierszy nie są pogrubione.  
  
    [!code-csharp[Trin_VstcoreExcelAutomation#42](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#42)]
    [!code-vb[Trin_VstcoreExcelAutomation#42](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#42)]  
  
7. Store bieżący wiersz, dzięki czemu może stać się poprzedniego wiersza w następnym przejściu.  
  
    [!code-csharp[Trin_VstcoreExcelAutomation#43](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#43)]
    [!code-vb[Trin_VstcoreExcelAutomation#43](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#43)]  
  
   Poniższy przykład pokazuje całą metodę.  
  
## <a name="example"></a>Przykład  
 [!code-csharp[Trin_VstcoreExcelAutomation#36](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#36)]
 [!code-vb[Trin_VstcoreExcelAutomation#36](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#36)]  
  
## <a name="see-also"></a>Zobacz także  
 [Praca z arkuszami](../vsto/working-with-worksheets.md)   
 [Porady: programowane stosowanie stylów do zakresów arkusza w skoroszycie](../vsto/how-to-programmatically-apply-styles-to-ranges-in-workbooks.md)   
 [Porady: programowane kopiowanie danych i formatowanie między arkuszami](../vsto/how-to-programmatically-copy-data-and-formatting-across-worksheets.md)   
 [Parametry opcjonalne w rozwiązaniach pakietu Office](../vsto/optional-parameters-in-office-solutions.md)  
  
  