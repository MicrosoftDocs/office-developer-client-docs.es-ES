---
title: Método Recordset.Requery (DAO)
TOCTitle: Requery Method
ms:assetid: a5d66eb5-499c-4133-f6c3-c7a1619a8a11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821155(v=office.15)
ms:contentKeyID: 48546840
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: bd6f2fdf7d1f8ba9fc47c6223a8f872a655a1e3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307626"
---
# <a name="recordsetrequery-method-dao"></a>Método Recordset.Requery (DAO)

**Se aplica a:** Access 2013, Office 2013

Actualiza los datos en un objeto **[Recordset](recordset-object-dao.md)** al volver a ejecutar la consulta en la que se basa el objeto.

## <a name="syntax"></a>Sintaxis

*expression* .Requery(***NewQueryDef***)

*expression* Variable que representa un objeto **Recordset**.

## <a name="parameters"></a>Parameters

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Obligatorio/opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>NewQueryDef</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Representa el valor de la propiedad <strong>Name</strong> de un objeto <strong><a href="querydef-object-dao.md">QueryDef</a></strong></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Use este método para asegurarse de que un **Recordset** contiene los datos más recientes. Este método rellena el objeto **Recordset** usando los parámetros de consulta actuales o (en un área de trabajo de Microsoft Access) los nuevos parámetros proporcionados por el argumento newquerydef.

Si no especifica un argumento newquerydef, **Recordset** se rellena basándose en la misma definición de consulta y parámetros que se usaron originalmente para llenar **Recordset**. Cualquier cambio en los datos subyacentes se reflejará durante este nuevo relleno. Si no usó **QueryDef** para crear **Recordset**, **Recordset** se vuelve a crear desde cero.

Si especifica el objeto **QueryDef** original en el argumento newquerydef, se vuelve a consultar **Recordset** mediante los parámetros especificados por **QueryDef**. Los cambios realizados en los datos subyacentes se reflejarán durante este nuevo relleno. Para reflejar cualquier cambio en los valores de los parámetros de consulta en **Recordset**, debe proporcionar el argumento newquerydef.

Si especifica un objeto **QueryDef** diferente al que se usó originalmente para crear **Recordset**, **Recordset** se vuelve a crear desde cero.

Cuando usa **Requery**, el primer registro de **Recordset** se convierte en el registro activo.

No puede usar el método **Requery** en objetos **Recordset** de tipo dynaset o snapshot cuya propiedad **[Restartable](recordset-restartable-property-dao.md)** está establecida en **False**. No obstante, si proporciona el argumento opcional newquerydef, se omite la propiedad **Restartable**.

Si los dos valores de las propiedades **[BOF](recordset-bof-property-dao.md)** y **[EOF](recordset-eof-property-dao.md)** del objeto **Recordset** son **True** después de usar el método **Requery**, la consulta no devuelve ningún registro y **Recordset** no contiene datos.

## <a name="example"></a>Ejemplo

Este ejemplo muestra cómo el método **Requery** puede usarse para actualizar una consulta después de cambiar los datos subyacentes.

```vb
    Sub RequeryX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim rstView As Recordset 
     Dim rstChange As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
     "PARAMETERS ViewCountry Text; " & _ 
     "SELECT FirstName, LastName, Country FROM " & _ 
     "Employees WHERE Country = [ViewCountry] " & _ 
     "ORDER BY LastName") 
     
     qdfTemp.Parameters!ViewCountry = "USA" 
     Debug.Print "Data after initial query, " & _ 
     [ViewCountry] = USA" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Change underlying data. 
     Set rstChange = dbsNorthwind.OpenRecordset("Employees") 
     rstChange.AddNew 
     rstChange!FirstName = "Nina" 
     rstChange!LastName = "Roberts" 
     rstChange!Country = "USA" 
     rstChange.Update 
     
     rstView.Requery 
     Debug.Print "Requery after changing underlying data" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Restore original data because this is only a 
     ' demonstration. 
     rstChange.Bookmark = rstChange.LastModified 
     rstChange.Delete 
     rstChange.Close 
     
     rstView.Close 
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

En este ejemplo se muestra cómo se puede utilizar el método **Requery** para actualizar una consulta después de cambiar los parámetros de consulta.

```vb 
Sub RequeryX2() 
 
 Dim dbsNorthwind As Database 
 Dim qdfTemp As QueryDef 
 Dim prmCountry As Parameter 
 Dim rstView As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
 "PARAMETERS ViewCountry Text; " & _ 
 "SELECT FirstName, LastName, Country FROM " & _ 
 "Employees WHERE Country = [ViewCountry] " & _ 
 "ORDER BY LastName") 
 Set prmCountry = qdfTemp.Parameters!ViewCountry 
 
 qdfTemp.Parameters!ViewCountry = "USA" 
 Debug.Print "Data after initial query, " & _ 
 [ViewCountry] = USA" 
 Set rstView = qdfTemp.OpenRecordset 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 ' Change query parameter. 
 qdfTemp.Parameters!ViewCountry = "UK" 
 ' QueryDef argument must be included so that the 
 ' resulting Recordset reflects the change in the query 
 ' parameter. 
 rstView.Requery qdfTemp 
 Debug.Print "Requery after changing parameter, " & _ 
 "[ViewCountry] = UK" 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 rstView.Close 
 dbsNorthwind.Close 
 
End Sub 
 
```

