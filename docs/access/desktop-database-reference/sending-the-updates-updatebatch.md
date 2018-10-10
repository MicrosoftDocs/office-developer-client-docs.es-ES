---
title: 'Enviar actualizaciones: UpdateBatch'
TOCTitle: 'Sending the Updates: UpdateBatch'
ms:assetid: a840b9a7-7ccd-9c31-7951-8921dadf381e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249778(v=office.15)
ms:contentKeyID: 48546898
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: df52f5bf2dbada1176a76cda3b77dcbc9966b313
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484071"
---
# <a name="sending-the-updates-updatebatch"></a><span data-ttu-id="3f86f-102">Enviar actualizaciones: UpdateBatch</span><span class="sxs-lookup"><span data-stu-id="3f86f-102">Sending the Updates: UpdateBatch</span></span>


<span data-ttu-id="3f86f-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f86f-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="sending-the-updates-updatebatch-method"></a><span data-ttu-id="3f86f-104">Enviar actualizaciones: método UpdateBatch</span><span class="sxs-lookup"><span data-stu-id="3f86f-104">Sending the Updates: UpdateBatch Method</span></span>

<span data-ttu-id="3f86f-p101">El código siguiente abre un **Recordset** en modo de proceso por lotes estableciendo la propiedad **LockType** en **adLockBatchOptimistic** y **CursorLocation** en **adUseClient**. Agrega dos registros nuevos, cambia el valor de un campo en un registro existente y guarda los valores originales; a continuación, llama a **UpdateBatch** para devolver los cambios al origen de datos.</span><span class="sxs-lookup"><span data-stu-id="3f86f-p101">The following code opens a **Recordset** in batch mode by setting the **LockType** property to **adLockBatchOptimistic** and the **CursorLocation** to **adUseClient**. It adds two new records and changes the value of a field in an existing record, saving the original values, and then calls **UpdateBatch** to send the changes back to the data source.</span></span>

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

<span data-ttu-id="3f86f-107">Si está modificando el registro actual o agregando un nuevo registro mientras llama al método **UpdateBatch**, ADO llamará automáticamente al método **Update** para guardar todos los cambios pendientes en el registro actual antes de transmitir los cambios por lotes al proveedor.</span><span class="sxs-lookup"><span data-stu-id="3f86f-107">If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

