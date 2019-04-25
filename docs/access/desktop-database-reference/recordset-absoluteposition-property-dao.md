---
title: Propiedad Recordset.AbsolutePosition (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: c35c0c07-f789-524b-0a3d-dfd18fa6eebc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823038(v=office.15)
ms:contentKeyID: 48547569
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 22284abf537f57d98d5f0416b58a9a2ac3c6ebe5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300703"
---
# <a name="recordsetabsoluteposition-property-dao"></a>Propiedad Recordset.AbsolutePosition (DAO)

**Se aplica a:** Access 2013, Office 2013

Configura o devuelve el número de registros con respecto al registro actual de un objeto **Recordset**.

## <a name="syntax"></a>Sintaxis

*expression* .AbsolutePosition

*expression* Variable que representa un objeto **Recordset**.

## <a name="remarks"></a>Comentarios

Puede usar la propiedad **AbsolutePosition** para colocar el puntero del registro actual en un registro específico en función de su posición ordinal en un objeto **Recordset** de tipo Dynaset o instantánea. También puede determinar el número de registro actual comprobando el valor de la propiedad **AbsolutePosition**.

Puesto que el valor de la propiedad **AbsolutePosition** está basado en cero (el valor 0 hace referencia al primer registro del objeto **Recordset**), no se puede establecer en un valor mayor o igual que el número de registros rellenados; si se hace, se produce un error capturable. Puede determinar el número de registros rellenados en el objeto **Recordset** comprobando el valor de la propiedad **RecordCount**. El valor máximo admisible para la propiedad **AbsolutePosition** es el valor de la propiedad **RecordCount** menos 1.

Si no hay un registro actual, por ejemplo cuando no hay ningún registro en el objeto **Recordset**, **AbsolutePosition** devuelve -1. Si el registro actual se elimina, el valor de la propiedad **AbsolutePosition** no se define y se producirá un error capturable si se le hace referencia. Los registros nuevos se agregan al final de la secuencia.

No debe usarse esta propiedad como un número de registro suplente. Los marcadores siguen siendo la forma recomendada de conservar una posición determinada y volver a ella, y son la única forma de colocar el registro actual en todos los tipos de objetos **Recordset**. En particular, la posición de un registro cambia cuando se eliminan uno o varios registros que le preceden. Tampoco hay garantía de que un registro tendrá la misma posición absoluta si se vuelve a crear el objeto **Recordset**, ya que el orden de los registros individuales en un objeto **Recordset** no está garantizado a menos que se cree con una instrucción SQL que use una cláusula ORDER BY.

> [!NOTE]
> - Si se establece la propiedad **AbsolutePosition** en un valor mayor que cero en un objeto **Recordset** recién abierto pero sin rellenar, se produce un error capturable. Primero debe rellenarse el objeto **Recordset** con el método **MoveLast**.
> - La propiedad **AbsolutePosition** no está disponible en objetos **Recordset** de sólo avance ni en objetos **Recordset** abiertos desde consultas de paso con bases de datos ODBC conectadas al motor de base de datos de Microsoft Access.

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
