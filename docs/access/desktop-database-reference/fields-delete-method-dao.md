---
title: Método Fields.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: a8e249e7-7526-3eff-a5cf-70cab2081970
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821417(v=office.15)
ms:contentKeyID: 48546913
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052868
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 8200d8ec7b10f33fe8bc1ef9faea122d3ff65409
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720992"
---
# <a name="fieldsdelete-method-dao"></a><span data-ttu-id="63b03-102">Método Fields.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="63b03-102">Fields.Delete method (DAO)</span></span>

<span data-ttu-id="63b03-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="63b03-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="63b03-104">Elimina un objeto **[Field](field-object-dao.md)** de la colección **[Fields](fields-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="63b03-104">Deletes a **[Field](field-object-dao.md)** from the **[Fields](fields-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="63b03-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63b03-105">Syntax</span></span>

<span data-ttu-id="63b03-106">*expresión* . Delete (***nombre***)</span><span class="sxs-lookup"><span data-stu-id="63b03-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="63b03-107">*expresión* Variable que representa un objeto **Fields** .</span><span class="sxs-lookup"><span data-stu-id="63b03-107">*expression* A variable that represents a **Fields** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="63b03-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63b03-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="63b03-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="63b03-109">Name</span></span></p></th>
<th><p><span data-ttu-id="63b03-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="63b03-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="63b03-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="63b03-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="63b03-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="63b03-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="63b03-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="63b03-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="63b03-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="63b03-114">Required</span></span></p></td>
<td><p><span data-ttu-id="63b03-115"><strong>Cadena</strong></span><span class="sxs-lookup"><span data-stu-id="63b03-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="63b03-116">Campo que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="63b03-116">The field to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="63b03-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63b03-117">Remarks</span></span>

<span data-ttu-id="63b03-118">La eliminación de un objeto almacenado se produce de inmediato pero debe utilizar el método **Refresh** en cualquier otra colección que pueda verse afectada por los cambios en la estructura de base de datos.</span><span class="sxs-lookup"><span data-stu-id="63b03-118">The deletion of a stored object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

## <a name="example"></a><span data-ttu-id="63b03-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="63b03-119">Example</span></span>

<span data-ttu-id="63b03-p101">En este ejemplo se utiliza el método **Append** o **Delete** para modificar la colección **Fields** de un objeto **TableDef**. Se requiere el procedimiento AppendDeleteField para que pueda ejecutarse este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="63b03-p101">This example uses either the **Append** method or the **Delete** method to modify the **Fields** collection of a **TableDef**. The AppendDeleteField procedure is required for this procedure to run.</span></span>

```vb
    Sub AppendX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldLoop As Field 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     ' Add three new fields. 
     AppendDeleteField tdfEmployees, "APPEND", _ 
     "E-mail", dbText, 50 
     AppendDeleteField tdfEmployees, "APPEND", _ 
     "Http", dbText, 80 
     AppendDeleteField tdfEmployees, "APPEND", _ 
     "Quota", dbInteger, 5 
     
     Debug.Print "Fields after Append" 
     Debug.Print , "Type", "Size", "Name" 
     
     ' Enumerate the Fields collection to show the new fields. 
     For Each fldLoop In tdfEmployees.Fields 
     Debug.Print , fldLoop.Type, fldLoop.Size, fldLoop.Name 
     Next fldLoop 
     
     ' Delete the newly added fields. 
     AppendDeleteField tdfEmployees, "DELETE", "E-mail" 
     AppendDeleteField tdfEmployees, "DELETE", "Http" 
     AppendDeleteField tdfEmployees, "DELETE", "Quota" 
     
     Debug.Print "Fields after Delete" 
     Debug.Print , "Type", "Size", "Name" 
     
     ' Enumerate the Fields collection to show that the new 
     ' fields have been deleted. 
     For Each fldLoop In tdfEmployees.Fields 
     Debug.Print , fldLoop.Type, fldLoop.Size, fldLoop.Name 
     Next fldLoop 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub AppendDeleteField(tdfTemp As TableDef, _ 
     strCommand As String, strName As String, _ 
     Optional varType, Optional varSize) 
     
     With tdfTemp 
     
     ' Check first to see if the TableDef object is 
     ' updatable. If it isn't, control is passed back to 
     ' the calling procedure. 
     If .Updatable = False Then 
     MsgBox "TableDef not Updatable! " & _ 
     "Unable to complete task." 
     Exit Sub 
     End If 
     
     ' Depending on the passed data, append or delete a 
     ' field to the Fields collection of the specified 
     ' TableDef object. 
     If strCommand = "APPEND" Then 
     .Fields.Append .CreateField(strName, _ 
     varType, varSize) 
     Else 
     If strCommand = "DELETE" Then .Fields.Delete _ 
     strName 
     End If 
     
     End With 
     
    End Sub
```
