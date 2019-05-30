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
# <a name="access-solution-specific-data-stored-as-a-hidden-message-in-a-folder"></a>Acceder a datos específicos de la solución almacenados como un mensaje oculto en una carpeta

Este ejemplo muestra cómo usar el objeto [StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) para recuperar datos almacenados como un mensaje oculto de una clase de mensaje específica de una carpeta.

## <a name="example"></a>Ejemplo

El objeto **StorageItem** generalmente se usa para ocultar datos específicos de la solución que no se pueden mostrar mediante programación. En un entorno de Exchange, el objeto **StorageItem** se usa para trasladar la configuración de la solución y garantizar que esté disponible en línea y sin conexión. Puede asignar una clase de mensajes personalizada al objeto **StorageItem** o identificar el objeto por asunto.

El siguiente ejemplo de código recupera los datos XML almacenados como mensaje oculto en la carpeta Calendario con la clase de mensajes igual a IPM.Configuration.WorkHours. 

El objeto [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) devuelve los archivos XML como un objeto que contiene una secuencia de bytes en lugar de una representación de cadena del XML. El código de ejemplo usa **System.Text.Encoding.Ascii.GetString** para convertir la secuencia de bytes en una cadena.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **Imports** o **using** no deben producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.

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


## <a name="see-also"></a>Vea también

- [Folders](folders.md) (Carpetas)

