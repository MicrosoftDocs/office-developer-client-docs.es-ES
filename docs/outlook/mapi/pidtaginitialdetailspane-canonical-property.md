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
ms.openlocfilehash: 3bf0f52dbeda37ac35024ae3bf38df8919e37b60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346581"
---
# <a name="pidtaginitialdetailspane-canonical-property"></a><span data-ttu-id="6c7ae-103">Propiedad canónica PidTagInitialDetailsPane</span><span class="sxs-lookup"><span data-stu-id="6c7ae-103">PidTagInitialDetailsPane Canonical Property</span></span>

  
  
<span data-ttu-id="6c7ae-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c7ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c7ae-105">Indica la página de una plantilla para mostrar que se mostrará primero.</span><span class="sxs-lookup"><span data-stu-id="6c7ae-105">Indicates the page of a display template to display first.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6c7ae-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="6c7ae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6c7ae-107">PR_INITIAL_DETAILS_PANE</span><span class="sxs-lookup"><span data-stu-id="6c7ae-107">PR_INITIAL_DETAILS_PANE</span></span>  <br/> |
|<span data-ttu-id="6c7ae-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6c7ae-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6c7ae-109">0x3F08</span><span class="sxs-lookup"><span data-stu-id="6c7ae-109">0x3F08</span></span>  <br/> |
|<span data-ttu-id="6c7ae-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="6c7ae-110">Data type:</span></span>  <br/> |<span data-ttu-id="6c7ae-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6c7ae-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6c7ae-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6c7ae-112">Area:</span></span>  <br/> |<span data-ttu-id="6c7ae-113">Tablas para mostrar MAPI</span><span class="sxs-lookup"><span data-stu-id="6c7ae-113">MAPI Display Tables</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c7ae-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6c7ae-114">Remarks</span></span>

<span data-ttu-id="6c7ae-115">Debe estar presente en todos los objetos de la libreta de direcciones en un servidor de interfaz de proveedor de servicios de nombres (NSPI) y debe tener el valor cero (0).</span><span class="sxs-lookup"><span data-stu-id="6c7ae-115">It must be present on all address book objects on an Name Service Provider Interface (NSPI) server, and must have the value zero (0).</span></span> <span data-ttu-id="6c7ae-116">No se debe definir para ningún objeto de una libreta de direcciones sin conexión.</span><span class="sxs-lookup"><span data-stu-id="6c7ae-116">It must not be defined for any objects in an Offline Address Book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6c7ae-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6c7ae-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6c7ae-118">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="6c7ae-118">Protocol specifications</span></span>

<span data-ttu-id="6c7ae-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c7ae-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c7ae-120">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="6c7ae-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6c7ae-121">[[MS-OJOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c7ae-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c7ae-122">Especifica las propiedades y operaciones de listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="6c7ae-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6c7ae-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="6c7ae-123">Header files</span></span>

<span data-ttu-id="6c7ae-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6c7ae-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="6c7ae-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="6c7ae-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="6c7ae-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6c7ae-126">Mapitags.h</span></span>
  
> <span data-ttu-id="6c7ae-127">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="6c7ae-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6c7ae-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6c7ae-128">See also</span></span>



[<span data-ttu-id="6c7ae-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6c7ae-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6c7ae-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="6c7ae-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6c7ae-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="6c7ae-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6c7ae-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="6c7ae-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

