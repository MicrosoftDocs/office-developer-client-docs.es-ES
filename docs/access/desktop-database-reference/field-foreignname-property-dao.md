---
title: Propiedad Field. ForeignName (DAO)
TOCTitle: ForeignName Property
ms:assetid: 5f412ab4-173b-9530-eb4f-71ee30bed9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194762(v=office.15)
ms:contentKeyID: 48545157
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7c340eee9972e8247654ec863ba0ef4588ef65f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293108"
---
# <a name="fieldforeignname-property-dao"></a>Propiedad Field. ForeignName (DAO)


**Se aplica a:** Access 2013, Office 2013

Establece o devuelve un valor que especifica el nombre del objeto **[Field](field-object-dao.md)** en una tabla externa que corresponde a un campo en una tabla primaria para una relación (sólo para áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . ForeignName

*expresión* Variable que representa un objeto **Field** .

## <a name="remarks"></a>Comentarios

Si el objeto **[Relation](relation-object-dao.md)** no está anexado a la **[Database](database-object-dao.md)**, pero el objeto **Field** está anexado al objeto **Relation**, la propiedad **ForeignName** es de lectura y escritura. Una vez que el objeto **Relation** se anexe a la base de datos, la propiedad **ForeignName** será de solo lectura.

Sólo un objeto **Field** que pertenece a la colección **Fields** de un objeto **Relation** admite la propiedad **ForeignName**.

Los valores de las propiedades **[Name](connection-name-property-dao.md)** y **ForeignName** para un objeto **Field** especifican los nombres de los correspondientes campos en las tablas primaria y externa de una relación. Los valores de las propiedades **[Table](relation-table-property-dao.md)** y **[ForeignTable](relation-foreigntable-property-dao.md)** para un objeto **Relation** determinan las tablas primaria y externa de una relación.

Por ejemplo, si tiene una lista de partes de códigos válidos, en un campo denominado PartNo, almacenada en una tabla ValidParts, podría establecer una relación con una tabla OrderItem como si una parte de un código estuviera contenida en la tabla OrderItem, lo que ya existiría en la tabla ValidParts. Si la parte del código no existe en la tabla ValidParts y no ha establecido la propiedad **[Attributes](field-attributes-property-dao.md)** del objeto **Relation** en **dbRelationDontEnforce**, se producirá un error capturable.

En este caso, la tabla ValidParts es la tabla externa, por lo que la propiedad **ForeignTable** del objeto **Relation** se podría establecer en ValidParts y la propiedad **Table** del objeto **Relation** se podría establecer en OrderItem. Las propiedades **Name** y **ForeignName** del objeto **Field** en la colección **Fields** del objeto **Relation** se podría establecer en PartNo.

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
