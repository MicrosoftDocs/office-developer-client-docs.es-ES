---
title: Propiedad canónica PidTagOriginalMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalMessageClass
api_type:
- COM
ms.assetid: 49deb153-03c6-4be2-a3a5-53cca01accba
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7167b7b51698cda5610356779a8e8342b34a6082
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819850"
---
# <a name="pidtagoriginalmessageclass-canonical-property"></a><span data-ttu-id="e46a7-103">Propiedad canónica PidTagOriginalMessageClass</span><span class="sxs-lookup"><span data-stu-id="e46a7-103">PidTagOriginalMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="e46a7-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e46a7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e46a7-105">Contiene la clase del mensaje original para su uso en un informe.</span><span class="sxs-lookup"><span data-stu-id="e46a7-105">Contains the class of the original message for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e46a7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e46a7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e46a7-107">PR_ORIG_MESSAGE_CLASS, PR_ORIG_MESSAGE_CLASS_A, PR_ORIG_MESSAGE_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="e46a7-107">PR_ORIG_MESSAGE_CLASS, PR_ORIG_MESSAGE_CLASS_A, PR_ORIG_MESSAGE_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="e46a7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e46a7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e46a7-109">0x004B</span><span class="sxs-lookup"><span data-stu-id="e46a7-109">0x004B</span></span>  <br/> |
|<span data-ttu-id="e46a7-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e46a7-110">Data type:</span></span>  <br/> |<span data-ttu-id="e46a7-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e46a7-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e46a7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e46a7-112">Area:</span></span>  <br/> |<span data-ttu-id="e46a7-113">Propiedades de mensajería de seguro</span><span class="sxs-lookup"><span data-stu-id="e46a7-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e46a7-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e46a7-114">Remarks</span></span>

<span data-ttu-id="e46a7-115">Estas propiedades contienen una copia de la propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) del mensaje para el que se está generando el informe.</span><span class="sxs-lookup"><span data-stu-id="e46a7-115">These properties contain a copy of the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message for which the report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e46a7-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e46a7-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e46a7-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e46a7-117">Protocol specifications</span></span>

<span data-ttu-id="e46a7-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e46a7-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e46a7-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e46a7-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e46a7-120">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e46a7-120">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e46a7-121">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="e46a7-121">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e46a7-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e46a7-122">Header files</span></span>

<span data-ttu-id="e46a7-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e46a7-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e46a7-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e46a7-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e46a7-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e46a7-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e46a7-126">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="e46a7-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e46a7-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e46a7-127">See also</span></span>



[<span data-ttu-id="e46a7-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e46a7-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e46a7-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e46a7-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e46a7-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e46a7-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e46a7-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="e46a7-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

