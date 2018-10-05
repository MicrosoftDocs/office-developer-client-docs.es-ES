---
title: Propiedad canónica PidLidAppointmentColor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentColor
api_type:
- COM
ms.assetid: 91147e85-f440-4463-850b-efc9bdbd36d1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1ea0830a06f303da8243f927e4a07cc744951ca9
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399875"
---
# <a name="pidlidappointmentcolor-canonical-property"></a><span data-ttu-id="d7f68-103">Propiedad canónica PidLidAppointmentColor</span><span class="sxs-lookup"><span data-stu-id="d7f68-103">PidLidAppointmentColor Canonical Property</span></span>

  
  
<span data-ttu-id="d7f68-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7f68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7f68-105">Especifica el color para utilizarla al mostrar el calendario.</span><span class="sxs-lookup"><span data-stu-id="d7f68-105">Specifies the color to use when displaying the calendar.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d7f68-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d7f68-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d7f68-107">dispidApptColor</span><span class="sxs-lookup"><span data-stu-id="d7f68-107">dispidApptColor</span></span>  <br/> |
|<span data-ttu-id="d7f68-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="d7f68-108">Property set:</span></span>  <br/> |<span data-ttu-id="d7f68-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="d7f68-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="d7f68-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="d7f68-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d7f68-111">0x00008214</span><span class="sxs-lookup"><span data-stu-id="d7f68-111">0x00008214</span></span>  <br/> |
|<span data-ttu-id="d7f68-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d7f68-112">Data type:</span></span>  <br/> |<span data-ttu-id="d7f68-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d7f68-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d7f68-114">Área:</span><span class="sxs-lookup"><span data-stu-id="d7f68-114">Area:</span></span>  <br/> |<span data-ttu-id="d7f68-115">Calendario</span><span class="sxs-lookup"><span data-stu-id="d7f68-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7f68-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d7f68-116">Remarks</span></span>

<span data-ttu-id="d7f68-117">Esta propiedad especifica el color para utilizarla al mostrar el calendario.</span><span class="sxs-lookup"><span data-stu-id="d7f68-117">This property specifies the color to use when displaying the calendar.</span></span> <span data-ttu-id="d7f68-118">Un cliente o servidor debe establecer este valor para la compatibilidad con versiones anteriores con los clientes más antiguos.</span><span class="sxs-lookup"><span data-stu-id="d7f68-118">A client or server should set this value for backward compatibility with older clients.</span></span> <span data-ttu-id="d7f68-119">En su lugar, puede mostrar el calendario en función del valor de la propiedad **palabras clave** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) como especifica en [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d7f68-119">It may instead display the calendar based on the value of the **Keywords** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) property as specified in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span> <span data-ttu-id="d7f68-120">Cuando se establece, el valor debe ser uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="d7f68-120">When set, the value must be one of the following.</span></span>
  
|<span data-ttu-id="d7f68-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d7f68-121">**Value**</span></span>|<span data-ttu-id="d7f68-122">**Color**</span><span class="sxs-lookup"><span data-stu-id="d7f68-122">**Color**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d7f68-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7f68-123">0x00000000</span></span>  <br/> |<span data-ttu-id="d7f68-124">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d7f68-124">None</span></span>  <br/> |
|<span data-ttu-id="d7f68-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d7f68-125">0x00000001</span></span>  <br/> |<span data-ttu-id="d7f68-126">Rojo</span><span class="sxs-lookup"><span data-stu-id="d7f68-126">Red</span></span>  <br/> |
|<span data-ttu-id="d7f68-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d7f68-127">0x00000002</span></span>  <br/> |<span data-ttu-id="d7f68-128">Azul</span><span class="sxs-lookup"><span data-stu-id="d7f68-128">Blue</span></span>  <br/> |
|<span data-ttu-id="d7f68-129">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="d7f68-129">0x00000003</span></span>  <br/> |<span data-ttu-id="d7f68-130">Verde</span><span class="sxs-lookup"><span data-stu-id="d7f68-130">Green</span></span>  <br/> |
|<span data-ttu-id="d7f68-131">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="d7f68-131">0x00000004</span></span>  <br/> |<span data-ttu-id="d7f68-132">Gris</span><span class="sxs-lookup"><span data-stu-id="d7f68-132">Grey</span></span>  <br/> |
|<span data-ttu-id="d7f68-133">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="d7f68-133">0x00000005</span></span>  <br/> |<span data-ttu-id="d7f68-134">Naranja</span><span class="sxs-lookup"><span data-stu-id="d7f68-134">Orange</span></span>  <br/> |
|<span data-ttu-id="d7f68-135">0 x 00000006</span><span class="sxs-lookup"><span data-stu-id="d7f68-135">0x00000006</span></span>  <br/> |<span data-ttu-id="d7f68-136">Cian</span><span class="sxs-lookup"><span data-stu-id="d7f68-136">Cyan</span></span>  <br/> |
|<span data-ttu-id="d7f68-137">0 x 00000007</span><span class="sxs-lookup"><span data-stu-id="d7f68-137">0x00000007</span></span>  <br/> |<span data-ttu-id="d7f68-138">Oliva</span><span class="sxs-lookup"><span data-stu-id="d7f68-138">Olive</span></span>  <br/> |
|<span data-ttu-id="d7f68-139">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="d7f68-139">0x00000008</span></span>  <br/> |<span data-ttu-id="d7f68-140">Púrpura</span><span class="sxs-lookup"><span data-stu-id="d7f68-140">Purple</span></span>  <br/> |
|<span data-ttu-id="d7f68-141">0 x 00000009</span><span class="sxs-lookup"><span data-stu-id="d7f68-141">0x00000009</span></span>  <br/> |<span data-ttu-id="d7f68-142">Verde azulado</span><span class="sxs-lookup"><span data-stu-id="d7f68-142">Teal</span></span>  <br/> |
|<span data-ttu-id="d7f68-143">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="d7f68-143">0x0000000A</span></span>  <br/> |<span data-ttu-id="d7f68-144">Amarillo</span><span class="sxs-lookup"><span data-stu-id="d7f68-144">Yellow</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d7f68-145">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d7f68-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d7f68-146">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d7f68-146">Protocol specifications</span></span>

<span data-ttu-id="d7f68-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7f68-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7f68-148">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d7f68-148">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d7f68-149">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7f68-149">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7f68-150">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="d7f68-150">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d7f68-151">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d7f68-151">Header files</span></span>

<span data-ttu-id="d7f68-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d7f68-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="d7f68-153">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d7f68-153">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d7f68-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7f68-154">See also</span></span>



[<span data-ttu-id="d7f68-155">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d7f68-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d7f68-156">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d7f68-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d7f68-157">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d7f68-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d7f68-158">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="d7f68-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

