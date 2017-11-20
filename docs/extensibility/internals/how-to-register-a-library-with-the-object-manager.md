---
title: "Porady: rejestrowanie biblioteki z Menedżera obiektów | Dokumentacja firmy Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- libraries, registering with object manager
- IVsLibrary2 interface, registering library with object manager
- IVsSimpleLibrary2 interface, registering library with object manager
- IVsObjectManager2 interface, registering library with object manager
- libraries, symbol-browsing tools
ms.assetid: f124dd05-cb0f-44ad-bb2a-7c0b34ef4038
caps.latest.revision: "26"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 6782e1cb84f4fbbe63a0e69a5c684d44ec7ccd21
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/31/2017
---
# <a name="how-to-register-a-library-with-the-object-manager"></a>Porady: rejestrowanie biblioteki z Menedżera obiektów
Przeglądanie symbole narzędzi, takich jak **widoku klasy**, **przeglądarki obiektów**, **przeglądarce wywołań** i **wyniki Znajdź Symbol**, umożliwiają wyświetlanie symbole w projekcie lub składników zewnętrznych. Symbole obejmują obszary nazw, klasy, interfejsy, metody i inne elementy języka. Biblioteki śledzenie tych symboli i ujawniać je, aby [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] Menedżera obiektów, które wypełnia narzędzia z danymi.  
  
 Menedżer obiektów przechowuje informacje o wszystkich dostępnych bibliotek. Każdej biblioteki należy zarejestrować się Menedżera obiektów przed zapewnienie symbole dla narzędzia przeglądanie symbolu.  
  
 Zazwyczaj biblioteki należy zarejestrować po załadowaniu pakiet VSPackage. Jednak mogą to robić w późniejszym terminie zgodnie z potrzebami. Można wyrejestrować biblioteki podczas VSPackage zamykania.  
  
 Aby zarejestrować bibliotekę, użyj <xref:Microsoft.VisualStudio.Shell.Interop.IVsObjectManager2.RegisterLibrary%2A> metody. W przypadku biblioteki kod zarządzany, użyj <xref:Microsoft.VisualStudio.Shell.Interop.IVsObjectManager2.RegisterSimpleLibrary%2A> metody.  
  
 Aby wyrejestrować bibliotekę, użyj <xref:Microsoft.VisualStudio.Shell.Interop.IVsObjectManager2.UnregisterLibrary%2A> metody.  
  
 Aby uzyskać odwołania do Menedżera obiektów <xref:Microsoft.VisualStudio.Shell.Interop.IVsObjectManager2>, przekazać <xref:Microsoft.VisualStudio.Shell.Interop.SVsObjectManager> usługi identyfikator `GetService` — metoda.  
  
## <a name="registering-and-unregistering-a-library-with-the-object-manager"></a>Rejestrowanie i Wyrejestrowywanie biblioteki z Menedżera obiektów  
  
#### <a name="to-register-a-library-with-the-object-manager"></a>Aby zarejestrować bibliotekę z Menedżera obiektów  
  
1.  Utwórz bibliotekę.  
  
    ```vb  
    Private m_CallBrowserLibrary As CallBrowser.Library = Nothing  
    Private m_nLibraryCookie As UInteger = 0  
    ' Create Library.  
    m_CallBrowserLibrary = New CallBrowser.Library()  
    ```  
  
    ```csharp  
    private CallBrowser.Library m_CallBrowserLibrary = null;  
    private uint m_nLibraryCookie = 0;  
    // Create Library.  
    m_CallBrowserLibrary = new CallBrowser.Library();  
  
    ```  
  
