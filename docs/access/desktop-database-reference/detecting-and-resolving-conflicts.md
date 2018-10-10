---
title: Detectar y resolver conflictos
TOCTitle: Detecting and Resolving Conflicts
ms:assetid: 8299745b-e595-21d5-26c1-a078d00a1c0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249566(v=office.15)
ms:contentKeyID: 48545983
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4468887c0ef187e6dd955c20db91050415ec68ed
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483752"
---
# <a name="detecting-and-resolving-conflicts"></a><span data-ttu-id="f7507-102">Detectar y resolver conflictos</span><span class="sxs-lookup"><span data-stu-id="f7507-102">Detecting and Resolving Conflicts</span></span>

<span data-ttu-id="f7507-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7507-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="detecting-and-resolving-conflicts"></a><span data-ttu-id="f7507-104">Detectar y resolver conflictos</span><span class="sxs-lookup"><span data-stu-id="f7507-104">Detecting and Resolving Conflicts</span></span>

<span data-ttu-id="f7507-p101">Si trabaja con un **conjunto de registros** en modo inmediato, las posibilidades de que se produzcan problemas de simultaneidad son mucho menores. Por otra parte, si la aplicación utiliza el modo de actualización por lotes, es muy probable que un usuario cambie un registro antes de que se hayan guardado los cambios realizados por otro usuario que esté editando el mismo registro. En tal caso, deseará que la aplicación pueda ocuparse de resolver el conflicto sin más problemas. Puede que prefiera que sea la última persona que envíe una actualización al servidor la que "gane". O tal vez desee que sea el usuario más reciente quien decida qué actualización debe tener prioridad, permitiéndole escoger entre los dos valores en conflicto.</span><span class="sxs-lookup"><span data-stu-id="f7507-p101">If you are dealing with your **Recordset** in immediate mode, there is much less chance for concurrency problems to arise. On the other hand, if your application uses batch mode updating, there may be a good chance that one user will change a record before changes made by another user editing the same record are saved. In such a case, you will want your application to gracefully handle the conflict. It may be your wish that the last person to send an update to the server "wins." Or you may want to let the most recent user to decide which update should take precedence by providing him with a choice between the two conflicting values.</span></span>

<span data-ttu-id="f7507-p102">En cualquier caso, ADO proporciona las propiedades **UnderlyingValue** y **OriginalValue** del objeto **Field** para controlar estos tipos de conflictos. Utilice estas propiedades en combinación con el método **Resync** y la propiedad **Filter** del **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="f7507-p102">Whatever the case, ADO provides the **UnderlyingValue** and **OriginalValue** properties of the **Field** object in order to handle these types of conflicts. Use these properties in combination with the **Resync** method and **Filter** property of the **Recordset**.</span></span>

## <a name="detecting-errors"></a><span data-ttu-id="f7507-112">Detectar errores</span><span class="sxs-lookup"><span data-stu-id="f7507-112">Detecting Errors</span></span>

<span data-ttu-id="f7507-p103">Cuando ADO detecta un conflicto durante una actualización por lotes, coloca una advertencia en la colección **Errors**. Por lo tanto, debe comprobar siempre si hay errores inmediatamente después de llamar a **BatchUpdate** y, si se observan, empiece por probar la suposición de que se ha producido un conflicto. El primer paso es establecer la propiedad **Filter** en el **conjunto de registros** como igual a **adFilterConflictingRecords** (la propiedad **Filter** se describe en el capítulo anterior). Esto limita la visión en el **conjunto de registros** a sólo los registros que están en conflicto. Si la propiedad **RecordCount** es igual a cero después de este paso, sabrá que el error se debe a una causa que no es un conflicto.</span><span class="sxs-lookup"><span data-stu-id="f7507-p103">When ADO encounters a conflict during a batch update, a warning will be placed in the **Errors** collection. Therefore, you should always check for errors immediately after calling **BatchUpdate**, and if you find them, begin testing the assumption that you have encountered a conflict. The first step is to set the **Filter** property on the **Recordset** equal to **adFilterConflictingRecords** (the **Filter** property is discussed in the preceding chapter). This limits the view on your **Recordset** to only those records that are in conflict. If the **RecordCount** property is equal to zero after this step, you know the error was raised by something other than a conflict.</span></span>

