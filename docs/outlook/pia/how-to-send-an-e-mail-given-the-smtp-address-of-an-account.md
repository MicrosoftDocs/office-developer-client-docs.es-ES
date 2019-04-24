---
title: Enviar un correo electrónico según la dirección SMTP de una cuenta
TOCTitle: Send an email given the SMTP address of an account
ms:assetid: 4ff4aaac-54ba-45c7-8b2e-aeba35af1e56
ms:mtpsurl: https://msdn.microsoft.com/library/Ff462095(v=office.15)
ms:contentKeyID: 55119865
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0771941581d0edaab1660790582cfb22bef48dc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332098"
---
# <a name="send-an-email-given-the-smtp-address-of-an-account"></a>Enviar un correo electrónico según la dirección SMTP de una cuenta

En este tema se muestra cómo crear un correo electrónico y enviarlo desde una cuenta de Microsoft Outlook según la dirección del protocolo simple de transferencia de correo (SMTP, Simple Mail Transfer Protocol) de esa cuenta.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> Helmut Obertanner proporciona los siguientes ejemplos de código. Los conocimientos de Helmut están en Office Developer Tools para Visual Studio y Outlook. 


Los siguientes ejemplos de código contienen los métodos SendEmailFromAccount y GetAccountForEmailAddress de la clase Sample, implementados como parte de un proyecto de complemento de Outlook. Cada proyecto agrega una referencia al ensamblado de interoperabilidad primario de Outlook, que se basa en el espacio de nombres [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)). El método SendEmailFromAccount acepta como argumentos de entrada un objeto [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) de confianza y cadenas que representan el asunto, el cuerpo, una lista delimitada por punto y coma de los destinatarios y la dirección SMTP de una cuenta de correo electrónico. SendEmailFromAccount crea un objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) e inicializa las propiedades [To](https://msdn.microsoft.com/library/bb624372\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)), y [Body](https://msdn.microsoft.com/library/bb646600\(v=office.15\)) con los determinados argumentos. Para buscar el objeto [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) desde el que se envíe el correo electrónico, SendEmailFromAccount llama al método GetAccountForEmailAddress, que permite a la dirección SMTP determinada coincidir con la propiedad [SmtpAddress](https://msdn.microsoft.com/library/bb623516\(v=office.15\)) de cada cuenta del perfil actual. El objeto **Account** coincidente se devuelve a SendEmailFromAccount que, luego, inicializa la propiedad [SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\)) del **MailItem** con este objeto **Account** y envía el **MailItem**.

A continuación, el ejemplo de código de Visual Basic, seguido por el ejemplo de código de C\#.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **Imports** o **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook

Namespace OutlookAddIn2
    Class Sample
        
        Shared Sub SendEmailFromAccount(ByVal application As Outlook.Application, _
            ByVal subject As String, ByVal body As String, ByVal recipients As String, ByVal smtpAddress As String)

            ' Create a new MailItem and set the To, Subject, and Body properties.
            Dim newMail As Outlook.MailItem = DirectCast(application.CreateItem(Outlook.OlItemType.olMailItem), Outlook.MailItem)
            newMail.To = recipients
            newMail.Subject = subject
            newMail.Body = body

            ' Retrieve the account that has the specific SMTP address.
            Dim account As Outlook.Account = GetAccountForEmailAddress(application, smtpAddress)
            ' Use this account to send the email.
            newMail.SendUsingAccount = account
            newMail.Send()
        End Sub

        Shared Function GetAccountForEmailAddress(ByVal application As Outlook.Application, ByVal smtpAddress As String) As Outlook.Account

            ' Loop over the Accounts collection of the current Outlook session.
            Dim accounts As Outlook.Accounts = application.Session.Accounts
            Dim account As Outlook.Account
            For Each account In accounts
                ' When the email address matches, return the account.
                If account.SmtpAddress = smtpAddress Then
                    Return account
                End If
            Next
            Throw New System.Exception(String.Format("No Account with SmtpAddress: {0} exists!", smtpAddress))
        End Function

    End Class
End Namespace
```


```csharp
using System;
using System.Text;
using Outlook = Microsoft.Office.Interop.Outlook;

namespace OutlookAddIn1
{
    class Sample
    {
        public static void SendEmailFromAccount(Outlook.Application application, string subject, string body, string to, string smtpAddress)
        {

            // Create a new MailItem and set the To, Subject, and Body properties.
            Outlook.MailItem newMail = (Outlook.MailItem)application.CreateItem(Outlook.OlItemType.olMailItem);
            newMail.To = to;
            newMail.Subject = subject;
            newMail.Body = body;

            // Retrieve the account that has the specific SMTP address.
            Outlook.Account account = GetAccountForEmailAddress(application, smtpAddress);
            // Use this account to send the email.
            newMail.SendUsingAccount = account;
            newMail.Send();
        }


        public static Outlook.Account GetAccountForEmailAddress(Outlook.Application application, string smtpAddress)
        {

            // Loop over the Accounts collection of the current Outlook session.
            Outlook.Accounts accounts = application.Session.Accounts;
            foreach (Outlook.Account account in accounts)
            {
                // When the email address matches, return the account.
                if (account.SmtpAddress == smtpAddress)
                {
                    return account;
                }
            }
            throw new System.Exception(string.Format("No Account with SmtpAddress: {0} exists!", smtpAddress));
        }

    }
}
```

## <a name="see-also"></a>Vea también

- [Correo](mail.md)

