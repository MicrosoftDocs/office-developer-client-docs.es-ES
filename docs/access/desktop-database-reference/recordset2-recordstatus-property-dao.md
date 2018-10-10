---
title: Recordset2.RecordStatus Property (DAO)
TOCTitle: RecordStatus Property
ms:assetid: 178872a9-e361-f277-627d-f91b01ceb6d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845575(v=office.15)
ms:contentKeyID: 48543451
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a13f9f64ab6f699979633c70fb2e8a9386ce2134
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483324"
---
# <a name="recordset2recordstatus-property-dao"></a>Recordset2.RecordStatus Property (DAO)


**Se aplica a**: Access 2013 | Office 2013

## <a name="syntax"></a>Sintaxis

*expresión* . RecordStatus

*expresión* Variable que representa un objeto **Recordset2** .

## <a name="remarks"></a>Observaciones

El valor de la propiedad **RecordStatus** indica si el registro actual estará implicado en la próxima actualización optimista por lotes y cómo estará implicado.

Cuando un usuario cambia un registro, la propiedad **RecordStatus** para ese registro cambia automáticamente a **dbRecordModified**. Igualmente, si se agrega o elimina un registro, **RecordStatus** refleja la constante apropiada. Si después utiliza un método **[Update](recordset2-update-method-dao.md)** en modo de proceso por lotes, DAO enviará una operación apropiada al servidor remoto para cada registro, basado en la propiedad **RecordStatus** del registro.

## <a name="example"></a>Ejemplo

En este ejemplo, se usan las propiedades **RecordStatus** y **DefaultCursorDriver** para mostrar cómo se realiza un seguimiento de los cambios en un objeto **Recordset** local durante la actualización por lotes. La función RecordStatusOutput es necesaria para que se ejecute este procedimiento.

```vb 
Sub RecordStatusX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset2 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM authors", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 .MoveFirst 
 Debug.Print "Original record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .Edit 
 !au_lname = "Bowen" 
 .Update 
 Debug.Print "Edited record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .AddNew 
 !au_lname = "NewName" 
 .Update 
 Debug.Print "New record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .Delete 
 Debug.Print "Deleted record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 ' Close the local recordset without updating the 
 ' data on the server. 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
Function RecordStatusOutput(lngTemp As Long) As String 
 
 Dim strTemp As String 
 
 strTemp = "" 
 
 ' Construct an output string based on the RecordStatus 
 ' value. 
If lngTemp = dbRecordUnmodified Then _ 
 strTemp = "[dbRecordUnmodified]" 
 If lngTemp = dbRecordModified Then _ 
 strTemp = "[dbRecordModified]" 
 If lngTemp = dbRecordNew Then _ 
 strTemp = "[dbRecordNew]" 
 If lngTemp = dbRecordDeleted Then _ 
 strTemp = "[dbRecordDeleted]" 
 If lngTemp = dbRecordDBDeleted Then _ 
 strTemp = "[dbRecordDBDeleted]" 
 
 RecordStatusOutput = strTemp 
 
End Function 
 
```

