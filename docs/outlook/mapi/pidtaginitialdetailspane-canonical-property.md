---
title: Propiedad canónica PidTagInitialDetailsPane
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInitialDetailsPane
api_type:
- HeaderDef
ms.assetid: c4712133-6fbd-4c50-a258-5f4317120476
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0ea7d0a17fdb6dba047cb97290d991ce384d4750
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573939"
---
# <a name="pidtaginitialdetailspane-canonical-property"></a><span data-ttu-id="dd1c2-103">Propiedad canónica PidTagInitialDetailsPane</span><span class="sxs-lookup"><span data-stu-id="dd1c2-103">PidTagInitialDetailsPane Canonical Property</span></span>

  
  
<span data-ttu-id="dd1c2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd1c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd1c2-105">Indica la página de una plantilla de presentación para mostrar primero.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-105">Indicates the page of a display template to display first.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dd1c2-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="dd1c2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dd1c2-107">PR_INITIAL_DETAILS_PANE</span><span class="sxs-lookup"><span data-stu-id="dd1c2-107">PR_INITIAL_DETAILS_PANE</span></span>  <br/> |
|<span data-ttu-id="dd1c2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="dd1c2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dd1c2-109">0x3F08</span><span class="sxs-lookup"><span data-stu-id="dd1c2-109">0x3F08</span></span>  <br/> |
|<span data-ttu-id="dd1c2-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="dd1c2-110">Data type:</span></span>  <br/> |<span data-ttu-id="dd1c2-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="dd1c2-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="dd1c2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="dd1c2-112">Area:</span></span>  <br/> |<span data-ttu-id="dd1c2-113">Tablas MAPI para mostrar</span><span class="sxs-lookup"><span data-stu-id="dd1c2-113">MAPI Display Tables</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd1c2-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dd1c2-114">Remarks</span></span>

<span data-ttu-id="dd1c2-115">Debe estar presente en todos los objetos de la libreta de direcciones en un servidor de la interfaz de proveedor de servicio de nombres (NSPI) y debe tener el valor cero (0).</span><span class="sxs-lookup"><span data-stu-id="dd1c2-115">It must be present on all address book objects on an Name Service Provider Interface (NSPI) server, and must have the value zero (0).</span></span> <span data-ttu-id="dd1c2-116">No se debe definir para los objetos en una libreta de direcciones sin conexión.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-116">It must not be defined for any objects in an Offline Address Book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dd1c2-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="dd1c2-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dd1c2-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="dd1c2-118">Protocol specifications</span></span>

<span data-ttu-id="dd1c2-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dd1c2-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dd1c2-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dd1c2-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dd1c2-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dd1c2-122">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dd1c2-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="dd1c2-123">Header files</span></span>

<span data-ttu-id="dd1c2-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dd1c2-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="dd1c2-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="dd1c2-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dd1c2-126">Mapitags.h</span></span>
  
> <span data-ttu-id="dd1c2-127">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="dd1c2-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dd1c2-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="dd1c2-128">See also</span></span>



[<span data-ttu-id="dd1c2-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="dd1c2-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dd1c2-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="dd1c2-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dd1c2-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="dd1c2-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dd1c2-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="dd1c2-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

