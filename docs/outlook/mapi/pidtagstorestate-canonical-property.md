---
title: Propiedad canónica PidTagStoreState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreState
api_type:
- COM
ms.assetid: 36e49cf5-1411-42c5-9112-09958243996d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8f00addf7abdd765d97c54350e46979f788f06ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341156"
---
# <a name="pidtagstorestate-canonical-property"></a><span data-ttu-id="a2e2f-103">Propiedad canónica PidTagStoreState</span><span class="sxs-lookup"><span data-stu-id="a2e2f-103">PidTagStoreState Canonical Property</span></span>

  
  
<span data-ttu-id="a2e2f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2e2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2e2f-105">Contiene una marca que describe el estado del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a2e2f-105">Contains a flag that describes the state of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a2e2f-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a2e2f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a2e2f-107">PR_STORE_STATE</span><span class="sxs-lookup"><span data-stu-id="a2e2f-107">PR_STORE_STATE</span></span>  <br/> |
|<span data-ttu-id="a2e2f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a2e2f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a2e2f-109">0x340E</span><span class="sxs-lookup"><span data-stu-id="a2e2f-109">0x340E</span></span>  <br/> |
|<span data-ttu-id="a2e2f-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a2e2f-110">Data type:</span></span>  <br/> |<span data-ttu-id="a2e2f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a2e2f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a2e2f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a2e2f-112">Area:</span></span>  <br/> |<span data-ttu-id="a2e2f-113">Almacén de mensajes MAPI</span><span class="sxs-lookup"><span data-stu-id="a2e2f-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2e2f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a2e2f-114">Remarks</span></span>

<span data-ttu-id="a2e2f-115">Esta propiedad es dinámica y puede cambiar en función de las acciones del usuario, a diferencia de la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a2e2f-115">This property is dynamic and can change based on user actions, unlike the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="a2e2f-116">Se puede establecer el siguiente valor:</span><span class="sxs-lookup"><span data-stu-id="a2e2f-116">The following value can be set:</span></span>
  
<span data-ttu-id="a2e2f-117">STORE_HAS_SEARCHES</span><span class="sxs-lookup"><span data-stu-id="a2e2f-117">STORE_HAS_SEARCHES</span></span> 
  
> <span data-ttu-id="a2e2f-118">El usuario ha creado una o más búsquedas activas en la tienda.</span><span class="sxs-lookup"><span data-stu-id="a2e2f-118">The user has created one or more active searches in the store.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="a2e2f-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a2e2f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a2e2f-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="a2e2f-120">Protocol specifications</span></span>

<span data-ttu-id="a2e2f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2e2f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2e2f-122">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a2e2f-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a2e2f-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2e2f-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2e2f-124">Especifica operaciones permitidas para los objetos de almacén de mensajes principales.</span><span class="sxs-lookup"><span data-stu-id="a2e2f-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a2e2f-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a2e2f-125">Header files</span></span>

<span data-ttu-id="a2e2f-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a2e2f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a2e2f-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a2e2f-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="a2e2f-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="a2e2f-128">Mapitags.h</span></span>
  
> <span data-ttu-id="a2e2f-129">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="a2e2f-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a2e2f-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2e2f-130">See also</span></span>



[<span data-ttu-id="a2e2f-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a2e2f-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a2e2f-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="a2e2f-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a2e2f-133">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a2e2f-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a2e2f-134">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="a2e2f-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

