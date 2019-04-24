---
title: Propiedad canónica PidTagContainerClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerClass
api_type:
- HeaderDef
ms.assetid: db249e9e-f1f0-4b95-8cd9-daa7c53ddb32
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c5b80831607f473208ce987a720c7e80e44b6d80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283152"
---
# <a name="pidtagcontainerclass-canonical-property"></a><span data-ttu-id="7f894-103">Propiedad canónica PidTagContainerClass</span><span class="sxs-lookup"><span data-stu-id="7f894-103">PidTagContainerClass Canonical Property</span></span>

  
  
<span data-ttu-id="7f894-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f894-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f894-105">Contiene una cadena de texto que describe el tipo de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="7f894-105">Contains a text string describing the type of a folder.</span></span> <span data-ttu-id="7f894-106">Aunque esta propiedad suele omitirse, las versiones de Microsoft ® Exchange Server anteriores a Exchange Server 2003 el administrador de buzones esperan que esta propiedad esté presente.</span><span class="sxs-lookup"><span data-stu-id="7f894-106">Although this property is generally ignored, versions of Microsoft® Exchange Server prior to Exchange Server 2003 Mailbox Manager expect this property to be present.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7f894-107">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7f894-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="7f894-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="7f894-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="7f894-109">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7f894-109">Identifier:</span></span>  <br/> |<span data-ttu-id="7f894-110">0x3613</span><span class="sxs-lookup"><span data-stu-id="7f894-110">0x3613</span></span>  <br/> |
|<span data-ttu-id="7f894-111">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7f894-111">Data type:</span></span>  <br/> |<span data-ttu-id="7f894-112">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7f894-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7f894-113">Área:</span><span class="sxs-lookup"><span data-stu-id="7f894-113">Area:</span></span>  <br/> |<span data-ttu-id="7f894-114">Container</span><span class="sxs-lookup"><span data-stu-id="7f894-114">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f894-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7f894-115">Remarks</span></span>

<span data-ttu-id="7f894-116">Normalmente, Exchange Server no usa estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7f894-116">These properties are not normally used by Exchange Server.</span></span> <span data-ttu-id="7f894-117">Sin embargo, Microsoft Office Outlook ® las adjunta a las carpetas del buzón.</span><span class="sxs-lookup"><span data-stu-id="7f894-117">However, Microsoft Office Outlook® attaches them to mailbox folders.</span></span> <span data-ttu-id="7f894-118">Además, las versiones de Exchange Server anteriores a Exchange Server 2003 el administrador de buzones podrían tratar incorrectamente las carpetas que no tienen estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7f894-118">In addition, versions of Exchange Server prior to Exchange Server 2003 Mailbox Manager might incorrectly handle folders that do not have these properties.</span></span>
  
<span data-ttu-id="7f894-119">A estas propiedades se les pueden asignar los valores de cadena de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="7f894-119">These properties can be assigned the string values in the following table.</span></span>
  
|<span data-ttu-id="7f894-120">**Value**</span><span class="sxs-lookup"><span data-stu-id="7f894-120">**Value**</span></span>|<span data-ttu-id="7f894-121">**Contenido de la carpeta**</span><span class="sxs-lookup"><span data-stu-id="7f894-121">**Contents of Folder**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7f894-122">Error. Convoca</span><span class="sxs-lookup"><span data-stu-id="7f894-122">IPF.Appointment</span></span>  <br/> |<span data-ttu-id="7f894-123">Citas</span><span class="sxs-lookup"><span data-stu-id="7f894-123">Appointments</span></span>  <br/> |
|<span data-ttu-id="7f894-124">Error. Contact</span><span class="sxs-lookup"><span data-stu-id="7f894-124">IPF.Contact</span></span>  <br/> |<span data-ttu-id="7f894-125">Contactos</span><span class="sxs-lookup"><span data-stu-id="7f894-125">Contacts</span></span>  <br/> |
|<span data-ttu-id="7f894-126">Error. Agenda</span><span class="sxs-lookup"><span data-stu-id="7f894-126">IPF.Journal</span></span>  <br/> |<span data-ttu-id="7f894-127">Entradas del diario de Outlook</span><span class="sxs-lookup"><span data-stu-id="7f894-127">Outlook Journal entries</span></span>  <br/> |
|<span data-ttu-id="7f894-128">Error. Note</span><span class="sxs-lookup"><span data-stu-id="7f894-128">IPF.Note</span></span>  <br/> |<span data-ttu-id="7f894-129">Notas y mensajes de correo</span><span class="sxs-lookup"><span data-stu-id="7f894-129">Mail Messages and notes</span></span>  <br/> |
|<span data-ttu-id="7f894-130">Error. StickyNote</span><span class="sxs-lookup"><span data-stu-id="7f894-130">IPF.StickyNote</span></span>  <br/> |<span data-ttu-id="7f894-131">Notas rápidas de Outlook</span><span class="sxs-lookup"><span data-stu-id="7f894-131">Outlook Sticky Notes</span></span>  <br/> |
|<span data-ttu-id="7f894-132">Error. Tareas</span><span class="sxs-lookup"><span data-stu-id="7f894-132">IPF.Task</span></span>  <br/> |<span data-ttu-id="7f894-133">Tareas de Outlook</span><span class="sxs-lookup"><span data-stu-id="7f894-133">Outlook Tasks</span></span>  <br/> |
   
<span data-ttu-id="7f894-134">Para las carpetas que contienen mensajes de correo, estas propiedades deben establecerse en IPF. Note.</span><span class="sxs-lookup"><span data-stu-id="7f894-134">For folders that contain mail messages, these properties should be set to IPF.Note.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7f894-135">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7f894-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7f894-136">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="7f894-136">Protocol specifications</span></span>

<span data-ttu-id="7f894-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f894-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f894-138">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="7f894-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7f894-139">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f894-139">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f894-140">Especifica las propiedades y operaciones para crear y ubicar las carpetas especiales en un buzón.</span><span class="sxs-lookup"><span data-stu-id="7f894-140">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="7f894-141">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f894-141">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f894-142">Especifica las propiedades y operaciones de la cita, la convocatoria de reunión y los mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="7f894-142">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="7f894-143">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f894-143">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f894-144">Especifica las propiedades y operaciones que se admiten para los objetos de contacto y de lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="7f894-144">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7f894-145">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7f894-145">Header files</span></span>

<span data-ttu-id="7f894-146">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7f894-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="7f894-147">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7f894-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="7f894-148">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="7f894-148">Mapitags.h</span></span>
  
> <span data-ttu-id="7f894-149">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="7f894-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f894-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f894-150">See also</span></span>



[<span data-ttu-id="7f894-151">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7f894-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7f894-152">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="7f894-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7f894-153">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7f894-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7f894-154">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="7f894-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

