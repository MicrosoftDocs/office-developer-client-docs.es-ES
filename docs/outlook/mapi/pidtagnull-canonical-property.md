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
ms.openlocfilehash: efb0812a88ad435c2456a729a6e950b371cc0250
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595352"
---
# <a name="pidtagnull-canonical-property"></a><span data-ttu-id="71e18-103">Propiedad canónica PidTagNull</span><span class="sxs-lookup"><span data-stu-id="71e18-103">PidTagNull Canonical Property</span></span>

  
  
<span data-ttu-id="71e18-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71e18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71e18-105">Representa un valor null o la configuración de una propiedad o se reserva espacio de matriz.</span><span class="sxs-lookup"><span data-stu-id="71e18-105">Represents a null value or setting of a property or reserves array space.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="71e18-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="71e18-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="71e18-107">PR_NULL</span><span class="sxs-lookup"><span data-stu-id="71e18-107">PR_NULL</span></span>  <br/> |
|<span data-ttu-id="71e18-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="71e18-108">Identifier:</span></span>  <br/> |<span data-ttu-id="71e18-109">0x0000</span><span class="sxs-lookup"><span data-stu-id="71e18-109">0x0000</span></span>  <br/> |
|<span data-ttu-id="71e18-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="71e18-110">Data type:</span></span>  <br/> |<span data-ttu-id="71e18-111">PT_NULL</span><span class="sxs-lookup"><span data-stu-id="71e18-111">PT_NULL</span></span>  <br/> |
|<span data-ttu-id="71e18-112">Área:</span><span class="sxs-lookup"><span data-stu-id="71e18-112">Area:</span></span>  <br/> |<span data-ttu-id="71e18-113">Common</span><span class="sxs-lookup"><span data-stu-id="71e18-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71e18-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="71e18-114">Remarks</span></span>

<span data-ttu-id="71e18-115">Esta propiedad se usa para reservar espacio en las matrices de estructuras [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="71e18-115">This property is used to reserve space in arrays of [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="71e18-116">Se usa en una matriz de estructuras de [elemento SPropTagArray](sproptagarray.md) para indicar al método para reservar espacio en la matriz devuelta de estructuras **SPropValue** .</span><span class="sxs-lookup"><span data-stu-id="71e18-116">It is used in an array of [SPropTagArray](sproptagarray.md) structures to tell the method to reserve space in the returned array of **SPropValue** structures.</span></span> <span data-ttu-id="71e18-117">Esto permite que las propiedades calculadas que deben rellenarse una manera económica.</span><span class="sxs-lookup"><span data-stu-id="71e18-117">This allows for computed properties to be filled in an inexpensive way.</span></span> 
  
<span data-ttu-id="71e18-118">Para obtener más información, vea [Información general sobre el tipo de propiedad MAPI](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="71e18-118">For more information, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="71e18-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="71e18-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="71e18-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="71e18-120">Protocol specifications</span></span>

<span data-ttu-id="71e18-121">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71e18-121">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71e18-122">Especifica las propiedades y operaciones que se permiten en los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="71e18-122">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="71e18-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="71e18-123">Header files</span></span>

<span data-ttu-id="71e18-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="71e18-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="71e18-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="71e18-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="71e18-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="71e18-126">Mapitags.h</span></span>
  
> <span data-ttu-id="71e18-127">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="71e18-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="71e18-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="71e18-128">See also</span></span>



[<span data-ttu-id="71e18-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="71e18-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="71e18-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="71e18-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="71e18-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="71e18-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="71e18-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="71e18-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

