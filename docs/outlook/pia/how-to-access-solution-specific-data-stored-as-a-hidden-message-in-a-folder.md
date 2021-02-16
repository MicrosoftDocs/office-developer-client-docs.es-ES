---
title: Acceder a datos específicos de la solución almacenados como un mensaje oculto en una carpeta
TOCTitle: Access solution-specific data stored as a hidden message in a folder
ms:assetid: bacf0562-1026-4c3b-87b0-4eaad5033592
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623414(v=office.15)
ms:contentKeyID: 55119861
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c64caf831f79ab61e5e3e0b9d712a511a7ba4f31
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537951"
---
# <a name="access-solution-specific-data-stored-as-a-hidden-message-in-a-folder"></a><span data-ttu-id="a2b9d-102">Acceder a datos específicos de la solución almacenados como un mensaje oculto en una carpeta</span><span class="sxs-lookup"><span data-stu-id="a2b9d-102">Access solution-specific data stored as a hidden message in a folder</span></span>

<span data-ttu-id="a2b9d-103">Este ejemplo muestra cómo usar el objeto [StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) para recuperar datos almacenados como un mensaje oculto de una clase de mensaje específica de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-103">This example shows how to use the [StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) object to retrieve data that is stored as a hidden message of a specific message class in a folder.</span></span>

## <a name="example"></a><span data-ttu-id="a2b9d-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a2b9d-104">Example</span></span>

<span data-ttu-id="a2b9d-p101">El objeto **StorageItem** generalmente se usa para ocultar datos específicos de la solución que no se pueden mostrar mediante programación. En un entorno de Exchange, el objeto **StorageItem** se usa para trasladar la configuración de la solución y garantizar que esté disponible en línea y sin conexión. Puede asignar una clase de mensajes personalizada al objeto **StorageItem** o identificar el objeto por asunto.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-p101">The **StorageItem** object is typically used to hide solution-specific data that cannot be displayed programmatically. In an Exchange environment, the **StorageItem** object is used to roam solution settings and ensure that these settings are available online and offline. You can assign a custom message class to the **StorageItem** object, or identify the object by subject.</span></span>

<span data-ttu-id="a2b9d-108">El siguiente ejemplo de código recupera los datos XML almacenados como mensaje oculto en la carpeta Calendario con la clase de mensajes igual a IPM.Configuration.WorkHours. </span><span class="sxs-lookup"><span data-stu-id="a2b9d-108">The following code sample retrieves the XML data that is stored as a hidden message in the Calendar folder with the message class equal to IPM.Configuration.WorkHours.</span></span>

<span data-ttu-id="a2b9d-109">El objeto [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) devuelve los archivos XML como un objeto que contiene una secuencia de bytes en lugar de una representación de cadena del XML.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-109">The [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object returns the XML as an object that contains a byte stream rather than a string representation of the XML.</span></span> <span data-ttu-id="a2b9d-110">El código de ejemplo usa **System.Text.Encoding.Ascii.GetString** para convertir la secuencia de bytes en una cadena.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-110">The code sample uses **System.Text.Encoding.Ascii.GetString** to convert the byte stream to a string.</span></span>

<span data-ttu-id="a2b9d-111">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="a2b9d-112">La instrucción **Imports** o **using** no deben producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-112">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="a2b9d-113">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.</span><span class="sxs-lookup"><span data-stu-id="a2b9d-113">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Function GetWorkHoursXML() As String
    Try
        Dim storage As Outlook.StorageItem = _
            Application.Session.GetDefaultFolder( _
            Outlook.OlDefaultFolders.olFolderCalendar).GetStorage( _
            "IPM.Configuration.WorkHours", _
            Outlook.OlStorageIdentifierType.olIdentifyByMessageClass)
        Dim pa As Outlook.PropertyAccessor = storage.PropertyAccessor
        ' PropertyAccessor will return a byte array for this property
        Dim rawXmlBytes As Byte() = CType(pa.GetProperty( _
            "http://schemas.microsoft.com/mapi/proptag/0x7C080102"), _
            Byte())
        ' Use Encoding to convert the array to a string
        Return System.Text.Encoding.ASCII.GetString(rawXmlBytes)
    Catch
        Return String.Empty
    End Try
End Function
```

```csharp
private string GetWorkHoursXML()
{
    try
    {
        Outlook.StorageItem storage =
            Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderCalendar).GetStorage(
            "IPM.Configuration.WorkHours",
            Outlook.OlStorageIdentifierType.olIdentifyByMessageClass);
        Outlook.PropertyAccessor pa = storage.PropertyAccessor;
        // PropertyAccessor will return a byte array for this property
        byte[] rawXmlBytes = (byte[])pa.GetProperty(
            "http://schemas.microsoft.com/mapi/proptag/0x7C080102");
        // Use Encoding to convert the array to a string
        return System.Text.Encoding.ASCII.GetString(rawXmlBytes);
    }
    catch
    {
        return string.Empty;
    }
}
```


## <a name="see-also"></a><span data-ttu-id="a2b9d-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2b9d-114">See also</span></span>

- <span data-ttu-id="a2b9d-115">[Folders](folders.md) (Carpetas)</span><span class="sxs-lookup"><span data-stu-id="a2b9d-115">[Folders](folders.md)</span></span>

