---
title: Propiedad canónica PidLidAppointmentReplyName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentReplyName
api_type:
- COM
ms.assetid: 2f3a44d1-600f-412e-bc89-078841db5308
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5b6d88b60f9f5c6a01a92ecc5905f711fbf3ab3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818529"
---
# <a name="pidlidappointmentreplyname-canonical-property"></a><span data-ttu-id="fb07d-103">Propiedad canónica PidLidAppointmentReplyName</span><span class="sxs-lookup"><span data-stu-id="fb07d-103">PidLidAppointmentReplyName Canonical Property</span></span>

  
  
<span data-ttu-id="fb07d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fb07d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fb07d-105">Especifica el usuario que modificó por última respondió a la convocatoria de reunión o reunión actualizar el objeto.</span><span class="sxs-lookup"><span data-stu-id="fb07d-105">Specifies the user who last replied to the meeting request or meeting update object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fb07d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fb07d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fb07d-107">dispidApptReplyName</span><span class="sxs-lookup"><span data-stu-id="fb07d-107">dispidApptReplyName</span></span>  <br/> |
|<span data-ttu-id="fb07d-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="fb07d-108">Property set:</span></span>  <br/> |<span data-ttu-id="fb07d-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="fb07d-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="fb07d-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="fb07d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fb07d-111">0x00008230</span><span class="sxs-lookup"><span data-stu-id="fb07d-111">0x00008230</span></span>  <br/> |
|<span data-ttu-id="fb07d-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fb07d-112">Data type:</span></span>  <br/> |<span data-ttu-id="fb07d-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fb07d-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fb07d-114">Área:</span><span class="sxs-lookup"><span data-stu-id="fb07d-114">Area:</span></span>  <br/> |<span data-ttu-id="fb07d-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="fb07d-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fb07d-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fb07d-116">Remarks</span></span>

<span data-ttu-id="fb07d-117">Esta propiedad sólo se establece para un usuario delegado cuando un delegado ha respondido.</span><span class="sxs-lookup"><span data-stu-id="fb07d-117">This property is only set for a delegator when a delegate responded.</span></span> <span data-ttu-id="fb07d-118">El valor es igual a la propiedad **PR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md)) para el almacenamiento del delegado.</span><span class="sxs-lookup"><span data-stu-id="fb07d-118">The value is equal to the **PR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md)) property for the delegate's store.</span></span> <span data-ttu-id="fb07d-119">Esta propiedad no tiene ningún significado para el organizador.</span><span class="sxs-lookup"><span data-stu-id="fb07d-119">This property has no meaning for the organizer.</span></span> <span data-ttu-id="fb07d-120">Para obtener información detallada en **PR_MAILBOX_OWNER_NAME**, vea almacenar protocolo de objeto que se especifica en [[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="fb07d-120">For details on **PR_MAILBOX_OWNER_NAME**, see store object protocol specified in [[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fb07d-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fb07d-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fb07d-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="fb07d-122">Protocol specifications</span></span>

<span data-ttu-id="fb07d-123">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb07d-123">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb07d-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fb07d-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="fb07d-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb07d-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb07d-126">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="fb07d-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fb07d-127">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb07d-127">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb07d-128">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="fb07d-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fb07d-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fb07d-129">Header files</span></span>

<span data-ttu-id="fb07d-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fb07d-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="fb07d-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fb07d-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fb07d-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb07d-132">See also</span></span>



[<span data-ttu-id="fb07d-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fb07d-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fb07d-134">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="fb07d-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fb07d-135">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="fb07d-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fb07d-136">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="fb07d-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

