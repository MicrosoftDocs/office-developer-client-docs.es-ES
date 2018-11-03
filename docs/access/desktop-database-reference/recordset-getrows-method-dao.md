---
title: Recordset.GetRows (método) (DAO)
TOCTitle: GetRows Method
ms:assetid: 59f6e4f0-e7b1-db60-31c7-3338b66d3345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194427(v=office.15)
ms:contentKeyID: 48545031
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053362
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1b0df2371ec9da675346cc24fd53d602cf69a170
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931242"
---
# <a name="recordsetgetrows-method-dao"></a><span data-ttu-id="403b7-102">Recordset.GetRows (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="403b7-102">Recordset.GetRows method (DAO)</span></span>


<span data-ttu-id="403b7-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="403b7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="403b7-104">Recupera varias filas de un objeto **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="403b7-104">Retrieves multiple rows from a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="403b7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="403b7-105">Syntax</span></span>

<span data-ttu-id="403b7-106">*expresión* . GetRows (***NumRows***)</span><span class="sxs-lookup"><span data-stu-id="403b7-106">*expression* .GetRows(***NumRows***)</span></span>

<span data-ttu-id="403b7-107">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="403b7-107">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="403b7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="403b7-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="403b7-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="403b7-109">Name</span></span></p></th>
<th><p><span data-ttu-id="403b7-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="403b7-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="403b7-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="403b7-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="403b7-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="403b7-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="403b7-113">NumRows</span><span class="sxs-lookup"><span data-stu-id="403b7-113">NumRows</span></span></p></td>
<td><p><span data-ttu-id="403b7-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="403b7-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="403b7-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="403b7-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="403b7-116">El número de filas que quiere recuperar.</span><span class="sxs-lookup"><span data-stu-id="403b7-116">The number of rows to retrieve.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="403b7-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="403b7-117">Return value</span></span>

<span data-ttu-id="403b7-118">Variant</span><span class="sxs-lookup"><span data-stu-id="403b7-118">Variant</span></span>

## <a name="remarks"></a><span data-ttu-id="403b7-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="403b7-119">Remarks</span></span>

<span data-ttu-id="403b7-p101">Use el método **GetRows** para copiar registros de un objeto **Recordset**. **GetRows** devuelve una matriz bidimensional. El primer subíndice identifica el campo y el segundo identifica el número de fila. Por ejemplo, intField representa el campo e intRecord identifica el número de fila:</span><span class="sxs-lookup"><span data-stu-id="403b7-p101">Use the **GetRows** method to copy records from a **Recordset**. **GetRows** returns a two-dimensional array. The first subscript identifies the field and the second identifies the row number. For example, intField represents the field, and intRecord identifies the row number:</span></span>

<span data-ttu-id="403b7-124">avarRecords (intField, intRecord)</span><span class="sxs-lookup"><span data-stu-id="403b7-124">avarRecords(intField, intRecord)</span></span>

<span data-ttu-id="403b7-125">Para obtener el primer valor de campo en la segunda fila devuelta, utilice un código como el siguiente:</span><span class="sxs-lookup"><span data-stu-id="403b7-125">To get the first field value in the second row returned, use code like the following:</span></span>

<span data-ttu-id="403b7-126">Campo1 = avarRecords(0,1)</span><span class="sxs-lookup"><span data-stu-id="403b7-126">field1 = avarRecords(0,1)</span></span>

<span data-ttu-id="403b7-127">Para obtener el segundo valor de campo en la primera fila, utilice un código como el siguiente:</span><span class="sxs-lookup"><span data-stu-id="403b7-127">To get the second field value in the first row, use code like the following:</span></span>

<span data-ttu-id="403b7-128">Field2 = avarRecords(1,0)</span><span class="sxs-lookup"><span data-stu-id="403b7-128">field2 = avarRecords(1,0)</span></span>

<span data-ttu-id="403b7-129">La variable avarRecords se convierte automáticamente en una matriz bidimensional cuando **GetRows** devuelve datos.</span><span class="sxs-lookup"><span data-stu-id="403b7-129">The avarRecords variable automatically becomes a two-dimensional array when **GetRows** returns data.</span></span>

<span data-ttu-id="403b7-130">Si solicitan más filas que las que están disponibles, **GetRows** devuelve sólo el número de filas disponibles.</span><span class="sxs-lookup"><span data-stu-id="403b7-130">If you request more rows than are available, then **GetRows** returns only the number of available rows.</span></span> <span data-ttu-id="403b7-131">Puede utilizar la función **UBound** de Visual Basic para Aplicaciones para determinar cuántas filas **GetRows** ha recuperado realmente porque la matriz está adaptada para que quepa el número de filas devueltas.</span><span class="sxs-lookup"><span data-stu-id="403b7-131">You can use the Visual Basic for Applications **UBound** function to determine how many rows **GetRows** actually retrieved, because the array is sized to fit the number of returned rows.</span></span> <span data-ttu-id="403b7-132">Por ejemplo, si ha devuelto los resultados en una **Variant** llamada varA, podría usar el siguiente código para determinar cuántas filas se han devuelto realmente:</span><span class="sxs-lookup"><span data-stu-id="403b7-132">For example, if you returned the results into a **Variant** called varA, you could use the following code to determine how many rows were actually returned:</span></span>

