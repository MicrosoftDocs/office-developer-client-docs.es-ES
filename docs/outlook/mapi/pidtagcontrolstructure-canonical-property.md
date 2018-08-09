---
title: Propiedad canónica PidTagControlStructure
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlStructure
api_type:
- HeaderDef
ms.assetid: 02910389-b346-431c-a282-dedbc9f7dfc6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e531c986ef6de2eccca446f5d560290fed831c21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819383"
---
# <a name="pidtagcontrolstructure-canonical-property"></a><span data-ttu-id="41c7d-103">Propiedad canónica PidTagControlStructure</span><span class="sxs-lookup"><span data-stu-id="41c7d-103">PidTagControlStructure Canonical Property</span></span>

  
  
<span data-ttu-id="41c7d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="41c7d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="41c7d-105">Contiene un puntero a una estructura para un control que se utiliza en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="41c7d-105">Contains a pointer to a structure for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="41c7d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="41c7d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="41c7d-107">PR_CONTROL_STRUCTURE</span><span class="sxs-lookup"><span data-stu-id="41c7d-107">PR_CONTROL_STRUCTURE</span></span>  <br/> |
|<span data-ttu-id="41c7d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="41c7d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="41c7d-109">0x3F01</span><span class="sxs-lookup"><span data-stu-id="41c7d-109">0x3F01</span></span>  <br/> |
|<span data-ttu-id="41c7d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="41c7d-110">Data type:</span></span>  <br/> |<span data-ttu-id="41c7d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="41c7d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="41c7d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="41c7d-112">Area:</span></span>  <br/> |<span data-ttu-id="41c7d-113">Tabla MAPI para mostrar</span><span class="sxs-lookup"><span data-stu-id="41c7d-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41c7d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="41c7d-114">Remarks</span></span>

<span data-ttu-id="41c7d-115">Esta propiedad representa un puntero de tipo long que se convierte en una de las estructuras de control.</span><span class="sxs-lookup"><span data-stu-id="41c7d-115">This property represents a long pointer that is cast to one of the control structures.</span></span> <span data-ttu-id="41c7d-116">Las estructuras de control incluyen:</span><span class="sxs-lookup"><span data-stu-id="41c7d-116">The control structures include:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="41c7d-117">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="41c7d-117">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |[<span data-ttu-id="41c7d-118">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="41c7d-118">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |
|[<span data-ttu-id="41c7d-119">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="41c7d-119">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |[<span data-ttu-id="41c7d-120">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="41c7d-120">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |
|[<span data-ttu-id="41c7d-121">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="41c7d-121">DTBLEDIT</span></span>](dtbledit.md) <br/> |[<span data-ttu-id="41c7d-122">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="41c7d-122">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |
|[<span data-ttu-id="41c7d-123">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="41c7d-123">DTBLLABEL</span></span>](dtbllabel.md) <br/> |[<span data-ttu-id="41c7d-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="41c7d-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |
|[<span data-ttu-id="41c7d-125">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="41c7d-125">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |[<span data-ttu-id="41c7d-126">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="41c7d-126">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |
|[<span data-ttu-id="41c7d-127">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="41c7d-127">DTBLPAGE</span></span>](dtblpage.md) <br/> |[<span data-ttu-id="41c7d-128">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="41c7d-128">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="41c7d-129">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="41c7d-129">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="41c7d-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="41c7d-130">Header files</span></span>

<span data-ttu-id="41c7d-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="41c7d-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="41c7d-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="41c7d-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="41c7d-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="41c7d-133">Mapitags.h</span></span>
  
> <span data-ttu-id="41c7d-134">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="41c7d-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="41c7d-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="41c7d-135">See also</span></span>



[<span data-ttu-id="41c7d-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="41c7d-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="41c7d-137">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="41c7d-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="41c7d-138">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="41c7d-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="41c7d-139">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="41c7d-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

