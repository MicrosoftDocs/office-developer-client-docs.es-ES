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
ms.openlocfilehash: 20ffc6f7f4d21f980e5f0f387464430ba187192a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359902"
---
# <a name="pidtagdelegateflags-canonical-property"></a><span data-ttu-id="18acf-103">Propiedad canónica PidTagDelegateFlags</span><span class="sxs-lookup"><span data-stu-id="18acf-103">PidTagDelegateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="18acf-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18acf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18acf-105">Especifica si un delegado puede ver los objetos de mensaje privados del delegado.</span><span class="sxs-lookup"><span data-stu-id="18acf-105">Specifies whether a delegate can view the delegator's private message objects.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="18acf-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="18acf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="18acf-107">PR_DELEGATE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="18acf-107">PR_DELEGATE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="18acf-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="18acf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="18acf-109">0x686B</span><span class="sxs-lookup"><span data-stu-id="18acf-109">0x686B</span></span>  <br/> |
|<span data-ttu-id="18acf-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="18acf-110">Data type:</span></span>  <br/> |<span data-ttu-id="18acf-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="18acf-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="18acf-112">Área:</span><span class="sxs-lookup"><span data-stu-id="18acf-112">Area:</span></span>  <br/> |<span data-ttu-id="18acf-113">Transmitible definida por la clase message</span><span class="sxs-lookup"><span data-stu-id="18acf-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18acf-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="18acf-114">Remarks</span></span>

<span data-ttu-id="18acf-115">Cada entrada de esta propiedad debe establecerse en uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="18acf-115">Each entry of this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="18acf-116">**Flag**</span><span class="sxs-lookup"><span data-stu-id="18acf-116">**Flag**</span></span>|<span data-ttu-id="18acf-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="18acf-117">**Value**</span></span>|<span data-ttu-id="18acf-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="18acf-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="18acf-119">HidePrivate</span><span class="sxs-lookup"><span data-stu-id="18acf-119">HidePrivate</span></span>  <br/> |<span data-ttu-id="18acf-120">0</span><span class="sxs-lookup"><span data-stu-id="18acf-120">0</span></span>  <br/> |<span data-ttu-id="18acf-121">No se debe permitir que el delegado vea objetos de mensaje privados.</span><span class="sxs-lookup"><span data-stu-id="18acf-121">The delegate should not be allowed to view private message objects.</span></span>  <br/> |
|<span data-ttu-id="18acf-122">ShowPrivate</span><span class="sxs-lookup"><span data-stu-id="18acf-122">ShowPrivate</span></span>  <br/> |<span data-ttu-id="18acf-123">1</span><span class="sxs-lookup"><span data-stu-id="18acf-123">1</span></span>  <br/> |<span data-ttu-id="18acf-124">El delegado debe tener permiso para ver objetos de mensaje privados.</span><span class="sxs-lookup"><span data-stu-id="18acf-124">The delegate should be allowed to view private message objects.</span></span>  <br/> |
   
<span data-ttu-id="18acf-125">Esta propiedad debe establecerse en el objeto de información de delegado.</span><span class="sxs-lookup"><span data-stu-id="18acf-125">This property must be set in the delegate information object.</span></span> <span data-ttu-id="18acf-126">El valor de "ShowPrivate" indica que el delegado desea que los objetos de mensaje privados sean visibles.</span><span class="sxs-lookup"><span data-stu-id="18acf-126">The value of "ShowPrivate" indicates that the delegator wants to make private message objects visible.</span></span> <span data-ttu-id="18acf-127">Esta preferencia se aplica a todas las carpetas para las que el delegado tiene un rol de revisor, autor o editor.</span><span class="sxs-lookup"><span data-stu-id="18acf-127">This preference is applicable to all folders for which the delegate has a role of reviewer, author, or editor.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="18acf-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="18acf-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="18acf-129">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="18acf-129">Protocol specifications</span></span>

<span data-ttu-id="18acf-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18acf-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18acf-131">Especifica métodos para conectarse y configurar buzones como delegados e interacciones con objetos de mensaje y calendario cuando actúan en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="18acf-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="18acf-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="18acf-132">Header files</span></span>

<span data-ttu-id="18acf-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="18acf-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="18acf-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="18acf-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="18acf-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="18acf-135">Mapitags.h</span></span>
  
> <span data-ttu-id="18acf-136">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="18acf-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18acf-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="18acf-137">See also</span></span>



[<span data-ttu-id="18acf-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="18acf-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="18acf-139">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="18acf-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="18acf-140">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="18acf-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="18acf-141">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="18acf-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

