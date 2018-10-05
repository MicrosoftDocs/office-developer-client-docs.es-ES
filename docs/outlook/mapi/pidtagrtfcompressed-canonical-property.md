---
title: Propiedad canónica PidTagRtfCompressed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfCompressed
api_type:
- COM
ms.assetid: fd0ccb88-55ce-4d7c-9573-6e5d6239b6a8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3091a76a1b755bf5a0d641ed9bd79bcfaa4641b7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394898"
---
# <a name="pidtagrtfcompressed-canonical-property"></a><span data-ttu-id="692e3-103">Propiedad canónica PidTagRtfCompressed</span><span class="sxs-lookup"><span data-stu-id="692e3-103">PidTagRtfCompressed Canonical Property</span></span>

  
  
<span data-ttu-id="692e3-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="692e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="692e3-105">Contiene la versión de formato de texto enriquecido (RTF) del texto del mensaje, normalmente en formato comprimido.</span><span class="sxs-lookup"><span data-stu-id="692e3-105">Contains the Rich Text Format (RTF) version of the message text, usually in compressed form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="692e3-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="692e3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="692e3-107">PR_RTF_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="692e3-107">PR_RTF_COMPRESSED</span></span>  <br/> |
|<span data-ttu-id="692e3-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="692e3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="692e3-109">0 x 1009</span><span class="sxs-lookup"><span data-stu-id="692e3-109">0x1009</span></span>  <br/> |
|<span data-ttu-id="692e3-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="692e3-110">Data type:</span></span>  <br/> |<span data-ttu-id="692e3-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="692e3-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="692e3-112">Área:</span><span class="sxs-lookup"><span data-stu-id="692e3-112">Area:</span></span>  <br/> |<span data-ttu-id="692e3-113">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="692e3-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="692e3-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="692e3-114">Remarks</span></span>

<span data-ttu-id="692e3-115">Esta propiedad contiene el mismo texto del mensaje como la propiedad **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), pero en formato RTF.</span><span class="sxs-lookup"><span data-stu-id="692e3-115">This property contains the same message text as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property but in RTF.</span></span> 
  
<span data-ttu-id="692e3-116">Texto del mensaje en formato RTF normalmente se almacena en formato comprimido.</span><span class="sxs-lookup"><span data-stu-id="692e3-116">Message text in RTF is normally stored in compressed form.</span></span> <span data-ttu-id="692e3-117">Sin embargo, algunos sistemas no comprimen el texto con formato.</span><span class="sxs-lookup"><span data-stu-id="692e3-117">However, some systems do not compress formatted text.</span></span> <span data-ttu-id="692e3-118">Para dar cabida a ellos, MAPI proporciona el valor de dwMagicUncompressedRTF para un encabezado de la secuencia identificar RTF sin comprimir y la marca **STORE_UNCOMPRESSED_RTF** en **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) para el mensaje almacén para indicar que puede almacenar sin comprimir RTF.</span><span class="sxs-lookup"><span data-stu-id="692e3-118">To accommodate them, MAPI provides the dwMagicUncompressedRTF value for a stream header to identify uncompressed RTF, and the **STORE_UNCOMPRESSED_RTF** flag in **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) for the message store to indicate it can store uncompressed RTF.</span></span> 
  
<span data-ttu-id="692e3-119">Para obtener el contenido de esta propiedad, llamada **OpenProperty**, a continuación, llame al método [WrapCompressedRTFStream](wrapcompressedrtfstream.md) con la marca **MAPI_READ** .</span><span class="sxs-lookup"><span data-stu-id="692e3-119">To obtain the contents of this property, call **OpenProperty**, then call [WrapCompressedRTFStream](wrapcompressedrtfstream.md) with the **MAPI_READ** flag.</span></span> <span data-ttu-id="692e3-120">Para escribir en esta propiedad, se abre con los indicadores **MAPI_MODIFY** y **MAPI_CREATE** .</span><span class="sxs-lookup"><span data-stu-id="692e3-120">To write into this property, open it with the **MAPI_MODIFY** and **MAPI_CREATE** flags.</span></span> <span data-ttu-id="692e3-121">Esto garantiza que los nuevos datos reemplazan completamente cualquier datos antiguos y que las escrituras se realizan con el número mínimo de almacén de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="692e3-121">This ensures that the new data completely replace any old data and that the writes are performed using the minimum number of store updates.</span></span> 
  
<span data-ttu-id="692e3-122">Almacenes de mensaje que admiten el formato RTF omitir los cambios realizados en el espacio en blanco en el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="692e3-122">Message stores that support RTF ignore any changes to white space in the message text.</span></span> <span data-ttu-id="692e3-123">Cuando **PR_BODY** se almacena por primera vez, el almacén de mensajes también genera y almacena esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="692e3-123">When **PR_BODY** is stored for the first time, the message store also generates and stores this property.</span></span> <span data-ttu-id="692e3-124">Si posteriormente se llama al método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) y **PR_BODY** se ha modificado, el almacén de mensajes llama a la función [RTFSync](rtfsync.md) para garantizar la sincronización con la versión RTF.</span><span class="sxs-lookup"><span data-stu-id="692e3-124">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="692e3-125">Si sólo se ha cambiado el espacio en blanco, las propiedades se dejan sin cambios.</span><span class="sxs-lookup"><span data-stu-id="692e3-125">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="692e3-126">Esto significa que mantiene cualquier RTF no trivial formato cuando el mensaje se transmite a través de clientes ajenos a RTF y sistemas de mensajería.</span><span class="sxs-lookup"><span data-stu-id="692e3-126">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="692e3-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="692e3-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="692e3-128">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="692e3-128">Protocol specifications</span></span>

<span data-ttu-id="692e3-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="692e3-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="692e3-130">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="692e3-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="692e3-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="692e3-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="692e3-132">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="692e3-132">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="692e3-133">[[MS-OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="692e3-133">[[MS-OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="692e3-134">Codifica y descodifica una secuencia comprimida en cuerpos de mensaje RTF.</span><span class="sxs-lookup"><span data-stu-id="692e3-134">Encodes and decodes a compressed stream in RTF message bodies.</span></span>
    
<span data-ttu-id="692e3-135">[[MS-OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="692e3-135">[[MS-OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="692e3-136">Encapsula formatos de contenido adicionales (por ejemplo, HTML) dentro de la propiedad body RTF de mensajes y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="692e3-136">Encapsulates additional content formats (such as HTML) within the RTF body property of messages and attachments.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="692e3-137">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="692e3-137">Header files</span></span>

<span data-ttu-id="692e3-138">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="692e3-138">Mapidefs.h</span></span>
  
> <span data-ttu-id="692e3-139">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="692e3-139">Provides data type definitions.</span></span>
    
<span data-ttu-id="692e3-140">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="692e3-140">Mapitags.h</span></span>
  
> <span data-ttu-id="692e3-141">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="692e3-141">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="692e3-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="692e3-142">See also</span></span>



[<span data-ttu-id="692e3-143">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="692e3-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="692e3-144">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="692e3-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="692e3-145">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="692e3-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="692e3-146">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="692e3-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

