---
title: QueryDef.MaxRecords Property (DAO)
TOCTitle: MaxRecords Property
ms:assetid: 7492cde9-be30-3473-dabc-9602465910d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195877(v=office.15)
ms:contentKeyID: 48545664
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053583
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 87f193be1f7261a4aecbfe1cceb4fe5a55038702
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882108"
---
# <a name="querydefmaxrecords-property-dao"></a>QueryDef.MaxRecords Property (DAO)


**Se aplica a**: Access 2013, Office 2013


Establece o devuelve el número máximo de registros que se devuelven desde una consulta en un origen de datos ODBC.

## <a name="syntax"></a>Sintaxis

*expresión* . Número máximo de registros

*expresión* Variable que representa un objeto **QueryDef** .

## <a name="remarks"></a>Observaciones

El valor predeterminado es 0, lo que indica que no hay límite en el número de registros devueltos.

Una vez que el número de filas especificado por **MaxRecords** se devuelve a la aplicación del usuario en un **[Recordset](recordset-object-dao.md)**, el procesador de consultas dejará de devolver registros adicionales incluso si hay más registros cualificados para su inclusión en **Recordset**. Esta propiedad es útil en situaciones donde los recursos de cliente limitados prohíben la administración de grandes cantidades de registros.


> [!NOTE]
> <P>[!NOTA] La propiedad <STRONG>MaxRecords</STRONG> sólo se puede usar con un origen de datos ODBC.</P>



## <a name="example"></a>Ejemplo

En este ejemplo se utiliza la propiedad **MaxRecords** para establecer un límite sobre el número de registros que devuelve una consulta en un origen de datos ODBC.

```vb 
Sub MaxRecordsX() 
 
 Dim dbsCurrent As Database 
 Dim qdfPassThrough As QueryDef 
 Dim qdfLocal As QueryDef 
 Dim rstTemp As Recordset 
 
 ' Open a database from which QueryDef objects can be 
 ' created. 
 Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
 ' Create a pass-through query to retrieve data from 
 ' a Microsoft SQL Server database. 
 Set qdfPassThrough = _ 
 dbsCurrent.CreateQueryDef("") 
 
 ' Set the properties of the new query, limiting the 
 ' number of returnable records to 20. 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 qdfPassThrough.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 qdfPassThrough.SQL = "SELECT * FROM titles" 
 qdfPassThrough.ReturnsRecords = True 
 qdfPassThrough.MaxRecords = 20 
 
 Set rstTemp = qdfPassThrough.OpenRecordset() 
 
 ' Display results of query. 
 Debug.Print "Query results:" 
 With rstTemp 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 dbsCurrent.Close 
 
End Sub 
 
```

