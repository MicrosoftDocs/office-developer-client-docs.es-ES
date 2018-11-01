---
title: 'Paso 3: Rellenar el cuadro de lista de campos'
TOCTitle: 'Step 3: Populate the Fields List Box'
ms:assetid: b304d3a1-2237-d6f5-6e32-c6e5b9946e10
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249855(v=office.15)
ms:contentKeyID: 48547187
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ae1513c47c79da4f4df7fee2f3f3d7b3507ac1c7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876662"
---
# <a name="step-3-populate-the-fields-list-box"></a><span data-ttu-id="6ca6a-102">Paso 3: Rellenar el cuadro de lista de campos</span><span class="sxs-lookup"><span data-stu-id="6ca6a-102">Step 3: Populate the Fields List Box</span></span>


<span data-ttu-id="6ca6a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6ca6a-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="step-3-populate-the-fields-list-box"></a><span data-ttu-id="6ca6a-104">Paso 3: Rellenar el cuadro de lista de campos</span><span class="sxs-lookup"><span data-stu-id="6ca6a-104">Step 3: Populate the Fields List Box</span></span>

<span data-ttu-id="6ca6a-105">**Para rellenar el cuadro de lista de campos**</span><span class="sxs-lookup"><span data-stu-id="6ca6a-105">**To populate the Fields list box**</span></span>

<span data-ttu-id="6ca6a-106">Inserte el siguiente código en el controlador del evento Click de lstMain:</span><span class="sxs-lookup"><span data-stu-id="6ca6a-106">Insert the following code into the Click event handler of lstMain:</span></span>

```vb 
 
Private Sub lstMain_Click() 
    Dim rec As Record 
    Dim rs As Recordset 
    Set rec = New Record 
    Set rs = New Recordset 
    grs.MoveFirst 
    grs.Move lstMain.ListIndex 
    lstDetails.Clear 
    rec.Open grs 
    Select Case rec.RecordType 
        Case adCollectionRecord: 
            Set rs = rec.GetChildren 
            While Not rs.EOF 
                lstDetails.AddItem rs(0) 
                rs.MoveNext 
            Wend 
        Case adSimpleRecord: 
            recFields rec, lstDetails, txtDetails 
             
        Case adStructDoc: 
    End Select 
     
End Sub 
```

<span data-ttu-id="6ca6a-107">Este código declara y crea una instancia local de **registro** y los objetos **Recordset** , rec y y rs, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6ca6a-107">This code declares and instantiates local **Record** and **Recordset** objects, rec and and rs, respectively.</span></span>

<span data-ttu-id="6ca6a-108">La fila correspondiente al recurso seleccionado en lstMain se convierte la fila actual de grs.</span><span class="sxs-lookup"><span data-stu-id="6ca6a-108">The row corresponding to the resource selected in lstMain is made the current row of grs.</span></span> <span data-ttu-id="6ca6a-109">A continuación, se borra el cuadro de lista **Detalles** y rec se abre con la fila actual de.</span><span class="sxs-lookup"><span data-stu-id="6ca6a-109">Then the **Details** list box is cleared and rec is opened with the current row of .</span></span> <span data-ttu-id="6ca6a-110">A continuación, se borra el cuadro de lista **Detalles** y rec se abre con la fila actual de grs como el origen.</span><span class="sxs-lookup"><span data-stu-id="6ca6a-110">Then the **Details** list box is cleared and rec is opened with the current row of grs as the source.</span></span>

<span data-ttu-id="6ca6a-111">Si el recurso es un registro de colección (según se especifica en **RecordType**), local **Recordset**, rs, se abre sobre los elementos secundarios de rec. A continuación, lstDetails se rellena con los valores de las filas de se abre sobre los elementos secundarios de rec. A continuación, lstDetails se rellena con los valores de las filas de rs.</span><span class="sxs-lookup"><span data-stu-id="6ca6a-111">If the resource is a collection record (as specified by **RecordType**), the local **Recordset**, rs, is opened on the children of rec. Then lstDetails is filled with the values from the rows of is opened on the children of rec. Then lstDetails is filled with the values from the rows of rs.</span></span>

<span data-ttu-id="6ca6a-p102">Si el recurso es un registro simple, se realiza una llamada a recFields. Para obtener más información acerca de recFields, vea el paso siguiente.</span><span class="sxs-lookup"><span data-stu-id="6ca6a-p102">If the resource is a simple record, recFields is called. For more information about recFields, see the next step.</span></span>

<span data-ttu-id="6ca6a-114">Si el recurso es un documento estructurado, entonces no se implementa ningún código.</span><span class="sxs-lookup"><span data-stu-id="6ca6a-114">No code is implemented if the resource is a structured document.</span></span>

