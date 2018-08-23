---
title: Propiedad canónica PidLidIsException
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsException
api_type:
- COM
ms.assetid: 802321fb-4261-4c3e-9de3-8b4f490dae13
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b1d4600810d4f773896f1880b7309c1f818c7dc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575780"
---
# <a name="pidlidisexception-canonical-property"></a><span data-ttu-id="70f76-103">Propiedad canónica PidLidIsException</span><span class="sxs-lookup"><span data-stu-id="70f76-103">PidLidIsException Canonical Property</span></span>

  
  
<span data-ttu-id="70f76-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70f76-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70f76-105">Indica que el objeto que representa una excepción (incluida una instancia huérfana).</span><span class="sxs-lookup"><span data-stu-id="70f76-105">Indicates that the object that represents an exception (including an orphan instance).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="70f76-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="70f76-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="70f76-107">LID_IS_EXCEPTION</span><span class="sxs-lookup"><span data-stu-id="70f76-107">LID_IS_EXCEPTION</span></span>  <br/> |
|<span data-ttu-id="70f76-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="70f76-108">Property set:</span></span>  <br/> |<span data-ttu-id="70f76-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="70f76-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="70f76-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="70f76-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="70f76-111">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="70f76-111">0x0000000A</span></span>  <br/> |
|<span data-ttu-id="70f76-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="70f76-112">Data type:</span></span>  <br/> |<span data-ttu-id="70f76-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="70f76-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="70f76-114">Área:</span><span class="sxs-lookup"><span data-stu-id="70f76-114">Area:</span></span>  <br/> |<span data-ttu-id="70f76-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="70f76-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70f76-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="70f76-116">Remarks</span></span>

<span data-ttu-id="70f76-117">Un valor de FALSE indica que el objeto que representa una sola instancia o una serie periódica.</span><span class="sxs-lookup"><span data-stu-id="70f76-117">A value of FALSE indicates that the object that represents a recurring series or a single instance.</span></span> <span data-ttu-id="70f76-118">La ausencia de esta propiedad para cualquier objeto indica un valor FALSE, excepto el mensaje incrustado de excepción, que se supone un valor de TRUE.</span><span class="sxs-lookup"><span data-stu-id="70f76-118">The absence of this property for any object indicates a value of FALSE except for the exception embedded message, which assumes a value of TRUE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="70f76-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="70f76-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="70f76-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="70f76-120">Protocol specifications</span></span>

<span data-ttu-id="70f76-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70f76-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70f76-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="70f76-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="70f76-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70f76-123">[[MS-OXOCAL] ](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70f76-124">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="70f76-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="70f76-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="70f76-125">Header files</span></span>

<span data-ttu-id="70f76-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="70f76-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="70f76-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="70f76-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="70f76-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="70f76-128">See also</span></span>



[<span data-ttu-id="70f76-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="70f76-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="70f76-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="70f76-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="70f76-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="70f76-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="70f76-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="70f76-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

