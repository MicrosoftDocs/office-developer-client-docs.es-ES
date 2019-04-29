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
# <a name="mapi-transport-provider-objects"></a><span data-ttu-id="3dff8-103">Objetos de proveedor de transporte MAPI</span><span class="sxs-lookup"><span data-stu-id="3dff8-103">MAPI transport provider objects</span></span>
  
<span data-ttu-id="3dff8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3dff8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3dff8-105">Además del proveedor estándar y los objetos de inicio de sesión implementados por todos los proveedores de servicios, se necesitan proveedores de transporte para implementar un objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="3dff8-105">In addition to the standard provider and logon objects implemented by all service providers, transport providers are required to implement a status object.</span></span> <span data-ttu-id="3dff8-106">Para los demás tipos de proveedores de servicios, implementar un objeto de estado es opcional.</span><span class="sxs-lookup"><span data-stu-id="3dff8-106">For the other service provider types, implementing a status object is optional.</span></span> <span data-ttu-id="3dff8-107">Sin embargo, MAPI lo necesita para los proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="3dff8-107">However, MAPI requires it for transport providers.</span></span> <span data-ttu-id="3dff8-108">Los proveedores de transporte que admiten la descarga de encabezados de mensaje desde un servidor remoto también implementan una carpeta y una tabla.</span><span class="sxs-lookup"><span data-stu-id="3dff8-108">Transport providers that support the downloading of message headers from a remote server also implement a folder and a table.</span></span> 
  
<span data-ttu-id="3dff8-109">En la siguiente ilustración se muestra cada uno de los objetos que los proveedores de transporte pueden implementar con sus interfaces correspondientes.</span><span class="sxs-lookup"><span data-stu-id="3dff8-109">The following illustration shows each of the objects that transport providers can implement with their corresponding interfaces.</span></span> <span data-ttu-id="3dff8-110">La ilustración también indica si MAPI o un cliente es el usuario del objeto.</span><span class="sxs-lookup"><span data-stu-id="3dff8-110">The illustration also indicates whether MAPI or a client is the object's user.</span></span>
  
<span data-ttu-id="3dff8-111">![Objetos que los proveedores de transporte implementan] (media/amapi_66.gif "Objetos que los proveedores de transporte implementan")</span><span class="sxs-lookup"><span data-stu-id="3dff8-111">![Objects that transport providers implement](media/amapi_66.gif "Objects that transport providers implement")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3dff8-112">Ver también</span><span class="sxs-lookup"><span data-stu-id="3dff8-112">See also</span></span>

- [<span data-ttu-id="3dff8-113">Objetos de proveedor de servicios MAPI</span><span class="sxs-lookup"><span data-stu-id="3dff8-113">MAPI Service Provider Objects</span></span>](mapi-service-provider-objects.md)

