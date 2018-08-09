---
title: Propiedad canónica PidTagOriginalSentRepresentingSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingSearchKey
api_type:
- COM
ms.assetid: 0fb1b803-f8b4-4d6d-8e2a-836daa98ac63
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ec87e9c602d556eec37fde292fbca8f40536530e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819873"
---
# <a name="pidtagoriginalsentrepresentingsearchkey-canonical-property"></a><span data-ttu-id="88754-103">Propiedad canónica PidTagOriginalSentRepresentingSearchKey</span><span class="sxs-lookup"><span data-stu-id="88754-103">PidTagOriginalSentRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="88754-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="88754-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="88754-105">Contiene la clave de búsqueda del usuario de mensajería en cuyo nombre se ha enviado el mensaje original.</span><span class="sxs-lookup"><span data-stu-id="88754-105">Contains the search key of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="88754-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="88754-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="88754-107">PR_ORIGINAL_SENT_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="88754-107">PR_ORIGINAL_SENT_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="88754-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="88754-108">Identifier:</span></span>  <br/> |<span data-ttu-id="88754-109">0x005F</span><span class="sxs-lookup"><span data-stu-id="88754-109">0x005F</span></span>  <br/> |
|<span data-ttu-id="88754-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="88754-110">Data type:</span></span>  <br/> |<span data-ttu-id="88754-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="88754-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="88754-112">Área:</span><span class="sxs-lookup"><span data-stu-id="88754-112">Area:</span></span>  <br/> |<span data-ttu-id="88754-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="88754-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88754-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="88754-114">Remarks</span></span>

<span data-ttu-id="88754-115">Esta propiedad es una de las propiedades de direcciones para el remitente original representado de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="88754-115">This property is one of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="88754-116">Se utiliza en una secuencia de conversación.</span><span class="sxs-lookup"><span data-stu-id="88754-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="88754-117">Una aplicación cliente enviar un mensaje en nombre de otro cliente debe establecer esta propiedad en el valor de la propiedad **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) en la primera presentación del mensaje.</span><span class="sxs-lookup"><span data-stu-id="88754-117">A client application sending a message on behalf of another client should set this property to the value of the **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="88754-118">Una vez no establecida, nunca se debe cambiar.</span><span class="sxs-lookup"><span data-stu-id="88754-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="88754-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="88754-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="88754-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="88754-120">Protocol specifications</span></span>

<span data-ttu-id="88754-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88754-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88754-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="88754-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="88754-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88754-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88754-124">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="88754-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="88754-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="88754-125">Header files</span></span>

<span data-ttu-id="88754-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="88754-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="88754-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="88754-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="88754-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="88754-128">Mapitags.h</span></span>
  
> <span data-ttu-id="88754-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="88754-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="88754-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="88754-130">See also</span></span>



[<span data-ttu-id="88754-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="88754-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="88754-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="88754-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="88754-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="88754-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="88754-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="88754-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

