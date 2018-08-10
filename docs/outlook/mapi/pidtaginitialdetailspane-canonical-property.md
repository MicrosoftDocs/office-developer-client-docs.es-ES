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
ms.openlocfilehash: 884bbad509e459d4f329e6468dd99124cec6c7d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819598"
---
# <a name="pidtaginitialdetailspane-canonical-property"></a><span data-ttu-id="897cc-103">Propiedad canónica PidTagInitialDetailsPane</span><span class="sxs-lookup"><span data-stu-id="897cc-103">PidTagInitialDetailsPane Canonical Property</span></span>

  
  
<span data-ttu-id="897cc-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="897cc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="897cc-105">Indica la página de una plantilla de presentación para mostrar primero.</span><span class="sxs-lookup"><span data-stu-id="897cc-105">Indicates the page of a display template to display first.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="897cc-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="897cc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="897cc-107">PR_INITIAL_DETAILS_PANE</span><span class="sxs-lookup"><span data-stu-id="897cc-107">PR_INITIAL_DETAILS_PANE</span></span>  <br/> |
|<span data-ttu-id="897cc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="897cc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="897cc-109">0x3F08</span><span class="sxs-lookup"><span data-stu-id="897cc-109">0x3F08</span></span>  <br/> |
|<span data-ttu-id="897cc-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="897cc-110">Data type:</span></span>  <br/> |<span data-ttu-id="897cc-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="897cc-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="897cc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="897cc-112">Area:</span></span>  <br/> |<span data-ttu-id="897cc-113">Tablas MAPI para mostrar</span><span class="sxs-lookup"><span data-stu-id="897cc-113">MAPI Display Tables</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="897cc-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="897cc-114">Remarks</span></span>

<span data-ttu-id="897cc-115">Debe estar presente en todos los objetos de la libreta de direcciones en un servidor de la interfaz de proveedor de servicio de nombres (NSPI) y debe tener el valor cero (0).</span><span class="sxs-lookup"><span data-stu-id="897cc-115">It must be present on all address book objects on an Name Service Provider Interface (NSPI) server, and must have the value zero (0).</span></span> <span data-ttu-id="897cc-116">No se debe definir para los objetos en una libreta de direcciones sin conexión.</span><span class="sxs-lookup"><span data-stu-id="897cc-116">It must not be defined for any objects in an Offline Address Book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="897cc-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="897cc-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="897cc-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="897cc-118">Protocol specifications</span></span>

<span data-ttu-id="897cc-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="897cc-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="897cc-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="897cc-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="897cc-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="897cc-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="897cc-122">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="897cc-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="897cc-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="897cc-123">Header files</span></span>

<span data-ttu-id="897cc-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="897cc-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="897cc-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="897cc-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="897cc-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="897cc-126">Mapitags.h</span></span>
  
> <span data-ttu-id="897cc-127">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="897cc-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="897cc-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="897cc-128">See also</span></span>



[<span data-ttu-id="897cc-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="897cc-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="897cc-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="897cc-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="897cc-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="897cc-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="897cc-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="897cc-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
