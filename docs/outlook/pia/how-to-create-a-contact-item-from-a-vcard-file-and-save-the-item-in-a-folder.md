---
title: Crear un elemento de contacto desde un archivo vCard y guardar el elemento en una carpeta
TOCTitle: Create a Contact item from a vCard file and save the item in a folder
ms:assetid: b207b584-ffcf-4ac5-ab1f-4f91d43000e1
ms:mtpsurl: https://msdn.microsoft.com/library/Bb646856(v=office.15)
ms:contentKeyID: 55119826
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3a048d090c946ff5a86fddf4b1ac8c6818e061b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321262"
---
# <a name="create-a-contact-item-from-a-vcard-file-and-save-the-item-in-a-folder"></a><span data-ttu-id="79f34-102">Crear un elemento de contacto desde un archivo vCard y guardar el elemento en una carpeta</span><span class="sxs-lookup"><span data-stu-id="79f34-102">Create a Contact item from a vCard file and save the item in a folder</span></span>

<span data-ttu-id="79f34-103">En este ejemplo se importan todos los archivos vCard en una carpeta del sistema de archivos y se guardan los contactos en la carpeta especificada por el parámetro *targetFolder*.</span><span class="sxs-lookup"><span data-stu-id="79f34-103">This example imports all the vCard files in a file system folder and saves the contacts into the folder specified by the *targetFolder* parameter.</span></span>

## <a name="example"></a><span data-ttu-id="79f34-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="79f34-104">Example</span></span>

<span data-ttu-id="79f34-105">Este ejemplo usa el método [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="79f34-105">This example uses the [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\)) method.</span></span> <span data-ttu-id="79f34-106">El método **OpenSharedItem** abre los mensajes almacenados como archivos de formato de mensaje de Outlook (.msg), archivos de citas de iCalendar (.ics) o archivos vCard (.vcf).</span><span class="sxs-lookup"><span data-stu-id="79f34-106">The **OpenSharedItem** method opens messages stored as Outlook message format (.msg) files, iCalendar appointment (.ics) files, or vCard (.vcf) files.</span></span> <span data-ttu-id="79f34-107">Asegúrese de convertir el objeto devuelto al tipo de elemento correspondiente y de llamar a los métodos **Save** correspondientes para conservar el elemento.</span><span class="sxs-lookup"><span data-stu-id="79f34-107">Be sure to cast the returned object to the appropriate item type and call the corresponding **Save** method to persist the item.</span></span> <span data-ttu-id="79f34-108">De forma predeterminada, el elemento devuelto por **OpenSharedItem** se guarda en la carpeta predeterminada para el tipo de elemento específico.</span><span class="sxs-lookup"><span data-stu-id="79f34-108">By default, the item returned by **OpenSharedItem** is saved in the default folder for the specific item type.</span></span> <span data-ttu-id="79f34-109">Puede usar el método **Move** correspondiente para mover el elemento a otra carpeta.</span><span class="sxs-lookup"><span data-stu-id="79f34-109">You can use the corresponding **Move** method to move the item to a different folder.</span></span>

<span data-ttu-id="79f34-110">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="79f34-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="79f34-111">La instrucción **Imports** o **using** no deben producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="79f34-111">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="79f34-112">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.</span><span class="sxs-lookup"><span data-stu-id="79f34-112">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub ImportContacts( _
    ByVal path As String, ByVal targetFolder As Outlook.Folder)
    Dim contact As Outlook.ContactItem
    Dim moveContact As Outlook.ContactItem
    If (Directory.Exists(path)) Then
        Dim files As String() = Directory.GetFiles(path, "*.vcf")
        For Each file As String In files
            contact = CType(Application.Session.OpenSharedItem(file), _
                Outlook.ContactItem)
            If (targetFolder Is _
                CType(Application.Session.GetDefaultFolder( _
                    Outlook.OlDefaultFolders.olFolderContacts) _
                    , Outlook.Folder)) Then
                contact.Save()
            Else
                moveContact = CType(contact.Move(targetFolder), _
                    Outlook.ContactItem)
                moveContact.Save()
            End If
        Next
    End If
End Sub
```


```csharp
private void ImportContacts(string path, Outlook.Folder targetFolder)
{
    Outlook.ContactItem contact;
    Outlook.ContactItem moveContact;
    if (Directory.Exists(path))
    {
        string[] files = Directory.GetFiles(path, "*.vcf");
        foreach (string file in files)
        {
            contact = Application.Session.OpenSharedItem(file)
                as Outlook.ContactItem;
            if (targetFolder ==
                Application.Session.GetDefaultFolder(
                Outlook.OlDefaultFolders.olFolderContacts)
                as Outlook.Folder)
            {
                contact.Save();
            }
            else
            {
                moveContact = contact.Move(targetFolder)
                    as Outlook.ContactItem;
                moveContact.Save();
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="79f34-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="79f34-113">See also</span></span>

- <span data-ttu-id="79f34-114">[Contacts](contacts.md) (Contactos)</span><span class="sxs-lookup"><span data-stu-id="79f34-114">[Contacts](contacts.md)</span></span>

