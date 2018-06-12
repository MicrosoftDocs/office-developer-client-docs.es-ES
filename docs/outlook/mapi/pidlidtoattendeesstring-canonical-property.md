---
title: Propiedad canónico PidLidToAttendeesString
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: c4daa46bf7c40f717f2bcd4a9ea87195f3d2c81f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819023"
---
# <a name="pidlidtoattendeesstring-canonical-property"></a><span data-ttu-id="577e6-103">Propiedad canónico PidLidToAttendeesString</span><span class="sxs-lookup"><span data-stu-id="577e6-103">PidLidToAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="577e6-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="577e6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="577e6-105">Contiene una lista de todos los asistentes que se puedan enviar que también son los asistentes necesarios.</span><span class="sxs-lookup"><span data-stu-id="577e6-105">Contains a list of all the sendable attendees who are also required attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="577e6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="577e6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="577e6-107">dispidToAttendeesString</span><span class="sxs-lookup"><span data-stu-id="577e6-107">dispidToAttendeesString</span></span>  <br/> |
|<span data-ttu-id="577e6-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="577e6-108">Property set:</span></span>  <br/> |<span data-ttu-id="577e6-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="577e6-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="577e6-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="577e6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="577e6-111">0x0000823B</span><span class="sxs-lookup"><span data-stu-id="577e6-111">0x0000823B</span></span>  <br/> |
|<span data-ttu-id="577e6-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="577e6-112">Data type:</span></span>  <br/> |<span data-ttu-id="577e6-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="577e6-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="577e6-114">Área:</span><span class="sxs-lookup"><span data-stu-id="577e6-114">Area:</span></span>  <br/> |<span data-ttu-id="577e6-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="577e6-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="577e6-116">Notas</span><span class="sxs-lookup"><span data-stu-id="577e6-116">Remarks</span></span>

<span data-ttu-id="577e6-117">El valor para cada asistente es la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de la libreta de direcciones del asistente.</span><span class="sxs-lookup"><span data-stu-id="577e6-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="577e6-118">Entradas independientes deben estar delimitadas por un punto y coma seguido de un espacio.</span><span class="sxs-lookup"><span data-stu-id="577e6-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="577e6-119">Esta propiedad no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="577e6-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="577e6-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="577e6-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="577e6-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="577e6-121">Protocol specifications</span></span>

<span data-ttu-id="577e6-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="577e6-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="577e6-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="577e6-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="577e6-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="577e6-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="577e6-125">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="577e6-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="577e6-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="577e6-126">Header files</span></span>

<span data-ttu-id="577e6-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="577e6-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="577e6-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="577e6-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="577e6-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="577e6-129">See also</span></span>



[<span data-ttu-id="577e6-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="577e6-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="577e6-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="577e6-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="577e6-132">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="577e6-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="577e6-133">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="577e6-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

