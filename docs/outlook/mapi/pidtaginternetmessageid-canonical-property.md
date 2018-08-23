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
ms.openlocfilehash: 3ce5de883d28d7575a8abb83ec48454752ea7ba6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580484"
---
# <a name="pidtaginternetmessageid-canonical-property"></a><span data-ttu-id="e19a8-103">Propiedad canónica PidTagInternetMessageId</span><span class="sxs-lookup"><span data-stu-id="e19a8-103">PidTagInternetMessageId Canonical Property</span></span>

  
  
<span data-ttu-id="e19a8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e19a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e19a8-105">Se corresponde con el campo de identificador de mensaje tal como se especifica en [RFC2822].</span><span class="sxs-lookup"><span data-stu-id="e19a8-105">Corresponds to the message ID field as specified in [RFC2822].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e19a8-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e19a8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e19a8-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span><span class="sxs-lookup"><span data-stu-id="e19a8-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span></span>  <br/> |
|<span data-ttu-id="e19a8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e19a8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e19a8-109">0x1035</span><span class="sxs-lookup"><span data-stu-id="e19a8-109">0x1035</span></span>  <br/> |
|<span data-ttu-id="e19a8-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e19a8-110">Data type:</span></span>  <br/> |<span data-ttu-id="e19a8-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e19a8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e19a8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e19a8-112">Area:</span></span>  <br/> |<span data-ttu-id="e19a8-113">MIME</span><span class="sxs-lookup"><span data-stu-id="e19a8-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e19a8-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e19a8-114">Remarks</span></span>

<span data-ttu-id="e19a8-115">Estas propiedades deben estar presentes en todos los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e19a8-115">These properties should be present on all email messages.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e19a8-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e19a8-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e19a8-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e19a8-117">Protocol specifications</span></span>

<span data-ttu-id="e19a8-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e19a8-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e19a8-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e19a8-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e19a8-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e19a8-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e19a8-121">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e19a8-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e19a8-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e19a8-122">Header files</span></span>

<span data-ttu-id="e19a8-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e19a8-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e19a8-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e19a8-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e19a8-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e19a8-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e19a8-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="e19a8-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e19a8-127">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="e19a8-127">See also</span></span>



[<span data-ttu-id="e19a8-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e19a8-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e19a8-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e19a8-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e19a8-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e19a8-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e19a8-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="e19a8-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

