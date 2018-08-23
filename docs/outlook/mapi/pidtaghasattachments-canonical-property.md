---
title: Propiedad canónica PidTagHasAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagHasAttachments
api_type:
- HeaderDef
ms.assetid: fd236d74-2868-46a8-bb3d-17f8365931b6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 505f9bb80c86b956cd920348f2120f7fc8494d8b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587505"
---
# <a name="pidtaghasattachments-canonical-property"></a><span data-ttu-id="c39cf-103">Propiedad canónica PidTagHasAttachments</span><span class="sxs-lookup"><span data-stu-id="c39cf-103">PidTagHasAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="c39cf-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c39cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c39cf-105">Contiene TRUE si un mensaje contiene al menos un dato adjunto.</span><span class="sxs-lookup"><span data-stu-id="c39cf-105">Contains TRUE if a message contains at least one attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c39cf-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c39cf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c39cf-107">PR_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="c39cf-107">PR_HASATTACH</span></span>  <br/> |
|<span data-ttu-id="c39cf-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c39cf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c39cf-109">0x0E1B</span><span class="sxs-lookup"><span data-stu-id="c39cf-109">0x0E1B</span></span>  <br/> |
|<span data-ttu-id="c39cf-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c39cf-110">Data type:</span></span>  <br/> |<span data-ttu-id="c39cf-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c39cf-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c39cf-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c39cf-112">Area:</span></span>  <br/> |<span data-ttu-id="c39cf-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="c39cf-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c39cf-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c39cf-114">Remarks</span></span>

<span data-ttu-id="c39cf-115">El almacén de mensajes copia esta propiedad de la marca **MSGFLAG_HASATTACH** de la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c39cf-115">The message store copies this property from the **MSGFLAG_HASATTACH** flag of the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="c39cf-116">Una aplicación de cliente, a continuación, puede usar **PR_HASATTACH** para ordenar en datos adjuntos de mensajes en un visor de mensaje.</span><span class="sxs-lookup"><span data-stu-id="c39cf-116">A client application can then use **PR_HASATTACH** to sort on message attachments in a message viewer.</span></span> 
  
<span data-ttu-id="c39cf-117">El valor de que esta propiedad se ha actualizado con el método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="c39cf-117">The value this property is updated with the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c39cf-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c39cf-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c39cf-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="c39cf-119">Protocol specifications</span></span>

<span data-ttu-id="c39cf-120">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c39cf-120">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c39cf-121">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="c39cf-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c39cf-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c39cf-122">Header files</span></span>

<span data-ttu-id="c39cf-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c39cf-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c39cf-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c39cf-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c39cf-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c39cf-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c39cf-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c39cf-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c39cf-127">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c39cf-127">See also</span></span>



[<span data-ttu-id="c39cf-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c39cf-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c39cf-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c39cf-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c39cf-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c39cf-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c39cf-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="c39cf-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

