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
ms.openlocfilehash: ae6202a1fdf7ec43bf2269236aa8120aa67e3c50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818634"
---
# <a name="pidliddistributionlistoneoffmembers-canonical-property"></a><span data-ttu-id="bbebe-103">Propiedad canónica PidLidDistributionListOneOffMembers</span><span class="sxs-lookup"><span data-stu-id="bbebe-103">PidLidDistributionListOneOffMembers Canonical Property</span></span>

  
  
<span data-ttu-id="bbebe-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bbebe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bbebe-105">Especifica la lista de identificadores de uso único que corresponden a los miembros de la lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="bbebe-105">Specifies the list of one-off EntryIds that correspond to the members of the personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bbebe-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="bbebe-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bbebe-107">dispidDLOneOffMembers</span><span class="sxs-lookup"><span data-stu-id="bbebe-107">dispidDLOneOffMembers</span></span>  <br/> |
|<span data-ttu-id="bbebe-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="bbebe-108">Property set:</span></span>  <br/> |<span data-ttu-id="bbebe-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="bbebe-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="bbebe-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="bbebe-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bbebe-111">0x00008054</span><span class="sxs-lookup"><span data-stu-id="bbebe-111">0x00008054</span></span>  <br/> |
|<span data-ttu-id="bbebe-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="bbebe-112">Data type:</span></span>  <br/> |<span data-ttu-id="bbebe-113">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="bbebe-113">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="bbebe-114">Área:</span><span class="sxs-lookup"><span data-stu-id="bbebe-114">Area:</span></span>  <br/> |<span data-ttu-id="bbebe-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="bbebe-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bbebe-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bbebe-116">Remarks</span></span>

<span data-ttu-id="bbebe-117">Estos identificadores de uso único encapsulan para mostrar los nombres y direcciones de correo electrónico de los miembros de la lista de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="bbebe-117">These one-off EntryIds encapsulate display names and email addresses of the personal distribution list members.</span></span>
  
<span data-ttu-id="bbebe-118">Si el cliente o el servidor establece esta propiedad, se debe sincronizar con la propiedad **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)): para cada entrada en la propiedad **dispidDLOneOffMembers** , debe haber una entrada en la misma posición en la propiedad **dispidDLMembers** .</span><span class="sxs-lookup"><span data-stu-id="bbebe-118">If the client or the server set this property, it must be synchronized with the **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) property: for each entry in the **dispidDLOneOffMembers** property, there must be an entry in the same position in the **dispidDLMembers** property.</span></span> 
  
<span data-ttu-id="bbebe-119">Al establecer **dispidDLOneOffMembers**, el cliente o el servidor debe asegurarse de que su tamaño total es menor de tamaño 15.000 bytes.</span><span class="sxs-lookup"><span data-stu-id="bbebe-119">When setting **dispidDLOneOffMembers**, the client or the server must ensure that its total size is less than 15,000 bytes in size.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bbebe-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bbebe-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bbebe-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="bbebe-121">Protocol specifications</span></span>

<span data-ttu-id="bbebe-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbebe-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bbebe-123">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="bbebe-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bbebe-124">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbebe-124">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bbebe-125">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="bbebe-125">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bbebe-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="bbebe-126">Header files</span></span>

<span data-ttu-id="bbebe-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bbebe-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="bbebe-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="bbebe-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bbebe-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="bbebe-129">See also</span></span>



[<span data-ttu-id="bbebe-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bbebe-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bbebe-131">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="bbebe-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bbebe-132">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="bbebe-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bbebe-133">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="bbebe-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

