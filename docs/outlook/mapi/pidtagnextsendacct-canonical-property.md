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
ms.openlocfilehash: 76584e248f03deac62af94e4638fcead15594b3e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581135"
---
# <a name="pidtagnextsendacct-canonical-property"></a><span data-ttu-id="494b9-103">Propiedad canónica PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="494b9-103">PidTagNextSendAcct Canonical Property</span></span>

  
  
<span data-ttu-id="494b9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="494b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="494b9-105">Especifica el servidor en el que un cliente actualmente está intentando utilizar para enviar correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="494b9-105">Specifies the server that a client is currently attempting to use to send email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="494b9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="494b9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="494b9-107">PR_NEXT_SEND_ACCT</span><span class="sxs-lookup"><span data-stu-id="494b9-107">PR_NEXT_SEND_ACCT</span></span>  <br/> |
|<span data-ttu-id="494b9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="494b9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="494b9-109">0x0E29</span><span class="sxs-lookup"><span data-stu-id="494b9-109">0x0E29</span></span>  <br/> |
|<span data-ttu-id="494b9-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="494b9-110">Data type:</span></span>  <br/> |<span data-ttu-id="494b9-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="494b9-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="494b9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="494b9-112">Area:</span></span>  <br/> |<span data-ttu-id="494b9-113">Aplicación de Outlook</span><span class="sxs-lookup"><span data-stu-id="494b9-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="494b9-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="494b9-114">Remarks</span></span>

<span data-ttu-id="494b9-115">El formato de esta propiedad es depende de la implementación.</span><span class="sxs-lookup"><span data-stu-id="494b9-115">The format of this property is implementation dependent.</span></span> <span data-ttu-id="494b9-116">Esta propiedad se puede usar el cliente para determinar en qué servidor para dirigir el correo electrónico a, pero es opcional y el valor no tiene ningún significado para el servidor.</span><span class="sxs-lookup"><span data-stu-id="494b9-116">This property can be used by the client to determine which server to direct the email to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="494b9-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="494b9-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="494b9-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="494b9-118">Protocol specifications</span></span>

<span data-ttu-id="494b9-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="494b9-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="494b9-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="494b9-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="494b9-121">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="494b9-121">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="494b9-122">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="494b9-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="494b9-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="494b9-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="494b9-124">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="494b9-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="494b9-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="494b9-125">Header files</span></span>

<span data-ttu-id="494b9-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="494b9-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="494b9-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="494b9-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="494b9-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="494b9-128">Mapitags.h</span></span>
  
> <span data-ttu-id="494b9-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="494b9-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="494b9-130">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="494b9-130">See also</span></span>



[<span data-ttu-id="494b9-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="494b9-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="494b9-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="494b9-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="494b9-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="494b9-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="494b9-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="494b9-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

