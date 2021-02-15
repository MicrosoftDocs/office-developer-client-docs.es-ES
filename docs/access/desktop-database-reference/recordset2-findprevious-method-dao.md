---
title: Método Recordset2.FindPrevious (DAO)
TOCTitle: FindPrevious Method
ms:assetid: ec35faf4-20f2-a83f-54e4-ac1f66c3c2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836294(v=office.15)
ms:contentKeyID: 48548509
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9cf53526f9643737c7236bb2c98589e74f3f2eb5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307318"
---
# <a name="recordset2findprevious-method-dao"></a><span data-ttu-id="8719f-102">Método Recordset2.FindPrevious (DAO)</span><span class="sxs-lookup"><span data-stu-id="8719f-102">Recordset2.FindPrevious method (DAO)</span></span>

<span data-ttu-id="8719f-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8719f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8719f-p101">Busca el registro anterior de un objeto **[Recordset](recordset-object-dao.md)** de tipo Dynaset o de instantánea que satisfaga los criterios especificados y hace que el registro sea el registro activo (solo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="8719f-p101">Locates the previous record in a dynaset- or snapshot-type **[Recordset](recordset-object-dao.md)** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="8719f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8719f-106">Syntax</span></span>

<span data-ttu-id="8719f-107">*expresión* . FindPrevious(***Criteria***)</span><span class="sxs-lookup"><span data-stu-id="8719f-107">*expression* .FindPrevious(***Criteria***)</span></span>

<span data-ttu-id="8719f-108">*expresión* Variable que representa un objeto **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="8719f-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="8719f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8719f-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8719f-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="8719f-110">Name</span></span></p></th>
<th><p><span data-ttu-id="8719f-111">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="8719f-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="8719f-112">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8719f-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="8719f-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="8719f-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8719f-114"><em>Criterios</em></span><span class="sxs-lookup"><span data-stu-id="8719f-114"><em>Criteria</em></span></span></p></td>
<td><p><span data-ttu-id="8719f-115">Necesario</span><span class="sxs-lookup"><span data-stu-id="8719f-115">Required</span></span></p></td>
<td><p><span data-ttu-id="8719f-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="8719f-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="8719f-117">Cadena que se utiliza para localizar el registro.</span><span class="sxs-lookup"><span data-stu-id="8719f-117">A String used to locate the record.</span></span> <span data-ttu-id="8719f-118">Es como una cláusula WHERE en una instrucción SQL pero sin la palabra WHERE.</span><span class="sxs-lookup"><span data-stu-id="8719f-118">It is like the WHERE clause in an SQL statement, but without the word WHERE.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8719f-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8719f-119">Remarks</span></span>

<span data-ttu-id="8719f-p103">Si quiere incluir en la búsqueda todos los registros, y no solo los que cumplan una condición determinada, use los métodos **Move** para moverse de un registro a otro. Para buscar un registro en un **Recordset** de tipo tabla, use el método **Seek**.</span><span class="sxs-lookup"><span data-stu-id="8719f-p103">If you want to include all the records in your search — not just those that meet a specific condition — use the **Move** methods to move from record to record. To locate a record in a table-type **Recordset**, use the **Seek** method.</span></span>

<span data-ttu-id="8719f-p104">Si no se encuentra ningún registro que coincida con los criterios, el puntero del registro actual será desconocido y la propiedad **NoMatch** se configurará como **True**. Si el conjunto de registros contiene varios registros que cumplen los criterios, **FindFirst** buscará el primero, **FindNext** buscará el segundo y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="8719f-p104">If a record matching the criteria isn't located, the current record pointer is unknown, and the **NoMatch** property is set to **True**. If recordset contains more than one record that satisfies the criteria, **FindFirst** locates the first occurrence, **FindNext** locates the next occurrence, and so on.</span></span>

<span data-ttu-id="8719f-124">Cada método **Find** empieza a buscar a partir de la ubicación y en la dirección que se especifican en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8719f-124">Each of the **Find** methods begins its search from the location and in the direction specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8719f-125">Método Find</span><span class="sxs-lookup"><span data-stu-id="8719f-125">Find method</span></span></p></th>
<th><p><span data-ttu-id="8719f-126">Empieza la búsqueda en</span><span class="sxs-lookup"><span data-stu-id="8719f-126">Begins searching at</span></span></p></th>
<th><p><span data-ttu-id="8719f-127">Dirección de búsqueda</span><span class="sxs-lookup"><span data-stu-id="8719f-127">Search direction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8719f-128"><strong>FindFirst</strong></span><span class="sxs-lookup"><span data-stu-id="8719f-128"><strong>FindFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="8719f-129">Principio del conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="8719f-129">Beginning of recordset</span></span></p></td>
<td><p><span data-ttu-id="8719f-130">Final del conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="8719f-130">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8719f-131"><strong>FindLast</strong></span><span class="sxs-lookup"><span data-stu-id="8719f-131"><strong>FindLast</strong></span></span></p></td>
<td><p><span data-ttu-id="8719f-132">Final del conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="8719f-132">End of recordset</span></span></p></td>
<td><p><span data-ttu-id="8719f-133">Principio del conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="8719f-133">Beginning of recordset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8719f-134"><strong>FindNext</strong></span><span class="sxs-lookup"><span data-stu-id="8719f-134"><strong>FindNext</strong></span></span></p></td>
<td><p><span data-ttu-id="8719f-135">Registro actual</span><span class="sxs-lookup"><span data-stu-id="8719f-135">Current record</span></span></p></td>
<td><p><span data-ttu-id="8719f-136">Final del conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="8719f-136">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8719f-137"><strong>FindPrevious</strong></span><span class="sxs-lookup"><span data-stu-id="8719f-137"><strong>FindPrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="8719f-138">Registro actual</span><span class="sxs-lookup"><span data-stu-id="8719f-138">Current record</span></span></p></td>
<td><p><span data-ttu-id="8719f-139">Principio del conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="8719f-139">Beginning of recordset</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8719f-p105">No obstante, el uso de uno de los métodos **Find** no es igual a utilizar el método **Move**, que activa simplemente el registro primero, último, siguiente o anterior sin especificar una condición. Puede proseguir una operación Find con una operación Move.</span><span class="sxs-lookup"><span data-stu-id="8719f-p105">Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition. You can follow a Find operation with a Move operation.</span></span>

<span data-ttu-id="8719f-p106">Compruebe siempre el valor de la propiedad **NoMatch** para determinar si la operación Find se ha realizado correctamente. Si la búsqueda es correcta, **NoMatch** es **False**. Si se produce un error, **NoMatch** es **True** y el registro activo no está definido. En este caso, debe colocar de nuevo el puntero de registros activo en un registro válido.</span><span class="sxs-lookup"><span data-stu-id="8719f-p106">Always check the value of the **NoMatch** property to determine whether the Find operation has succeeded. If the search succeeds, **NoMatch** is **False**. If it fails, **NoMatch** is **True** and the current record isn't defined. In this case, you must position the current record pointer back to a valid record.</span></span>

<span data-ttu-id="8719f-p107">Usar los métodos **Find** con conjuntos de registros a los que se accede por ODBC con conexión a un motor de base de datos de Microsoft Access puede resultar ineficiente. Tal vez observe que resulta más rápido reformular los criterios para buscar un determinado registro, especialmente al trabajar con conjuntos de registros de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="8719f-p107">Using the **Find** methods with Microsoft Access database engine-connected ODBC-accessed recordsets can be inefficient. You may find that rephrasing your criteria to locate a specific record is faster, especially when working with large recordsets.</span></span>

<span data-ttu-id="8719f-p108">Al trabajar con grandes objetos **Recordset** de tipo conjunto de registros dinámicos y bases de datos ODBC conectadas a un motor de base de datos de Microsoft Access, puede que compruebe que usar los métodos **Find** o las propiedades **Sort** o **Filter** resulta lento. Para mejorar el rendimiento, use consultas SQL con cláusulas ORDER BY o WHERE personalizadas, consultas de parámetros u objetos **QueryDef** que recuperen registros indexados concretos.</span><span class="sxs-lookup"><span data-stu-id="8719f-p108">When working with Microsoft Access database engine-connected ODBC databases and large dynaset-type **Recordset** objects, you might discover that using the **Find** methods or using the **Sort** or **Filter** property is slow. To improve performance, use SQL queries with customized ORDER BY or WHERE clauses, parameter queries, or **QueryDef** objects that retrieve specific indexed records.</span></span>

<span data-ttu-id="8719f-p109">Al buscar en campos que contengan fechas, debe usar el formato de fecha estadounidense (mes-día-año), aunque no esté usando la versión estadounidense del motor de base de datos de Microsoft Access. Si no lo hace así, es posible que no encuentre los datos. Use la función de Visual Basic **Format** para convertir la fecha. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8719f-p109">You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine; otherwise, the data may not be found. Use the Visual Basic **Format** function to convert the date. For example:</span></span>

```vb
rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

<span data-ttu-id="8719f-153">Si criteria está compuesto por una cadena concatenada con un valor de tipo no entero y los parámetros del sistema especifican un carácter decimal que no es de EE.UU. como una coma (por ejemplo, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), se produce un error cuando intenta llamar al método.</span><span class="sxs-lookup"><span data-stu-id="8719f-153">If criteria is composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to call the method.</span></span> <span data-ttu-id="8719f-154">Esto se produce porque durante la concatenación, el número se convertirá en una cadena utilizando el carácter decimal predeterminado de su sistema y Microsoft Access SQL sólo acepta caracteres decimales con el formato estándar de Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="8719f-154">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

> [!NOTE]
> - <span data-ttu-id="8719f-155">Para obtener un mejor rendimiento, los criterios \*\*\* deben tener el formato *"* valor de campo " donde campo es un campo indizado en la tabla base subyacente o " prefijo LIKE " donde campo es un campo indizado en la tabla base subyacente y prefijo es una cadena de búsqueda de prefijo  =  (por ejemplo, "ART\*").     </span><span class="sxs-lookup"><span data-stu-id="8719f-155">For best performance, the *criteria*\* should be in either the form "*field* = *value*" where *field* is an indexed field in the underlying base table, or "*field* LIKE *prefix*" where *field* is an indexed field in the underlying base table and *prefix* is a prefix search string (for example, "ART\*").</span></span>
> - <span data-ttu-id="8719f-p111">En general, con tipos de búsquedas equivalentes, el método **Seek** proporciona mejor rendimiento que los métodos **Find**, siempre que no necesite más que los objetos **Recordset** de tipo tabla por sí solos.</span><span class="sxs-lookup"><span data-stu-id="8719f-p111">In general, for equivalent types of searches, the **Seek** method provides better performance than the **Find** methods. This assumes that table-type **Recordset** objects alone can satisfy your needs.</span></span>


