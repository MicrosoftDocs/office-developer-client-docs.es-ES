---
title: Detección y resolución de conflictos
TOCTitle: Detecting and resolving conflicts
ms:assetid: 8299745b-e595-21d5-26c1-a078d00a1c0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249566(v=office.15)
ms:contentKeyID: 48545983
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ddd7566be2581fe449872eb576bf7f11e5a806fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293927"
---
# <a name="detecting-and-resolving-conflicts"></a>Detección y resolución de conflictos

**Se aplica a:** Access 2013, Office 2013

## <a name="detecting-and-resolving-conflicts"></a>Detectar y resolver conflictos

Si trabaja con un **conjunto de registros** en modo inmediato, las posibilidades de que se produzcan problemas de simultaneidad son mucho menores. Por otra parte, si la aplicación utiliza el modo de actualización por lotes, es muy probable que un usuario cambie un registro antes de que se hayan guardado los cambios realizados por otro usuario que esté editando el mismo registro. En tal caso, deseará que la aplicación pueda ocuparse de resolver el conflicto sin más problemas. Puede que prefiera que sea la última persona que envíe una actualización al servidor la que "gane". O tal vez desee que sea el usuario más reciente quien decida qué actualización debe tener prioridad, permitiéndole escoger entre los dos valores en conflicto.

En cualquier caso, ADO proporciona las propiedades **UnderlyingValue** y **OriginalValue** del objeto **Field** para controlar estos tipos de conflictos. Utilice estas propiedades en combinación con el método **Resync** y la propiedad **Filter** del **conjunto de registros**.

## <a name="detecting-errors"></a>Detectar errores

Cuando ADO detecta un conflicto durante una actualización por lotes, coloca una advertencia en la colección **Errors**. Por lo tanto, debe comprobar siempre si hay errores inmediatamente después de llamar a **BatchUpdate** y, si se observan, empiece por probar la suposición de que se ha producido un conflicto. El primer paso es establecer la propiedad **Filter** en el **conjunto de registros** como igual a **adFilterConflictingRecords** (la propiedad **Filter** se describe en el capítulo anterior). Esto limita la visión en el **conjunto de registros** a sólo los registros que están en conflicto. Si la propiedad **RecordCount** es igual a cero después de este paso, sabrá que el error se debe a una causa que no es un conflicto.

Al llamar a **BatchUpdate**, ADO y el proveedor generan instrucciones SQL para realizar actualizaciones en el origen de datos. Recuerde que ciertos orígenes de datos tienen limitaciones en cuanto a los tipos de columnas que se pueden utilizar en una cláusula WHERE.

A continuación, llame al método **Resync** en el **conjunto de registros** con el argumento *AffectRecords* establecido como igual a **adAffectGroup** y el argumento *ResyncValues* establecido como igual a **adResyncUnderlyingValues**. El método **Resync** actualiza los datos del objeto **Recordset** activo de la base de datos subyacente. Si utiliza **adAffectGroup**, se asegurará de que sólo se resincronicen con la base de datos los registros visibles con el valor de filtro actual, es decir, sólo los registros en conflicto. Esto podría suponer una diferencia de rendimiento considerable si se está trabajando con un **conjunto de registros** grande. Si establece el argumento *ResyncValues* en **adResyncUnderlyingValues** al llamar a **Resync**, se asegurará de que la propiedad **UnderlyingValue** contenga el valor (conflictivo) de la base de datos, que la propiedad **Valor** mantenga el valor que ha introducido el usuario y que la propiedad **OriginalValue** contenga el valor original del campo (el valor que tenía antes de realizarse la última llamada correcta a **UpdateBatch**). Posteriormente, puede utilizar estos valores para resolver el conflicto mediante programación o solicitar al usuario que elija el valor que se usará.

Esta técnica se muestra en el código de ejemplo siguiente. El ejemplo crea artificialmente un conflicto utilizando un **conjunto de registros** distinto para cambiar un valor en la tabla subyacente antes de llamar a **UpdateBatch**.

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

Puede utilizar la propiedad **Status** del **registro** activo o un **campo** específico para determinar qué tipo de conflicto se ha producido.

Para obtener información más detallada sobre el tratamiento de errores, vea [Capítulo 6: Tratamiento de errores](chapter-6-error-handling.md).