<span data-ttu-id="403b7-133">numReturned = UBound(varA,2) + 1</span><span class="sxs-lookup"><span data-stu-id="403b7-133">numReturned = UBound(varA,2) + 1</span></span>

<span data-ttu-id="403b7-p103">Debe utilizar "+ 1" porque la primera fila devuelta está en el elemento 0 de la matriz. El número de filas que puede recuperar está limitado por la cantidad de memoria disponible. No debe utilizar **GetRows** para recuperar toda una tabla en una matriz si es grande.</span><span class="sxs-lookup"><span data-stu-id="403b7-p103">You need to use "+ 1" because the first row returned is in the 0 element of the array. The number of rows that you can retrieve is constrained by the amount of available memory. You shouldn't use **GetRows** to retrieve an entire table into an array if it is large.</span></span>

<span data-ttu-id="403b7-137">Como **GetRows** devuelve todos los campos de **Recordset** a la matriz, incluidos los campos Memo y Long Binary, es posible que desee usar una consulta que limite los campos devueltos.</span><span class="sxs-lookup"><span data-stu-id="403b7-137">Because **GetRows** returns all fields of the **Recordset** into the array, including Memo and Long Binary fields, you might want to use a query that restricts the fields returned.</span></span>

<span data-ttu-id="403b7-138">Tras realizar una llamada **GetRows**, el registro activo se coloca en la siguiente fila no leída.</span><span class="sxs-lookup"><span data-stu-id="403b7-138">After you call **GetRows**, the current record is positioned at the next unread row.</span></span> <span data-ttu-id="403b7-139">Es decir, **GetRows** tiene el mismo efecto en el registro actual como numrows **mover** .</span><span class="sxs-lookup"><span data-stu-id="403b7-139">That is, **GetRows** has the same effect on the current record as **Move** numrows.</span></span>

<span data-ttu-id="403b7-p105">Si intenta recuperar todas las filas mediante varias llamadas **GetRows**, use la propiedad **[EOF](recordset-eof-property-dao.md)** para asegurarse de que está al final de **Recordset**. **GetRows** devuelve un número inferior al solicitado si está al final de **Recordset** o si no puede recuperar una fila en el intervalo solicitado. Por ejemplo, si está intentando recuperar 10 registros, pero no puede recuperar el quinto registro, **GetRows** devuelve cuatro registros y hace del quinto el registro activo. Esto no generará un error en tiempo de ejecución. Esto puede ocurrir si otro usuario elimina un registro en un objeto **Recordset** de tipo dynaset. Vea el ejemplo para obtener una demostración de cómo controlar esto.</span><span class="sxs-lookup"><span data-stu-id="403b7-p105">If you are trying to retrieve all the rows by using multiple **GetRows** calls, use the **[EOF](recordset-eof-property-dao.md)** property to be sure that you're at the end of the **Recordset**. **GetRows** returns less than the number requested if it's at the end of the **Recordset**, or if it can't retrieve a row in the range requested. For example, if you're trying to retrieve 10 records, but you can't retrieve the fifth record, **GetRows** returns four records and makes the fifth record the current record. This will not generate a run-time error. This might occur if another user deletes a record in a dynaset-type **Recordset**. See the example for a demonstration of how to handle this.</span></span>

## <a name="example"></a><span data-ttu-id="403b7-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="403b7-146">Example</span></span>

<span data-ttu-id="403b7-p106">En este ejemplo se usa el método **GetRows** para recuperar un número especificado de filas de un objeto **Recordset** y rellenar una matriz con los datos resultantes. El método **GetRows** devolverá un número de filas menor que el deseado en los dos siguientes casos: si se alcanza **EOF** o si **GetRows** ha tratado de recuperar un registro anteriormente eliminado por otro usuario. La función devuelve **False** solo si se produce el segundo caso. Se requiere la función GetRowsOK para que se ejecute este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="403b7-p106">This example uses the **GetRows** method to retrieve a specified number of rows from a **Recordset** and to fill an array with the resulting data. The **GetRows** method will return fewer than the desired number of rows in two cases: either if **EOF** has been reached, or if **GetRows** tried to retrieve a record that was deleted by another user. The function returns **False** only if the second case occurs. The GetRowsOK function is required for this procedure to run.</span></span>

```vb
    Sub GetRowsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
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
     
    Function GetRowsOK(rstTemp As Recordset, _ 
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
