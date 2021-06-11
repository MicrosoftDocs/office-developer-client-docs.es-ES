---
title: Propiedad canónica PidLidDistributionListOneOffMembers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListOneOffMembers
api_type:
- COM
ms.assetid: 0b92e654-9e2d-4c2e-9a63-d5fac603b0c0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fed4395274cb790ab8ab7ecf0456d4ecb9ec0134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335052"
---
# <a name="pidliddistributionlistoneoffmembers-canonical-property"></a><span data-ttu-id="12780-103">Propiedad canónica PidLidDistributionListOneOffMembers</span><span class="sxs-lookup"><span data-stu-id="12780-103">PidLidDistributionListOneOffMembers Canonical Property</span></span>

  
  
<span data-ttu-id="12780-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12780-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12780-105">Especifica la lista de entryids únicos que corresponden a los miembros de la lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="12780-105">Specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="12780-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="12780-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="12780-107">dispidDLOneOffMembers</span><span class="sxs-lookup"><span data-stu-id="12780-107">dispidDLOneOffMembers</span></span>  <br/> |
|<span data-ttu-id="12780-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="12780-108">Property set:</span></span>  <br/> |<span data-ttu-id="12780-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="12780-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="12780-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="12780-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="12780-111">0x00008054</span><span class="sxs-lookup"><span data-stu-id="12780-111">0x00008054</span></span>  <br/> |
|<span data-ttu-id="12780-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="12780-112">Data type:</span></span>  <br/> |<span data-ttu-id="12780-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="12780-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="12780-114">Área:</span><span class="sxs-lookup"><span data-stu-id="12780-114">Area:</span></span>  <br/> |<span data-ttu-id="12780-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="12780-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12780-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="12780-116">Remarks</span></span>

<span data-ttu-id="12780-117">Estos EntryIds únicos encapsulan los nombres para mostrar y las direcciones de correo electrónico de los miembros de la lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="12780-117">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="12780-118">Si el cliente o el servidor establecen esta propiedad, debe sincronizarse con la propiedad **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)): para cada entrada de la propiedad **dispidDLOneOffMembers,** debe haber una entrada en la misma posición en la propiedad **dispidDLMembers.**</span><span class="sxs-lookup"><span data-stu-id="12780-118">If the client or the server set this property, it must be synchronized with the **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) property: for each entry in the **dispidDLOneOffMembers** property, there must be an entry in the same position in the **dispidDLMembers** property.</span></span> 
  
<span data-ttu-id="12780-119">Al establecer **dispidDLOneOffMembers,** el cliente o el servidor deben asegurarse de que su tamaño total es inferior a 15 000 bytes de tamaño.</span><span class="sxs-lookup"><span data-stu-id="12780-119">When setting **dispidDLOneOffMembers**, the client or the server must ensure that its total size is less than 15,000 bytes in size.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="12780-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="12780-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="12780-121">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="12780-121">Protocol specifications</span></span>

<span data-ttu-id="12780-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12780-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12780-123">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="12780-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="12780-124">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12780-124">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12780-125">Especifica las propiedades y las operaciones permitidas para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="12780-125">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="12780-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="12780-126">Header files</span></span>

<span data-ttu-id="12780-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="12780-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="12780-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="12780-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="12780-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="12780-129">See also</span></span>



[<span data-ttu-id="12780-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="12780-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="12780-131">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="12780-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="12780-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="12780-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="12780-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="12780-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

