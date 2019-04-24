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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359139"
---
# <a name="pidtagswappedtododata-canonical-property"></a><span data-ttu-id="fcf39-103">Propiedad canónica PidTagSwappedToDoData</span><span class="sxs-lookup"><span data-stu-id="fcf39-103">PidTagSwappedToDoData Canonical Property</span></span>

  
  
<span data-ttu-id="fcf39-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcf39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcf39-105">Mantiene un segundo conjunto de valores de propiedad que no afectan al estado marcado del objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="fcf39-105">Maintains a second set of property values that do not affect the flagged state of the Message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fcf39-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fcf39-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fcf39-107">PR_SWAPPED_TODO_DATA</span><span class="sxs-lookup"><span data-stu-id="fcf39-107">PR_SWAPPED_TODO_DATA</span></span>  <br/> |
|<span data-ttu-id="fcf39-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fcf39-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fcf39-109">0x0E2D</span><span class="sxs-lookup"><span data-stu-id="fcf39-109">0x0E2D</span></span>  <br/> |
|<span data-ttu-id="fcf39-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fcf39-110">Data type:</span></span>  <br/> |<span data-ttu-id="fcf39-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fcf39-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fcf39-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fcf39-112">Area:</span></span>  <br/> |<span data-ttu-id="fcf39-113">MAPI no transmitible</span><span class="sxs-lookup"><span data-stu-id="fcf39-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fcf39-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fcf39-114">Remarks</span></span>

<span data-ttu-id="fcf39-115">Actuando como ubicación de almacenamiento de marca secundaria si se admiten marcas de remitente o avisos de remitente, esta estructura proporciona una ubicación en la que se almacenan todas las propiedades relacionadas con el protocolo de marcado inFormativo que son compatibles con las marcas de remitente y todos los propiedades relacionadas con el protocolo de configuración de avisos que se admiten en los avisos del remitente sin exponer la información de aviso de remitente o de remitente a los destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="fcf39-115">Acting as the secondary flag storage location if sender flags or sender reminders are supported, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in sender flags, and all properties relating to the Reminder Settings Protocol that are supported in sender reminders without exposing the sender flag or sender reminder information to the recipients of a message.</span></span>
  
<span data-ttu-id="fcf39-116">De forma similar, esta estructura proporciona una ubicación en la que se almacenan todas las propiedades relacionadas con el protocolo de marcado inFormativo que se admiten en las propiedades y marcas de destinatarios relacionadas con el protocolo de configuración de avisos que se admiten en el destinatario. avisos de un mensaje enviado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="fcf39-116">Similarly, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in recipient flags and properties relating to the Reminder Settings Protocol that are supported in recipient reminders on a previously sent message.</span></span>
  
<span data-ttu-id="fcf39-117">Para obtener más información acerca de esta propiedad, consulte [[ms-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="fcf39-117">For more information about this property, see [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fcf39-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fcf39-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fcf39-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="fcf39-119">Protocol specifications</span></span>

<span data-ttu-id="fcf39-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fcf39-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fcf39-121">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="fcf39-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fcf39-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fcf39-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fcf39-123">Especifica las propiedades y operaciones relacionadas con la marcación.</span><span class="sxs-lookup"><span data-stu-id="fcf39-123">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="fcf39-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fcf39-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fcf39-125">Especifica las propiedades y el modelo de interacción para el correo electrónico y otros recordatorios de objetos.</span><span class="sxs-lookup"><span data-stu-id="fcf39-125">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fcf39-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fcf39-126">Header files</span></span>

<span data-ttu-id="fcf39-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="fcf39-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="fcf39-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fcf39-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="fcf39-129">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="fcf39-129">Mapitags.h</span></span>
  
> <span data-ttu-id="fcf39-130">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="fcf39-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fcf39-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="fcf39-131">See also</span></span>



[<span data-ttu-id="fcf39-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fcf39-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fcf39-133">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="fcf39-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fcf39-134">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="fcf39-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fcf39-135">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="fcf39-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

