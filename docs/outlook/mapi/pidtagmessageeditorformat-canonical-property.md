---
title: Propiedad canónica PidTagMessageEditorFormat
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageEditorFormat
api_type:
- HeaderDef
ms.assetid: 197b21ed-9f2f-425f-a6ed-cae1208fa2ca
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 029df4397f4d24c7c111d2017d34e6403df367d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325637"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a><span data-ttu-id="69aaa-103">Propiedad canónica PidTagMessageEditorFormat</span><span class="sxs-lookup"><span data-stu-id="69aaa-103">PidTagMessageEditorFormat Canonical Property</span></span>

  
  
<span data-ttu-id="69aaa-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69aaa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69aaa-105">Especifica el formato de un editor que se usará para mostrar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="69aaa-105">Specifies the format for an editor to use to display a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="69aaa-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="69aaa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="69aaa-107">PR_MSG_EDITOR_FORMAT</span><span class="sxs-lookup"><span data-stu-id="69aaa-107">PR_MSG_EDITOR_FORMAT</span></span>  <br/> |
|<span data-ttu-id="69aaa-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="69aaa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="69aaa-109">0x5909</span><span class="sxs-lookup"><span data-stu-id="69aaa-109">0x5909</span></span>  <br/> |
|<span data-ttu-id="69aaa-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="69aaa-110">Data type:</span></span>  <br/> |<span data-ttu-id="69aaa-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="69aaa-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="69aaa-112">Área:</span><span class="sxs-lookup"><span data-stu-id="69aaa-112">Area:</span></span>  <br/> |<span data-ttu-id="69aaa-113">Varios</span><span class="sxs-lookup"><span data-stu-id="69aaa-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69aaa-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="69aaa-114">Remarks</span></span>

<span data-ttu-id="69aaa-115">Los valores posibles **PR_MSG_EDITOR_FORMAT** pueden ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="69aaa-115">The possible values for **PR_MSG_EDITOR_FORMAT** can be one of the following:</span></span> 
  
|<span data-ttu-id="69aaa-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="69aaa-116">**Value**</span></span>|<span data-ttu-id="69aaa-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="69aaa-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="69aaa-118">**EDITOR_FORMAT_DONTKNOW**</span><span class="sxs-lookup"><span data-stu-id="69aaa-118">**EDITOR_FORMAT_DONTKNOW**</span></span> <br/> |<span data-ttu-id="69aaa-119">El formato que debe usar el editor es desconocido.</span><span class="sxs-lookup"><span data-stu-id="69aaa-119">The format for the editor to use is unknown.</span></span>  <br/> |
|<span data-ttu-id="69aaa-120">**EDITOR_FORMAT_PLAINTEXT**</span><span class="sxs-lookup"><span data-stu-id="69aaa-120">**EDITOR_FORMAT_PLAINTEXT**</span></span> <br/> |<span data-ttu-id="69aaa-121">El editor debe mostrar el mensaje en formato de texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="69aaa-121">The editor should display the message in plain text format.</span></span>  <br/> |
|<span data-ttu-id="69aaa-122">**EDITOR_FORMAT_HTML**</span><span class="sxs-lookup"><span data-stu-id="69aaa-122">**EDITOR_FORMAT_HTML**</span></span> <br/> |<span data-ttu-id="69aaa-123">El editor debe mostrar el mensaje en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="69aaa-123">The editor should display the message in HTML format.</span></span>  <br/> |
|<span data-ttu-id="69aaa-124">**EDITOR_FORMAT_RTF**</span><span class="sxs-lookup"><span data-stu-id="69aaa-124">**EDITOR_FORMAT_RTF**</span></span> <br/> |<span data-ttu-id="69aaa-125">El editor debe mostrar el mensaje en formato de texto enriquecido.</span><span class="sxs-lookup"><span data-stu-id="69aaa-125">The editor should display the message in Rich Text Format.</span></span>  <br/> |
   
