---
title: Wyświetlanie zmiennych lokalnych | Dokumentacja firmy Microsoft
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- debugging [Debugging SDK], expression evaluation
- expression evaluation, displaying locals
ms.assetid: 62264cec-845b-4233-aed7-0b038fa79250
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: cbfff37c9a840da43219f3c3aab5a0dce4501218
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/12/2018
ms.locfileid: "49201334"
---
# <a name="displaying-locals"></a>Wyświetlanie zmiennych lokalnych
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

> [!IMPORTANT]
>  W programie Visual Studio 2015 ten sposób implementowania ewaluatory wyrażeń jest przestarzały. Informacji dotyczących implementowania ewaluatory wyrażeń CLR, zobacz [Ewaluatory wyrażeń CLR](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) i [zarządzane przykładowe ewaluatora wyrażeń](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Wykonanie zawsze odbywa się w kontekście metody, nazywana również metodą zawierającą lub bieżącej metody. Podczas wykonywania jest wstrzymana, Visual Studio wywołuje aparat debugowania (DE), aby uzyskać listę zmiennych lokalnych i argumenty, nazywane zmienne lokalne, metody. Visual Studio wyświetla te zmienne lokalne i ich wartości w **lokalne** okna.  
  
 Aby wyświetlić elementy lokalne, wywołuje DE [metody GetMethodProperty](../../extensibility/debugger/reference/idebugexpressionevaluator-getmethodproperty.md) metoda należąca do EE i nadaje jej kontekst oceny, który jest, dostawca symboli (SP), bieżący adres wykonywania i obiekt integratora. Aby uzyskać więcej informacji, zobacz [kontekst oceny](../../extensibility/debugger/evaluation-context.md). Jeśli wywołanie zakończy się powodzeniem, `IDebugExpressionEvaluator::GetMethodProperty` metoda zwraca [IDebugProperty2](../../extensibility/debugger/reference/idebugproperty2.md) obiektu, który reprezentuje metodę, która zawiera bieżący adres wykonywania.  
  
 Wywołania DE [EnumChildren](../../extensibility/debugger/reference/idebugproperty2-enumchildren.md) można pobrać [IEnumDebugPropertyInfo2](../../extensibility/debugger/reference/ienumdebugpropertyinfo2.md) obiektu, który jest filtrowana, aby zwrócić tylko elementy lokalne i wyliczenia w celu wygenerowania listy [DEBUG_PROPERTY_INFO](../../extensibility/debugger/reference/debug-property-info.md)struktury. Każda struktura zawiera nazwę, typ i wartość zmiennej lokalnej. Typ i wartość są przechowywane jako odpowiednią do wyświetlania sformatowanych ciągów. Nazwa, typ i wartość są zwykle wyświetlane razem w jednym wierszu **lokalne** okna.  
  
> [!NOTE]
>  **QuickWatch** i **Obejrzyj** również wyświetlania zmiennych o tym samym formacie nazwy, wartości i typ systemu windows. Jednak te wartości są uzyskiwane przez wywołanie metody [getpropertyinfo —](../../extensibility/debugger/reference/idebugproperty2-getpropertyinfo.md) zamiast `IDebugProperty2::EnumChildren`.  
  
## <a name="in-this-section"></a>W tej sekcji  
 [Przykłady implementacji zmiennych lokalnych](../../extensibility/debugger/sample-implementation-of-locals.md)  
 Używa przykładów, aby przejść przez proces implementowania zmiennych lokalnych.  
  
## <a name="related-sections"></a>Sekcje pokrewne  
 [Kontekst oceny](../../extensibility/debugger/evaluation-context.md)  
 W tym artykule wyjaśniono, że gdy aparat debugowania (DE) wywołuje Ewaluator wyrażeń (EE), przekazuje on trzy argumenty.  
  
## <a name="see-also"></a>Zobacz też  
 [Pisanie ewaluatora wyrażeń środowiska CLR](../../extensibility/debugger/writing-a-common-language-runtime-expression-evaluator.md)

