---
title: Ejemplo de la propiedad Status (Field) (VB)
TOCTitle: Status Property Example (Field) (VB)
ms:assetid: 1dc2807f-f469-de97-1280-4b1984b271b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248969(v=office.15)
ms:contentKeyID: 48543601
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ed9f0c90e994b221762588ab941174dbb9c4c764
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486764"
---
# <a name="status-property-example-field-vb"></a>Ejemplo de la propiedad Status (Field) (VB)


**Se aplica a**: Access 2013 | Office 2013

En el ejemplo siguiente se abre un documento desde una carpeta de lectura y escritura mediante el [Proveedor para Publicación en Internet](microsoft-ole-db-provider-for-internet-publishing.md). La propiedad [Status](status-property-ado-field.md) de un objeto [Field](field-object-ado.md) del objeto [Record](record-object-ado.md) primero se establecerá en **adFieldPendingInsert** y, a continuación, se actualizará a **adFieldOk**.

```vb
    'BeginStatusFieldVB
        
     ' to integrate this code replace the values in the source string
    
    Sub Main()
        
       Dim File As ADODB.Record
       Dim strFile As String
       Dim Cnxn As ADODB.Connection
       Dim strCnxn As String
       
       Set Cnxn = New ADODB.Connection
       strCnxn = "url=https://MyServer/"
       Cnxn.Open strCnxn
       
       Set File = New ADODB.Record
       strFile = "Folder/FileName"
       ' Open a read/write document
       File.Source = strFile
       File.ActiveConnection = Cnxn
       File.Mode = adModeReadWrite
       File.Open
    
       Debug.Print "Append a couple of fields"
       
       File.Fields.Append "chektest:fld1", adWChar, 42, adFldUpdatable, "fld1"
       File.Fields.Append "chektest:fld2", adWChar, 42, adFldUpdatable, "fld2"
       
       Debug.Print "status for the fields"
       Debug.Print File.Fields("chektest:fld1").Status 'adfldpendinginsert
       Debug.Print File.Fields("chektest:fld2").Status 'adfldpendinginsert
       
        'turn off error-handling to verify field status
       On Error Resume Next
       
       File.Fields.Update
       
       Debug.Print "Update succeeds"
       Debug.Print File.Fields("chektest:fld1").Status 'adfldpendinginsert + adFieldUnavailable
       Debug.Print File.Fields("chektest:fld2").Status 'adfldpendinginsert + adFieldUnavailable
        
        ' resume default error-handling
       On Error GoTo 0
         
         ' clean up
        File.Close
        Cnxn.Close
        Set File = Nothing
        Set Cnxn = Nothing
          
    End Sub
    'EndStatusFieldVB
```

<br/>

En el ejemplo siguiente se elimina un objeto **Field** conocido desde un objeto **Record** abierto desde un documento. La propiedad **Status** primero se establecerá en **adFieldOK** y, a continuación, en **adFieldPendingUnknown**.

```vb
    'BeginStatusField2VB
    
    ' to integrate this code replace the values in the source string
    
    Sub Main()
    
       Dim File As ADODB.Record
       Dim fld As ADODB.Field
       Dim strFile As String
       
       Dim Cnxn As ADODB.Connection
       Dim strCnxn As String
       
        ' create connection as a URL
       Set Cnxn = New ADODB.Connection
       strCnxn = "url=https://MyServer/"
       Cnxn.Open strCnxn
       Set File = New ADODB.Record
       strFile = "Folder/FileName"
       ' Open a read/write document
       File.Open strFile, Cnxn, adModeReadWrite
       Debug.Print File.Fields("chektest:fld1").Status ' should be adFldOK
       
       ' Delete a field which already exists in the collection
       File.Fields.Delete "chektest:fld1"
       Set fld = File.Fields("chektest:fld1")
       Debug.Print File.Fields("chektest:fld1").Status   ' Pending delete
       
        'turn off error-handling to verify field status
       On Error Resume Next
       
       File.Fields.Update
       
       Debug.Print "Deleted"
       Debug.Print fld.Status   ' Pending unknown
    
        ' resume default error-handling
       On Error GoTo 0
         
         ' clean up
        File.Close
        Cnxn.Close
        Set File = Nothing
        Set Cnxn = Nothing
    
    End Sub
    'EndStatusField2VB
```

<br/>

En el código siguiente se elimina un objeto **Field** desde un objeto **Record** abierto en un documento de sólo lectura. **Status** se establecerá en **adFieldPendingDelete**. Durante la llamada al método [Update](update-method-ado.md), el proceso de eliminación producirá un error y **Status** será **adFieldPendingDelete** más **adFieldPermissionDenied**. [CancelUpdate](cancelupdate-method-ado.md) borra el valor pendiente de **Status**.

```vb
    Sub Main()
       Dim File As ADODB.Record
       Dim fld As ADODB.Field
       Dim Cnxn As ADODB.Connection
       Dim strCnxn As String
       Dim strFile As String
       
        ' create connection as a URL
       Set Cnxn = New ADODB.Connection
       strCnxn = "url=https://MyServer/"
       Cnxn.Open strCnxn
    
       ' Open a read/write document
       Set File = New ADODB.Record
       strFile = "Folder/FileName"
       File.Open strFile, Cnxn, adModeReadWrite, adCreateCollection Or adOpenIfExists
    
       Debug.Print "Try to delete something without permission"
       File.Fields.Delete ("RESOURCE_PARSENAME")
       Set fld = File.Fields("RESOURCE_PARSENAME")
       
       Debug.Print "Pending delete"
       Debug.Print fld.Status   ' Pending delete
       Debug.Print "Delete should fail on Update"
       
        'turn off error-handling to verify field status
       On Error Resume Next
       
       File.Fields.Update   ' Should fail
       
       Debug.Print fld.Status   ' Pending delete plus error
       File.Fields.CancelUpdate
       Debug.Print fld.Status   ' Okay
        
        ' resume default error-handling
       On Error GoTo 0
            
         ' clean up
        File.Close
        Cnxn.Close
        Set File = Nothing
        Set Cnxn = Nothing
       
    End Sub
    'EndStatusField3VB
```
