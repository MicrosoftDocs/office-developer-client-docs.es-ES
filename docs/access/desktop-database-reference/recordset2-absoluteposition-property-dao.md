---
title: Recordset2.AbsolutePosition Property (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: 91ca203f-0c80-67f4-e180-415b6af05030
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197637(v=office.15)
ms:contentKeyID: 48546358
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053074
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c5eb8c80743b5fac17f7a3c8d11080863e511eb8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888604"
---
# <a name="recordset2absoluteposition-property-dao"></a>Recordset2.AbsolutePosition Property (DAO)


**Se aplica a**: Access 2013, Office 2013

Establece o devuelve el número de registro relativo del registro actual de un objeto **Recordset2**.

## <a name="syntax"></a>Sintaxis

*expresión* . AbsolutePosition

*expresión* Variable que representa un objeto **Recordset2** .

## <a name="remarks"></a>Observaciones

Puede usar la propiedad **AbsolutePosition** para colocar el puntero del registro actual en un registro específico basado en su posición ordinal en un objeto **Recordset2** de tipo Dynaset o Snapshot. Puede también determinar el número del registro actual comprobando del valor de la propiedad **AbsolutePosition**.

Como el valor de la propiedad **AbsolutePosition** se basa en cero (es decir, un valor de 0 hace referencia al primer registro en el objeto **Recordset2**), no puede establecerlo en un valor mayor o igual al número de registros rellenados; si lo hace se producirá un error capturable. Puede determinar el número de registros rellenados en el objeto **Recordset2** comprobando el valor de la propiedad **RecordCount**. El valor máximo permitido para la propiedad **AbsolutePosition** es el valor de la propiedad **RecordCount** menos 1.

Si no hay ningún registro actual, como cuando no hay ningún registro en el objeto **Recordset2** , **AbsolutePosition** devuelve – 1. Si se elimina el registro actual, el valor de la propiedad **AbsolutePosition** no se define y se produce un error si se hace referencia a él. Los registros nuevos se agregan al final de la secuencia.

No debería usar esta propiedad como un número de registro suplente. Los marcadores son todavía el método recomendado para retener cierta posición y volver a ella, y son la única manera de colocar el registro actual a través de todos los tipos de objetos **Recordset2**. En particular, la posición de un registro cambia cuando se eliminan uno o más registros anteriores. Además, no se tiene la certeza de que un registro tenga exactamente la misma posición si el objeto **Recordset2** se vuelve a crear porque no se garantiza el orden de los registros individuales en un objeto **Recordset** a no ser que se cree con una instrucción SQL mediante el uso de una cláusula ORDER BY.


> [!NOTE]
> <UL>
> <LI>
> <P>Al establecer la propiedad <STRONG>AbsolutePosition</STRONG> en un valor mayor que cero en un objeto <STRONG>Recordset2</STRONG> recién abierto pero sin rellenar, se provoca un error capturable. Primero, rellene el objeto <STRONG>Recordset2</STRONG> mediante el método <STRONG>MoveLast</STRONG>.</P>
> <LI>
> <P>La propiedad <STRONG>AbsolutePosition</STRONG> no está disponible en los objetos <STRONG>Recordset2</STRONG> tipo forward – only, o en los objetos <STRONG>Recordset2</STRONG> abiertos desde consultas de paso a través con bases de datos ODBC conectadas por el motor de base de datos de Microsoft Access.</P></LI></UL>



## <a name="example"></a>Ejemplo

En este ejemplo se usa la propiedad **AbsolutePosition** para realizar un seguimiento del proceso de un bucle que enumera todos los registros de un objeto **Recordset2**.

```vb
    Sub AbsolutePositionX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset2 
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
