---
title: Propiedad canónica PidTagOriginalSentRepresentingEntryId
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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: eaf91472794c5188a63897bccaa900c4882407bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341758"
---
# <a name="pidtagoriginalsentrepresentingentryid-canonical-property"></a><span data-ttu-id="37afb-103">Propiedad canónica PidTagOriginalSentRepresentingEntryId</span><span class="sxs-lookup"><span data-stu-id="37afb-103">PidTagOriginalSentRepresentingEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="37afb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37afb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37afb-105">Contiene el identificador de entrada del usuario de mensajería en cuyo nombre se envió el mensaje original.</span><span class="sxs-lookup"><span data-stu-id="37afb-105">Contains the entry identifier of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="37afb-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="37afb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="37afb-107">PR_ORIGINAL_SENT_REPRESENTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="37afb-107">PR_ORIGINAL_SENT_REPRESENTING_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="37afb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="37afb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="37afb-109">0x005E</span><span class="sxs-lookup"><span data-stu-id="37afb-109">0x005E</span></span>  <br/> |
|<span data-ttu-id="37afb-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="37afb-110">Data type:</span></span>  <br/> |<span data-ttu-id="37afb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="37afb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="37afb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="37afb-112">Area:</span></span>  <br/> |<span data-ttu-id="37afb-113">Mensajes generales</span><span class="sxs-lookup"><span data-stu-id="37afb-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37afb-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="37afb-114">Remarks</span></span>

<span data-ttu-id="37afb-115">Esta propiedad es una de las propiedades de dirección para el remitente representado original de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="37afb-115">This property is one of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="37afb-116">Se usa en un hilo de conversación.</span><span class="sxs-lookup"><span data-stu-id="37afb-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="37afb-117">Una aplicación cliente que envía un mensaje en nombre de otro cliente debe establecer esta propiedad en el valor de la propiedad **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) en el primer envío del mensaje.</span><span class="sxs-lookup"><span data-stu-id="37afb-117">A client application sending a message on behalf of another client should set this property to the value of the **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="37afb-118">Una vez establecido, nunca debe cambiarse.</span><span class="sxs-lookup"><span data-stu-id="37afb-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="37afb-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="37afb-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="37afb-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="37afb-120">Protocol specifications</span></span>

<span data-ttu-id="37afb-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37afb-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37afb-122">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="37afb-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="37afb-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="37afb-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="37afb-124">Especifica las propiedades y operaciones que se admiten en los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="37afb-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="37afb-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="37afb-125">Header files</span></span>

<span data-ttu-id="37afb-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="37afb-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="37afb-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="37afb-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="37afb-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="37afb-128">Mapitags.h</span></span>
  
> <span data-ttu-id="37afb-129">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="37afb-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="37afb-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="37afb-130">See also</span></span>



[<span data-ttu-id="37afb-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="37afb-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="37afb-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="37afb-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="37afb-133">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="37afb-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="37afb-134">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="37afb-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

