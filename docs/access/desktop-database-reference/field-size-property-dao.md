---
title: Field.Size Property (DAO)
TOCTitle: Size Property
ms:assetid: 15e25201-87b6-f62f-ff18-259414a47891
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845510(v=office.15)
ms:contentKeyID: 48543419
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052878
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c55c7cedb3ad249e30180af872aead372554e9a8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484531"
---
# <a name="fieldsize-property-dao"></a><span data-ttu-id="de044-102">Field.Size Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="de044-102">Field.Size Property (DAO)</span></span>


<span data-ttu-id="de044-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="de044-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="de044-104">Establece o devuelve un valor que indica el tamaño máximo en bytes de un objeto **[Field](field-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="de044-104">Sets or returns a value that indicates the maximum size, in bytes, of a **[Field](field-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="de044-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de044-105">Syntax</span></span>

<span data-ttu-id="de044-106">*expresión* . Tamaño</span><span class="sxs-lookup"><span data-stu-id="de044-106">*expression* .Size</span></span>

<span data-ttu-id="de044-107">*expresión* Variable que representa un objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="de044-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="de044-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de044-108">Remarks</span></span>

<span data-ttu-id="de044-109">Para un objeto no anexado todavía a la colección **[Fields](fields-collection-dao.md)**, esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="de044-109">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="de044-p101">Para campos (que no sean campos de tipo Memo) que contienen datos de caracteres, la propiedad **Size** indica el número máximo de caracteres que el campo puede contener. Para campos numéricos, la propiedad **Size** indica el número de bytes de almacenamiento que se requieren.</span><span class="sxs-lookup"><span data-stu-id="de044-p101">For fields (other than Memo type fields) that contain character data, the **Size** property indicates the maximum number of characters that the field can hold. For numeric fields, the **Size** property indicates how many bytes of storage are required.</span></span>

<span data-ttu-id="de044-112">El uso de la propiedad **Size** depende del objeto que contiene la colección **Fields** a la que se anexa el objeto **Field**, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="de044-112">Use of the **Size** property depends on the object that contains the **Fields** collection to which the **Field** object is appended, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de044-113">Objeto anexado a</span><span class="sxs-lookup"><span data-stu-id="de044-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="de044-114">Uso</span><span class="sxs-lookup"><span data-stu-id="de044-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de044-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="de044-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="de044-116">No admitido</span><span class="sxs-lookup"><span data-stu-id="de044-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de044-117"><strong>Objeto QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="de044-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="de044-118">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="de044-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de044-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="de044-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="de044-120">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="de044-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de044-121"><strong>Relación</strong></span><span class="sxs-lookup"><span data-stu-id="de044-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="de044-122">No admitido</span><span class="sxs-lookup"><span data-stu-id="de044-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de044-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="de044-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="de044-124">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="de044-124">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="de044-p102">Cuando se crea un objeto **Field** con un tipo de datos distinto de Text, el valor de la propiedad **[Type](field-type-property-dao.md)** determina automáticamente el valor de la propiedad **Size**; no es necesario establecerlo. Sin embargo, para un objeto **Field** con el tipo de datos Text, se puede establecer **Size** en cualquier entero que no supere el tamaño máximo de texto (255 para bases de datos de Microsoft Access). Si no se establece el tamaño, el campo tendrá el tamaño que la base de datos permita.</span><span class="sxs-lookup"><span data-stu-id="de044-p102">When you create a **Field** object with a data type other than Text, the **[Type](field-type-property-dao.md)** property setting automatically determines the **Size** property setting; you don't need to set it. For a **Field** object with the Text data type, however, you can set **Size** to any integer up to the maximum text size (255 for Microsoft Access databases). If you do not set the size, the field will be as large as the database allows.</span></span>

<span data-ttu-id="de044-p103">Para objetos **Field** Long Binary y Memo, **Size** se establece siempre en 0. Use la propiedad **[FieldSize](field-fieldsize-property-dao.md)** del objeto **Field** para determinar el tamaño de los datos en un registro concreto. El tamaño máximo de un campo Long Binary o Memo está limitado únicamente por los recursos del sistema o por el tamaño máximo permitido por la base de datos.</span><span class="sxs-lookup"><span data-stu-id="de044-p103">For Long Binary and Memo **Field** objects, **Size** is always set to 0. Use the **[FieldSize](field-fieldsize-property-dao.md)** property of the **Field** object to determine the size of the data in a specific record. The maximum size of a Long Binary or Memo field is limited only by your system resources or the maximum size that the database allows.</span></span>

## <a name="example"></a><span data-ttu-id="de044-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="de044-131">Example</span></span>

<span data-ttu-id="de044-132">En este ejemplo se enumeran los nombres y tamaños de los objetos **Field** en la tabla Employees para demostrar el uso de la propiedad **Size**.</span><span class="sxs-lookup"><span data-stu-id="de044-132">This example demonstrates the **Size** property by enumerating the names and sizes of the **Field** objects in the Employees table.</span></span>

```vb
    Sub SizeX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldNew As Field 
     Dim fldLoop As Field 
     
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