---
title: 'Objeto Field: objetos de acceso a datos (DAO)'
TOCTitle: Field Object
ms:assetid: 47282ce2-9b49-ccf9-ad37-c4bb25cfd037
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193203(v=office.15)
ms:contentKeyID: 48544587
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c58896fb0d0a5c5a28844fdd3a6df922dd587f32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293045"
---
# <a name="field-object-dao"></a><span data-ttu-id="5c853-102">Objeto Field (DAO)</span><span class="sxs-lookup"><span data-stu-id="5c853-102">Field object (DAO)</span></span>

<span data-ttu-id="5c853-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5c853-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5c853-104">Un objeto \*\*Field \*\* representa una columna de datos con un tipo de datos común y un conjunto común de propiedades.</span><span class="sxs-lookup"><span data-stu-id="5c853-104">A **Field** object represents a column of data with a common data type and a common set of properties.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c853-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5c853-105">Remarks</span></span>

<span data-ttu-id="5c853-p101">Las colecciones **Fields** de los objetos **Index**, **QueryDef**, **Relation** y **TableDef** contienen las especificaciones para los campos que estos objetos representan. La colección **Fields** de un objeto **Recordset** representa los objetos **Field** de una fila de datos o de un registro. Use los objetos **Field** de un objeto **Recordset** para leer y establecer valores para los campos en el registro activo del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="5c853-p101">The **Fields** collections of **Index**, **QueryDef**, **Relation**, and **TableDef** objects contain the specifications for the fields those objects represent. The **Fields** collection of a **Recordset** object represents the **Field** objects in a row of data, or in a record. You use the **Field** objects in a **Recordset** object to read and set values for the fields in the current record of the **Recordset** object.</span></span>

<span data-ttu-id="5c853-p102">En un área de trabajo de Microsoft Access, puede modificar un campo mediante un objeto **Field** y sus métodos y propiedades. Por ejemplo, puede:</span><span class="sxs-lookup"><span data-stu-id="5c853-p102">In a Microsoft Access workspacee, you manipulate a field using a **Field** object and its methods and properties. For example, you can:</span></span>

  - <span data-ttu-id="5c853-111">Utilizar la propiedad **OrdinalPosition** para establecer o devolver el orden de presentación del objeto **Field** en una colección **Fields**.</span><span class="sxs-lookup"><span data-stu-id="5c853-111">Use the **OrdinalPosition** property to set or return the presentation order of the **Field** object in a **Fields** collection.</span></span>

  - <span data-ttu-id="5c853-112">Usar la propiedad **Value** de un campo en un objeto **Recordset** para establecer o devolver datos guardados.</span><span class="sxs-lookup"><span data-stu-id="5c853-112">Use the **Value** property of a field in a **Recordset** object to set or return stored data.</span></span>

  - <span data-ttu-id="5c853-113">Usar los métodos **AppendChunk** y **GetChunk** y la propiedad **FieldSize** para obtener o establecer un valor en un campo de tipo Objeto o Memo OLE de un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="5c853-113">Use the **AppendChunk** and **GetChunk** methods and the **FieldSize** property to get or set a value in an OLE Object or Memo field of a **Recordset** object.</span></span>

  - <span data-ttu-id="5c853-114">Usar las propiedades **Type**, **Size** y **Attributes** para determinar el tipo de datos que se pueden guardar en el campo.</span><span class="sxs-lookup"><span data-stu-id="5c853-114">Use the **Type**, **Size**, and **Attributes** properties to determine the type of data that can be stored in the field.</span></span>

  - <span data-ttu-id="5c853-115">Utilizar las propiedades **SourceField** y **SourceTable** para determinar el origen de los datos original.</span><span class="sxs-lookup"><span data-stu-id="5c853-115">Use the **SourceField** and **SourceTable** properties to determine the original source of the data.</span></span>

  - <span data-ttu-id="5c853-116">Usar la propiedad **ForeignName** para establecer o devolver información sobre un campo externo de un objeto **Relation**.</span><span class="sxs-lookup"><span data-stu-id="5c853-116">Use the **ForeignName** property to set or return information about a foreign field in a **Relation** object.</span></span>

  - <span data-ttu-id="5c853-117">Utilizar las propiedades **AllowZeroLength**, **DefaultValue**, **Required**, **ValidateOnSet**, **ValidationRule** o **ValidationText** para establecer o devolver condiciones de validación.</span><span class="sxs-lookup"><span data-stu-id="5c853-117">Use the **AllowZeroLength**, **DefaultValue**, **Required**, **ValidateOnSet**, **ValidationRule**, or **ValidationText** properties to set or return validation conditions.</span></span>

  - <span data-ttu-id="5c853-118">Usar la propiedad **DefaultValue** de un campo en un **TableDef** para establecer el valor predeterminado para este campo cuando se agregan nuevos registros.</span><span class="sxs-lookup"><span data-stu-id="5c853-118">Use the **DefaultValue** property of a field on a **TableDef** object to set the default value for this field when new records are added.</span></span>

