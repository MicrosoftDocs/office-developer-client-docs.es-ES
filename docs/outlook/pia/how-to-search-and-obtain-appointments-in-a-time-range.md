---
title: Buscar y obtener citas de un intervalo de tiempo
TOCTitle: Search and obtain appointments in a time range
ms:assetid: ce5205ad-6967-4f21-8a9d-503b731dbd40
ms:mtpsurl: https://msdn.microsoft.com/library/Gg619398(v=office.15)
ms:contentKeyID: 55119927
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9088da5f2deb4b3d4ccb1c2bc5409e0ff280ed24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316096"
---
# <a name="search-and-obtain-appointments-in-a-time-range"></a><span data-ttu-id="3bc08-102">Buscar y obtener citas de un intervalo de tiempo</span><span class="sxs-lookup"><span data-stu-id="3bc08-102">Search and obtain appointments in a time range</span></span>

<span data-ttu-id="3bc08-103">En este ejemplo se devuelven citas de un intervalo de tiempo específico del calendario predeterminado de Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="3bc08-103">This example returns appointments in a specific time range in the default Microsoft Outlook calendar.</span></span>

## <a name="example"></a><span data-ttu-id="3bc08-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3bc08-104">Example</span></span>

<span data-ttu-id="3bc08-105">Este ejemplo de código contiene dos métodos: DemoAppointmentsInRange y GetAppointmentsInRange.</span><span class="sxs-lookup"><span data-stu-id="3bc08-105">This code example contains two methods: DemoAppointmentsInRange and GetAppointmentsInRange.</span></span> <span data-ttu-id="3bc08-106">DemoAppointmentsInRange obtiene el calendario predeterminado del perfil de Outlook que haya iniciado sesión en ese momento, establece un intervalo de fechas de 5 días desde las 12:00 A. M.</span><span class="sxs-lookup"><span data-stu-id="3bc08-106">DemoAppointmentsInRange obtains the default calendar for the current signed-in Outlook profile, sets a date range of 5 days from 12:00 A.M.</span></span> <span data-ttu-id="3bc08-107">de hoy, llama a GetAppointmentsInRange para obtener las citas que se encuentren en ese intervalo de tiempo, y muestra el asunto y la hora de inicio de cada una de las citas devueltas.</span><span class="sxs-lookup"><span data-stu-id="3bc08-107">today, calls GetAppointmentsInRange to obtain appointments that fall in that time range, and displays the subject and start time of each of the returned appointments.</span></span>

<span data-ttu-id="3bc08-108">GetAppointmentsInRange acepta una carpeta de Outlook y los valores de inicio y finalización de **DateTime** del intervalo de tiempo como parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="3bc08-108">GetAppointmentsInRange accepts an Outlook folder, and the start and end **DateTime** values of the time range as input parameters.</span></span> <span data-ttu-id="3bc08-109">Este método usa el método [Restrict(String)](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) y un filtro de cadena en formato Jet que devuelve las citas que empiezan y finalizan en ese intervalo de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="3bc08-109">This method uses the [Restrict(String)](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) method and a string filter in Jet format that returns appointments that start and end within the specified time range.</span></span> <span data-ttu-id="3bc08-110">Suponiendo que \[Start\] y \[End\] son la hora de inicio y la hora de finalización de una cita, y startTime y endTime son la hora de inicio o finalización del intervalo de tiempo especificado, GetAppointmentsInRange configura un filtro que busca citas con `[Start]>=startTime` y `[End]<=endTime`.</span><span class="sxs-lookup"><span data-stu-id="3bc08-110">Assuming \[Start\] and \[End\] are the start time and end time of an appointment, and startTime and endTime are the beginning and end time of the specified time range, GetAppointmentsInRange sets up a filter  that looks for appointments with `[Start]>=startTime`, and `[End]<=endTime`.</span></span> <span data-ttu-id="3bc08-111">El código siguiente muestra el filtro Jet en C\#.</span><span class="sxs-lookup"><span data-stu-id="3bc08-111">The following code shows the Jet filter in C\#.</span></span>

```csharp
string filter = "[Start] >= '"
    + startTime.ToString("g")
    + "' AND [End] <= '"
    + endTime.ToString("g") + "'";
```

<span data-ttu-id="3bc08-112">Antes de llamar al método **Items.Restrict** para buscar citas, GetAppointmentsInRange hace otras dos cosas para incluir las citas periódicas que se producen en el intervalo de tiempo especificado:</span><span class="sxs-lookup"><span data-stu-id="3bc08-112">Before calling the **Items.Restrict** method to search for appointments, GetAppointmentsInRange does two other things to include recurring appointments that occur in the specified time range:</span></span>

