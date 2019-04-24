---
title: 'Capítulo 3: Examen de datos'
TOCTitle: 'Chapter 3: Examining data'
ms:assetid: 73c69134-3127-3344-d5c3-5ecb9e0e958b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249474(v=office.15)
ms:contentKeyID: 48545648
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fcf837a02c40d11fecfa56b8aa34ac80a848411
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296461"
---
# <a name="chapter-3-examining-data"></a>Capítulo 3: Examen de datos

**Se aplica a:** Access 2013, Office 2013

El Capítulo 2 explicaba cómo se recuperan datos de un origen de datos en forma de objeto **Recordset**. En este capítulo se analizará con más detalle el objeto **Recordset**, incluyendo la forma de navegar a través de **Recordset** y ver sus datos.

Los objetos **Recordset** tienen métodos y propiedades que se diseñaron para facilitar el desplazamiento por ellos y examinar su contenido. En función de la funcionalidad admitida por el proveedor, algunas propiedades o métodos de **Recordset** pueden no estar disponibles. Para continuar explorando el objeto **Recordset**, considere un objeto **Recordset** que sería devuelto por la base de datos de ejemplo Neptuno en Microsoft SQL Server 2000, usando el código siguiente:

```vb 
 
'BeginRsTour 
Public Sub RecordsetTour() 
 On Error GoTo ErrHandler: 
 
 Dim objRs As New ADODB.Recordset 
 Dim strSQL As String 
 
 strSQL = "SELECT ProductID, ProductName, UnitPrice FROM Products " & _ 
 "WHERE CategoryID = 7" '7 = Produce 
 
 objRs.Open strSQL, strConnStr, adOpenForwardOnly, _ 
 adLockReadOnly, adCmdText 
 
 'Clean up 
 objRs.Close 
 Set objRs = Nothing 
 Exit Sub 
 
ErrHandler: 
 If Not objRs Is Nothing Then 
 If objRs.State = adStateOpen Then objRs.Close 
 Set objRs = Nothing 
 End If 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndRsTour 
```

<br/>

Esta consulta SQL devuelve un objeto **Recordset** con cinco filas (registros) y tres columnas (campos). En la tabla siguiente se muestran los valores correspondientes a cada fila.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>CAMPO 0<br />
Nombre = IdProducto</p></th>
<th><p>CAMPO 1<br />
Nombre = NombreProducto</p></th>
<th><p>CAMPO 2<br />
Name = UnitPrice</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0,7</p></td>
<td><p>Uncle Bob's Organic Dried Pears</p></td>
<td><p>30,0000</p></td>
</tr>
<tr class="even">
<td><p>apartado</p></td>
<td><p>Judías</p></td>
<td><p>23,2500</p></td>
</tr>
<tr class="odd">
<td><p>28</p></td>
<td><p>Rssle Sauerkraut</p></td>
<td><p>45,6000</p></td>
</tr>
<tr class="even">
<td><p>51</p></td>
<td><p>Manjimup Dried Apples</p></td>
<td><p>53,0000</p></td>
</tr>
<tr class="odd">
<td><p>74</p></td>
<td><p>Longlife Tofu</p></td>
<td><p>10,0000</p></td>
</tr>
</tbody>
</table>


En la siguiente sección se explica cómo buscar la posición actual del cursor en este **conjunto de registros**de ejemplo.

En este capítulo, se tratan los temas siguientes:

- [Buscar el registro actual (ADO)](locating-the-current-record.md)
- [DesPlazarse por los datos (ADO)](navigating-through-the-data.md)
- [Información sobre la estructura del objeto Recordset (ADO)](understanding-recordset-structure.md)
