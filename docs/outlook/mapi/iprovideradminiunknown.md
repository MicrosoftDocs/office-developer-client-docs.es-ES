---
title: IProviderAdmin IUnknown
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 41195a49d1bf3566c81fe6e97697012209cbc5ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817907"
---
# <a name="iprovideradmin--iunknown"></a><span data-ttu-id="ff4f6-103">IProviderAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ff4f6-103">IProviderAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="ff4f6-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ff4f6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ff4f6-105">Funciona con proveedores de servicios en un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ff4f6-105">Works with service providers in a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff4f6-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="ff4f6-106">Header file:</span></span>  <br/> |<span data-ttu-id="ff4f6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ff4f6-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ff4f6-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="ff4f6-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="ff4f6-109">Objetos de administración del proveedor</span><span class="sxs-lookup"><span data-stu-id="ff4f6-109">Provider administration objects</span></span>  <br/> |
|<span data-ttu-id="ff4f6-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="ff4f6-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="ff4f6-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="ff4f6-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="ff4f6-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="ff4f6-112">Called by:</span></span>  <br/> |<span data-ttu-id="ff4f6-113">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="ff4f6-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="ff4f6-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="ff4f6-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ff4f6-115">IID_IProviderAdmin</span><span class="sxs-lookup"><span data-stu-id="ff4f6-115">IID_IProviderAdmin</span></span>  <br/> |
|<span data-ttu-id="ff4f6-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="ff4f6-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="ff4f6-117">LPPROVIDERADMIN</span><span class="sxs-lookup"><span data-stu-id="ff4f6-117">LPPROVIDERADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ff4f6-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="ff4f6-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ff4f6-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="ff4f6-119">GetLastError</span></span>](iprovideradmin-getlasterror.md) <br/> |<span data-ttu-id="ff4f6-120">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produjeron en el objeto de administración del proveedor.</span><span class="sxs-lookup"><span data-stu-id="ff4f6-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span>  <br/> |
|[<span data-ttu-id="ff4f6-121">GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="ff4f6-121">GetProviderTable</span></span>](iprovideradmin-getprovidertable.md) <br/> |<span data-ttu-id="ff4f6-122">Proporciona acceso a la tabla de proveedor del servicio de mensajes, una lista de los proveedores de servicios en el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ff4f6-122">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>  <br/> |
|[<span data-ttu-id="ff4f6-123">CreateProvider</span><span class="sxs-lookup"><span data-stu-id="ff4f6-123">CreateProvider</span></span>](iprovideradmin-createprovider.md) <br/> |<span data-ttu-id="ff4f6-124">Agrega un proveedor de servicios para el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ff4f6-124">Adds a service provider to the message service.</span></span>  <br/> |
|[<span data-ttu-id="ff4f6-125">DeleteProvider</span><span class="sxs-lookup"><span data-stu-id="ff4f6-125">DeleteProvider</span></span>](iprovideradmin-deleteprovider.md) <br/> |<span data-ttu-id="ff4f6-126">Elimina un proveedor de servicios desde el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ff4f6-126">Deletes a service provider from the message service.</span></span>  <br/> |
|[<span data-ttu-id="ff4f6-127">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="ff4f6-127">OpenProfileSection</span></span>](iprovideradmin-openprofilesection.md) <br/> |<span data-ttu-id="ff4f6-128">Abre una sección de perfil desde el perfil actual y devuelve un puntero [IProfSect](iprofsectimapiprop.md) para aún más el acceso.</span><span class="sxs-lookup"><span data-stu-id="ff4f6-128">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff4f6-129">Notas</span><span class="sxs-lookup"><span data-stu-id="ff4f6-129">Remarks</span></span>

<span data-ttu-id="ff4f6-130">Los clientes pueden obtener un puntero a una interfaz **IProviderAdmin** llamando al método [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) ; proveedores de servicios se pasan un puntero **IProviderAdmin** cuando se llama a la función de punto de entrada del servicio de sus mensajes.</span><span class="sxs-lookup"><span data-stu-id="ff4f6-130">Clients can get a pointer to an **IProviderAdmin** interface by calling the [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) method; service providers are passed an **IProviderAdmin** pointer when their message service's entry point function is called.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ff4f6-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="ff4f6-131">See also</span></span>



[<span data-ttu-id="ff4f6-132">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="ff4f6-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

