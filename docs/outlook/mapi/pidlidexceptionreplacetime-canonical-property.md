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
ms.openlocfilehash: b364fb91bda7e895b546f9a281ef14ce33b073f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337986"
---
# <a name="pidlidexceptionreplacetime-canonical-property"></a><span data-ttu-id="55ac1-103">Propiedad canónica PidLidExceptionReplaceTime</span><span class="sxs-lookup"><span data-stu-id="55ac1-103">PidLidExceptionReplaceTime Canonical Property</span></span>

  
  
<span data-ttu-id="55ac1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55ac1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55ac1-105">Especifica la fecha y la hora dentro del patrón de periodicidad que reemplazará la excepción.</span><span class="sxs-lookup"><span data-stu-id="55ac1-105">Specifies the date and time within the recurrence pattern that the exception will replace.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="55ac1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="55ac1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="55ac1-107">dispidExceptionReplaceTime</span><span class="sxs-lookup"><span data-stu-id="55ac1-107">dispidExceptionReplaceTime</span></span>  <br/> |
|<span data-ttu-id="55ac1-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="55ac1-108">Property set:</span></span>  <br/> |<span data-ttu-id="55ac1-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="55ac1-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="55ac1-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="55ac1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="55ac1-111">0x00008228</span><span class="sxs-lookup"><span data-stu-id="55ac1-111">0x00008228</span></span>  <br/> |
|<span data-ttu-id="55ac1-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="55ac1-112">Data type:</span></span>  <br/> |<span data-ttu-id="55ac1-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="55ac1-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="55ac1-114">Área:</span><span class="sxs-lookup"><span data-stu-id="55ac1-114">Area:</span></span>  <br/> |<span data-ttu-id="55ac1-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="55ac1-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55ac1-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="55ac1-116">Remarks</span></span>

<span data-ttu-id="55ac1-117">El valor debe especificarse en hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="55ac1-117">The value must be specified in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="55ac1-118">Esta propiedad permite encontrar el objeto de datos adjuntos de excepción para una instancia determinada.</span><span class="sxs-lookup"><span data-stu-id="55ac1-118">This property allows the exception attachment object to be found for a particular instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="55ac1-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="55ac1-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="55ac1-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="55ac1-120">Protocol specifications</span></span>

<span data-ttu-id="55ac1-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55ac1-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55ac1-122">Proporciona definiciones de conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="55ac1-122">Provides property set definitions.</span></span>
    
<span data-ttu-id="55ac1-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55ac1-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55ac1-124">Especifica las propiedades y las operaciones de los mensajes de cita, de reunión y de respuesta.</span><span class="sxs-lookup"><span data-stu-id="55ac1-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="55ac1-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="55ac1-125">Header files</span></span>

<span data-ttu-id="55ac1-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="55ac1-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="55ac1-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="55ac1-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="55ac1-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="55ac1-128">See also</span></span>



[<span data-ttu-id="55ac1-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="55ac1-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="55ac1-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="55ac1-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="55ac1-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="55ac1-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="55ac1-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="55ac1-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

