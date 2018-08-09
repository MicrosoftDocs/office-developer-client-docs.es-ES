---
title: Propiedad canónica PidLidFExceptionalAttendees
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFExceptionalAttendees
api_type:
- COM
ms.assetid: f1f489a3-e83a-4e96-bf9a-d98bc17d29f5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7c7f654d42df7856b0e69bf276a763ccd29d1d87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818715"
---
# <a name="pidlidfexceptionalattendees-canonical-property"></a><span data-ttu-id="f3aa9-103">Propiedad canónica PidLidFExceptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="f3aa9-103">PidLidFExceptionalAttendees Canonical Property</span></span>

  
  
<span data-ttu-id="f3aa9-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f3aa9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f3aa9-105">Indica si esta propiedad es un objeto de calendario periódicos con excepciones de uno o más y, al menos uno de los mensajes de excepción incrustado tiene al menos un RecipientRow.</span><span class="sxs-lookup"><span data-stu-id="f3aa9-105">Indicates whether this property is a recurring calendar object with one or more exceptions, and at least one of the exception embedded messages has at least one RecipientRow.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f3aa9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f3aa9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f3aa9-107">dispidFExceptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="f3aa9-107">dispidFExceptionalAttendees</span></span>  <br/> |
|<span data-ttu-id="f3aa9-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="f3aa9-108">Property set:</span></span>  <br/> |<span data-ttu-id="f3aa9-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="f3aa9-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="f3aa9-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="f3aa9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f3aa9-111">0x0000822B</span><span class="sxs-lookup"><span data-stu-id="f3aa9-111">0x0000822B</span></span>  <br/> |
|<span data-ttu-id="f3aa9-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f3aa9-112">Data type:</span></span>  <br/> |<span data-ttu-id="f3aa9-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f3aa9-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f3aa9-114">Área:</span><span class="sxs-lookup"><span data-stu-id="f3aa9-114">Area:</span></span>  <br/> |<span data-ttu-id="f3aa9-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="f3aa9-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3aa9-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f3aa9-116">Remarks</span></span>

<span data-ttu-id="f3aa9-117">Un valor de FALSE, o la ausencia de esta propiedad indica que el objeto de calendario ya sea no tiene excepciones, o ninguno de los mensajes de excepción incrustado tiene RecipientRows.</span><span class="sxs-lookup"><span data-stu-id="f3aa9-117">A value of FALSE, or the absence of this property, indicates that the calendar object either has no exceptions, or none of the exception embedded messages has RecipientRows.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f3aa9-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f3aa9-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f3aa9-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f3aa9-119">Protocol specifications</span></span>

<span data-ttu-id="f3aa9-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3aa9-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3aa9-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f3aa9-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f3aa9-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3aa9-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3aa9-123">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="f3aa9-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f3aa9-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f3aa9-124">Header files</span></span>

<span data-ttu-id="f3aa9-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f3aa9-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f3aa9-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f3aa9-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f3aa9-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3aa9-127">See also</span></span>



[<span data-ttu-id="f3aa9-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f3aa9-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f3aa9-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f3aa9-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f3aa9-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f3aa9-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f3aa9-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="f3aa9-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

