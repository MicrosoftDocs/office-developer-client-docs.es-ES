---
title: Propiedad canónica PidTagMessageSubmissionId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSubmissionId
api_type:
- HeaderDef
ms.assetid: 0a799fe5-04e2-4e1d-b0cd-9bdd2577d299
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 723affa054cb35a9cc7a2ee28e051e3b9a6d04e0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401667"
---
# <a name="pidtagmessagesubmissionid-canonical-property"></a><span data-ttu-id="4405c-103">Propiedad canónica PidTagMessageSubmissionId</span><span class="sxs-lookup"><span data-stu-id="4405c-103">PidTagMessageSubmissionId Canonical Property</span></span>

  
  
<span data-ttu-id="4405c-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4405c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4405c-105">Contiene un identificador de sistema (MTS) de transferencia de mensaje para el agente de transferencia de mensajes (MTA).</span><span class="sxs-lookup"><span data-stu-id="4405c-105">Contains a message transfer system (MTS) identifier for the message transfer agent (MTA).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4405c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4405c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4405c-107">PR_MESSAGE_SUBMISSION_ID</span><span class="sxs-lookup"><span data-stu-id="4405c-107">PR_MESSAGE_SUBMISSION_ID</span></span>  <br/> |
|<span data-ttu-id="4405c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4405c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4405c-109">0x0047</span><span class="sxs-lookup"><span data-stu-id="4405c-109">0x0047</span></span>  <br/> |
|<span data-ttu-id="4405c-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4405c-110">Data type:</span></span>  <br/> |<span data-ttu-id="4405c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4405c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4405c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4405c-112">Area:</span></span>  <br/> |<span data-ttu-id="4405c-113">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="4405c-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4405c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4405c-114">Remarks</span></span>

<span data-ttu-id="4405c-115">Esta propiedad es devuelto por el MTA tras la finalización correcta de envío de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4405c-115">This property is returned by the MTA upon successful completion of message submission.</span></span> <span data-ttu-id="4405c-116">Cualquier contacto futuro con el MTA con respecto a este mensaje, como la cancelación solicitante, usa el identificador MTS en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4405c-116">Any future contact with the MTA regarding this message, such as requesting cancellation, uses the MTS identifier in this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4405c-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4405c-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4405c-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="4405c-118">Protocol specifications</span></span>

<span data-ttu-id="4405c-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4405c-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4405c-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="4405c-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4405c-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4405c-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4405c-122">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="4405c-122">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4405c-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4405c-123">Header files</span></span>

<span data-ttu-id="4405c-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4405c-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="4405c-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4405c-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="4405c-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4405c-126">Mapitags.h</span></span>
  
> <span data-ttu-id="4405c-127">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="4405c-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4405c-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4405c-128">See also</span></span>



[<span data-ttu-id="4405c-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4405c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4405c-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="4405c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4405c-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4405c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4405c-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="4405c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

