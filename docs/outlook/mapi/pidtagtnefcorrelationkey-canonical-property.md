---
title: Propiedad canónica PidTagTnefCorrelationKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTnefCorrelationKey
api_type:
- COM
ms.assetid: a7f05c8c-59b4-4d5b-8e70-ebcde5f2ed45
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5a0216616d9a35ef5ad4509bc377044c1d217d79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820387"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a><span data-ttu-id="4c07f-103">Propiedad canónica PidTagTnefCorrelationKey</span><span class="sxs-lookup"><span data-stu-id="4c07f-103">PidTagTnefCorrelationKey Canonical Property</span></span>

  
  
<span data-ttu-id="4c07f-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4c07f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4c07f-105">Contiene un valor que correlaciona un dato adjunto de formato de encapsulación neutro de transporte (TNEF) con un mensaje.</span><span class="sxs-lookup"><span data-stu-id="4c07f-105">Contains a value that correlates a Transport Neutral Encapsulation Format (TNEF) attachment with a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4c07f-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4c07f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4c07f-107">PR_TNEF_CORRELATION_KEY</span><span class="sxs-lookup"><span data-stu-id="4c07f-107">PR_TNEF_CORRELATION_KEY</span></span>  <br/> |
|<span data-ttu-id="4c07f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4c07f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4c07f-109">0x007F</span><span class="sxs-lookup"><span data-stu-id="4c07f-109">0x007F</span></span>  <br/> |
|<span data-ttu-id="4c07f-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4c07f-110">Data type:</span></span>  <br/> |<span data-ttu-id="4c07f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4c07f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4c07f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4c07f-112">Area:</span></span>  <br/> |<span data-ttu-id="4c07f-113">Sobres MAPI</span><span class="sxs-lookup"><span data-stu-id="4c07f-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c07f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4c07f-114">Remarks</span></span>

<span data-ttu-id="4c07f-115">Se recomienda que los objetos secundarios de los datos adjuntos TNEF exponen esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4c07f-115">It is recommended that TNEF attachment sub-objects expose this property.</span></span> <span data-ttu-id="4c07f-116">Esta propiedad determina si un archivo TNEF entrante pertenece al mensaje que está unido.</span><span class="sxs-lookup"><span data-stu-id="4c07f-116">This property determines whether or not an inbound TNEF file belongs to the message it is attached to.</span></span> <span data-ttu-id="4c07f-117">Se utiliza principalmente por proveedores de transporte y las puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="4c07f-117">It is used primarily by transport providers and gateways.</span></span>
  
<span data-ttu-id="4c07f-118">En un mensaje saliente, el proveedor de transporte debe calcular un valor binario único a ese mensaje, o usar un valor existente que cumple el requisito de unicidad, como un identificador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="4c07f-118">On an outbound message, the transport provider should compute a binary value unique to that message, or use an existing value that satisfies the uniqueness requirement, such as a message identifier.</span></span> <span data-ttu-id="4c07f-119">El proveedor de transporte debe almacenar este valor en esta propiedad y, a continuación, llamar al método [ITnef::AddProps](itnef-addprops.md) para encapsularlo.</span><span class="sxs-lookup"><span data-stu-id="4c07f-119">The transport provider should store this value in this property and then call the [ITnef::AddProps](itnef-addprops.md) method to encapsulate it.</span></span> <span data-ttu-id="4c07f-120">El valor de la misma también debe almacenarse en el contenedor de transporte en un lugar definido por el proveedor, por ejemplo, el encabezado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4c07f-120">The same value should also be stored in the transport envelope in a place defined by the provider, such as the message header.</span></span> 
  
<span data-ttu-id="4c07f-121">En un mensaje entrante, el proveedor de transporte debe llamar al método [ITnef::ExtractProps](itnef-extractprops.md) para los datos adjuntos TNEF desencapsulan y, a continuación, compare esta propiedad con el valor almacenado en el contenedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="4c07f-121">On an inbound message, the transport provider should call the [ITnef::ExtractProps](itnef-extractprops.md) method to decapsulate the TNEF attachment and then compare this property with the value stored in the transport envelope.</span></span> <span data-ttu-id="4c07f-122">Si los valores coinciden, se debe procesar TNEF normalmente, es decir, se deben usar todas las propiedades extraídas de los datos adjuntos TNEF.</span><span class="sxs-lookup"><span data-stu-id="4c07f-122">If the values match, TNEF should be processed normally, that is, all the properties extracted from the TNEF attachment should be used.</span></span> <span data-ttu-id="4c07f-123">Si los valores no coinciden, se deben omitir todas las propiedades de los datos adjuntos TNEF.</span><span class="sxs-lookup"><span data-stu-id="4c07f-123">If the values do not match, all the properties from the TNEF attachment should be ignored.</span></span> <span data-ttu-id="4c07f-124">Si no se establece esta propiedad, se debe considerar el archivo TNEF que pertenecen a este mensaje, y las demás propiedades extraídas de los deben usarse.</span><span class="sxs-lookup"><span data-stu-id="4c07f-124">If this property is not set, the TNEF file should be considered to belong to this message, and the other properties extracted from it should be used.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4c07f-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4c07f-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4c07f-126">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="4c07f-126">Protocol specifications</span></span>

<span data-ttu-id="4c07f-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c07f-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c07f-128">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="4c07f-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4c07f-129">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c07f-129">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c07f-130">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="4c07f-130">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="4c07f-131">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c07f-131">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c07f-132">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="4c07f-132">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="4c07f-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4c07f-133">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4c07f-134">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="4c07f-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4c07f-135">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4c07f-135">Header files</span></span>

<span data-ttu-id="4c07f-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4c07f-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="4c07f-137">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4c07f-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="4c07f-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4c07f-138">Mapitags.h</span></span>
  
> <span data-ttu-id="4c07f-139">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="4c07f-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4c07f-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c07f-140">See also</span></span>



[<span data-ttu-id="4c07f-141">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4c07f-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4c07f-142">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="4c07f-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4c07f-143">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4c07f-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4c07f-144">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="4c07f-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
