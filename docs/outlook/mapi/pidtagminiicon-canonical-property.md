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
ms.openlocfilehash: ea7f9e0ed57c56b48399b9ffd1ea42db28daf249
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405418"
---
# <a name="pidtagminiicon-canonical-property"></a><span data-ttu-id="547dd-103">Propiedad canónica PidTagMiniIcon</span><span class="sxs-lookup"><span data-stu-id="547dd-103">PidTagMiniIcon Canonical Property</span></span>

  
  
<span data-ttu-id="547dd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="547dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="547dd-105">Contiene un mapa de bits de un icono de tamaño medio de un formulario.</span><span class="sxs-lookup"><span data-stu-id="547dd-105">Contains a bitmap of a half-size icon for a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="547dd-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="547dd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="547dd-107">PR_MINI_ICON</span><span class="sxs-lookup"><span data-stu-id="547dd-107">PR_MINI_ICON</span></span>  <br/> |
|<span data-ttu-id="547dd-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="547dd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="547dd-109">0x0FFC</span><span class="sxs-lookup"><span data-stu-id="547dd-109">0x0FFC</span></span>  <br/> |
|<span data-ttu-id="547dd-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="547dd-110">Data type:</span></span>  <br/> |<span data-ttu-id="547dd-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="547dd-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="547dd-112">Área:</span><span class="sxs-lookup"><span data-stu-id="547dd-112">Area:</span></span>  <br/> |<span data-ttu-id="547dd-113">Mensajes generales</span><span class="sxs-lookup"><span data-stu-id="547dd-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="547dd-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="547dd-114">Remarks</span></span>

<span data-ttu-id="547dd-115">Esta propiedad contiene una imagen de 32 × 32 píxeles de un icono, que es la misma que el contenido de un. ICO, pero solo el extremo superior izquierdo de 16 x 16 píxeles se considera significativo.</span><span class="sxs-lookup"><span data-stu-id="547dd-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file, but only the upper left 16 × 16 pixels are considered significant.</span></span> <span data-ttu-id="547dd-116">Normalmente, esta propiedad se copia desde el. Archivo ICO especificado en la línea SmallIcon de la sección [deScription] correspondiente del archivo de configuración de formulario.</span><span class="sxs-lookup"><span data-stu-id="547dd-116">This property is normally copied from the .ICO file specified in the SmallIcon line of the appropriate [Description] section of the form configuration file.</span></span>
  
 <span data-ttu-id="547dd-117">**Nota:** Algunas plataformas no admiten iconos de 16 x 16 píxeles.</span><span class="sxs-lookup"><span data-stu-id="547dd-117">**Note** Some platforms do not support 16 × 16 pixel icons.</span></span> <span data-ttu-id="547dd-118">El formato 32 × 32 de esta propiedad se puede usar en este caso, pero las aplicaciones cliente deben tener en cuenta las incoherencias de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="547dd-118">The 32 × 32 format of this property is usable in such a case but client applications should be aware of display inconsistencies.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="547dd-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="547dd-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="547dd-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="547dd-120">Header files</span></span>

<span data-ttu-id="547dd-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="547dd-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="547dd-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="547dd-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="547dd-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="547dd-123">Mapitags.h</span></span>
  
> <span data-ttu-id="547dd-124">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="547dd-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="547dd-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="547dd-125">See also</span></span>



[<span data-ttu-id="547dd-126">Propiedad canónica PidTagIcon</span><span class="sxs-lookup"><span data-stu-id="547dd-126">PidTagIcon Canonical Property</span></span>](pidtagicon-canonical-property.md)


[<span data-ttu-id="547dd-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="547dd-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="547dd-128">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="547dd-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="547dd-129">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="547dd-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="547dd-130">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="547dd-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

