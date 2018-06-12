---
title: Propiedad canónico PidLidToDoSubOrdinal
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 9965ed059ba4596232111f5fbd86b9d177e3c3dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819005"
---
# <a name="pidlidtodosubordinal-canonical-property"></a><span data-ttu-id="a7257-103">Propiedad canónico PidLidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="a7257-103">PidLidToDoSubOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="a7257-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a7257-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a7257-105">Actúa como un separador de placa cuando la propiedad **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) ordena los objetos y el resultado en una placa.</span><span class="sxs-lookup"><span data-stu-id="a7257-105">Acts as a tie breaker when the **dispidToDoOrdinalDate** ([PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)) property sorts objects and the result in a tie.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a7257-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a7257-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a7257-107">dispidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="a7257-107">dispidToDoSubOrdinal</span></span>  <br/> |
|<span data-ttu-id="a7257-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="a7257-108">Property set:</span></span>  <br/> |<span data-ttu-id="a7257-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="a7257-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a7257-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="a7257-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a7257-111">0x000085A1</span><span class="sxs-lookup"><span data-stu-id="a7257-111">0x000085A1</span></span>  <br/> |
|<span data-ttu-id="a7257-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a7257-112">Data type:</span></span>  <br/> |<span data-ttu-id="a7257-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a7257-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a7257-114">Área:</span><span class="sxs-lookup"><span data-stu-id="a7257-114">Area:</span></span>  <br/> |<span data-ttu-id="a7257-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="a7257-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7257-116">Notas</span><span class="sxs-lookup"><span data-stu-id="a7257-116">Remarks</span></span>

<span data-ttu-id="a7257-117">Si se usa, esta propiedad se debe ordenar de manera lexicográfica.</span><span class="sxs-lookup"><span data-stu-id="a7257-117">If used, this property must be sorted lexicographically.</span></span> <span data-ttu-id="a7257-118">Los caracteres de componente de la cadena deben contener sólo los números del cero al nueve.</span><span class="sxs-lookup"><span data-stu-id="a7257-118">The component characters of the string must consist of only the numerals zero through nine.</span></span> <span data-ttu-id="a7257-119">Esta propiedad debe establecerse inicialmente en "5555555".</span><span class="sxs-lookup"><span data-stu-id="a7257-119">This property should be initially set to "5555555".</span></span> <span data-ttu-id="a7257-120">La longitud de esta propiedad no debe superar los 254 caracteres (excepto el carácter nulo).</span><span class="sxs-lookup"><span data-stu-id="a7257-120">The length of this property must not exceed 254 characters (excluding the terminating NULL character).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a7257-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a7257-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a7257-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="a7257-122">Protocol specifications</span></span>

<span data-ttu-id="a7257-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7257-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7257-124">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a7257-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a7257-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7257-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7257-126">Especifica las propiedades y las operaciones relacionadas con marcas.</span><span class="sxs-lookup"><span data-stu-id="a7257-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a7257-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a7257-127">Header files</span></span>

<span data-ttu-id="a7257-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a7257-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="a7257-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a7257-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a7257-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="a7257-130">See also</span></span>



[<span data-ttu-id="a7257-131">Propiedad canónico PidLidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="a7257-131">PidLidToDoOrdinalDate Canonical Property</span></span>](pidlidtodoordinaldate-canonical-property.md)


[<span data-ttu-id="a7257-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a7257-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a7257-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="a7257-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a7257-134">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="a7257-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a7257-135">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a7257-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

