---
title: Propiedad canónica PidTagStoreEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreEntryId
api_type:
- COM
ms.assetid: 0d705667-19f4-4eda-a068-e65ea8f00d9b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7dc8ea74d36dd8aee4acec426e97d8b5e3ba2234
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278753"
---
# <a name="pidtagstoreentryid-canonical-property"></a><span data-ttu-id="2a1f0-103">Propiedad canónica PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="2a1f0-103">PidTagStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="2a1f0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a1f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a1f0-105">Contiene el identificador de entrada único del almacén de mensajes donde reside un objeto.</span><span class="sxs-lookup"><span data-stu-id="2a1f0-105">Contains the unique entry identifier of the message store where an object resides.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2a1f0-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2a1f0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2a1f0-107">PR_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2a1f0-107">PR_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="2a1f0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2a1f0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2a1f0-109">0x0FFB</span><span class="sxs-lookup"><span data-stu-id="2a1f0-109">0x0FFB</span></span>  <br/> |
|<span data-ttu-id="2a1f0-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2a1f0-110">Data type:</span></span>  <br/> |<span data-ttu-id="2a1f0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2a1f0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2a1f0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2a1f0-112">Area:</span></span>  <br/> |<span data-ttu-id="2a1f0-113">Propiedades de identificador</span><span class="sxs-lookup"><span data-stu-id="2a1f0-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a1f0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2a1f0-114">Remarks</span></span>

<span data-ttu-id="2a1f0-115">Esta propiedad se usa para abrir un almacén de mensajes con el método [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) .</span><span class="sxs-lookup"><span data-stu-id="2a1f0-115">This property is used to open a message store with the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> <span data-ttu-id="2a1f0-116">También se usa para abrir cualquier objeto que pertenece al almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="2a1f0-116">It is also used to open any object that is owned by the message store.</span></span> 
  
<span data-ttu-id="2a1f0-117">Para un almacén de mensajes, esta propiedad es idéntica a la propiedad[PidTagEntryId](pidtagentryid-canonical-property.md)del almacén. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2a1f0-117">For a message store, this property is identical to the store's own **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="2a1f0-118">Una aplicación cliente puede comparar las dos propiedades mediante el método [IMAPISession:: CompareEntryIDs](imapisession-compareentryids.md) .</span><span class="sxs-lookup"><span data-stu-id="2a1f0-118">A client application can compare the two properties using the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2a1f0-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2a1f0-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2a1f0-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="2a1f0-120">Protocol specifications</span></span>

<span data-ttu-id="2a1f0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a1f0-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a1f0-122">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="2a1f0-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2a1f0-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a1f0-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a1f0-124">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="2a1f0-124">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="2a1f0-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a1f0-125">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a1f0-126">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="2a1f0-126">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="2a1f0-127">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a1f0-127">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a1f0-128">Especifica las propiedades y operaciones relacionadas con la marcación.</span><span class="sxs-lookup"><span data-stu-id="2a1f0-128">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="2a1f0-129">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2a1f0-129">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2a1f0-130">Comparte carpetas de buzones entre clientes.</span><span class="sxs-lookup"><span data-stu-id="2a1f0-130">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2a1f0-131">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2a1f0-131">Header files</span></span>

<span data-ttu-id="2a1f0-132">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2a1f0-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="2a1f0-133">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2a1f0-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="2a1f0-134">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="2a1f0-134">Mapitags.h</span></span>
  
> <span data-ttu-id="2a1f0-135">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="2a1f0-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2a1f0-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a1f0-136">See also</span></span>



[<span data-ttu-id="2a1f0-137">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2a1f0-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2a1f0-138">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="2a1f0-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2a1f0-139">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2a1f0-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2a1f0-140">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="2a1f0-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

