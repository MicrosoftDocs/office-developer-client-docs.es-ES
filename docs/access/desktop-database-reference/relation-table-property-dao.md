---
title: Propiedad reLation. Table (DAO)
TOCTitle: Table Property
ms:assetid: cc4f64ef-c4e9-1a14-9263-5f8220d89840
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834423(v=office.15)
ms:contentKeyID: 48547736
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053068
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 91a3262d92350618c2385013983020669b28ea5c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306996"
---
# <a name="relationtable-property-dao"></a><span data-ttu-id="e3688-102">Propiedad reLation. Table (DAO)</span><span class="sxs-lookup"><span data-stu-id="e3688-102">Relation.Table property (DAO)</span></span>


<span data-ttu-id="e3688-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e3688-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e3688-p101">Indica el nombre de la tabla principal de un objeto **[Relation](relation-object-dao.md)**. El resultado debe ser el mismo que el valor de la propiedad **[Name](connection-name-property-dao.md)** de un objeto **[TableDef](tabledef-object-dao.md)** o **[QueryDef](querydef-object-dao.md)** (únicamente áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="e3688-p101">Indicates the name of a **[Relation](relation-object-dao.md)** object's primary table. This should be equal to the **[Name](connection-name-property-dao.md)** property setting of a **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="e3688-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3688-106">Syntax</span></span>

<span data-ttu-id="e3688-107">*expresión* . Table</span><span class="sxs-lookup"><span data-stu-id="e3688-107">*expression* .Table</span></span>

<span data-ttu-id="e3688-108">*expresión* Variable que representa un objeto \*\*\*\* Relation.</span><span class="sxs-lookup"><span data-stu-id="e3688-108">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3688-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e3688-109">Remarks</span></span>

<span data-ttu-id="e3688-110">El valor de la propiedad **Table** es de lectura y escritura para un objeto **Relation** nuevo que no se haya anexado todavía a una colección, y de sólo lectura para un objeto **Relation** existente en una colección **[Relations](relations-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="e3688-110">The **Table** property setting is read/write for a new **Relation** object not yet appended to a collection and read-only for an existing **Relation** object in a **[Relations](relations-collection-dao.md)** collection.</span></span>

<span data-ttu-id="e3688-p102">Use la propiedad **Table** con la propiedad **[ForeignTable](relation-foreigntable-property-dao.md)** para definir un objeto **Relation**, que representa la relación entre campos de dos tablas o consultas. Establezca la propiedad **Table** en el valor de la propiedad **Name** del objeto **TableDef** o **QueryDef** principal, y establezca la propiedad **ForeignTable** en el valor de la propiedad **Name** del objeto **TableDef** o **QueryDef** externo (al que se hacer referencia). La propiedad **[Attributes](field-attributes-property-dao.md)** determina el tipo de relación entre los dos objetos.</span><span class="sxs-lookup"><span data-stu-id="e3688-p102">Use the **Table** property with the **[ForeignTable](relation-foreigntable-property-dao.md)** property to define a **Relation** object, which represents the relationship between fields in two tables or queries. Set the **Table** property to the **Name** property setting of the primary **TableDef** or **QueryDef** object, and set the **ForeignTable** property to the **Name** property setting of the foreign (referencing) **TableDef** or **QueryDef** object. The **[Attributes](field-attributes-property-dao.md)** property determines the type of relationship between the two objects.</span></span>

<span data-ttu-id="e3688-p103">Por ejemplo, si tuviera una lista de códigos de piezas válidas (en un campo denominado PartNo) almacenada en una tabla ValidParts, podría establecer una relación de uno a varios con una tabla OrderItem de modo que si se introdujera un código de pieza en la tabla OrderItem, tendría que estar ya en la tabla ValidParts. Si el código de pieza no existiese en la tabla ValidParts y no hubiera establecido la propiedad **Attributes** del objeto **Relation** en **dbRelationDontEnforce**, se produciría un error capturable.</span><span class="sxs-lookup"><span data-stu-id="e3688-p103">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a one-to-many relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already be in the ValidParts table. If the part code didn't exist in the ValidParts table and you had not set the **Attributes** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="e3688-p104">En este caso, la tabla ValidParts es la tabla principal, por lo que la propiedad **Table** del objeto **Relation** se establecería en ValidParts y la propiedad **ForeignTable** del objeto **Relation** se establecería en OrderItem. Las propiedades **Name** y **ForeignName** del objeto **[Field](field-object-dao.md)** de la colección [**Fields**](fields-collection-dao.md) del objeto **Relation** se establecerían en PartNo.</span><span class="sxs-lookup"><span data-stu-id="e3688-p104">In this case, the ValidParts table is the primary table, so the **Table** property of the **Relation** object would be set to ValidParts and the **ForeignTable** property of the **Relation** object would be set to OrderItem. The **Name** and **ForeignName** properties of the **[Field](field-object-dao.md)** object in the **Relation** object's **[Fields](fields-collection-dao.md)** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="e3688-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e3688-118">Example</span></span>

<span data-ttu-id="e3688-119">En este ejemplo se muestra cómo las propiedades **Table**, **ForeignTable** y **ForeignName** definen los términos de un objeto **Relation** entre dos tablas.</span><span class="sxs-lookup"><span data-stu-id="e3688-119">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

```vb
    Sub ForeignNameX() 
     
     Dim dbsNorthwind As Database 
     Dim relLoop As Relation 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     Debug.Print "Relation" 
     Debug.Print " Table - Field" 
     Debug.Print " Primary (One) "; 
     Debug.Print ".Table - .Fields(0).Name" 
     Debug.Print " Foreign (Many) "; 
     Debug.Print ".ForeignTable - .Fields(0).ForeignName" 
     
     ' Enumerate the Relations collection of the Northwind 
     ' database to report on the property values of 
     ' the Relation objects and their Field objects. 
     For Each relLoop In dbsNorthwind.Relations 
     With relLoop 
     Debug.Print 
     Debug.Print .Name & " Relation" 
     Debug.Print " Table - Field" 
     Debug.Print " Primary (One) "; 
     Debug.Print .Table & " - " & .Fields(0).Name 
     Debug.Print " Foreign (Many) "; 
     Debug.Print .ForeignTable & " - " & _ 
     .Fields(0).ForeignName 
     End With 
     Next relLoop 
     
     dbsNorthwind.Close 
     
    End Sub
```
