---
title: Método Field.AppendChunk (DAO)
TOCTitle: AppendChunk Method
ms:assetid: f98c6862-fecf-06cb-a7c0-42b0d3150a06
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837014(v=office.15)
ms:contentKeyID: 48548819
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b1ce1c359582194ce87dfaf4f409be4303486e09
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293171"
---
# <a name="fieldappendchunk-method-dao"></a><span data-ttu-id="9d588-102">Método Field.AppendChunk (DAO)</span><span class="sxs-lookup"><span data-stu-id="9d588-102">Field.AppendChunk method (DAO)</span></span>

<span data-ttu-id="9d588-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9d588-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9d588-104">Agrega datos de una expresión de cadena a un objeto **[Field](field-object-dao.md)** de Memo o binario largo en un objeto **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="9d588-104">Appends data from a string expression to a Memo or Long Binary **[Field](field-object-dao.md)** object in a **[Recordset](recordset-object-dao.md)**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d588-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d588-105">Syntax</span></span>

<span data-ttu-id="9d588-106">*expresión* . AppendChunk(***Val***)</span><span class="sxs-lookup"><span data-stu-id="9d588-106">*expression* .AppendChunk(***Val***)</span></span>

<span data-ttu-id="9d588-107">*expression* Variable que representa un objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="9d588-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="9d588-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d588-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9d588-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="9d588-109">Name</span></span></p></th>
<th><p><span data-ttu-id="9d588-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="9d588-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="9d588-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9d588-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="9d588-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d588-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d588-113"><em>Val</em></span><span class="sxs-lookup"><span data-stu-id="9d588-113"><em>Val</em></span></span></p></td>
<td><p><span data-ttu-id="9d588-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="9d588-114">Required</span></span></p></td>
<td><p><span data-ttu-id="9d588-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="9d588-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="9d588-116">Expresión o variable Variant (subtipo cadena) que contiene los datos que desea agregar al objeto <strong>Field</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d588-116">A Variant (String subtype) expression or variable containing the data you want to append to the <strong>Field</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9d588-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9d588-117">Remarks</span></span>

<span data-ttu-id="9d588-118">Puede utilizar los métodos **AppendChunk** y **[GetChunk](field-getchunk-method-dao.md)** para tener acceso a subconjuntos de datos en un campo Memo o Binario largo.</span><span class="sxs-lookup"><span data-stu-id="9d588-118">You can use the **AppendChunk** and **[GetChunk](field-getchunk-method-dao.md)** methods to access subsets of data in a Memo or Long Binary field.</span></span>

<span data-ttu-id="9d588-p101">Puede utilizar también estos métodos para conservar espacio de cadena cuando trabaje con campos Memo o Binario largo. En algunas operaciones (como copiar) se utilizan cadenas temporales. Si el espacio de cadena es limitado, quizás necesite trabajar con fragmentos de un campo en lugar de con todo el campo.</span><span class="sxs-lookup"><span data-stu-id="9d588-p101">You can also use these methods to conserve string space when you work with Memo and Long Binary fields. Certain operations (copying, for example) involve temporary strings. If string space is limited, you may need to work with chunks of a field instead of the entire field.</span></span>

<span data-ttu-id="9d588-122">Si no hay ningún registro actual cuando utiliza **AppendChunk**, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="9d588-122">If there is no current record when you use **AppendChunk**, an error occurs.</span></span>

> [!NOTE]
> <span data-ttu-id="9d588-p102">La operación **AppendChunk** inicial (después de una llamada a **[Edit](recordset-edit-method-dao.md)** o **[AddNew](recordset-addnew-method-dao.md)** ) sólo colocará los datos en el campo sobrescribiendo los existentes. Las siguientes llamadas a **AppendChunk** en la misma sesión **Edit** o **AddNew** agregarán entonces los datos a los datos existentes.</span><span class="sxs-lookup"><span data-stu-id="9d588-p102">The initial **AppendChunk** operation (after an **[Edit](recordset-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** call) will simply place the data in the field, overwriting any existing data. Subsequent **AppendChunk** calls within the same **Edit** or **AddNew** session will then add to the existing data.</span></span>

## <a name="example"></a><span data-ttu-id="9d588-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9d588-125">Example</span></span>

<span data-ttu-id="9d588-p103">En este ejemplo se utilizan los métodos **AppendChunk** y **GetChunk** para rellenar un campo de objeto OLE con datos de otro registro, 32 K cada vez. En una aplicación real, se podría utilizar un procedimiento como éste para copiar un registro de empleado (incluida la foto del mismo) de una tabla a otra. En este ejemplo, el registro simplemente se vuelve a copiar en la misma tabla. Tenga en cuenta que todas las operaciones con fragmentos de campo se producen dentro de una sola secuencia AddNew-Update.</span><span class="sxs-lookup"><span data-stu-id="9d588-p103">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time. In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another. In this example, the record is simply being copied back to same table. Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

```vb
    Sub AppendChunkX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim rstEmployees2 As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Open two recordsets from the Employees table. 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees", _ 
          dbOpenDynaset) 
       Set rstEmployees2 = rstEmployees.Clone 
     
       ' Add a new record to the first Recordset and copy the  
       ' data from a record in the second Recordset. 
       With rstEmployees 
          .AddNew 
          !FirstName = rstEmployees2!FirstName 
          !LastName = rstEmployees2!LastName 
          CopyLargeField rstEmployees2!Photo, !Photo 
          .Update 
     
          ' Delete new record because this is a demonstration. 
          .Bookmark = .LastModified 
          .Delete 
          .Close 
       End With 
     
       rstEmployees2.Close 
       dbsNorthwind.Close 
     
    End Sub 
     
    Function CopyLargeField(fldSource As Field, _ 
       fldDestination As Field) 
     
       ' Set size of chunk in bytes. 
       Const conChunkSize = 32768 
     
       Dim lngOffset As Long 
       Dim lngTotalSize As Long 
       Dim strChunk As String 
     
       ' Copy the photo from one Recordset to the other in 32K  
       ' chunks until the entire field is copied. 
       lngTotalSize = fldSource.FieldSize 
       Do While lngOffset < lngTotalSize 
          strChunk = fldSource.GetChunk(lngOffset, conChunkSize) 
          fldDestination.AppendChunk strChunk 
          lngOffset = lngOffset + conChunkSize 
       Loop 
     
    End Function
```
