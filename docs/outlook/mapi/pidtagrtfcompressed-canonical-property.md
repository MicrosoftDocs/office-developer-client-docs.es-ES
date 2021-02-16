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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357893"
---
# <a name="pidtagrtfcompressed-canonical-property"></a><span data-ttu-id="9ec79-103">Propiedad canónica PidTagRtfCompressed</span><span class="sxs-lookup"><span data-stu-id="9ec79-103">PidTagRtfCompressed Canonical Property</span></span>

  
  
<span data-ttu-id="9ec79-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ec79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ec79-105">Contiene la versión de formato de texto enriquecido (RTF) del texto del mensaje, normalmente en formato comprimido.</span><span class="sxs-lookup"><span data-stu-id="9ec79-105">Contains the Rich Text Format (RTF) version of the message text, usually in compressed form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9ec79-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9ec79-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9ec79-107">PR_RTF_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="9ec79-107">PR_RTF_COMPRESSED</span></span>  <br/> |
|<span data-ttu-id="9ec79-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9ec79-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9ec79-109">0x1009</span><span class="sxs-lookup"><span data-stu-id="9ec79-109">0x1009</span></span>  <br/> |
|<span data-ttu-id="9ec79-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9ec79-110">Data type:</span></span>  <br/> |<span data-ttu-id="9ec79-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9ec79-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9ec79-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9ec79-112">Area:</span></span>  <br/> |<span data-ttu-id="9ec79-113">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="9ec79-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ec79-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9ec79-114">Remarks</span></span>

<span data-ttu-id="9ec79-115">Esta propiedad contiene el mismo texto de mensaje que **la propiedad PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), pero en RTF.</span><span class="sxs-lookup"><span data-stu-id="9ec79-115">This property contains the same message text as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property but in RTF.</span></span> 
  
<span data-ttu-id="9ec79-116">El texto del mensaje en RTF normalmente se almacena en forma comprimida.</span><span class="sxs-lookup"><span data-stu-id="9ec79-116">Message text in RTF is normally stored in compressed form.</span></span> <span data-ttu-id="9ec79-117">Sin embargo, algunos sistemas no comprimen texto con formato.</span><span class="sxs-lookup"><span data-stu-id="9ec79-117">However, some systems do not compress formatted text.</span></span> <span data-ttu-id="9ec79-118">Para incluirlos, MAPI proporciona el valor dwMagicUncompressedRTF para un encabezado de secuencia para identificar RTF sin comprimir y la marca **STORE_UNCOMPRESSED_RTF** en **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) para que el almacén de mensajes indique que puede almacenar RTF sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="9ec79-118">To accommodate them, MAPI provides the dwMagicUncompressedRTF value for a stream header to identify uncompressed RTF, and the **STORE_UNCOMPRESSED_RTF** flag in **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) for the message store to indicate it can store uncompressed RTF.</span></span> 
  
<span data-ttu-id="9ec79-119">Para obtener el contenido de esta propiedad, llame **a OpenProperty** y, a continuación, llame a [WrapCompressedRTFStream](wrapcompressedrtfstream.md) **con MAPI_READ** marca.</span><span class="sxs-lookup"><span data-stu-id="9ec79-119">To obtain the contents of this property, call **OpenProperty**, then call [WrapCompressedRTFStream](wrapcompressedrtfstream.md) with the **MAPI_READ** flag.</span></span> <span data-ttu-id="9ec79-120">Para escribir en esta propiedad, ábrala con las **MAPI_MODIFY** y **MAPI_CREATE** marcas.</span><span class="sxs-lookup"><span data-stu-id="9ec79-120">To write into this property, open it with the **MAPI_MODIFY** and **MAPI_CREATE** flags.</span></span> <span data-ttu-id="9ec79-121">Esto garantiza que los nuevos datos reemplacen completamente los datos antiguos y que las escrituras se realicen con el número mínimo de actualizaciones del almacén.</span><span class="sxs-lookup"><span data-stu-id="9ec79-121">This ensures that the new data completely replace any old data and that the writes are performed using the minimum number of store updates.</span></span> 
  
<span data-ttu-id="9ec79-122">Los almacenes de mensajes que admiten RTF omiten los cambios en los espacios en blanco del texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="9ec79-122">Message stores that support RTF ignore any changes to white space in the message text.</span></span> <span data-ttu-id="9ec79-123">Cuando **PR_BODY** se almacena por primera vez, el almacén de mensajes también genera y almacena esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="9ec79-123">When **PR_BODY** is stored for the first time, the message store also generates and stores this property.</span></span> <span data-ttu-id="9ec79-124">Si posteriormente se llama al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) y PR_BODY se ha modificado, el almacén de mensajes llama **a** la función [RTFSync](rtfsync.md) para garantizar la sincronización con la versión RTF.</span><span class="sxs-lookup"><span data-stu-id="9ec79-124">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="9ec79-125">Si solo se han cambiado los espacios en blanco, las propiedades no se modifican.</span><span class="sxs-lookup"><span data-stu-id="9ec79-125">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="9ec79-126">Esto conserva cualquier formato RTF notrivial cuando el mensaje viaja a través de clientes y sistemas de mensajería que no son compatibles con RTF.</span><span class="sxs-lookup"><span data-stu-id="9ec79-126">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9ec79-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9ec79-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9ec79-128">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="9ec79-128">Protocol specifications</span></span>

<span data-ttu-id="9ec79-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ec79-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ec79-130">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="9ec79-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9ec79-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ec79-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ec79-132">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="9ec79-132">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="9ec79-133">[[MS-OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ec79-133">[[MS-OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ec79-134">Codifica y descodifica una secuencia comprimida en cuerpos de mensajes RTF.</span><span class="sxs-lookup"><span data-stu-id="9ec79-134">Encodes and decodes a compressed stream in RTF message bodies.</span></span>
    
<span data-ttu-id="9ec79-135">[[MS-OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ec79-135">[[MS-OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ec79-136">Encapsula formatos de contenido adicionales (como HTML) dentro de la propiedad rtf body de mensajes y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="9ec79-136">Encapsulates additional content formats (such as HTML) within the RTF body property of messages and attachments.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9ec79-137">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9ec79-137">Header files</span></span>

<span data-ttu-id="9ec79-138">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9ec79-138">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ec79-139">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9ec79-139">Provides data type definitions.</span></span>
    
<span data-ttu-id="9ec79-140">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9ec79-140">Mapitags.h</span></span>
  
> <span data-ttu-id="9ec79-141">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="9ec79-141">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ec79-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9ec79-142">See also</span></span>



[<span data-ttu-id="9ec79-143">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9ec79-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ec79-144">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="9ec79-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ec79-145">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9ec79-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ec79-146">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="9ec79-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

