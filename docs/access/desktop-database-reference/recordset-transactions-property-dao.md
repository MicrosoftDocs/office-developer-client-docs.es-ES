---
title: Propiedad Recordset.Transactions (DAO)
TOCTitle: Transactions Property
ms:assetid: 7830c056-8d6a-7942-7993-aa04b29cd77f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196110(v=office.15)
ms:contentKeyID: 48545746
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b23568e0830ef07e58119d02c4d221dad4b1d015
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307598"
---
# <a name="recordsettransactions-property-dao"></a>Propiedad Recordset.Transactions (DAO)


**Se aplica a:** Access 2013, Office 2013

Devuelve un valor que indica si un objeto admite transacciones. **Boolean** de solo lectura.

## <a name="syntax"></a>Sintaxis

*expresión* . Transacciones

*expression* Variable que representa un objeto **Recordset**.

## <a name="remarks"></a>Comentarios

En un área de trabajo de Microsoft Access, también puede usar la propiedad **Transactions** con objetos **Recordset** de tipo Dynaset o de tabla. Los objetos Recordset de tipo **[snapshot](recordset-object-dao.md)** y forward-only siempre **devuelven False**.

Si un objeto **Recordset** de tipo Dynaset o Table se basa en una tabla de motor de base de datos de Microsoft Access, la propiedad **Transactions** será **True** y se pueden usar las transacciones. Puede ser que otros motores de bases de datos no admitan transacciones. Por ejemplo, no se pueden usar transacciones en un objeto **Recordset** de tipo Dynaset basado en una tabla de Paradox.

Compruebe la propiedad **Transactions** antes de usar el método **[BeginTrans](dbengine-begintrans-method-dao.md)** en el objeto [**Workspace**](workspace-object-dao.md) del objeto **Recordset** para asegurarse de que se admiten transacciones. El uso de los métodos **BeginTrans**, **CommitTrans** o **Rollback** no tiene ningún efecto en un objeto no admitido.

## <a name="example"></a>Ejemplo

En este ejemplo se muestra la propiedad **Transactions** en áreas de trabajo de Microsoft Access.

```vb 
Sub TransactionsX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim conPubs As Connection 
 Dim rstTemp As Recordset 
 
 Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Open two different Recordset objects and display the 
 ' Transactions property of each. 
 
 Debug.Print "Opening Microsoft Access table-type " & _ 
 "recordset..." 
 Set rstTemp = dbsNorthwind.OpenRecordset( _ 
 "Employees", dbOpenTable) 
 Debug.Print " Transactions = " & rstTemp.Transactions 
 
 Debug.Print "Opening forward-only-type " & _ 
 "recordset where the source is an SQL statement..." 
 Set rstTemp = dbsNorthwind.OpenRecordset( _ 
 "SELECT * FROM Employees", dbOpenForwardOnly) 
 Debug.Print " Transactions = " & rstTemp.Transactions 
 
 rstTemp.Close 
 dbsNorthwind.Close 
 conPubs.Close 
 wrkAcc.Close 
End Sub 
 
```

