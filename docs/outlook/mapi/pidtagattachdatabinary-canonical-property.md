---
title: Propiedad canónica PidTagAttachDataBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataBinary
api_type:
- HeaderDef
ms.assetid: 3b0a8b28-863e-4b96-a4c0-fdb8f40555b9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 629746cedf8c6f4a8c960912a9ab1bcdc7a09e9e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574149"
---
# <a name="pidtagattachdatabinary-canonical-property"></a><span data-ttu-id="fd0bf-103">Propiedad canónica PidTagAttachDataBinary</span><span class="sxs-lookup"><span data-stu-id="fd0bf-103">PidTagAttachDataBinary Canonical Property</span></span>

  
  
<span data-ttu-id="fd0bf-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd0bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd0bf-105">Contiene los datos adjuntos binarios normalmente tiene acceso a través de la interfaz de vinculación e incrustación de objetos (OLE) **IStream** .</span><span class="sxs-lookup"><span data-stu-id="fd0bf-105">Contains binary attachment data typically accessed through the Object Linking and Embedding (OLE) **IStream** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fd0bf-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fd0bf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fd0bf-107">PR_ATTACH_DATA_BIN</span><span class="sxs-lookup"><span data-stu-id="fd0bf-107">PR_ATTACH_DATA_BIN</span></span>  <br/> |
|<span data-ttu-id="fd0bf-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fd0bf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fd0bf-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="fd0bf-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="fd0bf-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fd0bf-110">Data type:</span></span>  <br/> |<span data-ttu-id="fd0bf-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fd0bf-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fd0bf-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fd0bf-112">Area:</span></span>  <br/> |<span data-ttu-id="fd0bf-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="fd0bf-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd0bf-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fd0bf-114">Remarks</span></span>

<span data-ttu-id="fd0bf-115">Esta propiedad contiene los datos adjuntos cuando el valor de la propiedad **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) es ATTACH_BY_VALUE, que es el método habitual de datos adjuntos y el único que deben admitir.</span><span class="sxs-lookup"><span data-stu-id="fd0bf-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is ATTACH_BY_VALUE, which is the usual attachment method and the only one required to be supported.</span></span> <span data-ttu-id="fd0bf-116">**PR_ATTACH_DATA_BIN** también contiene datos adjuntos OLE 1.0 **OLESTREAM** cuando el valor de **PR_ATTACH_METHOD** es ATTACH_OLE.</span><span class="sxs-lookup"><span data-stu-id="fd0bf-116">**PR_ATTACH_DATA_BIN** also holds an OLE 1.0 **OLESTREAM** attachment when the value of **PR_ATTACH_METHOD** is ATTACH_OLE.</span></span> 
  
 <span data-ttu-id="fd0bf-117">Datos adjuntos de **OLESTREAM** pueden copiarse en un archivo llamando al método OLE **IStream:: CopyTo** .</span><span class="sxs-lookup"><span data-stu-id="fd0bf-117">**OLESTREAM** attachments can be copied into a file by calling the OLE **IStream::CopyTo** method.</span></span> <span data-ttu-id="fd0bf-118">El tipo de codificación de OLE puede estar determinado por la propiedad **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="fd0bf-118">The OLE encoding type can be determined from the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="fd0bf-119">Para datos adjuntos un archivo de documento OLE, el proveedor de almacenamiento de mensajes, debe responder a una llamada de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) en **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) y, opcionalmente, puede responder a una llamada en **PR_ATTACH_DATA_BIN **.</span><span class="sxs-lookup"><span data-stu-id="fd0bf-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) and may optionally respond to a call on **PR_ATTACH_DATA_BIN**.</span></span> <span data-ttu-id="fd0bf-120">Tenga en cuenta que **PR_ATTACH_DATA_BIN** y **PR_ATTACH_DATA_OBJ** compartan el mismo identificador de propiedad y, por tanto, son dos copias de la misma propiedad.</span><span class="sxs-lookup"><span data-stu-id="fd0bf-120">Note that **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="fd0bf-121">Para un objeto de almacenamiento, como un archivo compuesto en el formato de archivo doc de OLE 2.0, algunos proveedores de servicios de permitir que se va a abrir con la interfaz de MAPI **IStreamDocfile** para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="fd0bf-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface for improved performance.</span></span> <span data-ttu-id="fd0bf-122">Un proveedor que admita **IStreamDocfile** debe exponerlo en **PR_ATTACH_DATA_OBJ** y, opcionalmente, puede exponer en **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="fd0bf-122">A provider that supports **IStreamDocfile** must expose it on **PR_ATTACH_DATA_OBJ** and may optionally expose it on **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="fd0bf-123">Para obtener más información sobre las interfaces OLE y formatos, vea [OLE y la transferencia de datos](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span><span class="sxs-lookup"><span data-stu-id="fd0bf-123">For more information on OLE interfaces and formats, see [OLE and Data Transfer](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fd0bf-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fd0bf-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fd0bf-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="fd0bf-125">Protocol specifications</span></span>

<span data-ttu-id="fd0bf-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd0bf-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd0bf-127">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="fd0bf-127">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="fd0bf-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fd0bf-128">Header Files</span></span>

<span data-ttu-id="fd0bf-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fd0bf-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="fd0bf-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fd0bf-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="fd0bf-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fd0bf-131">Mapitags.h</span></span>
  
> <span data-ttu-id="fd0bf-132">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="fd0bf-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fd0bf-133">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="fd0bf-133">See also</span></span>



[<span data-ttu-id="fd0bf-134">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fd0bf-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fd0bf-135">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="fd0bf-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fd0bf-136">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="fd0bf-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fd0bf-137">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="fd0bf-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

