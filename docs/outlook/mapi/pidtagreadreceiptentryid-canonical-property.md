---
title: Propiedad canónica PidTagReadReceiptEntryId
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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 662c191f36f9ca30dcdf0f559ea5385bfe5fd305
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356528"
---
# <a name="pidtagreadreceiptentryid-canonical-property"></a><span data-ttu-id="1ae0b-103">Propiedad canónica PidTagReadReceiptEntryId</span><span class="sxs-lookup"><span data-stu-id="1ae0b-103">PidTagReadReceiptEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="1ae0b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ae0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ae0b-105">Contiene un identificador de entrada para el usuario de mensajería donde el sistema de mensajería debe dirigir un informe de lectura para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="1ae0b-105">Contains an entry identifier for the messaging user where the messaging system should direct a read report for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1ae0b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1ae0b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1ae0b-107">PR_READ_RECEIPT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1ae0b-107">PR_READ_RECEIPT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="1ae0b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1ae0b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1ae0b-109">0x0046</span><span class="sxs-lookup"><span data-stu-id="1ae0b-109">0x0046</span></span>  <br/> |
|<span data-ttu-id="1ae0b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1ae0b-110">Data type:</span></span>  <br/> |<span data-ttu-id="1ae0b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1ae0b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1ae0b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1ae0b-112">Area:</span></span>  <br/> |<span data-ttu-id="1ae0b-113">Sobre MAPI</span><span class="sxs-lookup"><span data-stu-id="1ae0b-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ae0b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1ae0b-114">Remarks</span></span>

<span data-ttu-id="1ae0b-115">Esta propiedad se omite a menos **PR_READ_RECEIPT_REQUESTED** propiedad ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) esté establecida en TRUE.</span><span class="sxs-lookup"><span data-stu-id="1ae0b-115">This property is ignored unless the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set to TRUE.</span></span>
  
<span data-ttu-id="1ae0b-116">Si una aplicación cliente desea recibir informes de lectura, puede dejar esta propiedad sin establecer o establecerla en el identificador de entrada contenido en la propiedad **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) en el momento del envío del mensaje.</span><span class="sxs-lookup"><span data-stu-id="1ae0b-116">If a client application wants to receive read reports itself, it can leave this property unset or set it to the entry identifier contained in the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property at message submission time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1ae0b-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1ae0b-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1ae0b-118">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="1ae0b-118">Protocol specifications</span></span>

<span data-ttu-id="1ae0b-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1ae0b-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1ae0b-120">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="1ae0b-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1ae0b-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1ae0b-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1ae0b-122">Especifica las propiedades y operaciones permitidas en los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1ae0b-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1ae0b-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1ae0b-123">Header files</span></span>

<span data-ttu-id="1ae0b-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1ae0b-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="1ae0b-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1ae0b-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="1ae0b-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1ae0b-126">Mapitags.h</span></span>
  
> <span data-ttu-id="1ae0b-127">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="1ae0b-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1ae0b-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1ae0b-128">See also</span></span>



[<span data-ttu-id="1ae0b-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1ae0b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1ae0b-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="1ae0b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1ae0b-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="1ae0b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1ae0b-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="1ae0b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

