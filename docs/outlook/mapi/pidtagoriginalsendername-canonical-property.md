---
title: Propiedad canónica PidTagOriginalSenderName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderName
api_type:
- COM
ms.assetid: 5e3b7764-b122-4405-be4f-7fec571c7dfc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 521fb544152dcb903450ff7dbd05ecbac808afe0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342612"
---
# <a name="pidtagoriginalsendername-canonical-property"></a><span data-ttu-id="dd895-103">Propiedad canónica PidTagOriginalSenderName</span><span class="sxs-lookup"><span data-stu-id="dd895-103">PidTagOriginalSenderName Canonical Property</span></span>

  
  
<span data-ttu-id="dd895-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd895-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd895-105">Contiene el nombre para mostrar del remitente de la primera versión de un mensaje, es decir, el mensaje antes de reenviarlo o responderlo.</span><span class="sxs-lookup"><span data-stu-id="dd895-105">Contains the display name of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dd895-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="dd895-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dd895-107">PR_ORIGINAL_SENDER_NAME, PR_ORIGINAL_SENDER_NAME_A, PR_ORIGINAL_SENDER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="dd895-107">PR_ORIGINAL_SENDER_NAME, PR_ORIGINAL_SENDER_NAME_A, PR_ORIGINAL_SENDER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="dd895-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="dd895-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dd895-109">0x005A</span><span class="sxs-lookup"><span data-stu-id="dd895-109">0x005A</span></span>  <br/> |
|<span data-ttu-id="dd895-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="dd895-110">Data type:</span></span>  <br/> |<span data-ttu-id="dd895-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dd895-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="dd895-112">Área:</span><span class="sxs-lookup"><span data-stu-id="dd895-112">Area:</span></span>  <br/> |<span data-ttu-id="dd895-113">Mensajería general</span><span class="sxs-lookup"><span data-stu-id="dd895-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd895-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dd895-114">Remarks</span></span>

<span data-ttu-id="dd895-115">Estas propiedades son ejemplos de las propiedades de dirección del remitente original de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="dd895-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="dd895-116">En el primer envío del mensaje, una aplicación cliente debe establecer estas propiedades en el valor de la **propiedad PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dd895-116">At first submission of the message, a client application should set these properties to the value of the **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) property.</span></span> <span data-ttu-id="dd895-117">Nunca se cambia cuando el mensaje se reenvía o se responde.</span><span class="sxs-lookup"><span data-stu-id="dd895-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dd895-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="dd895-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dd895-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="dd895-119">Protocol specifications</span></span>

<span data-ttu-id="dd895-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dd895-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dd895-121">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="dd895-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dd895-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dd895-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dd895-123">Especifica las propiedades y operaciones permitidas en los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="dd895-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dd895-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="dd895-124">Header files</span></span>

<span data-ttu-id="dd895-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dd895-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="dd895-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="dd895-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="dd895-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dd895-127">Mapitags.h</span></span>
  
> <span data-ttu-id="dd895-128">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="dd895-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dd895-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="dd895-129">See also</span></span>



[<span data-ttu-id="dd895-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="dd895-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dd895-131">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="dd895-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dd895-132">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="dd895-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dd895-133">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="dd895-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

