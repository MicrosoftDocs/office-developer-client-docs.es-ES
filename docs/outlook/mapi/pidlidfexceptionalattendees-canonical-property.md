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
ms.openlocfilehash: 544b5b5ac945eeedf787af0e311491da1f9d0217
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327478"
---
# <a name="pidlidfexceptionalattendees-canonical-property"></a><span data-ttu-id="62be6-103">Propiedad canónica PidLidFExceptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="62be6-103">PidLidFExceptionalAttendees Canonical Property</span></span>

  
  
<span data-ttu-id="62be6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62be6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62be6-105">Indica si esta propiedad es un objeto de calendario periódico con una o más excepciones, y al menos uno de los mensajes incrustados de excepción tiene al menos un RecipientRow.</span><span class="sxs-lookup"><span data-stu-id="62be6-105">Indicates whether this property is a recurring calendar object with one or more exceptions, and at least one of the exception embedded messages has at least one RecipientRow.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="62be6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="62be6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="62be6-107">dispidFExceptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="62be6-107">dispidFExceptionalAttendees</span></span>  <br/> |
|<span data-ttu-id="62be6-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="62be6-108">Property set:</span></span>  <br/> |<span data-ttu-id="62be6-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="62be6-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="62be6-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="62be6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="62be6-111">0x0000822B</span><span class="sxs-lookup"><span data-stu-id="62be6-111">0x0000822B</span></span>  <br/> |
|<span data-ttu-id="62be6-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="62be6-112">Data type:</span></span>  <br/> |<span data-ttu-id="62be6-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="62be6-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="62be6-114">Área:</span><span class="sxs-lookup"><span data-stu-id="62be6-114">Area:</span></span>  <br/> |<span data-ttu-id="62be6-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="62be6-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62be6-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="62be6-116">Remarks</span></span>

<span data-ttu-id="62be6-117">Un valor de FALSE, o la ausencia de esta propiedad, indica que el objeto calendar no tiene excepciones o ninguno de los mensajes incrustados de excepción tiene RecipientRows.</span><span class="sxs-lookup"><span data-stu-id="62be6-117">A value of FALSE, or the absence of this property, indicates that the calendar object either has no exceptions, or none of the exception embedded messages has RecipientRows.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="62be6-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="62be6-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="62be6-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="62be6-119">Protocol specifications</span></span>

<span data-ttu-id="62be6-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62be6-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62be6-121">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="62be6-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="62be6-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62be6-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62be6-123">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="62be6-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="62be6-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="62be6-124">Header files</span></span>

<span data-ttu-id="62be6-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="62be6-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="62be6-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="62be6-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="62be6-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="62be6-127">See also</span></span>



[<span data-ttu-id="62be6-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="62be6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="62be6-129">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="62be6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="62be6-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="62be6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="62be6-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="62be6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

