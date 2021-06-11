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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418517"
---
# <a name="pidtagstatuscode-canonical-property"></a><span data-ttu-id="82188-103">Propiedad canónica PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="82188-103">PidTagStatusCode Canonical Property</span></span>

  
  
<span data-ttu-id="82188-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82188-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82188-105">Contiene una máscara de bits de marcas que indican el estado actual de un recurso de sesión.</span><span class="sxs-lookup"><span data-stu-id="82188-105">Contains a bitmask of flags that indicate the current status of a session resource.</span></span> <span data-ttu-id="82188-106">Todos los proveedores de servicios establecen códigos de estado al igual que MAPI para informar sobre el estado del subsistema, la cola MAPI y la libreta de direcciones integrada.</span><span class="sxs-lookup"><span data-stu-id="82188-106">All service providers set status codes as does MAPI to report on the status of the subsystem, the MAPI spooler, and the integrated address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="82188-107">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="82188-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="82188-108">PR_STATUS_CODE</span><span class="sxs-lookup"><span data-stu-id="82188-108">PR_STATUS_CODE</span></span>  <br/> |
|<span data-ttu-id="82188-109">Identificador:</span><span class="sxs-lookup"><span data-stu-id="82188-109">Identifier:</span></span>  <br/> |<span data-ttu-id="82188-110">0x3E04</span><span class="sxs-lookup"><span data-stu-id="82188-110">0x3E04</span></span>  <br/> |
|<span data-ttu-id="82188-111">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="82188-111">Data type:</span></span>  <br/> |<span data-ttu-id="82188-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="82188-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="82188-113">Área:</span><span class="sxs-lookup"><span data-stu-id="82188-113">Area:</span></span>  <br/> |<span data-ttu-id="82188-114">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="82188-114">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82188-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="82188-115">Remarks</span></span>

<span data-ttu-id="82188-116">El código de estado debe aparecer en el archivo Mapisvc.inf para todos los proveedores.</span><span class="sxs-lookup"><span data-stu-id="82188-116">The status code must appear in the Mapisvc.inf file for all providers.</span></span> 
  
<span data-ttu-id="82188-117">Mapi y todos los proveedores de servicios implementan objetos de estado.</span><span class="sxs-lookup"><span data-stu-id="82188-117">Status objects are implemented by MAPI and by all service providers.</span></span> <span data-ttu-id="82188-118">Hay dos conjuntos de valores válidos para códigos de estado, uno establecido para todos los objetos de estado y otro conjunto solo para proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="82188-118">There are two sets of valid values for status codes, one set for all status objects and another set for transport providers only.</span></span> <span data-ttu-id="82188-119">Todos los objetos de estado pueden establecer esta propiedad en los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="82188-119">All status objects can set this property to the following values:</span></span>
  
<span data-ttu-id="82188-120">STATUS_AVAILABLE</span><span class="sxs-lookup"><span data-stu-id="82188-120">STATUS_AVAILABLE</span></span> 
  
> <span data-ttu-id="82188-121">Indica que el recurso está operativo.</span><span class="sxs-lookup"><span data-stu-id="82188-121">Indicates that the resource is operational.</span></span>
    
<span data-ttu-id="82188-122">STATUS_FAILURE</span><span class="sxs-lookup"><span data-stu-id="82188-122">STATUS_FAILURE</span></span> 
  
> <span data-ttu-id="82188-123">Indica que el recurso está experimentando un problema.</span><span class="sxs-lookup"><span data-stu-id="82188-123">Indicates that the resource is experiencing a problem.</span></span> <span data-ttu-id="82188-124">Para los proveedores de servicios, STATUS_FAILURE indica que el proveedor podría cerrarse pronto para finalizar la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="82188-124">For service providers, STATUS_FAILURE indicates that the provider might soon be shut down to end the current session.</span></span>
    
<span data-ttu-id="82188-125">STATUS_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="82188-125">STATUS_OFFLINE</span></span> 
  
> <span data-ttu-id="82188-126">Indica que solo están disponibles los datos o servicios locales.</span><span class="sxs-lookup"><span data-stu-id="82188-126">Indicates that only local data or services are available.</span></span>
    
<span data-ttu-id="82188-127">Los proveedores de transporte también pueden establecer las propiedades **de** PR_STATUS_CODE de sus objetos de estado en los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="82188-127">Transport providers can also set their status objects' **PR_STATUS_CODE** properties to the following values:</span></span> 
  
<span data-ttu-id="82188-128">STATUS_INBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="82188-128">STATUS_INBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="82188-129">Indica que el proveedor de transporte recibe un mensaje entrante.</span><span class="sxs-lookup"><span data-stu-id="82188-129">Indicates that the transport provider is receiving an inbound message.</span></span> 
    
<span data-ttu-id="82188-130">STATUS_INBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="82188-130">STATUS_INBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="82188-131">Indica que el proveedor de transporte puede recibir mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="82188-131">Indicates that the transport provider can receive inbound messages.</span></span>
    
<span data-ttu-id="82188-132">STATUS_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="82188-132">STATUS_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="82188-133">Indica que el proveedor de transporte está descargando mensajes de la cola entrante.</span><span class="sxs-lookup"><span data-stu-id="82188-133">Indicates that the transport provider is downloading messages from the inbound queue.</span></span>
    
<span data-ttu-id="82188-134">STATUS_OUTBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="82188-134">STATUS_OUTBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="82188-135">Indica que el proveedor de transporte recibe un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="82188-135">Indicates that the transport provider is receiving an outbound message.</span></span> 
    
<span data-ttu-id="82188-136">STATUS_OUTBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="82188-136">STATUS_OUTBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="82188-137">Indica que el proveedor de transporte puede controlar los mensajes salientes.</span><span class="sxs-lookup"><span data-stu-id="82188-137">Indicates that the transport provider can handle outbound messages.</span></span>
    
<span data-ttu-id="82188-138">STATUS_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="82188-138">STATUS_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="82188-139">Indica que el proveedor de transporte está cargando mensajes desde su cola de salida.</span><span class="sxs-lookup"><span data-stu-id="82188-139">Indicates that the transport provider is uploading messages from its outbound queue.</span></span>
    
<span data-ttu-id="82188-140">STATUS_REMOTE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="82188-140">STATUS_REMOTE_ACCESS</span></span> 
  
> <span data-ttu-id="82188-141">Indica que el proveedor de transporte admite el acceso remoto.</span><span class="sxs-lookup"><span data-stu-id="82188-141">Indicates that the transport provider supports remote access.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="82188-142">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="82188-142">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="82188-143">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="82188-143">Header files</span></span>

<span data-ttu-id="82188-144">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="82188-144">Mapidefs.h</span></span>
  
> <span data-ttu-id="82188-145">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="82188-145">Provides data type definitions.</span></span>
    
<span data-ttu-id="82188-146">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="82188-146">Mapitags.h</span></span>
  
> <span data-ttu-id="82188-147">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="82188-147">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="82188-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="82188-148">See also</span></span>



[<span data-ttu-id="82188-149">Propiedad canónica PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="82188-149">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)


[<span data-ttu-id="82188-150">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="82188-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="82188-151">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="82188-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="82188-152">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="82188-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="82188-153">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="82188-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

