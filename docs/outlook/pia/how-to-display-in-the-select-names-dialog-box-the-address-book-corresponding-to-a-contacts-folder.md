---
title: Mostrar en el cuadro de diálogo Seleccionar nombres la libreta de direcciones correspondiente a una carpeta Contactos
TOCTitle: Display in the Select Names dialog box the address book corresponding to a Contacts folder
ms:assetid: 6cbfc843-51b5-4841-bbb1-14b93a35ba78
ms:mtpsurl: https://msdn.microsoft.com/library/Bb610437(v=office.15)
ms:contentKeyID: 55119799
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3be678b13738fead1509f3854c7b23bd0cfc8528
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356402"
---
# <a name="display-in-the-select-names-dialog-box-the-address-book-corresponding-to-a-contacts-folder"></a><span data-ttu-id="e5382-102">Mostrar en el cuadro de diálogo Seleccionar nombres la libreta de direcciones correspondiente a una carpeta Contactos</span><span class="sxs-lookup"><span data-stu-id="e5382-102">Display in the Select Names dialog box the address book corresponding to a Contacts folder</span></span>

<span data-ttu-id="e5382-103">En este ejemplo se muestra cómo obtener la libreta de direcciones correspondiente a la carpeta Contactos predeterminada y, a continuación, mostrarla en el cuadro de diálogo **Seleccionar nombres**.</span><span class="sxs-lookup"><span data-stu-id="e5382-103">This example shows how to obtain the address book that corresponds to the default Contacts folder, and then displays the address book in the **Select Names** dialog box.</span></span>

## <a name="example"></a><span data-ttu-id="e5382-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e5382-104">Example</span></span>

<span data-ttu-id="e5382-105">La propiedad [AddressLists](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) del objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) representa todas las libretas de direcciones en Outlook como una colección.</span><span class="sxs-lookup"><span data-stu-id="e5382-105">All address books in Outlook are represented as a collection by the [AddressLists](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) property of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span> <span data-ttu-id="e5382-106">El código de ejemplo usa el método [GetContactsFolder](https://msdn.microsoft.com/library/bb609225\(v=office.15\)) del objeto [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) para encontrar la carpeta de contactos que corresponde a cada lista de direcciones.</span><span class="sxs-lookup"><span data-stu-id="e5382-106">The code sample uses the [GetContactsFolder](https://msdn.microsoft.com/library/bb609225\(v=office.15\)) method of the [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) object to find the contact folder that corresponds to each address list.</span></span> <span data-ttu-id="e5382-107">Cada carpeta de Outlook tiene un identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="e5382-107">Each Outlook folder has an Entry ID.</span></span> <span data-ttu-id="e5382-108">Compare el identificador de entrada de la carpeta Contactos predeterminada con el identificador de entrada de una carpeta Contactos para generar el AddressList que corresponde a la carpeta Contactos.</span><span class="sxs-lookup"><span data-stu-id="e5382-108">Compare the Entry ID of the default Contacts folder with the Entry ID of a Contacts folder to produce the AddressList that corresponds to the default Contacts folder.</span></span>

<span data-ttu-id="e5382-109">Antes de mostrar la lista de direcciones correspondiente a la carpeta Contactos predeterminada en el cuadro de diálogo **Seleccionar nombres**, el ejemplo de código la configura como el valor de la propiedad [InitialAddressList](https://msdn.microsoft.com/library/bb646633\(v=office.15\)) del objeto [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="e5382-109">Before displaying the address list corresponding to the default Contacts folder in the **Select Names** dialog box, the code sample sets it as the value of the [InitialAddressList](https://msdn.microsoft.com/library/bb646633\(v=office.15\)) property of the [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) object.</span></span>

<span data-ttu-id="e5382-110">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="e5382-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="e5382-111">La instrucción **Imports** o **using** no deben producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="e5382-111">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="e5382-112">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.</span><span class="sxs-lookup"><span data-stu-id="e5382-112">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub ShowContactsFolderAsInitialAddressList()
    Dim addrLists As Outlook.AddressLists
    Dim contactsFolder As Outlook.Folder = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderContacts), _
        Outlook.Folder)
    addrLists = Application.Session.AddressLists
    For Each addrList As Outlook.AddressList In addrLists
        Dim testFolder As Outlook.Folder = _
        CType(addrList.GetContactsFolder(), Outlook.Folder)
        If Not (testFolder Is Nothing) Then
            ' Test to determine if Folder returned
            ' by GetContactsFolder has same EntryID
            ' as default Contacts folder.
            If (Application.Session.CompareEntryIDs( _
                contactsFolder.EntryID, testFolder.EntryID)) Then
                Dim snd As Outlook.SelectNamesDialog = _
                    Application.Session.GetSelectNamesDialog()
                snd.InitialAddressList = addrList
                snd.Display()
            End If
        End If
    Next
End Sub
```


```csharp
private void ShowContactsFolderAsInitialAddressList()
{
    Outlook.AddressLists addrLists;
    Outlook.Folder contactsFolder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts)
        as Outlook.Folder;
    addrLists = Application.Session.AddressLists;
    foreach (Outlook.AddressList addrList in addrLists)
    {
        Outlook.Folder testFolder =
            addrList.GetContactsFolder() as Outlook.Folder;
        if (testFolder != null)
        {
            // Test to determine if Folder returned
            // by GetContactsFolder has same EntryID
            // as default Contacts folder.
            if (Application.Session.CompareEntryIDs(
                contactsFolder.EntryID, testFolder.EntryID))
            {
                Outlook.SelectNamesDialog snd =
                    Application.
                    Session.GetSelectNamesDialog();
                snd.InitialAddressList = addrList;
                snd.Display();
             }
         }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="e5382-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5382-113">See also</span></span>

- [<span data-ttu-id="e5382-114">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="e5382-114">Address book</span></span>](address-book.md)

