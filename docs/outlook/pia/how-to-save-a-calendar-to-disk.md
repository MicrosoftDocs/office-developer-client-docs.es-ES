---
title: Guardar un calendario en el disco
TOCTitle: Save a calendar to disk
ms:assetid: f1b57bd0-c972-4b86-8870-f26290f28050
ms:mtpsurl: https://msdn.microsoft.com/library/Bb647583(v=office.15)
ms:contentKeyID: 55119827
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b07df7458f80b751077358ac3c53ad41032d1080
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361050"
---
# <a name="save-a-calendar-to-disk"></a>Guardar un calendario en el disco

En este ejemplo se muestra cómo guardar un calendario completo en el disco en el formato de archivo de iCalendar (.ics).

## <a name="example"></a>Ejemplo

Este código de ejemplo usa el objeto [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) que admite guardar un calendario completo o un rango de citas del calendario en el disco. Outlook optimiza automáticamente un archivo .ics para que las citas periódicas no se guarden como citas individuales en el archivo .ics. Dependiendo del tamaño del calendario, guardarlo en el disco puede tardar mucho tiempo. Al guardar el calendario, la ventana de Outlook no responde. 

El ejemplo de código llama primero a [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) en la carpeta de Calendario predeterminada para obtener un objeto **CalendarSharing**. Luego, establece las propiedades del objeto **CalendarSharing** para especificar criterios para la exportación, por ejemplo, si desea guardar todo el calendario e incluir los detalles de las citas que están marcados como "privadas".

Para guardar la información del calendario en el formato de archivo .ics, el ejemplo de código llama al método [SaveAsICal](https://msdn.microsoft.com/library/bb644844\(v=office.15\)) del objeto **CalendarSharing**.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **Imports** o **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub SaveCalendarToDisk(ByVal calendarFileName As String)
    If String.IsNullOrEmpty(calendarFileName) Then
        Throw New ArgumentException( _
        "Parameter must contain a value.", "calendarFileName")
    End If

    Dim calendar As Outlook.Folder = TryCast( _
        Application.Session.GetDefaultFolder(_
        Outlook.OlDefaultFolders.olFolderCalendar), Outlook.Folder)
    Dim exporter As Outlook.CalendarSharing = _
        calendar.GetCalendarExporter()

    '' Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails
    exporter.IncludeAttachments = True
    exporter.IncludePrivateDetails = True
    exporter.RestrictToWorkingHours = False
    exporter.IncludeWholeCalendar = True

    '' Save the calendar to disk
    exporter.SaveAsICal(calendarFileName)
End Sub
```


```csharp
private void SaveCalendarToDisk(string calendarFileName)
{
    if (string.IsNullOrEmpty(calendarFileName))
        throw new ArgumentException("calendarFileName", 
        "Parameter must contain a value.");

    Outlook.Folder calendar = Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderCalendar) as Outlook.Folder;
    Outlook.CalendarSharing exporter = calendar.GetCalendarExporter();

    // Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails;
    exporter.IncludeAttachments = true;
    exporter.IncludePrivateDetails = true;
    exporter.RestrictToWorkingHours = false;
    exporter.IncludeWholeCalendar = true;

    // Save the calendar to disk
    exporter.SaveAsICal(calendarFileName);
}
```

## <a name="see-also"></a>Vea también

- [Calendario](calendar.md)

