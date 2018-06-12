---
title: Propiedad canónico PidTagDelegateFlags
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 160ddc53edf3d9681adf6f9d536a488c0c345a07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819419"
---
# <a name="pidtagdelegateflags-canonical-property"></a><span data-ttu-id="167fb-103">Propiedad canónico PidTagDelegateFlags</span><span class="sxs-lookup"><span data-stu-id="167fb-103">PidTagDelegateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="167fb-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="167fb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="167fb-105">Especifica si un delegado puede ver objetos de mensaje privado de la persona que delega.</span><span class="sxs-lookup"><span data-stu-id="167fb-105">Specifies whether a delegate can view the delegator's private message objects.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="167fb-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="167fb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="167fb-107">PR_DELEGATE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="167fb-107">PR_DELEGATE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="167fb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="167fb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="167fb-109">0x686B</span><span class="sxs-lookup"><span data-stu-id="167fb-109">0x686B</span></span>  <br/> |
|<span data-ttu-id="167fb-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="167fb-110">Data type:</span></span>  <br/> |<span data-ttu-id="167fb-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="167fb-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="167fb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="167fb-112">Area:</span></span>  <br/> |<span data-ttu-id="167fb-113">Mensaje definido por la clase transmisible</span><span class="sxs-lookup"><span data-stu-id="167fb-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="167fb-114">Notas</span><span class="sxs-lookup"><span data-stu-id="167fb-114">Remarks</span></span>

<span data-ttu-id="167fb-115">Cada entrada de esta propiedad debe establecerse en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="167fb-115">Each entry of this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="167fb-116">**Flag**</span><span class="sxs-lookup"><span data-stu-id="167fb-116">**Flag**</span></span>|<span data-ttu-id="167fb-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="167fb-117">**Value**</span></span>|<span data-ttu-id="167fb-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="167fb-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="167fb-119">HidePrivate</span><span class="sxs-lookup"><span data-stu-id="167fb-119">HidePrivate</span></span>  <br/> |<span data-ttu-id="167fb-120">0</span><span class="sxs-lookup"><span data-stu-id="167fb-120">0</span></span>  <br/> |<span data-ttu-id="167fb-121">El delegado no deberían ver objetos de mensaje privado.</span><span class="sxs-lookup"><span data-stu-id="167fb-121">The delegate should not be allowed to view private message objects.</span></span>  <br/> |
|<span data-ttu-id="167fb-122">ShowPrivate</span><span class="sxs-lookup"><span data-stu-id="167fb-122">ShowPrivate</span></span>  <br/> |<span data-ttu-id="167fb-123">1</span><span class="sxs-lookup"><span data-stu-id="167fb-123">1</span></span>  <br/> |<span data-ttu-id="167fb-124">El delegado debe permitirse para ver objetos de mensaje privado.</span><span class="sxs-lookup"><span data-stu-id="167fb-124">The delegate should be allowed to view private message objects.</span></span>  <br/> |
   
<span data-ttu-id="167fb-125">Esta propiedad se debe establecer en el objeto de información de delegado.</span><span class="sxs-lookup"><span data-stu-id="167fb-125">This property must be set in the delegate information object.</span></span> <span data-ttu-id="167fb-126">El valor de "ShowPrivate" indica que el usuario delegado desea hacer que los objetos de mensaje privado que esté visible.</span><span class="sxs-lookup"><span data-stu-id="167fb-126">The value of "ShowPrivate" indicates that the delegator wants to make private message objects visible.</span></span> <span data-ttu-id="167fb-127">Esta preferencia es aplicable a todas las carpetas para los que el delegado tiene un rol de revisor, el autor o editor.</span><span class="sxs-lookup"><span data-stu-id="167fb-127">This preference is applicable to all folders for which the delegate has a role of reviewer, author, or editor.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="167fb-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="167fb-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="167fb-129">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="167fb-129">Protocol specifications</span></span>

<span data-ttu-id="167fb-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="167fb-130">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="167fb-131">Especifica los métodos para conectarse a y configurar los buzones de correo como delegados y las interacciones con objetos de mensaje y calendario cuando actúen en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="167fb-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="167fb-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="167fb-132">Header files</span></span>

<span data-ttu-id="167fb-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="167fb-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="167fb-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="167fb-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="167fb-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="167fb-135">Mapitags.h</span></span>
  
> <span data-ttu-id="167fb-136">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="167fb-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="167fb-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="167fb-137">See also</span></span>



[<span data-ttu-id="167fb-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="167fb-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="167fb-139">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="167fb-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="167fb-140">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="167fb-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="167fb-141">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="167fb-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