<span data-ttu-id="f7507-p104">Al llamar a **BatchUpdate**, ADO y el proveedor generan instrucciones SQL para realizar actualizaciones en el origen de datos. Recuerde que ciertos orígenes de datos tienen limitaciones en cuanto a los tipos de columnas que se pueden utilizar en una cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="f7507-p104">When you call **BatchUpdate**, ADO and the provider are generating SQL statements to perform updates on the data source. Remember that certain data sources have limitations on which types of columns can be used in a WHERE clause.</span></span>

<span data-ttu-id="f7507-120">A continuación, llame al método **Resync** en el **conjunto de registros** con el argumento *AffectRecords* establecido igual a **adAffectGroup** y el argumento *ResyncValues* establecido como igual a **adResyncUnderlyingValues**.</span><span class="sxs-lookup"><span data-stu-id="f7507-120">Next, call the **Resync** method on the **Recordset** with the *AffectRecords* argument set equal to **adAffectGroup** and the *ResyncValues* argument set equal to **adResyncUnderlyingValues**.</span></span> <span data-ttu-id="f7507-121">El método **Resync** actualiza los datos del objeto **Recordset** activo de la base de datos subyacente.</span><span class="sxs-lookup"><span data-stu-id="f7507-121">The **Resync** method refreshes the data in the current **Recordset** object from the underlying database.</span></span> <span data-ttu-id="f7507-122">Si utiliza **adAffectGroup**, se asegurará de que sólo se resincronicen con la base de datos los registros visibles con el valor de filtro actual, es decir, sólo los registros en conflicto.</span><span class="sxs-lookup"><span data-stu-id="f7507-122">By using **adAffectGroup**, you are ensuring that only the records visible with the current filter setting, that is, only the conflicting records, are resynchronized with the database.</span></span> <span data-ttu-id="f7507-123">Esto podría suponer una diferencia de rendimiento considerable si se está trabajando con un **conjunto de registros** grande.</span><span class="sxs-lookup"><span data-stu-id="f7507-123">This could make a significant performance difference if you are dealing with a large **Recordset**.</span></span> <span data-ttu-id="f7507-124">Estableciendo el argumento *ResyncValues* en **adResyncUnderlyingValues** al llamar a **Resync**, asegúrese de que la propiedad **UnderlyingValue** contendrá el valor (conflicto) desde la base de datos que el **valor** propiedad mantendrá el valor especificado por el usuario, y que la propiedad **OriginalValue** contendrá el valor original del campo (el valor que tenía antes de que se realizó la última llamada correcta a **UpdateBatch** ).</span><span class="sxs-lookup"><span data-stu-id="f7507-124">By setting the *ResyncValues* argument to **adResyncUnderlyingValues** when calling **Resync**, you ensure that the **UnderlyingValue** property will contain the (conflicting) value from the database, that the **Value** property will maintain the value entered by the user, and that the **OriginalValue** property will hold the original value for the field (the value it had before the last successful **UpdateBatch** call was made).</span></span> <span data-ttu-id="f7507-125">Posteriormente, puede utilizar estos valores para resolver el conflicto mediante programación o solicitar al usuario que elija el valor que se usará.</span><span class="sxs-lookup"><span data-stu-id="f7507-125">You can then use these values to resolve the conflict programmatically or require the user to choose the value that will be used.</span></span>

<span data-ttu-id="f7507-p106">Esta técnica se muestra en el código de ejemplo siguiente. El ejemplo crea artificialmente un conflicto utilizando un **conjunto de registros** distinto para cambiar un valor en la tabla subyacente antes de llamar a **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="f7507-p106">This technique is shown in the code example below. The example artificially creates a conflict by using a separate **Recordset** to change a value in the underlying table before **UpdateBatch** is called.</span></span>

