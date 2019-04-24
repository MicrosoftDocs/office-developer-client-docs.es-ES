---
title: Objetos de estado MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 38310619-1b1d-4934-8533-d0612676c0b0
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 816d1b7c9c0b8c5a80a2351580ce3224fccf0b14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309537"
---
# <a name="mapi-status-objects"></a><span data-ttu-id="22dde-103">Objetos de estado MAPI</span><span class="sxs-lookup"><span data-stu-id="22dde-103">MAPI Status Objects</span></span>

  
  
<span data-ttu-id="22dde-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22dde-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22dde-105">Los objetos de estado notifican información sobre los recursos MAPI.</span><span class="sxs-lookup"><span data-stu-id="22dde-105">Status objects report information about MAPI resources.</span></span> <span data-ttu-id="22dde-106">Por ejemplo, un proveedor de servicios, el proceso de envío y recepción de MAPI o la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="22dde-106">For example, a service provider, the MAPI send/receive process, or the address book.</span></span>
  
<span data-ttu-id="22dde-107">Hay un objeto status que proporciona información acerca de cada proveedor de servicios individual en el perfil actual.</span><span class="sxs-lookup"><span data-stu-id="22dde-107">There is a status object supplying information about each individual service provider in the current profile.</span></span> <span data-ttu-id="22dde-108">MAPI es responsable de implementar objetos de estado para el subsistema, el proceso de envío y recepción de MAPI y la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="22dde-108">MAPI is responsible for implementing status objects for the subsystem, the MAPI send/receive process, and the address book.</span></span> <span data-ttu-id="22dde-109">El objeto de estado de subsistema proporciona información global.</span><span class="sxs-lookup"><span data-stu-id="22dde-109">The subsystem status object supplies global information.</span></span> <span data-ttu-id="22dde-110">El objeto de estado de la libreta de direcciones integrada proporciona el estado de todos los proveedores de la libreta de direcciones actualmente en funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="22dde-110">The status object for the integrated address book supplies the status of all address book providers currently operating.</span></span>
  
<span data-ttu-id="22dde-111">Cada objeto status se incluye en la tabla de estado, una tabla que mantiene MAPI y que proporciona a los clientes toda la información de estado de la sesión.</span><span class="sxs-lookup"><span data-stu-id="22dde-111">Every status object is included in the status table, a table maintained by MAPI that provides clients with all of the status information for the session.</span></span> <span data-ttu-id="22dde-112">Para obtener más información, vea [tablas de estado](status-tables.md).</span><span class="sxs-lookup"><span data-stu-id="22dde-112">For more information, see [Status Tables](status-tables.md).</span></span> <span data-ttu-id="22dde-113">Los clientes pueden tener acceso a un objeto de estado concreto a través de la tabla o, en el caso de un proveedor de servicios, a través de su objeto de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="22dde-113">Clients can access a particular status object either through the table or, for a service provider, through its logon object.</span></span> <span data-ttu-id="22dde-114">Por ejemplo, para tener acceso a un objeto de estado de un proveedor de libreta de direcciones, un cliente puede llamar a **IABLogon:: OpenStatusEntry**.</span><span class="sxs-lookup"><span data-stu-id="22dde-114">For example, to access an address book provider's status object, a client can call **IABLogon::OpenStatusEntry**.</span></span> <span data-ttu-id="22dde-115">Para obtener más información, vea [IABLogon:: OpenStatusEntry](iablogon-openstatusentry.md).</span><span class="sxs-lookup"><span data-stu-id="22dde-115">For more information, see [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md).</span></span>
  
<span data-ttu-id="22dde-116">Los clientes pueden usar objetos de estado para:</span><span class="sxs-lookup"><span data-stu-id="22dde-116">Clients can use status objects to:</span></span>
  
- <span data-ttu-id="22dde-117">Obtenga información sobre el estado de una sesión.</span><span class="sxs-lookup"><span data-stu-id="22dde-117">Learn about the state of a session.</span></span>
    
- <span data-ttu-id="22dde-118">Supervisar a un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="22dde-118">Monitor a service provider.</span></span>
    
- <span data-ttu-id="22dde-119">Controlar la transmisión de mensajes.</span><span class="sxs-lookup"><span data-stu-id="22dde-119">Control message transmission.</span></span>
    
- <span data-ttu-id="22dde-120">Ver o cambiar la configuración y el estado de un recurso.</span><span class="sxs-lookup"><span data-stu-id="22dde-120">View or change a resource's configuration and status.</span></span>
    
<span data-ttu-id="22dde-121">Cada objeto status implementa la interfaz **IMAPIStatus** .</span><span class="sxs-lookup"><span data-stu-id="22dde-121">Every status object implements the **IMAPIStatus** interface.</span></span> <span data-ttu-id="22dde-122">Para obtener más información, vea [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="22dde-122">For more information, see [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).</span></span> <span data-ttu-id="22dde-123">Sin embargo, no todos los objetos status admiten completamente todos los métodos **IMAPIStatus** .</span><span class="sxs-lookup"><span data-stu-id="22dde-123">However, not every status object fully supports every **IMAPIStatus** method.</span></span> <span data-ttu-id="22dde-124">Dado que hay variación en los métodos admitidos por un objeto status, los clientes necesitan obtener información sobre un objeto status determinado para poder usarlo.</span><span class="sxs-lookup"><span data-stu-id="22dde-124">Because there is variation in the methods that are supported by a status object, clients need to learn about a particular status object before they can use it.</span></span> <span data-ttu-id="22dde-125">Los objetos de estado son necesarios para publicar información sobre sus características en las siguientes tres propiedades:</span><span class="sxs-lookup"><span data-stu-id="22dde-125">Status objects are required to publish information about their features in the following three properties:</span></span> 
  
 <span data-ttu-id="22dde-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="22dde-126">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span> 
  
 <span data-ttu-id="22dde-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="22dde-127">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="22dde-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="22dde-128">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span> 
  
<span data-ttu-id="22dde-129">Para obtener más información sobre la implementación de un objeto status, vea status ( [implementación de objetos](status-object-implementation.md)).</span><span class="sxs-lookup"><span data-stu-id="22dde-129">For more information about implementing a status object, see [Status Object Implementation](status-object-implementation.md).</span></span> <span data-ttu-id="22dde-130">Para obtener más información acerca del uso de un objeto status, vea [tabla de estado y objetos de estado](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="22dde-130">For more information about using a status object, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

