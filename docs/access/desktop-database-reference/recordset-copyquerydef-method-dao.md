---
title: Recordset.CopyQueryDef Method (DAO)
TOCTitle: CopyQueryDef Method
ms:assetid: fee8c2fe-500e-dfb3-21ce-211e54ff334b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837296(v=office.15)
ms:contentKeyID: 48548950
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 607bfe534ae7f399fc7916ad1c3d423dbd8dae30
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483993"
---
# <a name="recordsetcopyquerydef-method-dao"></a><span data-ttu-id="2b206-102">Recordset.CopyQueryDef Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="2b206-102">Recordset.CopyQueryDef Method (DAO)</span></span>


<span data-ttu-id="2b206-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b206-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2b206-104">Devuelve un objeto **[QueryDef](querydef-object-dao.md)** que es una copia del **objeto QueryDef** utilizado para crear el objeto **[Recordset](recordset-object-dao.md)** representado por el marcador de posición de recordset (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="2b206-104">Returns a **[QueryDef](querydef-object-dao.md)** object that is a copy of the **QueryDef** used to create the **[Recordset](recordset-object-dao.md)** object represented by the recordset placeholder (Microsoft Access workspaces only).</span></span> <span data-ttu-id="2b206-105">.</span><span class="sxs-lookup"><span data-stu-id="2b206-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="2b206-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b206-106">Syntax</span></span>

<span data-ttu-id="2b206-107">*expresión* . CopyQueryDef</span><span class="sxs-lookup"><span data-stu-id="2b206-107">*expression* .CopyQueryDef</span></span>

<span data-ttu-id="2b206-108">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="2b206-108">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="return-value"></a><span data-ttu-id="2b206-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b206-109">Return Value</span></span>

<span data-ttu-id="2b206-110">Objeto QueryDef</span><span class="sxs-lookup"><span data-stu-id="2b206-110">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="2b206-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b206-111">Remarks</span></span>

<span data-ttu-id="2b206-112">Puede usar el método **CopyQueryDef** para crear un objeto **QueryDef** nuevo que sea un duplicado del **QueryDef** que se usó para crear el **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="2b206-112">You can use the **CopyQueryDef** method to create a new **QueryDef** that is a duplicate of the **QueryDef** used to create the **Recordset**.</span></span>

<span data-ttu-id="2b206-p102">Si no se usó un objeto **QueryDef** para crear este objeto **Recordset**, se produce un error. Debe abrir primero un objeto **Recordset** con el método **OpenRecordset** antes de utilizar el método **CopyQueryDef**.</span><span class="sxs-lookup"><span data-stu-id="2b206-p102">If a **QueryDef** wasn't used to create this **Recordset**, an error occurs. You must first open a **Recordset** with the **OpenRecordset** method before using the **CopyQueryDef** method.</span></span>

<span data-ttu-id="2b206-115">Este método le resultará útil cuando cree un objeto **Recordset** desde **QueryDef**, y pase el objeto **Recordset** a una función, y la función deba volver a crear el equivalente SQL de la consulta para, por ejemplo, modificarla de alguna forma.</span><span class="sxs-lookup"><span data-stu-id="2b206-115">This method is useful when you create a **Recordset** object from a **QueryDef**, and pass the **Recordset** to a function, and the function must re-create the SQL equivalent of the query, for example, to modify it in some way.</span></span>

## <a name="example"></a><span data-ttu-id="2b206-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2b206-116">Example</span></span>

<span data-ttu-id="2b206-p103">En este ejemplo se usa el método **CopyQueryDef** para crear una copia de un objeto **QueryDef** desde un objeto **Recordset** existente y se modifica la copia agregando una cláusula a la propiedad SQL. Cuando crea un objeto **QueryDef** permanente, es posible que se agreguen espacios, signos de punto y coma o saltos de línea a la propiedad SQL; se deben quitar estos caracteres adicionales antes de poder agregar cláusulas nuevas a la instrucción SQL.</span><span class="sxs-lookup"><span data-stu-id="2b206-p103">This example uses the **CopyQueryDef** method to create a copy of a **QueryDef** from an existing **Recordset** and modifies the copy by adding a clause to the SQL property. When you create a permanent **QueryDef**, spaces, semicolons, or linefeeds may be added to the SQL property; these extra characters must be stripped before any new clauses can be attached to the SQL statement.</span></span>

```vb
    Function CopyQueryNew(rstTemp As Recordset, _ 
     strAdd As String) As QueryDef 
     
     Dim strSQL As String 
     Dim strRightSQL As String 
     
     Set CopyQueryNew = rstTemp.CopyQueryDef 
     With CopyQueryNew 
     ' Strip extra characters. 
     strSQL = .SQL 
     strRightSQL = Right(strSQL, 1) 
     Do While strRightSQL = " " Or strRightSQL = ";" Or _ 
     strRightSQL = Chr(10) Or strRightSQL = vbCr 
     strSQL = Left(strSQL, Len(strSQL) - 1) 
     strRightSQL = Right(strSQL, 1) 
     Loop 
     .SQL = strSQL & strAdd 
     End With 
     
    End Function 
```

<br/>

<span data-ttu-id="2b206-119">En este ejemplo se muestra un uso posible de CopyQueryNew().</span><span class="sxs-lookup"><span data-stu-id="2b206-119">This example shows a possible use of CopyQueryNew().</span></span>

```vb 
Sub CopyQueryDefX() 
 
 Dim dbsNorthwind As Database 
 Dim qdfEmployees As QueryDef 
 Dim rstEmployees As Recordset 
 Dim intCommand As Integer 
 Dim strOrderBy As String 
 Dim qdfCopy As QueryDef 
 Dim rstCopy As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set qdfEmployees = dbsNorthwind.CreateQueryDef( _ 
 "NewQueryDef", "SELECT FirstName, LastName, " & _ 
 "BirthDate FROM Employees") 
 Set rstEmployees = qdfEmployees.OpenRecordset( _ 
 dbOpenForwardOnly) 
 
 Do While True 
 intCommand = Val(InputBox( _ 
 "Choose field on which to order a new " & _ 
 "Recordset:" & vbCr & "1 - FirstName" & vbCr & _ 
 "2 - LastName" & vbCr & "3 - BirthDate" & vbCr & _ 
 "[Cancel - exit]")) 
 Select Case intCommand 
 Case 1 
 strOrderBy = " ORDER BY FirstName" 
 Case 2 
 strOrderBy = " ORDER BY LastName" 
 Case 3 
 strOrderBy = " ORDER BY BirthDate" 
 Case Else 
 Exit Do 
 End Select 
 Set qdfCopy = CopyQueryNew(rstEmployees, strOrderBy) 
 Set rstCopy = qdfCopy.OpenRecordset(dbOpenSnapshot, _ 
 dbForwardOnly) 
 With rstCopy 
 Do While Not .EOF 
 Debug.Print !LastName & ", " & !FirstName & _ 
 " - " & !BirthDate 
 .MoveNext 
 Loop 
 .Close 
 End With 
 Exit Do 
 Loop 
 
 rstEmployees.Close 
 ' Delete new QueryDef because this is a demonstration. 
 dbsNorthwind.QueryDefs.Delete qdfEmployees.Name 
 dbsNorthwind.Close 
 
End Sub 
 
```
