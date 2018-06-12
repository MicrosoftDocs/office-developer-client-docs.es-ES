---
title: Prácticas recomendadas para desarrollar un proveedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: 'Debe cumplir las siguientes prácticas al desarrollar un proveedor de Outlook Social Connector 2013 (OSC):'
ms.openlocfilehash: a6ee9d54f33bbc855d178aba844a8f65ec92f964
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821081"
---
# <a name="best-practices-for-developing-a-provider"></a><span data-ttu-id="b5e91-103">Prácticas recomendadas para desarrollar un proveedor</span><span class="sxs-lookup"><span data-stu-id="b5e91-103">Best practices for developing a provider</span></span>

<span data-ttu-id="b5e91-104">Debe cumplir las siguientes prácticas al desarrollar un proveedor de Outlook Social Connector 2013 (OSC):</span><span class="sxs-lookup"><span data-stu-id="b5e91-104">You should adhere to the following practices when you develop an Outlook Social Connector 2013 (OSC) provider:</span></span>
  
- <span data-ttu-id="b5e91-105">Por motivos de seguridad, los proveedores que se comunican con servidores a través de Internet deben usar el protocolo HTTPS (transferencia de hipertexto protocolo (HTTP) con la capa de sockets seguros (SSL)).</span><span class="sxs-lookup"><span data-stu-id="b5e91-105">For security reasons, providers that communicate with servers over the Internet should use the HTTPS (Hypertext Transfer Protocol (HTTP) with Secure Socket Layer (SSL)) protocol.</span></span> <span data-ttu-id="b5e91-106">De lo contrario, hay un riesgo de que las direcciones de correo electrónico, las actividades de redes sociales y otro usuario datos podrían ser interceptados o expuestos mientras están en tránsito.</span><span class="sxs-lookup"><span data-stu-id="b5e91-106">Otherwise, there is a risk that email addresses, social network activities, and other user data could be intercepted or exposed while in transit.</span></span>
    
- <span data-ttu-id="b5e91-107">Si está desarrollando un proveedor de OSC para una red social de otro fabricante, su proveedor debe cumplir los términos de la red social de servicio.</span><span class="sxs-lookup"><span data-stu-id="b5e91-107">If you are developing an OSC provider for a third-party social network, your provider must adhere to the social network's terms of service.</span></span>
    
- <span data-ttu-id="b5e91-108">Para reducir el tamaño del paquete de descarga del proveedor, crear el proveedor mediante un compilador como C++ o cualquier otra herramienta que puede generar un componente COM nativo.</span><span class="sxs-lookup"><span data-stu-id="b5e91-108">To minimize the size of the provider download package, build the provider by using a native compiler such as C++ or any other tool that can build a COM component.</span></span>
    
- <span data-ttu-id="b5e91-109">En su proveedor, cree a un agente de usuario único que se envía a la red social para realizar un seguimiento de las llamadas realizadas por el proveedor para la red social.</span><span class="sxs-lookup"><span data-stu-id="b5e91-109">In your provider, create a unique user agent that is sent to the social network to track calls made by the provider to the social network.</span></span>
    
- <span data-ttu-id="b5e91-110">El método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) no debe confiar en una llamada a la red social a través de Internet para obtener las capacidades del proveedor.</span><span class="sxs-lookup"><span data-stu-id="b5e91-110">The [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method should not rely on calling the social network over the Internet to get the capabilities of the provider.</span></span> <span data-ttu-id="b5e91-111">Por ejemplo, los usuarios pueden iniciar Outlook sin conexión; Si el OSC llama a **GetCapabilities** y no hay ninguna conexión de red, la llamada **GetCapabilities** no devolverá válido XML de las **capacidades** .</span><span class="sxs-lookup"><span data-stu-id="b5e91-111">For example, users can start Outlook offline; if the OSC calls **GetCapabilities** and there is no network connection, the **GetCapabilities** call will not return valid **capabilities** XML.</span></span> <span data-ttu-id="b5e91-112">El procedimiento recomendado es almacenar **capacidades** XML como un recurso en su proveedor.</span><span class="sxs-lookup"><span data-stu-id="b5e91-112">The best practice is to store **capabilities** XML as a resource in your provider.</span></span> 
    
- <span data-ttu-id="b5e91-113">Su proveedor de OSC puede generar un volumen significativo de las llamadas a una red social.</span><span class="sxs-lookup"><span data-stu-id="b5e91-113">Your OSC provider can generate a significant volume of calls to a social network.</span></span> <span data-ttu-id="b5e91-114">Según los términos del servicio para la red social, considere la posibilidad de almacenamiento en caché de amigos a una carpeta de Outlook para reducir el número de llamadas desde el OSC a su proveedor y, a su vez, desde su proveedor de la red social.</span><span class="sxs-lookup"><span data-stu-id="b5e91-114">Depending on the terms of service for your social network, consider caching friends to an Outlook folder to reduce the number of calls from the OSC to your provider and, in turn, from your provider to the social network.</span></span>
    
- <span data-ttu-id="b5e91-115">Office 2013 está disponible en versiones de 32 bits y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="b5e91-115">Office 2013 is available in both 32-bit and 64-bit versions.</span></span> <span data-ttu-id="b5e91-116">Las versiones de Office anteriores a Office 2010 sólo están disponibles en una versión de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b5e91-116">Versions of Office prior to Office 2010 are available only in a 32-bit version.</span></span> <span data-ttu-id="b5e91-117">La instalación predeterminada de Office 2013 en Windows de 64 bits es de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b5e91-117">The default installation of Office 2013 on 64-bit Windows is 32-bit.</span></span> <span data-ttu-id="b5e91-118">Si piensa admitir la versión de 64 bits de la OSC que se instala con Office 2013 de 64 bits, también debe liberar una versión de 64 bits de su proveedor.</span><span class="sxs-lookup"><span data-stu-id="b5e91-118">If you intend to support the 64-bit version of the OSC that is installed with 64-bit Office 2013, you must also release a 64-bit version of your provider.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="b5e91-119">Ver también</span><span class="sxs-lookup"><span data-stu-id="b5e91-119">See also</span></span>

- [<span data-ttu-id="b5e91-120">Secuencias de llamada típicas de OSC</span><span class="sxs-lookup"><span data-stu-id="b5e91-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="b5e91-121">Desarrollar un proveedor con el esquema XML de OSC</span><span class="sxs-lookup"><span data-stu-id="b5e91-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="b5e91-122">Implementación de un proveedor</span><span class="sxs-lookup"><span data-stu-id="b5e91-122">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="b5e91-123">Introducción al desarrollo de un proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="b5e91-123">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

