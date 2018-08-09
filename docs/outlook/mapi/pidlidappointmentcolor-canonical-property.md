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
ms.openlocfilehash: 251377a7b9118437aff3fbb6b2b9376cbf70375c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818471"
---
# <a name="pidlidappointmentcolor-canonical-property"></a><span data-ttu-id="8bb12-103">Propiedad canónica PidLidAppointmentColor</span><span class="sxs-lookup"><span data-stu-id="8bb12-103">PidLidAppointmentColor Canonical Property</span></span>

  
  
<span data-ttu-id="8bb12-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8bb12-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8bb12-105">Especifica el color para utilizarla al mostrar el calendario.</span><span class="sxs-lookup"><span data-stu-id="8bb12-105">Specifies the color to use when displaying the calendar.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8bb12-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8bb12-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8bb12-107">dispidApptColor</span><span class="sxs-lookup"><span data-stu-id="8bb12-107">dispidApptColor</span></span>  <br/> |
|<span data-ttu-id="8bb12-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="8bb12-108">Property set:</span></span>  <br/> |<span data-ttu-id="8bb12-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="8bb12-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="8bb12-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="8bb12-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8bb12-111">0x00008214</span><span class="sxs-lookup"><span data-stu-id="8bb12-111">0x00008214</span></span>  <br/> |
|<span data-ttu-id="8bb12-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8bb12-112">Data type:</span></span>  <br/> |<span data-ttu-id="8bb12-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8bb12-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8bb12-114">Área:</span><span class="sxs-lookup"><span data-stu-id="8bb12-114">Area:</span></span>  <br/> |<span data-ttu-id="8bb12-115">Calendario</span><span class="sxs-lookup"><span data-stu-id="8bb12-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8bb12-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8bb12-116">Remarks</span></span>

<span data-ttu-id="8bb12-117">Esta propiedad especifica el color para utilizarla al mostrar el calendario.</span><span class="sxs-lookup"><span data-stu-id="8bb12-117">This property specifies the color to use when displaying the calendar.</span></span> <span data-ttu-id="8bb12-118">Un cliente o servidor debe establecer este valor para la compatibilidad con versiones anteriores con los clientes más antiguos.</span><span class="sxs-lookup"><span data-stu-id="8bb12-118">A client or server should set this value for backward compatibility with older clients.</span></span> <span data-ttu-id="8bb12-119">En su lugar, puede mostrar el calendario en función del valor de la propiedad **palabras clave** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) como especifica en [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8bb12-119">It may instead display the calendar based on the value of the **Keywords** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) property as specified in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span> <span data-ttu-id="8bb12-120">Cuando se establece, el valor debe ser uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="8bb12-120">When set, the value must be one of the following.</span></span>
  
|<span data-ttu-id="8bb12-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8bb12-121">**Value**</span></span>|<span data-ttu-id="8bb12-122">**Color**</span><span class="sxs-lookup"><span data-stu-id="8bb12-122">**Color**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8bb12-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8bb12-123">0x00000000</span></span>  <br/> |<span data-ttu-id="8bb12-124">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8bb12-124">None</span></span>  <br/> |
|<span data-ttu-id="8bb12-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8bb12-125">0x00000001</span></span>  <br/> |<span data-ttu-id="8bb12-126">Rojo</span><span class="sxs-lookup"><span data-stu-id="8bb12-126">Red</span></span>  <br/> |
|<span data-ttu-id="8bb12-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="8bb12-127">0x00000002</span></span>  <br/> |<span data-ttu-id="8bb12-128">Azul</span><span class="sxs-lookup"><span data-stu-id="8bb12-128">Blue</span></span>  <br/> |
|<span data-ttu-id="8bb12-129">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="8bb12-129">0x00000003</span></span>  <br/> |<span data-ttu-id="8bb12-130">Verde</span><span class="sxs-lookup"><span data-stu-id="8bb12-130">Green</span></span>  <br/> |
|<span data-ttu-id="8bb12-131">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="8bb12-131">0x00000004</span></span>  <br/> |<span data-ttu-id="8bb12-132">Gris</span><span class="sxs-lookup"><span data-stu-id="8bb12-132">Grey</span></span>  <br/> |
|<span data-ttu-id="8bb12-133">0 x 00000005</span><span class="sxs-lookup"><span data-stu-id="8bb12-133">0x00000005</span></span>  <br/> |<span data-ttu-id="8bb12-134">Naranja</span><span class="sxs-lookup"><span data-stu-id="8bb12-134">Orange</span></span>  <br/> |
|<span data-ttu-id="8bb12-135">0 x 00000006</span><span class="sxs-lookup"><span data-stu-id="8bb12-135">0x00000006</span></span>  <br/> |<span data-ttu-id="8bb12-136">Cian</span><span class="sxs-lookup"><span data-stu-id="8bb12-136">Cyan</span></span>  <br/> |
|<span data-ttu-id="8bb12-137">0 x 00000007</span><span class="sxs-lookup"><span data-stu-id="8bb12-137">0x00000007</span></span>  <br/> |<span data-ttu-id="8bb12-138">Oliva</span><span class="sxs-lookup"><span data-stu-id="8bb12-138">Olive</span></span>  <br/> |
|<span data-ttu-id="8bb12-139">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="8bb12-139">0x00000008</span></span>  <br/> |<span data-ttu-id="8bb12-140">Púrpura</span><span class="sxs-lookup"><span data-stu-id="8bb12-140">Purple</span></span>  <br/> |
|<span data-ttu-id="8bb12-141">0 x 00000009</span><span class="sxs-lookup"><span data-stu-id="8bb12-141">0x00000009</span></span>  <br/> |<span data-ttu-id="8bb12-142">Verde azulado</span><span class="sxs-lookup"><span data-stu-id="8bb12-142">Teal</span></span>  <br/> |
|<span data-ttu-id="8bb12-143">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="8bb12-143">0x0000000A</span></span>  <br/> |<span data-ttu-id="8bb12-144">Amarillo</span><span class="sxs-lookup"><span data-stu-id="8bb12-144">Yellow</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="8bb12-145">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8bb12-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8bb12-146">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="8bb12-146">Protocol specifications</span></span>

<span data-ttu-id="8bb12-147">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bb12-147">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bb12-148">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8bb12-148">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8bb12-149">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bb12-149">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bb12-150">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="8bb12-150">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8bb12-151">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8bb12-151">Header files</span></span>

<span data-ttu-id="8bb12-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8bb12-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="8bb12-153">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8bb12-153">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8bb12-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="8bb12-154">See also</span></span>



[<span data-ttu-id="8bb12-155">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8bb12-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8bb12-156">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="8bb12-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8bb12-157">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8bb12-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8bb12-158">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="8bb12-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

