---
title: Database.CreateRelation (método) (DAO)
TOCTitle: CreateRelation Method
ms:assetid: e240c7e3-c293-5e19-afcc-34d9a5549c64
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835692(v=office.15)
ms:contentKeyID: 48548279
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052969
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2a1ad7798fc6236f95d31c18cd864fe64e7a3fd8
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949932"
---
# <a name="databasecreaterelation-method-dao"></a><span data-ttu-id="ad498-102">Database.CreateRelation (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="ad498-102">Database.CreateRelation method (DAO)</span></span>

<span data-ttu-id="ad498-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad498-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ad498-p101">Crea un nuevo objeto **[Relation](relation-object-dao.md)** (solo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="ad498-p101">Creates a new **[Relation](relation-object-dao.md)** object (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="ad498-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad498-106">Syntax</span></span>

<span data-ttu-id="ad498-107">*expresión* . CreateRelation (***nombre***, ***tabla***, ***ForeignTable***, ***atributos***)</span><span class="sxs-lookup"><span data-stu-id="ad498-107">*expression* .CreateRelation(***Name***, ***Table***, ***ForeignTable***, ***Attributes***)</span></span>

<span data-ttu-id="ad498-108">*expresión* Variable que representa un objeto de **base de datos** .</span><span class="sxs-lookup"><span data-stu-id="ad498-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="ad498-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad498-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ad498-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="ad498-110">Name</span></span></p></th>
<th><p><span data-ttu-id="ad498-111">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="ad498-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="ad498-112">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ad498-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="ad498-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad498-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ad498-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="ad498-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="ad498-115">Opcional</span><span class="sxs-lookup"><span data-stu-id="ad498-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="ad498-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ad498-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ad498-p102"><strong>Variant</strong> (subtipo <strong>String</strong>) que designa inequívocamente el nuevo objeto <strong>Relation</strong>. Vea el tema relativo a la propiedad <strong><a href="connection-name-property-dao.md">Name</a></strong> para obtener información sobre los nombres de <strong>Relation</strong> válidos.</span><span class="sxs-lookup"><span data-stu-id="ad498-p102">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>Relation</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Relation</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad498-119"><em>Table</em></span><span class="sxs-lookup"><span data-stu-id="ad498-119"><em>Table</em></span></span></p></td>
<td><p><span data-ttu-id="ad498-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="ad498-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="ad498-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ad498-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ad498-p103"><strong>Variant</strong> (subtipo <strong>String</strong>) que designa la tabla principal de la relación. Si la tabla no existe antes de agregar el objeto <strong>Relation</strong>, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="ad498-p103">A <strong>Variant</strong> (<strong>String</strong> subtype) that names the primary table in the relation. If the table doesn't exist before you append the <strong>Relation</strong> object, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad498-124"><em>ForeignTable</em></span><span class="sxs-lookup"><span data-stu-id="ad498-124"><em>ForeignTable</em></span></span></p></td>
<td><p><span data-ttu-id="ad498-125">Opcional</span><span class="sxs-lookup"><span data-stu-id="ad498-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="ad498-126"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ad498-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ad498-p104"><strong>Variant</strong> (subtipo <strong>String</strong>) que designa la tabla externa de la relación. Si la tabla no existe antes de agregar el objeto <strong>Relation</strong>, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="ad498-p104">A <strong>Variant</strong> (<strong>String</strong> subtype) that names the foreign table in the relation. If the table doesn't exist before you append the <strong>Relation</strong> object, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad498-129"><em>Attributes</em></span><span class="sxs-lookup"><span data-stu-id="ad498-129"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="ad498-130">Opcional</span><span class="sxs-lookup"><span data-stu-id="ad498-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="ad498-131"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ad498-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ad498-p105">Constante o combinación de constantes que contienen información sobre el tipo de relación. Vea el tema relativo a la propiedad <strong><a href="field-attributes-property-dao.md">Attributes</a></strong> para obtener información detallada.</span><span class="sxs-lookup"><span data-stu-id="ad498-p105">A constant or combination of constants that contains information about the relationship type. See the <strong><a href="field-attributes-property-dao.md">Attributes</a></strong> property for details.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="ad498-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad498-134">Return value</span></span>

<span data-ttu-id="ad498-135">Relation</span><span class="sxs-lookup"><span data-stu-id="ad498-135">Relation</span></span>

## <a name="remarks"></a><span data-ttu-id="ad498-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad498-136">Remarks</span></span>

<span data-ttu-id="ad498-p106">El objeto **Relation** proporciona información al motor de base de datos de Microsoft Access sobre la relación entre los campos de dos objetos **[TableDef](tabledef-object-dao.md)** o **[QueryDef](querydef-object-dao.md)**. Puede implementar integridad referencial mediante la propiedad **Attributes**.</span><span class="sxs-lookup"><span data-stu-id="ad498-p106">The **Relation** object provides information to the Microsoft Access database engine about the relationship between fields in two **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** objects. You can implement referential integrity by using the **Attributes** property.</span></span>

<span data-ttu-id="ad498-p107">Si omite uno o varios de los argumentos opcionales cuando utiliza el método **CreateRelation**, puede usar la instrucción de asignación pertinente para establecer o restablecer la propiedad correspondiente antes de agregar el nuevo objeto a una colección. Después de agregar el objeto, no podrá modificar todos los valores de la propiedad. Vea los temas correspondientes a cada propiedad para obtener información más detallada.</span><span class="sxs-lookup"><span data-stu-id="ad498-p107">If you omit one or more of the optional parts when you use the **CreateRelation** method, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can't alter any of its property settings. See the individual property topics for more details.</span></span>

<span data-ttu-id="ad498-142">Antes de utilizar el método **[Append](fields-append-method-dao.md)** en un objeto **Relation**, debe agregar los objetos **[Field](field-object-dao.md)** correspondientes para definir las tablas principal y externa de la relación.</span><span class="sxs-lookup"><span data-stu-id="ad498-142">Before you can use the **[Append](fields-append-method-dao.md)** method on a **Relation** object, you must append the appropriate **[Field](field-object-dao.md)** objects to define the primary and foreign key relationship tables.</span></span>

<span data-ttu-id="ad498-143">Si name hace referencia a un objeto que ya es un miembro de la colección, o si los nombres de objeto **Field** proporcionados en la colección **Fields** subordinada no son válidos, se produce un error en tiempo de ejecución cuando se utiliza el método **Append** .</span><span class="sxs-lookup"><span data-stu-id="ad498-143">If name refers to an object that is already a member of the collection or if the **Field** object names provided in the subordinate **Fields** collection are invalid, a run-time error occurs when you use the **Append** method.</span></span>

<span data-ttu-id="ad498-144">No se puede establecer ni mantener una relación entre una tabla replicada y una tabla local.</span><span class="sxs-lookup"><span data-stu-id="ad498-144">You can't establish or maintain a relationship between a replicated table and a local table.</span></span>

<span data-ttu-id="ad498-145">Para quitar un objeto **Relation** de la colección **[Relations](relations-collection-dao.md)**, utilice el método **[Delete](fields-delete-method-dao.md)** en la colección.</span><span class="sxs-lookup"><span data-stu-id="ad498-145">To remove a **Relation** object from the **[Relations](relations-collection-dao.md)** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="ad498-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ad498-146">Example</span></span>

<span data-ttu-id="ad498-p108">En este ejemplo se utiliza el método **CreateRelation** para crear una **Relation** entre el objeto **TableDef** de empleados y un nuevo objeto **TableDef** denominado Departments (departamentos). En este ejemplo se muestra también cómo al crear una nueva **Relation** se crean también los **Indexes** necesarios en la tabla externa (el índice DepartmentsEmployees de la tabla Employees).</span><span class="sxs-lookup"><span data-stu-id="ad498-p108">This example uses the **CreateRelation** method to create a **Relation** between the Employees **TableDef** and a new **TableDef** called Departments. This example also demonstrates how creating a new **Relation** will also create any necessary **Indexes** in the foreign table (the DepartmentsEmployees Index in the Employees table).</span></span>

```vb
    Sub CreateRelationX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim tdfNew As TableDef 
     Dim idxNew As Index 
     Dim relNew As Relation 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Add new field to Employees table. 
     Set tdfEmployees = .TableDefs!Employees 
     tdfEmployees.Fields.Append _ 
     tdfEmployees.CreateField("DeptID", dbInteger, 2) 
     
     ' Create new Departments table. 
     Set tdfNew = .CreateTableDef("Departments") 
     
     With tdfNew 
     ' Create and append Field objects to Fields 
     ' collection of the new TableDef object. 
     .Fields.Append .CreateField("DeptID", dbInteger, 2) 
     .Fields.Append .CreateField("DeptName", dbText, 20) 
     
     ' Create Index object for Departments table. 
     Set idxNew = .CreateIndex("DeptIDIndex") 
     ' Create and append Field object to Fields 
     ' collection of the new Index object. 
     idxNew.Fields.Append idxNew.CreateField("DeptID") 
     ' The index in the primary table must be Unique in 
     ' order to be part of a Relation. 
     idxNew.Unique = True 
     .Indexes.Append idxNew 
     End With 
     
     .TableDefs.Append tdfNew 
     
     ' Create EmployeesDepartments Relation object, using 
     ' the names of the two tables in the relation. 
     Set relNew = .CreateRelation("EmployeesDepartments", _ 
     tdfNew.Name, tdfEmployees.Name, _ 
     dbRelationUpdateCascade) 
     
     ' Create Field object for the Fields collection of the 
     ' new Relation object. Set the Name and ForeignName 
     ' properties based on the fields to be used for the 
     ' relation. 
     relNew.Fields.Append relNew.CreateField("DeptID") 
     relNew.Fields!DeptID.ForeignName = "DeptID" 
     .Relations.Append relNew 
     
     ' Print report. 
     Debug.Print "Properties of " & relNew.Name & _ 
     " Relation" 
     Debug.Print " Table = " & relNew.Table 
     Debug.Print " ForeignTable = " & _ 
     relNew.ForeignTable 
     Debug.Print "Fields of " & relNew.Name & " Relation" 
     
     With relNew.Fields!DeptID 
     Debug.Print " " & .Name 
     Debug.Print " Name = " & .Name 
     Debug.Print " ForeignName = " & .ForeignName 
     End With 
     
     Debug.Print "Indexes in " & tdfEmployees.Name & _ 
     " TableDef" 
     For Each idxLoop In tdfEmployees.Indexes 
     Debug.Print " " & idxLoop.Name & _ 
     ", Foreign = " & idxLoop.Foreign 
     Next idxLoop 
     
     ' Delete new objects because this is a demonstration. 
     .Relations.Delete relNew.Name 
     .TableDefs.Delete tdfNew.Name 
     tdfEmployees.Fields.Delete "DeptID" 
     .Close 
     End With 
     
    End Sub
```
