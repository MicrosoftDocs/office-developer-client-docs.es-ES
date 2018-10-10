---
title: Parameter.Direction Property (DAO)
TOCTitle: Direction Property
ms:assetid: b78c87ff-1181-21ef-7126-92d309751005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822422(v=office.15)
ms:contentKeyID: 48547300
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053586
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4612b578971f59744e25c15d3762cc893f6f71ef
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483985"
---
# <a name="parameterdirection-property-dao"></a>Parameter.Direction Property (DAO)


**Se aplica a**: Access 2013 | Office 2013


## <a name="syntax"></a>Sintaxis

*expresión* . Dirección

*expresión* Variable que representa un objeto **Parameter** .

## <a name="remarks"></a>Observaciones

La configuración o el valor devuelto es un tipo de datos Long que se puede establecer en una de las constantes **[ParameterDirectionEnum](parameterdirectionenum-enumeration-dao.md)**.

Use la propiedad **Direction** para determinar si el parámetro es un parámetro de entrada, un parámetro de salida, ambos o el valor devuelto del procedimiento. Algunos controladores ODBC no proporcionan información sobre la dirección de los parámetros a una instrucción SELECT o llamada a procedimiento. En estos casos, es necesario establecer la dirección antes de ejecutar la consulta.

Por ejemplo, el siguiente procedimiento devuelve un valor desde un procedimiento almacenado llamado "obtener\_empleados":

{? = llamada get\_empleados}

Esta llamada produce un parámetro: el valor devuelto. Debe establecer la dirección de este parámetro en **dbParamOutput** o **dbParamReturnValue** antes de ejecutar **[QueryDef](querydef-object-dao.md)**.

Debe establecer todas las direcciones de parámetros excepto **dbParamInput** antes de establecer o tener acceso a los valores de los parámetros y antes de ejecutar **QueryDef**.

Debe usar **dbParamReturnValue** para los valores devueltos, pero en los casos en que el controlador o el servidor no admitan dicha opción, puede usar **dbParamOutput** en su lugar.

El controlador de Microsoft SQL Server establece automáticamente la propiedad **Direction** para todos los parámetros de procedimientos. No todos los controladores ODBC pueden determinar la dirección de un parámetro de consulta. En estos casos, es necesario establecer la dirección antes de ejecutar la consulta.

## <a name="example"></a>Ejemplo

En este ejemplo, se usa la propiedad **Direction** para configurar los parámetros de una consulta en un origen de datos ODBC.

```vb 
Sub DirectionX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset 
 Dim strSQL As String 
 Dim intLoop As Integer 
 
 ' Create ODBC workspace and open a connection to a 
 ' Microsoft SQL Server database. 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Set SQL string to call the stored procedure 
 ' getempsperjob. 
 strSQL = "{ call getempsperjob (?, ?) }" 
 
 Set qdfTemp = conMain.CreateQueryDef("", strSQL) 
 
 With qdfTemp 
 ' Indicate that the two query parameters will only 
 ' pass information to the stored procedure. 
 .Parameters(0).Direction = dbParamInput 
 .Parameters(1).Direction = dbParamInput 
 
 ' Assign initial parameter values. 
 .Parameters(0) = "0877" 
 .Parameters(1) = 0 
 
 Set rstTemp = .OpenRecordset() 
 
 With rstTemp 
 ' Loop through all valid values for the second 
 ' parameter. For each value, requery the recordset 
 ' to obtain the correct results and then print out 
 ' the contents of the recordset. 
 For intLoop = 1 To 14 
 qdfTemp.Parameters(1) = intLoop 
 .Requery 
 Debug.Print "Publisher = " & _ 
 qdfTemp.Parameters(0) & _ 
 ", job = " & intLoop 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 Next intLoop 
 .Close 
 End With 
 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

