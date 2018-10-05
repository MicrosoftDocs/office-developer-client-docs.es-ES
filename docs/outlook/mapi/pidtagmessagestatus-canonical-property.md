---
title: Propiedad canónica PidTagMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageStatus
api_type:
- HeaderDef
ms.assetid: e479e863-a8de-4f7e-9eae-3f721cd16e9a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dacd759d978394a5f4ed028915ed1c717bf6efe5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382809"
---
# <a name="pidtagmessagestatus-canonical-property"></a><span data-ttu-id="83216-103">Propiedad canónica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="83216-103">PidTagMessageStatus Canonical Property</span></span>

  
  
<span data-ttu-id="83216-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83216-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83216-105">Contiene una máscara de bits 32 bits de indicadores que define el estado de un mensaje en una tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="83216-105">Contains a 32-bit bitmask of flags that defines the status of a message in a contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="83216-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="83216-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="83216-107">PR_MSG_STATUS</span><span class="sxs-lookup"><span data-stu-id="83216-107">PR_MSG_STATUS</span></span>  <br/> |
|<span data-ttu-id="83216-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="83216-108">Identifier:</span></span>  <br/> |<span data-ttu-id="83216-109">0x0E17</span><span class="sxs-lookup"><span data-stu-id="83216-109">0x0E17</span></span>  <br/> |
|<span data-ttu-id="83216-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="83216-110">Data type:</span></span>  <br/> |<span data-ttu-id="83216-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="83216-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="83216-112">Área:</span><span class="sxs-lookup"><span data-stu-id="83216-112">Area:</span></span>  <br/> |<span data-ttu-id="83216-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="83216-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="83216-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="83216-114">Remarks</span></span>

<span data-ttu-id="83216-115">Puede haber un mensaje en una tabla de contenido y en una o varias tablas de resultados de búsqueda, y cada instancia del mensaje puede tener un estado diferente.</span><span class="sxs-lookup"><span data-stu-id="83216-115">A message can exist in a contents table and in one or more search-results tables, and each instance of the message can have a different status.</span></span> <span data-ttu-id="83216-116">Esta propiedad no se debe considerar una propiedad en un mensaje, pero una columna de una tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="83216-116">This property should not be considered a property on a message but a column in a contents table.</span></span> 
  
<span data-ttu-id="83216-117">Una aplicación cliente puede establecer una o varias de las siguientes marcas en esta propiedad:</span><span class="sxs-lookup"><span data-stu-id="83216-117">A client application can set one or more of the following flags in this property:</span></span> 
  
<span data-ttu-id="83216-118">MSGSTATUS_ANSWERED</span><span class="sxs-lookup"><span data-stu-id="83216-118">MSGSTATUS_ANSWERED</span></span> 
  
> <span data-ttu-id="83216-119">El mensaje se ha respondido.</span><span class="sxs-lookup"><span data-stu-id="83216-119">The message has been replied to.</span></span> 
    
<span data-ttu-id="83216-120">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="83216-120">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="83216-121">El mensaje se ha marcado para su eliminación subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="83216-121">The message has been marked for subsequent deletion.</span></span> 
    
<span data-ttu-id="83216-122">MSGSTATUS_DRAFT</span><span class="sxs-lookup"><span data-stu-id="83216-122">MSGSTATUS_DRAFT</span></span> 
  
> <span data-ttu-id="83216-123">El mensaje está en estado de revisión de borrador.</span><span class="sxs-lookup"><span data-stu-id="83216-123">The message is in draft revision status.</span></span> 
    
<span data-ttu-id="83216-124">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="83216-124">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="83216-125">El mensaje es se suprimen de muestra de la carpeta de los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="83216-125">The message is to be suppressed from recipients' folder displays.</span></span> 
    
<span data-ttu-id="83216-126">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="83216-126">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="83216-127">El mensaje es se resalta en la muestra de la carpeta de los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="83216-127">The message is to be highlighted in recipients' folder displays.</span></span> 
    
<span data-ttu-id="83216-128">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="83216-128">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="83216-129">El mensaje se ha marcado para su eliminación en el almacén de mensajes remoto sin descargar en el cliente local.</span><span class="sxs-lookup"><span data-stu-id="83216-129">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span> 
    
<span data-ttu-id="83216-130">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="83216-130">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="83216-131">El mensaje se ha marcado para la descarga desde el almacén de mensajes remoto para el cliente local.</span><span class="sxs-lookup"><span data-stu-id="83216-131">The message has been marked for downloading from the remote message store to the local client.</span></span> 
    
