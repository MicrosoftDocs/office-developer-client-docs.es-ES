---
title: Propiedad canónica PidTagInternetMessageId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetMessageId
api_type:
- HeaderDef
ms.assetid: 5c93d00c-a199-4d45-9bf6-87bd2ffe4784
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c2cc0eabd9c329953d9b0d252418549ea1c588a1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358578"
---
# <a name="pidtaginternetmessageid-canonical-property"></a><span data-ttu-id="6d848-103">Propiedad canónica PidTagInternetMessageId</span><span class="sxs-lookup"><span data-stu-id="6d848-103">PidTagInternetMessageId Canonical Property</span></span>

  
  
<span data-ttu-id="6d848-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d848-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d848-105">Corresponde al campo id. de mensaje como se especifica en [RFC2822].</span><span class="sxs-lookup"><span data-stu-id="6d848-105">Corresponds to the message ID field as specified in [RFC2822].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6d848-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="6d848-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6d848-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span><span class="sxs-lookup"><span data-stu-id="6d848-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span></span>  <br/> |
|<span data-ttu-id="6d848-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6d848-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6d848-109">0x1035</span><span class="sxs-lookup"><span data-stu-id="6d848-109">0x1035</span></span>  <br/> |
|<span data-ttu-id="6d848-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="6d848-110">Data type:</span></span>  <br/> |<span data-ttu-id="6d848-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6d848-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6d848-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6d848-112">Area:</span></span>  <br/> |<span data-ttu-id="6d848-113">MIME</span><span class="sxs-lookup"><span data-stu-id="6d848-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d848-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6d848-114">Remarks</span></span>

<span data-ttu-id="6d848-115">Estas propiedades deben estar presentes en todos los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="6d848-115">These properties should be present on all email messages.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6d848-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6d848-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6d848-117">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="6d848-117">Protocol specifications</span></span>

<span data-ttu-id="6d848-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d848-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d848-119">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="6d848-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6d848-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d848-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d848-121">Especifica las propiedades y operaciones permitidas para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="6d848-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6d848-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="6d848-122">Header files</span></span>

<span data-ttu-id="6d848-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6d848-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="6d848-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="6d848-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="6d848-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6d848-125">Mapitags.h</span></span>
  
> <span data-ttu-id="6d848-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="6d848-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6d848-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6d848-127">See also</span></span>



[<span data-ttu-id="6d848-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6d848-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6d848-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="6d848-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6d848-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="6d848-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6d848-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="6d848-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

