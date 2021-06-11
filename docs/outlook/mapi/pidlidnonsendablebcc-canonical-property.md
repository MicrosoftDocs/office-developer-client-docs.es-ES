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
# <a name="pidlidnonsendablebcc-canonical-property"></a><span data-ttu-id="e27f9-103">Propiedad canónica PidLidNonSendableBcc</span><span class="sxs-lookup"><span data-stu-id="e27f9-103">PidLidNonSendableBcc Canonical Property</span></span>

  
  
<span data-ttu-id="e27f9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e27f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e27f9-105">Contiene una lista de todos los asistentes insendibles que son recursos.</span><span class="sxs-lookup"><span data-stu-id="e27f9-105">Contains a list of all the unsendable attendees who are resources.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e27f9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e27f9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e27f9-107">dispidNonSendableBCC</span><span class="sxs-lookup"><span data-stu-id="e27f9-107">dispidNonSendableBCC</span></span>  <br/> |
|<span data-ttu-id="e27f9-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="e27f9-108">Property set:</span></span>  <br/> |<span data-ttu-id="e27f9-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="e27f9-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="e27f9-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="e27f9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e27f9-111">0x00008538</span><span class="sxs-lookup"><span data-stu-id="e27f9-111">0x00008538</span></span>  <br/> |
|<span data-ttu-id="e27f9-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e27f9-112">Data type:</span></span>  <br/> |<span data-ttu-id="e27f9-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e27f9-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e27f9-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e27f9-114">Area:</span></span>  <br/> |<span data-ttu-id="e27f9-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="e27f9-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e27f9-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e27f9-116">Remarks</span></span>

<span data-ttu-id="e27f9-117">El valor de cada asistente es **la propiedad PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de la libreta de direcciones del asistente.</span><span class="sxs-lookup"><span data-stu-id="e27f9-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="e27f9-118">Las entradas independientes deben delimitarse por un punto y coma seguido de un espacio.</span><span class="sxs-lookup"><span data-stu-id="e27f9-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="e27f9-119">Esta propiedad no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="e27f9-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e27f9-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e27f9-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e27f9-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="e27f9-121">Protocol specifications</span></span>

<span data-ttu-id="e27f9-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e27f9-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e27f9-123">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="e27f9-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e27f9-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e27f9-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e27f9-125">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="e27f9-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="e27f9-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e27f9-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e27f9-127">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="e27f9-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e27f9-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e27f9-128">Header files</span></span>

<span data-ttu-id="e27f9-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e27f9-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="e27f9-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e27f9-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e27f9-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="e27f9-131">See also</span></span>



[<span data-ttu-id="e27f9-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e27f9-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e27f9-133">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="e27f9-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e27f9-134">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e27f9-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e27f9-135">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="e27f9-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

