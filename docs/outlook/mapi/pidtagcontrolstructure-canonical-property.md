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
ms.openlocfilehash: cf91620042f916d51f27be50d15f72db537ad5f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412950"
---
# <a name="pidtagcontrolstructure-canonical-property"></a><span data-ttu-id="7f3ca-103">Propiedad canónica PidTagControlStructure</span><span class="sxs-lookup"><span data-stu-id="7f3ca-103">PidTagControlStructure Canonical Property</span></span>

  
  
<span data-ttu-id="7f3ca-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f3ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f3ca-105">Contiene un puntero a una estructura para un control utilizado en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7f3ca-105">Contains a pointer to a structure for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7f3ca-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7f3ca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7f3ca-107">PR_CONTROL_STRUCTURE</span><span class="sxs-lookup"><span data-stu-id="7f3ca-107">PR_CONTROL_STRUCTURE</span></span>  <br/> |
|<span data-ttu-id="7f3ca-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7f3ca-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7f3ca-109">0x3F01</span><span class="sxs-lookup"><span data-stu-id="7f3ca-109">0x3F01</span></span>  <br/> |
|<span data-ttu-id="7f3ca-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7f3ca-110">Data type:</span></span>  <br/> |<span data-ttu-id="7f3ca-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7f3ca-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7f3ca-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7f3ca-112">Area:</span></span>  <br/> |<span data-ttu-id="7f3ca-113">Tabla de visualización de MAPI</span><span class="sxs-lookup"><span data-stu-id="7f3ca-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f3ca-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7f3ca-114">Remarks</span></span>

<span data-ttu-id="7f3ca-115">Esta propiedad representa un puntero largo que se convierte en una de las estructuras de control.</span><span class="sxs-lookup"><span data-stu-id="7f3ca-115">This property represents a long pointer that is cast to one of the control structures.</span></span> <span data-ttu-id="7f3ca-116">Las estructuras de control incluyen:</span><span class="sxs-lookup"><span data-stu-id="7f3ca-116">The control structures include:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="7f3ca-117">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="7f3ca-117">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |[<span data-ttu-id="7f3ca-118">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="7f3ca-118">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |
|[<span data-ttu-id="7f3ca-119">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="7f3ca-119">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |[<span data-ttu-id="7f3ca-120">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="7f3ca-120">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |
|[<span data-ttu-id="7f3ca-121">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="7f3ca-121">DTBLEDIT</span></span>](dtbledit.md) <br/> |[<span data-ttu-id="7f3ca-122">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="7f3ca-122">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |
|[<span data-ttu-id="7f3ca-123">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="7f3ca-123">DTBLLABEL</span></span>](dtbllabel.md) <br/> |[<span data-ttu-id="7f3ca-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="7f3ca-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |
|[<span data-ttu-id="7f3ca-125">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="7f3ca-125">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |[<span data-ttu-id="7f3ca-126">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="7f3ca-126">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |
|[<span data-ttu-id="7f3ca-127">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="7f3ca-127">DTBLPAGE</span></span>](dtblpage.md) <br/> |[<span data-ttu-id="7f3ca-128">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="7f3ca-128">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7f3ca-129">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7f3ca-129">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7f3ca-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7f3ca-130">Header files</span></span>

<span data-ttu-id="7f3ca-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7f3ca-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="7f3ca-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7f3ca-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="7f3ca-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="7f3ca-133">Mapitags.h</span></span>
  
> <span data-ttu-id="7f3ca-134">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="7f3ca-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f3ca-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="7f3ca-135">See also</span></span>



[<span data-ttu-id="7f3ca-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7f3ca-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7f3ca-137">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="7f3ca-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7f3ca-138">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7f3ca-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7f3ca-139">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="7f3ca-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

