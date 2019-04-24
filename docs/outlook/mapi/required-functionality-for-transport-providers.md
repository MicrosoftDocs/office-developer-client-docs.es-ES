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
ms.openlocfilehash: 7f9768d47cf740bdf50b439ee3af4b0d2a191602
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328689"
---
# <a name="required-functionality-for-transport-providers"></a><span data-ttu-id="cd5c1-103">Funcionalidad necesaria para proveedores de transporte</span><span class="sxs-lookup"><span data-stu-id="cd5c1-103">Required Functionality for Transport Providers</span></span>

  
  
<span data-ttu-id="cd5c1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd5c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd5c1-105">Cada proveedor de transporte MAPI debe:</span><span class="sxs-lookup"><span data-stu-id="cd5c1-105">Every MAPI transport provider must:</span></span>
  
- <span data-ttu-id="cd5c1-106">Siga las instrucciones generales para trabajar con MAPI y otros proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="cd5c1-106">Follow the general guidelines for working with MAPI and other service providers.</span></span> <span data-ttu-id="cd5c1-107">Para obtener más información, consulte [desarrollo de aplicaciones MAPI](mapi-application-development.md) y [proveedores de servicios MAPI](mapi-service-providers.md).</span><span class="sxs-lookup"><span data-stu-id="cd5c1-107">For more information, see [MAPI Application Development](mapi-application-development.md) and [MAPI Service Providers](mapi-service-providers.md).</span></span>
    
- <span data-ttu-id="cd5c1-108">Hacer que su DLL de proveedor de transporte exponga a MAPI su función de inicialización de [XPProviderInit](xpproviderinit.md) .</span><span class="sxs-lookup"><span data-stu-id="cd5c1-108">Have its transport provider DLL expose to MAPI its [XPProviderInit](xpproviderinit.md) initialization function.</span></span> 
    
- <span data-ttu-id="cd5c1-109">Exponga a MAPI su implementación de las interfaces [IXPProvider: IUnknown](ixpprovideriunknown.md) y [IXPLogon: IUnknown](ixplogoniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="cd5c1-109">Expose to MAPI its implementation of the [IXPProvider : IUnknown](ixpprovideriunknown.md) and [IXPLogon : IUnknown](ixplogoniunknown.md) interfaces.</span></span> 
    
- <span data-ttu-id="cd5c1-110">Exponer a MAPI y a las aplicaciones cliente su implementación de la interfaz [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="cd5c1-110">Expose to MAPI and client applications its implementation of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="cd5c1-111">Para obtener más información sobre la implementación de **IMAPIStatus**, vea status ( [implementación de objetos](status-object-implementation.md)).</span><span class="sxs-lookup"><span data-stu-id="cd5c1-111">For more information about implementing **IMAPIStatus**, see [Status Object Implementation](status-object-implementation.md).</span></span> 
    
- <span data-ttu-id="cd5c1-112">Implemente un cuadro de diálogo de hoja de propiedades para la configuración.</span><span class="sxs-lookup"><span data-stu-id="cd5c1-112">Implement a property sheet dialog box for configuration.</span></span> <span data-ttu-id="cd5c1-113">Para obtener más información acerca de la implementación de hojas de propiedades, vea [implementación de hojas de propiedades](property-sheet-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="cd5c1-113">For more information about implementing property sheets, see [Property Sheet Implementation](property-sheet-implementation.md).</span></span>
    

