---
title: Propiedad canónica PidTagDelegateFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDelegateFlags
api_type:
- HeaderDef
ms.assetid: 3a504594-204c-472c-8be7-dca154c94ea2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d43ec0bd2978c64e3a5ceb635f0dcda57de01cfd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590739"
---
# <a name="pidtagdelegateflags-canonical-property"></a><span data-ttu-id="6bcf9-103">Propiedad canónica PidTagDelegateFlags</span><span class="sxs-lookup"><span data-stu-id="6bcf9-103">PidTagDelegateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="6bcf9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6bcf9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6bcf9-105">Especifica si un delegado puede ver objetos de mensaje privado de la persona que delega.</span><span class="sxs-lookup"><span data-stu-id="6bcf9-105">Specifies whether a delegate can view the delegator's private message objects.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6bcf9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="6bcf9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6bcf9-107">PR_DELEGATE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="6bcf9-107">PR_DELEGATE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="6bcf9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6bcf9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6bcf9-109">0x686B</span><span class="sxs-lookup"><span data-stu-id="6bcf9-109">0x686B</span></span>  <br/> |
|<span data-ttu-id="6bcf9-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="6bcf9-110">Data type:</span></span>  <br/> |<span data-ttu-id="6bcf9-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="6bcf9-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="6bcf9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6bcf9-112">Area:</span></span>  <br/> |<span data-ttu-id="6bcf9-113">Mensaje definido por la clase transmisible</span><span class="sxs-lookup"><span data-stu-id="6bcf9-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6bcf9-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6bcf9-114">Remarks</span></span>

<span data-ttu-id="6bcf9-115">Cada entrada de esta propiedad debe establecerse en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="6bcf9-115">Each entry of this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="6bcf9-116">**Flag**</span><span class="sxs-lookup"><span data-stu-id="6bcf9-116">**Flag**</span></span>|<span data-ttu-id="6bcf9-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6bcf9-117">**Value**</span></span>|<span data-ttu-id="6bcf9-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6bcf9-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6bcf9-119">HidePrivate</span><span class="sxs-lookup"><span data-stu-id="6bcf9-119">HidePrivate</span></span>  <br/> |<span data-ttu-id="6bcf9-120">0</span><span class="sxs-lookup"><span data-stu-id="6bcf9-120">0</span></span>  <br/> |<span data-ttu-id="6bcf9-121">El delegado no deberían ver objetos de mensaje privado.</span><span class="sxs-lookup"><span data-stu-id="6bcf9-121">The delegate should not be allowed to view private message objects.</span></span>  <br/> |
|<span data-ttu-id="6bcf9-122">ShowPrivate</span><span class="sxs-lookup"><span data-stu-id="6bcf9-122">ShowPrivate</span></span>  <br/> |<span data-ttu-id="6bcf9-123">1</span><span class="sxs-lookup"><span data-stu-id="6bcf9-123">1</span></span>  <br/> |<span data-ttu-id="6bcf9-124">El delegado debe permitirse para ver objetos de mensaje privado.</span><span class="sxs-lookup"><span data-stu-id="6bcf9-124">The delegate should be allowed to view private message objects.</span></span>  <br/> |
   
<span data-ttu-id="6bcf9-125">Esta propiedad se debe establecer en el objeto de información de delegado.</span><span class="sxs-lookup"><span data-stu-id="6bcf9-125">This property must be set in the delegate information object.</span></span> <span data-ttu-id="6bcf9-126">El valor de "ShowPrivate" indica que el usuario delegado desea hacer que los objetos de mensaje privado que esté visible.</span><span class="sxs-lookup"><span data-stu-id="6bcf9-126">The value of "ShowPrivate" indicates that the delegator wants to make private message objects visible.</span></span> <span data-ttu-id="6bcf9-127">Esta preferencia es aplicable a todas las carpetas para los que el delegado tiene un rol de revisor, el autor o editor.</span><span class="sxs-lookup"><span data-stu-id="6bcf9-127">This preference is applicable to all folders for which the delegate has a role of reviewer, author, or editor.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6bcf9-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6bcf9-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6bcf9-129">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="6bcf9-129">Protocol specifications</span></span>

<span data-ttu-id="6bcf9-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6bcf9-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6bcf9-131">Especifica los métodos para conectarse a y configurar los buzones de correo como delegados y las interacciones con objetos de mensaje y calendario cuando actúen en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="6bcf9-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6bcf9-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="6bcf9-132">Header files</span></span>

<span data-ttu-id="6bcf9-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6bcf9-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="6bcf9-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="6bcf9-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="6bcf9-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6bcf9-135">Mapitags.h</span></span>
  
> <span data-ttu-id="6bcf9-136">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="6bcf9-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6bcf9-137">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="6bcf9-137">See also</span></span>



[<span data-ttu-id="6bcf9-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6bcf9-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6bcf9-139">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="6bcf9-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6bcf9-140">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="6bcf9-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6bcf9-141">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="6bcf9-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

