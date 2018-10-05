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
ms.openlocfilehash: ee23e2f25370a253b914779b3bfd0ab82fd08c7e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388500"
---
# <a name="pidtagoriginalsentrepresentingsearchkey-canonical-property"></a><span data-ttu-id="74220-103">Propiedad canónica PidTagOriginalSentRepresentingSearchKey</span><span class="sxs-lookup"><span data-stu-id="74220-103">PidTagOriginalSentRepresentingSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="74220-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74220-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74220-105">Contiene la clave de búsqueda del usuario de mensajería en cuyo nombre se ha enviado el mensaje original.</span><span class="sxs-lookup"><span data-stu-id="74220-105">Contains the search key of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="74220-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="74220-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="74220-107">PR_ORIGINAL_SENT_REPRESENTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="74220-107">PR_ORIGINAL_SENT_REPRESENTING_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="74220-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="74220-108">Identifier:</span></span>  <br/> |<span data-ttu-id="74220-109">0x005F</span><span class="sxs-lookup"><span data-stu-id="74220-109">0x005F</span></span>  <br/> |
|<span data-ttu-id="74220-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="74220-110">Data type:</span></span>  <br/> |<span data-ttu-id="74220-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="74220-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="74220-112">Área:</span><span class="sxs-lookup"><span data-stu-id="74220-112">Area:</span></span>  <br/> |<span data-ttu-id="74220-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="74220-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74220-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="74220-114">Remarks</span></span>

<span data-ttu-id="74220-115">Esta propiedad es una de las propiedades de direcciones para el remitente original representado de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="74220-115">This property is one of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="74220-116">Se utiliza en una secuencia de conversación.</span><span class="sxs-lookup"><span data-stu-id="74220-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="74220-117">Una aplicación cliente enviar un mensaje en nombre de otro cliente debe establecer esta propiedad en el valor de la propiedad **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) en la primera presentación del mensaje.</span><span class="sxs-lookup"><span data-stu-id="74220-117">A client application sending a message on behalf of another client should set this property to the value of the **PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="74220-118">Una vez no establecida, nunca se debe cambiar.</span><span class="sxs-lookup"><span data-stu-id="74220-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="74220-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="74220-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="74220-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="74220-120">Protocol specifications</span></span>

<span data-ttu-id="74220-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74220-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74220-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="74220-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="74220-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74220-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74220-124">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="74220-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="74220-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="74220-125">Header files</span></span>

<span data-ttu-id="74220-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74220-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="74220-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="74220-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="74220-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="74220-128">Mapitags.h</span></span>
  
> <span data-ttu-id="74220-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="74220-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="74220-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="74220-130">See also</span></span>



[<span data-ttu-id="74220-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="74220-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="74220-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="74220-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="74220-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="74220-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="74220-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="74220-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

