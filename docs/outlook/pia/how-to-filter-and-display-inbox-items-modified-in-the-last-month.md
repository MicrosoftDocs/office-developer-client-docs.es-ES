---
title: Filtrar y mostrar los elementos de la bandeja de entrada modificados en el último mes
TOCTitle: Filter and display Inbox items modified in the last month
ms:assetid: ef6004dc-0b5a-4d1f-8937-1384d1dfc1ca
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424482(v=office.15)
ms:contentKeyID: 55119886
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 952d28cc64ffa3638f8147b665e88a372dc81848
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406879"
---
# <a name="filter-and-display-inbox-items-modified-in-the-last-month"></a><span data-ttu-id="8d94e-102">Filtrar y mostrar los elementos de la bandeja de entrada modificados en el último mes</span><span class="sxs-lookup"><span data-stu-id="8d94e-102">This example shows how to filter and display Inbox items that were modified in the last month.</span></span>

<span data-ttu-id="8d94e-103">En este ejemplo, se muestra cómo filtrar y mostrar elementos de la Bandeja de entrada modificados en el último mes.</span><span class="sxs-lookup"><span data-stu-id="8d94e-103">This example shows how to filter and display Inbox items that were modified in the last month.</span></span>

## <a name="example"></a><span data-ttu-id="8d94e-104">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8d94e-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="8d94e-105">El siguiente ejemplo de código es un fragmento de [Aplicaciones de programación para Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="8d94e-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="8d94e-106">El lenguaje de consulta búsqueda y ubicación DAV (DASL) se basa en la implementación de este lenguaje por parte de Microsoft Exchange en Outlook.</span><span class="sxs-lookup"><span data-stu-id="8d94e-106">DAV Search and Locating (DASL) query language is based on the Microsoft Exchange implementation of DASL in Outlook. DASL can be used to return results in the Table object.</span></span> <span data-ttu-id="8d94e-107">Se puede usar para devolver resultados basados en la propiedad para búsquedas de nivel de elemento en los datos de carpeta, como los representados por un objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="8d94e-107">It can be used to return property-based results for item-level searches in folder data, such as that represented by a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object.</span></span> <span data-ttu-id="8d94e-108">Los filtros DASL admiten comparaciones de cadenas, como equivalencias, prefijos, frases y coincidencias de subcadenas, mediante el operador igual (=).</span><span class="sxs-lookup"><span data-stu-id="8d94e-108">DASL filters support string comparisons, including equivalence, prefix, phrase, and substring matching, by using the equal (=) operator.</span></span> <span data-ttu-id="8d94e-109">Puede usar las consultas DASL para realizar la comparación y filtrado de fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="8d94e-109">You can use DASL queries to perform date-time comparison and filtering.</span></span>

