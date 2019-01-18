---
title: 'Envío de actualizaciones: UpdateBatch'
TOCTitle: 'Sending the updates: UpdateBatch'
ms:assetid: a840b9a7-7ccd-9c31-7951-8921dadf381e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249778(v=office.15)
ms:contentKeyID: 48546898
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca97f3ec2cbddfae4d62a72e5e6148a57abb4325
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718983"
---
# <a name="sending-the-updates-updatebatch"></a>Envío de actualizaciones: UpdateBatch


**Se aplica a**: Access 2013, Office 2013

## <a name="sending-the-updates-updatebatch-method"></a>Enviar actualizaciones: método UpdateBatch

El código siguiente abre un **Recordset** en modo de proceso por lotes estableciendo la propiedad **LockType** en **adLockBatchOptimistic** y **CursorLocation** en **adUseClient**. Agrega dos registros nuevos, cambia el valor de un campo en un registro existente y guarda los valores originales; a continuación, llama a **UpdateBatch** para devolver los cambios al origen de datos.

```vb 
 
'BeginBatchUpdate 
    strSQL = "SELECT ShipperId, CompanyName, Phone FROM Shippers" 
                  
    objRs1.CursorLocation = adUseClient 
    objRs1.Open strSQL, strConn, adOpenStatic, adLockBatchOptimistic, adCmdText 
     
    ' Change value of Phone field for first record in Recordset, saving value 
    ' for later restoration. 
    intId = objRs1("ShipperId") 
    strPhone = objRs1("Phone") 
     
    objRs1("Phone") = "(111) 555-1111" 
     
    'Add two new records 
    For i = 0 To 1 
        objRs1.AddNew 
        objRs1(1) = "New Shipper #" & CStr((i + 1)) 
        objRs1(2) = "(nnn) 555-" & i & i & i & i 
    Next i 
     
    ' Send the updates 
    objRs1.UpdateBatch 
'EndBatchUpdate 
```

Si está modificando el registro actual o agregando un nuevo registro mientras llama al método **UpdateBatch**, ADO llamará automáticamente al método **Update** para guardar todos los cambios pendientes en el registro actual antes de transmitir los cambios por lotes al proveedor.

