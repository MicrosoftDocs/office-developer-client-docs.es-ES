---
title: Propiedad Recordset2.LockEdits (DAO)
TOCTitle: LockEdits Property
ms:assetid: 77055f44-f8e9-ac64-ecc3-144ddb4a4558
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196045(v=office.15)
ms:contentKeyID: 48545716
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ff2db22dcb0119792eb57a971d3cf36e763d3049
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309649"
---
# <a name="recordset2lockedits-property-dao"></a><span data-ttu-id="6d3b8-102">Propiedad Recordset2.LockEdits (DAO)</span><span class="sxs-lookup"><span data-stu-id="6d3b8-102">Recordset2.LockEdits property (DAO)</span></span>

<span data-ttu-id="6d3b8-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d3b8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6d3b8-104">Establece o devuelve un valor que indica el tipo de bloqueo que está activo mientras se modifica.</span><span class="sxs-lookup"><span data-stu-id="6d3b8-104">Sets or returns a value indicating the type of locking that is in effect while editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d3b8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6d3b8-105">Syntax</span></span>

<span data-ttu-id="6d3b8-106">*expresión* . LockEdits</span><span class="sxs-lookup"><span data-stu-id="6d3b8-106">*expression* .LockEdits</span></span>

<span data-ttu-id="6d3b8-107">*expresión* Variable que representa un objeto **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="6d3b8-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d3b8-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6d3b8-108">Remarks</span></span>

<span data-ttu-id="6d3b8-109">La configuración o el valor devuelto indica el tipo de bloqueo, como se especifica en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="6d3b8-109">The setting or return value indicates the type of locking, as specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6d3b8-110">Valor</span><span class="sxs-lookup"><span data-stu-id="6d3b8-110">Value</span></span></p></th>
<th><p><span data-ttu-id="6d3b8-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d3b8-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d3b8-112">Verdadero</span><span class="sxs-lookup"><span data-stu-id="6d3b8-112">True</span></span></p></td>
<td><p><span data-ttu-id="6d3b8-p101">Predeterminado. Está activado un bloqueo pesimista. La página que contiene el registro que está editando se bloquea tan pronto como llama al método Edit.</span><span class="sxs-lookup"><span data-stu-id="6d3b8-p101">Default. Pessimistic locking is in effect. The page containing the record you're editing is locked as soon as you call the Edit method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d3b8-116">Falso</span><span class="sxs-lookup"><span data-stu-id="6d3b8-116">False</span></span></p></td>
<td><p><span data-ttu-id="6d3b8-117">Está activado un bloqueo optimista para la edición.</span><span class="sxs-lookup"><span data-stu-id="6d3b8-117">Optimistic locking is in effect for editing.</span></span> <span data-ttu-id="6d3b8-118">La página que contiene el registro no se bloquea hasta que se ejecuta el método Update .</span><span class="sxs-lookup"><span data-stu-id="6d3b8-118">The page containing the record is not locked until the Update method is executed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6d3b8-119">Puede usar la propiedad **LockEdits** con objetos **[Recordset](recordset-object-dao.md)** actualizables.</span><span class="sxs-lookup"><span data-stu-id="6d3b8-119">You can use the **LockEdits** property with updatable **[Recordset](recordset-object-dao.md)** objects.</span></span>

<span data-ttu-id="6d3b8-p103">Si la página está bloqueada, ningún otro usuario puede editar registros en esa página. Si establece **LockEdits** en **True** y otro usuario ya ha bloqueado la página, se producirá un error cuando usted intente utilizar el método **Edit**. Otros usuarios pueden leer datos de páginas bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="6d3b8-p103">If a page is locked, no other user can edit records on the same page. If you set **LockEdits** to **True** and another user already has the page locked, an error occurs when you use the **Edit** method. Other users can read data from locked pages.</span></span>

<span data-ttu-id="6d3b8-p104">Si establece la propiedad **LockEdits** en **False** y después utiliza el método **Update** mientras otro usuario ha bloqueado la página, se producirá un error. Para ver los cambios realizados por otro usuario en su registro, utilice el método **[Move](recordset2-move-method-dao.md)** con 0 como argumento; sin embargo, al hacer esto perderá sus cambios.</span><span class="sxs-lookup"><span data-stu-id="6d3b8-p104">If you set the **LockEdits** property to **False** and later use the **Update** method while another user has the page locked, an error occurs. To see the changes made to your record by another user, use the **[Move](recordset2-move-method-dao.md)** method with 0 as the argument; however, if you do this, you will lose your changes.</span></span>

<span data-ttu-id="6d3b8-p105">Cuando trabaje con un motor de base de datos Microsoft Access conectado a orígenes de datos ODBC, la propiedad **LockEdits** estará siempre establecida en **False** o en bloqueo optimista. El motor de base de datos Microsoft Access no tiene control sobre los mecanismos de bloqueo utilizados en servidores de bases de datos externos.</span><span class="sxs-lookup"><span data-stu-id="6d3b8-p105">When working with Microsoft Access database engine-connected ODBC data sources, the **LockEdits** property is always set to **False**, or optimistic locking. The Microsoft Access database engine has no control over the locking mechanisms used in external database servers.</span></span>

