---
title: Filtrar registros actualizados
TOCTitle: Filtering for Updated Records
ms:assetid: 0dc22b0a-3501-078d-788c-40aa97f2e644
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248857(v=office.15)
ms:contentKeyID: 48543229
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 54183ddff6cfb3f3648bc367588aa49dc17a13fe
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867758"
---
# <a name="filtering-for-updated-records"></a><span data-ttu-id="1233a-102">Filtrar registros actualizados</span><span class="sxs-lookup"><span data-stu-id="1233a-102">Filtering for Updated Records</span></span>


<span data-ttu-id="1233a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1233a-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="filtering-for-updated-records"></a><span data-ttu-id="1233a-104">Filtro de registros actualizados</span><span class="sxs-lookup"><span data-stu-id="1233a-104">Filtering for Updated Records</span></span>

<span data-ttu-id="1233a-p101">Antes de llamar a **UpdateBatch**, puede usar la propiedad **Filter** del **conjunto de registros** para ver sólo los registros que se han modificado desde que se abrió el **conjunto de registros** o desde la última llamada a **UpdateBatch**. Para ello, establezca **Filter** en **adFilterPendingRecords** para determinar la cantidad de registros que se actualizarán, como se indica más adelante.</span><span class="sxs-lookup"><span data-stu-id="1233a-p101">Before you call **UpdateBatch**, you can use the **Recordset** **Filter** property to view only those records which have been changed since the **Recordset** was opened or the last call to **UpdateBatch**. To do this, set **Filter** equal to **adFilterPendingRecords** to determine how many records will be updated, as shown below.</span></span>

<span data-ttu-id="1233a-107">Este ejemplo es una ampliación del ejemplo de **UpdateBatch** anterior. Ahora se filtra el **conjunto de registros** justo antes de llamar a **UpdateBatch**, mostrando al usuario los registros que cambiarán y permitiéndole cancelar la actualización (mediante el método **CancelBatch** ).</span><span class="sxs-lookup"><span data-stu-id="1233a-107">This example extends the previous **UpdateBatch** example by filtering the **Recordset** just before calling the **UpdateBatch**, showing the user which records will change and allowing her to cancel the update (using the **CancelBatch** method).</span></span>

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

