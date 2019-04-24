---
title: Filtrar y mostrar los elementos de la bandeja de entrada modificados en el último mes
TOCTitle: Filter and display Inbox items modified in the last month
ms:assetid: ef6004dc-0b5a-4d1f-8937-1384d1dfc1ca
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424482(v=office.15)
ms:contentKeyID: 55119886
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77fe6e7df4cf67ed1ca2d62b8cf48f1b2873ccbe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320297"
---
# <a name="filter-and-display-inbox-items-modified-in-the-last-month"></a>Filtrar y mostrar los elementos de la bandeja de entrada modificados en el último mes

En este ejemplo, se muestra cómo filtrar y mostrar elementos de la Bandeja de entrada modificados en el último mes.

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Aplicaciones de programación para Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

El lenguaje de consulta búsqueda y ubicación DAV (DASL) se basa en la implementación de este lenguaje por parte de Microsoft Exchange en Outlook. Se puede usar para devolver resultados basados en la propiedad para búsquedas de nivel de elemento en los datos de carpeta, como los representados por un objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)). Los filtros DASL admiten comparaciones de cadenas, como equivalencias, prefijos, frases y coincidencias de subcadenas, mediante el operador igual (=). Puede usar las consultas DASL para realizar la comparación y filtrado de fecha y hora.

Puesto que las consultas DASL siempre realizan comparaciones **DateTime** en hora universal coordinada (UTC), debe convertir el valor de hora local a UTC si quiere que la consulta funcione correctamente. También es necesario convertir el valor **DateTime** a representación de cadena porque los filtros DASL filtros soportan la comparación de cadenas. Puede hacer la conversión de **DateTime** de dos maneras: utilizando el método [LocalTimeToUTC(Object)](https://msdn.microsoft.com/library/bb645832\(v=office.15\)) del objeto [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)), o usando las macros **DateTime** de Outlook para realizar la conversión.

La línea de código siguiente muestra cómo usar el método **LocalTimeToUTC** para convertir el valor de la propiedad **LastModificationTime** (que es una columna predeterminada de todos los objetos **Item**) a la hora UTC. 

```csharp
DateTime modified = nextRow.LocalTimeUTC(“LastModificationTime”);
```

En la tabla siguiente se enumeran las macros **DateTime** que puede usar para devolver cadenas filtradas que comparan el valor de una propiedad **DateTime** determinada con una fecha relativa especificada o un intervalo de fechas en UTC. El valor de la propiedad SchemaName representa cualquier propiedad **DateTime** válida a la que hace referencia un espacio de nombres. 

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Macro</p></th>
<th><p>Sintaxis</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>hoy</p></td>
<td><p>%today(“SchemaName”)%</p></td>
<td><p>Restringe los elementos cuyos valores de la propiedad SchemaName son equivalentes a hoy.</p></td>
</tr>
<tr class="even">
<td><p>tomorrow</p></td>
<td><p>%tomorrow(“SchemaName”)%</p></td>
<td><p>Restringe los elementos cuyos valores de la propiedad SchemaName son equivalentes a mañana.</p></td>
</tr>
<tr class="odd">
<td><p>yesterday</p></td>
<td><p>%yesterday(“SchemaName”)%</p></td>
<td><p>Restringe los elementos cuyos valores de la propiedad SchemaName son equivalentes a ayer.</p></td>
</tr>
<tr class="even">
<td><p>next7days</p></td>
<td><p>%next7days(“SchemaName”)%</p></td>
<td><p>Restringe los elementos cuyos valores de la propiedad SchemaName están en un intervalo equivalente a los próximos siete días.</p></td>
</tr>
<tr class="odd">
<td><p>last7days</p></td>
<td><p>%last7days(“SchemaName”)%</p></td>
<td><p>Restringe los elementos cuyos valores de la propiedad SchemaName están en un intervalo equivalente a los últimos siete días.</p></td>
</tr>
<tr class="even">
<td><p>nextweek</p></td>
<td><p>%nextweek(“SchemaName”)%</p></td>
<td><p>Restringe los elementos cuyos valores de la propiedad SchemaName están en un intervalo equivalente a la semana próxima.</p></td>
</tr>
<tr class="odd">
<td><p>thisweek</p></td>
<td><p>%thisweek(“SchemaName”)%</p></td>
<td><p>Restringe los elementos cuyos valores de la propiedad SchemaName están en un intervalo equivalente a la semana actual.</p></td>
</tr>
<tr class="even">
<td><p>lastweek</p></td>
<td><p>%lastweek(“SchemaName”)%</p></td>
<td><p>Restringe los elementos cuyos valores de la propiedad SchemaName están en un intervalo equivalente a la semana pasada.</p></td>
</tr>
<tr class="odd">
<td><p>nextmonth</p></td>
<td><p>% nextmonth("SchemaName") %</p></td>
<td><p>Restringe los elementos cuyos valores de la propiedad SchemaName están en un intervalo equivalente al mes próximo.</p></td>
</tr>
<tr class="even">
<td><p>thismonth</p></td>
<td><p>% thismonth("SchemaName") %</p></td>
<td><p>Restringe los elementos cuyos valores de la propiedad SchemaName están en un intervalo equivalente al mes actual.</p></td>
</tr>
<tr class="odd">
<td><p>lastmonth</p></td>
<td><p>% lastmonth("SchemaName") %</p></td>
<td><p>Restringe los elementos cuyos valores de la propiedad SchemaName están en un intervalo equivalente al mes pasado.</p></td>
</tr>
</tbody>
</table>


En el siguiente ejemplo, DemoDASLDateMacro crea una consulta DASL que usa la macro **lastmonthDateTime** para filtrar los elementos de la bandeja de entrada del usuario modificados en el último mes. A continuación crea un objeto **Table** con el filtro, y enumera y muestra las filas en el objeto restringido **Table**.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

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

## <a name="see-also"></a>Vea también

- [Search and filter](search-and-filter.md) (Buscar y filtrar)

