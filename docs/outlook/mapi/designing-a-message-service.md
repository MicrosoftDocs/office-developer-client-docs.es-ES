---
title: Diseño de un servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32627ebb-547f-4fac-a406-e7243ec5521b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 04aa4348560396c8237811252fd96a2b461cd791
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816653"
---
# <a name="designing-a-message-service"></a><span data-ttu-id="7bb51-103">Diseño de un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="7bb51-103">Designing a message service</span></span>

<span data-ttu-id="7bb51-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7bb51-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7bb51-105">Antes de comenzar a escribir código para admitir el servicio de mensajes, es importante crear un diseño.</span><span class="sxs-lookup"><span data-stu-id="7bb51-105">Before you begin to write code to support your message service, it is important to create a design.</span></span> <span data-ttu-id="7bb51-106">Resolver los problemas siguientes en el proceso de diseño:</span><span class="sxs-lookup"><span data-stu-id="7bb51-106">Resolve the following issues in your design process:</span></span>
  
1. <span data-ttu-id="7bb51-107">Determinar cuántos proveedores de servicios deben incluirse en el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7bb51-107">Determine how many service providers should be included in the message service.</span></span> <span data-ttu-id="7bb51-108">Incluir sólo los proveedores de servicios relacionados (es decir, los proveedores que funcionan con el mismo sistema de mensajería) en su servicio.</span><span class="sxs-lookup"><span data-stu-id="7bb51-108">Include only related service providers (that is, providers that work with the same messaging system) in your service.</span></span> <span data-ttu-id="7bb51-109">Proveedores de servicios no relacionados no pertenecen en el mismo servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7bb51-109">Unrelated service providers do not belong in the same message service.</span></span> <span data-ttu-id="7bb51-110">Utilice el perfil de la integración de proveedores de servicios no relacionados y servicios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7bb51-110">Use the profile for integrating unrelated service providers and message services.</span></span>
    
2. <span data-ttu-id="7bb51-111">Determinar qué tipo de proveedores de servicios debe incluirse en el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7bb51-111">Determine what type of service providers should be included in the message service.</span></span> <span data-ttu-id="7bb51-112">La mayoría de los servicios de mensaje incluye un proveedor de cada uno de los tipos comunes.</span><span class="sxs-lookup"><span data-stu-id="7bb51-112">Most messge services include one provider of each of the common types.</span></span> <span data-ttu-id="7bb51-113">Es decir, el servicio de mensajes típico tiene proveedor de libretas de direcciones, proveedor de almacenamiento de un mensaje y proveedor de uno transporte.</span><span class="sxs-lookup"><span data-stu-id="7bb51-113">That is, the typical message service has one address book provider, one message store provider, and one transport provider.</span></span>
    
3. <span data-ttu-id="7bb51-114">Determinar cuántos archivos DLL debe contener el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7bb51-114">Determine how many DLLs should contain the message service.</span></span> <span data-ttu-id="7bb51-115">El número de archivos DLL que usa un servicio de mensajes depende de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7bb51-115">The number of DLLs that a message service uses depends on the following:</span></span>
    
   - <span data-ttu-id="7bb51-116">El grado de complejidad que usted, como el escritor del servicio de mensajes está dispuestos a controlar.</span><span class="sxs-lookup"><span data-stu-id="7bb51-116">The degree of complexity that you as the writer of the message service are willing to handle.</span></span>
    
   - <span data-ttu-id="7bb51-117">El tipo de proveedores de servicios en el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7bb51-117">The type of service providers in the message service.</span></span>
    
   - <span data-ttu-id="7bb51-118">La relación que podría tener el servicio de mensajes con otro servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7bb51-118">The relationship that the message service might have with another message service.</span></span>
    
   <span data-ttu-id="7bb51-119">Debido a que MAPI almacena sólo un punto de entrada para cada tipo de proveedor, no incluya varios proveedores del mismo tipo en un solo archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="7bb51-119">Because MAPI stores only one entry point for each provider type, do not include multiple providers of the same type in a single DLL.</span></span> <span data-ttu-id="7bb51-120">Si tiene sentido para incluir varios proveedores de un tipo, puede implementarlos en archivos DLL independientes o hacer que comparten una función de punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="7bb51-120">If it makes sense to include multiple providers of one type, either implement them in separate DLLs or have them share an entry point function.</span></span> <span data-ttu-id="7bb51-121">Otra opción consiste en implementar servicios de mensajes relacionados o servicios de mensajes que se pueden utilizar la misma instalación y código de configuración y el misma archivo DLL punto de entrada (función), en un archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="7bb51-121">Another option is to implement related message services, or message services that are able to use the same installation and configuration code and the same DLL entry point function, in one DLL.</span></span>
    
   <span data-ttu-id="7bb51-122">Si es posible, mantener simple y usar una DLL que contiene la implementación de todos los proveedores de servicio en el servicio de mensajes y todo el código para instalar y configurar el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7bb51-122">If possible, keep it simple and use one DLL that contains the implementation of all the service providers in the message service and all the code to install and configure the message service.</span></span> <span data-ttu-id="7bb51-123">Si esto no es posible, se puede implementar una DLL para el código de instalación y configuración y ya sea un solo archivo DLL para todos los proveedores de servicios o un archivo DLL para cada proveedor.</span><span class="sxs-lookup"><span data-stu-id="7bb51-123">If this is not possible, you can implement one DLL for the installation and configuration code and either a single DLL for all of the service providers or one DLL for each provider.</span></span>
    
4. <span data-ttu-id="7bb51-124">Determinar un nombre para el servicio de mensajes DLL o archivos DLL.</span><span class="sxs-lookup"><span data-stu-id="7bb51-124">Determine a name for the message service DLL or DLLs.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="7bb51-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="7bb51-125">See also</span></span>

- [<span data-ttu-id="7bb51-126">Implementación de servicios de mensajería</span><span class="sxs-lookup"><span data-stu-id="7bb51-126">Message Service Implementation</span></span>](message-service-implementation.md)

