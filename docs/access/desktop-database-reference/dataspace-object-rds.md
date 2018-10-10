---
title: DataSpace (objeto) (RDS)
TOCTitle: DataSpace Object (RDS)
ms:assetid: 7db181d5-422b-49fe-b6af-a20f5da520ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249527(v=office.15)
ms:contentKeyID: 48545862
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2466727f52a37d396e7478fa54d27a68158855a4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483736"
---
# <a name="dataspace-object-rds"></a><span data-ttu-id="4a925-102">DataSpace (objeto) (RDS)</span><span class="sxs-lookup"><span data-stu-id="4a925-102">DataSpace Object (RDS)</span></span>

<span data-ttu-id="4a925-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a925-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4a925-104">Crea proxies de cliente a objetos de negocio personalizados ubicados en el nivel medio.</span><span class="sxs-lookup"><span data-stu-id="4a925-104">Creates client-side proxies to custom business objects located on the middle tier.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a925-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4a925-105">Remarks</span></span>

<span data-ttu-id="4a925-p101">El servicio de datos remotos necesita servidores proxy de objetos de negocio para que un componente de cliente pueda establecer comunicación con objetos de negocio ubicados en el nivel medio. Los servidores proxy facilitan el empaquetado, desempaquetado y transporte (cálculo de referencias) de los datos [Recordset](recordset-object-ado.md) de la aplicación mediante límites de procesos o de equipo.</span><span class="sxs-lookup"><span data-stu-id="4a925-p101">Remote Data Service needs business object proxies so that client-side component can communicate with business objects located on the middle tier. Proxies facilitate the packaging, unpackaging, and transport (marshaling) of the application's [Recordset](recordset-object-ado.md) data across process or machine boundaries.</span></span>

<span data-ttu-id="4a925-p102">El servicio de datos remotos utiliza el método **CreateObject** del objeto [RDS.DataSpace](createobject-method-rds.md) para crear servidores proxy de objetos de negocio. El proxy de objetos de negocio se crea dinámicamente cada vez que se crea una instancia de su equivalente objeto de negocio de nivel medio. Además, admite los protocolos siguientes: HTTP, HTTPS (HTTP Secure Sockets), DCOM y en proceso (los componentes de cliente y el objeto de negocio residen en el mismo equipo).</span><span class="sxs-lookup"><span data-stu-id="4a925-p102">Remote Data Service uses the **RDS.DataSpace** object's [CreateObject](createobject-method-rds.md) method to create business object proxies. The business object proxy is dynamically created whenever an instance of its middle-tier business object counterpart is created. Remote Data Service supports the following protocols: HTTP, HTTPS (HTTP Secure Sockets), DCOM, and in-process (client components and the business object reside on the same computer).</span></span>

> [!NOTE]
> <span data-ttu-id="4a925-p103">[!NOTA] El servicio de datos remotos (RDS) se comporta de forma "independiente" cuando el objeto **RDS.DataSpace** utiliza los protocolos HTTP o HTTPS. Es decir, se descarta la información interna sobre una solicitud de cliente después de que el servidor devuelva una respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a925-p103">RDS behaves in a "stateless" manner when the **RDS.DataSpace** object uses the HTTP or HTTPS protocols. That is, any internal information about a client request is discarded after the server returns a response.</span></span>

<span data-ttu-id="4a925-p104">Aunque parezca que el objeto de negocio existe durante la vida útil del proxy de objetos de negocio, sólo existe realmente hasta que se envía una respuesta a una solicitud. Cuando se emite una solicitud (es decir, se llama a un método en el objeto de negocio), el proxy abre una nueva conexión con el servidor y el servidor crea una nueva instancia del objeto de negocio. Una vez que el objeto de negocio responde a la solicitud, el servidor lo destruye y cierra la conexión.</span><span class="sxs-lookup"><span data-stu-id="4a925-p104">Although the business object appears to exist for the lifetime of the business object proxy, the business object actually exists only until a response is sent to a request. When a request is issued (that is, a method is invoked on the business object), the proxy opens a new connection to the server and the server creates a new instance of the business object. After the business object responds to the request, the server destroys the business object and closes the connection.</span></span>

<span data-ttu-id="4a925-p105">Este comportamiento significa que no se pueden pasar datos de una solicitud a otra mediante el uso de una variable o una propiedad de objeto de negocio. Se debe utilizar otro mecanismo, como un archivo o un argumento de método, para conservar los datos de estado.</span><span class="sxs-lookup"><span data-stu-id="4a925-p105">This behavior means you cannot pass data from one request to another using a business object property or variable. You must employ some other mechanism, such as a file or a method argument, to persist state data.</span></span>

<span data-ttu-id="4a925-118">El identificador de clase para el objeto **RDS.DataSpace** es BD96C556-65A3-11D0-983A-00C04FC29E36.</span><span class="sxs-lookup"><span data-stu-id="4a925-118">The class ID for the **RDS.DataSpace** object is BD96C556-65A3-11D0-983A-00C04FC29E36.</span></span>

