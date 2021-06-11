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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356472"
---
# <a name="pidtagreadreceiptrequested-canonical-property"></a><span data-ttu-id="17c5e-103">Propiedad canónica PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="17c5e-103">PidTagReadReceiptRequested Canonical Property</span></span>

  
  
<span data-ttu-id="17c5e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17c5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17c5e-105">Contiene TRUE si un remitente de mensajes desea que el sistema de mensajería genere un informe de lectura cuando el destinatario haya leído un mensaje.</span><span class="sxs-lookup"><span data-stu-id="17c5e-105">Contains TRUE if a message sender wants the messaging system to generate a read report when the recipient has read a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="17c5e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="17c5e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="17c5e-107">PR_READ_RECEIPT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="17c5e-107">PR_READ_RECEIPT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="17c5e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="17c5e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="17c5e-109">0x0029</span><span class="sxs-lookup"><span data-stu-id="17c5e-109">0x0029</span></span>  <br/> |
|<span data-ttu-id="17c5e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="17c5e-110">Data type:</span></span>  <br/> |<span data-ttu-id="17c5e-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="17c5e-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="17c5e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="17c5e-112">Area:</span></span>  <br/> |<span data-ttu-id="17c5e-113">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="17c5e-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17c5e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="17c5e-114">Remarks</span></span>

<span data-ttu-id="17c5e-115">Esta propiedad debe establecerse en TRUE para validar los valores de las propiedades **PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)) y **PR_READ_RECEIPT_SEARCH_KEY** ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="17c5e-115">This property must be set to TRUE to validate the values in the **PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)) and **PR_READ_RECEIPT_SEARCH_KEY** ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="17c5e-116">Si un mensaje **con PR_READ_RECEIPT_REQUESTED** se elimina o expira antes de que el sistema de mensajería pueda generar un informe de lectura, se genera un informe no leído.</span><span class="sxs-lookup"><span data-stu-id="17c5e-116">If a message with **PR_READ_RECEIPT_REQUESTED** set is deleted or expires before the messaging system can generate a read report, a nonread report is generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="17c5e-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="17c5e-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="17c5e-118">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="17c5e-118">Protocol specifications</span></span>

<span data-ttu-id="17c5e-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17c5e-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17c5e-120">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="17c5e-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="17c5e-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17c5e-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17c5e-122">Especifica las propiedades y las operaciones que son permisibles para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="17c5e-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="17c5e-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="17c5e-123">Header files</span></span>

<span data-ttu-id="17c5e-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="17c5e-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="17c5e-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="17c5e-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="17c5e-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="17c5e-126">Mapitags.h</span></span>
  
> <span data-ttu-id="17c5e-127">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="17c5e-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="17c5e-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="17c5e-128">See also</span></span>



[<span data-ttu-id="17c5e-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="17c5e-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="17c5e-130">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="17c5e-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="17c5e-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="17c5e-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="17c5e-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="17c5e-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

