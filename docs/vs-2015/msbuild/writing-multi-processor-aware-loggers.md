---
title: Zapisywanie rejestratorów procesorów uwzględniających | Dokumentacja firmy Microsoft
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
- msbuild, multi-proc aware loggers
- multi-proc loggers
- loggers, multi-proc
ms.assetid: ff987d1b-1798-4803-9ef6-cc8fcc263516
caps.latest.revision: 15
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 2b05c0f1782382f437a5e1d90bf19c724a05ca6a
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49826393"
---
# <a name="writing-multi-processor-aware-loggers"></a>Zapisywanie rejestratorów uwzględniających wiele procesorów
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Zdolność [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] może korzystać z wielu procesorów skrócić czas tworzenia projektu, ale również dodaje złożoności do tworzenia rejestrowania zdarzeń. W środowisku jednoprocesorowym zdarzenia, komunikaty, ostrzeżenia i błędy przybyć rejestratora w sposób przewidywalny i sekwencyjne. Jednak w środowisku wielu procesorów zdarzeń z różnych źródeł mogą pojawić się w tym samym czasie lub poza sekwencją. Aby zapewnić w tym celu [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] udostępnia procesorów uwzględniających rejestratora i nowy model rejestrowania i umożliwia utworzenie niestandardowego "przekazywanie rejestratorów."  
  
## <a name="multi-processor-logging-challenges"></a>Rejestrowanie wielu procesorów wyzwania  
 Podczas tworzenia co najmniej jeden projekt w systemie wieloprocesorowym lub wielordzeniowych [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] zdarzenia kompilacji, dla wszystkich projektów są generowane w tym samym czasie. U rejestratora lawiny komunikaty o zdarzeniach może pojawić się w tym samym czasie lub poza sekwencją. Ponieważ [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] rejestratora 2.0 nie jest przeznaczony do obsługi takiej sytuacji, można przeciąży rejestratora i powodować czasy kompilacji zwiększona, rejestratora nieprawidłowe dane wyjściowe lub uszkodzone kompilacji. Aby rozwiązać te problemy, rejestratora (począwszy od [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] 3.5) może przetwarzać zdarzenia poza sekwencji i skorelować zdarzenia i ich źródła.  
  
 Może poprawić wydajność rejestrowania jeszcze więcej, tworząc rejestratora przekazywanie niestandardowych. Rejestrator niestandardowych przekazywania działa jako filtr, umożliwiając wybierz przed kompilacją, zdarzenia, które chcesz monitorować. Korzystając z Rejestratora przekazywanie niestandardowych zdarzeń niepożądanych nie przeciąży rejestratora, zbliżyć do siebie te dzienniki lub wolno budowania razy.  
  
## <a name="multi-processor-logging-models"></a>Modele rejestrowanie wielu procesorów  
 Zapewnienie problemy związane z procesorów wielu kompilacji [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] obsługuje dwa modele rejestrowania centralnej i rozproszonych.  
  
### <a name="central-logging-model"></a>Model centralnego rejestrowania  
 W modelu centralnego rejestrowania pojedyncze wystąpienie MSBuild.exe działa jako "węźle centralnym" i wystąpień podrzędnych ("węzłów pomocniczych") w węźle centralnym dołączanie do węźle centralnym, aby wykonywać zadania kompilacji.  
  
 ![Model rejestratora centralnego](../msbuild/media/centralnode.png "CentralNode")  
  
 Rejestratory różne typy, które dołączanie do węzła centralnej są określane jako "centralnej rejestratorów." Tylko jedno wystąpienie każdego typu rejestratora można dołączyć do centralnej węzła w tym samym czasie.  
  
 W przypadku kompilacji węzłów pomocniczych kierowanie ich zdarzeń kompilacji w węźle centralnym. W węźle centralnym kieruje ze zdarzeniami, a także tych węzłów pomocniczych do co najmniej jeden dołączony rejestratorów centralnej. Rejestratory, które następnie utworzyć plików dziennika, które są oparte na danych przychodzących.  
  
 Mimo że jest to jedyna <xref:Microsoft.Build.Framework.ILogger> jest wymagane do zaimplementowania przez rejestrator centralnej, firma Microsoft zaleca również Implementowanie <xref:Microsoft.Build.Framework.INodeLogger> tak, aby rejestratora centralnego inicjuje z liczbą węzłów, które uczestniczą w kompilacji. Następujące przeciążenia <xref:Microsoft.Build.Framework.ILogger.Initialize%2A> wywołuje metodę, gdy aparat inicjuje rejestratora.  
  
```  
public interface INodeLogger: ILogger  
{  
    public void Initialize(IEventSource eventSource, int nodeCount);  
}  
```  
  
 Wszystkie wstępnie istniejące <xref:Microsoft.Build.Framework.ILogger>— na podstawie rejestratorów może działać jako rejestratorów centralnej i można dołączyć do kompilacji. Jednak centralnej rejestratorów zapisywane bez jawnego obsługę scenariuszy rejestrowanie wielu procesorów i zdarzeń poza kolejnością może przerwanie kompilacji lub generowania danych wyjściowych bez znaczenia.  
  
### <a name="distributed-logging-model"></a>Model rejestrowania rozproszonego  
 W modelu centralnego rejestrowania zbyt dużej ilości ruchu przychodzącego komunikatu może spowodować przeciążenie węźle centralnym, na przykład, gdy wiele projektów kompilacji w tym samym czasie. Może to podkreślają zasobów systemowych i zmniejszyć wydajność kompilacji. Aby ułatwić ten problem, [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] obsługuje model rejestrowania rozproszonych.  
  
 ![Model rejestrowania rozproszonych](../msbuild/media/distnode.png "DistNode")  
  
 Model rejestrowania rozproszonych rozszerzają model centralnego rejestrowania, umożliwiając tworzenie rejestratora przekazywania.  
  
