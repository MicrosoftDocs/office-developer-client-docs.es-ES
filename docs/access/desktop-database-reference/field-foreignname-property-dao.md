---
title: Field.ForeignName Property (DAO)
TOCTitle: ForeignName Property
ms:assetid: 5f412ab4-173b-9530-eb4f-71ee30bed9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194762(v=office.15)
ms:contentKeyID: 48545157
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9366124a6d78358a184f25a0881e84ee27d6f86d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483401"
---
# <a name="fieldforeignname-property-dao"></a><span data-ttu-id="c2476-102">Field.ForeignName Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="c2476-102">Field.ForeignName Property (DAO)</span></span>


<span data-ttu-id="c2476-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2476-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c2476-104">Establece o devuelve un valor que especifica el nombre del objeto **[Field](field-object-dao.md)** en una tabla externa que corresponde a un campo en una tabla primaria para una relación (sólo para áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="c2476-104">Sets or returns a value that specifies the name of the **[Field](field-object-dao.md)** object in a foreign table that corresponds to a field in a primary table for a relationship (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="c2476-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2476-105">Syntax</span></span>

<span data-ttu-id="c2476-106">*expresión* . ForeignName</span><span class="sxs-lookup"><span data-stu-id="c2476-106">*expression* .ForeignName</span></span>

<span data-ttu-id="c2476-107">*expresión* Variable que representa un objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="c2476-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2476-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2476-108">Remarks</span></span>

<span data-ttu-id="c2476-p101">Si el objeto **[Relation](relation-object-dao.md)** no está anexado a la **[Database](database-object-dao.md)**, pero el objeto **Field** está anexado al objeto **Relation**, la propiedad **ForeignName** es de lectura y escritura. Una vez que el objeto **Relation** se anexe a la base de datos, la propiedad **ForeignName** será de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c2476-p101">If the **[Relation](relation-object-dao.md)** object isn't appended to the **[Database](database-object-dao.md)**, but the **Field** is appended to the **Relation** object, the **ForeignName** property is read/write. Once the **Relation** object is appended to the database, the **ForeignName** property is read-only.</span></span>

<span data-ttu-id="c2476-111">Sólo un objeto **Field** que pertenece a la colección **Fields** de un objeto **Relation** admite la propiedad **ForeignName**.</span><span class="sxs-lookup"><span data-stu-id="c2476-111">Only a **Field** object that belongs to the **Fields** collection of a **Relation** object can support the **ForeignName** property.</span></span>

<span data-ttu-id="c2476-p102">Los valores de las propiedades **[Name](connection-name-property-dao.md)** y **ForeignName** para un objeto **Field** especifican los nombres de los correspondientes campos en las tablas primaria y externa de una relación. Los valores de las propiedades **[Table](relation-table-property-dao.md)** y **[ForeignTable](relation-foreigntable-property-dao.md)** para un objeto **Relation** determinan las tablas primaria y externa de una relación.</span><span class="sxs-lookup"><span data-stu-id="c2476-p102">The **[Name](connection-name-property-dao.md)** and **ForeignName** property settings for a **Field** object specify the names of the corresponding fields in the primary and foreign tables of a relationship. The **[Table](relation-table-property-dao.md)** and **[ForeignTable](relation-foreigntable-property-dao.md)** property settings for a **Relation** object determine the primary and foreign tables of a relationship.</span></span>

<span data-ttu-id="c2476-p103">Por ejemplo, si tiene una lista de partes de códigos válidos, en un campo denominado PartNo, almacenada en una tabla ValidParts, podría establecer una relación con una tabla OrderItem como si una parte de un código estuviera contenida en la tabla OrderItem, lo que ya existiría en la tabla ValidParts. Si la parte del código no existe en la tabla ValidParts y no ha establecido la propiedad **[Attributes](field-attributes-property-dao.md)** del objeto **Relation** en **dbRelationDontEnforce**, se producirá un error capturable.</span><span class="sxs-lookup"><span data-stu-id="c2476-p103">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already exist in the ValidParts table. If the part code didn't exist in the ValidParts table and you had not set the **[Attributes](field-attributes-property-dao.md)** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="c2476-p104">En este caso, la tabla ValidParts es la tabla externa, por lo que la propiedad **ForeignTable** del objeto **Relation** se podría establecer en ValidParts y la propiedad **Table** del objeto **Relation** se podría establecer en OrderItem. Las propiedades **Name** y **ForeignName** del objeto **Field** en la colección **Fields** del objeto **Relation** se podría establecer en PartNo.</span><span class="sxs-lookup"><span data-stu-id="c2476-p104">In this case, the ValidParts table is the foreign table, so the **ForeignTable** property of the **Relation** object would be set to ValidParts and the **Table** property of the **Relation** object would be set to OrderItem. The **Name** and **ForeignName** properties of the **Field** object in the **Relation** object's **Fields** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="c2476-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c2476-118">Example</span></span>

<span data-ttu-id="c2476-119">En este ejemplo se muestra cómo las propiedades **Table**, **ForeignTable** y **ForeignName** definen los términos de **Relation** entre dos tablas.</span><span class="sxs-lookup"><span data-stu-id="c2476-119">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

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