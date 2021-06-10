---
title: Propiedad Relation.ForeignTable (DAO)
TOCTitle: ForeignTable Property
ms:assetid: 3f896433-2962-1c7c-f5a2-4e030ba8d4a0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192853(v=office.15)
ms:contentKeyID: 48544401
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052989
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fc7ee9b5bc832cc2a125024c592db2c7b13e72f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307050"
---
# <a name="relationforeigntable-property-dao"></a><span data-ttu-id="7743c-102">Propiedad Relation.ForeignTable (DAO)</span><span class="sxs-lookup"><span data-stu-id="7743c-102">Relation.ForeignTable property (DAO)</span></span>


<span data-ttu-id="7743c-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7743c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7743c-p101">Establece o devuelve el nombre de la tabla externa en una relación (solo en áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="7743c-p101">Sets or returns the name of the foreign table in a relationship (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="7743c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7743c-106">Syntax</span></span>

<span data-ttu-id="7743c-107">*expresión* . ForeignTable</span><span class="sxs-lookup"><span data-stu-id="7743c-107">*expression* .ForeignTable</span></span>

<span data-ttu-id="7743c-108">*expresión* Variable que representa un **objeto Relation.**</span><span class="sxs-lookup"><span data-stu-id="7743c-108">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7743c-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7743c-109">Remarks</span></span>

<span data-ttu-id="7743c-110">Esta propiedad es de lectura y escritura para un nuevo objeto **[Relation](relation-object-dao.md)** que todavía no está anexado a una colección y es de solo lectura para un objeto **Relation** existente en la colección **[Relations](relations-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="7743c-110">This property is read/write for a new **[Relation](relation-object-dao.md)** object not yet appended to a collection and read-only for an existing **Relation** object in the **[Relations](relations-collection-dao.md)** collection.</span></span>

<span data-ttu-id="7743c-111">El valor de la propiedad **ForeignTable** de un objeto **Relation** es el valor de la propiedad **[Name](connection-name-property-dao.md)** del objeto **[TableDef](tabledef-object-dao.md)** o **[QueryDef](querydef-object-dao.md)** que representa la tabla externa o consulta; el valor de la propiedad **[Table](relation-table-property-dao.md)** es el valor de la propiedad **Name** del objeto **TableDef** o **QueryDef** que representa la tabla principal o consulta.</span><span class="sxs-lookup"><span data-stu-id="7743c-111">The **ForeignTable** property setting of a **Relation** object is the **[Name](connection-name-property-dao.md)** property setting of the **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** object that represents the foreign table or query; the **[Table](relation-table-property-dao.md)** property setting is the **Name** property setting of the **TableDef** or **QueryDef** object that represents the primary table or query.</span></span>

<span data-ttu-id="7743c-p102">Por ejemplo, si tiene una lista de partes de códigos válidos, en un campo denominado PartNo, almacenada en una tabla ValidParts, podría establecer una relación con una tabla OrderItem como si una parte de un código estuviera contenida en la tabla OrderItem, lo que ya estaría en la tabla ValidParts. Si la parte del código no existe en la tabla ValidParts y no ha establecido la propiedad **[Attributes](field-attributes-property-dao.md)** del objeto **Relation** en **dbRelationDontEnforce**, se producirá un error capturable.</span><span class="sxs-lookup"><span data-stu-id="7743c-p102">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already be in the ValidParts table. If the part code didn't exist in the ValidParts table and you had not set the **[Attributes](field-attributes-property-dao.md)** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="7743c-p103">En este caso, la tabla ValidParts es la tabla principal, por lo que la propiedad **Table** del objeto **Relation** se podría establecer en ValidParts y la propiedad **ForeignTable** del objeto **Relation** se podría establecer en OrderItem. Las propiedades **Name** y **ForeignName** del objeto **Field** en la colección **Fields** del objeto **Relation** se podría establecer en PartNo.</span><span class="sxs-lookup"><span data-stu-id="7743c-p103">In this case, the ValidParts table is the primary table, so the **Table** property of the **Relation** object would be set to ValidParts and the **ForeignTable** property of the **Relation** object would be set to OrderItem. The **Name** and **ForeignName** properties of the **Field** object in the **Relation** object's **Fields** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="7743c-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7743c-116">Example</span></span>

<span data-ttu-id="7743c-117">En este ejemplo se muestra cómo las propiedades **Table**, **ForeignTable** y **ForeignName** definen los términos de un objeto **Relation** entre dos tablas.</span><span class="sxs-lookup"><span data-stu-id="7743c-117">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

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
