---
title: Using the Connection Object (Access)
TOCTitle: Using the Connection Object
ms:assetid: e8786411-2be4-8d75-9df7-e345d5a6a7e8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250177(v=office.15)
ms:contentKeyID: 48548423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cd3e691258fe5950f40c36a1efcaed8e79810c7a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484528"
---
# <a name="using-the-connection-object-access"></a><span data-ttu-id="95ade-102">Using the Connection Object (Access)</span><span class="sxs-lookup"><span data-stu-id="95ade-102">Using the Connection Object (Access)</span></span>


<span data-ttu-id="95ade-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="95ade-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="95ade-p101">Un objeto **Connection** representa una sesión única con un origen de datos. En el caso de un sistema de base de datos cliente/servidor, puede ser equivalente a una conexión de red real con el servidor. Según la funcionalidad admitida por el proveedor, algunas colecciones, métodos o propiedades de un objeto **Connection** podrían no estar disponibles.</span><span class="sxs-lookup"><span data-stu-id="95ade-p101">A **Connection** object represents a unique session with a data source. In the case of a client/server database system, it can be equivalent to an actual network connection to the server. Depending on the functionality supported by the provider, some collections, methods, or properties of a **Connection** object might not be available.</span></span>

<span data-ttu-id="95ade-107">Antes de abrir un objeto **Connection**, debe definir parte de la información sobre el origen de datos y el tipo de conexión.</span><span class="sxs-lookup"><span data-stu-id="95ade-107">Before opening a **Connection** object, you must define certain information about the data source and type of connection.</span></span> <span data-ttu-id="95ade-108">El parámetro *ConnectionString* del método **Open** del objeto de **conexión** , o la propiedad **ConnectionString** en el objeto **Connection** , normalmente contiene la mayoría de esta información.</span><span class="sxs-lookup"><span data-stu-id="95ade-108">The *ConnectionString* parameter of the **Connection** object **Open** method — or the **ConnectionString** property on the **Connection** object — usually contains most of this information.</span></span> <span data-ttu-id="95ade-109">Una cadena de conexión es una cadena de caracteres que define un número variable de argumentos.</span><span class="sxs-lookup"><span data-stu-id="95ade-109">A connection string is a string of characters that defines a variable number of arguments.</span></span> <span data-ttu-id="95ade-110">Los argumentos, algunos requeridos por ADO y otros específicos del proveedor, contienen información que el objeto **Connection** debe tener para realizar su trabajo.</span><span class="sxs-lookup"><span data-stu-id="95ade-110">The arguments — some required by ADO, but others provider-specific — contain information that the **Connection** object must have to carry out its work.</span></span> <span data-ttu-id="95ade-111">Los argumentos que componen el parámetro *ConnectionString* se separan con punto y coma (;).</span><span class="sxs-lookup"><span data-stu-id="95ade-111">The arguments that make up the *ConnectionString* parameter are separated with semicolons (;).</span></span>


> [!NOTE]
> <P><span data-ttu-id="95ade-p103">También puede especificar un nombre del origen de datos ODBC (DSN) o un archivo de vínculo de datos (UDL) en una cadena de conexión. Para obtener más información acerca de los DSN, vea Orígenes de datos en la primera parte de <EM>Referencia del programador de ODBC</EM>. Para obtener más información acerca de los UDL, vea Introducción a la API de vínculo de datos en la <EM>Referencia del programador de OLE DB</EM>.</span><span class="sxs-lookup"><span data-stu-id="95ade-p103">You can also specify an ODBC Data Source Name (DSN) or a Data Link (UDL) file in a connection string. For more information about DSNs, see Data Sources in Part 1 of the <EM>ODBC Programmer's Reference</EM>. For more information about UDLs, see Data Link API Overview in the <EM>OLE DB Programmer's Reference</EM>.</span></span></P>


