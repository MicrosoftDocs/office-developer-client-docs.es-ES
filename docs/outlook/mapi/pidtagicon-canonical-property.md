---
title: Propiedad canónica PidTagIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIcon
api_type:
- HeaderDef
ms.assetid: 815dabf3-3cac-40e1-b6ff-51db2ff5096a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ad8d6934b5e57429de5039e9420742caa9dd4294
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356731"
---
# <a name="pidtagicon-canonical-property"></a><span data-ttu-id="5e018-103">Propiedad canónica PidTagIcon</span><span class="sxs-lookup"><span data-stu-id="5e018-103">PidTagIcon Canonical Property</span></span>

  
  
<span data-ttu-id="5e018-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e018-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e018-105">Contiene un mapa de bits de un icono de tamaño completo para un formulario.</span><span class="sxs-lookup"><span data-stu-id="5e018-105">Contains a bitmap of a full size icon for a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5e018-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5e018-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5e018-107">PR_ICON</span><span class="sxs-lookup"><span data-stu-id="5e018-107">PR_ICON</span></span>  <br/> |
|<span data-ttu-id="5e018-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5e018-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5e018-109">0x0FFD</span><span class="sxs-lookup"><span data-stu-id="5e018-109">0x0FFD</span></span>  <br/> |
|<span data-ttu-id="5e018-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5e018-110">Data type:</span></span>  <br/> |<span data-ttu-id="5e018-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5e018-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5e018-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5e018-112">Area:</span></span>  <br/> |<span data-ttu-id="5e018-113">MAPI no transmitible</span><span class="sxs-lookup"><span data-stu-id="5e018-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e018-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5e018-114">Remarks</span></span>

<span data-ttu-id="5e018-115">Esta propiedad contiene una imagen de 32 × 32 píxeles de un icono, que es la misma que el contenido de un. Archivo ICO.</span><span class="sxs-lookup"><span data-stu-id="5e018-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file.</span></span> <span data-ttu-id="5e018-116">Normalmente, esta propiedad se copia desde el. Archivo ICO especificado en la línea LargeIcon de la sección [deScription] correspondiente del archivo de configuración de formulario.</span><span class="sxs-lookup"><span data-stu-id="5e018-116">This property is normally copied from the .ICO file specified in the LargeIcon line of the appropriate [Description] section of the form configuration file.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5e018-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5e018-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5e018-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="5e018-118">Protocol specifications</span></span>

<span data-ttu-id="5e018-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e018-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e018-120">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="5e018-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5e018-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5e018-121">Header files</span></span>

<span data-ttu-id="5e018-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5e018-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="5e018-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5e018-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="5e018-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5e018-124">Mapitags.h</span></span>
  
> <span data-ttu-id="5e018-125">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="5e018-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5e018-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e018-126">See also</span></span>



[<span data-ttu-id="5e018-127">Propiedad canónica PidTagMiniIcon</span><span class="sxs-lookup"><span data-stu-id="5e018-127">PidTagMiniIcon Canonical Property</span></span>](pidtagminiicon-canonical-property.md)


[<span data-ttu-id="5e018-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5e018-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5e018-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="5e018-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5e018-130">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5e018-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5e018-131">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="5e018-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