- <span data-ttu-id="3bc08-113">Establece la propiedad [IncludeRecurrences](https://msdn.microsoft.com/library/bb646522\(v=office.15\)) de la colección [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="3bc08-113">Sets the [IncludeRecurrences](https://msdn.microsoft.com/library/bb646522\(v=office.15\)) property of the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) collection.</span></span>

- <span data-ttu-id="3bc08-114">Ordena los elementos de cita en la carpeta de calendario determinada por la propiedad [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="3bc08-114">Sorts the appointment items in the given calendar folder by the [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) property.</span></span>

<span data-ttu-id="3bc08-115">De manera alternativa, si también está interesado en las citas que se superponen parcialmente o por completo con el intervalo de tiempo especificado, debe especificar un filtro diferente para devolver otros tipos de citas (como se muestra en la figura 1):</span><span class="sxs-lookup"><span data-stu-id="3bc08-115">Alternatively, if you are also interested in appointments that overlap partially or entirely with the specified time range, you would specify a different filter to return additional types of appointments (as shown in Figure 1):</span></span>

- <span data-ttu-id="3bc08-116">Citas que comienzan y finalizan en el intervalo de tiempo especificado (por ejemplo, cita A):</span><span class="sxs-lookup"><span data-stu-id="3bc08-116">Appointments that start and end within the specified time range (for example, appointment A):</span></span><br/><br/>`[Start]>=startTime and [End]<=endTime`

- <span data-ttu-id="3bc08-117">Citas que comienzan antes del intervalo de tiempo especificado, pero finalizan en el intervalo de tiempo especificado (por ejemplo, cita B):</span><span class="sxs-lookup"><span data-stu-id="3bc08-117">Appointments that start before the specified time range but end within the time range (for example, appointment B):</span></span><br/><br/>`[Start]<startTime and [End]<=endTime`

- <span data-ttu-id="3bc08-118">Citas que comienzan en el intervalo de tiempo especificado, pero finalizan después del intervalo de tiempo especificado (por ejemplo, cita C):</span><span class="sxs-lookup"><span data-stu-id="3bc08-118">Appointments that start within the specified time range but end after the time range (for example, appointment C):</span></span><br/><br/>`[Start]>=startTime and [End]>endTime`

- <span data-ttu-id="3bc08-119">Citas que comienzan antes del intervalo de tiempo especificado y finalizan después del intervalo de tiempo especificado (por ejemplo, cita D):</span><span class="sxs-lookup"><span data-stu-id="3bc08-119">Appointments that start before the specified time range and end after the time range (for example, appointment D):</span></span><br/><br/>`[Start]<startTime and [End]>endTime`

<span data-ttu-id="3bc08-120">**Figura 1. Tipos de citas que se producen en un intervalo de tiempo o se superponen con ese intervalo de tiempo**</span><span class="sxs-lookup"><span data-stu-id="3bc08-120">**Figure 1. Types of appointments that occur within a time range, or overlap with that time range**</span></span>

![Tipos de citas que se producen en un intervalo de tiempo o se superponen con ese intervalo de tiempo.](media/pia-appointment-starttime-endtime.gif)
 

<span data-ttu-id="3bc08-122">Como en cualquier intervalo de tiempo `startTime<=endTime`, un filtro con `[Start]<=endTime` y `[End]>=startTime` capturaría los tipos de citas anteriores en ese intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3bc08-122">Because in any time range `startTime<=endTime`, a filter with `[Start]<=endTime` and `[End]>=startTime` would capture the preceding types of appointments in that time range.</span></span>

<span data-ttu-id="3bc08-123">En C\#, puede expresar el filtro Jet de la manera siguiente.</span><span class="sxs-lookup"><span data-stu-id="3bc08-123">In C\#, you can express the Jet filter as follows.</span></span>

```csharp
string filter = "[Start] <= '"
    + endTime.ToString("g")
    + "' AND [End] >= '"
    + startTime.ToString("g") + "'";
```

<span data-ttu-id="3bc08-124">El siguiente código muestra el ejemplo completo.</span><span class="sxs-lookup"><span data-stu-id="3bc08-124">The following code shows the complete example.</span></span> <span data-ttu-id="3bc08-125">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="3bc08-125">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="3bc08-126">La instrucción **Imports** o **using** no deben producirse directamente antes de las funciones en el ejemplo de código, pero deben agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="3bc08-126">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="3bc08-127">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en Visual Basic y C\#.</span><span class="sxs-lookup"><span data-stu-id="3bc08-127">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoAppointmentsInRange()
{
    Outlook.Folder calFolder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderCalendar)
        as Outlook.Folder;
    DateTime start = DateTime.Now;
    DateTime end = start.AddDays(5);
    Outlook.Items rangeAppts = GetAppointmentsInRange(calFolder, start, end);
    if (rangeAppts != null)
    {
        foreach (Outlook.AppointmentItem appt in rangeAppts)
        {
            Debug.WriteLine("Subject: " + appt.Subject 
                + " Start: " + appt.Start.ToString("g"));
        }
    }
}

/// <summary>
/// Get recurring appointments in date range.
/// </summary>
/// <param name="folder"></param>
/// <param name="startTime"></param>
/// <param name="endTime"></param>
/// <returns>Outlook.Items</returns>
private Outlook.Items GetAppointmentsInRange(
    Outlook.Folder folder, DateTime startTime, DateTime endTime)
{
    string filter = "[Start] >= '"
        + startTime.ToString("g")
        + "' AND [End] <= '"
        + endTime.ToString("g") + "'";
    Debug.WriteLine(filter);
    try
    {
        Outlook.Items calItems = folder.Items;
        calItems.IncludeRecurrences = true;
        calItems.Sort("[Start]", Type.Missing);
        Outlook.Items restrictItems = calItems.Restrict(filter);
        if (restrictItems.Count > 0)
        {
            return restrictItems;
        }
        else
        {
            return null;
        }
    }
    catch { return null; }
}
```

## <a name="see-also"></a><span data-ttu-id="3bc08-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="3bc08-128">See also</span></span>

- <span data-ttu-id="3bc08-129">[Search and filter](search-and-filter.md) (Buscar y filtrar)</span><span class="sxs-lookup"><span data-stu-id="3bc08-129">[Search and filter](search-and-filter.md)</span></span>

