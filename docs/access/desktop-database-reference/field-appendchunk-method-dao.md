---
title: Field.AppendChunk (método) (DAO)
TOCTitle: AppendChunk Method
ms:assetid: f98c6862-fecf-06cb-a7c0-42b0d3150a06
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837014(v=office.15)
ms:contentKeyID: 48548819
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 830d9d10aa2d166f3e9dca013697acdeebe8a767
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923990"
---
# <a name="fieldappendchunk-method-dao"></a><span data-ttu-id="e075a-102">Field.AppendChunk (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="e075a-102">Field.AppendChunk method (DAO)</span></span>

<span data-ttu-id="e075a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e075a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e075a-104">Agrega datos de una expresión de cadena a un objeto **[Field](field-object-dao.md)** de Memo o binario largo en un objeto **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="e075a-104">Appends data from a string expression to a Memo or Long Binary **[Field](field-object-dao.md)** object in a **[Recordset](recordset-object-dao.md)**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e075a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e075a-105">Syntax</span></span>

<span data-ttu-id="e075a-106">*expresión* . AppendChunk (***Val***)</span><span class="sxs-lookup"><span data-stu-id="e075a-106">*expression* .AppendChunk(***Val***)</span></span>

<span data-ttu-id="e075a-107">*expresión* Variable que representa un objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="e075a-107">*expression* A variable that represents a **Field** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="e075a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e075a-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e075a-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="e075a-109">Name</span></span></p></th>
<th><p><span data-ttu-id="e075a-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="e075a-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="e075a-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e075a-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="e075a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e075a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e075a-113">Val</span><span class="sxs-lookup"><span data-stu-id="e075a-113">Val</span></span></p></td>
<td><p><span data-ttu-id="e075a-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e075a-114">Required</span></span></p></td>
<td><p><span data-ttu-id="e075a-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="e075a-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="e075a-116">Expresión o variable Variant (subtipo cadena) que contiene los datos que desea agregar al objeto <strong>Field</strong>.</span><span class="sxs-lookup"><span data-stu-id="e075a-116">A Variant (String subtype) expression or variable containing the data you want to append to the <strong>Field</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e075a-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e075a-117">Remarks</span></span>

<span data-ttu-id="e075a-118">Puede utilizar los métodos **AppendChunk** y **[GetChunk](field-getchunk-method-dao.md)** para tener acceso a subconjuntos de datos en un campo Memo o Binario largo.</span><span class="sxs-lookup"><span data-stu-id="e075a-118">You can use the **AppendChunk** and **[GetChunk](field-getchunk-method-dao.md)** methods to access subsets of data in a Memo or Long Binary field.</span></span>

<span data-ttu-id="e075a-p101">Puede utilizar también estos métodos para conservar espacio de cadena cuando trabaje con campos Memo o Binario largo. En algunas operaciones (como copiar) se utilizan cadenas temporales. Si el espacio de cadena es limitado, quizás necesite trabajar con fragmentos de un campo en lugar de con todo el campo.</span><span class="sxs-lookup"><span data-stu-id="e075a-p101">You can also use these methods to conserve string space when you work with Memo and Long Binary fields. Certain operations (copying, for example) involve temporary strings. If string space is limited, you may need to work with chunks of a field instead of the entire field.</span></span>

<span data-ttu-id="e075a-122">Si no hay ningún registro actual cuando utiliza **AppendChunk**, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="e075a-122">If there is no current record when you use **AppendChunk**, an error occurs.</span></span>

> [!NOTE]
> <span data-ttu-id="e075a-p102">La operación **AppendChunk** inicial (después de una llamada a **[Edit](recordset-edit-method-dao.md)** o **[AddNew](recordset-addnew-method-dao.md)** ) sólo colocará los datos en el campo sobrescribiendo los existentes. Las siguientes llamadas a **AppendChunk** en la misma sesión **Edit** o **AddNew** agregarán entonces los datos a los datos existentes.</span><span class="sxs-lookup"><span data-stu-id="e075a-p102">The initial **AppendChunk** operation (after an **[Edit](recordset-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** call) will simply place the data in the field, overwriting any existing data. Subsequent **AppendChunk** calls within the same **Edit** or **AddNew** session will then add to the existing data.</span></span>

## <a name="example"></a><span data-ttu-id="e075a-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e075a-125">Example</span></span>

<span data-ttu-id="e075a-p103">En este ejemplo se utilizan los métodos **AppendChunk** y **GetChunk** para rellenar un campo de objeto OLE con datos de otro registro, 32 K cada vez. En una aplicación real, se podría utilizar un procedimiento como éste para copiar un registro de empleado (incluida la foto del mismo) de una tabla a otra. En este ejemplo, el registro simplemente se vuelve a copiar en la misma tabla. Tenga en cuenta que todas las operaciones con fragmentos de campo se producen dentro de una sola secuencia AddNew-Update.</span><span class="sxs-lookup"><span data-stu-id="e075a-p103">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time. In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another. In this example, the record is simply being copied back to same table. Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
