---
title: Propiedad Recordset2.LastModified (DAO)
TOCTitle: LastModified Property
ms:assetid: 1c13cb43-23b5-73b6-af00-a3676cc37cc7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845726(v=office.15)
ms:contentKeyID: 48543557
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c3d9337c36a2b126f4ce6d9a27ae6d26712a7b6a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712865"
---
# <a name="recordset2lastmodified-property-dao"></a><span data-ttu-id="22d22-102">Propiedad Recordset2.LastModified (DAO)</span><span class="sxs-lookup"><span data-stu-id="22d22-102">Recordset2.LastModified property (DAO)</span></span>


<span data-ttu-id="22d22-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="22d22-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="22d22-104">Devuelve Bookmark que indica el último registro agregado o modificado.</span><span class="sxs-lookup"><span data-stu-id="22d22-104">Returns a ookmark indicating the most recently added or changed record.</span></span>

## <a name="syntax"></a><span data-ttu-id="22d22-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22d22-105">Syntax</span></span>

<span data-ttu-id="22d22-106">*expresión* . LastModified</span><span class="sxs-lookup"><span data-stu-id="22d22-106">*expression* .LastModified</span></span>

<span data-ttu-id="22d22-107">*expresión* Variable que representa un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="22d22-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="22d22-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22d22-108">Remarks</span></span>

<span data-ttu-id="22d22-p101">Puede usar la propiedad **LastModified** para mover los últimos registros agregados o modificados. Use la propiedad **LastModified** con objetos **[Recordset](recordset-object-dao.md)** de tipo Table y Dynaset. Un registro se debe agregar o modificar en el objeto **Recordset** mismo para que la propiedad **LastModified** tenga un valor.</span><span class="sxs-lookup"><span data-stu-id="22d22-p101">You can use the **LastModified** property to move to the most recently added or updated record. Use the **LastModified** property with table- and dynaset-type **[Recordset](recordset-object-dao.md)** objects. A record must be added or modified in the **Recordset** object itself in order for the **LastModified** property to have a value.</span></span>

## <a name="example"></a><span data-ttu-id="22d22-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="22d22-112">Example</span></span>

<span data-ttu-id="22d22-113">En este ejemplo se utiliza la propiedad **LastModified** para mover el puntero de registros actual a ambos registros, al que se ha modificado y al que se ha creado recientemente.</span><span class="sxs-lookup"><span data-stu-id="22d22-113">This example uses the **LastModified** property to move the current record pointer to both a record that has been modified and a newly created record.</span></span>

```vb
    Sub LastModifiedX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strFirst As String 
     Dim strLast As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     ' Store current data. 
     strFirst = !FirstName 
     strLast = !LastName 
     ' Change data in current record. 
     .Edit 
     !FirstName = "Julie" 
     !LastName = "Warren" 
     .Update 
     ' Move current record pointer to the most recently 
     ' changed or added record. 
     .Bookmark = .LastModified 
     Debug.Print _ 
     "Data in LastModified record after Edit: " & _ 
     !FirstName & " " & !LastName 
     
     ' Restore original data because this is a demonstration. 
     .Edit 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     
     ' Add new record. 
     .AddNew 
     !FirstName = "Roger" 
     !LastName = "Harui" 
     .Update 
     ' Move current record pointer to the most recently 
     ' changed or added record. 
     .Bookmark = .LastModified 
     Debug.Print _ 
     "Data in LastModified record after AddNew: " & _ 
     !FirstName & " " & !LastName 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="22d22-p102">En este ejemplo se utiliza el método **AddNew** para crear un registro nuevo con el nombre especificado. Se requiere la función AddName para que pueda ejecutarse este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="22d22-p102">This example uses the **AddNew** method to create a new record with the specified name. The AddName function is required for this procedure to run.</span></span>

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", dbOpenDynaset) 
     
     ' Get data from the user. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed only if the user actually entered something 
     ' for both the first and last names. 
     If strFirstName <> "" and strLastName <> "" Then 
     
     ' Call the function that adds the record. 
     AddName rstEmployees, strFirstName, strLastName 
     
     ' Show the newly added data. 
     With rstEmployees 
     Debug.Print "New record: " & !FirstName & _ 
     " " & !LastName 
     ' Delete new record because this is a demonstration. 
     .Delete 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function AddName(rstTemp As Recordset, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a Recordset using the data passed 
     ' by the calling procedure. The new record is then made 
     ' the current record. 
     With rstTemp 
     .AddNew 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Function
```
