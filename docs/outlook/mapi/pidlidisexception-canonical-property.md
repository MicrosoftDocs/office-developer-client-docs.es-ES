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
ms.openlocfilehash: 18dfa8a5936902afe0272274f7a48d01b28f94f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315452"
---
# <a name="pidlidisexception-canonical-property"></a><span data-ttu-id="2f043-103">Propiedad canónica PidLidIsException</span><span class="sxs-lookup"><span data-stu-id="2f043-103">PidLidIsException Canonical Property</span></span>

  
  
<span data-ttu-id="2f043-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f043-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f043-105">Indica que el objeto que representa una excepción (incluida una instancia huérfana).</span><span class="sxs-lookup"><span data-stu-id="2f043-105">Indicates that the object that represents an exception (including an orphan instance).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2f043-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2f043-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2f043-107">LID_IS_EXCEPTION</span><span class="sxs-lookup"><span data-stu-id="2f043-107">LID_IS_EXCEPTION</span></span>  <br/> |
|<span data-ttu-id="2f043-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="2f043-108">Property set:</span></span>  <br/> |<span data-ttu-id="2f043-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="2f043-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="2f043-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="2f043-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2f043-111">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="2f043-111">0x0000000A</span></span>  <br/> |
|<span data-ttu-id="2f043-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2f043-112">Data type:</span></span>  <br/> |<span data-ttu-id="2f043-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="2f043-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="2f043-114">Área:</span><span class="sxs-lookup"><span data-stu-id="2f043-114">Area:</span></span>  <br/> |<span data-ttu-id="2f043-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="2f043-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f043-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2f043-116">Remarks</span></span>

<span data-ttu-id="2f043-117">Un valor FALSE indica que el objeto que representa una serie periódica o una instancia única.</span><span class="sxs-lookup"><span data-stu-id="2f043-117">A value of FALSE indicates that the object that represents a recurring series or a single instance.</span></span> <span data-ttu-id="2f043-118">La ausencia de esta propiedad para cualquier objeto indica un valor FALSE excepto para el mensaje incrustado de excepción, que supone un valor TRUE.</span><span class="sxs-lookup"><span data-stu-id="2f043-118">The absence of this property for any object indicates a value of FALSE except for the exception embedded message, which assumes a value of TRUE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2f043-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2f043-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2f043-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="2f043-120">Protocol specifications</span></span>

<span data-ttu-id="2f043-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f043-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f043-122">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="2f043-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2f043-123">[[MS-OXOCAL] ](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f043-123">[[MS-OXOCAL] ](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f043-124">Especifica las propiedades y las operaciones de los mensajes de cita, de reunión y de respuesta.</span><span class="sxs-lookup"><span data-stu-id="2f043-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2f043-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2f043-125">Header files</span></span>

<span data-ttu-id="2f043-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2f043-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="2f043-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2f043-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2f043-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2f043-128">See also</span></span>



[<span data-ttu-id="2f043-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2f043-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2f043-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="2f043-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2f043-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2f043-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2f043-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="2f043-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

