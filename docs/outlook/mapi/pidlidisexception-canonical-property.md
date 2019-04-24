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
# <a name="pidlidisexception-canonical-property"></a><span data-ttu-id="55468-103">Propiedad canónica PidLidIsException</span><span class="sxs-lookup"><span data-stu-id="55468-103">PidLidIsException Canonical Property</span></span>

  
  
<span data-ttu-id="55468-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55468-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55468-105">Indica que el objeto que representa una excepción (incluida una instancia huérfana).</span><span class="sxs-lookup"><span data-stu-id="55468-105">Indicates that the object that represents an exception (including an orphan instance).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="55468-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="55468-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="55468-107">LID_IS_EXCEPTION</span><span class="sxs-lookup"><span data-stu-id="55468-107">LID_IS_EXCEPTION</span></span>  <br/> |
|<span data-ttu-id="55468-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="55468-108">Property set:</span></span>  <br/> |<span data-ttu-id="55468-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="55468-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="55468-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="55468-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="55468-111">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="55468-111">0x0000000A</span></span>  <br/> |
|<span data-ttu-id="55468-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="55468-112">Data type:</span></span>  <br/> |<span data-ttu-id="55468-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="55468-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="55468-114">Área:</span><span class="sxs-lookup"><span data-stu-id="55468-114">Area:</span></span>  <br/> |<span data-ttu-id="55468-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="55468-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55468-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="55468-116">Remarks</span></span>

<span data-ttu-id="55468-117">Un valor de FALSE indica que el objeto que representa una serie periódica o una instancia única.</span><span class="sxs-lookup"><span data-stu-id="55468-117">A value of FALSE indicates that the object that represents a recurring series or a single instance.</span></span> <span data-ttu-id="55468-118">La ausencia de esta propiedad para cualquier objeto indica un valor de FALSE excepto para el mensaje incrustado de la excepción, que asume el valor TRUE.</span><span class="sxs-lookup"><span data-stu-id="55468-118">The absence of this property for any object indicates a value of FALSE except for the exception embedded message, which assumes a value of TRUE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="55468-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="55468-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="55468-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="55468-120">Protocol specifications</span></span>

<span data-ttu-id="55468-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55468-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55468-122">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="55468-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="55468-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55468-123">[[MS-OXOCAL] ](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55468-124">Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="55468-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="55468-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="55468-125">Header files</span></span>

<span data-ttu-id="55468-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="55468-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="55468-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="55468-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="55468-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="55468-128">See also</span></span>



[<span data-ttu-id="55468-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="55468-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="55468-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="55468-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="55468-131">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="55468-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="55468-132">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="55468-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

