---
title: Propiedad canónico PidLidNonSendableTo
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 297d9047944388afcf75b9645d76eb2670841ba8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818809"
---
# <a name="pidlidnonsendableto-canonical-property"></a><span data-ttu-id="235f3-103">Propiedad canónico PidLidNonSendableTo</span><span class="sxs-lookup"><span data-stu-id="235f3-103">PidLidNonSendableTo Canonical Property</span></span>

  
  
<span data-ttu-id="235f3-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="235f3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="235f3-105">Contiene una lista de todos los asistentes compuestas que también son los asistentes necesarios.</span><span class="sxs-lookup"><span data-stu-id="235f3-105">Contains a list of all the unsendable attendees who are also required attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="235f3-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="235f3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="235f3-107">dispidNonSendableTo</span><span class="sxs-lookup"><span data-stu-id="235f3-107">dispidNonSendableTo</span></span>  <br/> |
|<span data-ttu-id="235f3-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="235f3-108">Property set:</span></span>  <br/> |<span data-ttu-id="235f3-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="235f3-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="235f3-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="235f3-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="235f3-111">0x00008536</span><span class="sxs-lookup"><span data-stu-id="235f3-111">0x00008536</span></span>  <br/> |
|<span data-ttu-id="235f3-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="235f3-112">Data type:</span></span>  <br/> |<span data-ttu-id="235f3-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="235f3-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="235f3-114">Área:</span><span class="sxs-lookup"><span data-stu-id="235f3-114">Area:</span></span>  <br/> |<span data-ttu-id="235f3-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="235f3-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="235f3-116">Notas</span><span class="sxs-lookup"><span data-stu-id="235f3-116">Remarks</span></span>

<span data-ttu-id="235f3-117">El valor para cada asistente es la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de la libreta de direcciones del asistente.</span><span class="sxs-lookup"><span data-stu-id="235f3-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="235f3-118">Entradas independientes deben estar delimitadas por un punto y coma seguido de un espacio.</span><span class="sxs-lookup"><span data-stu-id="235f3-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="235f3-119">Esta propiedad no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="235f3-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="235f3-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="235f3-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="235f3-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="235f3-121">Protocol specifications</span></span>

<span data-ttu-id="235f3-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="235f3-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="235f3-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="235f3-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="235f3-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="235f3-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="235f3-125">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="235f3-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="235f3-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="235f3-126">Header files</span></span>

<span data-ttu-id="235f3-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="235f3-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="235f3-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="235f3-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="235f3-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="235f3-129">See also</span></span>



[<span data-ttu-id="235f3-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="235f3-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="235f3-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="235f3-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="235f3-132">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="235f3-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="235f3-133">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="235f3-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

