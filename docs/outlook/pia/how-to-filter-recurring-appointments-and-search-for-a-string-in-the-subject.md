---
title: Filtrar citas periódicas y buscar una cadena en el asunto
TOCTitle: Filter recurring appointments and search for a string in the subject
ms:assetid: 997186aa-5264-4b19-bed6-51c38831c03d
ms:mtpsurl: https://msdn.microsoft.com/library/Bb611267(v=office.15)
ms:contentKeyID: 55119891
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6bda9cc663af1d1b9167ec78da286fe1c1991d40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320268"
---
# <a name="filter-recurring-appointments-and-search-for-a-string-in-the-subject"></a>Filtrar citas periódicas y buscar una cadena en el asunto

En este ejemplo se filtran citas periódicas que entran dentro de un intervalo de fechas de una carpeta Calendario y se buscan dos formas para la cadena "office" en el asunto.

## <a name="example"></a>Ejemplo

Para filtrar las citas periódicas, este ejemplo de código usa la colección [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) en lugar del objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)), ya que el objeto **Table** devuelve solo las citas de la serie principal y no incluye los elementos periódicos de la carpeta. Para incluir las citas periódicas al llamar al método [Find(String)](https://msdn.microsoft.com/library/bb646289\(v=office.15\)) o al método [Restrict(String)](https://msdn.microsoft.com/library/bb612531\(v=office.15\)), el ejemplo de código establece la propiedad [IncludeRecurrences](https://msdn.microsoft.com/library/bb646522\(v=office.15\)) de la colección **Items** y, luego, ordena las citas de la carpeta por la propiedad [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)). Después, usa una consulta Jet para especificar las fechas de inicio y finalización de las periodicidades.

Después de obtener una colección **Items** de citas periódicas que se encuentran dentro del intervalo de fechas especificado, el ejemplo de código lleva a cabo dos búsquedas más mediante consultas de búsqueda y ubicación DAV (DASL). La primera búsqueda usa **Items.Find**, [FindNext](https://msdn.microsoft.com/library/bb623799\(v=office.15\)) y la palabra clave **like** para buscar elementos que tengan la subcadena "office" en el asunto. La segunda búsqueda usa el método **Items.Restrict** y la palabra clave **ci\_startswith** para buscar elementos cuyos asuntos empiecen con "office."

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **Imports** o **using** no deben producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub SearchRecurringAppointments()
    Dim appt As Outlook.AppointmentItem = Nothing
    Dim folder As Outlook.Folder = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderCalendar), _
        Outlook.Folder)
    ' Set start value
    Dim startTime As DateTime = New DateTime(2006, 8, 9, 0, 0, 0)
    ' Set end value
    Dim endTime As DateTime = New DateTime(2006, 12, 14, 0, 0, 0)
    ' Initial restriction is Jet query for date range
    Dim filter1 As String = "[Start] >= '" & startTime.ToString("g") _
        & "' AND [End] <= '" & endTime.ToString("g") & "'"
    Dim calendarItems As Outlook.Items = folder.Items.Restrict(filter1)
    calendarItems.IncludeRecurrences = True
    calendarItems.Sort("[Start]")
    ' Must use 'like' comparison for Find/FindNext
    Dim filter2 As String
    filter2 = "@SQL=" & _
        Chr(34) & "urn:schemas:httpmail:subject" & Chr(34) & _
        " like '%Office%'"
    ' Create DASL query for additional Restrict method
    Dim filter3 As String
    If (Application.Session.DefaultStore.IsInstantSearchEnabled) Then
        filter3 = "@SQL=" & _
            Chr(34) & "urn:schemas:httpmail:subject" & Chr(34) & " _
            ci_startswith 'Office'"
    Else
        filter3 = "@SQL=" & _
            Chr(34) & "urn:schemas:httpmail:subject" & Chr(34) & " _
            like '%Office%'"
    End If
    ' Use Find and FindNext methods
    appt = CType(calendarItems.Find(filter2), Outlook.AppointmentItem)
    While Not (appt Is Nothing)
        Dim sb As StringBuilder = New StringBuilder()
        sb.AppendLine(appt.Subject)
        sb.AppendLine("Start: " & appt.Start)
        sb.AppendLine("End: " & appt.End)
        Debug.WriteLine(sb.ToString())
        ' Find the next appointment
        appt = CType(calendarItems.FindNext(), Outlook.AppointmentItem)
    End While
    ' Restrict calendarItems with DASL query
    Dim restrictedItems As Outlook.Items = _
        calendarItems.Restrict(filter3)
    For Each apptItem As Outlook.AppointmentItem In restrictedItems
        Dim sb As StringBuilder = New StringBuilder()
        sb.AppendLine(apptItem.Subject)
        sb.AppendLine("Start: " & apptItem.Start)
        sb.AppendLine("End: " & apptItem.End)
        sb.AppendLine()
        Debug.WriteLine(sb.ToString())
    Next
End Sub
```


```csharp
private void SearchRecurringAppointments()
{
    Outlook.AppointmentItem appt = null;
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderCalendar)
        as Outlook.Folder;
    // Set start value
    DateTime start =
        new DateTime(2006, 8, 9, 0, 0, 0);
    // Set end value
    DateTime end =
        new DateTime(2006, 12, 14, 0, 0, 0);
    // Initial restriction is Jet query for date range
    string filter1 = "[Start] >= '" +
        start.ToString("g")
        + "' AND [End] <= '" +
        end.ToString("g") + "'";
    Outlook.Items calendarItems = folder.Items.Restrict(filter1);
    calendarItems.IncludeRecurrences = true;
    calendarItems.Sort("[Start]", Type.Missing);
    // Must use 'like' comparison for Find/FindNext
    string filter2;
    filter2 = "@SQL="
        + "\"" + "urn:schemas:httpmail:subject" + "\""
        + " like '%Office%'";
    // Create DASL query for additional Restrict method
    string filter3;
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        filter3 = "@SQL="
            + "\"" + "urn:schemas:httpmail:subject" + "\""
            + " ci_startswith 'Office'";
    }
    else
    {
        filter3 = "@SQL="
            + "\"" + "urn:schemas:httpmail:subject" + "\""
            + " like '%Office%'";
    }
    // Use Find and FindNext methods
    appt = calendarItems.Find(filter2)
        as Outlook.AppointmentItem;
    while (appt != null)
    {
        StringBuilder sb = new StringBuilder();
        sb.AppendLine(appt.Subject);
        sb.AppendLine("Start: " + appt.Start);
        sb.AppendLine("End: " + appt.End);
        Debug.WriteLine(sb.ToString());
        // Find the next appointment
        appt = calendarItems.FindNext()
            as Outlook.AppointmentItem;
    }
    // Restrict calendarItems with DASL query
    Outlook.Items restrictedItems =
        calendarItems.Restrict(filter3);
    foreach (Outlook.AppointmentItem apptItem in restrictedItems)
    {
        StringBuilder sb = new StringBuilder();
        sb.AppendLine(apptItem.Subject);
        sb.AppendLine("Start: " + apptItem.Start);
        sb.AppendLine("End: " + apptItem.End);
        sb.AppendLine();
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a>Vea también

- [Search and filter](search-and-filter.md) (Buscar y filtrar)

