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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331258"
---
# <a name="pidtagrtfsyncbodycount-canonical-property"></a><span data-ttu-id="31247-103">Propiedad canónica PidTagRtfSyncBodyCount</span><span class="sxs-lookup"><span data-stu-id="31247-103">PidTagRtfSyncBodyCount Canonical Property</span></span>

  
  
<span data-ttu-id="31247-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31247-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31247-105">Contiene un recuento de los caracteres significativos del texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="31247-105">Contains a count of the significant characters of the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="31247-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="31247-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="31247-107">PR_RTF_SYNC_BODY_COUNT</span><span class="sxs-lookup"><span data-stu-id="31247-107">PR_RTF_SYNC_BODY_COUNT</span></span>  <br/> |
|<span data-ttu-id="31247-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="31247-108">Identifier:</span></span>  <br/> |<span data-ttu-id="31247-109">0x1007</span><span class="sxs-lookup"><span data-stu-id="31247-109">0x1007</span></span>  <br/> |
|<span data-ttu-id="31247-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="31247-110">Data type:</span></span>  <br/> |<span data-ttu-id="31247-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="31247-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="31247-112">Área:</span><span class="sxs-lookup"><span data-stu-id="31247-112">Area:</span></span>  <br/> |<span data-ttu-id="31247-113">Mensaje MAPI</span><span class="sxs-lookup"><span data-stu-id="31247-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31247-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="31247-114">Remarks</span></span>

<span data-ttu-id="31247-115">La [función RTFSync](rtfsync.md) calcula el recuento de caracteres del texto usando solo los que considera significativos para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="31247-115">The [RTFSync](rtfsync.md) function computes the count of characters in the text using only those that it considers to be significant to the message.</span></span> <span data-ttu-id="31247-116">Por ejemplo, se omiten algunos espacios en blanco y otros caracteres ignorables del recuento.</span><span class="sxs-lookup"><span data-stu-id="31247-116">For example, some white space and other ignorable characters are omitted from the count.</span></span> 
  
<span data-ttu-id="31247-117">Esta propiedad es una propiedad auxiliar de formato de texto enriquecido (RTF).</span><span class="sxs-lookup"><span data-stu-id="31247-117">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="31247-118">La función **RTFSync** usa estas propiedades y no están diseñadas para que las usen directamente las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="31247-118">These properties are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="31247-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="31247-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="31247-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="31247-120">Protocol specifications</span></span>

<span data-ttu-id="31247-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="31247-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="31247-122">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="31247-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="31247-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="31247-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="31247-124">Codifica y descodifica objetos de mensaje y datos adjuntos en una representación de secuencia eficiente.</span><span class="sxs-lookup"><span data-stu-id="31247-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="31247-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="31247-125">Header files</span></span>

<span data-ttu-id="31247-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="31247-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="31247-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="31247-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="31247-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="31247-128">Mapitags.h</span></span>
  
> <span data-ttu-id="31247-129">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="31247-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="31247-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="31247-130">See also</span></span>



[<span data-ttu-id="31247-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="31247-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="31247-132">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="31247-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="31247-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="31247-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="31247-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="31247-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

