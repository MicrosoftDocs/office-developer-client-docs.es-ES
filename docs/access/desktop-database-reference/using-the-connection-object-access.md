---
title: Uso del objeto Connection (Access)
TOCTitle: Using the Connection Object
ms:assetid: e8786411-2be4-8d75-9df7-e345d5a6a7e8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250177(v=office.15)
ms:contentKeyID: 48548423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d16b802140e2dcbbd85988bee316ae27236c3235
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305925"
---
# <a name="using-the-connection-object-access"></a><span data-ttu-id="86cb1-102">Uso del objeto Connection (Access)</span><span class="sxs-lookup"><span data-stu-id="86cb1-102">Using the Connection object (Access)</span></span>


<span data-ttu-id="86cb1-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="86cb1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="86cb1-p101">Un objeto **Connection** representa una sesión única con un origen de datos. En el caso de un sistema de base de datos cliente/servidor, puede ser equivalente a una conexión de red real con el servidor. Según la funcionalidad admitida por el proveedor, algunas colecciones, métodos o propiedades de un objeto **Connection** podrían no estar disponibles.</span><span class="sxs-lookup"><span data-stu-id="86cb1-p101">A **Connection** object represents a unique session with a data source. In the case of a client/server database system, it can be equivalent to an actual network connection to the server. Depending on the functionality supported by the provider, some collections, methods, or properties of a **Connection** object might not be available.</span></span>

<span data-ttu-id="86cb1-p102">Antes de abrir un objeto **Connection**, debe definir parte de la información sobre el origen de datos y el tipo de conexión. El parámetro *ConnectionString* del método **Open** del objeto **Connection** (o la propiedad **ConnectionString** del objeto **Connection**) normalmente contiene la mayor parte de esta información. Una cadena de conexión es una cadena de caracteres que define un número variable de argumentos. Los argumentos, algunos requeridos por ADO y otros específicos del proveedor, contienen información que el objeto **Connection** debe tener para realizar su trabajo. Los argumentos que componen el parámetro *ConnectionString* se separan con caracteres de punto y coma (;).</span><span class="sxs-lookup"><span data-stu-id="86cb1-p102">Before opening a **Connection** object, you must define certain information about the data source and type of connection. The *ConnectionString* parameter of the **Connection** object **Open** method — or the **ConnectionString** property on the **Connection** object — usually contains most of this information. A connection string is a string of characters that defines a variable number of arguments. The arguments — some required by ADO, but others provider-specific — contain information that the **Connection** object must have to carry out its work. The arguments that make up the *ConnectionString* parameter are separated with semicolons (;).</span></span>

> [!NOTE]
> <span data-ttu-id="86cb1-p103">También puede especificar un nombre del origen de datos ODBC (DSN) o un archivo de vínculo de datos (UDL) en una cadena de conexión. Para obtener más información acerca de los DSN, vea Orígenes de datos en la primera parte de *Referencia del programador de ODBC*. Para obtener más información acerca de los UDL, vea Introducción a la API de vínculo de datos en la *Referencia del programador de OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="86cb1-p103">You can also specify an ODBC Data Source Name (DSN) or a Data Link (UDL) file in a connection string. For more information about DSNs, see Data Sources in Part 1 of the *ODBC Programmer's Reference*. For more information about UDLs, see Data Link API Overview in the *OLE DB Programmer's Reference*.</span></span>

<span data-ttu-id="86cb1-115">Esta sección incluye los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="86cb1-115">This section includes the following topics:</span></span>

- [<span data-ttu-id="86cb1-116">Crear la cadena de conexión</span><span class="sxs-lookup"><span data-stu-id="86cb1-116">Creating the connection string</span></span>](creating-the-connection-string.md)
- [<span data-ttu-id="86cb1-117">Controlar transacciones</span><span class="sxs-lookup"><span data-stu-id="86cb1-117">Controlling transactions</span></span>](controlling-transactions.md)
