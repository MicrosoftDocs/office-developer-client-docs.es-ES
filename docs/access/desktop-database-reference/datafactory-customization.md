---
title: Personalización de DataFactory
TOCTitle: DataFactory customization
ms:assetid: 43cd7416-1f05-87ee-22f0-6cf0d2d1b39f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249205(v=office.15)
ms:contentKeyID: 48544511
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a5fc1c284ee7aae77c4fb067ad57d50200119594
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700027"
---
# <a name="datafactory-customization"></a><span data-ttu-id="756c5-102">Personalización de DataFactory</span><span class="sxs-lookup"><span data-stu-id="756c5-102">DataFactory customization</span></span>


<span data-ttu-id="756c5-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="756c5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="756c5-p101">El servicio de datos remoto (RDS) permite obtener fácilmente acceso a datos en un sistema de cliente-servidor de tres niveles. Un control de datos de cliente especifica los parámetros de las cadenas de conexión y de comandos para consultar un origen de datos remoto, o bien, los parámetros del objeto [Recordset](recordset-object-ado.md) y de la cadena de conexión para llevar a cabo una actualización.</span><span class="sxs-lookup"><span data-stu-id="756c5-p101">Remote Data Service (RDS) provides a way to easily perform data access in a three-tier client/server system. A client data control specifies connection and command string parameters to perform a query on a remote data source, or connection string and [Recordset](recordset-object-ado.md) object parameters to perform an update.</span></span>

<span data-ttu-id="756c5-p102">Los parámetros se pasan a un programa de servidor, que realiza la operación de acceso a datos en el origen de datos remoto. RDS proporciona un programa de servidor predeterminado denominado objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md). El objeto **RDSServer.DataFactory** devuelve cualquier objeto **Recordset** generado por una consulta al cliente.</span><span class="sxs-lookup"><span data-stu-id="756c5-p102">The parameters are passed to a server program, which performs the data-access operation on the remote data source. RDS provides a default server program called the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object. The **RDSServer.DataFactory** object returns any **Recordset** object produced by a query to the client.</span></span>

<span data-ttu-id="756c5-p103">Sin embargo, **RDSServer.DataFactory** se limita a realizar consultas y actualizaciones. No puede realizar validaciones ni procesamientos en las cadenas de conexión o de comandos.</span><span class="sxs-lookup"><span data-stu-id="756c5-p103">However, the **RDSServer.DataFactory** is limited to performing queries and updates. It cannot perform any validation or processing on the connection or command strings.</span></span>

<span data-ttu-id="756c5-p104">Con ADO, se puede especificar que **DataFactory** trabaje conjuntamente con otro tipo de programa de servidor denominado \* controlador\*. El controlador puede modificar las cadenas de conexión y de comandos del cliente antes de que se utilicen para obtener acceso al origen de datos. Además, el controlador puede exigir derechos de acceso, que rigen la capacidad del cliente para leer y escribir datos en el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="756c5-p104">With ADO, you can specify that the **DataFactory** work in conjunction with another type of server program called a *handler*. The handler can modify client connection and command strings before they are used to access the data source. In addition, the handler can enforce access rights, which govern the ability of the client to read and write data to the data source.</span></span>

<span data-ttu-id="756c5-114">Los parámetros que utiliza el controlador para modificar los derechos de acceso y parámetros de cliente se especifican en las secciones de un archivo de personalización.</span><span class="sxs-lookup"><span data-stu-id="756c5-114">The parameters the handler uses to modify client parameters and access rights are specified in sections of a customization file.</span></span>

<span data-ttu-id="756c5-115">Vea los temas siguientes para obtener más información sobre la personalización del objeto **DataFactory**:</span><span class="sxs-lookup"><span data-stu-id="756c5-115">See the following topics for more information about customizing the **DataFactory** object:</span></span>

- [<span data-ttu-id="756c5-116">Introducción al archivo de personalización</span><span class="sxs-lookup"><span data-stu-id="756c5-116">Understanding the Customization File</span></span>](understanding-the-customization-file.md)
- [<span data-ttu-id="756c5-117">Sección Connect del archivo de personalización</span><span class="sxs-lookup"><span data-stu-id="756c5-117">Customization File Connect section</span></span>](customization-file-connect-section.md)
- [<span data-ttu-id="756c5-118">Sección de SQL del archivo de personalización</span><span class="sxs-lookup"><span data-stu-id="756c5-118">Customization File SQL section</span></span>](customization-file-sql-section.md)
- [<span data-ttu-id="756c5-119">Sección de UserList del archivo de personalización</span><span class="sxs-lookup"><span data-stu-id="756c5-119">Customization File UserList section</span></span>](customization-file-userlist-section.md)
- [<span data-ttu-id="756c5-120">Sección de registros de archivo de personalización</span><span class="sxs-lookup"><span data-stu-id="756c5-120">Customization File Logs section</span></span>](customization-file-logs-section.md)
- [<span data-ttu-id="756c5-121">Configuración de cliente requerida</span><span class="sxs-lookup"><span data-stu-id="756c5-121">Required client settings</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/required-client-settings)
- [<span data-ttu-id="756c5-122">Escribir un controlador personalizado</span><span class="sxs-lookup"><span data-stu-id="756c5-122">Writing your own customized handler</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/writing-your-own-customized-handler)
