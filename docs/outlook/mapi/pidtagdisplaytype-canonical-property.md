---
title: Propiedad canónica PidTagDisplayType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayType
api_type:
- HeaderDef
ms.assetid: ee2bc6ca-3769-4b56-a77d-81418d28f768
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: da26fd2a8643817cf60adbfa6f4e85da345b875c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393473"
---
# <a name="pidtagdisplaytype-canonical-property"></a><span data-ttu-id="7bdb9-103">Propiedad canónica PidTagDisplayType</span><span class="sxs-lookup"><span data-stu-id="7bdb9-103">PidTagDisplayType Canonical Property</span></span>

  
  
<span data-ttu-id="7bdb9-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7bdb9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7bdb9-105">Contiene un valor que se utiliza para asociar un icono a una fila de una tabla determinada.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-105">Contains a value used to associate an icon with a particular row of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7bdb9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7bdb9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7bdb9-107">PR_DISPLAY_TYPE</span><span class="sxs-lookup"><span data-stu-id="7bdb9-107">PR_DISPLAY_TYPE</span></span>  <br/> |
|<span data-ttu-id="7bdb9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7bdb9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7bdb9-109">0x3900</span><span class="sxs-lookup"><span data-stu-id="7bdb9-109">0x3900</span></span>  <br/> |
|<span data-ttu-id="7bdb9-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7bdb9-110">Data type:</span></span>  <br/> |<span data-ttu-id="7bdb9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7bdb9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7bdb9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7bdb9-112">Area:</span></span>  <br/> |<span data-ttu-id="7bdb9-113">Libreta de direcciones MAPI</span><span class="sxs-lookup"><span data-stu-id="7bdb9-113">MAPI address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7bdb9-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7bdb9-114">Remarks</span></span>

<span data-ttu-id="7bdb9-115">Esta propiedad contiene un número entero largo que facilita un tratamiento especial de la entrada de la tabla en función de su tipo.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-115">This property contains a long integer that facilitates special treatment of the table entry based on its type.</span></span> <span data-ttu-id="7bdb9-116">Este tratamiento especial suele consta de mostrar un icono u otro elemento de presentación, asociado con el tipo de visualización.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-116">This special treatment typically consists of displaying an icon, or other display element, associated with the display type.</span></span> 
  
<span data-ttu-id="7bdb9-117">Esta propiedad no se usa en las tablas de contenido de carpeta.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-117">This property is not used in folder contents tables.</span></span> <span data-ttu-id="7bdb9-118">Aplicaciones cliente deben usar la propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) y la interfaz [IMAPIFormInfo](imapiforminfoimapiprop.md) adecuada de un mensaje para obtener la **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) y **PR_MINI_ICON** ([ PidTagMiniIcon](pidtagminiicon-canonical-property.md)) las propiedades de ese mensaje.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-118">Client applications should use a message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property and appropriate [IMAPIFormInfo](imapiforminfoimapiprop.md) interface to get the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties for that message.</span></span> 
  
<span data-ttu-id="7bdb9-119">Esta propiedad puede tener exactamente uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="7bdb9-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="7bdb9-120">DT_AGENT</span><span class="sxs-lookup"><span data-stu-id="7bdb9-120">DT_AGENT</span></span> 
  
> <span data-ttu-id="7bdb9-121">Un agente automatizado, como oferta del día o una presentación de gráfico del tiempo.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-121">An automated agent, such as Quote-Of-The-Day or a weather chart display.</span></span>
    
<span data-ttu-id="7bdb9-122">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="7bdb9-122">DT_DISTLIST</span></span> 
  
> <span data-ttu-id="7bdb9-123">Una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-123">A distribution list.</span></span>
    
<span data-ttu-id="7bdb9-124">DT_FOLDER</span><span class="sxs-lookup"><span data-stu-id="7bdb9-124">DT_FOLDER</span></span> 
  
> <span data-ttu-id="7bdb9-125">Muestra el icono de carpeta predeterminada adyacente a la carpeta.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-125">Display default folder icon adjacent to folder.</span></span>
    
<span data-ttu-id="7bdb9-126">DT_FOLDER_LINK</span><span class="sxs-lookup"><span data-stu-id="7bdb9-126">DT_FOLDER_LINK</span></span> 
  
> <span data-ttu-id="7bdb9-127">Mostrar el icono de vínculo de carpeta predeterminado adyacente a la carpeta en lugar del icono de carpeta predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-127">Display default folder link icon adjacent to folder rather than the default folder icon.</span></span>
    
<span data-ttu-id="7bdb9-128">DT_FOLDER_SPECIAL</span><span class="sxs-lookup"><span data-stu-id="7bdb9-128">DT_FOLDER_SPECIAL</span></span> 
  
> <span data-ttu-id="7bdb9-129">Muestra el icono de una carpeta con una distinción específicos de la aplicación, como un tipo especial de carpeta pública.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-129">Display icon for a folder with an application-specific distinction, such as a special type of public folder.</span></span>
    
<span data-ttu-id="7bdb9-130">DT_FORUM</span><span class="sxs-lookup"><span data-stu-id="7bdb9-130">DT_FORUM</span></span> 
  
> <span data-ttu-id="7bdb9-131">Un foro, como un servicio de boletín electrónico o una carpeta pública o compartida.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-131">A forum, such as a bulletin board service or a public or shared folder.</span></span>
    
<span data-ttu-id="7bdb9-132">DT_GLOBAL</span><span class="sxs-lookup"><span data-stu-id="7bdb9-132">DT_GLOBAL</span></span> 
  
> <span data-ttu-id="7bdb9-133">Una libreta de direcciones global.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-133">A global address book.</span></span>
    
