---
title: Crear una cita que comience en la zona horaria del Pacífico y finalice en la zona horaria oriental
TOCTitle: Create an appointment that starts in the Pacific Time Zone and ends in the Eastern Time Zone
ms:assetid: ba19532b-df31-4384-8816-e64e6eecbe53
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623388(v=office.15)
ms:contentKeyID: 55119808
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e9a1b9d5f65d8683c08821d4cf0851f599f32030
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698718"
---
# <a name="create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone"></a><span data-ttu-id="71742-102">Crear una cita que comience en la zona horaria del Pacífico y finalice en la zona horaria oriental</span><span class="sxs-lookup"><span data-stu-id="71742-102">Create an appointment that starts in the Pacific Time Zone and ends in the Eastern Time Zone</span></span>

<span data-ttu-id="71742-p101">En ocasiones, una cita puede abarcar un período de tiempo durante el cual es posible que el usuario haya viajado a una zona horaria diferente que cuando comenzó la cita. En este ejemplo se crea una cita que comienza en la zona Hora del Pacífico (UCT-8:00) y finaliza en la zona Hora oriental (UCT-5:30).</span><span class="sxs-lookup"><span data-stu-id="71742-p101">Occasionally, an appointment may span over a period of time during which the user may have traveled to a different time zone than when the appointment starts. This example creates an appointment that begins in the Pacific Time Zone (UTC-8) and ends in the Eastern Time Zone (UTC-5).</span></span>

## <a name="example"></a><span data-ttu-id="71742-105">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="71742-105">Example</span></span>

<span data-ttu-id="71742-106">Este ejemplo de código usa el objeto [TimeZones](https://msdn.microsoft.com/library/bb611081\(v=office.15\)), que representa las zonas horarias reconocidas en Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="71742-106">This code sample uses the [TimeZones](https://msdn.microsoft.com/library/bb611081\(v=office.15\)) object that represents all the time zones recognized in Microsoft Windows.</span></span> <span data-ttu-id="71742-107">También usa el objeto [TimeZone](https://msdn.microsoft.com/library/bb646259\(v=office.15\)) para establecer u obtener la propiedad [StartTimeZone](https://msdn.microsoft.com/library/bb623657\(v=office.15\)) y la propiedad [EndTimeZone](https://msdn.microsoft.com/library/bb612198\(v=office.15\)) en el objeto [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="71742-107">It also uses the [TimeZone](https://msdn.microsoft.com/library/bb646259\(v=office.15\)) object to set or get the [StartTimeZone](https://msdn.microsoft.com/library/bb623657\(v=office.15\)) property and the [EndTimeZone](https://msdn.microsoft.com/library/bb612198\(v=office.15\)) property on the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span>

<span data-ttu-id="71742-108">Outlook muestra todas las fechas en hora local, que se expresa en la zona horaria actual del usuario, controlada por la configuración del usuario en el Panel de control de Windows.</span><span class="sxs-lookup"><span data-stu-id="71742-108">Outlook displays all dates in local time, which is expressed in the user's current time zone, controlled by the user's settings in the Windows Control Panel.</span></span> <span data-ttu-id="71742-109">Outlook también obtiene o establece otras propiedades, como [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) y [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), en la hora local.</span><span class="sxs-lookup"><span data-stu-id="71742-109">Outlook also sets or gets properties, such as [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) and [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), in local time.</span></span> <span data-ttu-id="71742-110">Sin embargo, Outlook almacena los valores de fecha y hora en la hora del Pacífico (UTC) en lugar de la hora local.</span><span class="sxs-lookup"><span data-stu-id="71742-110">However, Outlook stores date and time values as Coordinated Universal Time (UTC) rather than local time.</span></span> <span data-ttu-id="71742-111">Si examina el valor interno de Appointment.Start mediante el objeto [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)), verá que el valor interno de fecha y hora es igual que el valor local de fecha y hora convertido al valor equivalente de fecha y hora UTC.</span><span class="sxs-lookup"><span data-stu-id="71742-111">If you examine the internal value of Appointment.Start by using the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object, you would find the internal date and time value is equal to the local date and time value converted to the equivalent UTC date and time value.</span></span>

