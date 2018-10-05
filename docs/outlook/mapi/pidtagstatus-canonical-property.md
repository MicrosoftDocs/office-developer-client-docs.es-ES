---
title: Propiedad canónica PidTagStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatus
api_type:
- COM
ms.assetid: 8b947660-eafe-47e1-9595-bd3ab7d455bf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: de2342ef4d3e9d06f198e06dc19c65b7b144624f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387912"
---
# <a name="pidtagstatus-canonical-property"></a><span data-ttu-id="0cd77-103">Propiedad canónica PidTagStatus</span><span class="sxs-lookup"><span data-stu-id="0cd77-103">PidTagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="0cd77-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0cd77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0cd77-105">Contiene una máscara de bits de 32 bits de marcadores que definen el estado de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="0cd77-105">Contains a 32-bit bitmask of flags that define folder status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0cd77-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0cd77-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0cd77-107">PR_STATUS</span><span class="sxs-lookup"><span data-stu-id="0cd77-107">PR_STATUS</span></span>  <br/> |
|<span data-ttu-id="0cd77-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0cd77-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0cd77-109">0x360B</span><span class="sxs-lookup"><span data-stu-id="0cd77-109">0x360B</span></span>  <br/> |
|<span data-ttu-id="0cd77-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0cd77-110">Data type:</span></span>  <br/> |<span data-ttu-id="0cd77-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0cd77-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0cd77-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0cd77-112">Area:</span></span>  <br/> |<span data-ttu-id="0cd77-113">Contenedor MAPI</span><span class="sxs-lookup"><span data-stu-id="0cd77-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0cd77-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0cd77-114">Remarks</span></span>

<span data-ttu-id="0cd77-115">Esta propiedad para las carpetas es análoga a la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) para los mensajes.</span><span class="sxs-lookup"><span data-stu-id="0cd77-115">This property for folders is analogous to the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property for messages.</span></span> <span data-ttu-id="0cd77-116">Sus indicadores se proporcionan para la aplicación de cliente sólo y no afectan el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0cd77-116">Its flags are provided for the client application only and do not affect the message store.</span></span> <span data-ttu-id="0cd77-117">Los clientes pueden usar u omitir estas opciones de configuración.</span><span class="sxs-lookup"><span data-stu-id="0cd77-117">Clients can use or ignore these settings.</span></span> <span data-ttu-id="0cd77-118">El cliente también puede definir sus propios valores para los bits definidos por el cliente de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0cd77-118">The client can also define its own values for the client-definable bits of this property.</span></span>
  
<span data-ttu-id="0cd77-119">La máscara de bits se pueden establecer uno o varios de los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="0cd77-119">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="0cd77-120">FLDSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="0cd77-120">FLDSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="0cd77-121">La carpeta está marcada para su eliminación.</span><span class="sxs-lookup"><span data-stu-id="0cd77-121">The folder is marked for deletion.</span></span> <span data-ttu-id="0cd77-122">La aplicación cliente establece esta marca.</span><span class="sxs-lookup"><span data-stu-id="0cd77-122">The client application sets this flag.</span></span>
    
<span data-ttu-id="0cd77-123">FLDSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="0cd77-123">FLDSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="0cd77-124">La carpeta está oculta.</span><span class="sxs-lookup"><span data-stu-id="0cd77-124">The folder is hidden.</span></span>
    
<span data-ttu-id="0cd77-125">FLDSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="0cd77-125">FLDSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="0cd77-126">La carpeta está resaltada, por ejemplo, se muestra en orden inverso vídeo.</span><span class="sxs-lookup"><span data-stu-id="0cd77-126">The folder is highlighted, for example, shown in reverse video.</span></span>
    
<span data-ttu-id="0cd77-127">FLDSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="0cd77-127">FLDSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="0cd77-128">La carpeta está etiquetada.</span><span class="sxs-lookup"><span data-stu-id="0cd77-128">The folder is tagged.</span></span>
    
<span data-ttu-id="0cd77-129">Los proveedores de almacén de mensajes establecen esta propiedad en una carpeta a uno o varios de estos valores y los clientes interpretan el estado según corresponda para sus aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="0cd77-129">Message store providers set this property on a folder to one or more of these values and clients interpret the status as appropriate for their applications.</span></span> <span data-ttu-id="0cd77-130">Por ejemplo, un cliente puede utilizar el estado de la carpeta para diferenciar entre las carpetas en una tabla de jerarquías, mostrar carpetas con el mismo estado de la misma manera.</span><span class="sxs-lookup"><span data-stu-id="0cd77-130">For example, a client can use the folder status to visually differentiate between folders in a hierarchy table, displaying folders with the same status in the same way.</span></span> <span data-ttu-id="0cd77-131">Resaltado de las carpetas se pueden mostrar en las carpetas de vídeos, con etiqueta inversas y las carpetas marcadas para eliminación que se pueden mostrar con un icono significativo y se pueden ocultar las carpetas ocultas.</span><span class="sxs-lookup"><span data-stu-id="0cd77-131">Highlighted folders can be shown in reverse video, tagged folders and folders marked for deletion can be shown with a meaningful icon, and hidden folders can be concealed.</span></span>
  
<span data-ttu-id="0cd77-132">Bits 16 a 31 ("0 x 10000" a través de "0 x 80000000") de esta propiedad están disponibles para su uso por la aplicación de cliente IPM.</span><span class="sxs-lookup"><span data-stu-id="0cd77-132">Bits 16 through 31 ("0x10000" through "0x80000000") of this property are available for use by the IPM client application.</span></span> <span data-ttu-id="0cd77-133">Todos los demás bits están reservados para su uso por MAPI; los no definidos en la lista anterior deben inicialmente se establece en cero y no se modifica.</span><span class="sxs-lookup"><span data-stu-id="0cd77-133">All other bits are reserved for use by MAPI; those not defined in the preceding list should be initially set to zero and not altered.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0cd77-134">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0cd77-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0cd77-135">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="0cd77-135">Protocol specifications</span></span>

<span data-ttu-id="0cd77-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0cd77-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0cd77-137">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0cd77-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0cd77-138">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0cd77-138">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0cd77-139">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="0cd77-139">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0cd77-140">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0cd77-140">Header files</span></span>

<span data-ttu-id="0cd77-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0cd77-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="0cd77-142">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0cd77-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="0cd77-143">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0cd77-143">Mapitags.h</span></span>
  
> <span data-ttu-id="0cd77-144">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="0cd77-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0cd77-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="0cd77-145">See also</span></span>



[<span data-ttu-id="0cd77-146">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0cd77-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0cd77-147">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="0cd77-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0cd77-148">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0cd77-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0cd77-149">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="0cd77-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

