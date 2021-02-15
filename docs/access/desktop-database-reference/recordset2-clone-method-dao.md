---
title: Método Recordset2.Clone (DAO)
TOCTitle: Clone Method
ms:assetid: f0d32cb1-03f6-395d-2509-b2139a5fdc68
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836567(v=office.15)
ms:contentKeyID: 48548614
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6780a27d573f5ff7ff41060074fb8abb9f8e2b80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307395"
---
# <a name="recordset2clone-method-dao"></a>Método Recordset2.Clone (DAO)

**Se aplica a:** Access 2013, Office 2013

Crea un objeto **[Recordset](recordset-object-dao.md)** duplicado que hace referencia al objeto **Recordset2** original.

## <a name="syntax"></a>Sintaxis

*expression* .Clone

*expresión* Variable que representa un objeto **Recordset2.**

## <a name="return-value"></a>Valor devuelto

Recordset

## <a name="remarks"></a>Comentarios

Utilice el método **Clone** para crear varios objetos **Recordset** duplicados. Cada conjunto de registros puede tener su propio registro actual. Si se utiliza **Clone** por sí mismo, no se modifican los datos en los objetos o en las estructuras subyacentes. Cuando utiliza el método **Clone**, puede compartir marcadores entre dos o más objetos **Recordset2** porque sus marcadores son intercambiables.

Puede utilizar el método **Clone** cuando desea realizar una operación en un conjunto de registros que requiere varios registros actuales. Es más rápido y eficaz que abrir un segundo conjunto de registros. Cuando se crea un conjunto de registros con el método **Clone**, al principio no tiene un registro actual. Para que haya un registro activo antes de utilizar el clon del conjunto de registros, debe definir la propiedad **[Bookmark](recordset2-bookmark-property-dao.md)** o utilizar uno de los métodos **[Move](recordset-movefirst-method-dao.md)**, uno de los métodos **[Find](recordset2-findfirst-method-dao.md)** o el método **[Seek](recordset2-seek-method-dao.md)**.

El uso del método **[Close](connection-close-method-dao.md)** en el objeto original o duplicado no afecta al otro objeto. Por ejemplo, utilizar **Close** en el conjunto de registros original no cierra el clon.

> [!NOTE]
> - Al cerrar una copia del conjunto de registros en una transacción pendiente, se genera una operación **Rollback** implícita.
> - Al clonar un objeto **Recordset** de tipo tabla en un área de trabajo de Microsoft Access, no se clona el valor de la propiedad **[Index](recordset2-index-property-dao.md)** en la nueva copia del conjunto de registros. Debe copiar el valor de la propiedad **Index** manualmente.

## <a name="example"></a>Ejemplo

En este ejemplo se utiliza el método **Clone** para crear copias de un conjunto de registros y, a continuación, se deja que el usuario coloque el puntero de registros de cada copia de manera independiente.

```vb
    Sub CloneX() 
     
       Dim dbsNorthwind As Database 
       Dim arstProducts(1 To 3) As Recordset2 
       Dim intLoop As Integer 
       Dim strMessage As String 
       Dim strFind As String 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' If the following SQL statement will be used often,  
       ' creating a permanent QueryDef will result in better 
       ' performance. 
       Set arstProducts(1) = dbsNorthwind.OpenRecordset( _ 
          "SELECT ProductName FROM Products " & _ 
          "ORDER BY ProductName", dbOpenSnapshot) 
     
       ' Create two clones of the original Recordset. 
       Set arstProducts(2) = arstProducts(1).Clone 
       Set arstProducts(3) = arstProducts(1).Clone 
     
       Do While True 
     
          ' Loop through the array so that on each pass, the  
          ' user is searching a different copy of the same  
          ' Recordset. 
          For intLoop = 1 To 3 
     
             ' Ask for search string while showing where the 
             ' current record pointer is for each Recordset. 
             strMessage = _ 
                "Recordsets from Products table:" & vbCr & _ 
                "  1 - Original - Record pointer at " & _ 
                arstProducts(1)!ProductName & vbCr & _ 
                "  2 - Clone - Record pointer at " & _ 
                arstProducts(2)!ProductName & vbCr & _ 
                "  3 - Clone - Record pointer at " & _ 
                arstProducts(3)!ProductName & vbCr & _ 
                "Enter search string for #" & intLoop & ":" 
             strFind = Trim(InputBox(strMessage)) 
             If strFind = "" Then Exit Do 
     
             ' Find the search string; if there's no match, jump 
             ' to the last record. 
             With arstProducts(intLoop) 
                .FindFirst "ProductName >= '" & strFind & "'" 
                If .NoMatch Then .MoveLast 
             End With 
     
          Next intLoop 
     
       Loop 
     
       arstProducts(1).Close 
       arstProducts(2).Close 
       arstProducts(3).Close 
       dbsNorthwind.Close 
     
    End Sub
```
