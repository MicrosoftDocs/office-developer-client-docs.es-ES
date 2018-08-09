---
title: Propiedad canónica PidTagMiniIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMiniIcon
api_type:
- HeaderDef
ms.assetid: a436b590-63f3-413c-a9c2-7664567e0ff0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 04d78bddc7bae27ba23cccf676eb6e7412ffc0db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819760"
---
# <a name="pidtagminiicon-canonical-property"></a><span data-ttu-id="c9ede-103">Propiedad canónica PidTagMiniIcon</span><span class="sxs-lookup"><span data-stu-id="c9ede-103">PidTagMiniIcon Canonical Property</span></span>

  
  
<span data-ttu-id="c9ede-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c9ede-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c9ede-105">Contiene un mapa de bits de un icono de tamaño para un formulario.</span><span class="sxs-lookup"><span data-stu-id="c9ede-105">Contains a bitmap of a half-size icon for a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c9ede-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c9ede-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c9ede-107">PR_MINI_ICON</span><span class="sxs-lookup"><span data-stu-id="c9ede-107">PR_MINI_ICON</span></span>  <br/> |
|<span data-ttu-id="c9ede-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c9ede-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c9ede-109">0x0FFC</span><span class="sxs-lookup"><span data-stu-id="c9ede-109">0x0FFC</span></span>  <br/> |
|<span data-ttu-id="c9ede-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c9ede-110">Data type:</span></span>  <br/> |<span data-ttu-id="c9ede-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c9ede-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c9ede-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c9ede-112">Area:</span></span>  <br/> |<span data-ttu-id="c9ede-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="c9ede-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9ede-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c9ede-114">Remarks</span></span>

<span data-ttu-id="c9ede-115">Esta propiedad contiene una imagen de 32 x 32 píxeles de un icono, el mismo que el contenido de una. Archivo ICO, pero sólo los píxeles de la parte superior izquierda de 16 x 16 se consideran importantes.</span><span class="sxs-lookup"><span data-stu-id="c9ede-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file, but only the upper left 16 × 16 pixels are considered significant.</span></span> <span data-ttu-id="c9ede-116">Esta propiedad normalmente se copia desde el. Archivo ICO especificado en la línea de iconos de la sección [descripción] adecuada del archivo de configuración de formulario.</span><span class="sxs-lookup"><span data-stu-id="c9ede-116">This property is normally copied from the .ICO file specified in the SmallIcon line of the appropriate [Description] section of the form configuration file.</span></span>
  
 <span data-ttu-id="c9ede-117">**Nota** Algunas plataformas hacer no los iconos de compatibilidad de 16 x 16 píxeles.</span><span class="sxs-lookup"><span data-stu-id="c9ede-117">**Note** Some platforms do not support 16 × 16 pixel icons.</span></span> <span data-ttu-id="c9ede-118">El formato de 32 x 32 de esta propiedad es utilizable en tal caso, pero las aplicaciones cliente deben tener en cuenta las incoherencias de presentación.</span><span class="sxs-lookup"><span data-stu-id="c9ede-118">The 32 × 32 format of this property is usable in such a case but client applications should be aware of display inconsistencies.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c9ede-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9ede-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c9ede-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c9ede-120">Header files</span></span>

<span data-ttu-id="c9ede-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c9ede-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="c9ede-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c9ede-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="c9ede-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c9ede-123">Mapitags.h</span></span>
  
> <span data-ttu-id="c9ede-124">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c9ede-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9ede-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9ede-125">See also</span></span>



[<span data-ttu-id="c9ede-126">Propiedad canónica PidTagIcon</span><span class="sxs-lookup"><span data-stu-id="c9ede-126">PidTagIcon Canonical Property</span></span>](pidtagicon-canonical-property.md)


[<span data-ttu-id="c9ede-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c9ede-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c9ede-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c9ede-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c9ede-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c9ede-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c9ede-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="c9ede-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