2.  Uzyskaj odwołanie do obiektu <xref:Microsoft.VisualStudio.Shell.Interop.IVsObjectManager2> wpisz i Wywołaj <xref:Microsoft.VisualStudio.Shell.Interop.IVsObjectManager2.RegisterSimpleLibrary%2A> metody.  
  
    ```vb  
    Private Sub RegisterLibrary()  
        If m_nLibraryCookie <> 0 Then  
            Throw New Exception("Library already registered with Object Manager")  
        End If  
  
        ' Obtain a reference to IVsObjectManager2 type object.  
        Dim objManager As IVsObjectManager2 = TryCast(GetService(GetType(SVsObjectManager)), IVsObjectManager2)  
        If objManager Is Nothing Then  
            Throw New NullReferenceException("GetService failed for SVsObjectManager")  
        End If  
  
        Try  
            Dim hr As Integer = objManager.RegisterSimpleLibrary(m_CallBrowserLibrary, m_nLibraryCookie)  
            Microsoft.VisualStudio.ErrorHandler.ThrowOnFailure(hr)  
        Catch e As Exception  
            ' Code to handle any CLS-compliant exception.  
            Trace.WriteLine(e.Message)  
            Throw  
        End Try  
    End Sub  
    ```  
  
    ```csharp  
    private void RegisterLibrary()  
    {  
        if (m_nLibraryCookie != 0)  
            throw new Exception("Library already registered with Object Manager");  
  
        // Obtain a reference to IVsObjectManager2 type object.  
        IVsObjectManager2 objManager =   
                          GetService(typeof(SVsObjectManager)) as IVsObjectManager2;  
        if (objManager == null)  
            throw new NullReferenceException("GetService failed for SVsObjectManager");  
  
        try  
        {  
            int hr =   
                objManager.RegisterSimpleLibrary(m_CallBrowserLibrary,   
                                                 out m_nLibraryCookie);  
                Microsoft.VisualStudio.ErrorHandler.ThrowOnFailure(hr);  
        }  
        catch (Exception e)  
        {  
            // Code to handle any CLS-compliant exception.  
            Trace.WriteLine(e.Message);  
            throw;  
        }  
    }  
  
    ```  
  
#### <a name="to-unregister-a-library-with-the-object-manager"></a>Wyrejestrowania biblioteki z Menedżera obiektów  
  
1.  Uzyskaj odwołanie do obiektu <xref:Microsoft.VisualStudio.Shell.Interop.IVsObjectManager2> wpisz i Wywołaj <xref:Microsoft.VisualStudio.Shell.Interop.IVsObjectManager2.UnregisterLibrary%2A> metody.  
  
    ```vb  
    Private Sub UnregisterLibrary()  
        If m_nLibraryCookie <> 0 Then  
            ' Obtain a reference to IVsObjectManager2 type object.  
            Dim objManager As IVsObjectManager2 = TryCast(GetService(GetType(SVsObjectManager)), IVsObjectManager2)  
            If objManager Is Nothing Then  
                Throw New NullReferenceException("GetService failed for SVsObjectManager")  
            End If  
  
            Try  
                objManager.UnregisterLibrary(m_nLibraryCookie)  
            Catch e As Exception  
                ' Code to handle any CLS-compliant exception.  
                Trace.WriteLine(e.Message)  
                Throw  
            Finally  
                m_nLibraryCookie = 0  
            End Try  
        End If  
    End Sub  
    ```  
  
    ```csharp  
    private void UnregisterLibrary()  
    {  
        if (m_nLibraryCookie != 0)  
        {  
            // Obtain a reference to IVsObjectManager2 type object.  
            IVsObjectManager2 objManager = GetService(typeof(SVsObjectManager)) as IVsObjectManager2;  
            if (objManager == null)  
                throw new NullReferenceException("GetService failed for SVsObjectManager");  
  
            try  
            {  
                objManager.UnregisterLibrary(m_nLibraryCookie);  
            }  
            catch (Exception e)  
            {  
                // Code to handle any CLS-compliant exception.  
                Trace.WriteLine(e.Message);  
                throw;  
            }  
            finally  
            {  
                m_nLibraryCookie = 0;  
            }  
        }  
    }  
  
    ```  
  
## <a name="see-also"></a>Zobacz też  
 [Rozszerzalność usługi starszej wersji języka](../../extensibility/internals/legacy-language-service-extensibility.md)   
 [Obsługa narzędzia do przeglądania Symbol](../../extensibility/internals/supporting-symbol-browsing-tools.md)   
 [Porady: udostępnianie list symboli udostępniane przez bibliotekę do Menedżera obiektów](../../extensibility/internals/how-to-expose-lists-of-symbols-provided-by-the-library-to-the-object-manager.md)