<span data-ttu-id="5c853-119">Para crear un nuevo objeto **Field** en un objeto **Index**, **TableDef** o **Relation**, utilice el método **CreateField**.</span><span class="sxs-lookup"><span data-stu-id="5c853-119">To create a new **Field** object in an **Index**, **TableDef**, or **Relation** object, use the **CreateField** method.</span></span>

<span data-ttu-id="5c853-p103">Cuando tiene acceso a un objeto **Field** como parte de un objeto **Recordset**, los datos del registro activo están visibles en la propiedad **Value** del objeto **Field**. Para manipular datos en el objeto **Recordset**, no suele hacer referencia a la colección **Fields** directamente, sino que hace referencia indirectamente a la propiedad **Value** del objeto **Field** en la colección **Fields** del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="5c853-p103">When you access a **Field** object as part of a **Recordset** object, data from the current record is visible in the **Field** object's **Value** property. To manipulate data in the **Recordset** object, you don't usually reference the **Fields** collection directly; instead, you indirectly reference the **Value** property of the **Field** object in the **Fields** collection of the **Recordset** object.</span></span>

<span data-ttu-id="5c853-122">Para hacer referencia a un objeto **Field** en una colección mediante su número ordinal o mediante el valor de la propiedad **Name**, utilice una de las formas sintácticas siguientes:</span><span class="sxs-lookup"><span data-stu-id="5c853-122">To refer to a **Field** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="5c853-123">**Fields**(0)</span><span class="sxs-lookup"><span data-stu-id="5c853-123">**Fields**(0)</span></span>

- <span data-ttu-id="5c853-124">**Fields**("name")</span><span class="sxs-lookup"><span data-stu-id="5c853-124">**Fields**("name")</span></span>

- <span data-ttu-id="5c853-125">**Fields**\!\[name\]</span><span class="sxs-lookup"><span data-stu-id="5c853-125">**Fields**\!\[name\]</span></span>

<span data-ttu-id="5c853-p104">Con las mismas formas sintácticas, puede hacer referencia igualmente a la propiedad **Value** de un objeto **Field** que cree y anexe a la colección **Fields**. El contexto de la referencia del campo determinará si hace referencia al objeto **Field** o a la propiedad **Value** del objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="5c853-p104">With the same syntax forms, you can also refer to the **Value** property of a **Field** object that you create and append to a **Fields** collection. The context of the field reference will determine whether you are referring to the **Field** object or the **Value** property of the **Field** object.</span></span>

## <a name="example"></a><span data-ttu-id="5c853-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5c853-128">Example</span></span>

