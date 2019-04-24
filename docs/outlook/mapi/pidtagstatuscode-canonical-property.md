---
title: Propiedad canónica PidTagStatusCode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusCode
api_type:
- COM
ms.assetid: e29190c5-52c3-4ef7-98db-699487c54325
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 751be8abe02dfb1d5bab2bcbbbc0cbd2a8243f85
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278761"
---
# <a name="pidtagstatuscode-canonical-property"></a><span data-ttu-id="63b94-103">Propiedad canónica PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="63b94-103">PidTagStatusCode Canonical Property</span></span>

  
  
<span data-ttu-id="63b94-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63b94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63b94-105">Contiene una máscara de máscara de marcas que indican el estado actual de un recurso de sesión.</span><span class="sxs-lookup"><span data-stu-id="63b94-105">Contains a bitmask of flags that indicate the current status of a session resource.</span></span> <span data-ttu-id="63b94-106">Todos los proveedores de servicios establecen los códigos de estado como hace MAPI para informar sobre el estado del subsistema, la cola MAPI y la libreta de direcciones integrada.</span><span class="sxs-lookup"><span data-stu-id="63b94-106">All service providers set status codes as does MAPI to report on the status of the subsystem, the MAPI spooler, and the integrated address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="63b94-107">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="63b94-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="63b94-108">PR_STATUS_CODE</span><span class="sxs-lookup"><span data-stu-id="63b94-108">PR_STATUS_CODE</span></span>  <br/> |
|<span data-ttu-id="63b94-109">Identificador:</span><span class="sxs-lookup"><span data-stu-id="63b94-109">Identifier:</span></span>  <br/> |<span data-ttu-id="63b94-110">0x3E04</span><span class="sxs-lookup"><span data-stu-id="63b94-110">0x3E04</span></span>  <br/> |
|<span data-ttu-id="63b94-111">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="63b94-111">Data type:</span></span>  <br/> |<span data-ttu-id="63b94-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="63b94-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="63b94-113">Área:</span><span class="sxs-lookup"><span data-stu-id="63b94-113">Area:</span></span>  <br/> |<span data-ttu-id="63b94-114">Estado de MAPI</span><span class="sxs-lookup"><span data-stu-id="63b94-114">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63b94-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="63b94-115">Remarks</span></span>

<span data-ttu-id="63b94-116">El código de Estado debe aparecer en el archivo MAPISVC. inf para todos los proveedores.</span><span class="sxs-lookup"><span data-stu-id="63b94-116">The status code must appear in the Mapisvc.inf file for all providers.</span></span> 
  
<span data-ttu-id="63b94-117">Los objetos de estado son implementados por MAPI y por todos los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="63b94-117">Status objects are implemented by MAPI and by all service providers.</span></span> <span data-ttu-id="63b94-118">Hay dos conjuntos de valores válidos para los códigos de estado: un conjunto para todos los objetos status y otro conjunto solo para los proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="63b94-118">There are two sets of valid values for status codes, one set for all status objects and another set for transport providers only.</span></span> <span data-ttu-id="63b94-119">Todos los objetos status pueden establecer esta propiedad en los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="63b94-119">All status objects can set this property to the following values:</span></span>
  
<span data-ttu-id="63b94-120">STATUS_AVAILABLE</span><span class="sxs-lookup"><span data-stu-id="63b94-120">STATUS_AVAILABLE</span></span> 
  
> <span data-ttu-id="63b94-121">Indica que el recurso está operativo.</span><span class="sxs-lookup"><span data-stu-id="63b94-121">Indicates that the resource is operational.</span></span>
    
<span data-ttu-id="63b94-122">STATUS_FAILURE</span><span class="sxs-lookup"><span data-stu-id="63b94-122">STATUS_FAILURE</span></span> 
  
