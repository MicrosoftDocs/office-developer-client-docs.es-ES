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
ms.openlocfilehash: de957c33165cc96eec82bf95c8f292c5b323676a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331146"
---
# <a name="pidtagoriginalsubject-canonical-property"></a><span data-ttu-id="0556c-103">Propiedad canónica PidTagOriginalSubject</span><span class="sxs-lookup"><span data-stu-id="0556c-103">PidTagOriginalSubject Canonical Property</span></span>

  
  
<span data-ttu-id="0556c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0556c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0556c-105">Contiene el asunto de un mensaje original para su uso en un informe sobre el mensaje.</span><span class="sxs-lookup"><span data-stu-id="0556c-105">Contains the subject of an original message for use in a report about the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0556c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0556c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0556c-107">PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="0556c-107">PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="0556c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0556c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0556c-109">0x0049</span><span class="sxs-lookup"><span data-stu-id="0556c-109">0x0049</span></span>  <br/> |
|<span data-ttu-id="0556c-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0556c-110">Data type:</span></span>  <br/> |<span data-ttu-id="0556c-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0556c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0556c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0556c-112">Area:</span></span>  <br/> |<span data-ttu-id="0556c-113">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="0556c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0556c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0556c-114">Remarks</span></span>

<span data-ttu-id="0556c-115">Estas propiedades se establecen originalmente en el mismo valor que **la propiedad PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0556c-115">These properties are originally set to the same value as the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="0556c-116">Las propiedades del asunto suelen ser pequeñas cadenas de menos de 256 caracteres y un proveedor de almacén de mensajes no está obligado a admitir la interfaz **IStream** de vinculación e inserción de objetos (OLE) en ellas.</span><span class="sxs-lookup"><span data-stu-id="0556c-116">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="0556c-117">El cliente siempre debe intentar el acceso a través de la interfaz **IMAPIProp** primero y recurrir a **IStream** solo si **MAPI_E_NOT_ENOUGH_MEMORY** se devuelve.</span><span class="sxs-lookup"><span data-stu-id="0556c-117">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0556c-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0556c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0556c-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="0556c-119">Protocol specifications</span></span>

<span data-ttu-id="0556c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0556c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0556c-121">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="0556c-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0556c-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0556c-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0556c-123">Controla la sincronización de datos de objetos de mensajería entre un servidor y un cliente.</span><span class="sxs-lookup"><span data-stu-id="0556c-123">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="0556c-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0556c-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0556c-125">Especifica las propiedades y las operaciones permitidas en objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="0556c-125">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0556c-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0556c-126">Header files</span></span>

<span data-ttu-id="0556c-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0556c-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="0556c-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0556c-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="0556c-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0556c-129">Mapitags.h</span></span>
  
> <span data-ttu-id="0556c-130">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="0556c-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0556c-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="0556c-131">See also</span></span>



[<span data-ttu-id="0556c-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0556c-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0556c-133">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="0556c-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0556c-134">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0556c-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0556c-135">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="0556c-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

