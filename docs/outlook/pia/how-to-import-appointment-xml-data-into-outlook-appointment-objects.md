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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320065"
---
# <a name="import-appointment-xml-data-into-outlook-appointment-objects"></a><span data-ttu-id="7aa52-102">Importar datos XML de una cita en objetos de citas de Outlook</span><span class="sxs-lookup"><span data-stu-id="7aa52-102">Import appointment XML data into Outlook appointment objects</span></span>

<span data-ttu-id="7aa52-103">En este tema se muestra cómo leer datos de citas con marcado XML, guardar los datos en objetos Outlook [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) del calendario predeterminado y devolver los objetos de citas en una matriz.</span><span class="sxs-lookup"><span data-stu-id="7aa52-103">This topic shows how to read appointment data formatted in XML, save the data to Outlook [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) objects in the default calendar, and return the appointment objects in an array.</span></span>

## <a name="example"></a><span data-ttu-id="7aa52-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7aa52-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="7aa52-105">Helmut Obertanner proporciona los siguientes ejemplos de código.</span><span class="sxs-lookup"><span data-stu-id="7aa52-105">Helmut Obertanner provided the following code examples.</span></span> <span data-ttu-id="7aa52-106">Los conocimientos de Helmut están en Office Developer Tools para Visual Studio y Outlook.</span><span class="sxs-lookup"><span data-stu-id="7aa52-106">Helmut's expertise is in Office Developer Tools for Visual Studio and Outlook.</span></span> 


<span data-ttu-id="7aa52-107">Los ejemplos de código siguientes contienen el método CreateAppointmentsFromXml de la clase Sample, implementado como parte de un proyecto de complemento de Outlook.</span><span class="sxs-lookup"><span data-stu-id="7aa52-107">The following code examples contain the CreateAppointmentsFromXml method of the Sample class, implemented as part of an Outlook add-in project.</span></span> <span data-ttu-id="7aa52-108">Cada proyecto agrega una referencia al ensamblado de interoperabilidad primario de Outlook, que se basa en el espacio de nombres [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="7aa52-108">Each project adds a reference to the Outlook Primary Interop Assembly, which is based on the [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)) namespace.</span></span>

