---
title: Propiedad canónica PidTagRtfSyncBodyCrc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCrc
api_type:
- COM
ms.assetid: 95db4837-400f-476f-b313-60e8baa1c6d1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 85ac61d968243283e5ad9283730941adcd87cd5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357872"
---
# <a name="pidtagrtfsyncbodycrc-canonical-property"></a><span data-ttu-id="a79bc-103">Propiedad canónica PidTagRtfSyncBodyCrc</span><span class="sxs-lookup"><span data-stu-id="a79bc-103">PidTagRtfSyncBodyCrc Canonical Property</span></span>

  
  
<span data-ttu-id="a79bc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a79bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a79bc-105">Contiene la comprobación de redundancia cíclica (CRC) calculada para el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="a79bc-105">Contains the cyclical redundancy check (CRC) computed for the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a79bc-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a79bc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a79bc-107">PR_RTF_SYNC_BODY_CRC</span><span class="sxs-lookup"><span data-stu-id="a79bc-107">PR_RTF_SYNC_BODY_CRC</span></span>  <br/> |
|<span data-ttu-id="a79bc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a79bc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a79bc-109">0x1006</span><span class="sxs-lookup"><span data-stu-id="a79bc-109">0x1006</span></span>  <br/> |
|<span data-ttu-id="a79bc-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a79bc-110">Data type:</span></span>  <br/> |<span data-ttu-id="a79bc-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a79bc-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a79bc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a79bc-112">Area:</span></span>  <br/> |<span data-ttu-id="a79bc-113">Mensaje MAPI</span><span class="sxs-lookup"><span data-stu-id="a79bc-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a79bc-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a79bc-114">Remarks</span></span>

<span data-ttu-id="a79bc-115">La [función RTFSync](rtfsync.md) calcula el CRC usando solo los caracteres que considera significativos para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="a79bc-115">The [RTFSync](rtfsync.md) function computes the CRC by using only the characters that it considers to be significant to the message.</span></span> <span data-ttu-id="a79bc-116">Por ejemplo, se omiten algunos espacios en blanco y otros caracteres ignorables del CRC.</span><span class="sxs-lookup"><span data-stu-id="a79bc-116">For example, some white space and other ignorable characters are omitted from the CRC.</span></span> 
  
<span data-ttu-id="a79bc-117">Esta propiedad es una propiedad auxiliar de formato de texto enriquecido (RTF).</span><span class="sxs-lookup"><span data-stu-id="a79bc-117">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="a79bc-118">La función **RTFSync** usa estas propiedades y no están diseñadas para que las usen directamente las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="a79bc-118">These properties are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a79bc-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a79bc-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a79bc-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="a79bc-120">Protocol specifications</span></span>

<span data-ttu-id="a79bc-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a79bc-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a79bc-122">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="a79bc-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a79bc-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a79bc-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a79bc-124">Codifica y descodifica objetos de mensaje y datos adjuntos en una representación de secuencia eficiente.</span><span class="sxs-lookup"><span data-stu-id="a79bc-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a79bc-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a79bc-125">Header files</span></span>

<span data-ttu-id="a79bc-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a79bc-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a79bc-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a79bc-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="a79bc-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a79bc-128">Mapitags.h</span></span>
  
> <span data-ttu-id="a79bc-129">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="a79bc-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a79bc-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a79bc-130">See also</span></span>



[<span data-ttu-id="a79bc-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a79bc-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a79bc-132">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="a79bc-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a79bc-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a79bc-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a79bc-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="a79bc-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

