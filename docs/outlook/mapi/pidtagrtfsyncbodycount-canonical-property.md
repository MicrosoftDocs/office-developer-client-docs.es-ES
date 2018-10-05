---
title: Propiedad canónica PidTagRtfSyncBodyCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCount
api_type:
- COM
ms.assetid: b7267be4-8d5c-4dc7-86b2-651e03e84f9b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6f6e687412dfce1e5fcee6b4a4d64f3e5106455f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398804"
---
# <a name="pidtagrtfsyncbodycount-canonical-property"></a><span data-ttu-id="23cda-103">Propiedad canónica PidTagRtfSyncBodyCount</span><span class="sxs-lookup"><span data-stu-id="23cda-103">PidTagRtfSyncBodyCount Canonical Property</span></span>

  
  
<span data-ttu-id="23cda-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23cda-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23cda-105">Contiene un recuento de los caracteres del texto del mensaje significativos.</span><span class="sxs-lookup"><span data-stu-id="23cda-105">Contains a count of the significant characters of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="23cda-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="23cda-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="23cda-107">PR_RTF_SYNC_BODY_COUNT</span><span class="sxs-lookup"><span data-stu-id="23cda-107">PR_RTF_SYNC_BODY_COUNT</span></span>  <br/> |
|<span data-ttu-id="23cda-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="23cda-108">Identifier:</span></span>  <br/> |<span data-ttu-id="23cda-109">0 x 1007</span><span class="sxs-lookup"><span data-stu-id="23cda-109">0x1007</span></span>  <br/> |
|<span data-ttu-id="23cda-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="23cda-110">Data type:</span></span>  <br/> |<span data-ttu-id="23cda-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="23cda-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="23cda-112">Área:</span><span class="sxs-lookup"><span data-stu-id="23cda-112">Area:</span></span>  <br/> |<span data-ttu-id="23cda-113">Mensaje MAPI</span><span class="sxs-lookup"><span data-stu-id="23cda-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23cda-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="23cda-114">Remarks</span></span>

<span data-ttu-id="23cda-115">La función [RTFSync](rtfsync.md) calcula el recuento de caracteres del texto sólo con los que considera que es importante para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="23cda-115">The [RTFSync](rtfsync.md) function computes the count of characters in the text using only those that it considers to be significant to the message.</span></span> <span data-ttu-id="23cda-116">Por ejemplo, se omiten algunos espacios en blanco y otros caracteres puede pasar por alto desde el recuento.</span><span class="sxs-lookup"><span data-stu-id="23cda-116">For example, some white space and other ignorable characters are omitted from the count.</span></span> 
  
<span data-ttu-id="23cda-117">Esta propiedad es una propiedad auxiliar de formato de texto enriquecido (RTF).</span><span class="sxs-lookup"><span data-stu-id="23cda-117">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="23cda-118">Estas propiedades se usan por la función **RTFSync** y no están diseñadas para usarse directamente por las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="23cda-118">These properties are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="23cda-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="23cda-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="23cda-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="23cda-120">Protocol specifications</span></span>

<span data-ttu-id="23cda-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23cda-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23cda-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="23cda-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="23cda-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23cda-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23cda-124">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="23cda-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="23cda-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="23cda-125">Header files</span></span>

<span data-ttu-id="23cda-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="23cda-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="23cda-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="23cda-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="23cda-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="23cda-128">Mapitags.h</span></span>
  
> <span data-ttu-id="23cda-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="23cda-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="23cda-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="23cda-130">See also</span></span>



[<span data-ttu-id="23cda-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="23cda-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="23cda-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="23cda-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="23cda-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="23cda-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="23cda-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="23cda-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

