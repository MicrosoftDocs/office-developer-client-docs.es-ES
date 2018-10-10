---
title: Property.Inherited Property (DAO)
TOCTitle: Inherited Property
ms:assetid: 10e624db-2301-b9be-beca-6e8caccf7274
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845349(v=office.15)
ms:contentKeyID: 48543304
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052991
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b89b751f96b78cf972d6461ce646498d82bc9169
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485176"
---
# <a name="propertyinherited-property-dao"></a>Property.Inherited Property (DAO)


**Se aplica a**: Access 2013 | Office 2013 

Devuelve un valor que indica si se hereda un objeto **[Property](property-object-dao.md)** desde un objeto base.

## <a name="syntax"></a>Sintaxis

*expresión* . Heredado

*expresión* Variable que representa un objeto **Property** .

## <a name="remarks"></a>Observaciones

Para objetos **Property** integrados que representan propiedades predefinidas, el único valor devuelto posible es **False**.

Puede utilizar la propiedad **Inherited** para determinar si una propiedad **Property** definida por el usuario se creó para el objeto al que se aplica, o si la **Property** se heredó desde otro objeto. Por ejemplo, suponga que crea una nueva **Property** para un objeto **[QueryDef](querydef-object-dao.md)** y después abre un objeto **[Recordset](recordset-object-dao.md)** desde el objeto **QueryDef**. Esta nueva **Property** será parte de la colección [**Properties**](properties-collection-dao.md) de los objetos **Recordset** y su propiedad **Inherited** se establecerá en **True** debido a que la propiedad se creó para el objeto **QueryDef** y no para el objeto **Recordset**.

## <a name="example"></a>Ejemplo

En este ejemplo se usa la propiedad **Inherited** para determinar si un objeto **Property** definido por el usuario se creó para un objeto **Recordset** o para algún objeto base.

```vb 
Sub InheritedX() 
 
 Dim dbsNorthwind As Database 
 Dim tdfTest As TableDef 
 Dim rstTest As Recordset 
 Dim prpNew As Property 
 Dim prpLoop As Property 
 
 ' Create a new property for a saved TableDef object, then 
 ' open a recordset from that TableDef object. 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set tdfTest = dbsNorthwind.TableDefs(0) 
 Set prpNew = tdfTest.CreateProperty("NewProperty", _ 
 dbBoolean, True) 
 tdfTest.Properties.Append prpNew 
 Set rstTest = tdfTest.OpenRecordset(dbOpenForwardOnly) 
 
 ' Show Name and Inherited property of the new Property 
 ' object in the TableDef. 
 Debug.Print "NewProperty of " & tdfTest.Name & _ 
 " TableDef:" 
 Debug.Print " Inherited = " & _ 
 tdfTest.Properties("NewProperty").Inherited 
 
 ' Show Name and Inherited property of the new Property 
 ' object in the Recordset. 
 Debug.Print "NewProperty of " & rstTest.Name & _ 
 " Recordset:" 
 Debug.Print " Inherited = " & _ 
 rstTest.Properties("NewProperty").Inherited 
 
 ' Delete new TableDef because this is a demonstration. 
 tdfTest.Properties.Delete prpNew.Name 
 dbsNorthwind.Close 
 
End Sub 
 
```

