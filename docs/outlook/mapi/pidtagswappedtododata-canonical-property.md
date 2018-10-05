---
title: Propiedad canónica PidTagSwappedToDoData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoData
api_type:
- COM
ms.assetid: d2a82fc8-de5d-4819-906e-b8314fd06ea0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3ecfa1e89688ae525a28e221424fb4a8194fc217
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386673"
---
# <a name="pidtagswappedtododata-canonical-property"></a><span data-ttu-id="d1a6d-103">Propiedad canónica PidTagSwappedToDoData</span><span class="sxs-lookup"><span data-stu-id="d1a6d-103">PidTagSwappedToDoData Canonical Property</span></span>

  
  
<span data-ttu-id="d1a6d-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1a6d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1a6d-105">Mantiene un segundo conjunto de valores de propiedad que no influyen en el estado del objeto de mensaje marcado.</span><span class="sxs-lookup"><span data-stu-id="d1a6d-105">Maintains a second set of property values that do not affect the flagged state of the Message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d1a6d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d1a6d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d1a6d-107">PR_SWAPPED_TODO_DATA</span><span class="sxs-lookup"><span data-stu-id="d1a6d-107">PR_SWAPPED_TODO_DATA</span></span>  <br/> |
|<span data-ttu-id="d1a6d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d1a6d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d1a6d-109">0x0E2D</span><span class="sxs-lookup"><span data-stu-id="d1a6d-109">0x0E2D</span></span>  <br/> |
|<span data-ttu-id="d1a6d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d1a6d-110">Data type:</span></span>  <br/> |<span data-ttu-id="d1a6d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d1a6d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d1a6d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d1a6d-112">Area:</span></span>  <br/> |<span data-ttu-id="d1a6d-113">MAPI no transmisible</span><span class="sxs-lookup"><span data-stu-id="d1a6d-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1a6d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d1a6d-114">Remarks</span></span>

<span data-ttu-id="d1a6d-115">Actúa como la ubicación de almacenamiento marca secundaria si son compatibles con marcas de remitente o avisos de remitente, esta estructura proporciona una ubicación en la que se va a almacenar todas las propiedades relacionadas con el protocolo de marcar informativos que son compatibles con marcas de remitente y todas propiedades relacionadas con el protocolo de configuración de aviso que son compatibles con los avisos de remitente sin exponer la información de aviso de remitente a los destinatarios de un mensaje o un indicador de remitente.</span><span class="sxs-lookup"><span data-stu-id="d1a6d-115">Acting as the secondary flag storage location if sender flags or sender reminders are supported, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in sender flags, and all properties relating to the Reminder Settings Protocol that are supported in sender reminders without exposing the sender flag or sender reminder information to the recipients of a message.</span></span>
  
<span data-ttu-id="d1a6d-116">De forma similar, esta estructura proporciona una ubicación en la que se va a almacenar todas las propiedades relacionadas con el protocolo de marcar informativos que son compatibles con marcas de destinatarios y propiedades relacionadas con el protocolo de configuración de aviso que son compatibles con destinatario avisos en un mensaje enviado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d1a6d-116">Similarly, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in recipient flags and properties relating to the Reminder Settings Protocol that are supported in recipient reminders on a previously sent message.</span></span>
  
<span data-ttu-id="d1a6d-117">Para obtener más información acerca de esta propiedad, vea [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d1a6d-117">For more information about this property, see [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d1a6d-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1a6d-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d1a6d-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d1a6d-119">Protocol specifications</span></span>

<span data-ttu-id="d1a6d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1a6d-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1a6d-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d1a6d-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d1a6d-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1a6d-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1a6d-123">Especifica las propiedades y las operaciones relacionadas con marcas.</span><span class="sxs-lookup"><span data-stu-id="d1a6d-123">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="d1a6d-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1a6d-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1a6d-125">Especifica las propiedades y el modelo de interacción para correo electrónico y otros avisos de objeto.</span><span class="sxs-lookup"><span data-stu-id="d1a6d-125">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d1a6d-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d1a6d-126">Header files</span></span>

<span data-ttu-id="d1a6d-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d1a6d-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="d1a6d-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d1a6d-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="d1a6d-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d1a6d-129">Mapitags.h</span></span>
  
> <span data-ttu-id="d1a6d-130">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d1a6d-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d1a6d-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1a6d-131">See also</span></span>



[<span data-ttu-id="d1a6d-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d1a6d-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d1a6d-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d1a6d-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d1a6d-134">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d1a6d-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d1a6d-135">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="d1a6d-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

