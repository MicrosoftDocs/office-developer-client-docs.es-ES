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
ms.openlocfilehash: 1a5f8688b8ea747590cf2a2d6d5efb271aa488f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356549"
---
# <a name="pidtagattachdatabinary-canonical-property"></a><span data-ttu-id="0232a-103">Propiedad canónica PidTagAttachDataBinary</span><span class="sxs-lookup"><span data-stu-id="0232a-103">PidTagAttachDataBinary Canonical Property</span></span>

  
  
<span data-ttu-id="0232a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0232a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0232a-105">Contiene datos adjuntos binarios a los que normalmente se accede a través de la interfaz **IStream** de vinculación e inserción de objetos (OLE).</span><span class="sxs-lookup"><span data-stu-id="0232a-105">Contains binary attachment data typically accessed through the Object Linking and Embedding (OLE) **IStream** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0232a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0232a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0232a-107">PR_ATTACH_DATA_BIN</span><span class="sxs-lookup"><span data-stu-id="0232a-107">PR_ATTACH_DATA_BIN</span></span>  <br/> |
|<span data-ttu-id="0232a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0232a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0232a-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="0232a-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="0232a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0232a-110">Data type:</span></span>  <br/> |<span data-ttu-id="0232a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0232a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0232a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0232a-112">Area:</span></span>  <br/> |<span data-ttu-id="0232a-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="0232a-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0232a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0232a-114">Remarks</span></span>

<span data-ttu-id="0232a-115">Esta propiedad contiene los datos adjuntos cuando el valor de la propiedad **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) es ATTACH_BY_VALUE, que es el método de datos adjuntos habitual y el único necesario para ser compatible.</span><span class="sxs-lookup"><span data-stu-id="0232a-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is ATTACH_BY_VALUE, which is the usual attachment method and the only one required to be supported.</span></span> <span data-ttu-id="0232a-116">**PR_ATTACH_DATA_BIN** también contiene datos adjuntos OLE 1.0 **OLESTREAM** cuando el valor de **PR_ATTACH_METHOD** es ATTACH_OLE.</span><span class="sxs-lookup"><span data-stu-id="0232a-116">**PR_ATTACH_DATA_BIN** also holds an OLE 1.0 **OLESTREAM** attachment when the value of **PR_ATTACH_METHOD** is ATTACH_OLE.</span></span> 
  
 <span data-ttu-id="0232a-117">**Los datos adjuntos** olestream se pueden copiar en un archivo llamando al método OLE **IStream::CopyTo.**</span><span class="sxs-lookup"><span data-stu-id="0232a-117">**OLESTREAM** attachments can be copied into a file by calling the OLE **IStream::CopyTo** method.</span></span> <span data-ttu-id="0232a-118">El tipo de codificación OLE se puede determinar desde **la PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) propiedad.</span><span class="sxs-lookup"><span data-stu-id="0232a-118">The OLE encoding type can be determined from the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="0232a-119">Para los datos adjuntos de un archivo de documento OLE, el proveedor del almacén de mensajes debe responder a una llamada [IMAPIProp::OpenProperty](imapiprop-openproperty.md) en **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) y puede responder opcionalmente a una llamada en **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="0232a-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) and may optionally respond to a call on **PR_ATTACH_DATA_BIN**.</span></span> <span data-ttu-id="0232a-120">Tenga en **cuenta que PR_ATTACH_DATA_BIN** y **PR_ATTACH_DATA_OBJ** comparten el mismo identificador de propiedad y, por lo tanto, son dos representaciones de la misma propiedad.</span><span class="sxs-lookup"><span data-stu-id="0232a-120">Note that **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="0232a-121">Para un objeto de almacenamiento, como un archivo compuesto en formato docfile OLE 2.0, algunos proveedores de servicios permiten que se abra con la interfaz **IStreamDocfile** MAPI para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="0232a-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface for improved performance.</span></span> <span data-ttu-id="0232a-122">Un proveedor que admite **IStreamDocfile** debe exponerlo en PR_ATTACH_DATA_OBJ y puede exponerlo opcionalmente en **PR_ATTACH_DATA_BIN**. </span><span class="sxs-lookup"><span data-stu-id="0232a-122">A provider that supports **IStreamDocfile** must expose it on **PR_ATTACH_DATA_OBJ** and may optionally expose it on **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="0232a-123">Para obtener más información sobre las interfaces y formatos [OLE,](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)vea OLE y Transferencia de datos .</span><span class="sxs-lookup"><span data-stu-id="0232a-123">For more information on OLE interfaces and formats, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0232a-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0232a-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0232a-125">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="0232a-125">Protocol specifications</span></span>

<span data-ttu-id="0232a-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0232a-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0232a-127">Controla objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="0232a-127">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="0232a-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0232a-128">Header Files</span></span>

<span data-ttu-id="0232a-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0232a-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="0232a-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0232a-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="0232a-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0232a-131">Mapitags.h</span></span>
  
> <span data-ttu-id="0232a-132">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="0232a-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0232a-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="0232a-133">See also</span></span>



[<span data-ttu-id="0232a-134">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0232a-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0232a-135">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="0232a-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0232a-136">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0232a-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0232a-137">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="0232a-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

