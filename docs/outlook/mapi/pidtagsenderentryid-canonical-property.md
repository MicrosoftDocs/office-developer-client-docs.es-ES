---
title: Propiedad canónica PidTagSenderEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderEntryId
api_type:
- COM
ms.assetid: 9f311dd2-853e-46f7-966a-c2ab7a1fb6c5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0bc8b8bd76d553cc4e12e331e9fe7047ef7aaf4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358915"
---
# <a name="pidtagsenderentryid-canonical-property"></a><span data-ttu-id="b0336-103">Propiedad canónica PidTagSenderEntryId</span><span class="sxs-lookup"><span data-stu-id="b0336-103">PidTagSenderEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="b0336-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0336-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0336-105">Contiene el identificador de entrada del remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="b0336-105">Contains the message sender's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b0336-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b0336-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b0336-107">PR_SENDER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b0336-107">PR_SENDER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="b0336-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b0336-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b0336-109">0x0C19</span><span class="sxs-lookup"><span data-stu-id="b0336-109">0x0C19</span></span>  <br/> |
|<span data-ttu-id="b0336-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b0336-110">Data type:</span></span>  <br/> |<span data-ttu-id="b0336-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b0336-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b0336-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b0336-112">Area:</span></span>  <br/> |<span data-ttu-id="b0336-113">Address</span><span class="sxs-lookup"><span data-stu-id="b0336-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0336-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b0336-114">Remarks</span></span>

<span data-ttu-id="b0336-115">Esta propiedad es una de las propiedades de dirección del remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="b0336-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="b0336-116">Debe establecerlo el proveedor de transporte saliente, que nunca debe propagar los valores existentes anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b0336-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="b0336-117">Si ningún proveedor de transporte ha proporcionado ninguna propiedad de dirección del remitente, la cola MAPI intenta rellenarlas llamando al método [IMAPISession::QueryIdentity](imapisession-queryidentity.md) para obtener un identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="b0336-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="b0336-118">Si no se han proporcionado identificadores de entrada, la cola MAPI tiene un identificador correspondiente a la cadena "Unknown" en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b0336-118">If no entry identifiers have been provided, the MAPI spooler an identifier corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b0336-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b0336-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b0336-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="b0336-120">Protocol specifications</span></span>

<span data-ttu-id="b0336-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0336-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0336-122">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="b0336-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b0336-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0336-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0336-124">Especifica las propiedades y operaciones permitidas para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="b0336-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="b0336-125">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0336-125">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0336-126">Especifica las propiedades y operaciones que representan elementos RSS.</span><span class="sxs-lookup"><span data-stu-id="b0336-126">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="b0336-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0336-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0336-128">Controla el orden y el flujo de las transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="b0336-128">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="b0336-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0336-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0336-130">Convierte entre IETF RFC2445, RFC2446 y RFC2447, y objetos de cita y reunión.</span><span class="sxs-lookup"><span data-stu-id="b0336-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="b0336-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0336-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0336-132">Especifica las propiedades y las operaciones de los mensajes de cita, de reunión y de respuesta.</span><span class="sxs-lookup"><span data-stu-id="b0336-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="b0336-133">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0336-133">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0336-134">Especifica las propiedades y operaciones permitidas para los objetos post.</span><span class="sxs-lookup"><span data-stu-id="b0336-134">Specifies the properties and operations that are permissible for post objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b0336-135">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b0336-135">Header files</span></span>

<span data-ttu-id="b0336-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b0336-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="b0336-137">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b0336-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="b0336-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b0336-138">Mapitags.h</span></span>
  
> <span data-ttu-id="b0336-139">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="b0336-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b0336-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b0336-140">See also</span></span>



[<span data-ttu-id="b0336-141">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b0336-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b0336-142">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="b0336-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b0336-143">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b0336-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b0336-144">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="b0336-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

