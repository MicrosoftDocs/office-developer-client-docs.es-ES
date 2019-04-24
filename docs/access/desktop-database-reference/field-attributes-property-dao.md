---
title: Propiedad Field.Attributes (DAO)
TOCTitle: Attributes Property
ms:assetid: 8e6f6afb-1a89-7315-c129-cf7ff19e0ca9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197380(v=office.15)
ms:contentKeyID: 48546287
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 010c7a2aea777a93d1ced2d33d8743320dd05ada
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293157"
---
# <a name="fieldattributes-property-dao"></a><span data-ttu-id="bf714-102">Propiedad Field.Attributes (DAO)</span><span class="sxs-lookup"><span data-stu-id="bf714-102">Field.Attributes property (DAO)</span></span>


<span data-ttu-id="bf714-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf714-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="bf714-104">Establece o devuelve un valor que indica una o varias características de un objeto **[Field](field-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="bf714-104">Sets or returns a value that indicates one or more characteristics of a **[Field](field-object-dao.md)** object.</span></span> <span data-ttu-id="bf714-105">**Long** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="bf714-105">Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf714-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf714-106">Syntax</span></span>

<span data-ttu-id="bf714-107">*expression* .Attributes</span><span class="sxs-lookup"><span data-stu-id="bf714-107">expression  . Attributes</span></span>

<span data-ttu-id="bf714-108">*expression* Variable que representa un objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="bf714-108">*expression*  A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf714-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bf714-109">Remarks</span></span>

