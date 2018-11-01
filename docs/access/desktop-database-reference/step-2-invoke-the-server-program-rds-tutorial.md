---
title: 'Paso 2: Llamar al programa de servidor (Tutorial de RDS)'
TOCTitle: 'Step 2: Invoke the Server Program (RDS Tutorial)'
ms:assetid: 45429faa-c1e2-d448-a5b4-b2d77cb94377
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249211(v=office.15)
ms:contentKeyID: 48544549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 53ad3306bf9e175566f0a3d02b1454872264d4b6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885482"
---
# <a name="step-2-invoke-the-server-program-rds-tutorial"></a>Paso 2: Invocar el programa de servidor (tutorial de RDS)


**Se aplica a**: Access 2013, Office 2013

Cuando se llama a un método en el *proxy* cliente, el programa real en el servidor ejecuta el método. En este paso, se ejecutará una consulta en el servidor.

**Parte A** Si no utilizo [RDSServer.DataFactory](datafactory-object-rdsserver.md) en este tutorial, la forma más conveniente para realizar este paso sería utilizar el [RDS. DataControl](datacontrol-object-rds.md) objeto. El objeto **RDS.DataControl** combina el paso anterior de crear un proxy con este paso que emite la consulta.

En el objeto **RDS.DataControl**, establezca su propiedad [Server](server-property-rds.md) para identificar dónde se debe crear la instancia del programa de servidor, la propiedad [Connect](connect-property-rds.md) para especificar la cadena de conexión para obtener acceso a los orígenes de datos y la propiedad [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) para especificar el texto de comando de la consulta. Después, use el método [Refresh](refresh-method-rds.md) para hacer que el programa de servidor se conecte al origen de datos, recupere las filas especificadas en la consulta y devuelva un objeto **Recordset** al cliente.

Este tutorial no utiliza el objeto **RDS.DataControl**, pero, en caso de utilizarlo, sería del siguiente modo:

```vb 
 
Sub RDSTutorial2A() 
 Dim DC as New RDS.DataControl 
 DC.Server = "https://yourServer" 
 DC.Connect = "DSN=Pubs" 
 DC.SQL = "SELECT * FROM Authors" 
 DC.Refresh 
... 
```

El tutorial tampoco llama a RDS con objetos de ADO, pero, en caso de hacerlo, sería del siguiente modo:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

**Parte B** El método general de realizar este paso consiste en invocar el método [Query](query-method-rds.md) del objeto **RDSServer.DataFactory** . Ese método toma una cadena de conexión, que se utiliza para conectar con un origen de datos, y un texto de comando, utilizado para especificar las filas devueltas desde el origen de datos.

Este tutorial utiliza el método **Query** del objeto **DataFactory**:

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

