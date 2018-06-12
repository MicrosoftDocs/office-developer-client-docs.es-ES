---
title: Propiedad canónico PidTagOriginalSubject
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 6cf81a5b4c10cb7bff5f03a1b25d11bbaa8ff277
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819856"
---
# <a name="pidtagoriginalsubject-canonical-property"></a><span data-ttu-id="1a815-103">Propiedad canónico PidTagOriginalSubject</span><span class="sxs-lookup"><span data-stu-id="1a815-103">PidTagOriginalSubject Canonical Property</span></span>

  
  
<span data-ttu-id="1a815-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1a815-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1a815-105">Contiene al asunto de un mensaje para su uso en un informe sobre el mensaje original.</span><span class="sxs-lookup"><span data-stu-id="1a815-105">Contains the subject of an original message for use in a report about the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1a815-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1a815-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1a815-107">PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="1a815-107">PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="1a815-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1a815-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1a815-109">0x0049</span><span class="sxs-lookup"><span data-stu-id="1a815-109">0x0049</span></span>  <br/> |
|<span data-ttu-id="1a815-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1a815-110">Data type:</span></span>  <br/> |<span data-ttu-id="1a815-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1a815-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1a815-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1a815-112">Area:</span></span>  <br/> |<span data-ttu-id="1a815-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="1a815-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a815-114">Notas</span><span class="sxs-lookup"><span data-stu-id="1a815-114">Remarks</span></span>

<span data-ttu-id="1a815-115">Estas propiedades se establecen originalmente en el mismo valor que la propiedad **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1a815-115">These properties are originally set to the same value as the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="1a815-116">Las propiedades de asunto son cadenas normalmente pequeñas de menos de 256 caracteres, y un proveedor de almacén de mensajes no está obligado a compatible con la interfaz de vinculación e incrustación de objetos (OLE) **IStream** en ellos.</span><span class="sxs-lookup"><span data-stu-id="1a815-116">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="1a815-117">El cliente siempre debe intentar el acceso a través de la interfaz de **IMAPIProp** en primer lugar y recurrir a **IStream** sólo si se devuelve **MAPI_E_NOT_ENOUGH_MEMORY** .</span><span class="sxs-lookup"><span data-stu-id="1a815-117">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1a815-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1a815-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1a815-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="1a815-119">Protocol specifications</span></span>

<span data-ttu-id="1a815-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a815-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a815-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1a815-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1a815-122">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a815-122">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a815-123">Controla la sincronización de datos de objeto mensajería entre un servidor y un cliente.</span><span class="sxs-lookup"><span data-stu-id="1a815-123">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="1a815-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a815-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a815-125">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1a815-125">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1a815-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1a815-126">Header files</span></span>

<span data-ttu-id="1a815-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1a815-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="1a815-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1a815-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="1a815-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1a815-129">Mapitags.h</span></span>
  
> <span data-ttu-id="1a815-130">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="1a815-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a815-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="1a815-131">See also</span></span>



[<span data-ttu-id="1a815-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1a815-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1a815-133">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="1a815-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1a815-134">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="1a815-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1a815-135">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="1a815-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

