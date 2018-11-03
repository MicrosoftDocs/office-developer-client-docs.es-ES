---
title: 'Paso 2: Llamar al programa de servidor (Tutorial de RDS)'
TOCTitle: 'Step 2: Invoke the Server Program (RDS Tutorial)'
ms:assetid: 45429faa-c1e2-d448-a5b4-b2d77cb94377
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249211(v=office.15)
ms:contentKeyID: 48544549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d3264c58434bf7af6ae4e75c249a7009f39b7d4
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947234"
---
# <a name="step-2-invoke-the-server-program-rds-tutorial"></a><span data-ttu-id="ba036-102">Paso 2: Llamar al programa de servidor (Tutorial de RDS)</span><span class="sxs-lookup"><span data-stu-id="ba036-102">Step 2: Invoke the server program (RDS Tutorial)</span></span>

<span data-ttu-id="ba036-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba036-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ba036-p101">Cuando se llama a un método en el *proxy* cliente, el programa real en el servidor ejecuta el método. En este paso, se ejecutará una consulta en el servidor.</span><span class="sxs-lookup"><span data-stu-id="ba036-p101">When you invoke a method on the client *proxy*, the actual program on the server executes the method. In this step, you'll execute a query on the server.</span></span>

<span data-ttu-id="ba036-106">**Parte A** Si no utilizo [RDSServer.DataFactory](datafactory-object-rdsserver.md) en este tutorial, la forma más conveniente para realizar este paso sería utilizar el [RDS. DataControl](datacontrol-object-rds.md) objeto.</span><span class="sxs-lookup"><span data-stu-id="ba036-106">**Part A**If you weren't using [RDSServer.DataFactory](datafactory-object-rdsserver.md) in this tutorial, the most convenient way to perform this step would be to use the [RDS.DataControl](datacontrol-object-rds.md) object.</span></span> <span data-ttu-id="ba036-107">El objeto **RDS.DataControl** combina el paso anterior de crear un proxy con este paso que emite la consulta.</span><span class="sxs-lookup"><span data-stu-id="ba036-107">The **RDS.DataControl** combines the previous step of creating a proxy, with this step, issuing the query.</span></span>

<span data-ttu-id="ba036-p103">En el objeto **RDS.DataControl**, establezca su propiedad [Server](server-property-rds.md) para identificar dónde se debe crear la instancia del programa de servidor, la propiedad [Connect](connect-property-rds.md) para especificar la cadena de conexión para obtener acceso a los orígenes de datos y la propiedad [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) para especificar el texto de comando de la consulta. Después, use el método [Refresh](refresh-method-rds.md) para hacer que el programa de servidor se conecte al origen de datos, recupere las filas especificadas en la consulta y devuelva un objeto **Recordset** al cliente.</span><span class="sxs-lookup"><span data-stu-id="ba036-p103">Set the **RDS.DataControl** object [Server](server-property-rds.md) property to identify where the server program should be instantiated; the [Connect](connect-property-rds.md) property to specify the connect string to access the data source; and the [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) property to specify the query command text. Then issue the [Refresh](refresh-method-rds.md) method to cause the server program to connect to the data source, retrieve rows specified by the query, and return a **Recordset** object to the client.</span></span>

<span data-ttu-id="ba036-110">Este tutorial no utiliza el objeto **RDS.DataControl**, pero, en caso de utilizarlo, sería del siguiente modo:</span><span class="sxs-lookup"><span data-stu-id="ba036-110">This tutorial does not use the **RDS.DataControl**, but this is how it would look if it did:</span></span>

```vb 
 
Sub RDSTutorial2A() 
 Dim DC as New RDS.DataControl 
 DC.Server = "https://yourServer" 
 DC.Connect = "DSN=Pubs" 
 DC.SQL = "SELECT * FROM Authors" 
 DC.Refresh 
... 
```

<span data-ttu-id="ba036-111">El tutorial tampoco llama a RDS con objetos de ADO, pero, en caso de hacerlo, sería del siguiente modo:</span><span class="sxs-lookup"><span data-stu-id="ba036-111">Nor does the tutorial invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

<span data-ttu-id="ba036-112">**Parte B** El método general de realizar este paso consiste en invocar el método [Query](query-method-rds.md) del objeto **RDSServer.DataFactory** .</span><span class="sxs-lookup"><span data-stu-id="ba036-112">**Part B**The general method of performing this step is to invoke the **RDSServer.DataFactory** object [Query](query-method-rds.md) method.</span></span> <span data-ttu-id="ba036-113">Ese método toma una cadena de conexión, que se utiliza para conectar con un origen de datos, y un texto de comando, utilizado para especificar las filas devueltas desde el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="ba036-113">That method takes a connect string, which is used to connect to a data source, and a command text, which is used to specify the rows to be returned from the data source.</span></span>

<span data-ttu-id="ba036-114">Este tutorial utiliza el método **Query** del objeto **DataFactory**:</span><span class="sxs-lookup"><span data-stu-id="ba036-114">This tutorial uses the **DataFactory** object **Query** method:</span></span>

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