<span data-ttu-id="83216-132">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="83216-132">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="83216-133">El mensaje se ha etiquetado con un fin definidas por el cliente.</span><span class="sxs-lookup"><span data-stu-id="83216-133">The message has been tagged for a client-defined purpose.</span></span>
    
<span data-ttu-id="83216-134">Los indicadores **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**y **MSGSTATUS_TAGGED** se definen por el cliente.</span><span class="sxs-lookup"><span data-stu-id="83216-134">The **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**, and **MSGSTATUS_TAGGED** flags are defined by the client.</span></span> <span data-ttu-id="83216-135">Proveedores de transporte y almacén de pasan estos bits sin ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="83216-135">Transport and store providers pass these bits without any action.</span></span> 
  
<span data-ttu-id="83216-136">Los clientes pueden interpretar estos valores de cualquier forma que es adecuado para sus aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="83216-136">Clients can interpret these values in any way that is appropriate for their applications.</span></span> <span data-ttu-id="83216-137">Es una forma de que muchos clientes usan esta propiedad Mostrar los mensajes marcados para eliminación con un icono representativo.</span><span class="sxs-lookup"><span data-stu-id="83216-137">One way that many clients use this property is to display messages marked for deletion with a representative icon.</span></span> 
  
<span data-ttu-id="83216-138">Un cliente remoto Visor puede establecer **MSGSTATUS_REMOTE_DELETE** o **MSGSTATUS_REMOTE_DOWNLOAD** en los mensajes en la carpeta de encabezado presentada por el proveedor de transporte remoto.</span><span class="sxs-lookup"><span data-stu-id="83216-138">A remote viewer client can set **MSGSTATUS_REMOTE_DELETE** or **MSGSTATUS_REMOTE_DOWNLOAD** on messages in the header folder presented to it by the remote transport provider.</span></span> <span data-ttu-id="83216-139">La aplicación cliente puede examinar cada encabezado de mensaje en esta carpeta para determinar si el mensaje debe ser descargado o eliminado en el almacén de mensajes remoto.</span><span class="sxs-lookup"><span data-stu-id="83216-139">The client application can examine each message header in this folder to determine whether the message should be downloaded or deleted at the remote message store.</span></span> <span data-ttu-id="83216-140">A continuación, se usa el método [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) para establecer la marca adecuada.</span><span class="sxs-lookup"><span data-stu-id="83216-140">It then uses the [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) method to set the appropriate flag.</span></span> <span data-ttu-id="83216-141">**SetMessageStatus** es la única forma de establecer cualquiera de los indicadores de esta propiedad; no se puede usar el método [IMAPIProp::SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="83216-141">**SetMessageStatus** is the only way to set any of the flags in this property; the [IMAPIProp::SetProps](imapiprop-setprops.md) method cannot be used.</span></span> <span data-ttu-id="83216-142">Para recuperar esta propiedad, los clientes llaman [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) en lugar de [IMAPIProp::GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="83216-142">To retrieve this property, clients call [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) rather than [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
  
<span data-ttu-id="83216-143">Bits 16 a 31 (0 x 10000 a través de 0 x 80000000) de esta propiedad están disponibles para su uso por la aplicación de cliente de mensajes interpersonales (IPM).</span><span class="sxs-lookup"><span data-stu-id="83216-143">Bits 16 through 31 (0x10000 through 0x80000000) of this property are available for use by the interpersonal message (IPM) client application.</span></span> <span data-ttu-id="83216-144">Todos los demás bits están reservados para su uso por MAPI; los no definidos en la tabla anterior deben inicialmente se establece en cero y no modifica posteriormente.</span><span class="sxs-lookup"><span data-stu-id="83216-144">All other bits are reserved for use by MAPI; those not defined in the preceding table should be initially set to zero and not altered subsequently.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="83216-145">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="83216-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="83216-146">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="83216-146">Protocol specifications</span></span>

<span data-ttu-id="83216-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="83216-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="83216-148">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="83216-148">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="83216-149">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="83216-149">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="83216-150">Controla la sincronización de datos de objeto mensajería entre un servidor y un cliente.</span><span class="sxs-lookup"><span data-stu-id="83216-150">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="83216-151">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="83216-151">Header files</span></span>

<span data-ttu-id="83216-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="83216-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="83216-153">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="83216-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="83216-154">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="83216-154">Mapitags.h</span></span>
  
> <span data-ttu-id="83216-155">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="83216-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="83216-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="83216-156">See also</span></span>



[<span data-ttu-id="83216-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="83216-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)


[<span data-ttu-id="83216-158">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="83216-158">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="83216-159">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="83216-159">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="83216-160">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="83216-160">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="83216-161">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="83216-161">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

