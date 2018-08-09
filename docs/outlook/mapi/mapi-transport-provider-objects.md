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
ms.openlocfilehash: 2d7311857ff54ef253fd00634671f4a510443f19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818230"
---
# <a name="mapi-transport-provider-objects"></a><span data-ttu-id="c4d5b-103">Objetos de proveedor de transporte MAPI</span><span class="sxs-lookup"><span data-stu-id="c4d5b-103">MAPI transport provider objects</span></span>
  
<span data-ttu-id="c4d5b-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c4d5b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c4d5b-105">Además de los objetos de inicio de sesión implementados por todos los proveedores de servicio y proveedor estándar, los proveedores de transporte necesarios para implementar un objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="c4d5b-105">In addition to the standard provider and logon objects implemented by all service providers, transport providers are required to implement a status object.</span></span> <span data-ttu-id="c4d5b-106">Para los demás tipos de proveedor servicio, la implementación de un objeto de estado es opcional.</span><span class="sxs-lookup"><span data-stu-id="c4d5b-106">For the other service provider types, implementing a status object is optional.</span></span> <span data-ttu-id="c4d5b-107">Sin embargo, MAPI requiere para los proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="c4d5b-107">However, MAPI requires it for transport providers.</span></span> <span data-ttu-id="c4d5b-108">Los proveedores de transporte que admiten la descarga de encabezados de los mensajes desde un servidor remoto también implementan una carpeta y una tabla.</span><span class="sxs-lookup"><span data-stu-id="c4d5b-108">Transport providers that support the downloading of message headers from a remote server also implement a folder and a table.</span></span> 
  
<span data-ttu-id="c4d5b-109">En la siguiente ilustración se muestra cada uno de los objetos que los proveedores de transporte se pueden implementar con sus interfaces correspondientes.</span><span class="sxs-lookup"><span data-stu-id="c4d5b-109">The following illustration shows each of the objects that transport providers can implement with their corresponding interfaces.</span></span> <span data-ttu-id="c4d5b-110">En la ilustración también indica si MAPI o un cliente es usuario del objeto.</span><span class="sxs-lookup"><span data-stu-id="c4d5b-110">The illustration also indicates whether MAPI or a client is the object's user.</span></span>
  
<span data-ttu-id="c4d5b-111">![Objetos que implementan los proveedores de transporte] (media/amapi_66.gif "Objetos que implementan los proveedores de transporte")</span><span class="sxs-lookup"><span data-stu-id="c4d5b-111">![Objects that transport providers implement](media/amapi_66.gif "Objects that transport providers implement")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c4d5b-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4d5b-112">See also</span></span>

- [<span data-ttu-id="c4d5b-113">Objetos de proveedor de servicio MAPI</span><span class="sxs-lookup"><span data-stu-id="c4d5b-113">MAPI Service Provider Objects</span></span>](mapi-service-provider-objects.md)

