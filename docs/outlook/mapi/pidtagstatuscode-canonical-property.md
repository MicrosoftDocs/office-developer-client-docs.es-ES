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
# <a name="pidtagstatuscode-canonical-property"></a><span data-ttu-id="8941a-103">Propiedad canónica PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="8941a-103">PidTagStatusCode Canonical Property</span></span>

  
  
<span data-ttu-id="8941a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8941a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8941a-105">Contiene una máscara de bits de marcas que indican el estado actual de un recurso de sesión.</span><span class="sxs-lookup"><span data-stu-id="8941a-105">Contains a bitmask of flags that indicate the current status of a session resource.</span></span> <span data-ttu-id="8941a-106">Todos los proveedores de servicios establecen códigos de estado como MAPI para informar sobre el estado del subsistema, la cola MAPI y la libreta de direcciones integrada.</span><span class="sxs-lookup"><span data-stu-id="8941a-106">All service providers set status codes as does MAPI to report on the status of the subsystem, the MAPI spooler, and the integrated address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8941a-107">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8941a-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="8941a-108">PR_STATUS_CODE</span><span class="sxs-lookup"><span data-stu-id="8941a-108">PR_STATUS_CODE</span></span>  <br/> |
|<span data-ttu-id="8941a-109">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8941a-109">Identifier:</span></span>  <br/> |<span data-ttu-id="8941a-110">0x3E04</span><span class="sxs-lookup"><span data-stu-id="8941a-110">0x3E04</span></span>  <br/> |
|<span data-ttu-id="8941a-111">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8941a-111">Data type:</span></span>  <br/> |<span data-ttu-id="8941a-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8941a-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8941a-113">Área:</span><span class="sxs-lookup"><span data-stu-id="8941a-113">Area:</span></span>  <br/> |<span data-ttu-id="8941a-114">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="8941a-114">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8941a-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8941a-115">Remarks</span></span>

<span data-ttu-id="8941a-116">El código de estado debe aparecer en el archivo Mapisvc.inf para todos los proveedores.</span><span class="sxs-lookup"><span data-stu-id="8941a-116">The status code must appear in the Mapisvc.inf file for all providers.</span></span> 
  
<span data-ttu-id="8941a-117">Mapi y todos los proveedores de servicios implementan objetos de estado.</span><span class="sxs-lookup"><span data-stu-id="8941a-117">Status objects are implemented by MAPI and by all service providers.</span></span> <span data-ttu-id="8941a-118">Hay dos conjuntos de valores válidos para códigos de estado, uno para todos los objetos de estado y otro para proveedores de transporte únicamente.</span><span class="sxs-lookup"><span data-stu-id="8941a-118">There are two sets of valid values for status codes, one set for all status objects and another set for transport providers only.</span></span> <span data-ttu-id="8941a-119">Todos los objetos de estado pueden establecer esta propiedad en los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="8941a-119">All status objects can set this property to the following values:</span></span>
  
<span data-ttu-id="8941a-120">STATUS_AVAILABLE</span><span class="sxs-lookup"><span data-stu-id="8941a-120">STATUS_AVAILABLE</span></span> 
  
> <span data-ttu-id="8941a-121">Indica que el recurso está operativo.</span><span class="sxs-lookup"><span data-stu-id="8941a-121">Indicates that the resource is operational.</span></span>
    
<span data-ttu-id="8941a-122">STATUS_FAILURE</span><span class="sxs-lookup"><span data-stu-id="8941a-122">STATUS_FAILURE</span></span> 
  
> <span data-ttu-id="8941a-123">Indica que el recurso está experimentando un problema.</span><span class="sxs-lookup"><span data-stu-id="8941a-123">Indicates that the resource is experiencing a problem.</span></span> <span data-ttu-id="8941a-124">Para los proveedores de servicios, STATUS_FAILURE indica que es posible que el proveedor se cierre pronto para finalizar la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="8941a-124">For service providers, STATUS_FAILURE indicates that the provider might soon be shut down to end the current session.</span></span>
    
<span data-ttu-id="8941a-125">STATUS_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="8941a-125">STATUS_OFFLINE</span></span> 
  
> <span data-ttu-id="8941a-126">Indica que solo están disponibles los datos o servicios locales.</span><span class="sxs-lookup"><span data-stu-id="8941a-126">Indicates that only local data or services are available.</span></span>
    
<span data-ttu-id="8941a-127">Los proveedores de transporte también pueden establecer las propiedades de los objetos **PR_STATUS_CODE** estado en los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="8941a-127">Transport providers can also set their status objects' **PR_STATUS_CODE** properties to the following values:</span></span> 
  
<span data-ttu-id="8941a-128">STATUS_INBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="8941a-128">STATUS_INBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="8941a-129">Indica que el proveedor de transporte recibe un mensaje entrante.</span><span class="sxs-lookup"><span data-stu-id="8941a-129">Indicates that the transport provider is receiving an inbound message.</span></span> 
    
<span data-ttu-id="8941a-130">STATUS_INBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="8941a-130">STATUS_INBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="8941a-131">Indica que el proveedor de transporte puede recibir mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="8941a-131">Indicates that the transport provider can receive inbound messages.</span></span>
    
<span data-ttu-id="8941a-132">STATUS_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="8941a-132">STATUS_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="8941a-133">Indica que el proveedor de transporte está descargando mensajes de la cola entrante.</span><span class="sxs-lookup"><span data-stu-id="8941a-133">Indicates that the transport provider is downloading messages from the inbound queue.</span></span>
    
<span data-ttu-id="8941a-134">STATUS_OUTBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="8941a-134">STATUS_OUTBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="8941a-135">Indica que el proveedor de transporte recibe un mensaje saliente.</span><span class="sxs-lookup"><span data-stu-id="8941a-135">Indicates that the transport provider is receiving an outbound message.</span></span> 
    
<span data-ttu-id="8941a-136">STATUS_OUTBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="8941a-136">STATUS_OUTBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="8941a-137">Indica que el proveedor de transporte puede controlar los mensajes salientes.</span><span class="sxs-lookup"><span data-stu-id="8941a-137">Indicates that the transport provider can handle outbound messages.</span></span>
    
<span data-ttu-id="8941a-138">STATUS_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="8941a-138">STATUS_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="8941a-139">Indica que el proveedor de transporte está cargando mensajes desde su cola de salida.</span><span class="sxs-lookup"><span data-stu-id="8941a-139">Indicates that the transport provider is uploading messages from its outbound queue.</span></span>
    
<span data-ttu-id="8941a-140">STATUS_REMOTE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8941a-140">STATUS_REMOTE_ACCESS</span></span> 
  
> <span data-ttu-id="8941a-141">Indica que el proveedor de transporte admite el acceso remoto.</span><span class="sxs-lookup"><span data-stu-id="8941a-141">Indicates that the transport provider supports remote access.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="8941a-142">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8941a-142">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8941a-143">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8941a-143">Header files</span></span>

<span data-ttu-id="8941a-144">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8941a-144">Mapidefs.h</span></span>
  
> <span data-ttu-id="8941a-145">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8941a-145">Provides data type definitions.</span></span>
    
<span data-ttu-id="8941a-146">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8941a-146">Mapitags.h</span></span>
  
> <span data-ttu-id="8941a-147">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="8941a-147">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8941a-148">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8941a-148">See also</span></span>



[<span data-ttu-id="8941a-149">Propiedad canónica PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="8941a-149">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)


[<span data-ttu-id="8941a-150">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8941a-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8941a-151">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="8941a-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8941a-152">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8941a-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8941a-153">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="8941a-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

