---
title: Propiedad canónica PidLidFExceptionalBody
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFExceptionalBody
api_type:
- COM
ms.assetid: 327516e8-ed3f-40fc-9604-03a70aecef5a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 93eb98aee19ea3f46a4e01e2c80150c3efe893a5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393904"
---
# <a name="pidlidfexceptionalbody-canonical-property"></a><span data-ttu-id="f5b53-103">Propiedad canónica PidLidFExceptionalBody</span><span class="sxs-lookup"><span data-stu-id="f5b53-103">PidLidFExceptionalBody Canonical Property</span></span>

  
  
<span data-ttu-id="f5b53-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5b53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5b53-105">Indica que el mensaje objeto tiene un cuerpo que difiere del objeto calendar periódica de incrustado de la excepción.</span><span class="sxs-lookup"><span data-stu-id="f5b53-105">Indicates that the exception embedded message object has a body that differs from the recurring calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f5b53-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f5b53-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f5b53-107">dispidFExceptionalBody</span><span class="sxs-lookup"><span data-stu-id="f5b53-107">dispidFExceptionalBody</span></span>  <br/> |
|<span data-ttu-id="f5b53-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="f5b53-108">Property set:</span></span>  <br/> |<span data-ttu-id="f5b53-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="f5b53-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="f5b53-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="f5b53-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f5b53-111">0x00008206</span><span class="sxs-lookup"><span data-stu-id="f5b53-111">0x00008206</span></span>  <br/> |
|<span data-ttu-id="f5b53-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f5b53-112">Data type:</span></span>  <br/> |<span data-ttu-id="f5b53-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f5b53-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f5b53-114">Área:</span><span class="sxs-lookup"><span data-stu-id="f5b53-114">Area:</span></span>  <br/> |<span data-ttu-id="f5b53-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="f5b53-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5b53-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f5b53-116">Remarks</span></span>

<span data-ttu-id="f5b53-117">Si el valor de esta propiedad es TRUE, la excepción incrustados objeto debe tener un cuerpo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="f5b53-117">If the value of this property is TRUE, then the exception embedded message object must have a body.</span></span> <span data-ttu-id="f5b53-118">Si el valor de esta propiedad es FALSE, o si la propiedad no existe, un cliente o servidor debe obtener el cuerpo desde el objeto de calendario periódica.</span><span class="sxs-lookup"><span data-stu-id="f5b53-118">If the value of this property is FALSE, or if the property does not exist, then a client or server must obtain the body from the recurring calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f5b53-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5b53-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f5b53-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f5b53-120">Protocol specifications</span></span>

<span data-ttu-id="f5b53-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5b53-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5b53-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f5b53-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f5b53-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5b53-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5b53-124">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="f5b53-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f5b53-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f5b53-125">Header files</span></span>

<span data-ttu-id="f5b53-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f5b53-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f5b53-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f5b53-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f5b53-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5b53-128">See also</span></span>



[<span data-ttu-id="f5b53-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f5b53-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f5b53-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f5b53-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f5b53-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f5b53-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f5b53-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="f5b53-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

