---
title: Propiedad canónica PidLidNonSendableTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableTo
api_type:
- COM
ms.assetid: 90e14969-652b-422a-9b0a-ee99e58bc8d5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6cc510cb9a4a79f977cb6c9721921833441df23c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394095"
---
# <a name="pidlidnonsendableto-canonical-property"></a><span data-ttu-id="cb70a-103">Propiedad canónica PidLidNonSendableTo</span><span class="sxs-lookup"><span data-stu-id="cb70a-103">PidLidNonSendableTo Canonical Property</span></span>

  
  
<span data-ttu-id="cb70a-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb70a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb70a-105">Contiene una lista de todos los asistentes compuestas que también son los asistentes necesarios.</span><span class="sxs-lookup"><span data-stu-id="cb70a-105">Contains a list of all the unsendable attendees who are also required attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cb70a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="cb70a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cb70a-107">dispidNonSendableTo</span><span class="sxs-lookup"><span data-stu-id="cb70a-107">dispidNonSendableTo</span></span>  <br/> |
|<span data-ttu-id="cb70a-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="cb70a-108">Property set:</span></span>  <br/> |<span data-ttu-id="cb70a-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="cb70a-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="cb70a-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="cb70a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="cb70a-111">0x00008536</span><span class="sxs-lookup"><span data-stu-id="cb70a-111">0x00008536</span></span>  <br/> |
|<span data-ttu-id="cb70a-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="cb70a-112">Data type:</span></span>  <br/> |<span data-ttu-id="cb70a-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cb70a-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="cb70a-114">Área:</span><span class="sxs-lookup"><span data-stu-id="cb70a-114">Area:</span></span>  <br/> |<span data-ttu-id="cb70a-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="cb70a-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb70a-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cb70a-116">Remarks</span></span>

<span data-ttu-id="cb70a-117">El valor para cada asistente es la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de la libreta de direcciones del asistente.</span><span class="sxs-lookup"><span data-stu-id="cb70a-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="cb70a-118">Entradas independientes deben estar delimitadas por un punto y coma seguido de un espacio.</span><span class="sxs-lookup"><span data-stu-id="cb70a-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="cb70a-119">Esta propiedad no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="cb70a-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cb70a-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cb70a-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cb70a-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="cb70a-121">Protocol specifications</span></span>

<span data-ttu-id="cb70a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb70a-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb70a-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="cb70a-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cb70a-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb70a-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb70a-125">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="cb70a-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cb70a-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="cb70a-126">Header files</span></span>

<span data-ttu-id="cb70a-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cb70a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="cb70a-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="cb70a-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cb70a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb70a-129">See also</span></span>



[<span data-ttu-id="cb70a-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cb70a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cb70a-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="cb70a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cb70a-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="cb70a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cb70a-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="cb70a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

