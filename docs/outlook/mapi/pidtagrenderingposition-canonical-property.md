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
ms.openlocfilehash: aa149a81102a4981712ea3ca897d8b1ad448a1eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820086"
---
# <a name="pidtagrenderingposition-canonical-property"></a><span data-ttu-id="58011-103">Propiedad canónica PidTagRenderingPosition</span><span class="sxs-lookup"><span data-stu-id="58011-103">PidTagRenderingPosition Canonical Property</span></span>

  
  
<span data-ttu-id="58011-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="58011-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="58011-105">Contiene un desplazamiento, en caracteres, que se usarán en la representación de un archivo adjunto dentro del texto principal del mensaje.</span><span class="sxs-lookup"><span data-stu-id="58011-105">Contains an offset, in characters, to use in rendering an attachment within the main message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="58011-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="58011-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="58011-107">PR_RENDERING_POSITION</span><span class="sxs-lookup"><span data-stu-id="58011-107">PR_RENDERING_POSITION</span></span>  <br/> |
|<span data-ttu-id="58011-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="58011-108">Identifier:</span></span>  <br/> |<span data-ttu-id="58011-109">0x370B</span><span class="sxs-lookup"><span data-stu-id="58011-109">0x370B</span></span>  <br/> |
|<span data-ttu-id="58011-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="58011-110">Data type:</span></span>  <br/> |<span data-ttu-id="58011-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="58011-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="58011-112">Área:</span><span class="sxs-lookup"><span data-stu-id="58011-112">Area:</span></span>  <br/> |<span data-ttu-id="58011-113">Datos adjuntos de MAPI</span><span class="sxs-lookup"><span data-stu-id="58011-113">MAPI attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58011-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="58011-114">Remarks</span></span>

<span data-ttu-id="58011-115">Cuando el desplazamiento suministrado es -1 (0xFFFFFFFF), los datos adjuntos no se representan mediante el uso de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="58011-115">When the supplied offset is -1 (0xFFFFFFFF), the attachment is not rendered by using this property.</span></span> <span data-ttu-id="58011-116">Todos los valores que no sea -1 indican la posición dentro de la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) en el que se representan los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="58011-116">All values other than -1 indicate the position within the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property at which the attachment is to be rendered.</span></span>
  
 <span data-ttu-id="58011-117">**Nota** El carácter indicado por esta propiedad en **PR_BODY** se ha reemplazado por los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="58011-117">**Note** The character indicated by this property in **PR_BODY** is replaced by the attachment.</span></span> <span data-ttu-id="58011-118">Normalmente, este carácter es un espacio, aunque también se puede usar un carácter de marcador de posición especial.</span><span class="sxs-lookup"><span data-stu-id="58011-118">Typically this character is a space, although a special placeholder character can also be used.</span></span> 
  
<span data-ttu-id="58011-119">Esta propiedad se expresa en caracteres.</span><span class="sxs-lookup"><span data-stu-id="58011-119">This property is expressed in characters.</span></span> <span data-ttu-id="58011-120">En algunos juegos de caracteres no es equivalente a bytes.</span><span class="sxs-lookup"><span data-stu-id="58011-120">In some character sets this is not equivalent to bytes.</span></span> <span data-ttu-id="58011-121">Las aplicaciones de Unicode pueden calcular la posición basada en caracteres de dos bytes.</span><span class="sxs-lookup"><span data-stu-id="58011-121">Unicode applications can compute the position based on two-byte characters.</span></span> <span data-ttu-id="58011-122">Las aplicaciones del conjunto de caracteres de doble Byte (DBCS) deben analizar el texto hasta el valor de esta propiedad, porque su representación de carácter varía entre uno y dos bytes por carácter.</span><span class="sxs-lookup"><span data-stu-id="58011-122">Double-Byte Character Set (DBCS) applications must scan the text up to this property value, because their character representation varies between one and two bytes per character.</span></span>
  
<span data-ttu-id="58011-123">Esta propiedad no debe usarse con texto de formato de texto enriquecido (RTF).</span><span class="sxs-lookup"><span data-stu-id="58011-123">This property should not be used with Rich Text Format (RTF) text.</span></span> <span data-ttu-id="58011-124">La posición de representación se indica en formato RTF mediante una secuencia de escape llamada el marcador de posición de datos adjuntos del objeto.</span><span class="sxs-lookup"><span data-stu-id="58011-124">The rendering position is indicated in RTF by an escape sequence called the object attachment placeholder.</span></span> <span data-ttu-id="58011-125">Esta secuencia se compone de la cadena `\objattph` seguido de un solo carácter, normalmente un espacio, que se reemplazará por la representación de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="58011-125">This sequence consists of the string  `\objattph` followed by a single character, normally a space, that will be replaced by the attachment rendering.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="58011-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="58011-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="58011-127">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="58011-127">Protocol specifications</span></span>

<span data-ttu-id="58011-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58011-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58011-129">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="58011-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="58011-130">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="58011-130">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="58011-131">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="58011-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="58011-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="58011-132">Header files</span></span>

<span data-ttu-id="58011-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="58011-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="58011-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="58011-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="58011-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="58011-135">Mapitags.h</span></span>
  
> <span data-ttu-id="58011-136">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="58011-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="58011-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="58011-137">See also</span></span>



[<span data-ttu-id="58011-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="58011-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="58011-139">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="58011-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="58011-140">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="58011-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="58011-141">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="58011-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

