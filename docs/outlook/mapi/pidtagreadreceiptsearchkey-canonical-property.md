---
title: Propiedad canónica PidTagReadReceiptSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptSearchKey
api_type:
- COM
ms.assetid: a0ea5628-1393-4ab8-bc34-a58cf130db51
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3210a8ab29127120ff139de51761bd84722ca52d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819993"
---
# <a name="pidtagreadreceiptsearchkey-canonical-property"></a><span data-ttu-id="7ad9e-103">Propiedad canónica PidTagReadReceiptSearchKey</span><span class="sxs-lookup"><span data-stu-id="7ad9e-103">PidTagReadReceiptSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="7ad9e-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7ad9e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7ad9e-105">Contiene una clave de búsqueda para el usuario de mensajería a la que el sistema de mensajería debe dirigir un informe de lectura para un mensaje.</span><span class="sxs-lookup"><span data-stu-id="7ad9e-105">Contains a search key for the messaging user to which the messaging system should direct a read report for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7ad9e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7ad9e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7ad9e-107">PR_READ_RECEIPT_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="7ad9e-107">PR_READ_RECEIPT_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="7ad9e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7ad9e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7ad9e-109">0x0053</span><span class="sxs-lookup"><span data-stu-id="7ad9e-109">0x0053</span></span>  <br/> |
|<span data-ttu-id="7ad9e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7ad9e-110">Data type:</span></span>  <br/> |<span data-ttu-id="7ad9e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7ad9e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7ad9e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7ad9e-112">Area:</span></span>  <br/> |<span data-ttu-id="7ad9e-113">Sobres MAPI</span><span class="sxs-lookup"><span data-stu-id="7ad9e-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7ad9e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7ad9e-114">Remarks</span></span>

<span data-ttu-id="7ad9e-115">Esta propiedad se omite a menos que la propiedad **PR_READ_RECEIPT_REQUESTED de MAPI** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) está establecida en TRUE.</span><span class="sxs-lookup"><span data-stu-id="7ad9e-115">This property is ignored unless the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set to TRUE.</span></span>
  
<span data-ttu-id="7ad9e-116">Si una aplicación cliente desea recibir informes de lectura propiamente dicha, puede deje sin establecer esta propiedad o establecer a la clave de búsqueda contenida en la propiedad **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) en tiempo de envío de mensaje.</span><span class="sxs-lookup"><span data-stu-id="7ad9e-116">If a client application wants to receive read reports itself, it can leave this property unset or set it to the search key contained in the **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) property at message submission time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7ad9e-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ad9e-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7ad9e-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="7ad9e-118">Protocol specifications</span></span>

<span data-ttu-id="7ad9e-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7ad9e-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7ad9e-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="7ad9e-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7ad9e-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7ad9e-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7ad9e-122">Especifica las propiedades y operaciones que se permiten en mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="7ad9e-122">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7ad9e-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7ad9e-123">Header files</span></span>

<span data-ttu-id="7ad9e-124">Mapidef.h</span><span class="sxs-lookup"><span data-stu-id="7ad9e-124">Mapidef.h</span></span>
  
> <span data-ttu-id="7ad9e-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7ad9e-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="7ad9e-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7ad9e-126">Mapitags.h</span></span>
  
> <span data-ttu-id="7ad9e-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="7ad9e-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7ad9e-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ad9e-128">See also</span></span>



[<span data-ttu-id="7ad9e-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7ad9e-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7ad9e-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="7ad9e-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7ad9e-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7ad9e-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7ad9e-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="7ad9e-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