<span data-ttu-id="7bdb9-134">DT_LOCAL</span><span class="sxs-lookup"><span data-stu-id="7bdb9-134">DT_LOCAL</span></span> 
  
> <span data-ttu-id="7bdb9-135">Una libreta de direcciones local que se comparte con un pequeño grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-135">A local address book that you share with a small workgroup.</span></span>
    
<span data-ttu-id="7bdb9-136">DT_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="7bdb9-136">DT_MAILUSER</span></span> 
  
> <span data-ttu-id="7bdb9-137">Un usuario típico de mensajería.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-137">A typical messaging user.</span></span>
    
<span data-ttu-id="7bdb9-138">DT_MODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="7bdb9-138">DT_MODIFIABLE</span></span> 
  
> <span data-ttu-id="7bdb9-139">Modificable; el contenedor debe indicado como modificable en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-139">Modifiable; the container should be denoted as modifiable in the user interface.</span></span>
    
<span data-ttu-id="7bdb9-140">DT_NOT_SPECIFIC</span><span class="sxs-lookup"><span data-stu-id="7bdb9-140">DT_NOT_SPECIFIC</span></span> 
  
> <span data-ttu-id="7bdb9-141">No coincide con ninguno de los otros valores.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-141">Does not match any of the other settings.</span></span>
    
<span data-ttu-id="7bdb9-142">DT_ORGANIZATION</span><span class="sxs-lookup"><span data-stu-id="7bdb9-142">DT_ORGANIZATION</span></span> 
  
> <span data-ttu-id="7bdb9-143">Un alias especial definido para un grupo de gran tamaño, como coordinador de la unidad de sangre, Contabilidad o departamento de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-143">A special alias defined for a large group, such as helpdesk, accounting, or blood-drive coordinator.</span></span>
    
<span data-ttu-id="7bdb9-144">DT_PRIVATE_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="7bdb9-144">DT_PRIVATE_DISTLIST</span></span> 
  
> <span data-ttu-id="7bdb9-145">Privado, personalmente administran la lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-145">A private, personally administered distribution list.</span></span>
    
<span data-ttu-id="7bdb9-146">DT_REMOTE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="7bdb9-146">DT_REMOTE_MAILUSER</span></span> 
  
> <span data-ttu-id="7bdb9-147">Destinatario que se conocen como desde un sistema de mensajería externo o remoto.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-147">A recipient known to be from a foreign or remote messaging system.</span></span>
    
<span data-ttu-id="7bdb9-148">DT_WAN</span><span class="sxs-lookup"><span data-stu-id="7bdb9-148">DT_WAN</span></span> 
  
> <span data-ttu-id="7bdb9-149">Una libreta de direcciones de red de área extensa.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-149">A wide area network address book.</span></span>
    
<span data-ttu-id="7bdb9-150">Tablas de contenido de la libreta de direcciones utilizan los valores DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST y DT_REMOTE_MAILUSER.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-150">Address book contents tables use the DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST, and DT_REMOTE_MAILUSER values.</span></span> <span data-ttu-id="7bdb9-151">Tablas de jerarquía de la libreta de direcciones y tablas de uso único usan los valores DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC y DT_WAN.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-151">Address book hierarchy tables and one-off tables use the DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC, and DT_WAN values.</span></span> <span data-ttu-id="7bdb9-152">Tablas de jerarquía de carpeta use los valores DT_FOLDER, DT_FOLDER_LINK y DT_FOLDER_SPECIAL.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-152">Folder hierarchy tables use the DT_FOLDER, DT_FOLDER_LINK, and DT_FOLDER_SPECIAL values.</span></span> 
  
<span data-ttu-id="7bdb9-153">Si no se establece esta propiedad, el cliente debe asumir el tipo predeterminado apropiado para la tabla, normalmente DT_FOLDER, DT_LOCAL o DT_MAILUSER.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-153">If this property is not set, the client should assume the default type appropriate for the table, typically DT_FOLDER, DT_LOCAL, or DT_MAILUSER.</span></span> 
  
 <span data-ttu-id="7bdb9-154">**Nota** Todos los valores no documentados están reservados para MAPI.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-154">**Note** All values not documented are reserved for MAPI.</span></span> <span data-ttu-id="7bdb9-155">Las aplicaciones cliente no deben definir los nuevos valores y deben estar preparadas abordar los problemas con un valor sin documentar.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-155">Client applications must not define any new values and must be prepared to deal with an undocumented value.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7bdb9-156">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7bdb9-156">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7bdb9-157">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="7bdb9-157">Protocol specifications</span></span>

<span data-ttu-id="7bdb9-158">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7bdb9-158">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7bdb9-159">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-159">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7bdb9-160">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7bdb9-160">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7bdb9-161">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-161">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="7bdb9-162">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7bdb9-162">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7bdb9-163">Especifica las propiedades y operaciones que se permiten para las plantillas de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-163">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
<span data-ttu-id="7bdb9-164">[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7bdb9-164">[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7bdb9-165">Habilita el acceso de Active directory.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-165">Enables directory access.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7bdb9-166">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7bdb9-166">Header files</span></span>

<span data-ttu-id="7bdb9-167">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7bdb9-167">Mapidefs.h</span></span>
  
> <span data-ttu-id="7bdb9-168">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-168">Provides data type definitions.</span></span>
    
<span data-ttu-id="7bdb9-169">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7bdb9-169">Mapitags.h</span></span>
  
> <span data-ttu-id="7bdb9-170">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-170">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7bdb9-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="7bdb9-171">See also</span></span>



[<span data-ttu-id="7bdb9-172">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7bdb9-172">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7bdb9-173">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="7bdb9-173">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7bdb9-174">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7bdb9-174">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7bdb9-175">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="7bdb9-175">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

