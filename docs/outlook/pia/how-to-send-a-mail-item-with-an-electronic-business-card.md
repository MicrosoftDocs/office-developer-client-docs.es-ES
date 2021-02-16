---
title: Enviar un elemento de correo con una tarjeta de presentación electrónica
TOCTitle: Send a mail item with an electronic business card
ms:assetid: f8aae7f2-85fc-4ed0-9f59-282ede702357
ms:mtpsurl: https://msdn.microsoft.com/library/Bb624312(v=office.15)
ms:contentKeyID: 55119839
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25809fc0d1726c9f56be417ae53fadecc831d62f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331153"
---
# <a name="send-a-mail-item-with-an-electronic-business-card"></a><span data-ttu-id="5a6fe-102">Enviar un elemento de correo con una tarjeta de presentación electrónica</span><span class="sxs-lookup"><span data-stu-id="5a6fe-102">Send a mail item with an electronic business card</span></span>

<span data-ttu-id="5a6fe-103">En este ejemplo se crea un elemento de correo, se busca una tarjeta de presentación electrónica y, si se encuentra una, se inserta en el elemento de correo.</span><span class="sxs-lookup"><span data-stu-id="5a6fe-103">This example creates a mail item, looks for an electronic business card, and if it finds one, inserts the electronic business card into the mail item.</span></span>

## <a name="example"></a><span data-ttu-id="5a6fe-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5a6fe-104">Example</span></span>

<span data-ttu-id="5a6fe-105">Para insertar una tarjeta de presentación electrónica, puede llamar a [AddBusinessCard](https://msdn.microsoft.com/library/bb647034\(v=office.15\)) en el objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="5a6fe-105">To insert an electronic business card, you can call [AddBusinessCard](https://msdn.microsoft.com/library/bb647034\(v=office.15\)) on the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object.</span></span> <span data-ttu-id="5a6fe-106">Este método toma una cadena que representa una dirección de correo electrónico e intenta encontrar un [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) con esa dirección en la carpeta Contactos.</span><span class="sxs-lookup"><span data-stu-id="5a6fe-106">This method takes a string representing an email address and attempts to find a [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) with that address in the default Contacts folder.</span></span> <span data-ttu-id="5a6fe-107">Un **ContactItem** puede tener hasta tres direcciones de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="5a6fe-107">A **ContactItem** can have as many as three email addresses.</span></span> <span data-ttu-id="5a6fe-108">Si se encuentra el contacto, el ejemplo llama al método **AddBusinessCard** y después muestra el mensaje para el usuario.</span><span class="sxs-lookup"><span data-stu-id="5a6fe-108">If the contact is found, the example calls the **AddBusinessCard** method, and then displays the message to the user.</span></span>

<span data-ttu-id="5a6fe-109">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="5a6fe-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="5a6fe-110">La instrucción **Imports** o **using** no deben producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="5a6fe-110">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="5a6fe-111">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.</span><span class="sxs-lookup"><span data-stu-id="5a6fe-111">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub AddBusinessCard(ByVal eMailAddress As String)
    Dim mail As Outlook.MailItem = CType(Application.CreateItem( _
        Outlook.OlItemType.olMailItem), Outlook.MailItem)
    mail.BodyFormat = Outlook.OlBodyFormat.olFormatHTML
    Dim contact As Outlook.ContactItem = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderContacts).Items.Find( _
        "[Email1Address]='" & eMailAddress & "'" & " OR " & _
        "[Email2Address]='" & eMailAddress & "'" + " OR " & _
        "[Email3Address]='" & eMailAddress & "'") _
        , Outlook.ContactItem)
    If (contact Is Nothing) Then
        Return
    End If
    mail.AddBusinessCard(contact)
    mail.Display(False)
End Sub
```


```csharp
private void AddBusinessCard(string eMailAddress)
{
    Outlook.MailItem mail = Application.CreateItem(
        Outlook.OlItemType.olMailItem) as Outlook.MailItem;
    mail.BodyFormat = Outlook.OlBodyFormat.olFormatHTML;
    Outlook.ContactItem contact = Application.Session.
        GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Items.Find(
        "[Email1Address]='" + eMailAddress + "'" + " OR " +
        "[Email2Address]='" + eMailAddress + "'" + " OR " +
        "[Email3Address]='" + eMailAddress + "'")
        as Outlook.ContactItem;
    if (contact == null)
    {
        return;
    }
    mail.AddBusinessCard(contact);
    mail.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="5a6fe-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a6fe-112">See also</span></span>

- [<span data-ttu-id="5a6fe-113">Tarjetas de presentación electrónicas</span><span class="sxs-lookup"><span data-stu-id="5a6fe-113">Electronic business cards</span></span>](electronic-business-cards.md)

