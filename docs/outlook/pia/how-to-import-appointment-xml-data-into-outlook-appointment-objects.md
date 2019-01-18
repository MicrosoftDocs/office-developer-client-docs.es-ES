---
title: Importar datos XML de una cita en objetos de citas de Outlook
TOCTitle: Import appointment XML data into Outlook appointment objects
ms:assetid: 166a648a-1c48-4984-8889-a7614cc277b1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff462092(v=office.15)
ms:contentKeyID: 55119821
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0af86772fced3e69d1d28cf8d98a544e3b4d90d2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705389"
---
# <a name="import-appointment-xml-data-into-outlook-appointment-objects"></a>Importar datos XML de una cita en objetos de citas de Outlook

En este tema se muestra cómo leer datos de citas con marcado XML, guardar los datos en objetos Outlook [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) del calendario predeterminado y devolver los objetos de citas en una matriz.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> Helmut Obertanner proporciona los siguientes ejemplos de código. Los conocimientos de Helmut están en Office Developer Tools para Visual Studio y Outlook. 


Los ejemplos de código siguientes contienen el método CreateAppointmentsFromXml de la clase Sample, implementado como parte de un proyecto de complemento de Outlook. Cada proyecto agrega una referencia al ensamblado de interoperabilidad primario de Outlook, que se basa en el espacio de nombres [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)).

El método CreateAppointmentsFromXml acepta dos parámetros de entrada:

  - application es un objeto [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) de Outlook de confianza.

  - xml es una cadena XML o una cadena que representa una ruta de acceso a un archivo XML válido. Para el fin de los siguientes ejemplos de código, el código XML delimita los datos de cita mediante las siguientes etiquetas XML:
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p>Datos de la cita</p></th>
    <th><p>Etiqueta XML delimitadora</p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>Todo el conjunto de datos de la cita</p></td>
    <td><p>appointments</p></td>
    </tr>
    <tr class="even">
    <td><p>Cada cita del conjunto</p></td>
    <td><p>appointment</p></td>
    </tr>
    <tr class="odd">
    <td><p>Hora de inicio de una cita</p></td>
    <td><p>starttime</p></td>
    </tr>
    <tr class="even">
    <td><p>Hora de finalización de una cita</p></td>
    <td><p>endtime</p></td>
    </tr>
    <tr class="odd">
    <td><p>Título de una cita</p></td>
    <td><p>subject</p></td>
    </tr>
    <tr class="even">
    <td><p>Ubicación de una cita</p></td>
    <td><p>location</p></td>
    </tr>
    <tr class="odd">
    <td><p>Detalles de una cita</p></td>
    <td><p>body</p></td>
    </tr>
    </tbody>
    </table>


En el ejemplo siguiente se muestran los datos de entrada para el parámetro *xml*.

```xml
<?xml version="1.0" encoding="utf-8" ?> 
<appointments>
    <appointment>
        <starttime>2009-06-01T15:00:00</starttime>
        <endtime>2009-06-01T16:15:00</endtime>
        <subject>This is a Test-Appointment</subject>
        <location>At your Desk</location>
        <body>Here is the Bodytext</body>
    </appointment>
    <appointment>
        <starttime>2009-06-01T17:00:00</starttime>
        <endtime>2009-06-01T17:15:00</endtime>
        <subject>This is a second Test-Appointment</subject>
        <location>At your Desk</location>
        <body>Here is the Bodytext</body>
    </appointment>
    <appointment>
        <starttime>2009-06-01T17:00:00</starttime>
        <endtime>2009-06-01T18:15:00</endtime>
        <subject>This is a third Test-Appointment</subject>
        <location>At your Desk</location>
        <body>Here is the Bodytext</body>
    </appointment>
</appointments>
```