<span data-ttu-id="7aa52-109">El método CreateAppointmentsFromXml acepta dos parámetros de entrada:</span><span class="sxs-lookup"><span data-stu-id="7aa52-109">The CreateAppointmentsFromXml method accepts two input parameters:</span></span>

  - <span data-ttu-id="7aa52-110">application es un objeto [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) de Outlook de confianza.</span><span class="sxs-lookup"><span data-stu-id="7aa52-110">application is a trusted Outlook [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object.</span></span>

  - <span data-ttu-id="7aa52-p103">xml es una cadena XML o una cadena que representa una ruta de acceso a un archivo XML válido. Para el fin de los siguientes ejemplos de código, el código XML delimita los datos de cita mediante las siguientes etiquetas XML:</span><span class="sxs-lookup"><span data-stu-id="7aa52-p103">xml is either an XML string, or a string that represents a path to a valid XML file. For the purpose of the following code examples, the XML delimits appointment data by using the following XML tags:</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="7aa52-113">Datos de la cita</span><span class="sxs-lookup"><span data-stu-id="7aa52-113">Appointment data</span></span></p></th>
    <th><p><span data-ttu-id="7aa52-114">Etiqueta XML delimitadora</span><span class="sxs-lookup"><span data-stu-id="7aa52-114">Delimiting XML tag</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="7aa52-115">Todo el conjunto de datos de la cita</span><span class="sxs-lookup"><span data-stu-id="7aa52-115">Entire set of appointment data</span></span></p></td>
    <td><p><span data-ttu-id="7aa52-116">appointments</span><span class="sxs-lookup"><span data-stu-id="7aa52-116">appointments</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="7aa52-117">Cada cita del conjunto</span><span class="sxs-lookup"><span data-stu-id="7aa52-117">Each appointment in the set</span></span></p></td>
    <td><p><span data-ttu-id="7aa52-118">appointment</span><span class="sxs-lookup"><span data-stu-id="7aa52-118">appointment</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="7aa52-119">Hora de inicio de una cita</span><span class="sxs-lookup"><span data-stu-id="7aa52-119">Start time of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="7aa52-120">starttime</span><span class="sxs-lookup"><span data-stu-id="7aa52-120">starttime</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="7aa52-121">Hora de finalización de una cita</span><span class="sxs-lookup"><span data-stu-id="7aa52-121">End time of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="7aa52-122">endtime</span><span class="sxs-lookup"><span data-stu-id="7aa52-122">endtime</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="7aa52-123">Título de una cita</span><span class="sxs-lookup"><span data-stu-id="7aa52-123">Title of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="7aa52-124">subject</span><span class="sxs-lookup"><span data-stu-id="7aa52-124">subject</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="7aa52-125">Ubicación de una cita</span><span class="sxs-lookup"><span data-stu-id="7aa52-125">Location of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="7aa52-126">location</span><span class="sxs-lookup"><span data-stu-id="7aa52-126">location</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="7aa52-127">Detalles de una cita</span><span class="sxs-lookup"><span data-stu-id="7aa52-127">Details of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="7aa52-128">body</span><span class="sxs-lookup"><span data-stu-id="7aa52-128">body</span></span></p></td>
    </tr>
    </tbody>
    </table>


<span data-ttu-id="7aa52-129">En el ejemplo siguiente se muestran los datos de entrada para el parámetro *xml*.</span><span class="sxs-lookup"><span data-stu-id="7aa52-129">The following example shows input data for the *xml* parameter.</span></span>

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

<span data-ttu-id="7aa52-p104">El método CreateAppointmentsFromXml usa la implementación de Microsoft COM de XML Document Object Model (DOM) para cargar y procesar los datos XML que proporciona xml. CreateAppointmentsFromXml primero comprueba si xml especifica un origen de datos XML válido. Si es así, carga los datos en un documento XML, [DOMDocument](https://msdn.microsoft.com/library/ms756987\(v=office.15\)). En caso contrario, CreateAppointmentsFromXml genera una excepción. Para obtener más información sobre XML DOM, vea [DOM](https://msdn.microsoft.com/library/ms766487\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="7aa52-p104">The CreateAppointmentsFromXml method uses the Microsoft COM implementation of the XML Document Object Model (DOM) to load and process the XML data that xml provides. CreateAppointmentsFromXml first checks whether xml specifies a valid source of XML data. If so, it loads the data into an XML document, [DOMDocument](https://msdn.microsoft.com/library/ms756987\(v=office.15\)). Otherwise, CreateAppointmentsFromXml throws an exception. For more information about the XML DOM, see [DOM](https://msdn.microsoft.com/library/ms766487\(v=office.15\)).</span></span>

<span data-ttu-id="7aa52-135">Para cada nodo secundario de cita delimitado por la etiqueta appointment en los datos XML, CreateAppointmentsFromXml busca etiquetas específicas, usa DOM para extraer los datos y los asigna a las propiedades correspondientes de un objeto **AppointmentItem**: [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)), [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611653\(v=office.15\)), [Location](https://msdn.microsoft.com/library/bb608946\(v=office.15\)) y [Body](https://msdn.microsoft.com/library/bb644880\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="7aa52-135">For each appointment child node delimited by the appointment tag in the XML data, CreateAppointmentsFromXml looks for specific tags, uses the DOM to extract the data, and assigns the data to corresponding properties of an **AppointmentItem** object: [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)), [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611653\(v=office.15\)), [Location](https://msdn.microsoft.com/library/bb608946\(v=office.15\)), and [Body](https://msdn.microsoft.com/library/bb644880\(v=office.15\)).</span></span> <span data-ttu-id="7aa52-136">A continuación, CreateAppointmentsFromXml guarda la cita en el calendario predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7aa52-136">CreateAppointmentsFromXml then saves the appointment to the default calendar.</span></span>

<span data-ttu-id="7aa52-137">CreateAppointmentsFromXml usa el método [Add](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.add?view=netframework-4.7.2) de la clase [List\<T\> ](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1?view=netframework-4.7.2) en el espacio de nombres [System.Collections.Generic](https://docs.microsoft.com/dotnet/api/system.collections.generic?view=netframework-4.7.2) para agregar estos objetos AppointmentItem.</span><span class="sxs-lookup"><span data-stu-id="7aa52-137">CreateAppointmentsFromXml uses the [Add](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.add?view=netframework-4.7.2) method of the [List\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1?view=netframework-4.7.2) class in the [System.Collections.Generic](https://docs.microsoft.com/dotnet/api/system.collections.generic?view=netframework-4.7.2) namespace to aggregate these AppointmentItem objects.</span></span> <span data-ttu-id="7aa52-138">Cuando el método ha procesado todas las citas de los datos XML, devuelve los objetos AppointmentItem en una matriz.</span><span class="sxs-lookup"><span data-stu-id="7aa52-138">When the method has processed all the appointments in the XML data, it returns the AppointmentItem objects in an array.</span></span>

<span data-ttu-id="7aa52-139">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="7aa52-139">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="7aa52-140">La instrucción **Imports** o **using** no deben producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="7aa52-140">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="7aa52-141">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.</span><span class="sxs-lookup"><span data-stu-id="7aa52-141">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```



```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

<span data-ttu-id="7aa52-142">A continuación, el ejemplo de código de Visual Basic, seguido por el ejemplo de código de C\#.</span><span class="sxs-lookup"><span data-stu-id="7aa52-142">The following is the Visual Basic code example, followed by the C\# code example.</span></span>



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

## <a name="see-also"></a><span data-ttu-id="7aa52-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="7aa52-143">See also</span></span>

- [<span data-ttu-id="7aa52-144">Citas</span><span class="sxs-lookup"><span data-stu-id="7aa52-144">Appointments</span></span>](appointments.md)

