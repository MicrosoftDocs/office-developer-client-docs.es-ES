---
title: Propiedad canónica PidLidNonSendableBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableBcc
api_type:
- COM
ms.assetid: c7523896-c391-443d-bd4e-cc13f3367f08
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7b7cfe1fc1068e5b5b228c4de4c9317d9bcbbc66
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328738"
---
# <a name="pidlidnonsendablebcc-canonical-property"></a><span data-ttu-id="48038-103">Propiedad canónica PidLidNonSendableBcc</span><span class="sxs-lookup"><span data-stu-id="48038-103">PidLidNonSendableBcc Canonical Property</span></span>

  
  
<span data-ttu-id="48038-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48038-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48038-105">Contiene una lista de todos los asistentes no enviados que son recursos.</span><span class="sxs-lookup"><span data-stu-id="48038-105">Contains a list of all the unsendable attendees who are resources.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="48038-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="48038-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="48038-107">dispidNonSendableBCC</span><span class="sxs-lookup"><span data-stu-id="48038-107">dispidNonSendableBCC</span></span>  <br/> |
|<span data-ttu-id="48038-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="48038-108">Property set:</span></span>  <br/> |<span data-ttu-id="48038-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="48038-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="48038-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="48038-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="48038-111">0x00008538</span><span class="sxs-lookup"><span data-stu-id="48038-111">0x00008538</span></span>  <br/> |
|<span data-ttu-id="48038-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="48038-112">Data type:</span></span>  <br/> |<span data-ttu-id="48038-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="48038-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="48038-114">Área:</span><span class="sxs-lookup"><span data-stu-id="48038-114">Area:</span></span>  <br/> |<span data-ttu-id="48038-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="48038-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48038-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="48038-116">Remarks</span></span>

<span data-ttu-id="48038-117">El valor de cada asistente es la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de la libreta de direcciones del asistente.</span><span class="sxs-lookup"><span data-stu-id="48038-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="48038-118">Las entradas independientes deben estar delimitadas por un punto y coma seguido de un espacio.</span><span class="sxs-lookup"><span data-stu-id="48038-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="48038-119">Esta propiedad no es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="48038-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="48038-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="48038-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="48038-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="48038-121">Protocol specifications</span></span>

<span data-ttu-id="48038-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48038-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48038-123">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="48038-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="48038-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48038-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48038-125">Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="48038-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="48038-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48038-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48038-127">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="48038-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="48038-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="48038-128">Header files</span></span>

<span data-ttu-id="48038-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="48038-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="48038-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="48038-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="48038-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="48038-131">See also</span></span>



[<span data-ttu-id="48038-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="48038-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="48038-133">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="48038-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="48038-134">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="48038-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="48038-135">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="48038-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

