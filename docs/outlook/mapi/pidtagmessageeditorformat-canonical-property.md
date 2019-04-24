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
# <a name="pidtagmessageeditorformat-canonical-property"></a><span data-ttu-id="8401c-103">Propiedad canónica PidTagMessageEditorFormat</span><span class="sxs-lookup"><span data-stu-id="8401c-103">PidTagMessageEditorFormat Canonical Property</span></span>

  
  
<span data-ttu-id="8401c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8401c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8401c-105">Especifica el formato que debe usar un editor para mostrar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="8401c-105">Specifies the format for an editor to use to display a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8401c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8401c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8401c-107">PR_MSG_EDITOR_FORMAT</span><span class="sxs-lookup"><span data-stu-id="8401c-107">PR_MSG_EDITOR_FORMAT</span></span>  <br/> |
|<span data-ttu-id="8401c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8401c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8401c-109">0x5909</span><span class="sxs-lookup"><span data-stu-id="8401c-109">0x5909</span></span>  <br/> |
|<span data-ttu-id="8401c-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8401c-110">Data type:</span></span>  <br/> |<span data-ttu-id="8401c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8401c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8401c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8401c-112">Area:</span></span>  <br/> |<span data-ttu-id="8401c-113">Varios</span><span class="sxs-lookup"><span data-stu-id="8401c-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8401c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8401c-114">Remarks</span></span>

<span data-ttu-id="8401c-115">Los valores posibles de **PR_MSG_EDITOR_FORMAT** pueden ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="8401c-115">The possible values for **PR_MSG_EDITOR_FORMAT** can be one of the following:</span></span> 
  
|<span data-ttu-id="8401c-116">**Value**</span><span class="sxs-lookup"><span data-stu-id="8401c-116">**Value**</span></span>|<span data-ttu-id="8401c-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8401c-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8401c-118">**EDITOR_FORMAT_DONTKNOW**</span><span class="sxs-lookup"><span data-stu-id="8401c-118">**EDITOR_FORMAT_DONTKNOW**</span></span> <br/> |<span data-ttu-id="8401c-119">El formato para el editor que se debe usar es desconocido.</span><span class="sxs-lookup"><span data-stu-id="8401c-119">The format for the editor to use is unknown.</span></span>  <br/> |
|<span data-ttu-id="8401c-120">**EDITOR_FORMAT_PLAINTEXT**</span><span class="sxs-lookup"><span data-stu-id="8401c-120">**EDITOR_FORMAT_PLAINTEXT**</span></span> <br/> |<span data-ttu-id="8401c-121">El editor debe mostrar el mensaje en texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="8401c-121">The editor should display the message in plain text format.</span></span>  <br/> |
|<span data-ttu-id="8401c-122">**EDITOR_FORMAT_HTML**</span><span class="sxs-lookup"><span data-stu-id="8401c-122">**EDITOR_FORMAT_HTML**</span></span> <br/> |<span data-ttu-id="8401c-123">El editor debe mostrar el mensaje en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="8401c-123">The editor should display the message in HTML format.</span></span>  <br/> |
|<span data-ttu-id="8401c-124">**EDITOR_FORMAT_RTF**</span><span class="sxs-lookup"><span data-stu-id="8401c-124">**EDITOR_FORMAT_RTF**</span></span> <br/> |<span data-ttu-id="8401c-125">El editor debe mostrar el mensaje en formato de texto enriquecido.</span><span class="sxs-lookup"><span data-stu-id="8401c-125">The editor should display the message in Rich Text Format.</span></span>  <br/> |
   