> <span data-ttu-id="63b94-123">Indica que el recurso está experimentando un problema.</span><span class="sxs-lookup"><span data-stu-id="63b94-123">Indicates that the resource is experiencing a problem.</span></span> <span data-ttu-id="63b94-124">Para los proveedores de servicios, STATUS_FAILURE indica que el proveedor puede cerrarse pronto para finalizar la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="63b94-124">For service providers, STATUS_FAILURE indicates that the provider might soon be shut down to end the current session.</span></span>
    
<span data-ttu-id="63b94-125">STATUS_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="63b94-125">STATUS_OFFLINE</span></span> 
  
> <span data-ttu-id="63b94-126">Indica que solo están disponibles los datos locales o los servicios.</span><span class="sxs-lookup"><span data-stu-id="63b94-126">Indicates that only local data or services are available.</span></span>
    
<span data-ttu-id="63b94-127">Los proveedores de transporte también pueden establecer sus propiedades **PR_STATUS_CODE** de objetos de estado en los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="63b94-127">Transport providers can also set their status objects' **PR_STATUS_CODE** properties to the following values:</span></span> 
  
<span data-ttu-id="63b94-128">STATUS_INBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="63b94-128">STATUS_INBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="63b94-129">Indica que el proveedor de transporte está recibiendo un mensaje entrante.</span><span class="sxs-lookup"><span data-stu-id="63b94-129">Indicates that the transport provider is receiving an inbound message.</span></span> 
    
<span data-ttu-id="63b94-130">STATUS_INBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="63b94-130">STATUS_INBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="63b94-131">Indica que el proveedor de transporte puede recibir mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="63b94-131">Indicates that the transport provider can receive inbound messages.</span></span>
    
<span data-ttu-id="63b94-132">STATUS_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="63b94-132">STATUS_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="63b94-133">Indica que el proveedor de transporte está descargando mensajes de la cola de entrada.</span><span class="sxs-lookup"><span data-stu-id="63b94-133">Indicates that the transport provider is downloading messages from the inbound queue.</span></span>
    
<span data-ttu-id="63b94-134">STATUS_OUTBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="63b94-134">STATUS_OUTBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="63b94-135">Indica que el proveedor de transporte está recibiendo un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="63b94-135">Indicates that the transport provider is receiving an outbound message.</span></span> 
    
<span data-ttu-id="63b94-136">STATUS_OUTBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="63b94-136">STATUS_OUTBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="63b94-137">Indica que el proveedor de transporte puede controlar los mensajes salientes.</span><span class="sxs-lookup"><span data-stu-id="63b94-137">Indicates that the transport provider can handle outbound messages.</span></span>
    
<span data-ttu-id="63b94-138">STATUS_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="63b94-138">STATUS_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="63b94-139">Indica que el proveedor de transporte está cargando mensajes desde su cola de salida.</span><span class="sxs-lookup"><span data-stu-id="63b94-139">Indicates that the transport provider is uploading messages from its outbound queue.</span></span>
    
<span data-ttu-id="63b94-140">STATUS_REMOTE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="63b94-140">STATUS_REMOTE_ACCESS</span></span> 
  
> <span data-ttu-id="63b94-141">Indica que el proveedor de transporte admite el acceso remoto.</span><span class="sxs-lookup"><span data-stu-id="63b94-141">Indicates that the transport provider supports remote access.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="63b94-142">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="63b94-142">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="63b94-143">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="63b94-143">Header files</span></span>

<span data-ttu-id="63b94-144">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="63b94-144">Mapidefs.h</span></span>
  
> <span data-ttu-id="63b94-145">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="63b94-145">Provides data type definitions.</span></span>
    
<span data-ttu-id="63b94-146">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="63b94-146">Mapitags.h</span></span>
  
> <span data-ttu-id="63b94-147">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="63b94-147">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="63b94-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="63b94-148">See also</span></span>



[<span data-ttu-id="63b94-149">Propiedad canónica PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="63b94-149">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)


[<span data-ttu-id="63b94-150">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="63b94-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="63b94-151">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="63b94-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="63b94-152">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="63b94-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="63b94-153">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="63b94-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