<span data-ttu-id="71742-112">Outlook usa la información de zona horaria para asignar la cita a la hora UTC correcta cuando guarda una cita, y a la hora local correcta cuando muestra el elemento en el calendario.</span><span class="sxs-lookup"><span data-stu-id="71742-112">Outlook uses the time zone information to map the appointment to the correct UTC time when it saves an appointment, and into the correct local time when it displays the item in the calendar.</span></span> <span data-ttu-id="71742-113">La modificación de la propiedad StartTimeZone afecta al valor de Appointment.Start, que siempre se expresa en la zona horaria local, representada por la propiedad [CurrentTimeZone](https://msdn.microsoft.com/library/bb612024\(v=office.15\)) del objeto devuelto por [TimeZones](https://msdn.microsoft.com/library/bb645170\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="71742-113">Changing StartTimeZone affects the value of Appointment.Start, which is always expressed in the local time zone, represented by the [CurrentTimeZone](https://msdn.microsoft.com/library/bb612024\(v=office.15\)) property of the object returned by [TimeZones](https://msdn.microsoft.com/library/bb645170\(v=office.15\)).</span></span> <span data-ttu-id="71742-114">De forma similar, la modificación de la propiedad EndTimeZone afecta al valor de Appointment.End, que siempre se expresa en la zona horaria local, representada por la propiedad CurrentTimeZone del objeto devuelto por Application.TimeZones.</span><span class="sxs-lookup"><span data-stu-id="71742-114">Similarly, changing EndTimeZone affects the value of Appointment.End, which is always expressed in the local time zone, represented by the CurrentTimeZone property of the object returned by Application.TimeZones.</span></span>

<span data-ttu-id="71742-115">Puede recuperar un objeto TimeZone específico del objeto TimeZones usando la clave independiente de TimeZone del registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="71742-115">You can retrieve a specific TimeZone from the TimeZones object by using the locale-independent key for the TimeZone in the Windows registry.</span></span> <span data-ttu-id="71742-116">Las claves independientes de TimeZone se muestran en la siguiente clave: `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\TimeZones`.</span><span class="sxs-lookup"><span data-stu-id="71742-116">Locale-independent TimeZone keys are listed under the following key: `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\TimeZones`.</span></span>

<span data-ttu-id="71742-117">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="71742-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="71742-118">La instrucción **Imports** o **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="71742-118">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="71742-119">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.</span><span class="sxs-lookup"><span data-stu-id="71742-119">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```



```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```



```vb
Private Sub TimeZoneExample()
    Dim appt As Outlook.AppointmentItem = _
        CType(Application.CreateItem( _
        Outlook.OlItemType.olAppointmentItem), Outlook.AppointmentItem)
    Dim tzs As Outlook.TimeZones = Application.TimeZones
    ' Obtain timezone using indexer and locale-independent key
    Dim tzEastern As Outlook.TimeZone = tzs("Eastern Standard Time")
    Dim tzPacific As Outlook.TimeZone = tzs("Pacific Standard Time")
    appt.Subject = "SEA - JFK Flight"
    appt.Start = DateTime.Parse("8/9/2006 8:00 AM")
    appt.StartTimeZone = tzPacific
    appt.End = DateTime.Parse("8/9/2006 5:30 PM")
    appt.EndTimeZone = tzEastern
    appt.Display(False)
End Sub
```



```csharp
private void TimeZoneExample()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    Outlook.TimeZones tzs = Application.TimeZones;
    // Obtain timezone using indexer and locale-independent key
    Outlook.TimeZone tzEastern = tzs["Eastern Standard Time"];
    Outlook.TimeZone tzPacific = tzs["Pacific Standard Time"];
    appt.Subject = "SEA - JFK Flight";
    appt.Start = DateTime.Parse("8/9/2006 8:00 AM");
    appt.StartTimeZone = tzPacific;
    appt.End = DateTime.Parse("8/9/2006 5:30 PM");
    appt.EndTimeZone = tzEastern; 
    appt.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="71742-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="71742-120">See also</span></span>

- [<span data-ttu-id="71742-121">Citas</span><span class="sxs-lookup"><span data-stu-id="71742-121">Appointments</span></span>](appointments.md)

