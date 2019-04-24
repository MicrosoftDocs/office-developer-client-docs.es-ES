---
title: Abrir y ver los contenidos de un archivo de iCalendar
TOCTitle: Open and display the contents of an iCalendar file
ms:assetid: 2066e404-7aaf-4fd2-bf5c-9604e3fc2681
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644609(v=office.15)
ms:contentKeyID: 55119818
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fad55b4e9b98a2157d1efdab83d5495cd2169429
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320023"
---
# <a name="open-and-display-the-contents-of-an-icalendar-file"></a><span data-ttu-id="7de63-102">Abrir y ver los contenidos de un archivo de iCalendar</span><span class="sxs-lookup"><span data-stu-id="7de63-102">Open and display the contents of an iCalendar file</span></span>

<span data-ttu-id="7de63-103">En este ejemplo se muestra cómo abrir y mostrar el contenido de un archivo de iCalendar, en función de si el archivo contiene una sola cita o una cita recurrente, o si el archivo contiene un grupo de citas.</span><span class="sxs-lookup"><span data-stu-id="7de63-103">This example shows how to open and display the contents of an iCalendar file, depending on whether the file contains a single or recurrent appointment, or the file contains a group of appointments.</span></span>

## <a name="example"></a><span data-ttu-id="7de63-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7de63-104">Example</span></span>

<span data-ttu-id="7de63-105">Este ejemplo de código primero intenta usar el método [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\)) del objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) para abrir el archivo de iCalendar como un archivo de iCalendar de una sola cita.</span><span class="sxs-lookup"><span data-stu-id="7de63-105">This code sample first tries to use the [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object to open the iCalendar file as a single-appointment iCalendar file.</span></span> <span data-ttu-id="7de63-106">Si lo consigue, mostrará los detalles del elemento de cita en una ventana de inspector.</span><span class="sxs-lookup"><span data-stu-id="7de63-106">If it succeeds, it will display the appointment item details in an inspector window.</span></span> <span data-ttu-id="7de63-107">Sin embargo, no copiará el elemento en el almacén predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7de63-107">However, it will not copy the item to the default store.</span></span> <span data-ttu-id="7de63-108">Si el ejemplo no puede abrir el archivo como un archivo de iCalendar de una sola cita, usará el método [OpenSharedFolder](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) del objeto **NameSpace** para tratar de importar los contenidos como un nuevo calendario en el almacén predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7de63-108">If the sample cannot open the file as a single-appointment iCalendar file, then it will use the [OpenSharedFolder](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) method of the **NameSpace** object to attempt to import the contents as a new calendar in the default store.</span></span> <span data-ttu-id="7de63-109">Si lo importa correctamente, mostrará el calendario en una ventana del explorador.</span><span class="sxs-lookup"><span data-stu-id="7de63-109">If it succeeds in importing, then it will display the calendar in an explorer window.</span></span>

<span data-ttu-id="7de63-110">Este ejemplo de código utiliza la clase auxiliar OutlookItem, definida en [Crear una clase auxiliar para acceder a los miembros de elementos comunes de Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), para llamar al método **OutlookItem.Display** y así poder mostrar el elemento de cita sin tener que convertir antes el elemento.</span><span class="sxs-lookup"><span data-stu-id="7de63-110">This code sample makes use of the OutlookItem helper class, defined in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), to conveniently call the **OutlookItem.Display** method to display the appointment item without having to first cast the item.</span></span>

<span data-ttu-id="7de63-111">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="7de63-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="7de63-112">La instrucción **Imports** o **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="7de63-112">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="7de63-113">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.</span><span class="sxs-lookup"><span data-stu-id="7de63-113">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub OpenICalendarFile(ByVal fileName As String)
    If String.IsNullOrEmpty(fileName) Then
        Throw New ArgumentException(_
        "Parameter must contain a value.", "exportFileName")
    End If
    If Not File.Exists(fileName) Then
        Throw New FileNotFoundException(fileName)
    End If

    '' First try to open the icalendar file as an appointment 
    '' (not a calendar folder).
    Dim item As Object = Nothing
    Try
         item = Application.Session.OpenSharedItem(fileName)
    Catch
    End Try

    If Not item Is Nothing Then
        '' Display the item
        Dim olItem As OutlookItem = New OutlookItem(item)
        olItem.Display()
        Return
    End If

    '' If unsucessful in opening it as an item, 
    '' try opening it as a folder
    Dim importedFolder As Outlook.Folder = Nothing
    Try
        importedFolder = TryCast( _
            Application.Session.OpenSharedFolder(fileName), _
            Outlook.Folder)
    Catch
    End Try

    '' If sucessful, open the folder in a new explorer window
    If Not importedFolder Is Nothing Then
        Dim explorer As Outlook.Explorer = _
            Application.Explorers.Add( _
            importedFolder, _
            Outlook.OlFolderDisplayMode.olFolderDisplayNormal)
        explorer.Display()
    End If
End Sub
```


```csharp
private void OpenICalendarFile(string fileName)
{
    if (string.IsNullOrEmpty(fileName))
        throw new ArgumentException("exportFileName", 
        "Parameter must contain a value.");
    if (!File.Exists(fileName))
        throw new FileNotFoundException(fileName);

    // First try to open the icalendar file as an appointment 
    // (not a calendar folder).
    object item = null;
    try
    {
        item = Application.Session.OpenSharedItem(fileName);
    }
    catch
    { }

    if (item != null)
    {
         // Display the item
         OutlookItem olItem = new OutlookItem(item);
         olItem.Display();
         return;
    }

    // If unsucessful in opening it as an item, 
    // try opening it as a folder
    Outlook.Folder importedFolder = null;
    try
    {
        importedFolder = Application.Session.OpenSharedFolder(
            fileName, Type.Missing, Type.Missing, Type.Missing) 
            as Outlook.Folder;
    }
    catch
    { }

    // If sucessful, open the folder in a new explorer window
    if (importedFolder != null)
    {
        Outlook.Explorer explorer =
            Application.Explorers.Add(importedFolder, 
            Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
        explorer.Display();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="7de63-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="7de63-114">See also</span></span>

- [<span data-ttu-id="7de63-115">Calendario</span><span class="sxs-lookup"><span data-stu-id="7de63-115">Calendar</span></span>](calendar.md)

