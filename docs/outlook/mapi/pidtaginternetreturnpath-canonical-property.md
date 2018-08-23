---
title: Propiedad canónica PidTagInternetReturnPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetReturnPath
api_type:
- HeaderDef
ms.assetid: 4530dbcf-9436-4f29-b79e-1bb0f791f60b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b3f108ff1053c0aa1046597cd2f11b74bc2dab0c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574177"
---
# <a name="pidtaginternetreturnpath-canonical-property"></a><span data-ttu-id="8ee93-103">Propiedad canónica PidTagInternetReturnPath</span><span class="sxs-lookup"><span data-stu-id="8ee93-103">PidTagInternetReturnPath Canonical Property</span></span>

  
  
<span data-ttu-id="8ee93-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ee93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ee93-105">Contiene el valor del campo de encabezado de un mensaje de extensiones multipropósito de correo Internet (MIME) Return-Path.</span><span class="sxs-lookup"><span data-stu-id="8ee93-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's Return-Path header field.</span></span> <span data-ttu-id="8ee93-106">La dirección de correo electrónico del remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="8ee93-106">The email address of the message's sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8ee93-107">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8ee93-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="8ee93-108">PR_INTERNET_RETURN_PATH, PR_INTERNET_RETURN_PATH_A, PR_INTERNET_RETURN_PATH_W</span><span class="sxs-lookup"><span data-stu-id="8ee93-108">PR_INTERNET_RETURN_PATH, PR_INTERNET_RETURN_PATH_A, PR_INTERNET_RETURN_PATH_W</span></span>  <br/> |
|<span data-ttu-id="8ee93-109">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8ee93-109">Identifier:</span></span>  <br/> |<span data-ttu-id="8ee93-110">0x1046</span><span class="sxs-lookup"><span data-stu-id="8ee93-110">0x1046</span></span>  <br/> |
|<span data-ttu-id="8ee93-111">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8ee93-111">Data type:</span></span>  <br/> |<span data-ttu-id="8ee93-112">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8ee93-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8ee93-113">Área:</span><span class="sxs-lookup"><span data-stu-id="8ee93-113">Area:</span></span>  <br/> |<span data-ttu-id="8ee93-114">MIME</span><span class="sxs-lookup"><span data-stu-id="8ee93-114">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ee93-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8ee93-115">Remarks</span></span>

<span data-ttu-id="8ee93-116">Para recuperar el valor de esta propiedad, en primer lugar utilice [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad y, a continuación, especifique esta etiqueta de propiedad en [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor.</span><span class="sxs-lookup"><span data-stu-id="8ee93-116">To retrieve the value of this property, first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="8ee93-117">Cuando se llama a [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique los siguientes valores de la estructura [MAPINAMEID](mapinameid.md) señalado por el parámetro de entrada _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="8ee93-117">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8ee93-118">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="8ee93-118">lpGuid:</span></span>  <br/> |<span data-ttu-id="8ee93-119">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="8ee93-119">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="8ee93-120">ulKind:</span><span class="sxs-lookup"><span data-stu-id="8ee93-120">ulKind:</span></span>  <br/> |<span data-ttu-id="8ee93-121">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="8ee93-121">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="8ee93-122">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="8ee93-122">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="8ee93-123">L "return-path"</span><span class="sxs-lookup"><span data-stu-id="8ee93-123">L"return-path"</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="8ee93-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8ee93-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8ee93-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="8ee93-125">Protocol specifications</span></span>

<span data-ttu-id="8ee93-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ee93-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8ee93-127">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8ee93-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8ee93-128">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8ee93-128">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8ee93-129">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="8ee93-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8ee93-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8ee93-130">Header files</span></span>

<span data-ttu-id="8ee93-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8ee93-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="8ee93-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8ee93-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="8ee93-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8ee93-133">Mapitags.h</span></span>
  
> <span data-ttu-id="8ee93-134">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="8ee93-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8ee93-135">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="8ee93-135">See also</span></span>



[<span data-ttu-id="8ee93-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8ee93-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8ee93-137">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="8ee93-137">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="8ee93-138">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="8ee93-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8ee93-139">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8ee93-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8ee93-140">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="8ee93-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

