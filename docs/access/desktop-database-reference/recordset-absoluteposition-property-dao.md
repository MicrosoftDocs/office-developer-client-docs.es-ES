---
title: Recordset.AbsolutePosition Property (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: c35c0c07-f789-524b-0a3d-dfd18fa6eebc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823038(v=office.15)
ms:contentKeyID: 48547569
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0140fc9895ae879296236161aee6776f9dbd850c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483552"
---
# <a name="recordsetabsoluteposition-property-dao"></a>Recordset.AbsolutePosition Property (DAO)

**Se aplica a**: Access 2013 | Office 2013

Configura o devuelve el número de registros con respecto al registro actual de un objeto **Recordset**.

## <a name="syntax"></a>Sintaxis

*expresión* . AbsolutePosition

*expresión* Variable que representa un objeto **Recordset** .

## <a name="remarks"></a>Observaciones

Puede usar la propiedad **AbsolutePosition** para colocar el puntero del registro actual en un registro específico en función de su posición ordinal en un objeto **Recordset** de tipo Dynaset o instantánea. También puede determinar el número de registro actual comprobando el valor de la propiedad **AbsolutePosition**.

Puesto que el valor de la propiedad **AbsolutePosition** está basado en cero (el valor 0 hace referencia al primer registro del objeto **Recordset**), no se puede establecer en un valor mayor o igual que el número de registros rellenados; si se hace, se produce un error capturable. Puede determinar el número de registros rellenados en el objeto **Recordset** comprobando el valor de la propiedad **RecordCount**. El valor máximo admisible para la propiedad **AbsolutePosition** es el valor de la propiedad **RecordCount** menos 1.

Si no hay ningún registro actual, como cuando no hay ningún registro en el objeto **Recordset** , **AbsolutePosition** devuelve – 1. Si se elimina el registro actual, el valor de la propiedad **AbsolutePosition** no se define y se produce un error si se hace referencia a él. Los registros nuevos se agregan al final de la secuencia.

No debe usarse esta propiedad como un número de registro suplente. Los marcadores siguen siendo la forma recomendada de conservar una posición determinada y volver a ella, y son la única forma de colocar el registro actual en todos los tipos de objetos **Recordset**. En particular, la posición de un registro cambia cuando se eliminan uno o varios registros que le preceden. Tampoco hay garantía de que un registro tendrá la misma posición absoluta si se vuelve a crear el objeto **Recordset**, ya que el orden de los registros individuales en un objeto **Recordset** no está garantizado a menos que se cree con una instrucción SQL que use una cláusula ORDER BY.

> [!NOTE]
> - Si se establece la propiedad **AbsolutePosition** en un valor mayor que cero en un objeto **Recordset** recién abierto pero sin rellenar, se produce un error capturable. Primero debe rellenarse el objeto **Recordset** con el método **MoveLast**.
> - La propiedad **AbsolutePosition** no está disponible en objetos **Recordset** de tipo forward – only, o en los objetos **Recordset** abiertos desde consultas de paso a través con bases de datos ODBC conectadas por el motor de base de datos de Microsoft Access.

## <a name="example"></a>Ejemplo

En este ejemplo, se usa la propiedad **AbsolutePosition** para realizar un seguimiento del progreso de un bucle que enumera todos los registros de un objeto **Recordset**.

```vb
    Sub AbsolutePositionX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim strMessage As String 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' AbsolutePosition only works with dynasets or snapshots. 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees", _ 
          dbOpenSnapshot) 
     
       With rstEmployees 
          ' Populate Recordset. 
          .MoveLast 
          .MoveFirst 
     
          ' Enumerate Recordset. 
          Do While Not .EOF 
             ' Display current record information. Add 1 to  
             ' AbsolutePosition value because it is zero-based. 
             strMessage = "Employee: " & !LastName & vbCr & _ 
                "(record " & (.AbsolutePosition + 1) & _ 
                " of " & .RecordCount & ")" 
             If MsgBox(strMessage, vbOKCancel) = vbCancel _ 
                Then Exit Do 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
