---
title: Propiedad canónica PidLidExceptionReplaceTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidExceptionReplaceTime
api_type:
- COM
ms.assetid: c3aae4f5-7f00-45bf-b007-370041ba360e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e28bde9571081d61b37f6939a991c11ddeb75a4c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566050"
---
# <a name="pidlidexceptionreplacetime-canonical-property"></a><span data-ttu-id="e0a94-103">Propiedad canónica PidLidExceptionReplaceTime</span><span class="sxs-lookup"><span data-stu-id="e0a94-103">PidLidExceptionReplaceTime Canonical Property</span></span>

  
  
<span data-ttu-id="e0a94-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0a94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0a94-105">Especifica la fecha y hora en el patrón de periodicidad que va a reemplazar la excepción.</span><span class="sxs-lookup"><span data-stu-id="e0a94-105">Specifies the date and time within the recurrence pattern that the exception will replace.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e0a94-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e0a94-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e0a94-107">dispidExceptionReplaceTime</span><span class="sxs-lookup"><span data-stu-id="e0a94-107">dispidExceptionReplaceTime</span></span>  <br/> |
|<span data-ttu-id="e0a94-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="e0a94-108">Property set:</span></span>  <br/> |<span data-ttu-id="e0a94-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="e0a94-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="e0a94-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="e0a94-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e0a94-111">0x00008228</span><span class="sxs-lookup"><span data-stu-id="e0a94-111">0x00008228</span></span>  <br/> |
|<span data-ttu-id="e0a94-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e0a94-112">Data type:</span></span>  <br/> |<span data-ttu-id="e0a94-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="e0a94-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="e0a94-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e0a94-114">Area:</span></span>  <br/> |<span data-ttu-id="e0a94-115">Calendario</span><span class="sxs-lookup"><span data-stu-id="e0a94-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0a94-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e0a94-116">Remarks</span></span>

<span data-ttu-id="e0a94-117">El valor debe especificarse en hora Universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="e0a94-117">The value must be specified in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="e0a94-118">Esta propiedad permite que el objeto de datos adjuntos de la excepción se encontrarán para una instancia determinada.</span><span class="sxs-lookup"><span data-stu-id="e0a94-118">This property allows the exception attachment object to be found for a particular instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e0a94-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e0a94-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e0a94-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e0a94-120">Protocol specifications</span></span>

<span data-ttu-id="e0a94-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0a94-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0a94-122">Proporciona definiciones de conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="e0a94-122">Provides property set definitions.</span></span>
    
<span data-ttu-id="e0a94-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e0a94-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e0a94-124">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="e0a94-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e0a94-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e0a94-125">Header files</span></span>

<span data-ttu-id="e0a94-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e0a94-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e0a94-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e0a94-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e0a94-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e0a94-128">See also</span></span>



[<span data-ttu-id="e0a94-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e0a94-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e0a94-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e0a94-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e0a94-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e0a94-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e0a94-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="e0a94-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

