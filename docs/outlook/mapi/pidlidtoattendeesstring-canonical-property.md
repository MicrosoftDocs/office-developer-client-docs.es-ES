---
title: Propiedad canónica PidLidToAttendeesString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToAttendeesString
api_type:
- COM
ms.assetid: ca1eedba-c617-4403-8490-315ab75f2edb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ea0cd256b025ae519272f32522bebbe6e9e17b5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339818"
---
# <a name="pidlidtoattendeesstring-canonical-property"></a><span data-ttu-id="321ce-103">Propiedad canónica PidLidToAttendeesString</span><span class="sxs-lookup"><span data-stu-id="321ce-103">PidLidToAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="321ce-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="321ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="321ce-105">Contiene una lista de todos los asistentes que se pueden enviar y que también son asistentes necesarios.</span><span class="sxs-lookup"><span data-stu-id="321ce-105">Contains a list of all the sendable attendees who are also required attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="321ce-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="321ce-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="321ce-107">dispidToAttendeesString</span><span class="sxs-lookup"><span data-stu-id="321ce-107">dispidToAttendeesString</span></span>  <br/> |
|<span data-ttu-id="321ce-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="321ce-108">Property set:</span></span>  <br/> |<span data-ttu-id="321ce-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="321ce-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="321ce-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="321ce-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="321ce-111">0x0000823B</span><span class="sxs-lookup"><span data-stu-id="321ce-111">0x0000823B</span></span>  <br/> |
|<span data-ttu-id="321ce-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="321ce-112">Data type:</span></span>  <br/> |<span data-ttu-id="321ce-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="321ce-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="321ce-114">Área:</span><span class="sxs-lookup"><span data-stu-id="321ce-114">Area:</span></span>  <br/> |<span data-ttu-id="321ce-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="321ce-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="321ce-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="321ce-116">Remarks</span></span>

<span data-ttu-id="321ce-117">El valor de cada asistente es la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de la libreta de direcciones del asistente.</span><span class="sxs-lookup"><span data-stu-id="321ce-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="321ce-118">Las entradas independientes deben estar delimitadas por un punto y coma seguido de un espacio.</span><span class="sxs-lookup"><span data-stu-id="321ce-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="321ce-119">Esta propiedad no es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="321ce-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="321ce-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="321ce-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="321ce-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="321ce-121">Protocol specifications</span></span>

<span data-ttu-id="321ce-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="321ce-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="321ce-123">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="321ce-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="321ce-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="321ce-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="321ce-125">Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="321ce-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="321ce-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="321ce-126">Header files</span></span>

<span data-ttu-id="321ce-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="321ce-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="321ce-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="321ce-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="321ce-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="321ce-129">See also</span></span>



[<span data-ttu-id="321ce-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="321ce-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="321ce-131">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="321ce-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="321ce-132">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="321ce-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="321ce-133">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="321ce-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

