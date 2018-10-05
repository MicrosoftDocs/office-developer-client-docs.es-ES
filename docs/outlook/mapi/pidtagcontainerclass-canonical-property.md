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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400260"
---
# <a name="pidtagcontainerclass-canonical-property"></a><span data-ttu-id="4cbe3-103">Propiedad canónica PidTagContainerClass</span><span class="sxs-lookup"><span data-stu-id="4cbe3-103">PidTagContainerClass Canonical Property</span></span>

  
  
<span data-ttu-id="4cbe3-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cbe3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cbe3-105">Contiene una cadena de texto que describe el tipo de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="4cbe3-105">Contains a text string describing the type of a folder.</span></span> <span data-ttu-id="4cbe3-106">Aunque esta propiedad se omite por lo general, las versiones de Microsoft® Exchange Server antes de administrador de buzones de Exchange Server 2003 esperan que esta propiedad esté presente.</span><span class="sxs-lookup"><span data-stu-id="4cbe3-106">Although this property is generally ignored, versions of Microsoft® Exchange Server prior to Exchange Server 2003 Mailbox Manager expect this property to be present.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4cbe3-107">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4cbe3-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="4cbe3-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="4cbe3-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="4cbe3-109">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4cbe3-109">Identifier:</span></span>  <br/> |<span data-ttu-id="4cbe3-110">0x3613</span><span class="sxs-lookup"><span data-stu-id="4cbe3-110">0x3613</span></span>  <br/> |
|<span data-ttu-id="4cbe3-111">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4cbe3-111">Data type:</span></span>  <br/> |<span data-ttu-id="4cbe3-112">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4cbe3-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4cbe3-113">Área:</span><span class="sxs-lookup"><span data-stu-id="4cbe3-113">Area:</span></span>  <br/> |<span data-ttu-id="4cbe3-114">Container</span><span class="sxs-lookup"><span data-stu-id="4cbe3-114">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4cbe3-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4cbe3-115">Remarks</span></span>

<span data-ttu-id="4cbe3-116">Estas propiedades no se usan normalmente por Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4cbe3-116">These properties are not normally used by Exchange Server.</span></span> <span data-ttu-id="4cbe3-117">Sin embargo, Microsoft Office Outlook® adjunta a las carpetas de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="4cbe3-117">However, Microsoft Office Outlook® attaches them to mailbox folders.</span></span> <span data-ttu-id="4cbe3-118">Además, las versiones de Exchange Server antes de administrador de buzones de Exchange Server 2003 incorrectamente podrían controlar las carpetas que no tengan estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4cbe3-118">In addition, versions of Exchange Server prior to Exchange Server 2003 Mailbox Manager might incorrectly handle folders that do not have these properties.</span></span>
  
<span data-ttu-id="4cbe3-119">Estas propiedades se pueden asignar los valores de cadena en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="4cbe3-119">These properties can be assigned the string values in the following table.</span></span>
  
|<span data-ttu-id="4cbe3-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4cbe3-120">**Value**</span></span>|<span data-ttu-id="4cbe3-121">**Contenido de carpeta**</span><span class="sxs-lookup"><span data-stu-id="4cbe3-121">**Contents of Folder**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4cbe3-122">IPF. Cita</span><span class="sxs-lookup"><span data-stu-id="4cbe3-122">IPF.Appointment</span></span>  <br/> |<span data-ttu-id="4cbe3-123">Citas</span><span class="sxs-lookup"><span data-stu-id="4cbe3-123">Appointments</span></span>  <br/> |
|<span data-ttu-id="4cbe3-124">IPF. Contacto</span><span class="sxs-lookup"><span data-stu-id="4cbe3-124">IPF.Contact</span></span>  <br/> |<span data-ttu-id="4cbe3-125">Contactos</span><span class="sxs-lookup"><span data-stu-id="4cbe3-125">Contacts</span></span>  <br/> |
|<span data-ttu-id="4cbe3-126">IPF. Diario</span><span class="sxs-lookup"><span data-stu-id="4cbe3-126">IPF.Journal</span></span>  <br/> |<span data-ttu-id="4cbe3-127">Entradas de diario de Outlook</span><span class="sxs-lookup"><span data-stu-id="4cbe3-127">Outlook Journal entries</span></span>  <br/> |
|<span data-ttu-id="4cbe3-128">IPF. Nota</span><span class="sxs-lookup"><span data-stu-id="4cbe3-128">IPF.Note</span></span>  <br/> |<span data-ttu-id="4cbe3-129">Los mensajes de correo y notas</span><span class="sxs-lookup"><span data-stu-id="4cbe3-129">Mail Messages and notes</span></span>  <br/> |
|<span data-ttu-id="4cbe3-130">IPF. Nota rápida</span><span class="sxs-lookup"><span data-stu-id="4cbe3-130">IPF.StickyNote</span></span>  <br/> |<span data-ttu-id="4cbe3-131">Notas rápidas de Outlook</span><span class="sxs-lookup"><span data-stu-id="4cbe3-131">Outlook Sticky Notes</span></span>  <br/> |
|<span data-ttu-id="4cbe3-132">IPF. Tarea</span><span class="sxs-lookup"><span data-stu-id="4cbe3-132">IPF.Task</span></span>  <br/> |<span data-ttu-id="4cbe3-133">Tareas de Outlook</span><span class="sxs-lookup"><span data-stu-id="4cbe3-133">Outlook Tasks</span></span>  <br/> |
   
<span data-ttu-id="4cbe3-134">Para las carpetas que contienen los mensajes de correo, estas propiedades deben establecerse en IPF. Tenga en cuenta.</span><span class="sxs-lookup"><span data-stu-id="4cbe3-134">For folders that contain mail messages, these properties should be set to IPF.Note.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4cbe3-135">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4cbe3-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4cbe3-136">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="4cbe3-136">Protocol specifications</span></span>

<span data-ttu-id="4cbe3-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4cbe3-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4cbe3-138">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="4cbe3-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4cbe3-139">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4cbe3-139">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4cbe3-140">Especifica las propiedades y operaciones para la creación y la ubicación de las carpetas especiales en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="4cbe3-140">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="4cbe3-141">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4cbe3-141">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4cbe3-142">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="4cbe3-142">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="4cbe3-143">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4cbe3-143">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4cbe3-144">Especifica las propiedades y operaciones que se permiten para el contacto y objetos de lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="4cbe3-144">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4cbe3-145">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4cbe3-145">Header files</span></span>

<span data-ttu-id="4cbe3-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4cbe3-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="4cbe3-147">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4cbe3-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="4cbe3-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4cbe3-148">Mapitags.h</span></span>
  
> <span data-ttu-id="4cbe3-149">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="4cbe3-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4cbe3-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="4cbe3-150">See also</span></span>



[<span data-ttu-id="4cbe3-151">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4cbe3-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4cbe3-152">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="4cbe3-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4cbe3-153">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4cbe3-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4cbe3-154">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="4cbe3-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