<span data-ttu-id="5c853-p105">En este ejemplo se muestra qué propiedades son válidas para un objeto **Field** según dónde resida el objeto **Field** (por ejemplo, la colección **Fields** de un objeto **TableDef**, la colección **Fields** de un objeto **QueryDef**, etc.). Se requiere el procedimiento FieldOutput para que pueda ejecutarse este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="5c853-p105">This example shows what properties are valid for a **Field** object depending on where the **Field** resides (for example, the **Fields** collection of a **TableDef**, the **Fields** collection of a **QueryDef**, and so forth). The FieldOutput procedure is required for this procedure to run.</span></span>

```vb
    Sub FieldX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim fldTableDef As Field 
     Dim fldQueryDef As Field 
     Dim fldRecordset As Field 
     Dim fldRelation As Field 
     Dim fldIndex As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Assign a Field object from different Fields 
     ' collections to object variables. 
     Set fldTableDef = _ 
     dbsNorthwind.TableDefs(0).Fields(0) 
     Set fldQueryDef =dbsNorthwind.QueryDefs(0).Fields(0) 
     Set fldRecordset = rstEmployees.Fields(0) 
     Set fldRelation =dbsNorthwind.Relations(0).Fields(0) 
     Set fldIndex = _ 
     dbsNorthwind.TableDefs(0).Indexes(0).Fields(0) 
     
     ' Print report. 
     FieldOutput "TableDef", fldTableDef 
     FieldOutput "QueryDef", fldQueryDef 
     FieldOutput "Recordset", fldRecordset 
     FieldOutput "Relation", fldRelation 
     FieldOutput "Index", fldIndex 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub FieldOutput(strTemp As String, fldTemp As Field) 
     ' Report function for FieldX. 
     
     Dim prpLoop As Property 
     
     Debug.Print "Valid Field properties in " & strTemp 
     
     ' Enumerate Properties collection of passed Field 
     ' object. 
     For Each prpLoop In fldTemp.Properties 
     ' Some properties are invalid in certain 
     ' contexts (the Value property in the Fields 
     ' collection of a TableDef for example). Any 
     ' attempt to use an invalid property will 
     ' trigger an error. 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " = " & _ 
     prpLoop.Value 
     On Error GoTo 0 
     Next prpLoop 
     
    End Sub 
```

<br/>

<span data-ttu-id="5c853-p106">En este ejemplo se utiliza el método **CreateField** para crear tres objetos **Fields** para un nuevo objeto **TableDef**. A continuación, se muestran las propiedades de estos objetos **Field** que se establecen automáticamente mediante el método **CreateField**. No aparecen las propiedades cuyos valores están vacíos en el momento de crear los objetos **Field**.</span><span class="sxs-lookup"><span data-stu-id="5c853-p106">This example uses the **CreateField** method to create three **Fields** for a new **TableDef**. It then displays the properties of those **Field** objects that are automatically set by the **CreateField** method. (Properties whose values are empty at the time of **Field** creation are not shown.)</span></span>

```vb
    Sub CreateFieldX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
     
     ' Create and append new Field objects for the new 
     ' TableDef object. 
     With tdfNew 
     ' The CreateField method will set a default Size 
     ' for a new Field object if one is not specified. 
     .Fields.Append .CreateField("TextField", dbText) 
     .Fields.Append .CreateField("IntegerField", dbInteger) 
     .Fields.Append .CreateField("DateField", dbDate) 
     End With 
     
     dbsNorthwind.TableDefs.Append tdfNew 
     
     Debug.Print "Properties of new Fields in " & tdfNew.Name 
     
     ' Enumerate Fields collection to show the properties of 
     ' the new Field objects. 
     For Each fldLoop In tdfNew.Fields 
     Debug.Print " " & fldLoop.Name 
     
     For Each prpLoop In fldLoop.Properties 
     ' Properties that are invalid in the context of 
     ' TableDefs will trigger an error if an attempt 
     ' is made to read their values. 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     On Error GoTo 0 
     Next prpLoop 
     
     Next fldLoop 
     
     ' Delete new TableDef because this is a demonstration. 
     dbsNorthwind.TableDefs.Delete tdfNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
