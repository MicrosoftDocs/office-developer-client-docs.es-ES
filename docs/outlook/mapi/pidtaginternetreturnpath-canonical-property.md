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
ms.openlocfilehash: c2d8eaf627f789c3e862a83d71e4ca2e3e55e1e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327961"
---
# <a name="pidtaginternetreturnpath-canonical-property"></a><span data-ttu-id="84d4b-103">Propiedad canónica PidTagInternetReturnPath</span><span class="sxs-lookup"><span data-stu-id="84d4b-103">PidTagInternetReturnPath Canonical Property</span></span>

  
  
<span data-ttu-id="84d4b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84d4b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84d4b-105">Contiene el valor del campo de encabezado de un mensaje Return-Path multipropósito de correo de Internet (MIME).</span><span class="sxs-lookup"><span data-stu-id="84d4b-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's Return-Path header field.</span></span> <span data-ttu-id="84d4b-106">La dirección de correo electrónico del remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="84d4b-106">The email address of the message's sender.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="84d4b-107">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="84d4b-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="84d4b-108">PR_INTERNET_RETURN_PATH, PR_INTERNET_RETURN_PATH_A, PR_INTERNET_RETURN_PATH_W</span><span class="sxs-lookup"><span data-stu-id="84d4b-108">PR_INTERNET_RETURN_PATH, PR_INTERNET_RETURN_PATH_A, PR_INTERNET_RETURN_PATH_W</span></span>  <br/> |
|<span data-ttu-id="84d4b-109">Identificador:</span><span class="sxs-lookup"><span data-stu-id="84d4b-109">Identifier:</span></span>  <br/> |<span data-ttu-id="84d4b-110">0x1046</span><span class="sxs-lookup"><span data-stu-id="84d4b-110">0x1046</span></span>  <br/> |
|<span data-ttu-id="84d4b-111">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="84d4b-111">Data type:</span></span>  <br/> |<span data-ttu-id="84d4b-112">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="84d4b-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="84d4b-113">Área:</span><span class="sxs-lookup"><span data-stu-id="84d4b-113">Area:</span></span>  <br/> |<span data-ttu-id="84d4b-114">MIME</span><span class="sxs-lookup"><span data-stu-id="84d4b-114">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84d4b-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="84d4b-115">Remarks</span></span>

<span data-ttu-id="84d4b-116">Para recuperar el valor de esta propiedad, use primero [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad y, a continuación, especifique esta etiqueta de propiedad en [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor.</span><span class="sxs-lookup"><span data-stu-id="84d4b-116">To retrieve the value of this property, first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="84d4b-117">Al llamar [a IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique los siguientes valores para la estructura [MAPINAMEID](mapinameid.md) señalada por el parámetro de entrada  _lppPropNames_:</span><span class="sxs-lookup"><span data-stu-id="84d4b-117">When calling [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), specify the following values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="84d4b-118">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="84d4b-118">lpGuid:</span></span>  <br/> |<span data-ttu-id="84d4b-119">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="84d4b-119">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="84d4b-120">ulKind:</span><span class="sxs-lookup"><span data-stu-id="84d4b-120">ulKind:</span></span>  <br/> |<span data-ttu-id="84d4b-121">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="84d4b-121">MNID_STRING</span></span>  <br/> |
|<span data-ttu-id="84d4b-122">Kind.lpwstrName:</span><span class="sxs-lookup"><span data-stu-id="84d4b-122">Kind.lpwstrName:</span></span>  <br/> |<span data-ttu-id="84d4b-123">L"return-path"</span><span class="sxs-lookup"><span data-stu-id="84d4b-123">L"return-path"</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="84d4b-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="84d4b-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="84d4b-125">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="84d4b-125">Protocol specifications</span></span>

<span data-ttu-id="84d4b-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84d4b-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84d4b-127">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="84d4b-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="84d4b-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84d4b-128">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84d4b-129">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="84d4b-129">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="84d4b-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="84d4b-130">Header files</span></span>

<span data-ttu-id="84d4b-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="84d4b-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="84d4b-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="84d4b-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="84d4b-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="84d4b-133">Mapitags.h</span></span>
  
> <span data-ttu-id="84d4b-134">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="84d4b-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84d4b-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="84d4b-135">See also</span></span>



[<span data-ttu-id="84d4b-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="84d4b-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="84d4b-137">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="84d4b-137">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="84d4b-138">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="84d4b-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="84d4b-139">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="84d4b-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="84d4b-140">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="84d4b-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

