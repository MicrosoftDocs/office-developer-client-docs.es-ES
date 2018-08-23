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
ms.openlocfilehash: eb04983015e8557541e69981ec130ebf07598655
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588373"
---
# <a name="pidtagstatus-canonical-property"></a><span data-ttu-id="44f33-103">Propiedad canónica PidTagStatus</span><span class="sxs-lookup"><span data-stu-id="44f33-103">PidTagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="44f33-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44f33-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44f33-105">Contiene una máscara de bits de 32 bits de marcadores que definen el estado de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="44f33-105">Contains a 32-bit bitmask of flags that define folder status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="44f33-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="44f33-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="44f33-107">PR_STATUS</span><span class="sxs-lookup"><span data-stu-id="44f33-107">PR_STATUS</span></span>  <br/> |
|<span data-ttu-id="44f33-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="44f33-108">Identifier:</span></span>  <br/> |<span data-ttu-id="44f33-109">0x360B</span><span class="sxs-lookup"><span data-stu-id="44f33-109">0x360B</span></span>  <br/> |
|<span data-ttu-id="44f33-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="44f33-110">Data type:</span></span>  <br/> |<span data-ttu-id="44f33-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="44f33-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="44f33-112">Área:</span><span class="sxs-lookup"><span data-stu-id="44f33-112">Area:</span></span>  <br/> |<span data-ttu-id="44f33-113">Contenedor MAPI</span><span class="sxs-lookup"><span data-stu-id="44f33-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44f33-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="44f33-114">Remarks</span></span>

<span data-ttu-id="44f33-115">Esta propiedad para las carpetas es análoga a la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) para los mensajes.</span><span class="sxs-lookup"><span data-stu-id="44f33-115">This property for folders is analogous to the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property for messages.</span></span> <span data-ttu-id="44f33-116">Sus indicadores se proporcionan para la aplicación de cliente sólo y no afectan el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="44f33-116">Its flags are provided for the client application only and do not affect the message store.</span></span> <span data-ttu-id="44f33-117">Los clientes pueden usar u omitir estas opciones de configuración.</span><span class="sxs-lookup"><span data-stu-id="44f33-117">Clients can use or ignore these settings.</span></span> <span data-ttu-id="44f33-118">El cliente también puede definir sus propios valores para los bits definidos por el cliente de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="44f33-118">The client can also define its own values for the client-definable bits of this property.</span></span>
  
<span data-ttu-id="44f33-119">La máscara de bits se pueden establecer uno o varios de los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="44f33-119">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="44f33-120">FLDSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="44f33-120">FLDSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="44f33-121">La carpeta está marcada para su eliminación.</span><span class="sxs-lookup"><span data-stu-id="44f33-121">The folder is marked for deletion.</span></span> <span data-ttu-id="44f33-122">La aplicación cliente establece esta marca.</span><span class="sxs-lookup"><span data-stu-id="44f33-122">The client application sets this flag.</span></span>
    
<span data-ttu-id="44f33-123">FLDSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="44f33-123">FLDSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="44f33-124">La carpeta está oculta.</span><span class="sxs-lookup"><span data-stu-id="44f33-124">The folder is hidden.</span></span>
    
<span data-ttu-id="44f33-125">FLDSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="44f33-125">FLDSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="44f33-126">La carpeta está resaltada, por ejemplo, se muestra en orden inverso vídeo.</span><span class="sxs-lookup"><span data-stu-id="44f33-126">The folder is highlighted, for example, shown in reverse video.</span></span>
    
<span data-ttu-id="44f33-127">FLDSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="44f33-127">FLDSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="44f33-128">La carpeta está etiquetada.</span><span class="sxs-lookup"><span data-stu-id="44f33-128">The folder is tagged.</span></span>
    
<span data-ttu-id="44f33-129">Los proveedores de almacén de mensajes establecen esta propiedad en una carpeta a uno o varios de estos valores y los clientes interpretan el estado según corresponda para sus aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="44f33-129">Message store providers set this property on a folder to one or more of these values and clients interpret the status as appropriate for their applications.</span></span> <span data-ttu-id="44f33-130">Por ejemplo, un cliente puede utilizar el estado de la carpeta para diferenciar entre las carpetas en una tabla de jerarquías, mostrar carpetas con el mismo estado de la misma manera.</span><span class="sxs-lookup"><span data-stu-id="44f33-130">For example, a client can use the folder status to visually differentiate between folders in a hierarchy table, displaying folders with the same status in the same way.</span></span> <span data-ttu-id="44f33-131">Resaltado de las carpetas se pueden mostrar en las carpetas de vídeos, con etiqueta inversas y las carpetas marcadas para eliminación que se pueden mostrar con un icono significativo y se pueden ocultar las carpetas ocultas.</span><span class="sxs-lookup"><span data-stu-id="44f33-131">Highlighted folders can be shown in reverse video, tagged folders and folders marked for deletion can be shown with a meaningful icon, and hidden folders can be concealed.</span></span>
  
<span data-ttu-id="44f33-132">Bits 16 a 31 ("0 x 10000" a través de "0 x 80000000") de esta propiedad están disponibles para su uso por la aplicación de cliente IPM.</span><span class="sxs-lookup"><span data-stu-id="44f33-132">Bits 16 through 31 ("0x10000" through "0x80000000") of this property are available for use by the IPM client application.</span></span> <span data-ttu-id="44f33-133">Todos los demás bits están reservados para su uso por MAPI; los no definidos en la lista anterior deben inicialmente se establece en cero y no se modifica.</span><span class="sxs-lookup"><span data-stu-id="44f33-133">All other bits are reserved for use by MAPI; those not defined in the preceding list should be initially set to zero and not altered.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="44f33-134">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="44f33-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="44f33-135">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="44f33-135">Protocol specifications</span></span>

<span data-ttu-id="44f33-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44f33-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44f33-137">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="44f33-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="44f33-138">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44f33-138">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44f33-139">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="44f33-139">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="44f33-140">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="44f33-140">Header files</span></span>

<span data-ttu-id="44f33-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="44f33-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="44f33-142">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="44f33-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="44f33-143">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="44f33-143">Mapitags.h</span></span>
  
> <span data-ttu-id="44f33-144">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="44f33-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="44f33-145">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="44f33-145">See also</span></span>



[<span data-ttu-id="44f33-146">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="44f33-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="44f33-147">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="44f33-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="44f33-148">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="44f33-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="44f33-149">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="44f33-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

