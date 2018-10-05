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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398076"
---
# <a name="pidtagattachdataobject-canonical-property"></a><span data-ttu-id="2c3d4-103">Propiedad canónica PidTagAttachDataObject</span><span class="sxs-lookup"><span data-stu-id="2c3d4-103">PidTagAttachDataObject Canonical Property</span></span>

  
  
<span data-ttu-id="2c3d4-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c3d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c3d4-105">Contiene un objeto attachment normalmente tiene acceso a través de la interfaz de vinculación e incrustación de objetos (OLE) **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="2c3d4-105">Contains an attachment object typically accessed through the Object Linking and Embedding (OLE) **IStorage** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2c3d4-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2c3d4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2c3d4-107">PR_ATTACH_DATA_OBJ</span><span class="sxs-lookup"><span data-stu-id="2c3d4-107">PR_ATTACH_DATA_OBJ</span></span>  <br/> |
|<span data-ttu-id="2c3d4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2c3d4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2c3d4-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="2c3d4-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="2c3d4-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2c3d4-110">Data type:</span></span>  <br/> |<span data-ttu-id="2c3d4-111">PT OBJECT</span><span class="sxs-lookup"><span data-stu-id="2c3d4-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="2c3d4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2c3d4-112">Area:</span></span>  <br/> |<span data-ttu-id="2c3d4-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="2c3d4-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c3d4-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2c3d4-114">Remarks</span></span>

<span data-ttu-id="2c3d4-115">Esta propiedad contiene los datos adjuntos cuando el valor de la propiedad **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) es **ATTACH_EMBEDDED_MSG** o **ATTACH_OLE**.</span><span class="sxs-lookup"><span data-stu-id="2c3d4-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is **ATTACH_EMBEDDED_MSG** or **ATTACH_OLE**.</span></span> <span data-ttu-id="2c3d4-116">Desde **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)), se puede determinar el tipo de codificación de OLE.</span><span class="sxs-lookup"><span data-stu-id="2c3d4-116">The OLE encoding type can be determined from **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span></span> 
  
<span data-ttu-id="2c3d4-117">Para los datos adjuntos asociados con el valor **ATTACH_EMBEDDED_MSG** , se puede usar la interfaz [IMessage:IMAPIProp](imessageimapiprop.md) para un acceso más rápido.</span><span class="sxs-lookup"><span data-stu-id="2c3d4-117">For an attachment associated with the **ATTACH_EMBEDDED_MSG** value, the [IMessage:IMAPIProp](imessageimapiprop.md) interface can be used for faster access.</span></span> 
  
<span data-ttu-id="2c3d4-118">Para un objeto OLE incrustado dinámico, la propiedad **PR_ATTACH_DATA_OBJ** contiene su propia información de representación y debe ser la propiedad **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) que no existe o está vacía.</span><span class="sxs-lookup"><span data-stu-id="2c3d4-118">For an embedded dynamic OLE object, the **PR_ATTACH_DATA_OBJ** property contains its own rendering information, and the **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) property should be either nonexistent or empty.</span></span> 
  
<span data-ttu-id="2c3d4-119">Para los datos adjuntos un archivo de documento OLE, el proveedor de almacén de mensajes, debe responder a una llamada de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) en **PR_ATTACH_DATA_OBJ** y, opcionalmente, puede responder a una llamada en **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="2c3d4-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** and may optionally respond to a call on **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span></span> <span data-ttu-id="2c3d4-120">Las propiedades **PR_ATTACH_DATA_BIN** y **PR_ATTACH_DATA_OBJ** compartan el mismo identificador de propiedad y, por tanto, son dos copias de la misma propiedad.</span><span class="sxs-lookup"><span data-stu-id="2c3d4-120">The **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** properties share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="2c3d4-121">Para un objeto de almacenamiento, como un archivo compuesto en el formato de archivo doc de OLE 2.0, algunos proveedores de servicios de permitir que se va a abrir con la interfaz de MAPI **IStreamDocfile** , una subclase de **IStream** sin miembros adicionales, diseñado para optimizar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="2c3d4-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface, a subclass of **IStream** with no additional members, designed to optimize performance.</span></span> <span data-ttu-id="2c3d4-122">El ahorro potencial es suficiente para justificar al intentar abrir **PR_ATTACH_DATA_OBJ** a través de **IStreamDocfile**.</span><span class="sxs-lookup"><span data-stu-id="2c3d4-122">The potential saving is enough to justify attempting to open **PR_ATTACH_DATA_OBJ** through **IStreamDocfile**.</span></span> <span data-ttu-id="2c3d4-123">Si se devuelve **MAPI_E_INTERFACE_NOT_SUPPORTED** , el cliente, a continuación, puede abrir **PR_ATTACH_DATA_BIN** con **IStream**.</span><span class="sxs-lookup"><span data-stu-id="2c3d4-123">If **MAPI_E_INTERFACE_NOT_SUPPORTED** is returned, the client can then open **PR_ATTACH_DATA_BIN** with **IStream**.</span></span> 
  
<span data-ttu-id="2c3d4-124">Si la aplicación cliente o el proveedor de servicios no se puede abrir un subobjetos datos adjuntos mediante el uso de **PR_ATTACH_DATA_OBJ** con la Ayuda de **PR_ATTACH_METHOD**, que debe usar **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="2c3d4-124">If the client application or service provider cannot open an attachment subobject by using **PR_ATTACH_DATA_OBJ** with the help of **PR_ATTACH_METHOD**, it should use **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="2c3d4-125">Para obtener más información sobre las interfaces OLE y formatos, vea [OLE y la transferencia de datos](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span><span class="sxs-lookup"><span data-stu-id="2c3d4-125">For more information on OLE interfaces and formats, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2c3d4-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2c3d4-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2c3d4-127">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="2c3d4-127">Protocol specifications</span></span>

<span data-ttu-id="2c3d4-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c3d4-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c3d4-129">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="2c3d4-129">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="2c3d4-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2c3d4-130">Header Files</span></span>

<span data-ttu-id="2c3d4-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2c3d4-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="2c3d4-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2c3d4-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="2c3d4-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2c3d4-133">Mapitags.h</span></span>
  
> <span data-ttu-id="2c3d4-134">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="2c3d4-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2c3d4-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c3d4-135">See also</span></span>



[<span data-ttu-id="2c3d4-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2c3d4-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2c3d4-137">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="2c3d4-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2c3d4-138">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2c3d4-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2c3d4-139">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="2c3d4-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

