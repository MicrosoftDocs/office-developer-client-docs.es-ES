---
title: OLE DB Provider for Internet Publishing
TOCTitle: The OLE DB Provider for Internet Publishing
ms:assetid: 864e5ece-0f50-5d88-4c40-f951b2a2eded
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249583(v=office.15)
ms:contentKeyID: 48546082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 617dca5ced5410e2023657ea1b0b748066f7843f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314059"
---
# <a name="ole-db-provider-for-internet-publishing"></a><span data-ttu-id="46631-102">Proveedor OLE DB para publicación en Internet</span><span class="sxs-lookup"><span data-stu-id="46631-102">OLE DB Provider for Internet Publishing</span></span>

<span data-ttu-id="46631-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="46631-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46631-104">Los objetos Record y [Stream](stream-object-ado.md) de [ADO](record-object-ado.md) se pueden usar con el proveedor microsoft OLE DB para internet Publishing (proveedor de publicación en Internet) para obtener acceso y manipular recursos, como carpetas web o archivos a los que sirve Microsoft FrontPage.</span><span class="sxs-lookup"><span data-stu-id="46631-104">The ADO [Record](record-object-ado.md) and [Stream](stream-object-ado.md) objects can be used with the Microsoft OLE DB Provider for Internet Publishing (Internet Publishing Provider) to access and manipulate resources, such as web folders or files served by Microsoft FrontPage.</span></span> <span data-ttu-id="46631-105">Con ADO, puede especificar que el origen de un **Record**, de un **Stream** o de un [Recordset](recordset-object-ado.md) sea una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="46631-105">With ADO, you can specify the source of a **Record**, **Stream**, or [Recordset](recordset-object-ado.md) to be a URL.</span></span> <span data-ttu-id="46631-106">Después, puede cargar, descargar, mover, copiar y eliminar recursos, o manipular directamente las propiedades de los recursos.</span><span class="sxs-lookup"><span data-stu-id="46631-106">You can then upload, download, move, copy, and delete resources, or directly manipulate resource properties.</span></span>

<span data-ttu-id="46631-107">Para obtener un ejemplo de código que utiliza **Records** y **Streams** con el Proveedor de publicación en Internet, vea el [Escenario de Internet Publishing](internet-publishing-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="46631-107">For example code using **Records** and **Streams** with the Internet Publishing Provider, see the [Internet Publishing Scenario](internet-publishing-scenario.md).</span></span>

<span data-ttu-id="46631-p102">El Proveedor de publicación en Internet se instala con Microsoft Windows 2000. También existen versiones anteriores del proveedor disponibles con Microsoft Office 2000 y Microsoft Internet Explorer 5.0.</span><span class="sxs-lookup"><span data-stu-id="46631-p102">The Internet Publishing Provider is installed with Microsoft Windows 2000. Earlier versions of the Internet Publishing Provider are also available with Microsoft Office 2000 and Microsoft Internet Explorer 5.0.</span></span>

<span data-ttu-id="46631-110">Hay tres maneras de conectar ADO con el Proveedor de publicación en Internet:</span><span class="sxs-lookup"><span data-stu-id="46631-110">There are three ways to connect ADO to the Internet Publishing Provider:</span></span>

- <span data-ttu-id="46631-p103">Especifique "URL=" en la cadena de conexión. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="46631-p103">Specify "URL=" in the connection string. For example:</span></span>
    
  ```vb 
     
    objConn.Open "URL=https://servername" 
  ```

- <span data-ttu-id="46631-113">Especifique Msdaipp.dso para la palabra clave *Provider* de la cadena de conexión.</span><span class="sxs-lookup"><span data-stu-id="46631-113">Specify Msdaipp.dso for the *Provider* keyword of the connection string.</span></span> <span data-ttu-id="46631-114">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="46631-114">For example:</span></span>
    
  ```vb 
     
    objConn.Open "provider=MSDAIPP.DSO;data source=https://servername" 
  ```

- <span data-ttu-id="46631-115">Especifique Msdaipp.dso para la propiedad [Provider](provider-property-ado.md) del objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="46631-115">Specify Msdaipp.dso for the [Provider](provider-property-ado.md) property of the [Connection](connection-object-ado.md) object.</span></span> <span data-ttu-id="46631-116">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="46631-116">For example:</span></span>
    
  ```vb 
     
    objConn.Provider = "MSDAIPP.DSO" 
    objConn.Open "https://servername" 
  ```

> [!NOTE]
> <span data-ttu-id="46631-117">Si se especifica explícitamente Msdaipp.dso como valor del proveedor, ya sea con la palabra clave *Provider* de la cadena de conexión o con la propiedad **Provider**, no podrá utilizar "URL=" en la cadena de conexión.</span><span class="sxs-lookup"><span data-stu-id="46631-117">If Msdaipp.dso is explicitly specified as the value of the provider, either with the *Provider* connection string keyword or the **Provider** property, you cannot use "URL=" in the connection string.</span></span> <span data-ttu-id="46631-118">Si lo hace, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="46631-118">If you do, an error will occur.</span></span> <span data-ttu-id="46631-119">En su lugar, simplemente especifique la dirección URL como se muestra anteriormente en este tema.</span><span class="sxs-lookup"><span data-stu-id="46631-119">Instead, simply specify the URL as shown earlier in this topic.</span></span>

<span data-ttu-id="46631-120">Para obtener información más específica acerca del proveedor de publicación en Internet, vea [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) o la documentación del proveedor proporcionada con la aplicación de origen con la que se instaló: Windows 2000, Office 2000 o Internet Explorer 5.0.</span><span class="sxs-lookup"><span data-stu-id="46631-120">For more specific information about the Internet Publishing Provider, see [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), or the provider documentation provided with the source application with which the OLE DB Provider for Internet Publishing was installed: Windows 2000, Office 2000, or Internet Explorer 5.0.</span></span>

