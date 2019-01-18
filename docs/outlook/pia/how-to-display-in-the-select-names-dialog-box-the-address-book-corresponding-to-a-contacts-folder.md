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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699222"
---
# <a name="display-in-the-select-names-dialog-box-the-address-book-corresponding-to-a-contacts-folder"></a>Mostrar en el cuadro de diálogo Seleccionar nombres la libreta de direcciones correspondiente a una carpeta Contactos

En este ejemplo se muestra cómo obtener la libreta de direcciones correspondiente a la carpeta Contactos predeterminada y, a continuación, mostrarla en el cuadro de diálogo **Seleccionar nombres**.

## <a name="example"></a>Ejemplo

La propiedad [AddressLists](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) del objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) representa todas las libretas de direcciones en Outlook como una colección. El código de ejemplo usa el método [GetContactsFolder](https://msdn.microsoft.com/library/bb609225\(v=office.15\)) del objeto [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) para encontrar la carpeta de contactos que corresponde a cada lista de direcciones. Cada carpeta de Outlook tiene un identificador de entrada. Compare el identificador de entrada de la carpeta Contactos predeterminada con el identificador de entrada de una carpeta Contactos para generar el AddressList que corresponde a la carpeta Contactos.

Antes de mostrar la lista de direcciones correspondiente a la carpeta Contactos predeterminada en el cuadro de diálogo **Seleccionar nombres**, el ejemplo de código la configura como el valor de la propiedad [InitialAddressList](https://msdn.microsoft.com/library/bb646633\(v=office.15\)) del objeto [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)).

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **Imports** o **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.

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

## <a name="see-also"></a>Vea también

- [Libreta de direcciones](address-book.md)

