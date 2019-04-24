---
title: Propiedad canónica PidTagContentUnreadCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentUnreadCount
api_type:
- HeaderDef
ms.assetid: 4fe207e9-a77f-46b9-b51d-d989847a9d02
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9572a053182aaa59020a6816736b8a4b92e778b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331874"
---
# <a name="pidtagcontentunreadcount-canonical-property"></a><span data-ttu-id="ab646-103">Propiedad canónica PidTagContentUnreadCount</span><span class="sxs-lookup"><span data-stu-id="ab646-103">PidTagContentUnreadCount Canonical Property</span></span>

  
  
<span data-ttu-id="ab646-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab646-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab646-105">Contiene el número de mensajes no leídos de una carpeta, como calcula el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ab646-105">Contains the number of unread messages in a folder, as computed by the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ab646-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ab646-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ab646-107">PR_CONTENT_UNREAD</span><span class="sxs-lookup"><span data-stu-id="ab646-107">PR_CONTENT_UNREAD</span></span>  <br/> |
|<span data-ttu-id="ab646-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ab646-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ab646-109">0x3603</span><span class="sxs-lookup"><span data-stu-id="ab646-109">0x3603</span></span>  <br/> |
|<span data-ttu-id="ab646-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ab646-110">Data type:</span></span>  <br/> |<span data-ttu-id="ab646-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ab646-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ab646-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ab646-112">Area:</span></span>  <br/> |<span data-ttu-id="ab646-113">Folder</span><span class="sxs-lookup"><span data-stu-id="ab646-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab646-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ab646-114">Remarks</span></span>

<span data-ttu-id="ab646-115">Esta propiedad calculada por el almacén de mensajes se utiliza para dos propósitos diferentes, aunque relacionados.</span><span class="sxs-lookup"><span data-stu-id="ab646-115">This property computed by the message store is used for two different, though related, purposes.</span></span> <span data-ttu-id="ab646-116">En un objeto Folder de MAPI, contiene el número de mensajes que hay en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="ab646-116">On a MAPI folder object, it contains the number of messages in a folder.</span></span> <span data-ttu-id="ab646-117">En una fila de encabezado de las tablas MAPI por categorías, contiene el número de mensajes no asociados sin leer en la categoría correspondiente a esa fila de encabezado.</span><span class="sxs-lookup"><span data-stu-id="ab646-117">In a heading row in categorized MAPI tables, it contains the number of unread non-associated messages in the category corresponding to that heading row.</span></span>
  
<span data-ttu-id="ab646-118">Esta propiedad contiene el número de mensajes de la tabla contenido de la carpeta para los que la marca MSGFLAG_READ no se establece en la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ab646-118">This property contains the number of messages in the folder contents table for which the MSGFLAG_READ flag is not set in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="ab646-119">La propiedad **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) contiene el número total de mensajes para la carpeta.</span><span class="sxs-lookup"><span data-stu-id="ab646-119">The **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) property contains the total message count for the folder.</span></span> <span data-ttu-id="ab646-120">**PR_CONTENT_COUNT** y esta propiedad son de solo lectura para los clientes.</span><span class="sxs-lookup"><span data-stu-id="ab646-120">The **PR_CONTENT_COUNT** and this property are read-only to clients.</span></span> 
  
<span data-ttu-id="ab646-121">Algunas aplicaciones cliente muestran la fila de encabezado de una categoría de forma diferente según el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="ab646-121">Some client applications display the heading row of a category differently depending on the value of this property.</span></span> <span data-ttu-id="ab646-122">Por ejemplo, un cliente puede mostrar una categoría que incluya los mensajes no leídos en negrita.</span><span class="sxs-lookup"><span data-stu-id="ab646-122">For example, a client can display a category that includes unread messages in bold.</span></span> <span data-ttu-id="ab646-123">Esta propiedad no se puede usar como categoría y un intento de hacerlo da como resultado el valor MAPI_E_INVALID_PARAMETER que se devuelve desde el método [IMAPITable:: SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="ab646-123">This property cannot be used as a category and an attempt to do so results in the MAPI_E_INVALID_PARAMETER value being returned from the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ab646-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ab646-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ab646-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="ab646-125">Protocol specifications</span></span>

<span data-ttu-id="ab646-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab646-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab646-127">Proporciona referencias a especificaciones del Protocolo de Microsoft Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ab646-127">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ab646-128">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab646-128">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab646-129">Controla las operaciones de carpeta.</span><span class="sxs-lookup"><span data-stu-id="ab646-129">Handles folder operations.</span></span>
    
<span data-ttu-id="ab646-130">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab646-130">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab646-131">Incluye operaciones admitidas para los objetos de la tabla principal.</span><span class="sxs-lookup"><span data-stu-id="ab646-131">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ab646-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ab646-132">Header files</span></span>

<span data-ttu-id="ab646-133">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ab646-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="ab646-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ab646-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="ab646-135">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="ab646-135">Mapitags.h</span></span>
  
> <span data-ttu-id="ab646-136">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="ab646-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ab646-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab646-137">See also</span></span>



[<span data-ttu-id="ab646-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ab646-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ab646-139">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="ab646-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ab646-140">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="ab646-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ab646-141">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="ab646-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

