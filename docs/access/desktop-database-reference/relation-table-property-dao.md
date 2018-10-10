---
title: Relation.Table Property (DAO)
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
ms.openlocfilehash: ba1c70a9aded0ce26cd24d2dc25ecb65c30b1f8e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485371"
---
# <a name="relationtable-property-dao"></a>Relation.Table Property (DAO)


**Se aplica a**: Access 2013 | Office 2013

Indica el nombre de la tabla principal de un objeto **[Relation](relation-object-dao.md)**. El resultado debe ser el mismo que el valor de la propiedad **[Name](connection-name-property-dao.md)** de un objeto **[TableDef](tabledef-object-dao.md)** o **[QueryDef](querydef-object-dao.md)** (únicamente áreas de trabajo de Microsoft Access).

## <a name="syntax"></a>Sintaxis

*expresión* . Tabla

*expresión* Variable que representa un objeto **Relation** .

## <a name="remarks"></a>Observaciones

El valor de la propiedad **Table** es de lectura y escritura para un objeto **Relation** nuevo que no se haya anexado todavía a una colección, y de sólo lectura para un objeto **Relation** existente en una colección **[Relations](relations-collection-dao.md)**.

Use la propiedad **Table** con la propiedad **[ForeignTable](relation-foreigntable-property-dao.md)** para definir un objeto **Relation**, que representa la relación entre campos de dos tablas o consultas. Establezca la propiedad **Table** en el valor de la propiedad **Name** del objeto **TableDef** o **QueryDef** principal, y establezca la propiedad **ForeignTable** en el valor de la propiedad **Name** del objeto **TableDef** o **QueryDef** externo (al que se hacer referencia). La propiedad **[Attributes](field-attributes-property-dao.md)** determina el tipo de relación entre los dos objetos.

Por ejemplo, si tuviera una lista de códigos de piezas válidas (en un campo denominado PartNo) almacenada en una tabla ValidParts, podría establecer una relación de uno a varios con una tabla OrderItem de modo que si se introdujera un código de pieza en la tabla OrderItem, tendría que estar ya en la tabla ValidParts. Si el código de pieza no existiese en la tabla ValidParts y no hubiera establecido la propiedad **Attributes** del objeto **Relation** en **dbRelationDontEnforce**, se produciría un error capturable.

En este caso, la tabla ValidParts es la tabla principal, por lo que la propiedad **Table** del objeto **Relation** se establecería en ValidParts y la propiedad **ForeignTable** del objeto **Relation** se establecería en OrderItem. Las propiedades **Name** y **ForeignName** del objeto **[Field](field-object-dao.md)** de la colección [**Fields**](fields-collection-dao.md) del objeto **Relation** se establecerían en PartNo.

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
