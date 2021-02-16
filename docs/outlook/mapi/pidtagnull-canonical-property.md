---
title: Propiedad canónica PidTagNull
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNull
api_type:
- HeaderDef
ms.assetid: 192cdab8-c615-47b9-9f04-a1414eaf0c77
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7e9c3340dfad47a811b56c86e8e6104fb6aac7c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329270"
---
# <a name="pidtagnull-canonical-property"></a><span data-ttu-id="5dea7-103">Propiedad canónica PidTagNull</span><span class="sxs-lookup"><span data-stu-id="5dea7-103">PidTagNull Canonical Property</span></span>

  
  
<span data-ttu-id="5dea7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5dea7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5dea7-105">Representa un valor nulo o un valor de una propiedad o reserva espacio de matriz.</span><span class="sxs-lookup"><span data-stu-id="5dea7-105">Represents a null value or setting of a property or reserves array space.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5dea7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5dea7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5dea7-107">PR_NULL</span><span class="sxs-lookup"><span data-stu-id="5dea7-107">PR_NULL</span></span>  <br/> |
|<span data-ttu-id="5dea7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5dea7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5dea7-109">0x0000</span><span class="sxs-lookup"><span data-stu-id="5dea7-109">0x0000</span></span>  <br/> |
|<span data-ttu-id="5dea7-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5dea7-110">Data type:</span></span>  <br/> |<span data-ttu-id="5dea7-111">PT_NULL</span><span class="sxs-lookup"><span data-stu-id="5dea7-111">PT_NULL</span></span>  <br/> |
|<span data-ttu-id="5dea7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5dea7-112">Area:</span></span>  <br/> |<span data-ttu-id="5dea7-113">Común</span><span class="sxs-lookup"><span data-stu-id="5dea7-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5dea7-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5dea7-114">Remarks</span></span>

<span data-ttu-id="5dea7-115">Esta propiedad se usa para reservar espacio en matrices de [estructuras SPropValue.](spropvalue.md)</span><span class="sxs-lookup"><span data-stu-id="5dea7-115">This property is used to reserve space in arrays of [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="5dea7-116">Se usa en una matriz de estructuras [SPropTagArray](sproptagarray.md) para decir al método que reserve espacio en la matriz devuelta de **estructuras SPropValue.**</span><span class="sxs-lookup"><span data-stu-id="5dea7-116">It is used in an array of [SPropTagArray](sproptagarray.md) structures to tell the method to reserve space in the returned array of **SPropValue** structures.</span></span> <span data-ttu-id="5dea7-117">Esto permite que las propiedades calculadas se llenen de forma económica.</span><span class="sxs-lookup"><span data-stu-id="5dea7-117">This allows for computed properties to be filled in an inexpensive way.</span></span> 
  
<span data-ttu-id="5dea7-118">Para obtener más información, vea [Información general sobre el tipo de propiedad MAPI.](mapi-property-type-overview.md)</span><span class="sxs-lookup"><span data-stu-id="5dea7-118">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5dea7-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5dea7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5dea7-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="5dea7-120">Protocol specifications</span></span>

<span data-ttu-id="5dea7-121">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5dea7-121">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5dea7-122">Especifica las propiedades y operaciones permitidas en los contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="5dea7-122">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5dea7-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5dea7-123">Header files</span></span>

<span data-ttu-id="5dea7-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5dea7-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="5dea7-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5dea7-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="5dea7-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5dea7-126">Mapitags.h</span></span>
  
> <span data-ttu-id="5dea7-127">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="5dea7-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5dea7-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5dea7-128">See also</span></span>



[<span data-ttu-id="5dea7-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5dea7-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5dea7-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="5dea7-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5dea7-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5dea7-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5dea7-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="5dea7-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

