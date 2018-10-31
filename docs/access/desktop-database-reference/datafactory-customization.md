---
title: Personalización de DataFactory
TOCTitle: DataFactory Customization
ms:assetid: 43cd7416-1f05-87ee-22f0-6cf0d2d1b39f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249205(v=office.15)
ms:contentKeyID: 48544511
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3f058dd76d9ae4f95b6a3d051e741039eb7609f5
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860871"
---
# <a name="datafactory-customization"></a><span data-ttu-id="7c330-102">Personalización de DataFactory</span><span class="sxs-lookup"><span data-stu-id="7c330-102">DataFactory Customization</span></span>


<span data-ttu-id="7c330-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7c330-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7c330-p101">El servicio de datos remoto (RDS) permite obtener fácilmente acceso a datos en un sistema de cliente-servidor de tres niveles. Un control de datos de cliente especifica los parámetros de las cadenas de conexión y de comandos para consultar un origen de datos remoto, o bien, los parámetros del objeto [Recordset](recordset-object-ado.md) y de la cadena de conexión para llevar a cabo una actualización.</span><span class="sxs-lookup"><span data-stu-id="7c330-p101">Remote Data Service (RDS) provides a way to easily perform data access in a three-tier client/server system. A client data control specifies connection and command string parameters to perform a query on a remote data source, or connection string and [Recordset](recordset-object-ado.md) object parameters to perform an update.</span></span>

<span data-ttu-id="7c330-p102">Los parámetros se pasan a un programa de servidor, que realiza la operación de acceso a datos en el origen de datos remoto. RDS proporciona un programa de servidor predeterminado denominado objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md). El objeto **RDSServer.DataFactory** devuelve cualquier objeto **Recordset** generado por una consulta al cliente.</span><span class="sxs-lookup"><span data-stu-id="7c330-p102">The parameters are passed to a server program, which performs the data-access operation on the remote data source. RDS provides a default server program called the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object. The **RDSServer.DataFactory** object returns any **Recordset** object produced by a query to the client.</span></span>

<span data-ttu-id="7c330-p103">Sin embargo, **RDSServer.DataFactory** se limita a realizar consultas y actualizaciones. No puede realizar validaciones ni procesamientos en las cadenas de conexión o de comandos.</span><span class="sxs-lookup"><span data-stu-id="7c330-p103">However, the **RDSServer.DataFactory** is limited to performing queries and updates. It cannot perform any validation or processing on the connection or command strings.</span></span>

<span data-ttu-id="7c330-p104">Con ADO, se puede especificar que **DataFactory** trabaje conjuntamente con otro tipo de programa de servidor denominado \* controlador\*. El controlador puede modificar las cadenas de conexión y de comandos del cliente antes de que se utilicen para obtener acceso al origen de datos. Además, el controlador puede exigir derechos de acceso, que rigen la capacidad del cliente para leer y escribir datos en el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="7c330-p104">With ADO, you can specify that the **DataFactory** work in conjunction with another type of server program called a *handler*. The handler can modify client connection and command strings before they are used to access the data source. In addition, the handler can enforce access rights, which govern the ability of the client to read and write data to the data source.</span></span>

<span data-ttu-id="7c330-114">Los parámetros que utiliza el controlador para modificar los derechos de acceso y parámetros de cliente se especifican en las secciones de un archivo de personalización.</span><span class="sxs-lookup"><span data-stu-id="7c330-114">The parameters the handler uses to modify client parameters and access rights are specified in sections of a customization file.</span></span>

<span data-ttu-id="7c330-115">Vea los temas siguientes para obtener más información sobre la personalización del objeto **DataFactory**:</span><span class="sxs-lookup"><span data-stu-id="7c330-115">See the following topics for more information about customizing the **DataFactory** object:</span></span>

  - [<span data-ttu-id="7c330-116">Introducción al archivo de personalización</span><span class="sxs-lookup"><span data-stu-id="7c330-116">Understanding the Customization File</span></span>](understanding-the-customization-file.md)

  - [<span data-ttu-id="7c330-117">Sección Connect del archivo de personalización</span><span class="sxs-lookup"><span data-stu-id="7c330-117">Customization File Connect Section</span></span>](customization-file-connect-section.md)

  - [<span data-ttu-id="7c330-118">Sección SQL del archivo de personalización</span><span class="sxs-lookup"><span data-stu-id="7c330-118">Customization File SQL Section</span></span>](customization-file-sql-section.md)

  - [<span data-ttu-id="7c330-119">Sección UserList del archivo de personalización</span><span class="sxs-lookup"><span data-stu-id="7c330-119">Customization File UserList Section</span></span>](customization-file-userlist-section.md)

  - [<span data-ttu-id="7c330-120">Sección Logs del archivo de personalización</span><span class="sxs-lookup"><span data-stu-id="7c330-120">Customization File Logs Section</span></span>](customization-file-logs-section.md)

  - [<span data-ttu-id="7c330-121">Configuración de cliente requerida</span><span class="sxs-lookup"><span data-stu-id="7c330-121">Required Client Settings</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/required-client-settings)

  - [<span data-ttu-id="7c330-122">Escribir un controlador personalizado</span><span class="sxs-lookup"><span data-stu-id="7c330-122">Writing Your Own Customized Handler</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/writing-your-own-customized-handler)
