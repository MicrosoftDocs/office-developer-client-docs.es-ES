---
title: Modelo de programación básico de RDS
TOCTitle: Basic RDS Programming Model
ms:assetid: a8dd22b0-ac9b-b5c3-4e31-d2990d36230a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249781(v=office.15)
ms:contentKeyID: 48546911
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2a90423f6bd05ae3d721faf97291ea6d21aa4393
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485244"
---
# <a name="basic-rds-programming-model"></a><span data-ttu-id="8eb8f-102">Modelo de programación básico de RDS</span><span class="sxs-lookup"><span data-stu-id="8eb8f-102">Basic RDS Programming Model</span></span>


<span data-ttu-id="8eb8f-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8eb8f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8eb8f-p101">RDS se orienta a las aplicaciones que existen en el entorno siguiente: una aplicación de cliente especifica un programa que se ejecutará en un servidor y los parámetros necesarios para que se devuelva la información deseada. El programa invocado en el servidor obtiene acceso al origen de datos especificado, recupera la información, procesa los datos opcionalmente y devuelve la información resultante a la aplicación de cliente de modo que pueda utilizarse fácilmente. RDS permite llevar a cabo la siguiente secuencia de acciones:</span><span class="sxs-lookup"><span data-stu-id="8eb8f-p101">RDS addresses applications that exist in the following environment: A client application specifies a program that will execute on a server and the parameters required to return the desired information. The program invoked on the server gains access to the specified data source, retrieves the information, optionally processes the data, and then returns the resulting information to your client application in a form that it can easily use. RDS provides the means for you to perform the following sequence of actions:</span></span>

  - <span data-ttu-id="8eb8f-p102">Especifique el programa que se va a invocar en el servidor y haga referencia al mismo desde el cliente. (Esta referencia se denomina a veces un servidor \* proxy\*. Representa el programa de servidor remoto. La aplicación de cliente "llamará" al proxy como si fuese un programa local pero, en realidad, invoca el programa de servidor remoto.)</span><span class="sxs-lookup"><span data-stu-id="8eb8f-p102">Specify the program to be invoked on the server, and obtain a way to refer to it from the client. (This reference is sometimes called a *proxy*. It represents the remote server program. The client application will "call" the proxy as if it were a local program, but it actually invokes the remote server program.)</span></span>

  - <span data-ttu-id="8eb8f-p103">Invoque el programa de servidor. Pase al programa de servidor los parámetros que identifiquen el origen de datos y el comando que se va a emitir. (En realidad, el programa de servidor utiliza ADO para obtener acceso al origen de datos. ADO establece una conexión con uno de los parámetros especificados y, después, emite el comando especificado en el otro parámetro.)</span><span class="sxs-lookup"><span data-stu-id="8eb8f-p103">Invoke the server program. Pass parameters to the server program that identify the data source and the command to issue. (The server program actually uses ADO to gain access to the data source. ADO makes a connection with one of the given parameters, and then issues the command specified in the other parameter.)</span></span>

  - <span data-ttu-id="8eb8f-p104">El programa de servidor obtiene un objeto [Recordset](recordset-object-ado.md) desde el origen de datos. El objeto **Recordset** se procesa opcionalmente en el servidor.</span><span class="sxs-lookup"><span data-stu-id="8eb8f-p104">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source. Optionally, the **Recordset** object is processed on the server.</span></span>

  - <span data-ttu-id="8eb8f-117">El programa de servidor devuelve el objeto **Recordset** final a la aplicación de cliente.</span><span class="sxs-lookup"><span data-stu-id="8eb8f-117">The server program returns the final **Recordset** object to the client application.</span></span>

  - <span data-ttu-id="8eb8f-118">En el cliente, el objeto **Recordset** se coloca de manera que los controles visuales lo puedan utilizar fácilmente.</span><span class="sxs-lookup"><span data-stu-id="8eb8f-118">On the client, the **Recordset** object is put into a form that can be easily used by visual controls.</span></span>

  - <span data-ttu-id="8eb8f-119">Cualquier modificación que se realice en el objeto \*\* Recordset\*\* se envía de nuevo al programa de servidor, que las usa para actualizar el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="8eb8f-119">Any modifications to the **Recordset** object are sent back to the server program, which uses them to update the data source.</span></span>

<span data-ttu-id="8eb8f-p105">Este modelo de programación contiene algunas características prácticas. Si no necesita un programa de servidor complejo para obtener acceso al origen de datos y si proporciona los parámetros de conexión y comando necesarios, RDS recuperará automáticamente los datos especificados con un sencillo programa de servidor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8eb8f-p105">This programming model contains certain convenience features. If you do not need a complex server program to access the data source, and if you provide the required connection and command parameters, RDS will automatically retrieve the specified data with a simple, default server program.</span></span>

<span data-ttu-id="8eb8f-p106">Si necesita un procesamiento más complejo, puede especificar su propio programa de servidor personalizado. Por ejemplo, dado que un programa de servidor personalizado tiene a su disposición todas las funciones de ADO, podrá conectarse a varios orígenes de datos, combinar sus datos de alguna manera compleja y, a continuación, devolver un resultado simple procesado a la aplicación de cliente.</span><span class="sxs-lookup"><span data-stu-id="8eb8f-p106">If you need more complex processing, you can specify your own custom server program. For example, because a custom server program has the full power of ADO at its disposal, it could connect to several different data sources, combine their data in some complex way, and then return a simple, processed result to the client application.</span></span>

<span data-ttu-id="8eb8f-124">Finalmente, si sus necesidades son intermedias, ADO admite ahora la personalización del comportamiento del programa de servidor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8eb8f-124">Finally, if your needs are somewhere in between, ADO now supports customizing the behavior of the default server program.</span></span>

