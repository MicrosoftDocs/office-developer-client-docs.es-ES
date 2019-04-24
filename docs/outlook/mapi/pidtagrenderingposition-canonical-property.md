---
title: Propiedad canónica PidTagRenderingPosition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRenderingPosition
api_type:
- COM
ms.assetid: bce46687-17dc-4a3f-96be-303d8755158e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d463be4a14ecf478bdcbddc50b4ad9360829befc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355156"
---
# <a name="pidtagrenderingposition-canonical-property"></a><span data-ttu-id="f1814-103">Propiedad canónica PidTagRenderingPosition</span><span class="sxs-lookup"><span data-stu-id="f1814-103">PidTagRenderingPosition Canonical Property</span></span>

  
  
<span data-ttu-id="f1814-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1814-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1814-105">Contiene un desplazamiento, en caracteres, que se usa para representar datos adjuntos dentro del texto del mensaje principal.</span><span class="sxs-lookup"><span data-stu-id="f1814-105">Contains an offset, in characters, to use in rendering an attachment within the main message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f1814-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f1814-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f1814-107">PR_RENDERING_POSITION</span><span class="sxs-lookup"><span data-stu-id="f1814-107">PR_RENDERING_POSITION</span></span>  <br/> |
|<span data-ttu-id="f1814-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f1814-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f1814-109">0x370B</span><span class="sxs-lookup"><span data-stu-id="f1814-109">0x370B</span></span>  <br/> |
|<span data-ttu-id="f1814-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f1814-110">Data type:</span></span>  <br/> |<span data-ttu-id="f1814-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f1814-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f1814-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f1814-112">Area:</span></span>  <br/> |<span data-ttu-id="f1814-113">Datos adjuntos MAPI</span><span class="sxs-lookup"><span data-stu-id="f1814-113">MAPI attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1814-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f1814-114">Remarks</span></span>

<span data-ttu-id="f1814-115">Cuando el desplazamiento proporcionado es-1 (0xFFFFFFFF), los datos adjuntos no se representan mediante esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f1814-115">When the supplied offset is -1 (0xFFFFFFFF), the attachment is not rendered by using this property.</span></span> <span data-ttu-id="f1814-116">Todos los valores que no sean-1 indican la posición dentro de la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) en la que se van a representar los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="f1814-116">All values other than -1 indicate the position within the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property at which the attachment is to be rendered.</span></span>
  
 <span data-ttu-id="f1814-117">**Nota:** El carácter que indica esta propiedad en **PR_BODY** se ha reemplazado por los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="f1814-117">**Note** The character indicated by this property in **PR_BODY** is replaced by the attachment.</span></span> <span data-ttu-id="f1814-118">Normalmente este carácter es un espacio, aunque también se puede usar un carácter de marcador de posición especial.</span><span class="sxs-lookup"><span data-stu-id="f1814-118">Typically this character is a space, although a special placeholder character can also be used.</span></span> 
  
<span data-ttu-id="f1814-119">Esta propiedad se expresa en caracteres.</span><span class="sxs-lookup"><span data-stu-id="f1814-119">This property is expressed in characters.</span></span> <span data-ttu-id="f1814-120">En algunos juegos de caracteres no equivale a los bytes.</span><span class="sxs-lookup"><span data-stu-id="f1814-120">In some character sets this is not equivalent to bytes.</span></span> <span data-ttu-id="f1814-121">Las aplicaciones Unicode pueden calcular la posición basándose en caracteres de dos bytes.</span><span class="sxs-lookup"><span data-stu-id="f1814-121">Unicode applications can compute the position based on two-byte characters.</span></span> <span data-ttu-id="f1814-122">Las aplicaciones del juego de caracteres de doble byte (DBCS) deben analizar el texto hasta el valor de esta propiedad, porque su representación de caracteres varía entre uno y dos bytes por carácter.</span><span class="sxs-lookup"><span data-stu-id="f1814-122">Double-Byte Character Set (DBCS) applications must scan the text up to this property value, because their character representation varies between one and two bytes per character.</span></span>
  
<span data-ttu-id="f1814-123">Esta propiedad no debe usarse con texto con formato de texto enriquecido (RTF).</span><span class="sxs-lookup"><span data-stu-id="f1814-123">This property should not be used with Rich Text Format (RTF) text.</span></span> <span data-ttu-id="f1814-124">La posición de representación se indica en RTF mediante una secuencia de escape denominada marcador de posición de datos adjuntos del objeto.</span><span class="sxs-lookup"><span data-stu-id="f1814-124">The rendering position is indicated in RTF by an escape sequence called the object attachment placeholder.</span></span> <span data-ttu-id="f1814-125">Esta secuencia consta de la cadena `\objattph` seguida de un único carácter, normalmente un espacio, que se reemplazará por la representación de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="f1814-125">This sequence consists of the string  `\objattph` followed by a single character, normally a space, that will be replaced by the attachment rendering.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f1814-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1814-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f1814-127">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f1814-127">Protocol specifications</span></span>

<span data-ttu-id="f1814-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1814-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1814-129">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f1814-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f1814-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1814-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1814-131">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="f1814-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f1814-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f1814-132">Header files</span></span>

<span data-ttu-id="f1814-133">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f1814-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="f1814-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f1814-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="f1814-135">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f1814-135">Mapitags.h</span></span>
  
> <span data-ttu-id="f1814-136">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f1814-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f1814-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1814-137">See also</span></span>



[<span data-ttu-id="f1814-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f1814-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f1814-139">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="f1814-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f1814-140">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f1814-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f1814-141">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="f1814-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

