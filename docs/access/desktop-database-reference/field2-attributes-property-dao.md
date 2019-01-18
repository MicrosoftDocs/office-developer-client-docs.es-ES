---
title: Propiedad Field2.Attributes (DAO)
TOCTitle: Attributes Property
ms:assetid: 08ae9b6b-21e4-9b7e-0852-cfc6639027a7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845025(v=office.15)
ms:contentKeyID: 48543102
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052896
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a655cfa5c6f0427b1a26a01f01e991564ab8e387
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700720"
---
# <a name="field2attributes-property-dao"></a><span data-ttu-id="e98a2-102">Propiedad Field2.Attributes (DAO)</span><span class="sxs-lookup"><span data-stu-id="e98a2-102">Field2.Attributes property (DAO)</span></span>


<span data-ttu-id="e98a2-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e98a2-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="e98a2-p101">Establece o devuelve un valor que indica una o varias características de un objeto **Field2**. **Long** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e98a2-p101">Sets or returns a value that indicates one or more characteristics of a **Field2** object. Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e98a2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e98a2-106">Syntax</span></span>

<span data-ttu-id="e98a2-107">*expresión* . Atributos</span><span class="sxs-lookup"><span data-stu-id="e98a2-107">*expression* .Attributes</span></span>

<span data-ttu-id="e98a2-108">*expresión* Variable que representa un objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="e98a2-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e98a2-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e98a2-109">Remarks</span></span>

