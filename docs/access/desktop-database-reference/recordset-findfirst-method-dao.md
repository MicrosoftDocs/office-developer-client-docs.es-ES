---
title: Recordset.FindFirst (método) (DAO)
TOCTitle: FindFirst Method
ms:assetid: 5fcf78cd-7d2c-2e47-14e5-996f2e14ff51
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194787(v=office.15)
ms:contentKeyID: 48545170
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 489e6060fdbaa4183c006e3f422c207d9a5013ee
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998857"
---
# <a name="recordsetfindfirst-method-dao"></a><span data-ttu-id="398dc-102">Recordset.FindFirst (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="398dc-102">Recordset.FindFirst method (DAO)</span></span>

<span data-ttu-id="398dc-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="398dc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="398dc-104">Busca el primer registro de un objeto **Recordset** de tipo Dynaset o instantánea que satisfaga los criterios especificados y convierte el registro en el registro actual (solo en áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="398dc-104">Locates the first record in a dynaset- or snapshot-type **Recordset** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="398dc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="398dc-105">Syntax</span></span>

<span data-ttu-id="398dc-106">*expresión* . FindFirst (***criterios***)</span><span class="sxs-lookup"><span data-stu-id="398dc-106">*expression* .FindFirst(***Criteria***)</span></span>

<span data-ttu-id="398dc-107">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="398dc-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="398dc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="398dc-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="398dc-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="398dc-109">Name</span></span></p></th>
<th><p><span data-ttu-id="398dc-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="398dc-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="398dc-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="398dc-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="398dc-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="398dc-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="398dc-113"><em>Criteria</em></span><span class="sxs-lookup"><span data-stu-id="398dc-113"><em>Criteria</em></span></span></p></td>
<td><p><span data-ttu-id="398dc-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="398dc-114">Required</span></span></p></td>
<td><p><span data-ttu-id="398dc-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="398dc-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="398dc-p101">Cadena que se utiliza para localizar el registro. Es como una cláusula WHERE en una instrucción SQL pero sin la palabra WHERE.</span><span class="sxs-lookup"><span data-stu-id="398dc-p101">A String used to locate the record. It is like the WHERE clause in an SQL statement, but without the word WHERE.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="398dc-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="398dc-118">Remarks</span></span>

<span data-ttu-id="398dc-p102">Si quiere incluir en la búsqueda todos los registros, y no solo los que cumplan una condición determinada, use los métodos **Move** para moverse de un registro a otro. Para buscar un registro en un **Recordset** de tipo tabla, use el método **Seek**.</span><span class="sxs-lookup"><span data-stu-id="398dc-p102">If you want to include all the records in your search — not just those that meet a specific condition — use the **Move** methods to move from record to record. To locate a record in a table-type **Recordset**, use the **Seek** method.</span></span>

<span data-ttu-id="398dc-p103">Si no se encuentra ningún registro que coincida con los criterios, el puntero del registro actual será desconocido y la propiedad **NoMatch** se configurará como **True**. Si el conjunto de registros contiene varios registros que cumplen los criterios, **FindFirst** buscará el primero, **FindNext** buscará el segundo y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="398dc-p103">If a record matching the criteria isn't located, the current record pointer is unknown, and the **NoMatch** property is set to **True**. If recordset contains more than one record that satisfies the criteria, **FindFirst** locates the first occurrence, **FindNext** locates the next occurrence, and so on.</span></span>

<span data-ttu-id="398dc-123">Cada método **Find** empieza a buscar a partir de la ubicación y en la dirección que se especifican en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="398dc-123">Each of the **Find** methods begins its search from the location and in the direction specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="398dc-124">Método Find</span><span class="sxs-lookup"><span data-stu-id="398dc-124">Find method</span></span></p></th>
<th><p><span data-ttu-id="398dc-125">Empieza la búsqueda en</span><span class="sxs-lookup"><span data-stu-id="398dc-125">Begins searching at</span></span></p></th>
<th><p><span data-ttu-id="398dc-126">Dirección de búsqueda</span><span class="sxs-lookup"><span data-stu-id="398dc-126">Search direction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="398dc-127"><strong>FindFirst</strong></span><span class="sxs-lookup"><span data-stu-id="398dc-127"><strong>FindFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="398dc-128">Principio del conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="398dc-128">Beginning of recordset</span></span></p></td>
<td><p><span data-ttu-id="398dc-129">Final del conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="398dc-129">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="398dc-130"><strong>FindLast</strong></span><span class="sxs-lookup"><span data-stu-id="398dc-130"><strong>FindLast</strong></span></span></p></td>
<td><p><span data-ttu-id="398dc-131">Final del conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="398dc-131">End of recordset</span></span></p></td>
<td><p><span data-ttu-id="398dc-132">Principio del conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="398dc-132">Beginning of recordset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="398dc-133"><strong>FindNext</strong></span><span class="sxs-lookup"><span data-stu-id="398dc-133"><strong>FindNext</strong></span></span></p></td>
<td><p><span data-ttu-id="398dc-134">Registro actual</span><span class="sxs-lookup"><span data-stu-id="398dc-134">Current record</span></span></p></td>
<td><p><span data-ttu-id="398dc-135">Final del conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="398dc-135">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="398dc-136"><strong>FindPrevious</strong></span><span class="sxs-lookup"><span data-stu-id="398dc-136"><strong>FindPrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="398dc-137">Registro actual</span><span class="sxs-lookup"><span data-stu-id="398dc-137">Current record</span></span></p></td>
<td><p><span data-ttu-id="398dc-138">Principio del conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="398dc-138">Beginning of recordset</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="398dc-p104">No obstante, el uso de uno de los métodos **Find** no es igual a utilizar el método **Move**, que activa simplemente el registro primero, último, siguiente o anterior sin especificar una condición. Puede proseguir una operación Find con una operación Move.</span><span class="sxs-lookup"><span data-stu-id="398dc-p104">Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition. You can follow a Find operation with a Move operation.</span></span>

<span data-ttu-id="398dc-p105">Compruebe siempre el valor de la propiedad **NoMatch** para determinar si la operación Find se ha realizado correctamente. Si la búsqueda es correcta, **NoMatch** es **False**. Si se produce un error, **NoMatch** es **True** y el registro activo no está definido. En este caso, debe colocar de nuevo el puntero de registros activo en un registro válido.</span><span class="sxs-lookup"><span data-stu-id="398dc-p105">Always check the value of the **NoMatch** property to determine whether the Find operation has succeeded. If the search succeeds, **NoMatch** is **False**. If it fails, **NoMatch** is **True** and the current record isn't defined. In this case, you must position the current record pointer back to a valid record.</span></span>

<span data-ttu-id="398dc-p106">Usar los métodos **Find** con conjuntos de registros a los que se accede por ODBC con conexión a un motor de base de datos de Microsoft Access puede resultar ineficiente. Tal vez observe que resulta más rápido reformular los criterios para buscar un determinado registro, especialmente al trabajar con conjuntos de registros de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="398dc-p106">Using the **Find** methods with Microsoft Access database engine-connected ODBC-accessed recordsets can be inefficient. You may find that rephrasing your criteria to locate a specific record is faster, especially when working with large recordsets.</span></span>

<span data-ttu-id="398dc-p107">Al trabajar con grandes objetos **Recordset** de tipo conjunto de registros dinámicos y bases de datos ODBC conectadas a un motor de base de datos de Microsoft Access, puede que compruebe que usar los métodos **Find** o las propiedades **Sort** o **Filter** resulta lento. Para mejorar el rendimiento, use consultas SQL con cláusulas ORDER BY o WHERE personalizadas, consultas de parámetros u objetos **QueryDef** que recuperen registros indexados concretos.</span><span class="sxs-lookup"><span data-stu-id="398dc-p107">When working with Microsoft Access database engine-connected ODBC databases and large dynaset-type **Recordset** objects, you might discover that using the **Find** methods or using the **Sort** or **Filter** property is slow. To improve performance, use SQL queries with customized ORDER BY or WHERE clauses, parameter queries, or **QueryDef** objects that retrieve specific indexed records.</span></span>

<span data-ttu-id="398dc-p108">Debe utilizar el formato de fecha de EE.UU. (mes-día-año) cuando busca campos que contienen fechas, incluso si no utiliza la versión americana del motor de base de datos de Microsoft Access; de lo contrario, es posible que no se encuentre la fecha. Utilice la función **Format** de Visual Basic para convertir la fecha. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="398dc-p108">You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine; otherwise, the data may not be found. Use the Visual Basic **Format** function to convert the date. For example:</span></span>

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

<span data-ttu-id="398dc-152">Si criteria está compuesto de una cadena que se concatena con un valor no entero y los parámetros del sistema especifican un carácter decimal que no sean-US como una coma (por ejemplo, strSQL = "PRICE \> " & lngPrice y lngPrice = 125,50), se produce un error al intentar Llame al método.</span><span class="sxs-lookup"><span data-stu-id="398dc-152">If criteria is composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to call the method.</span></span> <span data-ttu-id="398dc-153">Esto se produce porque durante la concatenación, el número se convertirá en una cadena utilizando el carácter decimal predeterminado de su sistema y Microsoft Access SQL sólo acepta caracteres decimales con el formato estándar de Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="398dc-153">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>


> [!NOTE]
> - <span data-ttu-id="398dc-154">Para obtener el mejor rendimiento, los *criterios* deben tener el formulario "*campo* = *valor*" donde *campo* es un campo indizado en la tabla base subyacente o "*campo* LIKE *prefijo*" donde *campo* es un campo indizado en la tabla base subyacente y *prefijo* es una cadena de búsqueda de prefijo (por ejemplo, "ART \*").</span><span class="sxs-lookup"><span data-stu-id="398dc-154">For best performance, the *criteria* should be in either the form "*field* = *value*" where *field* is an indexed field in the underlying base table, or "*field* LIKE *prefix*" where *field* is an indexed field in the underlying base table and *prefix* is a prefix search string (for example, "ART\*" ).</span></span>
> 
> - <span data-ttu-id="398dc-p110">En general, para tipos de búsquedas equivalentes, el método **Seek** proporciona un mejor rendimiento que los métodos **Find**. Esto supone que los objetos **Recordset** de tipo tabla por sí mismos pueden satisfacer sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="398dc-p110">In general, for equivalent types of searches, the **Seek** method provides better performance than the **Find** methods. This assumes that table-type **Recordset** objects alone can satisfy your needs.</span></span>


## <a name="example"></a><span data-ttu-id="398dc-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="398dc-157">Example</span></span>

<span data-ttu-id="398dc-158">En el siguiente ejemplo, se muestra cómo usar los métodos FindFirst y FindNext para buscar un registro en un Recordset.</span><span class="sxs-lookup"><span data-stu-id="398dc-158">The following example shows how to use the FindFirst and FindNext methods to find a record in a Recordset.</span></span>

<span data-ttu-id="398dc-159">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="398dc-159">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub FindOrgName()
    
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset
        
        'Get the database and Recordset
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblCustomers")
    
        'Search for the first matching record   
        rst.FindFirst "[OrgName] LIKE '*parts*'"
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
            GotTo Cleanup
        Else
            Do While Not rst.NoMatch
                MsgBox "Customer name: " & rst!CustName
                rst.FindNext "[OrgName] LIKE '*parts*'"
            Loop
    
            'Search for the next matching record
            rst.FindNext "[OrgName] LIKE '*parts*'"
        End If
       
        Cleanup:
            rst.Close
            Set rst = Nothing
            Set dbs = Nothing
    
    End Sub
```