#### <a name="forwarding-loggers"></a>Przekazywanie rejestratorów  
 Rejestrator przekazywania jest rejestratora pomocniczego, lekki, zawierający filtr zdarzeń, który dołącza do węzła pomocniczego i odbiera zdarzenia przychodzące kompilacji z tego węzła. On filtruje zdarzenia przychodzące i przekazuje tylko te, które określają na węźle centralnym. Zmniejsza to ruch komunikat, który jest wysyłany do węźle centralnym i zwiększa ogólną wydajność kompilacji.  
  
 Istnieją dwa sposoby korzystania z rejestrowania rozproszonych, w następujący sposób:  
  
- Dostosowywanie rejestratora wstępnie metalowych przesyłania dalej o nazwie <xref:Microsoft.Build.BuildEngine.ConfigurableForwardingLogger>.  
  
- Napisać własne niestandardowe przekazywania rejestratora.  
  
  Można zmodyfikować ConfigurableForwardingLogger ze swoimi potrzebami. Aby to zrobić, należy wywołać rejestratora w wierszu polecenia przy użyciu MSBuild.exe, a listy zdarzeń kompilacji, które rejestratora do przekazywania na węźle centralnym.  
  
  Alternatywnie można utworzyć rejestratora przekazywanie niestandardowych. Tworząc rejestratora przekazywanie niestandardowych, można dostosować zachowanie programu rejestrującego. Jednak tworzenie rejestratora przekazywanie niestandardowych jest bardziej skomplikowane niż po prostu Dostosowywanie ConfigurableForwardingLogger. Aby uzyskać więcej informacji, zobacz [tworzenie przekazywania rejestratorów](../msbuild/creating-forwarding-loggers.md).  
  
## <a name="using-the-configurableforwardinglogger-for-simple-distributed-logging"></a>Przy użyciu ConfigurableForwardingLogger proste rozproszone rejestrowania  
 Aby dołączyć ConfigurableForwardingLogger lub rejestratora przekazywanie niestandardowych, należy użyć `/distributedlogger` przełącznika (`/dl` w skrócie) MSBuild.exe kompilacji wiersza polecenia. Format określająca nazwy klasy i typy rejestratora jest taka sama jak dla `/logger` przełącznika, z tą różnicą, że rozproszonych rejestratora zawsze ma dwie klasy rejestrowania zamiast jednym Rejestrator przekazywania i rejestratora centralnego. Oto przykładowy sposób dołączyć Rejestrator przekazywanie niestandardowej o nazwie XMLForwardingLogger.  
  
```  
msbuild.exe myproj.proj/distributedlogger:XMLCentralLogger,MyLogger,Version=1.0.2,Culture=neutral*XMLForwardingLogger,MyLogger,Version=1.0.2,Culture=neutral  
```  
  
> [!NOTE]
>  Znak gwiazdki (*) muszą być rozdzielone nazwy dwóch rejestratora w `/dl` przełącznika.  
  
 Za pomocą ConfigurableForwardingLogger przypomina przy użyciu innych rejestratora (zgodnie z opisem w [uzyskiwanie dzienników kompilacji](../msbuild/obtaining-build-logs-with-msbuild.md)), z tą różnicą, że możesz dołączyć rejestratora ConfigurableForwardingLogger zamiast typowej [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] i rejestratora Określ jako parametry zdarzeń, które chcesz ConfigurableForwardingLogger w celu przekazania ich węźle centralnym.  
  
 Na przykład, jeśli chcesz otrzymywać powiadomienia, tylko wtedy, gdy kompilacja rozpoczyna i kończy i po wystąpieniu błędu, należy wprowadzić `BUILDSTARTEDEVENT`, `BUILDFINISHEDEVENT`, i `ERROREVENT` jako parametry. Wiele parametrów mogą być przekazywane, oddzielając je średnikami. Oto przykład sposobu użycia ConfigurableForwardingLogger do przekazywania tylko `BUILDSTARTEDEVENT`, `BUILDFINISHEDEVENT`, i `ERROREVENT` zdarzenia.  
  
```  
msbuild.exe myproj.proj /distributedlogger:XMLCentralLogger,MyLogger,Version=1.0.2,Culture=neutral*ConfigureableForwardingLogger,C:\My.dll;BUILDSTARTEDEVENT; BUILDFINISHEDEVENT;ERROREVENT  
```  
  
 Oto lista dostępnych parametrów ConfigurableForwardingLogger.  
  
|Parametry ConfigurableForwardingLogger|  
|---------------------------------------------|  
|BUILDSTARTEDEVENT|  
|BUILDFINISHEDEVENT|  
|PROJECTSTARTEDEVENT|  
|PROJECTFINISHEDEVENT|  
|TARGETSTARTEDEVENT|  
|TARGETFINISHEDEVENT|  
|TASKSTARTEDEVENT|  
|TASKFINISHEDEVENT|  
|ERROREVENT|  
|WARNINGEVENT|  
|HIGHMESSAGEEVENT|  
|NORMALMESSAGEEVENT|  
|LOWMESSAGEEVENT|  
|CUSTOMEVENT|  
|WIERSZ POLECENIA|  
|PERFORMANCESUMMARY|  
|NOSUMMARY|  
|SHOWCOMMANDLINE|  
  
## <a name="see-also"></a>Zobacz też  
 [Tworzenie przekazywania rejestratorów](../msbuild/creating-forwarding-loggers.md)



