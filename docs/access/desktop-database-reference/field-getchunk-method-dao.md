---
title: Método Field. GetChunk (DAO)
TOCTitle: GetChunk Method
ms:assetid: b8984e79-54f7-8052-85a3-d12033daf7a1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822448(v=office.15)
ms:contentKeyID: 48547328
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052871
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c7eabceb1f7c130e349428aeb6b2dc079fe4319d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293101"
---
# <a name="fieldgetchunk-method-dao"></a><span data-ttu-id="4dd95-102">Método Field. GetChunk (DAO)</span><span class="sxs-lookup"><span data-stu-id="4dd95-102">Field.GetChunk method (DAO)</span></span>

<span data-ttu-id="4dd95-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4dd95-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4dd95-104">Devuelve todo o parte del contenido de un objeto **Memo** o **Long Binary** **[Field](field-object-dao.md)** en la colección **[Fields](fields-collection-dao.md)** de un objeto **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="4dd95-104">Returns all or a portion of the contents of a **Memo** or **Long Binary** **[Field](field-object-dao.md)** object in the **[Fields](fields-collection-dao.md)** collection of a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dd95-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4dd95-105">Syntax</span></span>

<span data-ttu-id="4dd95-106">*expresión* . GetChunk (***desplazamiento***, ***bytes***)</span><span class="sxs-lookup"><span data-stu-id="4dd95-106">*expression* .GetChunk(***Offset***, ***Bytes***)</span></span>

<span data-ttu-id="4dd95-107">*expresión* Variable que representa un objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="4dd95-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="4dd95-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="4dd95-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4dd95-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="4dd95-109">Name</span></span></p></th>
<th><p><span data-ttu-id="4dd95-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="4dd95-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="4dd95-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4dd95-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="4dd95-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4dd95-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4dd95-113"><em>Offset</em></span><span class="sxs-lookup"><span data-stu-id="4dd95-113"><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="4dd95-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4dd95-114">Required</span></span></p></td>
<td><p><span data-ttu-id="4dd95-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="4dd95-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="4dd95-116">Número de bytes que se omiten antes de que se inicie la copia.</span><span class="sxs-lookup"><span data-stu-id="4dd95-116">The number of bytes to skip before copying begins.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4dd95-117"><em>Bytes</em></span><span class="sxs-lookup"><span data-stu-id="4dd95-117"><em>Bytes</em></span></span></p></td>
<td><p><span data-ttu-id="4dd95-118">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="4dd95-118">Required</span></span></p></td>
<td><p><span data-ttu-id="4dd95-119"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="4dd95-119"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="4dd95-120">Número de bytes que desea devolver.</span><span class="sxs-lookup"><span data-stu-id="4dd95-120">The number of bytes you want to return.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="4dd95-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4dd95-121">Return value</span></span>

<span data-ttu-id="4dd95-122">Variant</span><span class="sxs-lookup"><span data-stu-id="4dd95-122">Variant</span></span>

## <a name="remarks"></a><span data-ttu-id="4dd95-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4dd95-123">Remarks</span></span>

<span data-ttu-id="4dd95-p101">Los bytes devueltos por **GetChunk** se asignan a una variable. Utilice **GetChunk** para devolver una parte del valor de datos total cada vez. Puede usar el método **[AppendChunk](field-appendchunk-method-dao.md)** para reorganizar las piezas.</span><span class="sxs-lookup"><span data-stu-id="4dd95-p101">The bytes returned by **GetChunk** are assigned to variable. Use **GetChunk** to return a portion of the total data value at a time. You can use the **[AppendChunk](field-appendchunk-method-dao.md)** method to reassemble the pieces.</span></span>

<span data-ttu-id="4dd95-127">Si offset es 0, **GetChunk** inicia la copia desde el primer byte del campo.</span><span class="sxs-lookup"><span data-stu-id="4dd95-127">If offset is 0, **GetChunk** begins copying from the first byte of the field.</span></span>

<span data-ttu-id="4dd95-128">Si NumBytes es mayor que el número de bytes del campo, **GetChunk** devuelve el número real de bytes restantes en el campo.</span><span class="sxs-lookup"><span data-stu-id="4dd95-128">If numbytes is greater than the number of bytes in the field, **GetChunk** returns the actual number of remaining bytes in the field.</span></span>

> [!NOTE]
> <span data-ttu-id="4dd95-129">Use un campo **Memo** para texto y coloque datos binarios sólo en campos **binarios largos** .</span><span class="sxs-lookup"><span data-stu-id="4dd95-129">Use a **Memo** field for text, and put binary data only in **Long Binary** fields.</span></span> <span data-ttu-id="4dd95-130">Si lo hace, se producirán resultados no deseados.</span><span class="sxs-lookup"><span data-stu-id="4dd95-130">Doing otherwise will cause undesirable results.</span></span>

## <a name="example"></a><span data-ttu-id="4dd95-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4dd95-131">Example</span></span>

<span data-ttu-id="4dd95-p103">En este ejemplo se utilizan los métodos **AppendChunk** y **GetChunk** para rellenar un campo de objeto OLE con datos de otro registro, 32 K cada vez. En una aplicación real, se podría utilizar un procedimiento como éste para copiar un registro de empleado (incluida la foto del mismo) de una tabla a otra. En este ejemplo, el registro simplemente se vuelve a copiar en la misma tabla. Tenga en cuenta que todas las operaciones con fragmentos de campo se producen dentro de una sola secuencia AddNew-Update.</span><span class="sxs-lookup"><span data-stu-id="4dd95-p103">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time. In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another. In this example, the record is simply being copied back to same table. Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
