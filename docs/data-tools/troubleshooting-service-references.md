---
title: "Rozwiązywanie problemów z odwołaniami usługi | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- msvse_wcf.Err.ReferenceGroup_NamespaceConflictsOther
- msvse_wcf.Err.AddSvcRefDlg_NothingSelectedOnGo
- msvse_wcf.Err.ErrorOnOK
- msvse_wcf.cfg.ConfigurationErrorsException
helpviewer_keywords:
- service references [Visual Studio], troubleshooting
- WCF services, troubleshooting
ms.assetid: 3b531120-1325-4734-90c6-6e6113bd12ac
caps.latest.revision: "22"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.technology: vs-data-tools
ms.openlocfilehash: e46c8bf778ff18ea25096e524716bcb44916f460
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="troubleshooting-service-references"></a>Rozwiązywanie problemów z odwołaniami usługi
Ten temat zawiera listę typowych problemów, które mogą wystąpić podczas pracy z [!INCLUDE[vsindigo](../data-tools/includes/vsindigo_md.md)] lub [!INCLUDE[ssAstoria](../data-tools/includes/ssastoria_md.md)] odwołania w [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].  
  
## <a name="error-returning-data-from-a-service"></a>Błąd zwracać dane z usługi  
 Po powrocie `DataSet` lub `DataTable` z usługą, może zostać wyświetlony wyjątek "został przekroczony maksymalny rozmiar limit przydziału dla komunikatów przychodzących". Domyślnie `MaxReceivedMessageSize` właściwość dla niektórych powiązań ma ustawioną wartość stosunkowo mały ograniczenia narażenia na ataki typu "odmowa usługi". Można zwiększyć tę wartość, aby zapobiec wyjątek. Aby uzyskać więcej informacji, zobacz <xref:System.ServiceModel.HttpBindingBase.MaxReceivedMessageSize%2A>.  
  
 Aby naprawić ten błąd:  
  
1.  W **Eksploratora rozwiązań**, kliknij dwukrotnie plik app.config, aby go otworzyć.  
  
2.  Zlokalizuj `MaxReceivedMessageSize` właściwości i zmień ją na większej wartości.  
  
## <a name="cannot-find-a-service-in-my-solution"></a>Nie można odnaleźć usługi w Moje rozwiązanie  
 Po kliknięciu **odnajdowania** przycisk **dodać odwołania do usług** okno dialogowe, co najmniej jeden projekt biblioteki usługi WCF w rozwiązaniu nie są wyświetlane na liście usług. Może to wystąpić, jeśli biblioteka usługi został dodany do rozwiązania, ale jeszcze nie został skompilowany.  
  
 Aby naprawić ten błąd:  
  
-   W **Eksploratora rozwiązań**, kliknij prawym przyciskiem myszy projekt biblioteki usługi WCF i kliknij przycisk **kompilacji**.  
  
## <a name="error-accessing-a-service-over-a-remote-desktop"></a>Błąd podczas uzyskiwania dostępu do usługi za pośrednictwem pulpitu zdalnego  
 Gdy użytkownik uzyskuje dostęp do usługi WCF hostowanych w sieci Web za pośrednictwem połączenia pulpitu zdalnego i użytkownik nie ma uprawnienia administratora, używane jest uwierzytelnianie NTLM. Jeśli użytkownik nie ma uprawnień administracyjnych, użytkownik może zostać wyświetlony następujący komunikat o błędzie: "żądanie HTTP jest autoryzowane na podstawie schematu uwierzytelniania klienta"Anonymous". Nagłówek uwierzytelnienia otrzymany z serwera to "NTLM"."  
  
 Aby naprawić ten błąd:  
  
1.  Projekt witryny sieci Web otwórz **właściwości** stron.  
  
2.  Na **opcje uruchamiania** kartę, wyczyść **uwierzytelniania NTLM** pole wyboru.  
  
    > [!NOTE]
    >  Należy wyłączyć uwierzytelnianie NTLM tylko dla witryn sieci Web, zawierające wyłącznie usługi WCF. Zabezpieczenia usług WCF jest zarządzana za pomocą konfiguracji w pliku web.config. Dzięki temu można niepotrzebnych uwierzytelniania NTLM.  
  
