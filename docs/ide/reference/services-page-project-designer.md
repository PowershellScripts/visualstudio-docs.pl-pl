---
title: "Strona usług, Projektant projektu | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vb.ProjectPropertiesServices
helpviewer_keywords:
- Services page in Project Designer
- Project Designer, Services page
ms.assetid: 6dd9e0fa-acba-4d7d-b081-705b0fc86ff5
caps.latest.revision: "26"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 0800884a03544aec822d31cf64fd47a4f63f3e07
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="services-page-project-designer"></a>Strona usług, Projektant projektu
Usługi aplikacji klienta udostępnienia uproszczony [!INCLUDE[ajax_current_short](../../ide/reference/includes/ajax_current_short_md.md)] logowania, ról i usług profilu w aplikacjach formularzy systemu Windows i Windows Presentation Foundation (WPF). Można użyć **usług** strony **projektanta projektu** Włączanie i konfigurowanie usługi aplikacji klienta dla projektu.  
  
 Z usługi aplikacji klienta można użyć scentralizowanego serwera do uwierzytelniania użytkowników, określić przypisanej roli każdego użytkownika lub ról i zapisać ustawienia aplikacji dla poszczególnych użytkowników, które można udostępnić w sieci. Aby uzyskać więcej informacji, zobacz [usługi aplikacji klienta](/dotnet/framework/common-client-technologies/client-application-services).  
  
 Aby uzyskać dostęp do **usług** wybierz węzeł projektu w **Eksploratora rozwiązań**, a następnie kliknij przycisk **właściwości** na **projektu** menu. Gdy **projektanta projektu** pojawia się, kliknij przycisk **usług** kartę.  
  
> [!NOTE]
>  Usługi aplikacji klienta wymaga pełnej wersji programu .NET Framework i nie są obsługiwane w programie .NET Framework Client Profile. Jeśli **włączyć usługi aplikacji klienckiej** pole wyboru jest wyłączone, upewnij się, że **platformy docelowej** jest ustawiony do programu .NET Framework 3.5 lub nowszej. Aby wyświetlić **platformy docelowej** ustawienie w języku C#, Otwórz w Projektancie projektu, a następnie kliknij przycisk **aplikacji** strony. Aby wyświetlić **platformy docelowej** ustawienie w języku Visual Basic, Otwórz w Projektancie projektu, kliknij przycisk **skompilować** , a następnie kliknij przycisk **zaawansowane opcje kompilacji**.  
  
## <a name="task-list"></a>Lista zadań  
 [Porady: Konfigurowanie usług aplikacji klienta](/dotnet/framework/common-client-technologies/how-to-configure-client-application-services)  
  
## <a name="uielement-list"></a>Lista elementów UI  
 **Konfiguracja**  
 Ten formant nie jest możliwa na tej stronie. Opis tego formantu, zobacz [strona kompilowania, Projektant projektu (Visual Basic)](../../ide/reference/compile-page-project-designer-visual-basic.md) lub [strona kompilacji, Projektant projektu (C#)](../../ide/reference/build-page-project-designer-csharp.md).  
  
 **Platformy**  
 Ten formant nie jest możliwa na tej stronie. Opis tego formantu, zobacz [strona kompilowania, Projektant projektu (Visual Basic)](../../ide/reference/compile-page-project-designer-visual-basic.md) lub [strona kompilacji, Projektant projektu (C#)](../../ide/reference/build-page-project-designer-csharp.md).  
  
 **Włącz usługi aplikacji klienta**  
 Zaznacz, aby włączyć usługi aplikacji klienta. Należy określić lokalizacji usług na **usług** stronę, aby korzystać z usługi aplikacji klienta.  
  
 **Uwierzytelnianie systemu Windows**  
 Wskazuje, że dostawca uwierzytelniania będzie używać uwierzytelniania systemu Windows, czyli tożsamość dostarczane przez system operacyjny Windows.  
  
 **Uwierzytelnianie formularzy**  
 Wskazuje, że dostawca uwierzytelniania korzystają z uwierzytelniania formularzy. Oznacza to, aplikacja musi udostępniają interfejs użytkownika dla nazwy logowania. Aby uzyskać więcej informacji, zobacz [porady: Implementowanie logowania użytkownika z usługi aplikacji klienta](/dotnet/framework/common-client-technologies/how-to-implement-user-login-with-client-application-services).  
  
 **Lokalizacja usługi uwierzytelniania**  
 Używana tylko z uwierzytelniania formularzy. Określa lokalizację usługi uwierzytelniania.  
  
 **Opcjonalnie: Dostawca poświadczeń**  
 Używana tylko z uwierzytelniania formularzy. Wskazuje <xref:System.Web.ClientServices.Providers.IClientFormsAuthenticationCredentialsProvider> implementacji, którego będzie używać usługa uwierzytelniania, aby wyświetlić okno dialogowe logowania, gdy wywołuje aplikację `static` <xref:System.Web.Security.Membership.ValidateUser%2A?displayProperty=fullName> — metoda i przekazuje pustych ciągów ani `null` parametrów. Jeśli to pole pozostanie puste, należy podać prawidłową nazwę użytkownika i hasło, aby <xref:System.Web.Security.Membership.ValidateUser%2A?displayProperty=fullName> metody. Należy określić jako nazwa typu kwalifikowana zestawu dostawcy poświadczeń. Aby uzyskać więcej informacji, zobacz <xref:System.Type.AssemblyQualifiedName%2A?displayProperty=fullName> i [nazwy zestawu](/dotnet/framework/app-domains/assembly-names). W najprostszej postaci nazwa kwalifikowana zestawu typu wygląda podobnie do poniższego przykładu:`MyNamespace.MyLoginClass, MyAssembly`  
  
 **Lokalizacja usługi ról**  
 Określa lokalizację usługi ról.  
  
 **Lokalizacja usługi ustawień sieci Web**  
 Określa lokalizację usługi profilu (ustawień sieci Web).  
  
 **Zaawansowane**  
 Otwiera [Zaawansowane ustawienia dla usług — okno dialogowe](../../ide/reference/advanced-settings-for-services-dialog-box.md), która umożliwia zastąpienie zachowania domyślnego. Na przykład można użyć tego okna dialogowego bazy danych dla magazynu offline zamiast lokalnego systemu plików. Aby uzyskać więcej informacji, zobacz [Zaawansowane ustawienia dla usług — okno dialogowe](../../ide/reference/advanced-settings-for-services-dialog-box.md).  
  
## <a name="see-also"></a>Zobacz też  
 [Usługi aplikacji klienta](/dotnet/framework/common-client-technologies/client-application-services)   
 [Zaawansowane ustawienia dla usług — okno dialogowe](../../ide/reference/advanced-settings-for-services-dialog-box.md)   
 [Porady: Konfigurowanie usług aplikacji klienta](/dotnet/framework/common-client-technologies/how-to-configure-client-application-services)   
 [Strona kompilowania, Projektant projektu (Visual Basic)](../../ide/reference/compile-page-project-designer-visual-basic.md)   
 [Strona kompilacji, Projektant projektu (C#)](../../ide/reference/build-page-project-designer-csharp.md)   