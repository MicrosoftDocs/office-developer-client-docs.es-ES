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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715315"
---
# <a name="fieldattributes-property-dao"></a>Propiedad Field.Attributes (DAO)


**Se aplica a**: Access 2013, Office 2013


Establece o devuelve un valor que indica una o varias características de un objeto **[Field](field-object-dao.md)**. **Long** de lectura y escritura.

## <a name="syntax"></a>Sintaxis

*expresión* . Atributos

*expresión* Variable que representa un objeto **Field** .

## <a name="remarks"></a>Observaciones

El valor especifica características del campo representado por el objeto **Field** y puede ser una combinación de las siguientes constantes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbAutoIncrField</strong></p></td>
<td><p>El valor del campo para nuevos registros se incrementa de forma automática en un valor de tipo Long integer único que no se puede modificar (en un área de trabajo de Microsoft Access, sólo se admite para tablas de bases de datos del motor de base de datos de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDescending</strong></p></td>
<td><p>El campo se ordena en orden descendente (de Z a A o de 100 a 0); esta opción sólo se aplica a un objeto <strong>Field</strong> de una colección <strong>Fields</strong> de un objeto <strong>Index</strong>. Si se omite esta constante, el campo se ordena en orden ascendente (de A a Z o de 0 a 100). Éste es el valor predeterminado para los campos <strong>Index</strong> y <strong>TableDef</strong> (sólo áreas de trabajo de Microsoft Access)..</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFixedField</strong></p></td>
<td><p>El tamaño del campo es fijo (valor predeterminado para los campos numéricos).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbHyperlinkField</strong></p></td>
<td><p>El campo contiene información de hipervínculo (sólo campos de tipo Memo).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSystemField</strong></p></td>
<td><p>El campo almacena información de réplica para las réplicas; este tipo de campo no se puede eliminar (solo en áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbUpdatableField</strong></p></td>
<td><p>El valor del campo se puede cambiar.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVariableField</strong></p></td>
<td><p>El tamaño del campo es variable (sólo campos de tipo Text).</p></td>
</tr>
</tbody>
</table>


Para un objeto que aún no se haya anexado a una colección, esta propiedad es de lectura y escritura. Para un objeto **Field** anexado, la disponibilidad de la propiedad **Attributes** depende del objeto que contenga la colección **Fields**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Si el objeto Field pertenece a</p></th>
<th><p>Disponibilidad de Attributes</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Objeto <strong>Index</strong></p></td>
<td><p>Lectura y escritura hasta que el objeto <strong>TableDef</strong> al que está anexado el objeto <strong>Index</strong> se anexe a un objeto <strong>Database</strong>; después, la propiedad es de sólo lectura.</p></td>
</tr>
<tr class="even">
<td><p>							Objeto <strong>QueryDef</strong></p></td>
<td><p>Solo lectura</p></td>
</tr>
<tr class="odd">
<td><p>							Objeto <strong>Recordset</strong></p></td>
<td><p>Solo lectura</p></td>
</tr>
<tr class="even">
<td><p>							Objeto <strong>Relation</strong></p></td>
<td><p>No admitido</p></td>
</tr>
<tr class="odd">
<td><p>							Objeto <strong>TableDef</strong></p></td>
<td><p>Lectura y escritura</p></td>
</tr>
</tbody>
</table>


Si se establecen varios atributos, se pueden combinar sumando las constantes correspondientes. Los valores no válidos se omiten sin producir un error.

## <a name="example"></a>Ejemplo

En este ejemplo, se muestra la propiedad **Attributes** para los objetos **Field**, **Relation** y **TableDef** de la base de datos Northwind.

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

