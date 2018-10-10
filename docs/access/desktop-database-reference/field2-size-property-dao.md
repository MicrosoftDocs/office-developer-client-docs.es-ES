---
title: Field2.Size Property (DAO)
TOCTitle: Size Property
ms:assetid: e252759a-cea9-25cb-667d-80b422fbf97e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835700(v=office.15)
ms:contentKeyID: 48548282
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ffca40d22d77a604e4c0b794a8070fb444d44a32
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485838"
---
# <a name="field2size-property-dao"></a><span data-ttu-id="51a32-102">Field2.Size Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="51a32-102">Field2.Size Property (DAO)</span></span>


<span data-ttu-id="51a32-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="51a32-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="51a32-104">Establece o devuelve un valor que indica el tamaño máximo, en bytes, de un objeto **Field2**.</span><span class="sxs-lookup"><span data-stu-id="51a32-104">Sets or returns a value that indicates the maximum size, in bytes, of a **Field2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="51a32-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51a32-105">Syntax</span></span>

<span data-ttu-id="51a32-106">*expresión* . Tamaño</span><span class="sxs-lookup"><span data-stu-id="51a32-106">*expression* .Size</span></span>

<span data-ttu-id="51a32-107">*expresión* Variable que representa un objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="51a32-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="51a32-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51a32-108">Remarks</span></span>

<span data-ttu-id="51a32-109">Para un objeto no anexado todavía a la colección **[Fields](fields-collection-dao.md)**, esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="51a32-109">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="51a32-p101">Para aquellos campos (distintos de los campos tipo Memo) que contienen datos sobre caracteres, la propiedad **Size** indica el número máximo de caracteres que admite ese campo. Para los campos numéricos, la propiedad **Size** indica cuántos bytes de almacenamiento son necesarios.</span><span class="sxs-lookup"><span data-stu-id="51a32-p101">For fields (other than Memo type fields) that contain character data, the **Size** property indicates the maximum number of characters that the field can hold. For numeric fields, the **Size** property indicates how many bytes of storage are required.</span></span>

<span data-ttu-id="51a32-112">El uso de la propiedad **Size** depende del objeto que contenga la colección **Fields** para el que está anexado el objeto **Field2**, como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="51a32-112">Use of the **Size** property depends on the object that contains the **Fields** collection to which the **Field2** object is appended, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="51a32-113">Objeto anexado a</span><span class="sxs-lookup"><span data-stu-id="51a32-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="51a32-114">Uso</span><span class="sxs-lookup"><span data-stu-id="51a32-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51a32-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="51a32-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="51a32-116">No admitido</span><span class="sxs-lookup"><span data-stu-id="51a32-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51a32-117"><strong>Objeto QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="51a32-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="51a32-118">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="51a32-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51a32-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="51a32-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="51a32-120">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="51a32-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51a32-121"><strong>Relación</strong></span><span class="sxs-lookup"><span data-stu-id="51a32-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="51a32-122">No admitido</span><span class="sxs-lookup"><span data-stu-id="51a32-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51a32-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="51a32-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="51a32-124">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="51a32-124">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="51a32-p102">Cuando se crea un objeto **Field2** con un tipo de datos distinto de Texto, el valor de la propiedad **Type** determina automáticamente el valor de la propiedad **Size** y no es necesario establecer este valor. Sin embargo, para un objeto **Field2** con el tipo de datos Texto, se puede establecer **Size** en cualquier entero hasta el tamaño máximo del texto (255 para las bases de datos del motor de base de datos de Microsoft Access). Si no se establece el tamaño, el campo será tan grande como lo permita la base de datos.</span><span class="sxs-lookup"><span data-stu-id="51a32-p102">When you create a **Field2** object with a data type other than Text, the **Type** property setting automatically determines the **Size** property setting; you don't need to set it. For a **Field2** object with the Text data type, however, you can set **Size** to any integer up to the maximum text size (255 for Microsoft Access database engine databases). If you do not set the size, the field will be as large as the database allows.</span></span>

<span data-ttu-id="51a32-p103">Para Long Binary y Memo de los objetos **Field2**, **Size** está establecido siempre en 0. Utilice la propiedad **FieldSize** del objeto **Field2** para determinar el tamaño de los datos en un registro específico. El tamaño máximo de un campo Long Binary o Memo está limitado sólo por los recursos de su sistema o por el tamaño máximo permitido por la base de datos.</span><span class="sxs-lookup"><span data-stu-id="51a32-p103">For Long Binary and Memo **Field2** objects, **Size** is always set to 0. Use the **FieldSize** property of the **Field2** object to determine the size of the data in a specific record. The maximum size of a Long Binary or Memo field is limited only by your system resources or the maximum size that the database allows.</span></span>

## <a name="example"></a><span data-ttu-id="51a32-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="51a32-131">Example</span></span>

<span data-ttu-id="51a32-132">En este ejemplo se muestra la propiedad **Size** mediante la enumeración de los nombres y tamaños de los objetos **Field2** en la tabla Empleados.</span><span class="sxs-lookup"><span data-stu-id="51a32-132">This example demonstrates the **Size** property by enumerating the names and sizes of the **Field2** objects in the Employees table.</span></span>

```vb
    Sub SizeX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldNew As Field2 
     Dim fldLoop As Field2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     With tdfEmployees 
     
     ' Create and append a new Field object to the 
     ' Employees table. 
     Set fldNew = .CreateField("FaxPhone") 
     fldNew.Type = dbText 
     fldNew.Size = 20 
     .Fields.Append fldNew 
     
     Debug.Print "TableDef: " & .Name 
     Debug.Print " Field.Name - Field.Type - Field.Size" 
     
     ' Enumerate Fields collection; print field names, 
     ' types, and sizes. 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name & " - " & _ 
     fldLoop.Type & " - " & fldLoop.Size 
     Next fldLoop 
     
     ' Delete new field because this is a demonstration. 
     .Fields.Delete fldNew.Name 
     
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
