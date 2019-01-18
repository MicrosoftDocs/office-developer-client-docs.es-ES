---
title: Objeto Parameter (DAO)
TOCTitle: Parameter Object
ms:assetid: 194efd23-6086-13ac-beb9-c2aec101d6fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845640(v=office.15)
ms:contentKeyID: 48543495
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5df04b1ee06a2224db9e21f67e9c68a3ee5740bf
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698102"
---
# <a name="parameter-object-dao"></a>Objeto Parameter (DAO)


**Se aplica a**: Access 2013, Office 2013

Un objeto **Parameter** representa un valor suministrado a una consulta. El parámetro está asociado con un objeto **QueryDef** creado a partir de una consulta de parámetros.

## <a name="remarks"></a>Observaciones

Los objetos **Parameter** permiten cambiar los argumentos de un objeto **QueryDef** ejecutado con frecuencia sin tener que volver a compilar la consulta.

Mediante las propiedades de un objeto **Parameter**, puede establecer un parámetro de consulta que se puede cambiar antes de ejecutar la consulta. Se puede:

  - Usar la propiedad **Name** para devolver el nombre de un parámetro.

  - Usar la propiedad **Value** para establecer o devolver los valores de parámetros que se utilizarán en la consulta.

  - Usar la propiedad **Type** para devolver el tipo de datos del objeto **Parameter**.

  - Usar la propiedad **Direction** para establecer o devolver si el parámetro es un parámetro de entrada, un parámetro de salida o ambos.

## <a name="example"></a>Ejemplo

En este ejemplo se utilizan objetos **Parameter** y la colección **Parameters** para crear un objeto **QueryDef** temporal y recuperar datos a partir de los cambios efectuados en los **Parameters** del objeto **QueryDef**. Se requiere el procedimiento ParametersChange para que pueda ejecutarse este procedimiento.

```vb
    Sub ParameterX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfReport As QueryDef 
     Dim prmBegin As Parameter 
     Dim prmEnd As Parameter 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create temporary QueryDef object with two 
     ' parameters. 
     Set qdfReport = dbsNorthwind.CreateQueryDef("", _ 
     "PARAMETERS dteBegin DateTime, dteEnd DateTime; " & _ 
     "SELECT EmployeeID, COUNT(OrderID) AS NumOrders " & _ 
     "FROM Orders WHERE ShippedDate BETWEEN " & _ 
     "[dteBegin] AND [dteEnd] GROUP BY EmployeeID " & _ 
     "ORDER BY EmployeeID") 
     Set prmBegin = qdfReport.Parameters!dteBegin 
     Set prmEnd = qdfReport.Parameters!dteEnd 
     
     ' Print report using specified parameter values. 
     ParametersChange qdfReport, prmBegin, #1/1/95#, _ 
     prmEnd, #6/30/95# 
     ParametersChange qdfReport, prmBegin, #7/1/95#, _ 
     prmEnd, #12/31/95# 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub ParametersChange(qdfTemp As QueryDef, _ 
     prmFirst As Parameter, dteFirst As Date, _ 
     prmLast As Parameter, dteLast As Date) 
     ' Report function for ParameterX. 
     
     Dim rstTemp As Recordset 
     Dim fldLoop As Field 
     
     ' Set parameter values and open recordset from 
     ' temporary QueryDef object. 
     prmFirst = dteFirst 
     prmLast = dteLast 
     Set rstTemp = _ 
     qdfTemp.OpenRecordset(dbOpenForwardOnly) 
     Debug.Print "Period " & dteFirst & " to " & dteLast 
     
     ' Enumerate recordset. 
     Do While Not rstTemp.EOF 
     
     ' Enumerate Fields collection of recordset. 
     For Each fldLoop In rstTemp.Fields 
     Debug.Print " - " & fldLoop.Name & " = " & fldLoop; 
     Next fldLoop 
     
     Debug.Print 
     rstTemp.MoveNext 
     Loop 
     
     rstTemp.Close 
     
    End Sub
```
