---
title: Propiedad canónico PidTagReadReceiptEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptEntryId
api_type:
- COM
ms.assetid: 141d49c8-87cf-4d80-a33b-ccbf3eeae19e
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 82bc5fd99df115527f703eff7261d02d1bf4d3ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819988"
---
# <a name="pidtagreadreceiptentryid-canonical-property"></a><span data-ttu-id="3bfc1-103">Propiedad canónico PidTagReadReceiptEntryId</span><span class="sxs-lookup"><span data-stu-id="3bfc1-103">PidTagReadReceiptEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="3bfc1-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3bfc1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3bfc1-105">Contiene un identificador de entrada para el usuario de mensajería donde el sistema de mensajería debe dirigir un informe de lectura para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-105">Contains an entry identifier for the messaging user where the messaging system should direct a read report for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3bfc1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="3bfc1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3bfc1-107">PR_READ_RECEIPT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="3bfc1-107">PR_READ_RECEIPT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="3bfc1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3bfc1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3bfc1-109">0x0046</span><span class="sxs-lookup"><span data-stu-id="3bfc1-109">0x0046</span></span>  <br/> |
|<span data-ttu-id="3bfc1-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="3bfc1-110">Data type:</span></span>  <br/> |<span data-ttu-id="3bfc1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3bfc1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3bfc1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3bfc1-112">Area:</span></span>  <br/> |<span data-ttu-id="3bfc1-113">Sobres MAPI</span><span class="sxs-lookup"><span data-stu-id="3bfc1-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3bfc1-114">Notas</span><span class="sxs-lookup"><span data-stu-id="3bfc1-114">Remarks</span></span>

<span data-ttu-id="3bfc1-115">Esta propiedad se omite a menos que la propiedad **PR_READ_RECEIPT_REQUESTED de MAPI** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) está establecida en TRUE.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-115">This property is ignored unless the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set to TRUE.</span></span>
  
<span data-ttu-id="3bfc1-116">Si una aplicación cliente desea recibir informes de lectura propiamente dicha, puede deje sin establecer esta propiedad o establecer el identificador de entrada contenida en la propiedad **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) en tiempo de envío de mensaje.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-116">If a client application wants to receive read reports itself, it can leave this property unset or set it to the entry identifier contained in the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property at message submission time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3bfc1-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3bfc1-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3bfc1-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="3bfc1-118">Protocol specifications</span></span>

<span data-ttu-id="3bfc1-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3bfc1-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3bfc1-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3bfc1-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3bfc1-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3bfc1-122">Especifica las propiedades y operaciones que se permiten en los objetos de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3bfc1-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="3bfc1-123">Header files</span></span>

<span data-ttu-id="3bfc1-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3bfc1-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="3bfc1-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="3bfc1-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3bfc1-126">Mapitags.h</span></span>
  
> <span data-ttu-id="3bfc1-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="3bfc1-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3bfc1-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="3bfc1-128">See also</span></span>



[<span data-ttu-id="3bfc1-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3bfc1-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3bfc1-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="3bfc1-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3bfc1-131">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="3bfc1-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3bfc1-132">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="3bfc1-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

