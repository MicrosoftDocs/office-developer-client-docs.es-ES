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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355723"
---
# <a name="pidtagmessagestatus-canonical-property"></a><span data-ttu-id="12875-103">Propiedad canónica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="12875-103">PidTagMessageStatus Canonical Property</span></span>

  
  
<span data-ttu-id="12875-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12875-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12875-105">Contiene una máscara de bits de 32 bits de marcas que define el estado de un mensaje en una tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="12875-105">Contains a 32-bit bitmask of flags that defines the status of a message in a contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="12875-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="12875-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="12875-107">PR_MSG_STATUS</span><span class="sxs-lookup"><span data-stu-id="12875-107">PR_MSG_STATUS</span></span>  <br/> |
|<span data-ttu-id="12875-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="12875-108">Identifier:</span></span>  <br/> |<span data-ttu-id="12875-109">0x0E17</span><span class="sxs-lookup"><span data-stu-id="12875-109">0x0E17</span></span>  <br/> |
|<span data-ttu-id="12875-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="12875-110">Data type:</span></span>  <br/> |<span data-ttu-id="12875-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="12875-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="12875-112">Área:</span><span class="sxs-lookup"><span data-stu-id="12875-112">Area:</span></span>  <br/> |<span data-ttu-id="12875-113">Mensajes generales</span><span class="sxs-lookup"><span data-stu-id="12875-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12875-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="12875-114">Remarks</span></span>

<span data-ttu-id="12875-115">Puede existir un mensaje en una tabla de contenido y en una o varias tablas de resultados de búsqueda, y cada instancia del mensaje puede tener un estado diferente.</span><span class="sxs-lookup"><span data-stu-id="12875-115">A message can exist in a contents table and in one or more search-results tables, and each instance of the message can have a different status.</span></span> <span data-ttu-id="12875-116">Esta propiedad no debe considerarse una propiedad de un mensaje, sino una columna de una tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="12875-116">This property should not be considered a property on a message but a column in a contents table.</span></span> 
  
<span data-ttu-id="12875-117">Una aplicación cliente puede establecer uno o más de los siguientes indicadores en esta propiedad:</span><span class="sxs-lookup"><span data-stu-id="12875-117">A client application can set one or more of the following flags in this property:</span></span> 
  
<span data-ttu-id="12875-118">MSGSTATUS_ANSWERED</span><span class="sxs-lookup"><span data-stu-id="12875-118">MSGSTATUS_ANSWERED</span></span> 
  
> <span data-ttu-id="12875-119">Se ha respondido al mensaje.</span><span class="sxs-lookup"><span data-stu-id="12875-119">The message has been replied to.</span></span> 
    
<span data-ttu-id="12875-120">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="12875-120">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="12875-121">El mensaje se ha marcado para su posterior eliminación.</span><span class="sxs-lookup"><span data-stu-id="12875-121">The message has been marked for subsequent deletion.</span></span> 
    
<span data-ttu-id="12875-122">MSGSTATUS_DRAFT</span><span class="sxs-lookup"><span data-stu-id="12875-122">MSGSTATUS_DRAFT</span></span> 
  
> <span data-ttu-id="12875-123">El mensaje está en estado de revisión de borrador.</span><span class="sxs-lookup"><span data-stu-id="12875-123">The message is in draft revision status.</span></span> 
    
<span data-ttu-id="12875-124">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="12875-124">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="12875-125">El mensaje se debe suprimir de las visualizaciones de carpetas de los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="12875-125">The message is to be suppressed from recipients' folder displays.</span></span> 
    
<span data-ttu-id="12875-126">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="12875-126">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="12875-127">El mensaje se resaltará en la carpeta de muestra de los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="12875-127">The message is to be highlighted in recipients' folder displays.</span></span> 
    
<span data-ttu-id="12875-128">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="12875-128">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="12875-129">El mensaje se marcó para ser eliminado en el almacén de mensajes remoto sin descargarse al cliente local.</span><span class="sxs-lookup"><span data-stu-id="12875-129">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span> 
    
<span data-ttu-id="12875-130">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="12875-130">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="12875-131">El mensaje se marcó para descargar del almacén de mensajes remoto en el cliente local.</span><span class="sxs-lookup"><span data-stu-id="12875-131">The message has been marked for downloading from the remote message store to the local client.</span></span> 
    
<span data-ttu-id="12875-132">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="12875-132">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="12875-133">El mensaje se ha etiquetado para un propósito definido por el cliente.</span><span class="sxs-lookup"><span data-stu-id="12875-133">The message has been tagged for a client-defined purpose.</span></span>
    
