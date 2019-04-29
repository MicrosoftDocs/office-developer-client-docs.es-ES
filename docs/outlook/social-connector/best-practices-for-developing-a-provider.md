---
title: Procedimientos recomendados para el desarrollo de un proveedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: 'Debe cumplir con los siguientes procedimientos al desarrollar un proveedor de Outlook Social Connector 2013 (OSC):'
ms.openlocfilehash: 6a48a56d8065fb9a176ca6527340c99551cdb52a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425921"
---
# <a name="best-practices-for-developing-a-provider"></a><span data-ttu-id="7c79c-103">Procedimientos recomendados para el desarrollo de un proveedor</span><span class="sxs-lookup"><span data-stu-id="7c79c-103">Best practices for developing a provider</span></span>

<span data-ttu-id="7c79c-104">Debe cumplir con los siguientes procedimientos al desarrollar un proveedor de Outlook Social Connector 2013 (OSC):</span><span class="sxs-lookup"><span data-stu-id="7c79c-104">You should adhere to the following practices when you develop an Outlook Social Connector 2013 (OSC) provider:</span></span>
  
- <span data-ttu-id="7c79c-105">Por motivos de seguridad, los proveedores que se comunican con los servidores a través de Internet deben usar el protocolo HTTPS (Protocolo de transferencia de hiperTexto (HTTP) con capa de sockets seguros (SSL)).</span><span class="sxs-lookup"><span data-stu-id="7c79c-105">For security reasons, providers that communicate with servers over the Internet should use the HTTPS (Hypertext Transfer Protocol (HTTP) with Secure Socket Layer (SSL)) protocol.</span></span> <span data-ttu-id="7c79c-106">De lo contrario, existe el riesgo de que las direcciones de correo electrónico, las actividades de red social y otros datos de usuario se puedan interceptar o exponer durante el tránsito.</span><span class="sxs-lookup"><span data-stu-id="7c79c-106">Otherwise, there is a risk that email addresses, social network activities, and other user data could be intercepted or exposed while in transit.</span></span>
    
- <span data-ttu-id="7c79c-107">Si está desarrollando un proveedor OSC para una red social de terceros, el proveedor debe adherirse a los términos de servicio de la red social.</span><span class="sxs-lookup"><span data-stu-id="7c79c-107">If you are developing an OSC provider for a third-party social network, your provider must adhere to the social network's terms of service.</span></span>
    
- <span data-ttu-id="7c79c-108">Para minimizar el tamaño del paquete de descarga del proveedor, genere el proveedor mediante un compilador nativo como C++ o cualquier otra herramienta que pueda compilar un componente COM.</span><span class="sxs-lookup"><span data-stu-id="7c79c-108">To minimize the size of the provider download package, build the provider by using a native compiler such as C++ or any other tool that can build a COM component.</span></span>
    
- <span data-ttu-id="7c79c-109">En su proveedor, cree un agente de usuario único que se envíe a la red social para realizar un seguimiento de las llamadas realizadas por el proveedor a la red social.</span><span class="sxs-lookup"><span data-stu-id="7c79c-109">In your provider, create a unique user agent that is sent to the social network to track calls made by the provider to the social network.</span></span>
    
- <span data-ttu-id="7c79c-110">El método [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) no debe confiar en llamar a la red social a través de Internet para obtener las funciones del proveedor.</span><span class="sxs-lookup"><span data-stu-id="7c79c-110">The [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method should not rely on calling the social network over the Internet to get the capabilities of the provider.</span></span> <span data-ttu-id="7c79c-111">Por ejemplo, los usuarios pueden iniciar Outlook sin conexión; Si el OSC llama a **GetCapabilities** y no hay ninguna conexión de red, la llamada **GetCapabilities** no devolverá XML de **capacidades** válidas.</span><span class="sxs-lookup"><span data-stu-id="7c79c-111">For example, users can start Outlook offline; if the OSC calls **GetCapabilities** and there is no network connection, the **GetCapabilities** call will not return valid **capabilities** XML.</span></span> <span data-ttu-id="7c79c-112">El procedimiento recomendado es almacenar el XML de **capacidades** como un recurso en el proveedor.</span><span class="sxs-lookup"><span data-stu-id="7c79c-112">The best practice is to store **capabilities** XML as a resource in your provider.</span></span> 
    
- <span data-ttu-id="7c79c-113">El proveedor de OSC puede generar un volumen significativo de llamadas a una red social.</span><span class="sxs-lookup"><span data-stu-id="7c79c-113">Your OSC provider can generate a significant volume of calls to a social network.</span></span> <span data-ttu-id="7c79c-114">En función de las condiciones del servicio de su red social, considere la posibilidad de almacenar en caché amigos en una carpeta de Outlook para reducir el número de llamadas desde el OSC a su proveedor y, a su vez, de su proveedor a la red social.</span><span class="sxs-lookup"><span data-stu-id="7c79c-114">Depending on the terms of service for your social network, consider caching friends to an Outlook folder to reduce the number of calls from the OSC to your provider and, in turn, from your provider to the social network.</span></span>
    
- <span data-ttu-id="7c79c-115">Office 2013 está disponible en las versiones de 32 y de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7c79c-115">Office 2013 is available in both 32-bit and 64-bit versions.</span></span> <span data-ttu-id="7c79c-116">Las versiones de Office anteriores a Office 2010 solo están disponibles en una versión de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7c79c-116">Versions of Office prior to Office 2010 are available only in a 32-bit version.</span></span> <span data-ttu-id="7c79c-117">La instalación predeterminada de Office 2013 en Windows de 64 bits es 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7c79c-117">The default installation of Office 2013 on 64-bit Windows is 32-bit.</span></span> <span data-ttu-id="7c79c-118">Si desea admitir la versión de 64 bits del OSC que se instala con Office 2013 de 64 bits, también debe liberar una versión de 64 bits de su proveedor.</span><span class="sxs-lookup"><span data-stu-id="7c79c-118">If you intend to support the 64-bit version of the OSC that is installed with 64-bit Office 2013, you must also release a 64-bit version of your provider.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="7c79c-119">Ver también</span><span class="sxs-lookup"><span data-stu-id="7c79c-119">See also</span></span>

- [<span data-ttu-id="7c79c-120">Secuencias de llamada típicas de OSC</span><span class="sxs-lookup"><span data-stu-id="7c79c-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="7c79c-121">Desarrollo de un proveedor con el esquema XML de OSC</span><span class="sxs-lookup"><span data-stu-id="7c79c-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="7c79c-122">Implementación de un proveedor</span><span class="sxs-lookup"><span data-stu-id="7c79c-122">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="7c79c-123">Introducción al desarrollo de un proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="7c79c-123">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

