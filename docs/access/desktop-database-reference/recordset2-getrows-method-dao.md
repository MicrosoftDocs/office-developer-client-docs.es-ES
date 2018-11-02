---
title: Recordset2.GetRows (método) (DAO)
TOCTitle: GetRows Method
ms:assetid: e5c0a082-e9d2-359f-fed5-835ab91d2311
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835959(v=office.15)
ms:contentKeyID: 48548367
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d0489361a3c739527fb44db0c566986dc2a40a0
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921400"
---
# <a name="recordset2getrows-method-dao"></a>Recordset2.GetRows (método) (DAO)


**Se aplica a**: Access 2013, Office 2013

Recupera varias filas de un objeto **[Recordset](recordset-object-dao.md)**.

## <a name="syntax"></a>Sintaxis

*expresión* . GetRows (***NumRows***)

*expresión* Variable que representa un objeto **Recordset2** .

### <a name="parameters"></a>Parámetros

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
<th><p>Necesario/Opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>NumRows</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>El número de filas que quiere recuperar.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor devuelto

Variant

## <a name="remarks"></a>Comentarios

Use el método **GetRows** para copiar registros de un objeto **Recordset**. **GetRows** devuelve una matriz bidimensional. El primer subíndice identifica el campo y el segundo identifica el número de fila. Por ejemplo, intField representa el campo e intRecord identifica el número de fila:

avarRecords (intField, intRecord)

Para obtener el primer valor de campo en la segunda fila devuelta, utilice un código como el siguiente:

Campo1 = avarRecords(0,1)

Para obtener el segundo valor de campo en la primera fila, utilice un código como el siguiente:

Field2 = avarRecords(1,0)

La variable avarRecords se convierte automáticamente en una matriz bidimensional cuando **GetRows** devuelve datos.

Si solicitan más filas que las que están disponibles, **GetRows** devuelve sólo el número de filas disponibles. Puede utilizar la función **UBound** de Visual Basic para Aplicaciones para determinar cuántas filas **GetRows** ha recuperado realmente porque la matriz está adaptada para que quepa el número de filas devueltas. Por ejemplo, si ha devuelto los resultados en una **Variant** llamada varA, podría usar el siguiente código para determinar cuántas filas se han devuelto realmente:

numReturned = UBound(varA,2) + 1

Debe utilizar "+ 1" porque la primera fila devuelta está en el elemento 0 de la matriz. El número de filas que puede recuperar está limitado por la cantidad de memoria disponible. No debe utilizar **GetRows** para recuperar toda una tabla en una matriz si es grande.

Como **GetRows** devuelve todos los campos de **Recordset** a la matriz, incluidos los campos Memo y Long Binary, es posible que desee usar una consulta que limite los campos devueltos.

Tras realizar una llamada **GetRows**, el registro activo se coloca en la siguiente fila no leída. Es decir, **GetRows** tiene el mismo efecto en el registro actual como numrows **mover**.

Si intenta recuperar todas las filas mediante varias llamadas **GetRows**, use la propiedad **[EOF](recordset2-eof-property-dao.md)** para asegurarse de que está al final de **Recordset**. **GetRows** devuelve un número inferior al solicitado si está al final de **Recordset** o si no puede recuperar una fila en el intervalo solicitado. Por ejemplo, si está intentando recuperar 10 registros, pero no puede recuperar el quinto registro, **GetRows** devuelve cuatro registros y hace del quinto el registro activo. Esto no generará un error en tiempo de ejecución. Esto puede ocurrir si otro usuario elimina un registro en un objeto **Recordset** de tipo dynaset. Vea el ejemplo para obtener una demostración de cómo controlar esto.

## <a name="example"></a>Ejemplo

En este ejemplo se usa el método **GetRows** para recuperar un número especificado de filas de un objeto **Recordset** y rellenar una matriz con los datos resultantes. El método **GetRows** devolverá un número de filas menor que el deseado en los dos siguientes casos: si se alcanza **EOF** o si **GetRows** ha tratado de recuperar un registro anteriormente eliminado por otro usuario. La función devuelve **False** solo si se produce el segundo caso. Se requiere la función GetRowsOK para que se ejecute este procedimiento.

```vb
    Sub GetRowsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strMessage As String 
     Dim intRows As Integer 
     Dim avarRecords As Variant 
     Dim intRecord As Integer 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
     "SELECT FirstName, LastName, Title " & _ 
     "FROM Employees ORDER BY LastName", dbOpenSnapshot) 
     
     With rstEmployees 
     Do While True 
     ' Get user input for number of rows. 
     strMessage = "Enter number of rows to retrieve." 
     intRows = Val(InputBox(strMessage)) 
     
     If intRows <= 0 Then Exit Do 
     
     ' If GetRowsOK is successful, print the results, 
     ' noting if the end of the file was reached. 
     If GetRowsOK(rstEmployees, intRows, _ 
     avarRecords) Then 
     If intRows > UBound(avarRecords, 2) + 1 Then 
     Debug.Print "(Not enough records in " & _ 
     "Recordset to retrieve " & intRows & _ 
     " rows.)" 
     End If 
     Debug.Print UBound(avarRecords, 2) + 1 & _ 
     " records found." 
     
     ' Print the retrieved data. 
     For intRecord = 0 To UBound(avarRecords, 2) 
     Debug.Print " " & _ 
     avarRecords(0, intRecord) & " " & _ 
     avarRecords(1, intRecord) & ", " & _ 
     avarRecords(2, intRecord) 
     Next intRecord 
     Else 
     ' Assuming the GetRows error was due to data 
     ' changes by another user, use Requery to 
     ' refresh the Recordset and start over. 
     If .Restartable Then 
     If MsgBox("GetRows failed--retry?", _ 
     vbYesNo) = vbYes Then 
     .Requery 
     Else 
     Debug.Print "GetRows failed!" 
     Exit Do 
     End If 
     Else 
     Debug.Print "GetRows failed! " & _ 
     "Recordset not Restartable!" 
     Exit Do 
     End If 
     End If 
     
     ' Because using GetRows leaves the current record 
     ' pointer at the last record accessed, move the 
     ' pointer back to the beginning of the Recordset 
     ' before looping back for another search. 
     .MoveFirst 
     Loop 
     End With 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function GetRowsOK(rstTemp As Recordset2, _ 
     intNumber As Integer, avarData As Variant) As Boolean 
     
     ' Store results of GetRows method in array. 
     avarData = rstTemp.GetRows(intNumber) 
     ' Return False only if fewer than the desired number of 
     ' rows were returned, but not because the end of the 
     ' Recordset was reached. 
     If intNumber > UBound(avarData, 2) + 1 And _ 
     Not rstTemp.EOF Then 
     GetRowsOK = False 
     Else 
     GetRowsOK = True 
     End If 
     
    End Function
```
