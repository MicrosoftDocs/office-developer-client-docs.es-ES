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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345440"
---
# <a name="pidlidappointmentcolor-canonical-property"></a><span data-ttu-id="e3e63-103">Propiedad canónica PidLidAppointmentColor</span><span class="sxs-lookup"><span data-stu-id="e3e63-103">PidLidAppointmentColor Canonical Property</span></span>

  
  
<span data-ttu-id="e3e63-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3e63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3e63-105">Especifica el color que se va a usar al mostrar el calendario.</span><span class="sxs-lookup"><span data-stu-id="e3e63-105">Specifies the color to use when displaying the calendar.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e3e63-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e3e63-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e3e63-107">dispidApptColor</span><span class="sxs-lookup"><span data-stu-id="e3e63-107">dispidApptColor</span></span>  <br/> |
|<span data-ttu-id="e3e63-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="e3e63-108">Property set:</span></span>  <br/> |<span data-ttu-id="e3e63-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="e3e63-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="e3e63-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="e3e63-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e3e63-111">0x00008214</span><span class="sxs-lookup"><span data-stu-id="e3e63-111">0x00008214</span></span>  <br/> |
|<span data-ttu-id="e3e63-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e3e63-112">Data type:</span></span>  <br/> |<span data-ttu-id="e3e63-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e3e63-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e3e63-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e3e63-114">Area:</span></span>  <br/> |<span data-ttu-id="e3e63-115">Calendar</span><span class="sxs-lookup"><span data-stu-id="e3e63-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3e63-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e3e63-116">Remarks</span></span>

<span data-ttu-id="e3e63-117">Esta propiedad especifica el color que se va a usar al mostrar el calendario.</span><span class="sxs-lookup"><span data-stu-id="e3e63-117">This property specifies the color to use when displaying the calendar.</span></span> <span data-ttu-id="e3e63-118">Un cliente o un servidor debe establecer este valor para mantener la compatibilidad con los clientes más antiguos.</span><span class="sxs-lookup"><span data-stu-id="e3e63-118">A client or server should set this value for backward compatibility with older clients.</span></span> <span data-ttu-id="e3e63-119">En su lugar, puede mostrar el calendario en función del valor de \*\*\*\* la propiedad Keywords ([PidNameKeywords](pidnamekeywords-canonical-property.md)) tal como se especifica en [[ms-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e3e63-119">It may instead display the calendar based on the value of the **Keywords** ([PidNameKeywords](pidnamekeywords-canonical-property.md)) property as specified in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx).</span></span> <span data-ttu-id="e3e63-120">Cuando se establece, el valor debe ser uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="e3e63-120">When set, the value must be one of the following.</span></span>
  
|<span data-ttu-id="e3e63-121">**Value**</span><span class="sxs-lookup"><span data-stu-id="e3e63-121">**Value**</span></span>|<span data-ttu-id="e3e63-122">**Color**</span><span class="sxs-lookup"><span data-stu-id="e3e63-122">**Color**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e3e63-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3e63-123">0x00000000</span></span>  <br/> |<span data-ttu-id="e3e63-124">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e3e63-124">None</span></span>  <br/> |
|<span data-ttu-id="e3e63-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e3e63-125">0x00000001</span></span>  <br/> |<span data-ttu-id="e3e63-126">Rojo</span><span class="sxs-lookup"><span data-stu-id="e3e63-126">Red</span></span>  <br/> |
|<span data-ttu-id="e3e63-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e3e63-127">0x00000002</span></span>  <br/> |<span data-ttu-id="e3e63-128">Azul</span><span class="sxs-lookup"><span data-stu-id="e3e63-128">Blue</span></span>  <br/> |
|<span data-ttu-id="e3e63-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="e3e63-129">0x00000003</span></span>  <br/> |<span data-ttu-id="e3e63-130">Verde</span><span class="sxs-lookup"><span data-stu-id="e3e63-130">Green</span></span>  <br/> |
|<span data-ttu-id="e3e63-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="e3e63-131">0x00000004</span></span>  <br/> |<span data-ttu-id="e3e63-132">Gris</span><span class="sxs-lookup"><span data-stu-id="e3e63-132">Grey</span></span>  <br/> |
|<span data-ttu-id="e3e63-133">0x00000005</span><span class="sxs-lookup"><span data-stu-id="e3e63-133">0x00000005</span></span>  <br/> |<span data-ttu-id="e3e63-134">Anaranjado</span><span class="sxs-lookup"><span data-stu-id="e3e63-134">Orange</span></span>  <br/> |
|<span data-ttu-id="e3e63-135">0x00000006</span><span class="sxs-lookup"><span data-stu-id="e3e63-135">0x00000006</span></span>  <br/> |<span data-ttu-id="e3e63-136">Aguamarina</span><span class="sxs-lookup"><span data-stu-id="e3e63-136">Cyan</span></span>  <br/> |
|<span data-ttu-id="e3e63-137">0x00000007</span><span class="sxs-lookup"><span data-stu-id="e3e63-137">0x00000007</span></span>  <br/> |<span data-ttu-id="e3e63-138">Oliva</span><span class="sxs-lookup"><span data-stu-id="e3e63-138">Olive</span></span>  <br/> |
|<span data-ttu-id="e3e63-139">0x00000008</span><span class="sxs-lookup"><span data-stu-id="e3e63-139">0x00000008</span></span>  <br/> |<span data-ttu-id="e3e63-140">Púrpura</span><span class="sxs-lookup"><span data-stu-id="e3e63-140">Purple</span></span>  <br/> |
|<span data-ttu-id="e3e63-141">0x00000009</span><span class="sxs-lookup"><span data-stu-id="e3e63-141">0x00000009</span></span>  <br/> |<span data-ttu-id="e3e63-142">Verde azulado</span><span class="sxs-lookup"><span data-stu-id="e3e63-142">Teal</span></span>  <br/> |
|<span data-ttu-id="e3e63-143">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="e3e63-143">0x0000000A</span></span>  <br/> |<span data-ttu-id="e3e63-144">Amarillo</span><span class="sxs-lookup"><span data-stu-id="e3e63-144">Yellow</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e3e63-145">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e3e63-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e3e63-146">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e3e63-146">Protocol specifications</span></span>

<span data-ttu-id="e3e63-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3e63-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3e63-148">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e3e63-148">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e3e63-149">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3e63-149">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3e63-150">Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="e3e63-150">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e3e63-151">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e3e63-151">Header files</span></span>

<span data-ttu-id="e3e63-152">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e3e63-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="e3e63-153">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e3e63-153">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e3e63-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3e63-154">See also</span></span>



[<span data-ttu-id="e3e63-155">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e3e63-155">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e3e63-156">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="e3e63-156">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e3e63-157">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e3e63-157">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e3e63-158">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="e3e63-158">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

