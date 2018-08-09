---
title: Propiedad canónica PidTagOriginalSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSubject
api_type:
- COM
ms.assetid: 8668ba4f-3236-4a87-a5aa-9cf7eea3d87b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6cf81a5b4c10cb7bff5f03a1b25d11bbaa8ff277
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819856"
---
# <a name="pidtagoriginalsubject-canonical-property"></a><span data-ttu-id="c0a59-103">Propiedad canónica PidTagOriginalSubject</span><span class="sxs-lookup"><span data-stu-id="c0a59-103">PidTagOriginalSubject Canonical Property</span></span>

  
  
<span data-ttu-id="c0a59-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c0a59-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c0a59-105">Contiene al asunto de un mensaje para su uso en un informe sobre el mensaje original.</span><span class="sxs-lookup"><span data-stu-id="c0a59-105">Contains the subject of an original message for use in a report about the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c0a59-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c0a59-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c0a59-107">PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="c0a59-107">PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="c0a59-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c0a59-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c0a59-109">0x0049</span><span class="sxs-lookup"><span data-stu-id="c0a59-109">0x0049</span></span>  <br/> |
|<span data-ttu-id="c0a59-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c0a59-110">Data type:</span></span>  <br/> |<span data-ttu-id="c0a59-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c0a59-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c0a59-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c0a59-112">Area:</span></span>  <br/> |<span data-ttu-id="c0a59-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="c0a59-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0a59-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c0a59-114">Remarks</span></span>

<span data-ttu-id="c0a59-115">Estas propiedades se establecen originalmente en el mismo valor que la propiedad **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c0a59-115">These properties are originally set to the same value as the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="c0a59-116">Las propiedades de asunto son cadenas normalmente pequeñas de menos de 256 caracteres, y un proveedor de almacén de mensajes no está obligado a compatible con la interfaz de vinculación e incrustación de objetos (OLE) **IStream** en ellos.</span><span class="sxs-lookup"><span data-stu-id="c0a59-116">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="c0a59-117">El cliente siempre debe intentar el acceso a través de la interfaz de **IMAPIProp** en primer lugar y recurrir a **IStream** sólo si se devuelve **MAPI_E_NOT_ENOUGH_MEMORY** .</span><span class="sxs-lookup"><span data-stu-id="c0a59-117">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c0a59-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c0a59-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c0a59-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="c0a59-119">Protocol specifications</span></span>

<span data-ttu-id="c0a59-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0a59-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0a59-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c0a59-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c0a59-122">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0a59-122">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0a59-123">Controla la sincronización de datos de objeto mensajería entre un servidor y un cliente.</span><span class="sxs-lookup"><span data-stu-id="c0a59-123">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="c0a59-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c0a59-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c0a59-125">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="c0a59-125">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c0a59-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c0a59-126">Header files</span></span>

<span data-ttu-id="c0a59-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c0a59-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="c0a59-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c0a59-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="c0a59-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c0a59-129">Mapitags.h</span></span>
  
> <span data-ttu-id="c0a59-130">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c0a59-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c0a59-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0a59-131">See also</span></span>



[<span data-ttu-id="c0a59-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c0a59-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c0a59-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c0a59-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c0a59-134">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c0a59-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c0a59-135">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="c0a59-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