<span data-ttu-id="8d94e-110">Puesto que las consultas DASL siempre realizan comparaciones **DateTime** en hora universal coordinada (UTC), debe convertir el valor de hora local a UTC si quiere que la consulta funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="8d94e-110">Because DASL queries always perform **DateTime** comparisons in Coordinated Universal Time (UTC), you must convert the local time value to UTC if you want the query to operate correctly.</span></span> <span data-ttu-id="8d94e-111">También es necesario convertir el valor **DateTime** a representación de cadena porque los filtros DASL filtros soportan la comparación de cadenas.</span><span class="sxs-lookup"><span data-stu-id="8d94e-111">You must also convert the **DateTime** value to a string representation because DASL filters support string comparisons.</span></span> <span data-ttu-id="8d94e-112">Puede hacer la conversión de **DateTime** de dos maneras: utilizando el método [LocalTimeToUTC(Object)](https://msdn.microsoft.com/library/bb645832\(v=office.15\)) del objeto [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)), o usando las macros **DateTime** de Outlook para realizar la conversión.</span><span class="sxs-lookup"><span data-stu-id="8d94e-112">You can make the **DateTime** conversion in two ways: by using the [LocalTimeToUTC(Object)](https://msdn.microsoft.com/library/bb645832\(v=office.15\)) method of the [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) object, or by using Outlook **DateTime** macros to make the conversion.</span></span>

<span data-ttu-id="8d94e-113">La línea de código siguiente muestra cómo usar el método **LocalTimeToUTC** para convertir el valor de la propiedad **LastModificationTime** (que es una columna predeterminada de todos los objetos **Item**) a la hora UTC. </span><span class="sxs-lookup"><span data-stu-id="8d94e-113">The following line of code shows how to use the **LocalTimeToUTC** method to convert the value of the **LastModificationTime** property (which is a default column in all **Item** objects) to UTC.</span></span>

```csharp
DateTime modified = nextRow.LocalTimeUTC(“LastModificationTime”);
```

<span data-ttu-id="8d94e-p103">En la tabla siguiente se enumeran las macros **DateTime** que puede usar para devolver cadenas filtradas que comparan el valor de una propiedad **DateTime** determinada con una fecha relativa especificada o un intervalo de fechas en UTC. El valor de la propiedad SchemaName representa cualquier propiedad **DateTime** válida a la que hace referencia un espacio de nombres. </span><span class="sxs-lookup"><span data-stu-id="8d94e-p103">The following table lists the **DateTime** macros you can use to return filtered strings that compare the value of a given **DateTime** property with a specified relative date or date range in UTC. The SchemaName property value represents any valid **DateTime** property referenced by namespace.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d94e-116">Macro</span><span class="sxs-lookup"><span data-stu-id="8d94e-116">Macro</span></span></p></th>
<th><p><span data-ttu-id="8d94e-117">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d94e-117">Syntax</span></span></p></th>
<th><p><span data-ttu-id="8d94e-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d94e-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d94e-119">hoy</span><span class="sxs-lookup"><span data-stu-id="8d94e-119">today</span></span></p></td>
<td><p><span data-ttu-id="8d94e-120">%today(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="8d94e-120">%today(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="8d94e-121">Restringe los elementos cuyos valores de la propiedad SchemaName son equivalentes a hoy.</span><span class="sxs-lookup"><span data-stu-id="8d94e-121">Restricts for items with a SchemaName property value equal to today.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d94e-122">tomorrow</span><span class="sxs-lookup"><span data-stu-id="8d94e-122">tomorrow</span></span></p></td>
<td><p><span data-ttu-id="8d94e-123">%tomorrow(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="8d94e-123">%tomorrow(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="8d94e-124">Restringe los elementos cuyos valores de la propiedad SchemaName son equivalentes a mañana.</span><span class="sxs-lookup"><span data-stu-id="8d94e-124">Restricts for items with a SchemaName property value equal to tomorrow.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d94e-125">yesterday</span><span class="sxs-lookup"><span data-stu-id="8d94e-125">yesterday</span></span></p></td>
<td><p><span data-ttu-id="8d94e-126">%yesterday(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="8d94e-126">%yesterday(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="8d94e-127">Restringe los elementos cuyos valores de la propiedad SchemaName son equivalentes a ayer.</span><span class="sxs-lookup"><span data-stu-id="8d94e-127">Restricts for items with a SchemaName property value equal to yesterday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d94e-128">next7days</span><span class="sxs-lookup"><span data-stu-id="8d94e-128">next7days</span></span></p></td>
<td><p><span data-ttu-id="8d94e-129">%next7days(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="8d94e-129">%next7days(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="8d94e-130">Restringe los elementos cuyos valores de la propiedad SchemaName están en un intervalo equivalente a los próximos siete días.</span><span class="sxs-lookup"><span data-stu-id="8d94e-130">Restricts for items with SchemaName property values in a range equivalent to the next seven days.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d94e-131">last7days</span><span class="sxs-lookup"><span data-stu-id="8d94e-131">last7days</span></span></p></td>
<td><p><span data-ttu-id="8d94e-132">%last7days(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="8d94e-132">%last7days(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="8d94e-133">Restringe los elementos cuyos valores de la propiedad SchemaName están en un intervalo equivalente a los últimos siete días.</span><span class="sxs-lookup"><span data-stu-id="8d94e-133">Restricts for items with SchemaName property values in a range equivalent to the last seven days.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d94e-134">nextweek</span><span class="sxs-lookup"><span data-stu-id="8d94e-134">nextweek</span></span></p></td>
<td><p><span data-ttu-id="8d94e-135">%nextweek(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="8d94e-135">%nextweek(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="8d94e-136">Restringe los elementos cuyos valores de la propiedad SchemaName están en un intervalo equivalente a la semana próxima.</span><span class="sxs-lookup"><span data-stu-id="8d94e-136">Restricts for items with SchemaName property values in a range equivalent to next week.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d94e-137">thisweek</span><span class="sxs-lookup"><span data-stu-id="8d94e-137">thisweek</span></span></p></td>
<td><p><span data-ttu-id="8d94e-138">%thisweek(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="8d94e-138">%thisweek(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="8d94e-139">Restringe los elementos cuyos valores de la propiedad SchemaName están en un intervalo equivalente a la semana actual.</span><span class="sxs-lookup"><span data-stu-id="8d94e-139">Restricts for items with SchemaName property values in a range equivalent to this week.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d94e-140">lastweek</span><span class="sxs-lookup"><span data-stu-id="8d94e-140">lastweek</span></span></p></td>
<td><p><span data-ttu-id="8d94e-141">%lastweek(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="8d94e-141">%lastweek(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="8d94e-142">Restringe los elementos cuyos valores de la propiedad SchemaName están en un intervalo equivalente a la semana pasada.</span><span class="sxs-lookup"><span data-stu-id="8d94e-142">Restricts for items with SchemaName property values in a range equivalent to last week.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d94e-143">nextmonth</span><span class="sxs-lookup"><span data-stu-id="8d94e-143">nextmonth</span></span></p></td>
<td><p><span data-ttu-id="8d94e-144">% nextmonth("SchemaName") %</span><span class="sxs-lookup"><span data-stu-id="8d94e-144">%nextmonth(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="8d94e-145">Restringe los elementos cuyos valores de la propiedad SchemaName están en un intervalo equivalente al mes próximo.</span><span class="sxs-lookup"><span data-stu-id="8d94e-145">Restricts for items with SchemaName property values in a range equivalent to next month.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d94e-146">thismonth</span><span class="sxs-lookup"><span data-stu-id="8d94e-146">thismonth</span></span></p></td>
<td><p><span data-ttu-id="8d94e-147">% thismonth("SchemaName") %</span><span class="sxs-lookup"><span data-stu-id="8d94e-147">%thismonth(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="8d94e-148">Restringe los elementos cuyos valores de la propiedad SchemaName están en un intervalo equivalente al mes actual.</span><span class="sxs-lookup"><span data-stu-id="8d94e-148">Restricts for items with SchemaName property values in a   range equivalent to this month.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d94e-149">lastmonth</span><span class="sxs-lookup"><span data-stu-id="8d94e-149">lastmonth</span></span></p></td>
<td><p><span data-ttu-id="8d94e-150">% lastmonth("SchemaName") %</span><span class="sxs-lookup"><span data-stu-id="8d94e-150">%lastmonth(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="8d94e-151">Restringe los elementos cuyos valores de la propiedad SchemaName están en un intervalo equivalente al mes pasado.</span><span class="sxs-lookup"><span data-stu-id="8d94e-151">Restricts for items with SchemaName property values in a range equivalent to last month.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8d94e-152">En el siguiente ejemplo, DemoDASLDateMacro crea una consulta DASL que usa la macro **lastmonthDateTime** para filtrar los elementos de la bandeja de entrada del usuario modificados en el último mes.</span><span class="sxs-lookup"><span data-stu-id="8d94e-152">In the following example, DemoDASLDateMacro creates a DASL query that uses the **lastmonth**DateTime macro to filter for items in the user’s Inbox that were modified in the last month. It then creates a Table object with that filter, and enumerates and displays the rows in the restricted Table object.</span></span> <span data-ttu-id="8d94e-153">A continuación crea un objeto **Table** con el filtro, y enumera y muestra las filas en el objeto restringido **Table**.</span><span class="sxs-lookup"><span data-stu-id="8d94e-153">It then creates a **Table** object with that filter, and enumerates and displays the rows in the restricted **Table** object.</span></span>

<span data-ttu-id="8d94e-154">Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="8d94e-154">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="8d94e-155">La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública.</span><span class="sxs-lookup"><span data-stu-id="8d94e-155">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="8d94e-156">La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.</span><span class="sxs-lookup"><span data-stu-id="8d94e-156">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoDASLDateMacro()
{
    string filter = "@SQL=" + "%lastmonth(" + "\"" +
        "DAV:getlastmodified" + "\"" + ")%";
    Outlook.Table table = Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).GetTable(
        filter, Outlook.OlTableContents.olUserItems);
    while (!table.EndOfTable)
    {
        Outlook.Row row = table.GetNextRow();
        Debug.WriteLine(row["Subject"]);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="8d94e-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d94e-157">See also</span></span>

- [<span data-ttu-id="8d94e-158">Buscar y filtrar</span><span class="sxs-lookup"><span data-stu-id="8d94e-158">Search and Filter</span></span>](search-and-filter.md)
