---
title: Field2.ForeignName Property (DAO)
TOCTitle: ForeignName Property
ms:assetid: 76da233a-efb4-63cd-a2a2-d18d9e2fb2fb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196027(v=office.15)
ms:contentKeyID: 48545708
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052932
f1_categories:
- Office.Version=v15
ms.openlocfilehash: eff81bf8d2e7f7f040611ffc1aafdedff1e35ddf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874051"
---
# <a name="field2foreignname-property-dao"></a>Field2.ForeignName Property (DAO)


**Se aplica a**: Access 2013, Office 2013

Establece o devuelve un valor que especifica el nombre del objeto **Field2** en una tabla externa que corresponde a un campo de una tabla primaria para una relación (sólo para áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . ForeignName

*expresión* Variable que representa un objeto **Field2** .

## <a name="remarks"></a>Observaciones

Si el objeto **[Relation](relation-object-dao.md)** no está anexado a la **[Database](database-object-dao.md)**, pero el objeto **Field2** está anexado al objeto **Relation**, la propiedad **ForeignName** es de lectura y escritura. Una vez que el objeto **Relation** se anexe a la base de datos, la propiedad **ForeignName** será de solo lectura.

Sólo un objeto **Field2** que pertenece a la colección **Fields** de un objeto **Relation** admite la propiedad **ForeignName**.

Los valores de las propiedades **[Name](connection-name-property-dao.md)** y **ForeignName** para un objeto **Field2** especifican los nombres de los correspondientes campos en las tablas primaria y externa de una relación. Los valores de las propiedades **[Table](relation-table-property-dao.md)** y **[ForeignTable](relation-foreigntable-property-dao.md)** para un objeto **Relation** determinan las tablas primaria y externa de una relación.

Por ejemplo, si tiene una lista de partes de códigos válidos, en un campo denominado PartNo, almacenada en una tabla ValidParts, podría establecer una relación con una tabla OrderItem como si una parte de un código estuviera contenida en la tabla OrderItem, lo que ya existiría en la tabla ValidParts. Si la parte del código no existe en la tabla ValidParts y no ha establecido la propiedad **[Attributes](field-attributes-property-dao.md)** del objeto **Relation** en **dbRelationDontEnforce**, se producirá un error capturable.

En este caso, la tabla ValidParts es la tabla externa, por lo que la propiedad **ForeignTable** del objeto **Relation** se podría establecer en ValidParts y la propiedad **Table** del objeto **Relation** se podría establecer en OrderItem. Las propiedades **Name** y **ForeignName** del objeto **Field2** en la colección **Fields** del objeto **Relation** se podría establecer en PartNo.

## <a name="example"></a>Ejemplo

En este ejemplo se muestra cómo las propiedades **Table**, **ForeignTable** y **ForeignName** definen los términos de **Relation** entre dos tablas.

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
