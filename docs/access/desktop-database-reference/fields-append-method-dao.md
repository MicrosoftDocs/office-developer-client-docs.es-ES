---
title: Método Fields.Append (DAO)
TOCTitle: Append Method
ms:assetid: a0e553ba-6a57-09af-3436-4f6ca3cbe561
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820791(v=office.15)
ms:contentKeyID: 48546719
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: ec3cacbe1f1c7ac5d6bda16bdd47891dc58ebfe0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292590"
---
# <a name="fieldsappend-method-dao"></a><span data-ttu-id="d029a-102">Método Fields.Append (DAO)</span><span class="sxs-lookup"><span data-stu-id="d029a-102">Fields.Append method (DAO)</span></span>

<span data-ttu-id="d029a-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d029a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d029a-104">Agrega un nuevo **[Field](field-object-dao.md)** a la colección **[Fields](fields-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="d029a-104">Adds a new **[Field](field-object-dao.md)** to the **[Fields](fields-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d029a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d029a-105">Syntax</span></span>

<span data-ttu-id="d029a-106">*expression* .Append(***Object***)</span><span class="sxs-lookup"><span data-stu-id="d029a-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="d029a-107">*expression* Variable que representa un objeto **Fields**.</span><span class="sxs-lookup"><span data-stu-id="d029a-107">*expression*  A variable that represents a **Fields** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="d029a-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="d029a-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d029a-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="d029a-109">Name</span></span></p></th>
<th><p><span data-ttu-id="d029a-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="d029a-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="d029a-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d029a-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="d029a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d029a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d029a-113"><em>Objeto</em></span><span class="sxs-lookup"><span data-stu-id="d029a-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="d029a-114">Necesario</span><span class="sxs-lookup"><span data-stu-id="d029a-114">Required</span></span></p></td>
<td><p><span data-ttu-id="d029a-115"><strong>Objeto</strong></span><span class="sxs-lookup"><span data-stu-id="d029a-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="d029a-116">Variable de objeto que representa el campo que se va a anexar a la colección.</span><span class="sxs-lookup"><span data-stu-id="d029a-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d029a-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d029a-117">Remarks</span></span>

<span data-ttu-id="d029a-118">Puede utilizar el método **Append** para agregar una nueva tabla a una base de datos, un campo a una tabla y un campo a un índice.</span><span class="sxs-lookup"><span data-stu-id="d029a-118">You can use the **Append** method to add a new table to a database, add a field to a table, and add a field to an index.</span></span>

<span data-ttu-id="d029a-119">El objeto anexado se convierte en un objeto persistente, almacenado en un disco, hasta que lo elimine mediante el método **Delete**.</span><span class="sxs-lookup"><span data-stu-id="d029a-119">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="d029a-120">La agregación de un nuevo objeto se produce de inmediato pero debe utilizar el método **Refresh** en cualquier otra colección que pueda verse afectada por los cambios en la estructura de base de datos.</span><span class="sxs-lookup"><span data-stu-id="d029a-120">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="d029a-121">Si el objeto que está anexando está incompleto (como cuando no ha anexado ningún objeto **Field** a una colección **Fields** de un objeto **Index** antes de anexarlo a una colección **Indexes**) o si las propiedades establecidas en uno o varios objetos subordinados son incorrectas, el uso del método **Append** provoca un error.</span><span class="sxs-lookup"><span data-stu-id="d029a-121">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="d029a-122">Por ejemplo, si no ha especificado un campo e intenta anexar el objeto **Field** a la colección **Fields** en un objeto **TableDef**, el uso del método **Append** desencadena un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d029a-122">For example, if you haven't specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

## <a name="example"></a><span data-ttu-id="d029a-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d029a-123">Example</span></span>

<span data-ttu-id="d029a-p102">En este ejemplo se utiliza el método **Append** o **Delete** para modificar la colección **Fields** de un objeto **TableDef**. Se requiere el procedimiento AppendDeleteField para que pueda ejecutarse este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="d029a-p102">This example uses either the **Append** method or the **Delete** method to modify the **Fields** collection of a **TableDef**. The AppendDeleteField procedure is required for this procedure to run.</span></span>

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
