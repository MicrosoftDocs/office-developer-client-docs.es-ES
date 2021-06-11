---
title: Propiedad canónica PidTagIpmSentMailEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmSentMailEntryId
api_type:
- HeaderDef
ms.assetid: f6877435-6b26-4060-924f-a65591ad9538
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fd29afc93bc952bb619dfac752fae232bf7991cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437325"
---
# <a name="pidtagipmsentmailentryid-canonical-property"></a><span data-ttu-id="c48bb-103">Propiedad canónica PidTagIpmSentMailEntryId</span><span class="sxs-lookup"><span data-stu-id="c48bb-103">PidTagIpmSentMailEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="c48bb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c48bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c48bb-105">Contiene el identificador de entrada de la carpeta elementos enviados del mensaje interpersonal estándar (IPM).</span><span class="sxs-lookup"><span data-stu-id="c48bb-105">Contains the entry identifier of the standard interpersonal message (IPM) Sent Items folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c48bb-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c48bb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c48bb-107">PR_IPM_SENTMAIL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c48bb-107">PR_IPM_SENTMAIL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="c48bb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c48bb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c48bb-109">0x35E4</span><span class="sxs-lookup"><span data-stu-id="c48bb-109">0x35E4</span></span>  <br/> |
|<span data-ttu-id="c48bb-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c48bb-110">Data type:</span></span>  <br/> |<span data-ttu-id="c48bb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c48bb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c48bb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c48bb-112">Area:</span></span>  <br/> |<span data-ttu-id="c48bb-113">Carpeta</span><span class="sxs-lookup"><span data-stu-id="c48bb-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c48bb-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c48bb-114">Remarks</span></span>

<span data-ttu-id="c48bb-115">Después de enviarse, los mensajes interpersonales suelen colocarse en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="c48bb-115">After being sent, interpersonal messages are usually placed in the Sent Items folder.</span></span> <span data-ttu-id="c48bb-116">Un cliente puede usar esta propiedad para establecer la propiedad **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) en un mensaje enviado.</span><span class="sxs-lookup"><span data-stu-id="c48bb-116">A client can use this property to set the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property on a submitted message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c48bb-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c48bb-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c48bb-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c48bb-118">Header files</span></span>

<span data-ttu-id="c48bb-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c48bb-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="c48bb-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c48bb-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="c48bb-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c48bb-121">Mapitags.h</span></span>
  
> <span data-ttu-id="c48bb-122">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="c48bb-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c48bb-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c48bb-123">See also</span></span>



[<span data-ttu-id="c48bb-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c48bb-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c48bb-125">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="c48bb-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c48bb-126">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c48bb-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c48bb-127">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="c48bb-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

