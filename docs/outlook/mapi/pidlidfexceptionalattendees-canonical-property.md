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
# <a name="pidlidfexceptionalattendees-canonical-property"></a><span data-ttu-id="8b1cd-103">Propiedad canónica PidLidFExceptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="8b1cd-103">PidLidFExceptionalAttendees Canonical Property</span></span>

  
  
<span data-ttu-id="8b1cd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b1cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b1cd-105">Indica si esta propiedad es un objeto periódico Calendar con una o más excepciones y al menos uno de los mensajes incrustados de excepción tiene al menos un RecipientRow.</span><span class="sxs-lookup"><span data-stu-id="8b1cd-105">Indicates whether this property is a recurring calendar object with one or more exceptions, and at least one of the exception embedded messages has at least one RecipientRow.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8b1cd-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8b1cd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8b1cd-107">dispidFExceptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="8b1cd-107">dispidFExceptionalAttendees</span></span>  <br/> |
|<span data-ttu-id="8b1cd-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="8b1cd-108">Property set:</span></span>  <br/> |<span data-ttu-id="8b1cd-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="8b1cd-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="8b1cd-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="8b1cd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8b1cd-111">0x0000822B</span><span class="sxs-lookup"><span data-stu-id="8b1cd-111">0x0000822B</span></span>  <br/> |
|<span data-ttu-id="8b1cd-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8b1cd-112">Data type:</span></span>  <br/> |<span data-ttu-id="8b1cd-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="8b1cd-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="8b1cd-114">Área:</span><span class="sxs-lookup"><span data-stu-id="8b1cd-114">Area:</span></span>  <br/> |<span data-ttu-id="8b1cd-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="8b1cd-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b1cd-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8b1cd-116">Remarks</span></span>

<span data-ttu-id="8b1cd-117">Un valor de FALSE o la ausencia de esta propiedad indica que el objeto de calendario no tiene excepciones o que ninguno de los mensajes incrustados de la excepción tiene RecipientRows.</span><span class="sxs-lookup"><span data-stu-id="8b1cd-117">A value of FALSE, or the absence of this property, indicates that the calendar object either has no exceptions, or none of the exception embedded messages has RecipientRows.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8b1cd-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8b1cd-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8b1cd-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="8b1cd-119">Protocol specifications</span></span>

<span data-ttu-id="8b1cd-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b1cd-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b1cd-121">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8b1cd-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8b1cd-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b1cd-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b1cd-123">Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="8b1cd-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8b1cd-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8b1cd-124">Header files</span></span>

<span data-ttu-id="8b1cd-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8b1cd-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8b1cd-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8b1cd-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b1cd-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b1cd-127">See also</span></span>



[<span data-ttu-id="8b1cd-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8b1cd-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8b1cd-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="8b1cd-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8b1cd-130">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8b1cd-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8b1cd-131">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="8b1cd-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

