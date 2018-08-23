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
ms.openlocfilehash: 98dfdab24d2c4170609d9db1c3104a3f17436736
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578069"
---
# <a name="pidlidtodosubordinal-canonical-property"></a><span data-ttu-id="949f8-103">Propiedad canónica PidLidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="949f8-103">PidLidToDoSubOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="949f8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="949f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="949f8-105">Actúa como un separador de placa cuando la propiedad **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) ordena los objetos y el resultado en una placa.</span><span class="sxs-lookup"><span data-stu-id="949f8-105">Acts as a tie breaker when the **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) property sorts objects and the result in a tie.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="949f8-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="949f8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="949f8-107">dispidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="949f8-107">dispidToDoSubOrdinal</span></span>  <br/> |
|<span data-ttu-id="949f8-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="949f8-108">Property set:</span></span>  <br/> |<span data-ttu-id="949f8-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="949f8-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="949f8-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="949f8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="949f8-111">0x000085A1</span><span class="sxs-lookup"><span data-stu-id="949f8-111">0x000085A1</span></span>  <br/> |
|<span data-ttu-id="949f8-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="949f8-112">Data type:</span></span>  <br/> |<span data-ttu-id="949f8-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="949f8-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="949f8-114">Área:</span><span class="sxs-lookup"><span data-stu-id="949f8-114">Area:</span></span>  <br/> |<span data-ttu-id="949f8-115">Task</span><span class="sxs-lookup"><span data-stu-id="949f8-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="949f8-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="949f8-116">Remarks</span></span>

<span data-ttu-id="949f8-117">Si se usa, esta propiedad se debe ordenar de manera lexicográfica.</span><span class="sxs-lookup"><span data-stu-id="949f8-117">If used, this property must be sorted lexicographically.</span></span> <span data-ttu-id="949f8-118">Los caracteres de componente de la cadena deben contener sólo los números del cero al nueve.</span><span class="sxs-lookup"><span data-stu-id="949f8-118">The component characters of the string must consist of only the numerals zero through nine.</span></span> <span data-ttu-id="949f8-119">Esta propiedad debe establecerse inicialmente en "5555555".</span><span class="sxs-lookup"><span data-stu-id="949f8-119">This property should be initially set to "5555555".</span></span> <span data-ttu-id="949f8-120">La longitud de esta propiedad no debe superar los 254 caracteres (excepto el carácter nulo).</span><span class="sxs-lookup"><span data-stu-id="949f8-120">The length of this property must not exceed 254 characters (excluding the terminating NULL character).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="949f8-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="949f8-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="949f8-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="949f8-122">Protocol specifications</span></span>

<span data-ttu-id="949f8-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="949f8-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="949f8-124">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="949f8-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="949f8-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="949f8-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="949f8-126">Especifica las propiedades y las operaciones relacionadas con marcas.</span><span class="sxs-lookup"><span data-stu-id="949f8-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="949f8-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="949f8-127">Header files</span></span>

<span data-ttu-id="949f8-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="949f8-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="949f8-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="949f8-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="949f8-130">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="949f8-130">See also</span></span>



[<span data-ttu-id="949f8-131">Propiedad canónica PidLidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="949f8-131">PidLidToDoOrdinalDate Canonical Property</span></span>](pidlidtodoordinaldate-canonical-property.md)


[<span data-ttu-id="949f8-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="949f8-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="949f8-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="949f8-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="949f8-134">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="949f8-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="949f8-135">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="949f8-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