```vb 
 
'BeginConflicts 
    On Error GoTo ErrHandler: 
     
    Dim objRs1 As New ADODB.Recordset 
    Dim objRs2 As New ADODB.Recordset 
    Dim strSQL As String 
    Dim strMsg As String 
     
    strSQL = "SELECT * FROM Shippers WHERE ShipperID = 2" 
                  
    'Open Rs and change a value 
    objRs1.CursorLocation = adUseClient 
    objRs1.Open strSQL, strConn, adOpenStatic, adLockBatchOptimistic, adCmdText 
    objRs1("Phone") = "(111) 555-1111" 
     
    'Introduce a conflict at the db... 
    objRs2.Open strSQL, strConn, adOpenKeyset, adLockOptimistic, adCmdText 
    objRs2("Phone") = "(999) 555-9999" 
    objRs2.Update 
    objRs2.Close 
    Set objRs2 = Nothing 
     
    On Error Resume Next 
    objRs1.UpdateBatch 
     
    If objRs1.ActiveConnection.Errors.Count <> 0 Then 
        Dim intConflicts As Integer 
         
        intConflicts = 0 
         
        objRs1.Filter = adFilterConflictingRecords 
         
        intConflicts = objRs1.RecordCount 
         
        'Resync so we can see the UnderlyingValue and offer user a choice. 
        'This sample only displays all three values and resets to original. 
        objRs1.Resync adAffectGroup, adResyncUnderlyingValues 
         
        If intConflicts > 0 Then 
            strMsg = "A conflict occurred with updates for " & intConflicts & _ 
                     " record(s)." & vbCrLf & "The values will be restored" & _ 
                     " to their original values." & vbCrLf & vbCrLf 
                      
            objRs1.MoveFirst 
            While Not objRs1.EOF 
                strMsg = strMsg & "SHIPPER = " & objRs1("CompanyName") & vbCrLf 
                strMsg = strMsg & "Value = " & objRs1("Phone").Value & vbCrLf 
                strMsg = strMsg & "UnderlyingValue = " & _ 
                                   objRs1("Phone").UnderlyingValue & vbCrLf 
                strMsg = strMsg & "OriginalValue = " & _ 
                                   objRs1("Phone").OriginalValue & vbCrLf 
                strMsg = strMsg & vbCrLf & "Original value has been restored." 
                   
                MsgBox strMsg, vbOKOnly, _ 
                      "Conflict " & objRs1.AbsolutePosition & _ 
                      " of " & intConflicts 
                   
                objRs1("Phone").Value = objRs1("Phone").OriginalValue 
                objRs1.MoveNext 
            Wend 
             
            objRs1.UpdateBatch adAffectGroup 
        Else 
            'Other error occurred. Minimal handling in this example. 
             strMsg = "Errors occurred during the update. " & _ 
                        objRs1.ActiveConnection.Errors(0).Number & " " & _ 
                        objRs1.ActiveConnection.Errors(0).Description 
        End If 
         
        On Error GoTo 0 
    End If 
     
    objRs1.MoveFirst 
     
    'Clean up 
    objRs1.Close 
    Set objRs1 = Nothing 
    Exit Sub 
     
ErrHandler: 
    
    If Not objRs1 Is Nothing Then 
        If objRs1.State = adStateOpen Then objRs1.Close 
        Set objRs1 = Nothing 
    End If 
     
    If Not objRs2 Is Nothing Then 
        If objRs2.State = adStateOpen Then objRs2.Close 
        Set objRs2 = Nothing 
    End If 
     
    If Err <> 0 Then 
        MsgBox Err.Source & "-->" & Err.Description, , "Error" 
    End If 
     
'EndConflicts 
```

<span data-ttu-id="f7507-128">Puede utilizar la propiedad **Status** del **registro** activo o un **campo** específico para determinar qué tipo de conflicto se ha producido.</span><span class="sxs-lookup"><span data-stu-id="f7507-128">You can use the **Status** property of the current **Record** or of a specific **Field** to determine what kind of a conflict has occurred.</span></span>

<span data-ttu-id="f7507-129">Para obtener información más detallada sobre el tratamiento de errores, vea [Capítulo 6: Tratamiento de errores](chapter-6-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="f7507-129">For more detailed information on error handling, see [Chapter 6: Error Handling](chapter-6-error-handling.md).</span></span>

