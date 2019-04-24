---
title: Propiedad canónica PidTagOriginalSenderEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderEntryId
api_type:
- COM
ms.assetid: bd182589-afea-4967-92f5-ba1914e4db3f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: bd32ef6540e0deec1b793bd49bab651d864754c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342619"
---
# <a name="pidtagoriginalsenderentryid-canonical-property"></a><span data-ttu-id="a6b15-103">Propiedad canónica PidTagOriginalSenderEntryId</span><span class="sxs-lookup"><span data-stu-id="a6b15-103">PidTagOriginalSenderEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="a6b15-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6b15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6b15-105">Contiene el identificador de entrada del remitente de la primera versión de un mensaje, es decir, el mensaje antes de reenviarse o responderse a él.</span><span class="sxs-lookup"><span data-stu-id="a6b15-105">Contains the entry identifier of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a6b15-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a6b15-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a6b15-107">PR_ORIGINAL_SENDER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="a6b15-107">PR_ORIGINAL_SENDER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="a6b15-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a6b15-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a6b15-109">0x005B</span><span class="sxs-lookup"><span data-stu-id="a6b15-109">0x005B</span></span>  <br/> |
|<span data-ttu-id="a6b15-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a6b15-110">Data type:</span></span>  <br/> |<span data-ttu-id="a6b15-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a6b15-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a6b15-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a6b15-112">Area:</span></span>  <br/> |<span data-ttu-id="a6b15-113">Mensajes generales</span><span class="sxs-lookup"><span data-stu-id="a6b15-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6b15-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a6b15-114">Remarks</span></span>

<span data-ttu-id="a6b15-115">Esta propiedad es una de las propiedades de dirección para el remitente original de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="a6b15-115">This property is one of the address properties for the original sender of a message.</span></span> <span data-ttu-id="a6b15-116">En el primer envío del mensaje, una aplicación cliente debe establecer esta propiedad en el valor de la propiedad **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a6b15-116">At first submission of the message, a client application should set this property to the value of the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="a6b15-117">Nunca se cambia cuando se reenvía o se responde al mensaje.</span><span class="sxs-lookup"><span data-stu-id="a6b15-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a6b15-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a6b15-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a6b15-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="a6b15-119">Protocol specifications</span></span>

<span data-ttu-id="a6b15-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a6b15-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a6b15-121">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a6b15-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a6b15-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a6b15-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a6b15-123">Especifica las propiedades y operaciones que se admiten en los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a6b15-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a6b15-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a6b15-124">Header files</span></span>

<span data-ttu-id="a6b15-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a6b15-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a6b15-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a6b15-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="a6b15-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="a6b15-127">Mapitags.h</span></span>
  
> <span data-ttu-id="a6b15-128">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="a6b15-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a6b15-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6b15-129">See also</span></span>



[<span data-ttu-id="a6b15-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a6b15-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a6b15-131">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="a6b15-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a6b15-132">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a6b15-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a6b15-133">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="a6b15-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