El método CreateAppointmentsFromXml usa la implementación de Microsoft COM de XML Document Object Model (DOM) para cargar y procesar los datos XML que proporciona xml. CreateAppointmentsFromXml primero comprueba si xml especifica un origen de datos XML válido. Si es así, carga los datos en un documento XML, [DOMDocument](https://msdn.microsoft.com/library/ms756987\(v=office.15\)). En caso contrario, CreateAppointmentsFromXml genera una excepción. Para obtener más información sobre XML DOM, vea [DOM](https://msdn.microsoft.com/library/ms766487\(v=office.15\)).

Para cada nodo secundario de cita delimitado por la etiqueta appointment en los datos XML, CreateAppointmentsFromXml busca etiquetas específicas, usa DOM para extraer los datos y los asigna a las propiedades correspondientes de un objeto **AppointmentItem**: [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)), [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611653\(v=office.15\)), [Location](https://msdn.microsoft.com/library/bb608946\(v=office.15\)) y [Body](https://msdn.microsoft.com/library/bb644880\(v=office.15\)). A continuación, CreateAppointmentsFromXml guarda la cita en el calendario predeterminado.

CreateAppointmentsFromXml usa el método [Add](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.add?view=netframework-4.7.2) de la clase [List\<T\> ](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1?view=netframework-4.7.2) en el espacio de nombres [System.Collections.Generic](https://docs.microsoft.com/dotnet/api/system.collections.generic?view=netframework-4.7.2) para agregar estos objetos AppointmentItem. Cuando el método ha procesado todas las citas de los datos XML, devuelve los objetos AppointmentItem en una matriz.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **Imports** o **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```



```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

A continuación, el ejemplo de código de Visual Basic, seguido por el ejemplo de código de C\#.



```vb
Imports System.IO
Imports System.Xml
Imports Outlook = Microsoft.Office.Interop.Outlook

Namespace OutlookAddIn2
    Class Sample
        Function CreateAppointmentsFromXml(ByVal application As Outlook.Application, _
            ByVal xml As String) As Outlook.AppointmentItem()

            Dim appointments As New List(Of Outlook.AppointmentItem)
            Dim xmlDoc As New XmlDocument()

            ' If xml is an XML string, create the XML document directly.
            If xml.StartsWith("<?xml") Then
                xmlDoc.LoadXml(xml)
            ElseIf (File.Exists(xml)) Then
                xmlDoc.Load(xml)
            Else
                Throw New Exception("The input string is not valid XML data or the specified file doesn't exist.")
            End If


            ' Select all appointment nodes under the root appointments node.
            Dim appointmentNodes As XmlNodeList = xmlDoc.SelectNodes("appointments/appointment")

            For Each appointmentNode As XmlNode In appointmentNodes

                ' Create a new AppointmentItem object.
                Dim newAppointment As Outlook.AppointmentItem = _
                    DirectCast(application.CreateItem(Outlook.OlItemType.olAppointmentItem), _
                    Outlook.AppointmentItem)

                ' Loop over all child nodes, check the node name, and import the data into the appointment fields.

                For Each node As XmlNode In appointmentNode.ChildNodes
                    Select Case (node.Name)

                        Case "starttime"
                            newAppointment.Start = DateTime.Parse(node.InnerText)


                        Case "endtime"
                            newAppointment.End = DateTime.Parse(node.InnerText)


                        Case "subject"
                            newAppointment.Subject = node.InnerText


                        Case "location"
                            newAppointment.Location = node.InnerText


                        Case "body"
                            newAppointment.Body = node.InnerText


                    End Select
                Next

                ' Save the item in the default calendar.
                newAppointment.Save()
                appointments.Add(newAppointment)
            Next

            ' Return an array of new appointments.
            Return appointments.ToArray()
        End Function


    End Class
End Namespace
```



```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Text;
using System.Xml;
using Outlook = Microsoft.Office.Interop.Outlook;

namespace OutlookAddIn1
{
    class Sample
    {
        Outlook.AppointmentItem[] CreateAppointmentsFromXml(Outlook.Application application, 
            string xml)
        {
            // Create a list of appointment objects.
            List<Outlook.AppointmentItem> appointments = new 
                List<Microsoft.Office.Interop.Outlook.AppointmentItem>();
            XmlDocument xmlDoc = new XmlDocument();

            // If xml is an XML string, create the document directly. 
            if (xml.StartsWith("<?xml"))
            {
                xmlDoc.LoadXml(xml);
            }
            else if (File.Exists(xml))
            {
                xmlDoc.Load(xml);
            }
            else
            {
                throw new Exception(
                    "The input string is not valid XML data or the specified file doesn't exist.");
            }

            // Select all appointment nodes under the root appointments node.
            XmlNodeList appointmentNodes = xmlDoc.SelectNodes("appointments/appointment");
            foreach (XmlNode appointmentNode in appointmentNodes)
            {

                // Create a new AppointmentItem object.
                Outlook.AppointmentItem newAppointment = 
                    (Outlook.AppointmentItem)application.CreateItem(Outlook.OlItemType.olAppointmentItem);

                // Loop over all child nodes, check the node name, and import the data into the 
                // appointment fields.
                foreach (XmlNode node in appointmentNode.ChildNodes)
                {
                    switch (node.Name)
                    {

                        case "starttime":
                            newAppointment.Start = DateTime.Parse(node.InnerText);
                            break;

                        case "endtime":
                            newAppointment.End = DateTime.Parse(node.InnerText);
                            break;

                        case "subject":
                            newAppointment.Subject = node.InnerText;
                            break;

                        case "location":
                            newAppointment.Location = node.InnerText;
                            break;

                        case "body":
                            newAppointment.Body = node.InnerText;
                            break;

                    }
                }

                // Save the item in the default calendar.
                newAppointment.Save();
                appointments.Add(newAppointment);
            }

            // Return an array of new appointments.
            return appointments.ToArray();
        }

    }
}
```

## <a name="see-also"></a>Vea también

- [Citas](appointments.md)

