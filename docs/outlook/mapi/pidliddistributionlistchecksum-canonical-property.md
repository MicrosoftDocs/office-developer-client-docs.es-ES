---
title: Propiedad canónica PidLidDistributionListChecksum
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidLidDistributionListChecksum
api_type:
- COM
ms.assetid: bd50ab34-caae-4258-8afc-769e3cbc5220
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ac1f0d839b1ea059ec2b8d94556808bea3850862
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357613"
---
# <a name="pidliddistributionlistchecksum-canonical-property"></a><span data-ttu-id="87438-103">Propiedad canónica PidLidDistributionListChecksum</span><span class="sxs-lookup"><span data-stu-id="87438-103">PidLidDistributionListChecksum Canonical Property</span></span>

  
  
<span data-ttu-id="87438-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87438-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87438-105">Especifica la suma de comprobación de redundancia cíclica de 32 bits (CRC-32) para una lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="87438-105">Specifies the 32-bit cyclic redundancy check (CRC-32) polynomial checksum for a personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="87438-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="87438-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="87438-107">dispidDLChecksum</span><span class="sxs-lookup"><span data-stu-id="87438-107">dispidDLChecksum</span></span>  <br/> |
|<span data-ttu-id="87438-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="87438-108">Property set:</span></span>  <br/> |<span data-ttu-id="87438-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="87438-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="87438-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="87438-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="87438-111">0x0000804C</span><span class="sxs-lookup"><span data-stu-id="87438-111">0x0000804C</span></span>  <br/> |
|<span data-ttu-id="87438-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="87438-112">Data type:</span></span>  <br/> |<span data-ttu-id="87438-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="87438-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="87438-114">Área:</span><span class="sxs-lookup"><span data-stu-id="87438-114">Area:</span></span>  <br/> |<span data-ttu-id="87438-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="87438-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87438-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="87438-116">Remarks</span></span>

<span data-ttu-id="87438-117">El valor de esta propiedad se puede usar para detectar cuándo se actualizó la propiedad **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) sin actualizar las demás propiedades de miembros de la lista de distribución personal al calcular el CRC-32 en el valor existente de **dispidDLMembers** y compararlo con el valor de la propiedad **dispidDLChecksum.**</span><span class="sxs-lookup"><span data-stu-id="87438-117">The value of this property can be used to detect when the **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) property was updated without updating the other personal distribution list member properties by computing the CRC-32 on the existing value of **dispidDLMembers** and comparing it with the value of the **dispidDLChecksum** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="87438-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="87438-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="87438-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="87438-119">Protocol specifications</span></span>

<span data-ttu-id="87438-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87438-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87438-121">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="87438-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="87438-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87438-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87438-123">Especifica las propiedades y las operaciones permitidas para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="87438-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="87438-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="87438-124">Header files</span></span>

<span data-ttu-id="87438-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="87438-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="87438-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="87438-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="87438-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="87438-127">See also</span></span>



[<span data-ttu-id="87438-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="87438-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="87438-129">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="87438-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="87438-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="87438-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="87438-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="87438-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

