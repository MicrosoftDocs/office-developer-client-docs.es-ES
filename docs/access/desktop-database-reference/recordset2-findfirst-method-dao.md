---
title: Método Recordset2.FindFirst (DAO)
TOCTitle: FindFirst Method
ms:assetid: 2a18e81a-a9e5-cc1a-50b2-40c1f1b7fa06
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192064(v=office.15)
ms:contentKeyID: 48543902
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 823a9b0e095bb726d749021cca99d26f1cc8ceba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309411"
---
# <a name="recordset2findfirst-method-dao"></a><span data-ttu-id="eff67-102">Método Recordset2.FindFirst (DAO)</span><span class="sxs-lookup"><span data-stu-id="eff67-102">Recordset2.FindFirst method (DAO)</span></span>

<span data-ttu-id="eff67-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eff67-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eff67-104">Busca el primer registro de un objeto **Recordset** de tipo conjunto de registros dinámicos o de tipo instantánea que cumpla los criterios especificados, y convierte ese registro en el registro actual (solo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="eff67-104">Locates the first record in a dynaset- or snapshot-type **Recordset** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="eff67-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eff67-105">Syntax</span></span>

<span data-ttu-id="eff67-106">*expression* .FindFirst(***Criteria***)</span><span class="sxs-lookup"><span data-stu-id="eff67-106">*expression* .FindFirst(***Criteria***)</span></span>

<span data-ttu-id="eff67-107">*expresión* Variable que representa un **objeto Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="eff67-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="eff67-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="eff67-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eff67-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="eff67-109">Name</span></span></p></th>
<th><p><span data-ttu-id="eff67-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="eff67-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="eff67-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="eff67-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="eff67-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="eff67-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eff67-113"><em>Criterios</em></span><span class="sxs-lookup"><span data-stu-id="eff67-113"><em>Criteria</em></span></span></p></td>
<td><p><span data-ttu-id="eff67-114">Necesario</span><span class="sxs-lookup"><span data-stu-id="eff67-114">Required</span></span></p></td>
<td><p><span data-ttu-id="eff67-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="eff67-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="eff67-p101">Cadena que se utiliza para localizar el registro. Es como una cláusula WHERE en una instrucción SQL pero sin la palabra WHERE.</span><span class="sxs-lookup"><span data-stu-id="eff67-p101">A String used to locate the record. It is like the WHERE clause in an SQL statement, but without the word WHERE.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="eff67-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eff67-118">Remarks</span></span>

<span data-ttu-id="eff67-p102">Si quiere incluir en la búsqueda todos los registros, y no solo los que cumplan una condición determinada, use los métodos **Move** para moverse de un registro a otro. Para buscar un registro en un **Recordset** de tipo tabla, use el método **Seek**.</span><span class="sxs-lookup"><span data-stu-id="eff67-p102">If you want to include all the records in your search — not just those that meet a specific condition — use the **Move** methods to move from record to record. To locate a record in a table-type **Recordset**, use the **Seek** method.</span></span>

<span data-ttu-id="eff67-p103">Si no se encuentra ningún registro que coincida con los criterios, el puntero del registro actual será desconocido y la propiedad **NoMatch** se configurará como **True**. Si el conjunto de registros contiene varios registros que cumplen los criterios, **FindFirst** buscará el primero, **FindNext** buscará el segundo y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="eff67-p103">If a record matching the criteria isn't located, the current record pointer is unknown, and the **NoMatch** property is set to **True**. If recordset contains more than one record that satisfies the criteria, **FindFirst** locates the first occurrence, **FindNext** locates the next occurrence, and so on.</span></span>

<span data-ttu-id="eff67-123">Cada método **Find** empieza a buscar a partir de la ubicación y en la dirección que se especifican en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="eff67-123">Each of the **Find** methods begins its search from the location and in the direction specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eff67-124">Método Find</span><span class="sxs-lookup"><span data-stu-id="eff67-124">Find method</span></span></p></th>
<th><p><span data-ttu-id="eff67-125">Empieza la búsqueda en</span><span class="sxs-lookup"><span data-stu-id="eff67-125">Begins searching at</span></span></p></th>
<th><p><span data-ttu-id="eff67-126">Dirección de búsqueda</span><span class="sxs-lookup"><span data-stu-id="eff67-126">Search direction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eff67-127"><strong>FindFirst</strong></span><span class="sxs-lookup"><span data-stu-id="eff67-127"><strong>FindFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="eff67-128">Principio del conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="eff67-128">Beginning of recordset</span></span></p></td>
<td><p><span data-ttu-id="eff67-129">Final del conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="eff67-129">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff67-130"><strong>FindLast</strong></span><span class="sxs-lookup"><span data-stu-id="eff67-130"><strong>FindLast</strong></span></span></p></td>
<td><p><span data-ttu-id="eff67-131">Final del conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="eff67-131">End of recordset</span></span></p></td>
<td><p><span data-ttu-id="eff67-132">Principio del conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="eff67-132">Beginning of recordset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eff67-133"><strong>FindNext</strong></span><span class="sxs-lookup"><span data-stu-id="eff67-133"><strong>FindNext</strong></span></span></p></td>
<td><p><span data-ttu-id="eff67-134">Registro actual</span><span class="sxs-lookup"><span data-stu-id="eff67-134">Current record</span></span></p></td>
<td><p><span data-ttu-id="eff67-135">Final del conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="eff67-135">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eff67-136"><strong>FindPrevious</strong></span><span class="sxs-lookup"><span data-stu-id="eff67-136"><strong>FindPrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="eff67-137">Registro actual</span><span class="sxs-lookup"><span data-stu-id="eff67-137">Current record</span></span></p></td>
<td><p><span data-ttu-id="eff67-138">Principio del conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="eff67-138">Beginning of recordset</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eff67-p104">No obstante, el uso de uno de los métodos **Find** no es igual a utilizar el método **Move**, que activa simplemente el registro primero, último, siguiente o anterior sin especificar una condición. Puede proseguir una operación Find con una operación Move.</span><span class="sxs-lookup"><span data-stu-id="eff67-p104">Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition. You can follow a Find operation with a Move operation.</span></span>

<span data-ttu-id="eff67-p105">Compruebe siempre el valor de la propiedad **NoMatch** para determinar si la operación Find se ha realizado correctamente. Si la búsqueda es correcta, **NoMatch** es **False**. Si se produce un error, **NoMatch** es **True** y el registro activo no está definido. En este caso, debe colocar de nuevo el puntero de registros activo en un registro válido.</span><span class="sxs-lookup"><span data-stu-id="eff67-p105">Always check the value of the **NoMatch** property to determine whether the Find operation has succeeded. If the search succeeds, **NoMatch** is **False**. If it fails, **NoMatch** is **True** and the current record isn't defined. In this case, you must position the current record pointer back to a valid record.</span></span>

<span data-ttu-id="eff67-p106">Usar los métodos **Find** con conjuntos de registros a los que se accede por ODBC con conexión a un motor de base de datos de Microsoft Access puede resultar ineficiente. Tal vez observe que resulta más rápido reformular los criterios para buscar un determinado registro, especialmente al trabajar con conjuntos de registros de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="eff67-p106">Using the **Find** methods with Microsoft Access database engine-connected ODBC-accessed recordsets can be inefficient. You may find that rephrasing your criteria to locate a specific record is faster, especially when working with large recordsets.</span></span>

<span data-ttu-id="eff67-p107">Al trabajar con grandes objetos **Recordset** de tipo conjunto de registros dinámicos y bases de datos ODBC conectadas a un motor de base de datos de Microsoft Access, puede que compruebe que usar los métodos **Find** o las propiedades **Sort** o **Filter** resulta lento. Para mejorar el rendimiento, use consultas SQL con cláusulas ORDER BY o WHERE personalizadas, consultas de parámetros u objetos **QueryDef** que recuperen registros indexados concretos.</span><span class="sxs-lookup"><span data-stu-id="eff67-p107">When working with Microsoft Access database engine-connected ODBC databases and large dynaset-type **Recordset** objects, you might discover that using the **Find** methods or using the **Sort** or **Filter** property is slow. To improve performance, use SQL queries with customized ORDER BY or WHERE clauses, parameter queries, or **QueryDef** objects that retrieve specific indexed records.</span></span>

<span data-ttu-id="eff67-p108">Al buscar en campos que contengan fechas, debe usar el formato de fecha estadounidense (mes-día-año), aunque no esté usando la versión estadounidense del motor de base de datos de Microsoft Access. Si no lo hace así, es posible que no encuentre los datos. Use la función de Visual Basic **Format** para convertir la fecha. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="eff67-p108">You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine; otherwise, the data may not be found. Use the Visual Basic **Format** function to convert the date. For example:</span></span>

```vb
rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

<span data-ttu-id="eff67-152">Si criteria está compuesto por una cadena concatenada con un valor de tipo no entero y los parámetros del sistema especifican un carácter decimal que no es de EE.UU. como una coma (por ejemplo, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), se produce un error cuando intenta llamar al método.</span><span class="sxs-lookup"><span data-stu-id="eff67-152">If criteria is composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to call the method.</span></span> <span data-ttu-id="eff67-153">Esto se produce porque durante la concatenación, el número se convertirá en una cadena utilizando el carácter decimal predeterminado de su sistema y Microsoft Access SQL sólo acepta caracteres decimales con el formato estándar de Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="eff67-153">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

> [!NOTE]
> - <span data-ttu-id="eff67-154">Para obtener el mejor rendimiento, los criterios \*\*\* deben tener el formato "*valor* de campo " donde field es un campo indizado en la tabla base subyacente, o " field LIKE prefix " donde field es un campo indizado en la tabla base subyacente y el prefijo es una cadena de búsqueda de prefijo  =  (por ejemplo, "ART\*").     </span><span class="sxs-lookup"><span data-stu-id="eff67-154">For best performance, the *criteria*\* should be in either the form "*field* = *value*" where *field* is an indexed field in the underlying base table, or "*field* LIKE *prefix*" where *field* is an indexed field in the underlying base table and *prefix* is a prefix search string (for example, "ART\*").</span></span>
> - <span data-ttu-id="eff67-p110">En general, con tipos de búsquedas equivalentes, el método **Seek** proporciona mejor rendimiento que los métodos **Find**, siempre que no necesite más que los objetos **Recordset** de tipo tabla por sí solos.</span><span class="sxs-lookup"><span data-stu-id="eff67-p110">In general, for equivalent types of searches, the **Seek** method provides better performance than the **Find** methods. This assumes that table-type **Recordset** objects alone can satisfy your needs.</span></span>


