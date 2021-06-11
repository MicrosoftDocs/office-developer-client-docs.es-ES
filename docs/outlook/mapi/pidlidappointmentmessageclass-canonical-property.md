---
title: Propiedad canónica PidLidAppointmentMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentMessageClass
api_type:
- COM
ms.assetid: 8b8c8484-0cb4-4842-8b11-de42d97e0140
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7149ba5a4a0378951942df790003b6d09c1155f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358103"
---
# <a name="pidlidappointmentmessageclass-canonical-property"></a><span data-ttu-id="0b166-103">Propiedad canónica PidLidAppointmentMessageClass</span><span class="sxs-lookup"><span data-stu-id="0b166-103">PidLidAppointmentMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="0b166-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b166-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b166-105">Indica la **propiedad PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) de la reunión que se va a generar a partir de la solicitud de reunión.</span><span class="sxs-lookup"><span data-stu-id="0b166-105">Indicates the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the meeting that is to be generated from the meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0b166-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0b166-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0b166-107">dispidApptMessageClass</span><span class="sxs-lookup"><span data-stu-id="0b166-107">dispidApptMessageClass</span></span>  <br/> |
|<span data-ttu-id="0b166-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="0b166-108">Property set:</span></span>  <br/> |<span data-ttu-id="0b166-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="0b166-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="0b166-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="0b166-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0b166-111">0x00000024</span><span class="sxs-lookup"><span data-stu-id="0b166-111">0x00000024</span></span>  <br/> |
|<span data-ttu-id="0b166-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0b166-112">Data type:</span></span>  <br/> |<span data-ttu-id="0b166-113">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="0b166-113">PT_TSTRING</span></span>  <br/> |
|<span data-ttu-id="0b166-114">Área:</span><span class="sxs-lookup"><span data-stu-id="0b166-114">Area:</span></span>  <br/> |<span data-ttu-id="0b166-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="0b166-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b166-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0b166-116">Remarks</span></span>

<span data-ttu-id="0b166-117">El valor de esta propiedad debe ser "IPM. Appointment" o tener el prefijo "IPM. Cita.".</span><span class="sxs-lookup"><span data-stu-id="0b166-117">The value of this property must either be "IPM.Appointment" or be prefixed with "IPM.Appointment.".</span></span> <span data-ttu-id="0b166-118">Esta propiedad no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="0b166-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0b166-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0b166-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0b166-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="0b166-120">Protocol specifications</span></span>

<span data-ttu-id="0b166-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b166-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b166-122">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="0b166-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0b166-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b166-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b166-124">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="0b166-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0b166-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0b166-125">Header files</span></span>

<span data-ttu-id="0b166-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0b166-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="0b166-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0b166-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0b166-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b166-128">See also</span></span>



[<span data-ttu-id="0b166-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0b166-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0b166-130">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="0b166-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0b166-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0b166-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0b166-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="0b166-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

