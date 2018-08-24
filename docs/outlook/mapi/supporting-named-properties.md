---
title: Admitir propiedades con nombre
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9ee41469914e52295af219428f26854662c9e2f9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582251"
---
# <a name="supporting-named-properties"></a><span data-ttu-id="a424b-103">Admitir propiedades con nombre</span><span class="sxs-lookup"><span data-stu-id="a424b-103">Supporting Named Properties</span></span>

  
  
<span data-ttu-id="a424b-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a424b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a424b-105">Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties.</span><span class="sxs-lookup"><span data-stu-id="a424b-105">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties.</span></span> <span data-ttu-id="a424b-106">Es necesario para la compatibilidad con las propiedades con nombre:</span><span class="sxs-lookup"><span data-stu-id="a424b-106">Support for named properties is required for:</span></span> 
  
- <span data-ttu-id="a424b-107">Proveedores de libreta de direcciones que permiten las entradas de otros proveedores que se copiarán a sus contenedores.</span><span class="sxs-lookup"><span data-stu-id="a424b-107">Address book providers that allow entries from other providers to be copied into their containers.</span></span>
    
- <span data-ttu-id="a424b-108">Los proveedores que se pueden usar para crear tipos de mensaje arbitrario del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a424b-108">Message store providers that can be used to create arbitrary message types.</span></span>
    
<span data-ttu-id="a424b-109">Compatibilidad con la propiedad con nombre es opcional para todos los demás proveedores de servicio.</span><span class="sxs-lookup"><span data-stu-id="a424b-109">Named property support is optional for all other service providers.</span></span> <span data-ttu-id="a424b-110">Proveedores de servicios que admiten las propiedades con nombre deben implementar la asignación de nombre a identificador en los métodos [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) y [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="a424b-110">Service providers that do support named properties must implement name-to-identifier mapping in the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods.</span></span> <span data-ttu-id="a424b-111">Los clientes llaman **GetNamesFromIDs** para recuperar los nombres correspondientes para uno o varios identificadores de propiedad en el intervalo de 0 x 8000 sobre y **a GetIDsFromNames** para crear o recuperar los identificadores de uno o varios nombres.</span><span class="sxs-lookup"><span data-stu-id="a424b-111">Clients call **GetNamesFromIDs** to retrieve the corresponding names for one or more property identifiers in the over 0x8000 range and **GetIDsFromNames** to either create or retrieve the identifiers for one or more names.</span></span> 
  
<span data-ttu-id="a424b-112">Proveedores de servicios que no admiten las propiedades con nombre deben:</span><span class="sxs-lookup"><span data-stu-id="a424b-112">Service providers that do not support named properties must:</span></span>
  
- <span data-ttu-id="a424b-113">Producirá un error en las llamadas a [IMAPIProp::SetProps](imapiprop-setprops.md) para establecer las propiedades con identificadores de 0 x 8000 o posterior mediante la devolución de MAPI_E_UNEXPECTED_ID en la matriz [SPropProblem](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="a424b-113">Fail calls to [IMAPIProp::SetProps](imapiprop-setprops.md) to set properties with identifiers of 0x8000 or greater by returning MAPI_E_UNEXPECTED_ID in the [SPropProblem](spropproblem.md) array.</span></span> 
    
- <span data-ttu-id="a424b-114">Devolver MAPI_E_NO_SUPPORT de los métodos [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) y [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="a424b-114">Return MAPI_E_NO_SUPPORT from the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods .</span></span> 
    

