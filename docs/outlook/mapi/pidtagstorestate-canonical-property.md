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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399014"
---
# <a name="pidtagstorestate-canonical-property"></a><span data-ttu-id="2b14b-103">Propiedad canónica PidTagStoreState</span><span class="sxs-lookup"><span data-stu-id="2b14b-103">PidTagStoreState Canonical Property</span></span>

  
  
<span data-ttu-id="2b14b-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b14b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b14b-105">Contiene un indicador que describe el estado del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="2b14b-105">Contains a flag that describes the state of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2b14b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2b14b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2b14b-107">PR_STORE_STATE</span><span class="sxs-lookup"><span data-stu-id="2b14b-107">PR_STORE_STATE</span></span>  <br/> |
|<span data-ttu-id="2b14b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2b14b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2b14b-109">0x340E</span><span class="sxs-lookup"><span data-stu-id="2b14b-109">0x340E</span></span>  <br/> |
|<span data-ttu-id="2b14b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2b14b-110">Data type:</span></span>  <br/> |<span data-ttu-id="2b14b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2b14b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2b14b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2b14b-112">Area:</span></span>  <br/> |<span data-ttu-id="2b14b-113">Almacén de mensajes MAPI</span><span class="sxs-lookup"><span data-stu-id="2b14b-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b14b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2b14b-114">Remarks</span></span>

<span data-ttu-id="2b14b-115">Esta propiedad es dinámica y puede cambiar en función de las acciones del usuario, a diferencia de la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2b14b-115">This property is dynamic and can change based on user actions, unlike the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="2b14b-116">Se puede establecer el siguiente valor:</span><span class="sxs-lookup"><span data-stu-id="2b14b-116">The following value can be set:</span></span>
  
<span data-ttu-id="2b14b-117">STORE_HAS_SEARCHES</span><span class="sxs-lookup"><span data-stu-id="2b14b-117">STORE_HAS_SEARCHES</span></span> 
  
> <span data-ttu-id="2b14b-118">El usuario ha creado uno o más búsquedas activas en el almacén.</span><span class="sxs-lookup"><span data-stu-id="2b14b-118">The user has created one or more active searches in the store.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="2b14b-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2b14b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2b14b-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="2b14b-120">Protocol specifications</span></span>

<span data-ttu-id="2b14b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2b14b-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2b14b-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="2b14b-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2b14b-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2b14b-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2b14b-124">Especifica las operaciones permitidas para los objetos de almacén de mensajes principales.</span><span class="sxs-lookup"><span data-stu-id="2b14b-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2b14b-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2b14b-125">Header files</span></span>

<span data-ttu-id="2b14b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2b14b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="2b14b-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2b14b-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="2b14b-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2b14b-128">Mapitags.h</span></span>
  
> <span data-ttu-id="2b14b-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="2b14b-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2b14b-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b14b-130">See also</span></span>



[<span data-ttu-id="2b14b-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2b14b-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2b14b-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="2b14b-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2b14b-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2b14b-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2b14b-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="2b14b-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

