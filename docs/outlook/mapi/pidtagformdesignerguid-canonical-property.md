---
title: Propiedad canónica PidTagFormDesignerGuid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFormDesignerGuid
api_type:
- HeaderDef
ms.assetid: 8d7f5789-610c-47f6-a109-5513d677ef60
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 30c8f31c104be52da2900eb81c7b7c29dfa55015
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586532"
---
# <a name="pidtagformdesignerguid-canonical-property"></a><span data-ttu-id="a59fb-103">Propiedad canónica PidTagFormDesignerGuid</span><span class="sxs-lookup"><span data-stu-id="a59fb-103">PidTagFormDesignerGuid Canonical Property</span></span>

  
  
<span data-ttu-id="a59fb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a59fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a59fb-105">Contiene el identificador único para el objeto que se utiliza para diseñar un formulario.</span><span class="sxs-lookup"><span data-stu-id="a59fb-105">Contains the unique identifier for the object that is used to design a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a59fb-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a59fb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a59fb-107">PR_FORM_DESIGNER_GUID</span><span class="sxs-lookup"><span data-stu-id="a59fb-107">PR_FORM_DESIGNER_GUID</span></span>  <br/> |
|<span data-ttu-id="a59fb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a59fb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a59fb-109">0x3309</span><span class="sxs-lookup"><span data-stu-id="a59fb-109">0x3309</span></span>  <br/> |
|<span data-ttu-id="a59fb-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a59fb-110">Data type:</span></span>  <br/> |<span data-ttu-id="a59fb-111">PT_GUID</span><span class="sxs-lookup"><span data-stu-id="a59fb-111">PT_GUID</span></span>  <br/> |
|<span data-ttu-id="a59fb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a59fb-112">Area:</span></span>  <br/> |<span data-ttu-id="a59fb-113">MAPI comunes</span><span class="sxs-lookup"><span data-stu-id="a59fb-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a59fb-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a59fb-114">Remarks</span></span>

<span data-ttu-id="a59fb-115">Normalmente, esta propiedad contiene el identificador único global (GUID) del programa de diseño que se usa para crear el formulario.</span><span class="sxs-lookup"><span data-stu-id="a59fb-115">This property usually contains the globally unique identifier (GUID) of the design program that is used to create the form.</span></span> <span data-ttu-id="a59fb-116">Esta propiedad puede estar vacía.</span><span class="sxs-lookup"><span data-stu-id="a59fb-116">This property can be empty.</span></span> 
  
<span data-ttu-id="a59fb-117">La estructura [MAPIUID](mapiuid.md) contiene la definición del identificador único.</span><span class="sxs-lookup"><span data-stu-id="a59fb-117">The [MAPIUID](mapiuid.md) structure contains the definition of the unique identifier.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a59fb-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a59fb-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a59fb-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a59fb-119">Header files</span></span>

<span data-ttu-id="a59fb-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a59fb-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="a59fb-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a59fb-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="a59fb-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a59fb-122">Mapitags.h</span></span>
  
> <span data-ttu-id="a59fb-123">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="a59fb-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a59fb-124">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="a59fb-124">See also</span></span>



[<span data-ttu-id="a59fb-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a59fb-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a59fb-126">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="a59fb-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a59fb-127">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a59fb-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a59fb-128">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="a59fb-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