<span data-ttu-id="12875-134">El cliente define los indicadores **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**y **MSGSTATUS_TAGGED** .</span><span class="sxs-lookup"><span data-stu-id="12875-134">The **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**, and **MSGSTATUS_TAGGED** flags are defined by the client.</span></span> <span data-ttu-id="12875-135">Los proveedores de transporte y almacenamiento pasan estos bits sin ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="12875-135">Transport and store providers pass these bits without any action.</span></span> 
  
<span data-ttu-id="12875-136">Los clientes pueden interpretar estos valores de manera que sean apropiados para sus aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="12875-136">Clients can interpret these values in any way that is appropriate for their applications.</span></span> <span data-ttu-id="12875-137">Una forma por la que muchos clientes usan esta propiedad es mostrar los mensajes marcados para su eliminación con un icono representativo.</span><span class="sxs-lookup"><span data-stu-id="12875-137">One way that many clients use this property is to display messages marked for deletion with a representative icon.</span></span> 
  
<span data-ttu-id="12875-138">Un cliente del visor remoto puede establecer **MSGSTATUS_REMOTE_DELETE** o **MSGSTATUS_REMOTE_DOWNLOAD** en los mensajes de la carpeta de encabezado que el proveedor de transporte remoto presenta a él.</span><span class="sxs-lookup"><span data-stu-id="12875-138">A remote viewer client can set **MSGSTATUS_REMOTE_DELETE** or **MSGSTATUS_REMOTE_DOWNLOAD** on messages in the header folder presented to it by the remote transport provider.</span></span> <span data-ttu-id="12875-139">La aplicación cliente puede examinar cada encabezado de mensaje en esta carpeta para determinar si el mensaje debe descargarse o eliminarse en el almacén de mensajes remotos.</span><span class="sxs-lookup"><span data-stu-id="12875-139">The client application can examine each message header in this folder to determine whether the message should be downloaded or deleted at the remote message store.</span></span> <span data-ttu-id="12875-140">A continuación, se usa el método [IMAPIFolder:: SetMessageStatus](imapifolder-setmessagestatus.md) para establecer la marca adecuada.</span><span class="sxs-lookup"><span data-stu-id="12875-140">It then uses the [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) method to set the appropriate flag.</span></span> <span data-ttu-id="12875-141">**SetMessageStatus** es la única forma de establecer cualquiera de las marcas en esta propiedad; no se puede usar el método [IMAPIProp:: SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="12875-141">**SetMessageStatus** is the only way to set any of the flags in this property; the [IMAPIProp::SetProps](imapiprop-setprops.md) method cannot be used.</span></span> <span data-ttu-id="12875-142">Para recuperar esta propiedad, los clientes llaman a [IMAPIFolder:: GetMessageStatus](imapifolder-getmessagestatus.md) en lugar de [IMAPIProp:: GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="12875-142">To retrieve this property, clients call [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) rather than [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
  
<span data-ttu-id="12875-143">Los bits 16 a 31 (0x10000 a 0x80000000) de esta propiedad están disponibles para su uso por parte de la aplicación cliente interpersonal de mensajes (IPM).</span><span class="sxs-lookup"><span data-stu-id="12875-143">Bits 16 through 31 (0x10000 through 0x80000000) of this property are available for use by the interpersonal message (IPM) client application.</span></span> <span data-ttu-id="12875-144">El resto de los bits están reservados para su uso por parte de MAPI; los que no están definidos en la tabla anterior deben establecerse inicialmente en cero y no modificarse posteriormente.</span><span class="sxs-lookup"><span data-stu-id="12875-144">All other bits are reserved for use by MAPI; those not defined in the preceding table should be initially set to zero and not altered subsequently.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="12875-145">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="12875-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="12875-146">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="12875-146">Protocol specifications</span></span>

<span data-ttu-id="12875-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12875-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12875-148">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="12875-148">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="12875-149">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12875-149">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12875-150">Controla los datos de objetos de mensajería que se sincronizan entre un servidor y un cliente.</span><span class="sxs-lookup"><span data-stu-id="12875-150">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="12875-151">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="12875-151">Header files</span></span>

<span data-ttu-id="12875-152">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="12875-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="12875-153">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="12875-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="12875-154">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="12875-154">Mapitags.h</span></span>
  
> <span data-ttu-id="12875-155">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="12875-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="12875-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="12875-156">See also</span></span>



[<span data-ttu-id="12875-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="12875-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)


[<span data-ttu-id="12875-158">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="12875-158">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="12875-159">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="12875-159">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="12875-160">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="12875-160">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="12875-161">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="12875-161">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

