---
title: 'Błąd: proces roboczy witryny sieci Web został zakończony przez usługi IIS | Dokumentacja firmy Microsoft'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.web_server_process_terminated
dev_langs:
- CSharp
- VB
- FSharp
- C++
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 582cf1b5faf0cc62d85e17544aa03c4ede4ab0a8
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/23/2018
ms.locfileid: "49852846"
---
# <a name="error-web-site-worker-process-has-been-terminated-by-iis"></a>Błąd: proces roboczy witryny sieci Web został zakończony przez usługę IIS
Debuger zatrzymana wykonywanie kodu na witrynie sieci Web. Spowodowało to Internet Information Services (IIS) aby założył, że proces roboczy przestał odpowiadać. W związku z tym usługi IIS zakończone procesu roboczego.  
  
 Aby kontynuować debugowanie, należy skonfigurować serwer IIS zezwala na proces roboczy kontynuować. Nie ma tego komunikatu o błędzie z wersjami usług IIS, które są starsze niż IIS 7.  
  
### <a name="to-configure-iis-7-to-allow-the-worker-process-to-continue"></a>Aby skonfigurować usługi IIS 7, aby zezwolić na proces roboczy kontynuować  
  
1. Otwórz **narzędzia administracyjne** okna.  
  
   1.  Kliknij przycisk **Start**, a następnie wybierz **Panelu sterowania**.  
  
   2.  W **Panelu sterowania**, wybierz **Przełącz na widok klasyczny**, jeśli to konieczne, a następnie kliknij dwukrotnie **narzędzia administracyjne**.  
  
2. W **narzędzia administracyjne** okna, kliknij dwukrotnie **Internet Information Services (IIS) Manager**.  
  
    Zostanie otwarty Menedżer usług IIS.  
  
3. W **połączeń** okienku rozwiń \<nazwa komputera > węzła, jeśli to konieczne.  
  
4. W obszarze \<nazwa komputera > węzła, kliknij przycisk **pul aplikacji**.  
  
5. W **pul aplikacji** listy, kliknij prawym przyciskiem myszy nazwę puli aplikacji działa w, a następnie kliknij **Zaawansowane ustawienia**.  
  
6. W **Zaawansowane ustawienia** dialogowym zlokalizuj **Model procesu** sekcji, a następnie wykonaj jedną z następujących czynności:  
  
   - Ustaw **pingowanie włączone** do **False**.  
  
   - Ustaw **maksymalny czas odpowiedzi polecenia Ping** wartość, która jest większa niż 90 sekund.  
  
     Ustawienie **pingowanie włączone** do **False** zatrzymuje IIS sprawdzanie, czy Proces roboczy jest nadal uruchomione i utrzymuje aktywność procesu roboczego aż do zatrzymania usługi debugowanego procesu. Ustawienie **maksymalny czas odpowiedzi polecenia Ping** na dużą wartość umożliwia usług IIS kontynuować monitorowanie procesu roboczego.  
  
7. Kliknij przycisk **OK** zamknąć **Zaawansowane ustawienia** okno dialogowe.  
  
8. Zamknij Menedżera usług IIS i **narzędzia administracyjne** okna.  
  
## <a name="see-also"></a>Zobacz też  
 [Błędy związane z debugowaniem zdalnym i rozwiązywanie problemów](../debugger/remote-debugging-errors-and-troubleshooting.md)