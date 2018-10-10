---
title: 'Paso 3: Rellenar el cuadro de lista de campos'
TOCTitle: 'Step 3: Populate the Fields List Box'
ms:assetid: b304d3a1-2237-d6f5-6e32-c6e5b9946e10
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249855(v=office.15)
ms:contentKeyID: 48547187
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ca764e2339d0c866922be2982a168afc03d84c1d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483991"
---
# <a name="step-3-populate-the-fields-list-box"></a>Paso 3: Rellenar el cuadro de lista de campos


**Se aplica a**: Access 2013 | Office 2013

## <a name="step-3-populate-the-fields-list-box"></a>Paso 3: Rellenar el cuadro de lista de campos

**Para rellenar el cuadro de lista de campos**

Inserte el siguiente código en el controlador del evento Click de lstMain:

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

Este código declara y crea una instancia local de **registro** y los objetos **Recordset** , rec y y rs, respectivamente.

La fila correspondiente al recurso seleccionado en lstMain se convierte la fila actual de grs. A continuación, se borra el cuadro de lista **Detalles** y rec se abre con la fila actual de. A continuación, se borra el cuadro de lista **Detalles** y rec se abre con la fila actual de grs como el origen.

Si el recurso es un registro de colección (según se especifica en **RecordType**), local **Recordset**, rs, se abre sobre los elementos secundarios de rec. A continuación, lstDetails se rellena con los valores de las filas de se abre sobre los elementos secundarios de rec. A continuación, lstDetails se rellena con los valores de las filas de rs.

Si el recurso es un registro simple, se realiza una llamada a recFields. Para obtener más información acerca de recFields, vea el paso siguiente.

Si el recurso es un documento estructurado, entonces no se implementa ningún código.

