---
title: Realizar una conexión
TOCTitle: Making a Connection
ms:assetid: 188f6794-f4ec-8e8d-5adc-bdee36f4c9ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248932(v=office.15)
ms:contentKeyID: 48543472
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7bd99419a841a8fa876dd0ad30b4d06360a27df1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882052"
---
# <a name="making-a-connection"></a><span data-ttu-id="8c4af-102">Realizar una conexión</span><span class="sxs-lookup"><span data-stu-id="8c4af-102">Making a Connection</span></span>

<span data-ttu-id="8c4af-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8c4af-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8c4af-p101">Para conectarse a un origen de datos, debe especificar una *cadena de conexión*, cuyos parámetros podrían ser distintos para cada proveedor y para cada origen de datos. Para obtener más información, vea [Crear la cadena de conexión](creating-the-connection-string.md).</span><span class="sxs-lookup"><span data-stu-id="8c4af-p101">To connect to a data source, you must specify a *connection string*, the parameters of which might differ for each provider and data source. For more information, see [Creating the Connection String](creating-the-connection-string.md).</span></span>

<span data-ttu-id="8c4af-p102">Lo más normal es que ADO abra una conexión utilizando el método **Open** del objeto **Connection**. La sintaxis del método **Open** se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="8c4af-p102">ADO most commonly opens a connection by using the **Connection** object **Open** method. The syntax for the **Open** method is shown here:</span></span>

```vb
Dim connection as New ADODB.Connection 
connection.Open ConnectionString, UserID, Password, OpenOptions
```

<span data-ttu-id="8c4af-108">Otra posibilidad es invocar una técnica de acceso directo, **Recordset.Open**, para abrir una conexión implícita y emitir un comando a través de esa conexión en una sola operación.</span><span class="sxs-lookup"><span data-stu-id="8c4af-108">Alternatively, you can invoke a shortcut technique, **Recordset.Open**, to open an implicit connection and issue a command over that connection in one operation.</span></span> <span data-ttu-id="8c4af-109">Para ello, pasando una cadena de conexión válida como el argumento *ActiveConnection* para el método **Open** .</span><span class="sxs-lookup"><span data-stu-id="8c4af-109">Do this by passing in a valid connection string as the *ActiveConnection* argument to the **Open** method.</span></span> <span data-ttu-id="8c4af-110">Esta es la sintaxis para cada método en Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="8c4af-110">Here is the syntax for each method in Visual Basic:</span></span>

```vb
Dim recordset as ADODB.Recordset 
Set recordset = New ADODB.Recordset 
recordset.Open Source, ActiveConnection, CursorType, LockType, Options
```

> [!NOTE]
> <span data-ttu-id="8c4af-p104">[!NOTA] ¿Cuándo conviene utilizar un objeto **Connection** y cuando el acceso directo **Recordset.Open** ? Utilice el objeto **Connection** si piensa abrir más de un **conjunto de registros**, o cuando tenga que ejecutar varios comandos. ADO sigue creando una conexión implícitamente cuando se utiliza el acceso directo **Recordset.Open**.</span><span class="sxs-lookup"><span data-stu-id="8c4af-p104">When should you use a **Connection** object vs. the **Recordset.Open** shortcut? Use the **Connection** object if you plan to open more than one **Recordset**, or when executing multiple commands. A connection is still created by ADO implicitly when you use the **Recordset.Open** shortcut.</span></span>


