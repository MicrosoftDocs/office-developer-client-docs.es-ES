---
title: IUnknown IProviderAdmin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin
api_type:
- COM
ms.assetid: bdb4cdca-8dfd-4f90-9467-ec31cea3f518
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bedec72e8371d0e8aa69415d2f0dc77b4c62ff76
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315529"
---
# <a name="iprovideradmin--iunknown"></a><span data-ttu-id="70e98-103">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="70e98-103">IProviderAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="70e98-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70e98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70e98-105">Trabaja con proveedores de servicios en un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="70e98-105">Works with service providers in a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="70e98-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="70e98-106">Header file:</span></span>  <br/> |<span data-ttu-id="70e98-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="70e98-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="70e98-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="70e98-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="70e98-109">Objetos de administración del proveedor</span><span class="sxs-lookup"><span data-stu-id="70e98-109">Provider administration objects</span></span>  <br/> |
|<span data-ttu-id="70e98-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="70e98-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="70e98-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="70e98-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="70e98-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="70e98-112">Called by:</span></span>  <br/> |<span data-ttu-id="70e98-113">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="70e98-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="70e98-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="70e98-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="70e98-115">IID_IProviderAdmin</span><span class="sxs-lookup"><span data-stu-id="70e98-115">IID_IProviderAdmin</span></span>  <br/> |
|<span data-ttu-id="70e98-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="70e98-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="70e98-117">LPPROVIDERADMIN</span><span class="sxs-lookup"><span data-stu-id="70e98-117">LPPROVIDERADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="70e98-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="70e98-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="70e98-119">Volvió</span><span class="sxs-lookup"><span data-stu-id="70e98-119">GetLastError</span></span>](iprovideradmin-getlasterror.md) <br/> |<span data-ttu-id="70e98-120">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produjo en el objeto de administración del proveedor.</span><span class="sxs-lookup"><span data-stu-id="70e98-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span>  <br/> |
|[<span data-ttu-id="70e98-121">GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="70e98-121">GetProviderTable</span></span>](iprovideradmin-getprovidertable.md) <br/> |<span data-ttu-id="70e98-122">Proporciona acceso a la tabla de proveedores del servicio de mensajes, una lista de los proveedores de servicios del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="70e98-122">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>  <br/> |
|[<span data-ttu-id="70e98-123">CreateProvider</span><span class="sxs-lookup"><span data-stu-id="70e98-123">CreateProvider</span></span>](iprovideradmin-createprovider.md) <br/> |<span data-ttu-id="70e98-124">Agrega un proveedor de servicios al servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="70e98-124">Adds a service provider to the message service.</span></span>  <br/> |
|[<span data-ttu-id="70e98-125">DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="70e98-125">DeleteProvider</span></span>](iprovideradmin-deleteprovider.md) <br/> |<span data-ttu-id="70e98-126">Elimina un proveedor de servicios del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="70e98-126">Deletes a service provider from the message service.</span></span>  <br/> |
|[<span data-ttu-id="70e98-127">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="70e98-127">OpenProfileSection</span></span>](iprovideradmin-openprofilesection.md) <br/> |<span data-ttu-id="70e98-128">Abre una sección de perfil desde el perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="70e98-128">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70e98-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="70e98-129">Remarks</span></span>

<span data-ttu-id="70e98-130">Los clientes pueden obtener un puntero a una interfaz **IProviderAdmin** llamando al método [IMsgServiceAdmin:: AdminProviders](imsgserviceadmin-adminproviders.md) ; a los proveedores de servicios se les pasa un puntero **IProviderAdmin** cuando se llama a la función de punto de entrada del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="70e98-130">Clients can get a pointer to an **IProviderAdmin** interface by calling the [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) method; service providers are passed an **IProviderAdmin** pointer when their message service's entry point function is called.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="70e98-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="70e98-131">See also</span></span>



[<span data-ttu-id="70e98-132">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="70e98-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

