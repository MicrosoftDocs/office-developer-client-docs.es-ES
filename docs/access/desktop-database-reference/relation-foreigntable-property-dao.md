---
title: Propiedad reLation. ForeignTable (DAO)
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
# <a name="relationforeigntable-property-dao"></a>Propiedad reLation. ForeignTable (DAO)


**Se aplica a:** Access 2013, Office 2013

Establece o devuelve el nombre de la tabla externa en una relación (solo áreas de trabajo de Microsoft Access). .

## <a name="syntax"></a>Sintaxis

*expresión* . TablaExterna

*expresión* Variable que representa un objeto **** Relation.

## <a name="remarks"></a>Comentarios

Esta propiedad es de lectura y escritura para un nuevo objeto **[Relation](relation-object-dao.md)** que todavía no está anexado a una colección y es de solo lectura para un objeto **Relation** existente en la colección **[Relations](relations-collection-dao.md)**.

El valor de la propiedad **ForeignTable** de un objeto **Relation** es el valor de la propiedad **[Name](connection-name-property-dao.md)** del objeto **[TableDef](tabledef-object-dao.md)** o **[QueryDef](querydef-object-dao.md)** que representa la tabla externa o consulta; el valor de la propiedad **[Table](relation-table-property-dao.md)** es el valor de la propiedad **Name** del objeto **TableDef** o **QueryDef** que representa la tabla principal o consulta.

Por ejemplo, si tiene una lista de partes de códigos válidos, en un campo denominado PartNo, almacenada en una tabla ValidParts, podría establecer una relación con una tabla OrderItem como si una parte de un código estuviera contenida en la tabla OrderItem, lo que ya estaría en la tabla ValidParts. Si la parte del código no existe en la tabla ValidParts y no ha establecido la propiedad **[Attributes](field-attributes-property-dao.md)** del objeto **Relation** en **dbRelationDontEnforce**, se producirá un error capturable.

En este caso, la tabla ValidParts es la tabla principal, por lo que la propiedad **Table** del objeto **Relation** se podría establecer en ValidParts y la propiedad **ForeignTable** del objeto **Relation** se podría establecer en OrderItem. Las propiedades **Name** y **ForeignName** del objeto **Field** en la colección **Fields** del objeto **Relation** se podría establecer en PartNo.

## <a name="example"></a>Ejemplo

En este ejemplo se muestra cómo las propiedades **Table**, **ForeignTable** y **ForeignName** definen los términos de un objeto **Relation** entre dos tablas.

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