<span data-ttu-id="8401c-126">De forma predeterminada, los mensajes de correo (con la clase de mensaje **IPM. Note** o con una clase de mensaje personalizada derivada de **IPM. Note**) enviados desde una cuenta de correo POP3/SMTP se envían en el formato de encapsulaMiento neutro para el transporte (TNEF).</span><span class="sxs-lookup"><span data-stu-id="8401c-126">By default, mail messages (with the message class **IPM.Note** or with a custom message class derived from **IPM.Note**) sent from a POP3/SMTP mail account are sent in the Transport Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="8401c-127">La propiedad **PR_MSG_EDITOR_FORMAT** puede usarse para exigir únicamente texto sin formato, y no TNEF, al enviar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="8401c-127">The **PR_MSG_EDITOR_FORMAT** property can be used to enforce only plain text, and not TNEF, when sending a message.</span></span> <span data-ttu-id="8401c-128">Si **PR_MSG_EDITOR_FORMAT** se establece en **EDITOR_FORMAT_PLAINTEXT**, el mensaje se envía como texto sin formato TNEF.</span><span class="sxs-lookup"><span data-stu-id="8401c-128">If **PR_MSG_EDITOR_FORMAT** is set to **EDITOR_FORMAT_PLAINTEXT**, the message is sent as plain text without TNEF.</span></span> <span data-ttu-id="8401c-129">Si **PR_MSG_EDITOR_FORMAT** se establece en **EDITOR_FORMAT_RTF**, la codificación TNEF está habilitada de forma implícita y el mensaje se envía mediante el formato de Internet predeterminado que se especifica en el cliente de Outlook.</span><span class="sxs-lookup"><span data-stu-id="8401c-129">If **PR_MSG_EDITOR_FORMAT** is set to **EDITOR_FORMAT_RTF**, TNEF encoding is implicitly enabled, and the message is sent by using the default Internet format that is specified in the Outlook client.</span></span>
  
<span data-ttu-id="8401c-130">Hay otras dos maneras de exigir el uso de TNEF al enviar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="8401c-130">There are two other ways to enforce the use of TNEF when sending a message.</span></span>
  
- <span data-ttu-id="8401c-131">La configuración de la propiedad con nombre **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) en true en un mensaje indica que TNEF debe incluirse cuando se convierte el mensaje de MAPI a MIME/SMTP.</span><span class="sxs-lookup"><span data-stu-id="8401c-131">Setting the **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) named property to True on a message indicates TNEF should be included when converting the message from MAPI to MIME/SMTP.</span></span> <span data-ttu-id="8401c-132">Tenga en cuenta que **dispidUseTNEF** solo se aplica cuando el mensaje se envía desde una cuenta de correo POP3/SMTP y no se aplica cuando otros proveedores envían el mensaje, como Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8401c-132">Note that **dispidUseTNEF** only applies when the message is sent from a POP3/SMTP mail account, and does not apply when the message is sent by other providers, such as Microsoft Exchange Server.</span></span> <span data-ttu-id="8401c-133">**dispidUseTNEF** reemplaza la configuración de **PR_MSG_EDITOR_FORMAT**.</span><span class="sxs-lookup"><span data-stu-id="8401c-133">**dispidUseTNEF** overrides the setting in **PR_MSG_EDITOR_FORMAT**.</span></span>
    
- <span data-ttu-id="8401c-134">Usar la marca **CCSF_USE_TNEF** al llamar a [IConverterSession:: MAPIToMIMEStm](iconvertersession-mapitomimestm.md) para convertir un mensaje MAPI saliente en una secuencia MIME también puede exigir TNEF.</span><span class="sxs-lookup"><span data-stu-id="8401c-134">Using the **CCSF_USE_TNEF** flag when calling [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to convert an outgoing MAPI message to a MIME stream can also enforce TNEF.</span></span> <span data-ttu-id="8401c-135">Esto es válido incluso si no se establece **dispidUseTNEF** .</span><span class="sxs-lookup"><span data-stu-id="8401c-135">This applies even if **dispidUseTNEF** is not set.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="8401c-136">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8401c-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8401c-137">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="8401c-137">Protocol specifications</span></span>

<span data-ttu-id="8401c-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8401c-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8401c-139">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8401c-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8401c-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8401c-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8401c-141">Define las estructuras de datos básicas que se usan en las operaciones remotas.</span><span class="sxs-lookup"><span data-stu-id="8401c-141">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="8401c-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8401c-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8401c-143">Especifica las propiedades y operaciones que se admiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="8401c-143">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8401c-144">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8401c-144">Header files</span></span>

<span data-ttu-id="8401c-145">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8401c-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="8401c-146">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8401c-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="8401c-147">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="8401c-147">Mapitags.h</span></span>
  
> <span data-ttu-id="8401c-148">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="8401c-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8401c-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="8401c-149">See also</span></span>



[<span data-ttu-id="8401c-150">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8401c-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8401c-151">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="8401c-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8401c-152">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8401c-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8401c-153">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="8401c-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