> [!NOTE]
> <span data-ttu-id="6d3b8-127">Puede preestablecer el valor de **LockEdits** cuando abra por primera vez el conjunto de registros estableciendo el argumento lockedits del método  **[OpenRecordset.](connection-openrecordset-method-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="6d3b8-127">You can preset the value of **LockEdits** when you first open the **Recordset** by setting the lockedits argument of the **[OpenRecordset](connection-openrecordset-method-dao.md)** method.</span></span> <span data-ttu-id="6d3b8-128">Al establecer el argumento LockEdits en **dbPessimistic** se establecerá la propiedad **LockEdits** en **True** y al establecer LockEdits en cualquier otro valor se establecerá la propiedad **LockEdits** en **False**.</span><span class="sxs-lookup"><span data-stu-id="6d3b8-128">Setting the lockedits argument to **dbPessimistic** will set the **LockEdits** property to **True**, and setting lockedits to any other value will set the **LockEdits** property to **False**.</span></span>

## <a name="example"></a><span data-ttu-id="6d3b8-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6d3b8-129">Example</span></span>

<span data-ttu-id="6d3b8-p107">En este ejemplo se muestra un bloqueo pesimista al establecer la propiedad **LockEdits** en **True**, después se muestra un bloqueo optimista al establecer la propiedad **LockEdits** en False. También se muestra el tipo de tratamiento de errores necesario en un entorno de base de datos multiusuario para poder modificar un campo. Se requieren las funciones PessimisticLock y OptimisticLock para que pueda ejecutarse este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="6d3b8-p107">This example demonstrates pessimistic locking by setting the **LockEdits** property to **True**, and then demonstrates optimistic locking by setting the **LockEdits** property to False. It also demonstrates what kind of error handling is required in a multiuser database environment in order to modify a field. The PessimisticLock and OptimisticLock functions are required for this procedure to run.</span></span>

```vb
    Sub LockEditsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCustomers As Recordset2 
     Dim strOldName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCustomers = _ 
     dbsNorthwind.OpenRecordset("Customers", _ 
     dbOpenDynaset) 
     
     With rstCustomers 
     ' Store original data. 
     strOldName = !CompanyName 
     
     If MsgBox("Pessimistic locking demonstration...", _ 
     vbOKCancel) = vbOK Then 
     
     ' Attempt to modify data with pessimistic locking 
     ' in effect. 
     If PessimisticLock(rstCustomers, !CompanyName, _ 
     "Acme Foods") Then 
     MsgBox "Record successfully edited." 
     
     ' Restore original data... 
     .Edit 
     !CompanyName = strOldName 
     .Update 
     End If 
     
     End If 
     
     If MsgBox("Optimistic locking demonstration...", _ 
     vbOKCancel) = vbOK Then 
     
     ' Attempt to modify data with optimistic locking 
     ' in effect. 
     If OptimisticLock(rstCustomers, !CompanyName, _ 
     "Acme Foods") Then 
     MsgBox "Record successfully edited." 
     
     ' Restore original data... 
     .Edit 
     !CompanyName = strOldName 
     .Update 
     End If 
     
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function PessimisticLock(rstTemp As Recordset2, _ 
     fldTemp As Field, strNew As String) As Boolean 
     
     dim ErrLoop as Error 
     
     PessimisticLock = True 
     
     With rstTemp 
     .LockEdits = True 
     
     ' When you set LockEdits to True, you trap for errors 
     ' when you call the Edit method. 
     On Error GoTo Err_Lock 
     .Edit 
     On Error GoTo 0 
     
     ' If the Edit is still in progress, then no errors 
     ' were triggered; you may modify the data. 
     If .EditMode = dbEditInProgress Then 
     fldTemp = strNew 
     .Update 
     .Bookmark = .LastModified 
     Else 
     ' Retrieve current record to see changes made by 
     ' other user. 
     .Move 0 
     End If 
     
     End With 
     
     Exit Function 
     
    Err_Lock: 
     
     If DBEngine.Errors.Count > 0 Then 
     ' Enumerate the Errors collection. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     PessimisticLock = False 
     End If 
     
     Resume Next 
     
    End Function 
     
    Function OptimisticLock(rstTemp As Recordset, _ 
     fldTemp As Field, strNew As String) As Boolean 
     
     dim ErrLoop as Error 
     
     OptimisticLock = True 
     
     With rstTemp 
     .LockEdits = False 
     .Edit 
     fldTemp = strNew 
     
     ' When you set LockEdits to False, you trap for errors 
     ' when you call the Update method. 
     On Error GoTo Err_Lock 
     .Update 
     On Error GoTo 0 
     
     ' If there is no Edit in progress, then no errors were 
     ' triggered; you may modify the data. 
     If .EditMode = dbEditNone Then 
     ' Move current record pointer to the most recently 
     ' modified record. 
     .Bookmark = .LastModified 
     Else 
     .CancelUpdate 
     ' Retrieve current record to see changes made by 
     ' other user. 
     .Move 0 
     End If 
     
     End With 
     
     Exit Function 
     
    Err_Lock: 
     
     If DBEngine.Errors.Count > 0 Then 
     ' Enumerate the Errors collection. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     OptimisticLock = False 
     End If 
     
     Resume Next 
     
    End Function
```
