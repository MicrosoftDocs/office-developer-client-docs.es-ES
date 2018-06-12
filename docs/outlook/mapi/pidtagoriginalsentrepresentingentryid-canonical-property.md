---
title: Propiedad canónico PidTagOriginalSentRepresentingEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingEntryId
api_type:
- COM
ms.assetid: ece3df57-47f3-4d27-854f-b511c920ac75
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 92300733d32f021bb0ab8ab29a9676b740eeda12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819857"
---
# <a name="pidtagoriginalsentrepresentingentryid-canonical-property"></a><span data-ttu-id="27fb8-103">Propiedad canónico PidTagOriginalSentRepresentingEntryId</span><span class="sxs-lookup"><span data-stu-id="27fb8-103">PidTagOriginalSentRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="27fb8-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="27fb8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="27fb8-105">Contiene el identificador de entrada del usuario de mensajería en cuyo nombre se ha enviado el mensaje original.</span><span class="sxs-lookup"><span data-stu-id="27fb8-105">Contains the entry identifier of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="27fb8-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="27fb8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="27fb8-107">PR_ORIGINAL_SENT_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="27fb8-107">PR_ORIGINAL_SENT_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="27fb8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="27fb8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="27fb8-109">0x005E</span><span class="sxs-lookup"><span data-stu-id="27fb8-109">0x005E</span></span>  <br/> |
|<span data-ttu-id="27fb8-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="27fb8-110">Data type:</span></span>  <br/> |<span data-ttu-id="27fb8-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="27fb8-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="27fb8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="27fb8-112">Area:</span></span>  <br/> |<span data-ttu-id="27fb8-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="27fb8-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27fb8-114">Notas</span><span class="sxs-lookup"><span data-stu-id="27fb8-114">Remarks</span></span>

<span data-ttu-id="27fb8-115">Esta propiedad es una de las propiedades de direcciones para el remitente original representado de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="27fb8-115">This property is one of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="27fb8-116">Se utiliza en una secuencia de conversación.</span><span class="sxs-lookup"><span data-stu-id="27fb8-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="27fb8-117">Una aplicación cliente enviar un mensaje en nombre de otro cliente debe establecer esta propiedad en el valor de la propiedad **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) en la primera presentación del mensaje.</span><span class="sxs-lookup"><span data-stu-id="27fb8-117">A client application sending a message on behalf of another client should set this property to the value of the **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="27fb8-118">Una vez no establecida, nunca se debe cambiar.</span><span class="sxs-lookup"><span data-stu-id="27fb8-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="27fb8-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="27fb8-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="27fb8-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="27fb8-120">Protocol specifications</span></span>

<span data-ttu-id="27fb8-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27fb8-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27fb8-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="27fb8-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="27fb8-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27fb8-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27fb8-124">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="27fb8-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="27fb8-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="27fb8-125">Header files</span></span>

<span data-ttu-id="27fb8-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="27fb8-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="27fb8-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="27fb8-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="27fb8-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="27fb8-128">Mapitags.h</span></span>
  
> <span data-ttu-id="27fb8-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="27fb8-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27fb8-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="27fb8-130">See also</span></span>



[<span data-ttu-id="27fb8-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="27fb8-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="27fb8-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="27fb8-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="27fb8-133">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="27fb8-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="27fb8-134">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="27fb8-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

