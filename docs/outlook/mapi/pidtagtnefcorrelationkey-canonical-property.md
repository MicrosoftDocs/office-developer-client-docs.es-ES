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
ms.openlocfilehash: e38cf93523c14d2d58c48e24a79249674298b4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341954"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a><span data-ttu-id="f4daa-103">Propiedad canónica PidTagTnefCorrelationKey</span><span class="sxs-lookup"><span data-stu-id="f4daa-103">PidTagTnefCorrelationKey Canonical Property</span></span>

  
  
<span data-ttu-id="f4daa-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4daa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4daa-105">Contiene un valor que correlaciona los datos adjuntos del formato de encapsulamiento neutro de transporte (TNEF) con un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f4daa-105">Contains a value that correlates a Transport Neutral Encapsulation Format (TNEF) attachment with a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f4daa-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f4daa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f4daa-107">PR_TNEF_CORRELATION_KEY</span><span class="sxs-lookup"><span data-stu-id="f4daa-107">PR_TNEF_CORRELATION_KEY</span></span>  <br/> |
|<span data-ttu-id="f4daa-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f4daa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f4daa-109">0x007F</span><span class="sxs-lookup"><span data-stu-id="f4daa-109">0x007F</span></span>  <br/> |
|<span data-ttu-id="f4daa-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f4daa-110">Data type:</span></span>  <br/> |<span data-ttu-id="f4daa-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f4daa-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f4daa-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f4daa-112">Area:</span></span>  <br/> |<span data-ttu-id="f4daa-113">Sobre MAPI</span><span class="sxs-lookup"><span data-stu-id="f4daa-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4daa-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f4daa-114">Remarks</span></span>

<span data-ttu-id="f4daa-115">Se recomienda que los subdominios de datos adjuntos TNEF exponán esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f4daa-115">It is recommended that TNEF attachment sub-objects expose this property.</span></span> <span data-ttu-id="f4daa-116">Esta propiedad determina si un archivo TNEF entrante pertenece o no al mensaje al que está adjunto.</span><span class="sxs-lookup"><span data-stu-id="f4daa-116">This property determines whether or not an inbound TNEF file belongs to the message it is attached to.</span></span> <span data-ttu-id="f4daa-117">Lo usan principalmente los proveedores de transporte y las puertas de enlace.</span><span class="sxs-lookup"><span data-stu-id="f4daa-117">It is used primarily by transport providers and gateways.</span></span>
  
<span data-ttu-id="f4daa-118">En un mensaje saliente, el proveedor de transporte debe calcular un valor binario único para ese mensaje o usar un valor existente que satisfaga el requisito de unidad, como un identificador de mensaje.</span><span class="sxs-lookup"><span data-stu-id="f4daa-118">On an outbound message, the transport provider should compute a binary value unique to that message, or use an existing value that satisfies the uniqueness requirement, such as a message identifier.</span></span> <span data-ttu-id="f4daa-119">El proveedor de transporte debe almacenar este valor en esta propiedad y, a continuación, llamar al método [ITnef::AddProps](itnef-addprops.md) para encapsularlo.</span><span class="sxs-lookup"><span data-stu-id="f4daa-119">The transport provider should store this value in this property and then call the [ITnef::AddProps](itnef-addprops.md) method to encapsulate it.</span></span> <span data-ttu-id="f4daa-120">El mismo valor también debe almacenarse en el sobre de transporte en un lugar definido por el proveedor, como el encabezado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f4daa-120">The same value should also be stored in the transport envelope in a place defined by the provider, such as the message header.</span></span> 
  
<span data-ttu-id="f4daa-121">En un mensaje entrante, el proveedor de transporte debe llamar al método [ITnef::ExtractProps](itnef-extractprops.md) para decapsular los datos adjuntos TNEF y, a continuación, comparar esta propiedad con el valor almacenado en el sobre de transporte.</span><span class="sxs-lookup"><span data-stu-id="f4daa-121">On an inbound message, the transport provider should call the [ITnef::ExtractProps](itnef-extractprops.md) method to decapsulate the TNEF attachment and then compare this property with the value stored in the transport envelope.</span></span> <span data-ttu-id="f4daa-122">Si los valores coinciden, TNEF debe procesarse normalmente, es decir, deben usarse todas las propiedades extraídas de los datos adjuntos TNEF.</span><span class="sxs-lookup"><span data-stu-id="f4daa-122">If the values match, TNEF should be processed normally, that is, all the properties extracted from the TNEF attachment should be used.</span></span> <span data-ttu-id="f4daa-123">Si los valores no coinciden, se deben omitir todas las propiedades de los datos adjuntos TNEF.</span><span class="sxs-lookup"><span data-stu-id="f4daa-123">If the values do not match, all the properties from the TNEF attachment should be ignored.</span></span> <span data-ttu-id="f4daa-124">Si no se establece esta propiedad, se debe considerar que el archivo TNEF pertenece a este mensaje y se deben usar las demás propiedades extraídas de él.</span><span class="sxs-lookup"><span data-stu-id="f4daa-124">If this property is not set, the TNEF file should be considered to belong to this message, and the other properties extracted from it should be used.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f4daa-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f4daa-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f4daa-126">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="f4daa-126">Protocol specifications</span></span>

<span data-ttu-id="f4daa-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4daa-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4daa-128">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="f4daa-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f4daa-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4daa-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4daa-130">Controla el orden y el flujo de las transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="f4daa-130">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="f4daa-131">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4daa-131">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4daa-132">Convierte las convenciones de correo electrónico estándar de Internet en objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="f4daa-132">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="f4daa-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4daa-133">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4daa-134">Codifica y descodifica objetos de mensaje y datos adjuntos a una representación de secuencia eficiente.</span><span class="sxs-lookup"><span data-stu-id="f4daa-134">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f4daa-135">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f4daa-135">Header files</span></span>

<span data-ttu-id="f4daa-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f4daa-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="f4daa-137">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f4daa-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="f4daa-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f4daa-138">Mapitags.h</span></span>
  
> <span data-ttu-id="f4daa-139">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f4daa-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4daa-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f4daa-140">See also</span></span>



[<span data-ttu-id="f4daa-141">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f4daa-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f4daa-142">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="f4daa-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f4daa-143">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f4daa-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f4daa-144">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="f4daa-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

