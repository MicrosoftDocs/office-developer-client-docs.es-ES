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
ms.openlocfilehash: f6707c49c70804aeb757119aa411ca4059e378eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356045"
---
# <a name="pidlidappointmentreplyname-canonical-property"></a><span data-ttu-id="747e4-103">Propiedad canónica PidLidAppointmentReplyName</span><span class="sxs-lookup"><span data-stu-id="747e4-103">PidLidAppointmentReplyName Canonical Property</span></span>

  
  
<span data-ttu-id="747e4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="747e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="747e4-105">Especifica el usuario que respondió por última vez a la solicitud de reunión o al objeto de actualización de reunión.</span><span class="sxs-lookup"><span data-stu-id="747e4-105">Specifies the user who last replied to the meeting request or meeting update object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="747e4-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="747e4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="747e4-107">dispidApptReplyName</span><span class="sxs-lookup"><span data-stu-id="747e4-107">dispidApptReplyName</span></span>  <br/> |
|<span data-ttu-id="747e4-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="747e4-108">Property set:</span></span>  <br/> |<span data-ttu-id="747e4-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="747e4-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="747e4-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="747e4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="747e4-111">0x00008230</span><span class="sxs-lookup"><span data-stu-id="747e4-111">0x00008230</span></span>  <br/> |
|<span data-ttu-id="747e4-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="747e4-112">Data type:</span></span>  <br/> |<span data-ttu-id="747e4-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="747e4-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="747e4-114">Área:</span><span class="sxs-lookup"><span data-stu-id="747e4-114">Area:</span></span>  <br/> |<span data-ttu-id="747e4-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="747e4-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="747e4-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="747e4-116">Remarks</span></span>

<span data-ttu-id="747e4-117">Esta propiedad solo se establece para un delegador cuando un delegado respondió.</span><span class="sxs-lookup"><span data-stu-id="747e4-117">This property is only set for a delegator when a delegate responded.</span></span> <span data-ttu-id="747e4-118">El valor es igual a la **propiedad PR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md)) del almacén del delegado.</span><span class="sxs-lookup"><span data-stu-id="747e4-118">The value is equal to the **PR_MAILBOX_OWNER_NAME** ([PidTagMailboxOwnerName](pidtagmailboxownername-canonical-property.md)) property for the delegate's store.</span></span> <span data-ttu-id="747e4-119">Esta propiedad no tiene ningún significado para el organizador.</span><span class="sxs-lookup"><span data-stu-id="747e4-119">This property has no meaning for the organizer.</span></span> <span data-ttu-id="747e4-120">Para obtener más **información PR_MAILBOX_OWNER_NAME**, vea el protocolo de objetos de almacén especificado en [[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="747e4-120">For details on **PR_MAILBOX_OWNER_NAME**, see store object protocol specified in [[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="747e4-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="747e4-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="747e4-122">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="747e4-122">Protocol specifications</span></span>

<span data-ttu-id="747e4-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="747e4-123">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="747e4-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="747e4-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="747e4-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="747e4-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="747e4-126">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="747e4-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="747e4-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="747e4-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="747e4-128">Especifica las propiedades y las operaciones de los mensajes de cita, de reunión y de respuesta.</span><span class="sxs-lookup"><span data-stu-id="747e4-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="747e4-129">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="747e4-129">Header files</span></span>

<span data-ttu-id="747e4-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="747e4-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="747e4-131">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="747e4-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="747e4-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="747e4-132">See also</span></span>



[<span data-ttu-id="747e4-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="747e4-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="747e4-134">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="747e4-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="747e4-135">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="747e4-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="747e4-136">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="747e4-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

