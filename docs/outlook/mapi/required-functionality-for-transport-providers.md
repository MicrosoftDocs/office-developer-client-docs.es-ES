---
title: Funcionalidad necesaria para proveedores de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: dc1189df1b8ad8f8e613d6813681ed3f4148b122
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580498"
---
# <a name="required-functionality-for-transport-providers"></a><span data-ttu-id="9779a-103">Funcionalidad necesaria para proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="9779a-103">Required Functionality for Transport Providers</span></span>

  
  
<span data-ttu-id="9779a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9779a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9779a-105">Cada proveedor de transporte MAPI debe:</span><span class="sxs-lookup"><span data-stu-id="9779a-105">Every MAPI transport provider must:</span></span>
  
- <span data-ttu-id="9779a-106">Siga las instrucciones generales para trabajar con MAPI y otros proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="9779a-106">Follow the general guidelines for working with MAPI and other service providers.</span></span> <span data-ttu-id="9779a-107">Para obtener más información, vea [El desarrollo de aplicaciones MAPI](mapi-application-development.md) y [Proveedores de servicios de MAPI](mapi-service-providers.md).</span><span class="sxs-lookup"><span data-stu-id="9779a-107">For more information, see [MAPI Application Development](mapi-application-development.md) and [MAPI Service Providers](mapi-service-providers.md).</span></span>
    
- <span data-ttu-id="9779a-108">Tienen su función de inicialización [XPProviderInit](xpproviderinit.md) de su proveedor de transporte exponen DLL a MAPI.</span><span class="sxs-lookup"><span data-stu-id="9779a-108">Have its transport provider DLL expose to MAPI its [XPProviderInit](xpproviderinit.md) initialization function.</span></span> 
    
- <span data-ttu-id="9779a-109">Exponer a MAPI en su implementación de la [IXPProvider: IUnknown](ixpprovideriunknown.md) y [IXPLogon: IUnknown](ixplogoniunknown.md) interfaces.</span><span class="sxs-lookup"><span data-stu-id="9779a-109">Expose to MAPI its implementation of the [IXPProvider : IUnknown](ixpprovideriunknown.md) and [IXPLogon : IUnknown](ixplogoniunknown.md) interfaces.</span></span> 
    
- <span data-ttu-id="9779a-110">Exponer las aplicaciones MAPI y cliente de su implementación de la [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="9779a-110">Expose to MAPI and client applications its implementation of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="9779a-111">Para obtener más información acerca de cómo implementar **IMAPIStatus**, vea [Implementación de objeto de estado](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="9779a-111">For more information about implementing **IMAPIStatus**, see [Status Object Implementation](status-object-implementation.md).</span></span> 
    
- <span data-ttu-id="9779a-112">Implementar un cuadro de diálogo de la hoja de propiedad para la configuración.</span><span class="sxs-lookup"><span data-stu-id="9779a-112">Implement a property sheet dialog box for configuration.</span></span> <span data-ttu-id="9779a-113">Para obtener más información acerca de cómo implementar las hojas de propiedades, vea [Implementación de la hoja de propiedad](property-sheet-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="9779a-113">For more information about implementing property sheets, see [Property Sheet Implementation](property-sheet-implementation.md).</span></span>
    

