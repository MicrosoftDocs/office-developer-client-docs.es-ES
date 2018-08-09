---
title: Propiedad canónica PidTagOriginalAuthorName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorNam
api_type:
- COM
ms.assetid: beb23742-d844-4d90-9b13-1ad376d4206c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4b2f47f503caa32a1bdcd287e2fa5e894d667573
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819803"
---
# <a name="pidtagoriginalauthorname-canonical-property"></a><span data-ttu-id="e5806-103">Propiedad canónica PidTagOriginalAuthorName</span><span class="sxs-lookup"><span data-stu-id="e5806-103">PidTagOriginalAuthorName Canonical Property</span></span>

  
  
<span data-ttu-id="e5806-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e5806-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e5806-105">Contiene el nombre para mostrar del autor de la primera versión de un mensaje, es decir, el mensaje antes de que se reenvía o se responde a.</span><span class="sxs-lookup"><span data-stu-id="e5806-105">Contains the display name of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e5806-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e5806-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e5806-107">PR_ORIGINAL_AUTHOR_NAME, PR_ORIGINAL_AUTHOR_NAME_A, PR_ORIGINAL_AUTHOR_NAME_W</span><span class="sxs-lookup"><span data-stu-id="e5806-107">PR_ORIGINAL_AUTHOR_NAME, PR_ORIGINAL_AUTHOR_NAME_A, PR_ORIGINAL_AUTHOR_NAME_W</span></span>  <br/> |
|<span data-ttu-id="e5806-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e5806-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e5806-109">0x004D</span><span class="sxs-lookup"><span data-stu-id="e5806-109">0x004D</span></span>  <br/> |
|<span data-ttu-id="e5806-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e5806-110">Data type:</span></span>  <br/> |<span data-ttu-id="e5806-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="e5806-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="e5806-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e5806-112">Area:</span></span>  <br/> |<span data-ttu-id="e5806-113">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="e5806-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5806-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e5806-114">Remarks</span></span>

<span data-ttu-id="e5806-115">Estas propiedades son ejemplos de las propiedades de dirección para el autor de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="e5806-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="e5806-116">En el primer envío del mensaje, la aplicación cliente debe establecer estas propiedades en el valor de **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e5806-116">At first submission of the message, the client application should set these properties to the value of **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span></span> <span data-ttu-id="e5806-117">Nunca se ha cambiado cuando el mensaje se reenvía o se responde a.</span><span class="sxs-lookup"><span data-stu-id="e5806-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="e5806-118">Permitir que las propiedades autor original para la conservación de la información desde fuera del dominio de mensajería local.</span><span class="sxs-lookup"><span data-stu-id="e5806-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="e5806-119">Cuando un mensaje llega desde otro dominio de mensajería, como desde Internet, estas propiedades proporcionan una forma de garantizar que no se pierda la información original.</span><span class="sxs-lookup"><span data-stu-id="e5806-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e5806-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e5806-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e5806-121">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e5806-121">Protocol specifications</span></span>

<span data-ttu-id="e5806-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5806-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e5806-123">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e5806-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e5806-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5806-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e5806-125">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="e5806-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e5806-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e5806-126">Header files</span></span>

<span data-ttu-id="e5806-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e5806-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="e5806-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e5806-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="e5806-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e5806-129">Mapitags.h</span></span>
  
> <span data-ttu-id="e5806-130">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="e5806-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e5806-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5806-131">See also</span></span>



[<span data-ttu-id="e5806-132">Propiedad canónica PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="e5806-132">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)


[<span data-ttu-id="e5806-133">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e5806-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e5806-134">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e5806-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e5806-135">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e5806-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e5806-136">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="e5806-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

