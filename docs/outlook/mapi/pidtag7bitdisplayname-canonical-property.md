---
title: Propiedad canónica PidTag7BitDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTag7BitDisplayName
api_type:
- HeaderDef
ms.assetid: 803d7c4e-ed80-4d5b-988f-27068a8ccd63
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4ae7645e45efb461ac53b6718569d909cec76504
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819158"
---
# <a name="pidtag7bitdisplayname-canonical-property"></a><span data-ttu-id="b75ec-103">Propiedad canónica PidTag7BitDisplayName</span><span class="sxs-lookup"><span data-stu-id="b75ec-103">PidTag7BitDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="b75ec-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b75ec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b75ec-105">Contiene una representación de ASCII de 7 bits de nombre de un usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="b75ec-105">Contains a 7-bit ASCII representation of a messaging user's name.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b75ec-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b75ec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b75ec-107">PR_7BIT_DISPLAY_NAME, PR_7BIT_DISPLAY_NAME_A, PR_7BIT_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="b75ec-107">PR_7BIT_DISPLAY_NAME, PR_7BIT_DISPLAY_NAME_A, PR_7BIT_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="b75ec-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b75ec-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b75ec-109">0x39FF</span><span class="sxs-lookup"><span data-stu-id="b75ec-109">0x39FF</span></span>  <br/> |
|<span data-ttu-id="b75ec-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b75ec-110">Data type:</span></span>  <br/> |<span data-ttu-id="b75ec-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b75ec-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b75ec-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b75ec-112">Area:</span></span>  <br/> |<span data-ttu-id="b75ec-113">Libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="b75ec-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b75ec-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b75ec-114">Remarks</span></span>

<span data-ttu-id="b75ec-115">Estas propiedades asignarán la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) en un juego de caracteres de 7 bits.</span><span class="sxs-lookup"><span data-stu-id="b75ec-115">These properties map the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property into a 7-bit character set.</span></span> <span data-ttu-id="b75ec-116">Algunos sistemas de mensajería, como Internet y algunos vínculos X.400, se limitan al conjunto de código 128 caracteres ASCII de 7 bits.</span><span class="sxs-lookup"><span data-stu-id="b75ec-116">Some messaging systems, such as Internet and certain X.400 links, are limited to the 128-character 7-bit ASCII code set.</span></span> <span data-ttu-id="b75ec-117">Las puertas de enlace a estos sistemas de mensajería pueden mejorar su rendimiento llamando al método [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) directamente para recuperar esta propiedad, lo que evita procesamiento adicional para la conversión de código.</span><span class="sxs-lookup"><span data-stu-id="b75ec-117">Gateways to such messaging systems can improve their performance by calling the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) method directly to retrieve the this property, thereby avoiding extra processing for code conversion.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b75ec-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b75ec-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b75ec-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="b75ec-119">Protocol specifications</span></span>

<span data-ttu-id="b75ec-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b75ec-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b75ec-121">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="b75ec-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b75ec-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b75ec-122">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b75ec-123">Especifica las propiedades y operaciones con listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="b75ec-123">Specifies the properties and operations on lists of users, contacts, groups and resources.</span></span>
    
<span data-ttu-id="b75ec-124">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b75ec-124">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b75ec-125">Administra las comunicaciones de un cliente con un servidor NSPI.</span><span class="sxs-lookup"><span data-stu-id="b75ec-125">Handles a client's communications with an NSPI server.</span></span>
    
<span data-ttu-id="b75ec-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b75ec-126">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b75ec-127">Controla el flujo de datos y el orden que se usa para las transferencias de datos entre cliente y servidor.</span><span class="sxs-lookup"><span data-stu-id="b75ec-127">Handles the order and data flow that is used to transfers data between client and server.</span></span>
    
<span data-ttu-id="b75ec-128">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b75ec-128">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b75ec-129">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="b75ec-129">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="b75ec-130">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b75ec-130">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b75ec-131">Especifica las propiedades y operaciones que se permiten en mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="b75ec-131">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b75ec-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b75ec-132">Header files</span></span>

<span data-ttu-id="b75ec-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b75ec-133">Mapitags.h</span></span>
  
> <span data-ttu-id="b75ec-134">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="b75ec-134">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="b75ec-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b75ec-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="b75ec-136">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b75ec-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b75ec-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="b75ec-137">See also</span></span>



[<span data-ttu-id="b75ec-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b75ec-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b75ec-139">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="b75ec-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b75ec-140">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b75ec-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b75ec-141">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="b75ec-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