<span data-ttu-id="bf714-110">El valor especifica características del campo representado por el objeto **Field** y puede ser una combinación de estas constantes.</span><span class="sxs-lookup"><span data-stu-id="bf714-110">The value specifies characteristics of the field represented by the **Field** object and can be a combination of these constants.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bf714-111">Constante</span><span class="sxs-lookup"><span data-stu-id="bf714-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="bf714-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf714-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf714-113"><strong>dbAutoIncrField</strong></span><span class="sxs-lookup"><span data-stu-id="bf714-113"><strong>dbAutoIncrField</strong></span></span></p></td>
<td><p><span data-ttu-id="bf714-114">El valor del campo para nuevos registros se incrementa de forma automática en un valor de tipo Long integer único que no se puede modificar (en un área de trabajo de Microsoft Access, sólo se admite para tablas de bases de datos del motor de base de datos de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bf714-114">The field value for new records is automatically incremented to a unique Long integer that can't be changed (in a Microsoft Access workspace, supported only for Microsoft Access database engine database tables).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf714-115"><strong>dbDescending</strong></span><span class="sxs-lookup"><span data-stu-id="bf714-115"><strong>dbDescending</strong></span></span></p></td>
<td><p><span data-ttu-id="bf714-116">El campo se ordena en orden descendente (de Z a A o de 100 a 0); esta opción sólo se aplica a un objeto <strong>Field</strong> de una colección <strong>Fields</strong> de un objeto <strong>Index</strong>.</span><span class="sxs-lookup"><span data-stu-id="bf714-116">The field is sorted in descending (Z to A or 100 to 0) order; this option applies only to a <strong>Field</strong> object in a <strong>Fields</strong> collection of an <strong>Index</strong> object.</span></span> <span data-ttu-id="bf714-117">Si omite esta constante, el campo se ordena en orden ascendente (de A a Z o de 0 a 100).</span><span class="sxs-lookup"><span data-stu-id="bf714-117">If you omit this constant, the field is sorted in ascending (A to Z or 0 to 100) order.</span></span> <span data-ttu-id="bf714-118">Este es el valor predeterminado para campos <strong>Index</strong> y <strong>TableDef</strong> (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bf714-118">This is the default value for <strong>Index</strong> and <strong>TableDef</strong> fields (Microsoft Access workspaces only)..</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf714-119"><strong>dbFixedField</strong></span><span class="sxs-lookup"><span data-stu-id="bf714-119"><strong>dbFixedField</strong></span></span></p></td>
<td><p><span data-ttu-id="bf714-120">El tamaño de campo es fijo (valor predeterminado para los campos numéricos).</span><span class="sxs-lookup"><span data-stu-id="bf714-120">The field size is fixed (default for Numeric fields).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf714-121"><strong>dbHyperlinkField</strong></span><span class="sxs-lookup"><span data-stu-id="bf714-121"><strong>dbHyperlinkField</strong></span></span></p></td>
<td><p><span data-ttu-id="bf714-122">El campo contiene información de hipervínculo (sólo campos Memo).</span><span class="sxs-lookup"><span data-stu-id="bf714-122">The field contains hyperlink information (Memo fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf714-123"><strong>dbSystemField</strong></span><span class="sxs-lookup"><span data-stu-id="bf714-123"><strong>dbSystemField</strong></span></span></p></td>
<td><p><span data-ttu-id="bf714-124">El campo almacena información de replicación de réplicas, no puede eliminar este tipo de campo (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bf714-124">The field stores replication information for replicas; you can't delete this type of field (Microsoft Access workspace only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf714-125"><strong>dbUpdatableField</strong></span><span class="sxs-lookup"><span data-stu-id="bf714-125"><strong>dbUpdatableField</strong></span></span></p></td>
<td><p><span data-ttu-id="bf714-126">Puede cambiar el valor del campo.</span><span class="sxs-lookup"><span data-stu-id="bf714-126">The field value can be changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf714-127"><strong>dbVariableField</strong></span><span class="sxs-lookup"><span data-stu-id="bf714-127"><strong>dbVariableField</strong></span></span></p></td>
<td><p><span data-ttu-id="bf714-128">El tamaño del campo es variable (sólo campos de texto).</span><span class="sxs-lookup"><span data-stu-id="bf714-128">The field size is variable (Text fields only).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bf714-p103">Para un objeto que aún no se haya anexado a una colección, esta propiedad es de lectura y escritura. Para un objeto **Field** anexado, la disponibilidad de la propiedad **Attributes** depende del objeto que contenga la colección **Fields**.</span><span class="sxs-lookup"><span data-stu-id="bf714-p103">For an object not yet appended to a collection, this property is read/write. For an appended **Field** object, the availability of the **Attributes** property depends on the object that contains the **Fields** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bf714-131">Si el objeto Field pertenece a</span><span class="sxs-lookup"><span data-stu-id="bf714-131">If the Field object belongs to an</span></span></p></th>
<th><p><span data-ttu-id="bf714-132">Disponibilidad de Attributes</span><span class="sxs-lookup"><span data-stu-id="bf714-132">Then Attributes is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf714-133">Objeto <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="bf714-133"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="bf714-134">Lectura y escritura hasta que el objeto <strong>TableDef</strong> al que está anexado el objeto <strong>Index</strong> se anexe a un objeto <strong>Database</strong>, después, la propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bf714-134">Read/write until the <strong>TableDef</strong> object that the <strong>Index</strong> object is appended to is appended to a <strong>Database</strong> object; then the property is read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf714-135">
						Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="bf714-135"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="bf714-136">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bf714-136">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf714-137">
						Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="bf714-137"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="bf714-138">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bf714-138">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf714-139">
						Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="bf714-139"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="bf714-140">No admitido</span><span class="sxs-lookup"><span data-stu-id="bf714-140">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf714-141">
						Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="bf714-141"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="bf714-142">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="bf714-142">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bf714-p104">Si se establecen varios atributos, se pueden combinar sumando las constantes correspondientes. Los valores no válidos se omiten sin producir un error.</span><span class="sxs-lookup"><span data-stu-id="bf714-p104">When you set multiple attributes, you can combine them by summing the appropriate constants. Any invalid values are ignored without producing an error.</span></span>

## <a name="example"></a><span data-ttu-id="bf714-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bf714-145">Example</span></span>

<span data-ttu-id="bf714-146">En este ejemplo se muestra la propiedad **Attributes** de los objetos **Field**, **Relation** y **TableDef** en la base de datos Neptuno.</span><span class="sxs-lookup"><span data-stu-id="bf714-146">This example displays the **Attributes** property for **Field**, **Relation**, and **TableDef** objects in the Northwind database.</span></span>

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field 
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

