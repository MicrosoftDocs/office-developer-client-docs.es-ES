---
title: Objetos de proveedor de transporte MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3f05e5b4b45e18d580737d37250e183c4cead881
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430360"
---
# <a name="mapi-transport-provider-objects"></a><span data-ttu-id="5eab3-103">Objetos de proveedor de transporte MAPI</span><span class="sxs-lookup"><span data-stu-id="5eab3-103">MAPI transport provider objects</span></span>
  
<span data-ttu-id="5eab3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5eab3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5eab3-105">Además del proveedor estándar y los objetos de inicio de sesión implementados por todos los proveedores de servicios, los proveedores de transporte deben implementar un objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="5eab3-105">In addition to the standard provider and logon objects implemented by all service providers, transport providers are required to implement a status object.</span></span> <span data-ttu-id="5eab3-106">Para los demás tipos de proveedor de servicios, la implementación de un objeto status es opcional.</span><span class="sxs-lookup"><span data-stu-id="5eab3-106">For the other service provider types, implementing a status object is optional.</span></span> <span data-ttu-id="5eab3-107">Sin embargo, MAPI lo requiere para los proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="5eab3-107">However, MAPI requires it for transport providers.</span></span> <span data-ttu-id="5eab3-108">Los proveedores de transporte que admiten la descarga de encabezados de mensaje desde un servidor remoto también implementan una carpeta y una tabla.</span><span class="sxs-lookup"><span data-stu-id="5eab3-108">Transport providers that support the downloading of message headers from a remote server also implement a folder and a table.</span></span> 
  
<span data-ttu-id="5eab3-109">En la siguiente ilustración se muestra cada uno de los objetos que los proveedores de transporte pueden implementar con sus interfaces correspondientes.</span><span class="sxs-lookup"><span data-stu-id="5eab3-109">The following illustration shows each of the objects that transport providers can implement with their corresponding interfaces.</span></span> <span data-ttu-id="5eab3-110">La ilustración también indica si MAPI o un cliente es el usuario del objeto.</span><span class="sxs-lookup"><span data-stu-id="5eab3-110">The illustration also indicates whether MAPI or a client is the object's user.</span></span>
  
<span data-ttu-id="5eab3-111">![Objetos que los proveedores de transporte implementan]Objetos que los proveedores de transporte(media/amapi_66.gif "implementan")</span><span class="sxs-lookup"><span data-stu-id="5eab3-111">![Objects that transport providers implement](media/amapi_66.gif "Objects that transport providers implement")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5eab3-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="5eab3-112">See also</span></span>

- [<span data-ttu-id="5eab3-113">Objetos del proveedor de servicios MAPI</span><span class="sxs-lookup"><span data-stu-id="5eab3-113">MAPI Service Provider Objects</span></span>](mapi-service-provider-objects.md)

