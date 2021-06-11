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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327464"
---
# <a name="pidlidfexceptionalbody-canonical-property"></a><span data-ttu-id="46098-103">Propiedad canónica PidLidFExceptionalBody</span><span class="sxs-lookup"><span data-stu-id="46098-103">PidLidFExceptionalBody Canonical Property</span></span>

  
  
<span data-ttu-id="46098-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46098-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46098-105">Indica que el objeto de mensaje incrustado de excepción tiene un cuerpo que difiere del objeto de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="46098-105">Indicates that the exception embedded message object has a body that differs from the recurring calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="46098-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="46098-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="46098-107">dispidFExceptionalBody</span><span class="sxs-lookup"><span data-stu-id="46098-107">dispidFExceptionalBody</span></span>  <br/> |
|<span data-ttu-id="46098-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="46098-108">Property set:</span></span>  <br/> |<span data-ttu-id="46098-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="46098-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="46098-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="46098-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="46098-111">0x00008206</span><span class="sxs-lookup"><span data-stu-id="46098-111">0x00008206</span></span>  <br/> |
|<span data-ttu-id="46098-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="46098-112">Data type:</span></span>  <br/> |<span data-ttu-id="46098-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="46098-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="46098-114">Área:</span><span class="sxs-lookup"><span data-stu-id="46098-114">Area:</span></span>  <br/> |<span data-ttu-id="46098-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="46098-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46098-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="46098-116">Remarks</span></span>

<span data-ttu-id="46098-117">Si el valor de esta propiedad es TRUE, el objeto de mensaje incrustado de excepción debe tener un cuerpo.</span><span class="sxs-lookup"><span data-stu-id="46098-117">If the value of this property is TRUE, then the exception embedded message object must have a body.</span></span> <span data-ttu-id="46098-118">Si el valor de esta propiedad es FALSE o si la propiedad no existe, un cliente o servidor debe obtener el cuerpo del objeto de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="46098-118">If the value of this property is FALSE, or if the property does not exist, then a client or server must obtain the body from the recurring calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="46098-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="46098-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="46098-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="46098-120">Protocol specifications</span></span>

<span data-ttu-id="46098-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46098-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46098-122">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="46098-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="46098-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46098-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46098-124">Especifica las propiedades y las operaciones de los mensajes de cita, solicitud de reunión y respuesta.</span><span class="sxs-lookup"><span data-stu-id="46098-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="46098-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="46098-125">Header files</span></span>

<span data-ttu-id="46098-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="46098-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="46098-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="46098-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="46098-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="46098-128">See also</span></span>



[<span data-ttu-id="46098-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="46098-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="46098-130">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="46098-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="46098-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="46098-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="46098-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="46098-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

