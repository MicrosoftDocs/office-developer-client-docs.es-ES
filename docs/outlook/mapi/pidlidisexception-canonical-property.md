---
title: Propiedad canónico PidLidIsException
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 5a36cf21a36f83ec252923ddbb137b3b99456927
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818765"
---
# <a name="pidlidisexception-canonical-property"></a><span data-ttu-id="51e59-103">Propiedad canónico PidLidIsException</span><span class="sxs-lookup"><span data-stu-id="51e59-103">PidLidIsException Canonical Property</span></span>

  
  
<span data-ttu-id="51e59-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="51e59-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="51e59-105">Indica que el objeto que representa una excepción (incluida una instancia huérfana).</span><span class="sxs-lookup"><span data-stu-id="51e59-105">Indicates that the object that represents an exception (including an orphan instance).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="51e59-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="51e59-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="51e59-107">LID_IS_EXCEPTION</span><span class="sxs-lookup"><span data-stu-id="51e59-107">LID_IS_EXCEPTION</span></span>  <br/> |
|<span data-ttu-id="51e59-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="51e59-108">Property set:</span></span>  <br/> |<span data-ttu-id="51e59-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="51e59-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="51e59-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="51e59-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="51e59-111">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="51e59-111">0x0000000A</span></span>  <br/> |
|<span data-ttu-id="51e59-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="51e59-112">Data type:</span></span>  <br/> |<span data-ttu-id="51e59-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="51e59-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="51e59-114">Área:</span><span class="sxs-lookup"><span data-stu-id="51e59-114">Area:</span></span>  <br/> |<span data-ttu-id="51e59-115">Reuniones</span><span class="sxs-lookup"><span data-stu-id="51e59-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51e59-116">Notas</span><span class="sxs-lookup"><span data-stu-id="51e59-116">Remarks</span></span>

<span data-ttu-id="51e59-117">Un valor de FALSE indica que el objeto que representa una sola instancia o una serie periódica.</span><span class="sxs-lookup"><span data-stu-id="51e59-117">A value of FALSE indicates that the object that represents a recurring series or a single instance.</span></span> <span data-ttu-id="51e59-118">La ausencia de esta propiedad para cualquier objeto indica un valor FALSE, excepto el mensaje incrustado de excepción, que se supone un valor de TRUE.</span><span class="sxs-lookup"><span data-stu-id="51e59-118">The absence of this property for any object indicates a value of FALSE except for the exception embedded message, which assumes a value of TRUE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="51e59-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="51e59-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="51e59-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="51e59-120">Protocol specifications</span></span>

<span data-ttu-id="51e59-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51e59-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51e59-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="51e59-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="51e59-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51e59-123">[[MS-OXOCAL] ](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51e59-124">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="51e59-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="51e59-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="51e59-125">Header files</span></span>

<span data-ttu-id="51e59-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="51e59-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="51e59-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="51e59-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="51e59-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="51e59-128">See also</span></span>



[<span data-ttu-id="51e59-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="51e59-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="51e59-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="51e59-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="51e59-131">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="51e59-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="51e59-132">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="51e59-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

