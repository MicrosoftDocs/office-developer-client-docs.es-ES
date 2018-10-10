---
title: Filtrar registros actualizados
TOCTitle: Filtering for Updated Records
ms:assetid: 0dc22b0a-3501-078d-788c-40aa97f2e644
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248857(v=office.15)
ms:contentKeyID: 48543229
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5f95c38da17ded3cc09c4fd8be0ad30342024093
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485821"
---
# <a name="filtering-for-updated-records"></a><span data-ttu-id="3f841-102">Filtrar registros actualizados</span><span class="sxs-lookup"><span data-stu-id="3f841-102">Filtering for Updated Records</span></span>


<span data-ttu-id="3f841-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f841-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="filtering-for-updated-records"></a><span data-ttu-id="3f841-104">Filtrar registros actualizados</span><span class="sxs-lookup"><span data-stu-id="3f841-104">Filtering for Updated Records</span></span>

<span data-ttu-id="3f841-p101">Antes de llamar a **UpdateBatch**, puede usar la propiedad **Filter** del **conjunto de registros** para ver sólo los registros que se han modificado desde que se abrió el **conjunto de registros** o desde la última llamada a **UpdateBatch**. Para ello, establezca **Filter** en **adFilterPendingRecords** para determinar la cantidad de registros que se actualizarán, como se indica más adelante.</span><span class="sxs-lookup"><span data-stu-id="3f841-p101">Before you call **UpdateBatch**, you can use the **Recordset** **Filter** property to view only those records which have been changed since the **Recordset** was opened or the last call to **UpdateBatch**. To do this, set **Filter** equal to **adFilterPendingRecords** to determine how many records will be updated, as shown below.</span></span>

<span data-ttu-id="3f841-107">Este ejemplo es una ampliación del ejemplo de **UpdateBatch** anterior. Ahora se filtra el **conjunto de registros** justo antes de llamar a **UpdateBatch**, mostrando al usuario los registros que cambiarán y permitiéndole cancelar la actualización (mediante el método **CancelBatch** ).</span><span class="sxs-lookup"><span data-stu-id="3f841-107">This example extends the previous **UpdateBatch** example by filtering the **Recordset** just before calling the **UpdateBatch**, showing the user which records will change and allowing her to cancel the update (using the **CancelBatch** method).</span></span>

```vb 
 
'BeginFilterAffected 
    objRs1.Filter = adFilterPendingRecords 
    objRs1.MoveFirst 
     
    strMsg = "The following " & objRs1.RecordCount & " values will " & _ 
             "be updated. Do you wish to proceed?" 
    While Not objRs1.EOF 
        strMsg = strMsg & vbCrLf & objRs1(0) & vbTab & objRs1(1) & vbTab & _ 
                 objRs1(2) & vbCrLf 
        objRs1.MoveNext 
    Wend 
     
    blnResp = MsgBox(strMsg, vbYesNo, "Proceed with Update?") 
    If blnResp = True Then 
        objRs1.UpdateBatch 
    Else 
        objRs1.CancelBatch 
    End If 
'EndFilterAffected 
```

