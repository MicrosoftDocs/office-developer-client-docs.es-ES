---
title: Modelo de programación de BDC básico
TOCTitle: Basic RDS programming model
ms:assetid: a8dd22b0-ac9b-b5c3-4e31-d2990d36230a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249781(v=office.15)
ms:contentKeyID: 48546911
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 947a6355d07ba2e9fb9b2a9b76c4c1941d83e668
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296888"
---
# <a name="basic-rds-programming-model"></a><span data-ttu-id="9b618-102">Modelo de programación de BDC básico</span><span class="sxs-lookup"><span data-stu-id="9b618-102">Basic RDS programming model</span></span>

<span data-ttu-id="9b618-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9b618-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9b618-p101">RDS se orienta a las aplicaciones que existen en el entorno siguiente: una aplicación de cliente especifica un programa que se ejecutará en un servidor y los parámetros necesarios para que se devuelva la información deseada. El programa invocado en el servidor obtiene acceso al origen de datos especificado, recupera la información, procesa los datos opcionalmente y devuelve la información resultante a la aplicación de cliente de modo que pueda utilizarse fácilmente. RDS permite llevar a cabo la siguiente secuencia de acciones:</span><span class="sxs-lookup"><span data-stu-id="9b618-p101">RDS addresses applications that exist in the following environment: A client application specifies a program that will execute on a server and the parameters required to return the desired information. The program invoked on the server gains access to the specified data source, retrieves the information, optionally processes the data, and then returns the resulting information to your client application in a form that it can easily use. RDS provides the means for you to perform the following sequence of actions:</span></span>

- <span data-ttu-id="9b618-p102">Especifique el programa que se va a invocar en el servidor y haga referencia al mismo desde el cliente. (Esta referencia se denomina a veces un servidor *proxy*. Representa el programa de servidor remoto. La aplicación de cliente "llamará" al proxy como si fuese un programa local pero, en realidad, invoca el programa de servidor remoto.)</span><span class="sxs-lookup"><span data-stu-id="9b618-p102">Specify the program to be invoked on the server, and obtain a way to refer to it from the client. (This reference is sometimes called a *proxy*. It represents the remote server program. The client application will "call" the proxy as if it were a local program, but it actually invokes the remote server program.)</span></span>

- <span data-ttu-id="9b618-p103">Invoque el programa de servidor. Pase al programa de servidor los parámetros que identifiquen el origen de datos y el comando que se va a emitir. (En realidad, el programa de servidor utiliza ADO para obtener acceso al origen de datos. ADO establece una conexión con uno de los parámetros especificados y, después, emite el comando especificado en el otro parámetro.)</span><span class="sxs-lookup"><span data-stu-id="9b618-p103">Invoke the server program. Pass parameters to the server program that identify the data source and the command to issue. (The server program actually uses ADO to gain access to the data source. ADO makes a connection with one of the given parameters, and then issues the command specified in the other parameter.)</span></span>

- <span data-ttu-id="9b618-p104">El programa de servidor obtiene un objeto [Recordset](recordset-object-ado.md) desde el origen de datos. El objeto **Recordset** se procesa opcionalmente en el servidor.</span><span class="sxs-lookup"><span data-stu-id="9b618-p104">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source. Optionally, the **Recordset** object is processed on the server.</span></span>

- <span data-ttu-id="9b618-117">El programa de servidor devuelve el objeto **Recordset** final a la aplicación de cliente.</span><span class="sxs-lookup"><span data-stu-id="9b618-117">The server program returns the final **Recordset** object to the client application.</span></span>

- <span data-ttu-id="9b618-118">En el cliente, el objeto **Recordset** se coloca de manera que los controles visuales lo puedan utilizar fácilmente.</span><span class="sxs-lookup"><span data-stu-id="9b618-118">On the client, the **Recordset** object is put into a form that can be easily used by visual controls.</span></span>

- <span data-ttu-id="9b618-119">Any modifications to the **Recordset** object are sent back to the server program, which uses them to update the data source.</span><span class="sxs-lookup"><span data-stu-id="9b618-119">Any modifications to the **Recordset** object are sent back to the server program, which uses them to update the data source.</span></span>

<span data-ttu-id="9b618-p105">Este modelo de programación contiene algunas características prácticas. Si no necesita un programa de servidor complejo para obtener acceso al origen de datos y si proporciona los parámetros de conexión y comando necesarios, RDS recuperará automáticamente los datos especificados con un sencillo programa de servidor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9b618-p105">This programming model contains certain convenience features. If you do not need a complex server program to access the data source, and if you provide the required connection and command parameters, RDS will automatically retrieve the specified data with a simple, default server program.</span></span>

<span data-ttu-id="9b618-p106">Si necesita un procesamiento más complejo, puede especificar su propio programa de servidor personalizado. Por ejemplo, dado que un programa de servidor personalizado tiene a su disposición todas las funciones de ADO, podrá conectarse a varios orígenes de datos, combinar sus datos de alguna manera compleja y, a continuación, devolver un resultado simple procesado a la aplicación de cliente.</span><span class="sxs-lookup"><span data-stu-id="9b618-p106">If you need more complex processing, you can specify your own custom server program. For example, because a custom server program has the full power of ADO at its disposal, it could connect to several different data sources, combine their data in some complex way, and then return a simple, processed result to the client application.</span></span>

<span data-ttu-id="9b618-124">Finalmente, si sus necesidades son intermedias, ADO admite ahora la personalización del comportamiento del programa de servidor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9b618-124">Finally, if your needs are somewhere in between, ADO now supports customizing the behavior of the default server program.</span></span>

