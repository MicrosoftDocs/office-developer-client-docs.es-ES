---
title: Propiedad canónica PidLidToDoSubOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoSubOrdinal
api_type:
- COM
ms.assetid: e3bc15ef-155e-49fd-88e5-64713df9b939
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c4ea125a5bde89e0885be4c04e3f106f202b1e18
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344922"
---
# <a name="pidlidtodosubordinal-canonical-property"></a><span data-ttu-id="ee3d9-103">Propiedad canónica PidLidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="ee3d9-103">PidLidToDoSubOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="ee3d9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee3d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee3d9-105">Actúa como un disyuntor cuando la propiedad **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) ordena los objetos y el resultado está en empate.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-105">Acts as a tie breaker when the **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) property sorts objects and the result in a tie.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ee3d9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ee3d9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ee3d9-107">dispidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="ee3d9-107">dispidToDoSubOrdinal</span></span>  <br/> |
|<span data-ttu-id="ee3d9-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="ee3d9-108">Property set:</span></span>  <br/> |<span data-ttu-id="ee3d9-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="ee3d9-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="ee3d9-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="ee3d9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ee3d9-111">0x000085A1</span><span class="sxs-lookup"><span data-stu-id="ee3d9-111">0x000085A1</span></span>  <br/> |
|<span data-ttu-id="ee3d9-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ee3d9-112">Data type:</span></span>  <br/> |<span data-ttu-id="ee3d9-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ee3d9-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ee3d9-114">Área:</span><span class="sxs-lookup"><span data-stu-id="ee3d9-114">Area:</span></span>  <br/> |<span data-ttu-id="ee3d9-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="ee3d9-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee3d9-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ee3d9-116">Remarks</span></span>

<span data-ttu-id="ee3d9-117">Si se usa, esta propiedad debe estar ordenada lexicographically.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-117">If used, this property must be sorted lexicographically.</span></span> <span data-ttu-id="ee3d9-118">Los caracteres del componente de la cadena deben estar formados sólo por números del 0 al 9.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-118">The component characters of the string must consist of only the numerals zero through nine.</span></span> <span data-ttu-id="ee3d9-119">Esta propiedad debe establecerse inicialmente en "5555555".</span><span class="sxs-lookup"><span data-stu-id="ee3d9-119">This property should be initially set to "5555555".</span></span> <span data-ttu-id="ee3d9-120">La longitud de esta propiedad no debe superar los 254 caracteres (excepto el carácter NULL de terminación).</span><span class="sxs-lookup"><span data-stu-id="ee3d9-120">The length of this property must not exceed 254 characters (excluding the terminating NULL character).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ee3d9-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ee3d9-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ee3d9-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="ee3d9-122">Protocol specifications</span></span>

<span data-ttu-id="ee3d9-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee3d9-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee3d9-124">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ee3d9-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee3d9-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee3d9-126">Especifica las propiedades y operaciones relacionadas con la marcación.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ee3d9-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ee3d9-127">Header files</span></span>

<span data-ttu-id="ee3d9-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ee3d9-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="ee3d9-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ee3d9-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ee3d9-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee3d9-130">See also</span></span>



[<span data-ttu-id="ee3d9-131">Propiedad canónica PidLidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="ee3d9-131">PidLidToDoOrdinalDate Canonical Property</span></span>](pidlidtodoordinaldate-canonical-property.md)


[<span data-ttu-id="ee3d9-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ee3d9-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ee3d9-133">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="ee3d9-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ee3d9-134">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ee3d9-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ee3d9-135">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="ee3d9-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