<span data-ttu-id="69aaa-126">De forma predeterminada, los mensajes de correo (con la clase de **mensaje IPM. Nota** o con una clase de mensaje personalizada derivada de **IPM. Nota**) los envíos desde una cuenta de correo POP3/SMTP se envían en el formato de encapsulación neutral de transporte (TNEF).</span><span class="sxs-lookup"><span data-stu-id="69aaa-126">By default, mail messages (with the message class **IPM.Note** or with a custom message class derived from **IPM.Note**) sent from a POP3/SMTP mail account are sent in the Transport Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="69aaa-127">La **PR_MSG_EDITOR_FORMAT** puede usarse para aplicar solo texto sin formato, y no TNEF, al enviar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="69aaa-127">The **PR_MSG_EDITOR_FORMAT** property can be used to enforce only plain text, and not TNEF, when sending a message.</span></span> <span data-ttu-id="69aaa-128">Si **PR_MSG_EDITOR_FORMAT** se establece **en EDITOR_FORMAT_PLAINTEXT**, el mensaje se envía como texto sin formato sin TNEF.</span><span class="sxs-lookup"><span data-stu-id="69aaa-128">If **PR_MSG_EDITOR_FORMAT** is set to **EDITOR_FORMAT_PLAINTEXT**, the message is sent as plain text without TNEF.</span></span> <span data-ttu-id="69aaa-129">Si **PR_MSG_EDITOR_FORMAT** se establece en **EDITOR_FORMAT_RTF**, la codificación TNEF está habilitada implícitamente y el mensaje se envía mediante el formato de Internet predeterminado que se especifica en el Outlook cliente.</span><span class="sxs-lookup"><span data-stu-id="69aaa-129">If **PR_MSG_EDITOR_FORMAT** is set to **EDITOR_FORMAT_RTF**, TNEF encoding is implicitly enabled, and the message is sent by using the default Internet format that is specified in the Outlook client.</span></span>
  
<span data-ttu-id="69aaa-130">Existen otras dos formas de exigir el uso de TNEF al enviar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="69aaa-130">There are two other ways to enforce the use of TNEF when sending a message.</span></span>
  
- <span data-ttu-id="69aaa-131">Si se establece la propiedad **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) en True en un mensaje, se indica que TNEF debe incluirse al convertir el mensaje de MAPI a MIME/SMTP.</span><span class="sxs-lookup"><span data-stu-id="69aaa-131">Setting the **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) named property to True on a message indicates TNEF should be included when converting the message from MAPI to MIME/SMTP.</span></span> <span data-ttu-id="69aaa-132">Tenga en cuenta que **dispidUseTNEF** solo se aplica cuando el mensaje se envía desde una cuenta de correo POP3/SMTP y no se aplica cuando el mensaje lo envían otros proveedores, como Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="69aaa-132">Note that **dispidUseTNEF** only applies when the message is sent from a POP3/SMTP mail account, and does not apply when the message is sent by other providers, such as Microsoft Exchange Server.</span></span> <span data-ttu-id="69aaa-133">**dispidUseTNEF** invalida la configuración de **PR_MSG_EDITOR_FORMAT**.</span><span class="sxs-lookup"><span data-stu-id="69aaa-133">**dispidUseTNEF** overrides the setting in **PR_MSG_EDITOR_FORMAT**.</span></span>
    
- <span data-ttu-id="69aaa-134">El uso **de CCSF_USE_TNEF** al llamar a [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) para convertir un mensaje MAPI saliente en una secuencia MIME también puede aplicar TNEF.</span><span class="sxs-lookup"><span data-stu-id="69aaa-134">Using the **CCSF_USE_TNEF** flag when calling [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to convert an outgoing MAPI message to a MIME stream can also enforce TNEF.</span></span> <span data-ttu-id="69aaa-135">Esto se aplica incluso si **dispidUseTNEF** no está establecido.</span><span class="sxs-lookup"><span data-stu-id="69aaa-135">This applies even if **dispidUseTNEF** is not set.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="69aaa-136">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="69aaa-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="69aaa-137">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="69aaa-137">Protocol specifications</span></span>

<span data-ttu-id="69aaa-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69aaa-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69aaa-139">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="69aaa-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="69aaa-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69aaa-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69aaa-141">Define las estructuras de datos básicas que se usan en operaciones remotas.</span><span class="sxs-lookup"><span data-stu-id="69aaa-141">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="69aaa-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69aaa-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69aaa-143">Especifica las propiedades y las operaciones que son permisibles para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="69aaa-143">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="69aaa-144">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="69aaa-144">Header files</span></span>

<span data-ttu-id="69aaa-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="69aaa-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="69aaa-146">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="69aaa-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="69aaa-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="69aaa-147">Mapitags.h</span></span>
  
> <span data-ttu-id="69aaa-148">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="69aaa-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="69aaa-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="69aaa-149">See also</span></span>



[<span data-ttu-id="69aaa-150">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="69aaa-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="69aaa-151">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="69aaa-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="69aaa-152">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="69aaa-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="69aaa-153">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="69aaa-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

