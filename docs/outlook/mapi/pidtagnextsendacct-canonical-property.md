---
title: Propiedad canónica PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNextSendAcct
api_type:
- HeaderDef
ms.assetid: b7429c2e-0d9d-4921-9f56-9ecad817f8cb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: eff053fda58266afd5500e322559059f051d5ac3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329396"
---
# <a name="pidtagnextsendacct-canonical-property"></a><span data-ttu-id="cd751-103">Propiedad canónica PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="cd751-103">PidTagNextSendAcct Canonical Property</span></span>

  
  
<span data-ttu-id="cd751-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd751-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd751-105">Especifica el servidor que un cliente está intentando usar actualmente para enviar correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="cd751-105">Specifies the server that a client is currently attempting to use to send email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cd751-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="cd751-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cd751-107">PR_NEXT_SEND_ACCT</span><span class="sxs-lookup"><span data-stu-id="cd751-107">PR_NEXT_SEND_ACCT</span></span>  <br/> |
|<span data-ttu-id="cd751-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cd751-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cd751-109">0x0E29</span><span class="sxs-lookup"><span data-stu-id="cd751-109">0x0E29</span></span>  <br/> |
|<span data-ttu-id="cd751-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="cd751-110">Data type:</span></span>  <br/> |<span data-ttu-id="cd751-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cd751-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="cd751-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cd751-112">Area:</span></span>  <br/> |<span data-ttu-id="cd751-113">Aplicación de Outlook</span><span class="sxs-lookup"><span data-stu-id="cd751-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd751-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cd751-114">Remarks</span></span>

<span data-ttu-id="cd751-115">El formato de esta propiedad depende de la implementación.</span><span class="sxs-lookup"><span data-stu-id="cd751-115">The format of this property is implementation dependent.</span></span> <span data-ttu-id="cd751-116">El cliente puede usar esta propiedad para determinar a qué servidor dirigir el correo electrónico, pero es opcional y el valor no tiene ningún significado para el servidor.</span><span class="sxs-lookup"><span data-stu-id="cd751-116">This property can be used by the client to determine which server to direct the email to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cd751-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cd751-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cd751-118">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="cd751-118">Protocol specifications</span></span>

<span data-ttu-id="cd751-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd751-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd751-120">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="cd751-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cd751-121">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd751-121">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd751-122">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="cd751-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="cd751-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd751-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd751-124">Especifica las propiedades y operaciones permitidas para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="cd751-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cd751-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="cd751-125">Header files</span></span>

<span data-ttu-id="cd751-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cd751-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="cd751-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="cd751-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="cd751-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cd751-128">Mapitags.h</span></span>
  
> <span data-ttu-id="cd751-129">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="cd751-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cd751-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cd751-130">See also</span></span>



[<span data-ttu-id="cd751-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cd751-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cd751-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="cd751-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cd751-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="cd751-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cd751-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="cd751-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

