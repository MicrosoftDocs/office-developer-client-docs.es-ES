---
title: Propiedad canónica PidTagAttachDataObject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataObject
api_type:
- HeaderDef
ms.assetid: b76312c6-7682-4ded-be25-55e21b0b091b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3961330476cad8947f94152e49c90adb1e8f8b21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339287"
---
# <a name="pidtagattachdataobject-canonical-property"></a><span data-ttu-id="0291c-103">Propiedad canónica PidTagAttachDataObject</span><span class="sxs-lookup"><span data-stu-id="0291c-103">PidTagAttachDataObject Canonical Property</span></span>

  
  
<span data-ttu-id="0291c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0291c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0291c-105">Contiene un objeto adjunto al que normalmente se tiene acceso a través de la interfaz **IStorage** de vinculación e incrustación de objetos (OLE).</span><span class="sxs-lookup"><span data-stu-id="0291c-105">Contains an attachment object typically accessed through the Object Linking and Embedding (OLE) **IStorage** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0291c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0291c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0291c-107">PR_ATTACH_DATA_OBJ</span><span class="sxs-lookup"><span data-stu-id="0291c-107">PR_ATTACH_DATA_OBJ</span></span>  <br/> |
|<span data-ttu-id="0291c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0291c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0291c-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="0291c-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="0291c-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0291c-110">Data type:</span></span>  <br/> |<span data-ttu-id="0291c-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="0291c-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="0291c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0291c-112">Area:</span></span>  <br/> |<span data-ttu-id="0291c-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="0291c-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0291c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0291c-114">Remarks</span></span>

<span data-ttu-id="0291c-115">Esta propiedad contiene los datos adjuntos cuando el valor de la propiedad **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) es **ATTACH_EMBEDDED_MSG** o **ATTACH_OLE**.</span><span class="sxs-lookup"><span data-stu-id="0291c-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is **ATTACH_EMBEDDED_MSG** or **ATTACH_OLE**.</span></span> <span data-ttu-id="0291c-116">El tipo de codificación OLE se puede determinar **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0291c-116">The OLE encoding type can be determined from **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span></span> 
  
<span data-ttu-id="0291c-117">Para los datos adjuntos asociados **ATTACH_EMBEDDED_MSG** valor, la [interfaz IMessage:IMAPIProp](imessageimapiprop.md) se puede usar para un acceso más rápido.</span><span class="sxs-lookup"><span data-stu-id="0291c-117">For an attachment associated with the **ATTACH_EMBEDDED_MSG** value, the [IMessage:IMAPIProp](imessageimapiprop.md) interface can be used for faster access.</span></span> 
  
<span data-ttu-id="0291c-118">Para un objeto OLE dinámico incrustado, la propiedad **PR_ATTACH_DATA_OBJ** contiene su propia información de representación y la propiedad **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) debe ser inexistente o vacía.</span><span class="sxs-lookup"><span data-stu-id="0291c-118">For an embedded dynamic OLE object, the **PR_ATTACH_DATA_OBJ** property contains its own rendering information, and the **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) property should be either nonexistent or empty.</span></span> 
  
<span data-ttu-id="0291c-119">Para los datos adjuntos de un archivo de documento OLE, el proveedor del almacén de mensajes debe responder **a** una llamada [IMAPIProp::OpenProperty](imapiprop-openproperty.md) en PR_ATTACH_DATA_OBJ y, opcionalmente, puede responder a una llamada en **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0291c-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** and may optionally respond to a call on **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span></span> <span data-ttu-id="0291c-120">Las **PR_ATTACH_DATA_BIN** y **PR_ATTACH_DATA_OBJ** comparten el mismo identificador de propiedad y, por lo tanto, son dos representaciones de la misma propiedad.</span><span class="sxs-lookup"><span data-stu-id="0291c-120">The **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** properties share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="0291c-121">Para un objeto de almacenamiento, como un archivo compuesto en formato docfile OLE 2.0, algunos proveedores de servicios permiten que se abra con la interfaz **MAPI IStreamDocfile,** una subclase de **IStream** sin miembros adicionales, diseñada para optimizar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="0291c-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface, a subclass of **IStream** with no additional members, designed to optimize performance.</span></span> <span data-ttu-id="0291c-122">El posible almacenamiento es suficiente para justificar el intento de abrir **PR_ATTACH_DATA_OBJ** a través **de IStreamDocfile**.</span><span class="sxs-lookup"><span data-stu-id="0291c-122">The potential saving is enough to justify attempting to open **PR_ATTACH_DATA_OBJ** through **IStreamDocfile**.</span></span> <span data-ttu-id="0291c-123">Si **MAPI_E_INTERFACE_NOT_SUPPORTED** se devuelve, el cliente puede abrir **PR_ATTACH_DATA_BIN** con **IStream**.</span><span class="sxs-lookup"><span data-stu-id="0291c-123">If **MAPI_E_INTERFACE_NOT_SUPPORTED** is returned, the client can then open **PR_ATTACH_DATA_BIN** with **IStream**.</span></span> 
  
<span data-ttu-id="0291c-124">Si la aplicación cliente o el proveedor de servicios no pueden abrir un subobjeto de datos adjuntos mediante **PR_ATTACH_DATA_OBJ** con la ayuda de **PR_ATTACH_METHOD**, debe usar **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="0291c-124">If the client application or service provider cannot open an attachment subobject by using **PR_ATTACH_DATA_OBJ** with the help of **PR_ATTACH_METHOD**, it should use **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="0291c-125">Para obtener más información sobre las interfaces y formatos OLE, vea [OLE y transferencia de datos.](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)</span><span class="sxs-lookup"><span data-stu-id="0291c-125">For more information on OLE interfaces and formats, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0291c-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0291c-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0291c-127">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="0291c-127">Protocol specifications</span></span>

<span data-ttu-id="0291c-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0291c-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0291c-129">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="0291c-129">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="0291c-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0291c-130">Header Files</span></span>

<span data-ttu-id="0291c-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0291c-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="0291c-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0291c-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="0291c-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0291c-133">Mapitags.h</span></span>
  
> <span data-ttu-id="0291c-134">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="0291c-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0291c-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0291c-135">See also</span></span>



[<span data-ttu-id="0291c-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0291c-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0291c-137">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="0291c-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0291c-138">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0291c-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0291c-139">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="0291c-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

