---
title: Propiedad canónica PidTagSentMailEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentMailEntryId
api_type:
- COM
ms.assetid: 8f14dc15-d7d7-4894-b6a8-0d589f576c42
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e7aef8e9ba605d47b110a496e46f629df60a28ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342514"
---
# <a name="pidtagsentmailentryid-canonical-property"></a><span data-ttu-id="4e552-103">Propiedad canónica PidTagSentMailEntryId</span><span class="sxs-lookup"><span data-stu-id="4e552-103">PidTagSentMailEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="4e552-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e552-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e552-105">Contiene el identificador de entrada de la carpeta donde se debe mover el mensaje después del envío.</span><span class="sxs-lookup"><span data-stu-id="4e552-105">Contains the entry identifier of the folder where the message should be moved after submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4e552-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4e552-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4e552-107">PR_SENTMAIL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4e552-107">PR_SENTMAIL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="4e552-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4e552-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4e552-109">0x0E0A</span><span class="sxs-lookup"><span data-stu-id="4e552-109">0x0E0A</span></span>  <br/> |
|<span data-ttu-id="4e552-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4e552-110">Data type:</span></span>  <br/> |<span data-ttu-id="4e552-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4e552-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4e552-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4e552-112">Area:</span></span>  <br/> |<span data-ttu-id="4e552-113">MAPI no transmitible</span><span class="sxs-lookup"><span data-stu-id="4e552-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e552-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4e552-114">Remarks</span></span>

<span data-ttu-id="4e552-115">Esta propiedad a menudo se copia de la **propiedad PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)), la carpeta de elementos enviados estándar de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="4e552-115">This property is often copied from the **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) property, the client application's standard Sent Items folder.</span></span>
  
<span data-ttu-id="4e552-116">La aplicación cliente usa esta propiedad con la propiedad **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) para controlar lo que sucede con un mensaje después de enviarlo.</span><span class="sxs-lookup"><span data-stu-id="4e552-116">The client application uses this property with the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="4e552-117">Uno o el otro deben establecerse, pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="4e552-117">Either one or the other should be set, but not both.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4e552-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e552-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4e552-119">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="4e552-119">Protocol specifications</span></span>

<span data-ttu-id="4e552-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e552-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e552-121">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="4e552-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4e552-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e552-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e552-123">Especifica las propiedades y las operaciones que son permisibles para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="4e552-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="4e552-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e552-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e552-125">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="4e552-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4e552-126">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4e552-126">Header files</span></span>

<span data-ttu-id="4e552-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4e552-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="4e552-128">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4e552-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="4e552-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4e552-129">Mapitags.h</span></span>
  
> <span data-ttu-id="4e552-130">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="4e552-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4e552-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e552-131">See also</span></span>



[<span data-ttu-id="4e552-132">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4e552-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4e552-133">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="4e552-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4e552-134">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4e552-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4e552-135">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="4e552-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

