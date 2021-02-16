---
title: Diseñar un servicio de mensajería
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32627ebb-547f-4fac-a406-e7243ec5521b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 19a8a939685c440901f3f57d72baf673a579e590
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404298"
---
# <a name="designing-a-message-service"></a><span data-ttu-id="96778-103">Diseñar un servicio de mensajería</span><span class="sxs-lookup"><span data-stu-id="96778-103">Designing a message service</span></span>

<span data-ttu-id="96778-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96778-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96778-105">Antes de empezar a escribir código para admitir el servicio de mensajes, es importante crear un diseño.</span><span class="sxs-lookup"><span data-stu-id="96778-105">Before you begin to write code to support your message service, it is important to create a design.</span></span> <span data-ttu-id="96778-106">Resuelva los siguientes problemas en el proceso de diseño:</span><span class="sxs-lookup"><span data-stu-id="96778-106">Resolve the following issues in your design process:</span></span>
  
1. <span data-ttu-id="96778-107">Determine cuántos proveedores de servicios deben incluirse en el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="96778-107">Determine how many service providers should be included in the message service.</span></span> <span data-ttu-id="96778-108">Incluya solo los proveedores de servicios relacionados (es decir, los proveedores que trabajan con el mismo sistema de mensajería) en su servicio.</span><span class="sxs-lookup"><span data-stu-id="96778-108">Include only related service providers (that is, providers that work with the same messaging system) in your service.</span></span> <span data-ttu-id="96778-109">Los proveedores de servicios no relacionados no pertenecen al mismo servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="96778-109">Unrelated service providers do not belong in the same message service.</span></span> <span data-ttu-id="96778-110">Use el perfil para integrar proveedores de servicios no relacionados y servicios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="96778-110">Use the profile for integrating unrelated service providers and message services.</span></span>
    
2. <span data-ttu-id="96778-111">Determine qué tipo de proveedores de servicios se deben incluir en el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="96778-111">Determine what type of service providers should be included in the message service.</span></span> <span data-ttu-id="96778-112">La mayoría de los servicios de desorden incluyen un proveedor de cada uno de los tipos comunes.</span><span class="sxs-lookup"><span data-stu-id="96778-112">Most messge services include one provider of each of the common types.</span></span> <span data-ttu-id="96778-113">Es decir, el servicio de mensajes típico tiene un proveedor de libreta de direcciones, un proveedor de almacenamiento de mensajes y un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="96778-113">That is, the typical message service has one address book provider, one message store provider, and one transport provider.</span></span>
    
3. <span data-ttu-id="96778-114">Determine cuántos archivos DLL deben contener el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="96778-114">Determine how many DLLs should contain the message service.</span></span> <span data-ttu-id="96778-115">El número de DLL que usa un servicio de mensajes depende de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="96778-115">The number of DLLs that a message service uses depends on the following:</span></span>
    
   - <span data-ttu-id="96778-116">El grado de complejidad que usted, como escritor del servicio de mensajes, está dispuesto a controlar.</span><span class="sxs-lookup"><span data-stu-id="96778-116">The degree of complexity that you as the writer of the message service are willing to handle.</span></span>
    
   - <span data-ttu-id="96778-117">El tipo de proveedores de servicios en el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="96778-117">The type of service providers in the message service.</span></span>
    
   - <span data-ttu-id="96778-118">Relación que el servicio de mensajes puede tener con otro servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="96778-118">The relationship that the message service might have with another message service.</span></span>
    
   <span data-ttu-id="96778-119">Dado que MAPI almacena solo un punto de entrada para cada tipo de proveedor, no incluya varios proveedores del mismo tipo en una sola DLL.</span><span class="sxs-lookup"><span data-stu-id="96778-119">Because MAPI stores only one entry point for each provider type, do not include multiple providers of the same type in a single DLL.</span></span> <span data-ttu-id="96778-120">Si tiene sentido incluir varios proveedores de un tipo, puede implementarlos en DLL independientes o hacer que compartan una función de punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="96778-120">If it makes sense to include multiple providers of one type, either implement them in separate DLLs or have them share an entry point function.</span></span> <span data-ttu-id="96778-121">Otra opción es implementar servicios de mensajes relacionados o servicios de mensajes que puedan usar el mismo código de instalación y configuración y la misma función de punto de entrada dll, en una DLL.</span><span class="sxs-lookup"><span data-stu-id="96778-121">Another option is to implement related message services, or message services that are able to use the same installation and configuration code and the same DLL entry point function, in one DLL.</span></span>
    
   <span data-ttu-id="96778-122">Si es posible, siga estando sencillo y use una DLL que contenga la implementación de todos los proveedores de servicios en el servicio de mensajes y todo el código para instalar y configurar el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="96778-122">If possible, keep it simple and use one DLL that contains the implementation of all the service providers in the message service and all the code to install and configure the message service.</span></span> <span data-ttu-id="96778-123">Si esto no es posible, puede implementar una DLL para el código de instalación y configuración y una sola DLL para todos los proveedores de servicios o una DLL para cada proveedor.</span><span class="sxs-lookup"><span data-stu-id="96778-123">If this is not possible, you can implement one DLL for the installation and configuration code and either a single DLL for all of the service providers or one DLL for each provider.</span></span>
    
4. <span data-ttu-id="96778-124">Determine un nombre para la DLL o dll del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="96778-124">Determine a name for the message service DLL or DLLs.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="96778-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="96778-125">See also</span></span>

- [<span data-ttu-id="96778-126">Implementación del servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="96778-126">Message Service Implementation</span></span>](message-service-implementation.md)

