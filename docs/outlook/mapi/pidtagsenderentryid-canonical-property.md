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
ms.openlocfilehash: 46ccc3c7e07e6920508fea630c96700d39366a35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820273"
---
# <a name="pidtagsenderentryid-canonical-property"></a><span data-ttu-id="c1a6a-103">Propiedad canónica PidTagSenderEntryId</span><span class="sxs-lookup"><span data-stu-id="c1a6a-103">PidTagSenderEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="c1a6a-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c1a6a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c1a6a-105">Contiene el identificador de entrada de la dirección del remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="c1a6a-105">Contains the message sender's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c1a6a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="c1a6a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c1a6a-107">PR_SENDER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c1a6a-107">PR_SENDER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="c1a6a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c1a6a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c1a6a-109">0x0C19</span><span class="sxs-lookup"><span data-stu-id="c1a6a-109">0x0C19</span></span>  <br/> |
|<span data-ttu-id="c1a6a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="c1a6a-110">Data type:</span></span>  <br/> |<span data-ttu-id="c1a6a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c1a6a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c1a6a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c1a6a-112">Area:</span></span>  <br/> |<span data-ttu-id="c1a6a-113">Address</span><span class="sxs-lookup"><span data-stu-id="c1a6a-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1a6a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c1a6a-114">Remarks</span></span>

<span data-ttu-id="c1a6a-115">Esta propiedad es una de las propiedades de direcciones para el remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="c1a6a-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="c1a6a-116">Se debe establecer por el proveedor de transporte saliente, que nunca se debe propagar los valores existentes anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c1a6a-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="c1a6a-117">Si no hay proveedor de transporte ha proporcionado las propiedades de dirección del remitente, la cola MAPI intenta rellenar llamando al método [IMAPISession::QueryIdentity](imapisession-queryidentity.md) para obtener un identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="c1a6a-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="c1a6a-118">Si no hay entrada identificadores se han proporcionado, la cola MAPI un identificador que corresponde a la cadena "Unknown" en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="c1a6a-118">If no entry identifiers have been provided, the MAPI spooler an identifier corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c1a6a-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c1a6a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c1a6a-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="c1a6a-120">Protocol specifications</span></span>

<span data-ttu-id="c1a6a-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1a6a-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c1a6a-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="c1a6a-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c1a6a-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1a6a-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c1a6a-124">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="c1a6a-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="c1a6a-125">[[MS-OXORSS]](http://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1a6a-125">[[MS-OXORSS]](http://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c1a6a-126">Especifica las propiedades y operaciones que representan elementos RSS.</span><span class="sxs-lookup"><span data-stu-id="c1a6a-126">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="c1a6a-127">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1a6a-127">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c1a6a-128">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="c1a6a-128">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="c1a6a-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1a6a-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c1a6a-130">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="c1a6a-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="c1a6a-131">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1a6a-131">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c1a6a-132">Especifica las propiedades y operaciones para una cita, convocatoria de reunión y mensajes de respuesta.</span><span class="sxs-lookup"><span data-stu-id="c1a6a-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="c1a6a-133">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c1a6a-133">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c1a6a-134">Especifica las propiedades y operaciones que se permiten para registrar objetos.</span><span class="sxs-lookup"><span data-stu-id="c1a6a-134">Specifies the properties and operations that are permissible for post objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c1a6a-135">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="c1a6a-135">Header files</span></span>

<span data-ttu-id="c1a6a-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c1a6a-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="c1a6a-137">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="c1a6a-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="c1a6a-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c1a6a-138">Mapitags.h</span></span>
  
> <span data-ttu-id="c1a6a-139">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="c1a6a-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c1a6a-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1a6a-140">See also</span></span>



[<span data-ttu-id="c1a6a-141">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c1a6a-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c1a6a-142">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="c1a6a-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c1a6a-143">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="c1a6a-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c1a6a-144">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="c1a6a-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