## <a name="access-level-for-generated-classes-setting-has-no-effect"></a>Poziom dostępu dla klas wygenerowane ustawienie nie ma wpływu  
 Ustawienie **dostępu poziom wygenerowane klasy** opcji **skonfigurować odwołania do usług** okno dialogowe, aby **wewnętrzne** lub **Friend** może nie zawsze działać. Nawet jeśli jest dostępna w oknie dialogowym, zostanie wygenerowany wynikowa klasy obsługi z poziomu dostępu `Public`.  
  
 Jest to znane ograniczenie określonych typów, takich jak zserializowanym przy użyciu <xref:System.Xml.Serialization.XmlSerializer>.  
  
## <a name="error-debugging-service-code"></a>Błąd podczas debugowania kodu usługi  
 Gdy krok do kodu dla usługi WCF z kodu klienta może zostać wyświetlony komunikat o błędzie dotyczący Brak symbole. Taka sytuacja może wystąpić, gdy usługa, która jest częścią rozwiązania został przeniesiony lub usunięty z rozwiązania.  
  
 Podczas dodawania odwołania do usługi WCF, która jest częścią bieżącego rozwiązania zależność kompilacji jawne dodawany jest odstęp projektu usługi i projektu usługi klienta. Gwarantuje to, że klient zawsze uzyskuje dostęp do plików binarnych usługi aktualne, która jest szczególnie ważne w przypadku scenariuszy, takich jak wykonywanie krok po kroku z kodu klienta usługi kodu do debugowania.  
  
 Jeśli projekt usługi zostanie usunięty z rozwiązania, ta zależność kompilacji jawne zostało unieważnione. Visual Studio mogą już zagwarantować, że odbudowaniu projektu usługi niezbędne.  
  
 Aby naprawić ten błąd, należy ręcznie ponownie skompilować projekt usługi:  
  
1.  Na **narzędzia** menu, kliknij przycisk **opcje**.  
  
2.  W **opcje** okna dialogowego rozwiń **projekty i rozwiązania**, a następnie wybierz **ogólne**.  
  
3.  Upewnij się, że **Pokaż zaawansowane konfiguracje kompilacji** pole wyboru jest zaznaczone, a następnie kliknij przycisk **OK**.  
  
4.  Załaduj projekt usługi WCF.  
  
5.  W **programu Configuration Manager** okno dialogowe, zestaw **aktywnej konfiguracji rozwiązania** do **debugowania**. Aby uzyskać więcej informacji, zobacz [porady: tworzenie i edycja konfiguracji](../ide/how-to-create-and-edit-configurations.md).  
  
6.  W **Eksploratora rozwiązań**, wybierz projekt usługi WCF.  
  
7.  Na **kompilacji** menu, kliknij przycisk **odbudować** odbudować projektu usługi WCF.  
  
## <a name="wcf-data-services-do-not-display-in-the-browser"></a>Usługi danych WCF nie są wyświetlane w przeglądarce  
 Gdy próbuje wyświetlić reprezentację XML z danymi w [!INCLUDE[ss_data_service](../data-tools/includes/ss_data_service_md.md)], Internet Explorer mogą niewłaściwą interpretację danych jako źródła danych RSS. Należy się upewnić, że opcja wyświetlania źródeł danych RSS jest wyłączona.  
  
 Aby naprawić ten błąd, należy wyłączyć źródeł danych RSS:  
  
1.  W programie Internet Explorer na **narzędzia** menu, kliknij przycisk **Opcje internetowe**.  
  
2.  Na **zawartości** karcie **źródła** kliknij **ustawienia**.  
  
3.  W **ustawienia źródła danych** okno dialogowe, usuń zaznaczenie **włączyć odczytywania widoku źródła danych** pole wyboru, a następnie kliknij przycisk **OK**.  
  
4.  Kliknij przycisk **OK** zamknąć **Opcje internetowe** okno dialogowe.  
  
## <a name="see-also"></a>Zobacz też  
 [Usługi Windows Communication Foundation oraz usługi danych WCF w programie Visual Studio](../data-tools/windows-communication-foundation-services-and-wcf-data-services-in-visual-studio.md)