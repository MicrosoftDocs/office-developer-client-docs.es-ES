---
title: Propiedad Recordset2.PercentPosition (DAO)
TOCTitle: PercentPosition Property
ms:assetid: 830a7d26-6817-233f-ce24-80b572c1c100
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196732(v=office.15)
ms:contentKeyID: 48545996
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052973
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7cf5a0e0a9d0cf3d3cd5ce2b89dc287b41c72f74
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998801"
---
# <a name="recordset2percentposition-property-dao"></a>Propiedad Recordset2.PercentPosition (DAO)

**Se aplica a**: Access 2013, Office 2013

Establece o devuelve un valor que indica la ubicación aproximada del registro actual en el objeto **[Recordset](recordset-object-dao.md)** a partir de un porcentaje de los registros en **Recordset**.

## <a name="syntax"></a>Sintaxis

*expresión* . PercentPosition

*expresión* Variable que representa un objeto **Recordset2** .

## <a name="remarks"></a>Observaciones

Para indicar o cambiar la ubicación aproximada del registro actual en un objeto **Recordset**, puede comprobar o establecer la propiedad **PercentPosition**. Al trabajar con un objeto **Recordset** de tipo Dynaset o Snapshot abierto directamente desde una tabla base, primero rellene el objeto **Recordset** moviendo el último registro antes de establecer o comprobar la propiedad **PercentPosition**. Si usa la propiedad **PercentPosition** antes de rellenar completamente el objeto **Recordset**, el número de movimientos será relativo al número de registros a los que se tuvo acceso como indica el valor de la propiedad **[RecordCount](recordset2-recordcount-property-dao.md)**. Puede moverse hasta el último registro usando el método **[MoveLast](recordset2-movelast-method-dao.md)**.

> [!NOTE]
> No se recomienda el uso de la propiedad **PercentPosition** para mover el registro actual hasta un registro específico en un objeto **Recordset** . La propiedad **[Bookmark](recordset2-bookmark-property-dao.md)** es más apropiada para esta tarea.

Una vez que establezca la propiedad **PercentPosition** en un valor, el registro en la ubicación aproximada correspondiente a ese valor se convierte en el actual y la propiedad **PercentPosition** se restablece con el valor que refleja la ubicación aproximada del registro actual. Por ejemplo, si su objeto **Recordset** contiene solo cinco registros y establece el valor de su propiedad **PercentPosition** en 77, el valor devuelto desde la propiedad **PercentPosition** puede que sea 80 y no 77.

La propiedad **PercentPosition** se aplica a todos los tipos de objetos **Recordset** excepto los objetos **Recordset** de tipo forward – only o los objetos **Recordset** abiertos desde consultas de paso a través con bases de datos remotas.

Puede usar la propiedad **PercentPosition** con una barra de desplazamiento en un formulario o en un cuadro de texto para indicar la ubicación del registro actual en un objeto **Recordset**.

## <a name="example"></a>Ejemplo

En este ejemplo se usa la propiedad **PercentPosition** para mostrar la ubicación del puntero de registro actual con respecto al principio del **Recordset**.

```vb
    Sub PercentPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim strFind As String 
     Dim strMessage As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' PercentPosition only works with dynasets or snapshots. 
     Set rstProducts = dbsNorthwind.OpenRecordset( _ 
     "SELECT ProductName FROM Products " & _ 
     "ORDER BY ProductName", dbOpenSnapshot) 
     
     With rstProducts 
     ' Populate the Recordset. 
     .MoveLast 
     .MoveFirst 
     
     Do While True 
     ' Show current record information and ask user 
     ' for input. 
     strMessage = "Product: " & !ProductName & vbCr & _ 
     "The record pointer is " & _ 
     Format(.PercentPosition, "##0.0") & _ 
     "% from the " & vbCr & _ 
     "beginning of the Recordset." & vbCr & _ 
     "Please enter a character search string " & _ 
     "for a product name." 
     strFind = Trim(InputBox(strMessage)) 
     If strFind = "" Then Exit Do 
     
     ' Try to find a record matching the search string. 
     .FindFirst "ProductName >= '" & strFind & "'" 
     If .NoMatch Then .MoveLast 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
