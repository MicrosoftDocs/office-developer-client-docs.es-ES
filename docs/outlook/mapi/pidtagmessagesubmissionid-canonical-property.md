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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329403"
---
# <a name="pidtagmessagesubmissionid-canonical-property"></a><span data-ttu-id="ce49d-103">Propiedad canónica PidTagMessageSubmissionId</span><span class="sxs-lookup"><span data-stu-id="ce49d-103">PidTagMessageSubmissionId Canonical Property</span></span>

  
  
<span data-ttu-id="ce49d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce49d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce49d-105">Contiene un identificador de sistema de transferencia de mensajes (MTS) para el agente de transferencia de mensajes (MTA).</span><span class="sxs-lookup"><span data-stu-id="ce49d-105">Contains a message transfer system (MTS) identifier for the message transfer agent (MTA).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ce49d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ce49d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ce49d-107">PR_MESSAGE_SUBMISSION_ID</span><span class="sxs-lookup"><span data-stu-id="ce49d-107">PR_MESSAGE_SUBMISSION_ID</span></span>  <br/> |
|<span data-ttu-id="ce49d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ce49d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ce49d-109">0x0047</span><span class="sxs-lookup"><span data-stu-id="ce49d-109">0x0047</span></span>  <br/> |
|<span data-ttu-id="ce49d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ce49d-110">Data type:</span></span>  <br/> |<span data-ttu-id="ce49d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ce49d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ce49d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ce49d-112">Area:</span></span>  <br/> |<span data-ttu-id="ce49d-113">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="ce49d-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce49d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ce49d-114">Remarks</span></span>

<span data-ttu-id="ce49d-115">Esta propiedad es devuelta por el MTA una vez completado correctamente el envío de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ce49d-115">This property is returned by the MTA upon successful completion of message submission.</span></span> <span data-ttu-id="ce49d-116">Cualquier contacto futuro con el MTA con respecto a este mensaje, como solicitar la cancelación, usa el identificador mts en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="ce49d-116">Any future contact with the MTA regarding this message, such as requesting cancellation, uses the MTS identifier in this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ce49d-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ce49d-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ce49d-118">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="ce49d-118">Protocol specifications</span></span>

<span data-ttu-id="ce49d-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ce49d-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ce49d-120">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="ce49d-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ce49d-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ce49d-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ce49d-122">Codifica y descodifica objetos de mensaje y datos adjuntos en una representación de secuencia eficiente.</span><span class="sxs-lookup"><span data-stu-id="ce49d-122">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ce49d-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ce49d-123">Header files</span></span>

<span data-ttu-id="ce49d-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ce49d-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="ce49d-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ce49d-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="ce49d-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ce49d-126">Mapitags.h</span></span>
  
> <span data-ttu-id="ce49d-127">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="ce49d-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ce49d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce49d-128">See also</span></span>



[<span data-ttu-id="ce49d-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ce49d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ce49d-130">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="ce49d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ce49d-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ce49d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ce49d-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="ce49d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

