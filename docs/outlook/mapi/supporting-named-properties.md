---
title: Compatibilidad con propiedades con nombre
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 27625e913f06e858295351ed62de840ae7789915
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434329"
---
# <a name="supporting-named-properties"></a><span data-ttu-id="cd2f4-103">Compatibilidad con propiedades con nombre</span><span class="sxs-lookup"><span data-stu-id="cd2f4-103">Supporting Named Properties</span></span>

  
  
<span data-ttu-id="cd2f4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd2f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd2f4-105">Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties.</span><span class="sxs-lookup"><span data-stu-id="cd2f4-105">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties.</span></span> <span data-ttu-id="cd2f4-106">Se requiere compatibilidad con propiedades con nombre para:</span><span class="sxs-lookup"><span data-stu-id="cd2f4-106">Support for named properties is required for:</span></span> 
  
- <span data-ttu-id="cd2f4-107">Proveedores de libretas de direcciones que permiten que las entradas de otros proveedores se copien en sus contenedores.</span><span class="sxs-lookup"><span data-stu-id="cd2f4-107">Address book providers that allow entries from other providers to be copied into their containers.</span></span>
    
- <span data-ttu-id="cd2f4-108">Proveedores de almacenamiento de mensajes que se pueden usar para crear tipos de mensajes arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="cd2f4-108">Message store providers that can be used to create arbitrary message types.</span></span>
    
<span data-ttu-id="cd2f4-109">La compatibilidad con propiedades con nombre es opcional para todos los demás proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="cd2f4-109">Named property support is optional for all other service providers.</span></span> <span data-ttu-id="cd2f4-110">Los proveedores de servicios que admiten propiedades con nombre deben implementar la asignación de nombre a identificador en los métodos [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) e [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="cd2f4-110">Service providers that do support named properties must implement name-to-identifier mapping in the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods.</span></span> <span data-ttu-id="cd2f4-111">Los clientes llaman a **GetNamesFromIDs** para recuperar los nombres correspondientes de uno o más identificadores de propiedad en el intervalo de más de 0x8000 y **GetIDsFromNames** para crear o recuperar los identificadores de uno o más nombres.</span><span class="sxs-lookup"><span data-stu-id="cd2f4-111">Clients call **GetNamesFromIDs** to retrieve the corresponding names for one or more property identifiers in the over 0x8000 range and **GetIDsFromNames** to either create or retrieve the identifiers for one or more names.</span></span> 
  
<span data-ttu-id="cd2f4-112">Los proveedores de servicios que no admiten propiedades con nombre deben:</span><span class="sxs-lookup"><span data-stu-id="cd2f4-112">Service providers that do not support named properties must:</span></span>
  
- <span data-ttu-id="cd2f4-113">Error en las llamadas a [IMAPIProp::SetProps](imapiprop-setprops.md) para establecer propiedades con identificadores de 0x8000 o superior devolviendo MAPI_E_UNEXPECTED_ID en la matriz [SPropProblem.](spropproblem.md)</span><span class="sxs-lookup"><span data-stu-id="cd2f4-113">Fail calls to [IMAPIProp::SetProps](imapiprop-setprops.md) to set properties with identifiers of 0x8000 or greater by returning MAPI_E_UNEXPECTED_ID in the [SPropProblem](spropproblem.md) array.</span></span> 
    
- <span data-ttu-id="cd2f4-114">Devolver MAPI_E_NO_SUPPORT de los [métodos IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) e [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="cd2f4-114">Return MAPI_E_NO_SUPPORT from the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods .</span></span> 
    

