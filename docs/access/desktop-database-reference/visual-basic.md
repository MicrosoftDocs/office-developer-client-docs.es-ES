---
title: Visual Basic (referencia de escritorio de la base de datos de Access)
TOCTitle: Visual Basic
ms:assetid: 9d153b6c-c860-7350-cb3c-b9bd08f75ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249714(v=office.15)
ms:contentKeyID: 48546616
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3045cf3861409d2909f31536670a27c282eb2cdc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709806"
---
# <a name="visual-basic"></a>Visual Basic


**Se aplica a**: Access 2013, Office 2013

Para controlar eventos de ADO en Microsoft Visual Basic, se debe declarar una variable de nivel de módulo mediante la palabra clave **WithEvents**. La variable se puede declarar sólo como parte de un módulo de clase y se debe declarar en el nivel de módulo. No obstante, esto no es tan restrictivo como parece, ya que los objetos **Form** de Visual Basic también son clases. La forma más sencilla de controlar eventos de ADO es declarar una variable mediante **WithEvents**. En el ejemplo siguiente, se controla el evento **ConnectComplete** para un objeto **Connection**:

```vb 
 
' BeginEventExampleVB02 
Dim WithEvents connEvent As Connection 
Attribute connEvent.VB_VarHelpID = -1 
Dim strMsg As String 
 
Private Sub Form_Load() 
 On Error GoTo ErrHandler: 
 
 Dim strConn As String 
 
 ' Create a new object with event 
 ' handling enabled. 
 strConn = "Provider='sqloledb';" & _ 
 "Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';" & _ 
 "Integrated Security='SSPI';" 
 Set connEvent = New ADODB.Connection 
 connEvent.Open strConn 
 
 Exit Sub 
 
ErrHandler: 
 MsgBox strMsg 
End Sub 
 
Private Sub connEvent_ConnectComplete(ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pConnection As ADODB.Connection) 
 
 If adStatus = adStatusErrorsOccurred Then 
 If Not pError Is Nothing Then 
 Select Case pError.Number 
 Case adErrOperationCancelled 
 ' The operation was cancelled in the 
 ' Will event. Notify the user and exit. 
 strMsg = "I'm sorry you can't connect right now." & vbCrLf 
 strMsg = strMsg & " Click OK to exit." 
 Unload Me 
 Case Else 
 strMsg = "Error " & Format(pError.Number) & vbCrLf 
 strMsg = strMsg & pError.Description 
 strMsg = strMsg & " Click OK to exit." 
 Unload Me 
 End Select 
 Else 
 strMsg = "Error occured. Click OK to exit." 
 Unload Me 
 End If 
 End If 
 'frmWait.btnOK.Enabled = True 
End Sub 
' EndEventExampleVB02 
```

El objeto **Connection** se declara en el nivel de **formulario** mediante la palabra clave **WithEvents** para permitir el control de eventos. El formulario\_controlador de eventos de carga realmente crea el objeto asignando un nuevo objeto **Connection** a *connEvent* y, a continuación, se abre la conexión. Por supuesto, en que una aplicación real realizará más procesamiento en el formulario\_controlador de eventos de carga que se muestra aquí.

