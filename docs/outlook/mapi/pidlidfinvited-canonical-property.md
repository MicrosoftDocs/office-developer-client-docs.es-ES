---
title: Propiedad canónica PidLidFInvited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFInvited
api_type:
- COM
ms.assetid: ca1ea5ec-20d5-4b70-95de-c2246a10beae
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3c2ddb5da9202e9cf0d1c78da1c1ad085ef9687c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357802"
---
# <a name="pidlidfinvited-canonical-property"></a><span data-ttu-id="c51a6-103">Propiedad canónica PidLidFInvited</span><span class="sxs-lookup"><span data-stu-id="c51a6-103">PidLidFInvited Canonical Property</span></span>

  
  
<span data-ttu-id="c51a6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c51a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c51a6-105">Indica si se han enviado o no invitaciones para la reunión que representa esta reunión.</span><span class="sxs-lookup"><span data-stu-id="c51a6-105">Indicates whether or not invitations have been sent for the meeting that this meeting represents.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c51a6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c51a6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c51a6-107">dispidFInvited</span><span class="sxs-lookup"><span data-stu-id="c51a6-107">dispidFInvited</span></span>  <br/> |
|<span data-ttu-id="c51a6-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="c51a6-108">Property set:</span></span>  <br/> |<span data-ttu-id="c51a6-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="c51a6-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="c51a6-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="c51a6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c51a6-111">0x00008229</span><span class="sxs-lookup"><span data-stu-id="c51a6-111">0x00008229</span></span>  <br/> |
|<span data-ttu-id="c51a6-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c51a6-112">Data type:</span></span>  <br/> |<span data-ttu-id="c51a6-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c51a6-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c51a6-114">Área:</span><span class="sxs-lookup"><span data-stu-id="c51a6-114">Area:</span></span>  <br/> |<span data-ttu-id="c51a6-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="c51a6-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c51a6-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c51a6-116">Remarks</span></span>

<span data-ttu-id="c51a6-117">Un valor de FALSE, o la ausencia de esta propiedad, indica que nunca se ha enviado una solicitud de reunión.</span><span class="sxs-lookup"><span data-stu-id="c51a6-117">A value of FALSE, or the absence of this property, indicates that a meeting request has never been sent.</span></span> <span data-ttu-id="c51a6-118">Un valor de TRUE indica que se ha enviado una solicitud de reunión.</span><span class="sxs-lookup"><span data-stu-id="c51a6-118">A value of TRUE indicates that a meeting request has been sent.</span></span> <span data-ttu-id="c51a6-119">Una vez que este valor se establece en TRUE en una reunión, no se debe cambiar.</span><span class="sxs-lookup"><span data-stu-id="c51a6-119">Once this value is set to TRUE on a meeting, it must not be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c51a6-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c51a6-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c51a6-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="c51a6-121">Protocol specifications</span></span>

<span data-ttu-id="c51a6-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c51a6-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c51a6-123">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="c51a6-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c51a6-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c51a6-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c51a6-125">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="c51a6-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c51a6-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c51a6-126">Header files</span></span>

<span data-ttu-id="c51a6-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c51a6-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="c51a6-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c51a6-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c51a6-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c51a6-129">See also</span></span>



[<span data-ttu-id="c51a6-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c51a6-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c51a6-131">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="c51a6-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c51a6-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c51a6-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c51a6-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="c51a6-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

