---
title: Modelo de programación de RDS con objetos
TOCTitle: RDS programming model with objects
ms:assetid: 207150ec-8eb5-bec5-3059-db37a0e28c19
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248987(v=office.15)
ms:contentKeyID: 48543663
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 079106e1c1a6651f68d10c5b93675c9b28b473e5
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945526"
---
# <a name="rds-programming-model-with-objects"></a><span data-ttu-id="a5e28-102">Modelo de programación de RDS con objetos</span><span class="sxs-lookup"><span data-stu-id="a5e28-102">RDS programming model with objects</span></span>

<span data-ttu-id="a5e28-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a5e28-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a5e28-p101">El objetivo de RDS es obtener acceso y actualizar los orígenes de datos a través de un intermediario como IIS. El modelo de programación especifica la secuencia de las actividades necesarias para lograr este objetivo. El modelo de objetos especifica los objetos cuyos métodos y propiedades afectan al modelo de programación.</span><span class="sxs-lookup"><span data-stu-id="a5e28-p101">The goal of RDS is to gain access to and update data sources through an intermediary such as IIS. The programming model specifies the sequence of activities necessary to accomplish this goal. The object model specifies the objects whose methods and properties affect the programming model.</span></span>

<span data-ttu-id="a5e28-107">RDS proporciona el medio para realizar la siguiente secuencia de acciones:</span><span class="sxs-lookup"><span data-stu-id="a5e28-107">RDS provides the means to perform the following sequence of actions:</span></span>

- <span data-ttu-id="a5e28-108">Especifique el programa que se va a invocar en el servidor y obtenga una forma (proxy) de hacer referencia al mismo desde el cliente ([RDS.DataSpace](dataspace-object-rds.md)).</span><span class="sxs-lookup"><span data-stu-id="a5e28-108">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client ([RDS.DataSpace](dataspace-object-rds.md)).</span></span>

- <span data-ttu-id="a5e28-p102">Invoque el programa de servidor. Pase al programa de servidor los parámetros que identifiquen el origen de datos y el comando que se va a emitir (proxy o [ RDS.DataControl ](datacontrol-object-rds.md)).</span><span class="sxs-lookup"><span data-stu-id="a5e28-p102">Invoke the server program. Pass parameters to the server program that identifies the data source and the command to issue (proxy or [RDS.DataControl](datacontrol-object-rds.md)).</span></span>

- <span data-ttu-id="a5e28-p103">El programa de servidor obtiene un objeto [Recordset](recordset-object-ado.md) desde el origen de datos, normalmente mediante ADO. De manera opcional, el objeto **Recordset** se procesa en el servidor ([RDSServer.DataFactory](datafactory-object-rdsserver.md)).</span><span class="sxs-lookup"><span data-stu-id="a5e28-p103">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source, typically by using ADO. Optionally, the **Recordset** object is processed on the server ([RDSServer.DataFactory](datafactory-object-rdsserver.md)).</span></span>

- <span data-ttu-id="a5e28-113">El programa de servidor devuelve el objeto **Recordset** final a la aplicación de cliente (proxy).</span><span class="sxs-lookup"><span data-stu-id="a5e28-113">The server program returns the final **Recordset** object to the client application (proxy).</span></span>

- <span data-ttu-id="a5e28-114">En el cliente, el objeto **Recordset** se coloca de manera que los controles visuales lo puedan utilizar fácilmente (control visual y **RDS.DataControl**).</span><span class="sxs-lookup"><span data-stu-id="a5e28-114">On the client, the **Recordset** object is put into a form that can be easily used by visual controls (visual control and **RDS.DataControl**).</span></span>

- <span data-ttu-id="a5e28-115">Los cambios realizados en el objeto **Recordset** se envían de nuevo al servidor y se utilizan para actualizar el origen de datos (**RDS.DataControl** o **RDSServer.DataFactory**).</span><span class="sxs-lookup"><span data-stu-id="a5e28-115">Changes to the **Recordset** object are sent back to the server and used to update the data source (**RDS.DataControl** or **RDSServer.DataFactory**).</span></span>

