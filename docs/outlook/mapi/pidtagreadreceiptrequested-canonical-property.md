---
title: Propiedad canónica PidTagReadReceiptRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptRequested
api_type:
- COM
ms.assetid: 7db0645b-f3ab-4fc4-b865-68c952aeb359
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0e49b73c777988ad3559a442af920af3d8f4bdbb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385112"
---
# <a name="pidtagreadreceiptrequested-canonical-property"></a><span data-ttu-id="0245d-103">Propiedad canónica PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="0245d-103">PidTagReadReceiptRequested Canonical Property</span></span>

  
  
<span data-ttu-id="0245d-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0245d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0245d-105">Contiene TRUE si desea que el sistema de mensajería para generar un informe de lectura cuando el destinatario leyó un mensaje de un remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="0245d-105">Contains TRUE if a message sender wants the messaging system to generate a read report when the recipient has read a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0245d-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0245d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0245d-107">PR_READ_RECEIPT_REQUESTED DE MAPI</span><span class="sxs-lookup"><span data-stu-id="0245d-107">PR_READ_RECEIPT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="0245d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0245d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0245d-109">0x0029</span><span class="sxs-lookup"><span data-stu-id="0245d-109">0x0029</span></span>  <br/> |
|<span data-ttu-id="0245d-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0245d-110">Data type:</span></span>  <br/> |<span data-ttu-id="0245d-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0245d-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0245d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0245d-112">Area:</span></span>  <br/> |<span data-ttu-id="0245d-113">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="0245d-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0245d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0245d-114">Remarks</span></span>

<span data-ttu-id="0245d-115">Esta propiedad debe establecerse en TRUE para validar los valores de las propiedades de **PR_READ_RECEIPT_SEARCH_KEY** ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)) y **PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0245d-115">This property must be set to TRUE to validate the values in the **PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)) and **PR_READ_RECEIPT_SEARCH_KEY** ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="0245d-116">Si un mensaje con el conjunto de **PR_READ_RECEIPT_REQUESTED de MAPI** se elimina o expira antes de que el sistema de mensajería puede generar un informe de lectura, se genera un informe nonread.</span><span class="sxs-lookup"><span data-stu-id="0245d-116">If a message with **PR_READ_RECEIPT_REQUESTED** set is deleted or expires before the messaging system can generate a read report, a nonread report is generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0245d-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0245d-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0245d-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="0245d-118">Protocol specifications</span></span>

<span data-ttu-id="0245d-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0245d-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0245d-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0245d-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0245d-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0245d-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0245d-122">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="0245d-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0245d-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0245d-123">Header files</span></span>

<span data-ttu-id="0245d-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0245d-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="0245d-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0245d-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="0245d-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0245d-126">Mapitags.h</span></span>
  
> <span data-ttu-id="0245d-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="0245d-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0245d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0245d-128">See also</span></span>



[<span data-ttu-id="0245d-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0245d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0245d-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="0245d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0245d-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0245d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0245d-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="0245d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

