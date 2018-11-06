---
title: Fields.Append (método) (DAO)
TOCTitle: Append Method
ms:assetid: a0e553ba-6a57-09af-3436-4f6ca3cbe561
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820791(v=office.15)
ms:contentKeyID: 48546719
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 576928e6538ea704bf6f10d0826c0e6bbb359bf1
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998241"
---
# <a name="fieldsappend-method-dao"></a><span data-ttu-id="14532-102">Fields.Append (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="14532-102">Fields.Append method (DAO)</span></span>

<span data-ttu-id="14532-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="14532-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="14532-104">Agrega un nuevo objeto **[Field](field-object-dao.md)** a la colección **[Fields](fields-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="14532-104">Adds a new **[Field](field-object-dao.md)** to the **[Fields](fields-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="14532-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14532-105">Syntax</span></span>

<span data-ttu-id="14532-106">*expresión* . Append (***objeto***)</span><span class="sxs-lookup"><span data-stu-id="14532-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="14532-107">*expresión* Variable que representa un objeto **Fields** .</span><span class="sxs-lookup"><span data-stu-id="14532-107">*expression* A variable that represents a **Fields** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="14532-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14532-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="14532-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="14532-109">Name</span></span></p></th>
<th><p><span data-ttu-id="14532-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="14532-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="14532-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="14532-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="14532-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="14532-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14532-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="14532-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="14532-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="14532-114">Required</span></span></p></td>
<td><p><span data-ttu-id="14532-115"><strong>Object</strong></span><span class="sxs-lookup"><span data-stu-id="14532-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="14532-116">Variable de objeto que representa el campo que se va a anexar a la colección.</span><span class="sxs-lookup"><span data-stu-id="14532-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="14532-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14532-117">Remarks</span></span>

<span data-ttu-id="14532-118">Puede utilizar el método **Append** para agregar una nueva tabla a una base de datos, un campo a una tabla y un campo a un índice.</span><span class="sxs-lookup"><span data-stu-id="14532-118">You can use the **Append** method to add a new table to a database, add a field to a table, and add a field to an index.</span></span>

<span data-ttu-id="14532-119">El objeto anexado se convierte en un objeto persistente, almacenado en un disco, hasta que lo elimine mediante el método **Delete**.</span><span class="sxs-lookup"><span data-stu-id="14532-119">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="14532-120">La agregación de un nuevo objeto se produce de inmediato pero debe utilizar el método **Refresh** en cualquier otra colección que pueda verse afectada por los cambios en la estructura de base de datos.</span><span class="sxs-lookup"><span data-stu-id="14532-120">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="14532-121">Si el objeto que está anexando está incompleto (como cuando no ha anexado ningún objeto **Field** a una colección **Fields** de un objeto **Index** antes de anexarlo a una colección **Indexes**) o si las propiedades establecidas en uno o varios objetos subordinados son incorrectas, el uso del método **Append** provoca un error.</span><span class="sxs-lookup"><span data-stu-id="14532-121">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="14532-122">Por ejemplo, si no ha especificado un tipo de campo y, a continuación, intente anexar el objeto **Field** a la colección **Fields** de un objeto **TableDef** , utilizando el método **Append** desencadena un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="14532-122">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

## <a name="example"></a><span data-ttu-id="14532-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="14532-123">Example</span></span>

<span data-ttu-id="14532-p102">En este ejemplo se utiliza el método **Append** o **Delete** para modificar la colección **Fields** de un objeto **TableDef**. Se requiere el procedimiento AppendDeleteField para que pueda ejecutarse este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="14532-p102">This example uses either the **Append** method or the **Delete** method to modify the **Fields** collection of a **TableDef**. The AppendDeleteField procedure is required for this procedure to run.</span></span>

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