<span data-ttu-id="e98a2-110">El valor especifica características del campo representado por el objeto **Field2** y puede ser una combinación de las siguientes constantes.</span><span class="sxs-lookup"><span data-stu-id="e98a2-110">The value specifies characteristics of the field represented by the **Field2** object and can be a combination of these constants.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e98a2-111">Constante</span><span class="sxs-lookup"><span data-stu-id="e98a2-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="e98a2-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e98a2-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e98a2-113"><strong>dbAutoIncrField</strong></span><span class="sxs-lookup"><span data-stu-id="e98a2-113"><strong>dbAutoIncrField</strong></span></span></p></td>
<td><p><span data-ttu-id="e98a2-114">El valor del campo para nuevos registros se incrementa de forma automática en un valor de tipo Long integer único que no se puede modificar (en un área de trabajo de Microsoft Access, sólo se admite para tablas de bases de datos del motor de base de datos de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="e98a2-114">The field value for new records is automatically incremented to a unique Long integer that can't be changed (in a Microsoft Access workspace, supported only for Microsoft Access database engine database tables).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e98a2-115"><strong>dbDescending</strong></span><span class="sxs-lookup"><span data-stu-id="e98a2-115"><strong>dbDescending</strong></span></span></p></td>
<td><p><span data-ttu-id="e98a2-p102">El campo se ordena en orden descendente (de Z a A o de 100 a 0); esta opción sólo se aplica a un objeto <strong>Field2</strong> de una colección <strong>Fields</strong> de un objeto <strong>Index</strong>. Si se omite esta constante, el campo se ordena en orden ascendente (de A a Z o de 0 a 100). Éste es el valor predeterminado para los campos <strong>Index</strong> y <strong>TableDef</strong> (sólo áreas de trabajo de Microsoft Access)..</span><span class="sxs-lookup"><span data-stu-id="e98a2-p102">The field is sorted in descending (Z to A or 100 to 0) order; this option applies only to a <strong>Field2</strong> object in a <strong>Fields</strong> collection of an <strong>Index</strong> object. If you omit this constant, the field is sorted in ascending (A to Z or 0 to 100) order. This is the default value for <strong>Index</strong> and <strong>TableDef</strong> fields (Microsoft Access workspaces only)..</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e98a2-119"><strong>dbFixedField</strong></span><span class="sxs-lookup"><span data-stu-id="e98a2-119"><strong>dbFixedField</strong></span></span></p></td>
<td><p><span data-ttu-id="e98a2-120">El tamaño del campo es fijo (valor predeterminado para los campos numéricos).</span><span class="sxs-lookup"><span data-stu-id="e98a2-120">The field size is fixed (default for Numeric fields).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e98a2-121"><strong>dbHyperlinkField</strong></span><span class="sxs-lookup"><span data-stu-id="e98a2-121"><strong>dbHyperlinkField</strong></span></span></p></td>
<td><p><span data-ttu-id="e98a2-122">El campo contiene información de hipervínculo (sólo campos de tipo Memo).</span><span class="sxs-lookup"><span data-stu-id="e98a2-122">The field contains hyperlink information (Memo fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e98a2-123"><strong>dbSystemField</strong></span><span class="sxs-lookup"><span data-stu-id="e98a2-123"><strong>dbSystemField</strong></span></span></p></td>
<td><p><span data-ttu-id="e98a2-124">El campo almacena información de réplica para las réplicas; este tipo de campo no se puede eliminar (solo en áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="e98a2-124">The field stores replication information for replicas; you can't delete this type of field (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e98a2-125"><strong>dbUpdatableField</strong></span><span class="sxs-lookup"><span data-stu-id="e98a2-125"><strong>dbUpdatableField</strong></span></span></p></td>
<td><p><span data-ttu-id="e98a2-126">El valor del campo se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="e98a2-126">The field value can be changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e98a2-127"><strong>dbVariableField</strong></span><span class="sxs-lookup"><span data-stu-id="e98a2-127"><strong>dbVariableField</strong></span></span></p></td>
<td><p><span data-ttu-id="e98a2-128">El tamaño del campo es variable (sólo campos de tipo Text).</span><span class="sxs-lookup"><span data-stu-id="e98a2-128">The field size is variable (Text fields only).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e98a2-p103">Para un objeto que aún no se haya anexado a una colección, esta propiedad es de lectura y escritura. Para un objeto **Field2** anexado, la disponibilidad de la propiedad **Attributes** depende del objeto que contenga la colección **Fields**.</span><span class="sxs-lookup"><span data-stu-id="e98a2-p103">For an object not yet appended to a collection, this property is read/write. For an appended **Field2** object, the availability of the **Attributes** property depends on the object that contains the **Fields** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e98a2-131">Si el objeto Field pertenece a</span><span class="sxs-lookup"><span data-stu-id="e98a2-131">If the Field object belongs to an</span></span></p></th>
<th><p><span data-ttu-id="e98a2-132">Disponibilidad de Attributes</span><span class="sxs-lookup"><span data-stu-id="e98a2-132">Then Attributes is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e98a2-133">Objeto <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="e98a2-133"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="e98a2-134">Lectura y escritura hasta que el objeto <strong>TableDef</strong> al que está anexado el objeto <strong>Index</strong> se anexe a un objeto <strong>Database</strong>; después, la propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="e98a2-134">Read/write until the <strong>TableDef</strong> object that the <strong>Index</strong> object is appended to is appended to a <strong>Database</strong> object; then the property is read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e98a2-135">							Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="e98a2-135"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="e98a2-136">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e98a2-136">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e98a2-137">							Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="e98a2-137"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="e98a2-138">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e98a2-138">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e98a2-139">							Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="e98a2-139"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="e98a2-140">No admitido</span><span class="sxs-lookup"><span data-stu-id="e98a2-140">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e98a2-141">							Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="e98a2-141"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="e98a2-142">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="e98a2-142">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e98a2-p104">Si se establecen varios atributos, se pueden combinar sumando las constantes correspondientes. Los valores no válidos se omiten sin producir un error.</span><span class="sxs-lookup"><span data-stu-id="e98a2-p104">When you set multiple attributes, you can combine them by summing the appropriate constants. Any invalid values are ignored without producing an error.</span></span>

## <a name="example"></a><span data-ttu-id="e98a2-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e98a2-145">Example</span></span>

<span data-ttu-id="e98a2-146">En este ejemplo, se muestra la propiedad **Attributes** para objetos **Field2**, **Relation** y **TableDef** de la base de datos Northwind.</span><span class="sxs-lookup"><span data-stu-id="e98a2-146">This example displays the **Attributes** property for **Field2**, **Relation**, and **TableDef** objects in the Northwind database.</span></span>

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field2 
 Dim relLoop As Relation 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 
 ' Display the attributes of a TableDef object's 
 ' fields. 
 Debug.Print "Attributes of fields in " & _ 
 .TableDefs(0).Name & " table:" 
 For Each fldLoop In .TableDefs(0).Fields 
 Debug.Print " " & fldLoop.Name & " = " & _ 
 fldLoop.Attributes 
 Next fldLoop 
 
 ' Display the attributes of the Northwind database's 
 ' relations. 
 Debug.Print "Attributes of relations in " & _ 
 .Name & ":" 
 For Each relLoop In .Relations 
 Debug.Print " " & relLoop.Name & " = " & _ 
 relLoop.Attributes 
 Next relLoop 
 
 ' Display the attributes of the Northwind database's 
 ' tables. 
 Debug.Print "Attributes of tables in " & .Name & ":" 
 For Each tdfloop In .TableDefs 
 Debug.Print " " & tdfloop.Name & " = " & _ 
 tdfloop.Attributes 
 Next tdfloop 
 
 .Close 
 End With 
 
End Sub 
 
```

