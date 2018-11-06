---
title: Método Recordset.Requery (DAO)
TOCTitle: Requery Method
ms:assetid: a5d66eb5-499c-4133-f6c3-c7a1619a8a11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821155(v=office.15)
ms:contentKeyID: 48546840
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d5c98eeb94e49693cf13d358987307f61f15069c
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998339"
---
# <a name="recordsetrequery-method-dao"></a>Método Recordset.Requery (DAO)

**Se aplica a**: Access 2013, Office 2013

Actualiza los datos de un objeto **[Recordset](recordset-object-dao.md)** volviendo a ejecutar la consulta en la que se basa el objeto.

## <a name="syntax"></a>Sintaxis

*expresión* . Requery (***NewQueryDef***)

*expresión* Variable que representa un objeto **Recordset** .

## <a name="parameters"></a>Parámetros

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
<td><p>Representa el valor de la propiedad <strong>Name</strong> de un objeto <strong><a href="querydef-object-dao.md">QueryDef</a></strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Observaciones

Use este método para asegurarse de que un objeto **Recordset** contiene los datos más recientes. Este método rellena el actual **objeto Recordset** mediante el uso de los parámetros de consulta actuales o (en un área de trabajo de Microsoft Access) los nuevos proporcionados por el argumento newquerydef.

Si no especifica un argumento newquerydef, el **objeto Recordset** se rellena volver a según la misma definición de consulta y los parámetros que se utilizaron originalmente para llenar el **conjunto de registros**. Cualquier cambio en los datos subyacentes se reflejará durante este nuevo relleno. Si no usó **QueryDef** para crear **Recordset**, **Recordset** se vuelve a crear desde cero.

Si especifica **QueryDef** original en el argumento newquerydef, a continuación, se vuelve a consultar el **conjunto de registros** mediante los parámetros especificados por **QueryDef**. Cualquier cambio en los datos subyacentes se reflejará durante este nuevo relleno. Para reflejar los cambios realizados en los valores de parámetro de consulta en el **conjunto de registros**, debe proporcionar el argumento newquerydef.

Si especifica un objeto **QueryDef** diferente al que se usó originalmente para crear **Recordset**, **Recordset** se vuelve a crear desde cero.

Cuando usa **Requery**, el primer registro de **Recordset** se convierte en el registro activo.

No puede usar el método **Requery** en objetos **Recordset** de tipo dynaset o snapshot cuya propiedad **[Restartable](recordset-restartable-property-dao.md)** está establecida en **False**. Sin embargo, si se proporciona el argumento opcional newquerydef, se omite la propiedad **Restartable** .

Si los dos valores de las propiedades **[BOF](recordset-bof-property-dao.md)** y **[EOF](recordset-eof-property-dao.md)** del objeto **Recordset** son **True** después de usar el método **Requery**, la consulta no devuelve ningún registro y **Recordset** no contiene datos.

## <a name="example"></a>Ejemplo

En este ejemplo se muestra cómo se puede utilizar el método **Requery** para actualizar una consulta después de cambiar los datos subyacentes.

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

