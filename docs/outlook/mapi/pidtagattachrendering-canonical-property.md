---
title: Propiedad canónica PidTagAttachRendering
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachRendering
api_type:
- HeaderDef
ms.assetid: 1f31f7f4-fbda-4337-95e5-5474dd1bf84a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 45d4b0bfe7f902ee2cfe1d735c990d80f8fbb60d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588947"
---
# <a name="pidtagattachrendering-canonical-property"></a><span data-ttu-id="91f8a-103">Propiedad canónica PidTagAttachRendering</span><span class="sxs-lookup"><span data-stu-id="91f8a-103">PidTagAttachRendering Canonical Property</span></span>

  
  
<span data-ttu-id="91f8a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91f8a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91f8a-105">Contiene un metarchivo de Microsoft Windows con la información de representación de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="91f8a-105">Contains a Microsoft Windows metafile with rendering information for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="91f8a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="91f8a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="91f8a-107">PR_ATTACH_RENDERING</span><span class="sxs-lookup"><span data-stu-id="91f8a-107">PR_ATTACH_RENDERING</span></span>  <br/> |
|<span data-ttu-id="91f8a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="91f8a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="91f8a-109">0x3709</span><span class="sxs-lookup"><span data-stu-id="91f8a-109">0x3709</span></span>  <br/> |
|<span data-ttu-id="91f8a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="91f8a-110">Data type:</span></span>  <br/> |<span data-ttu-id="91f8a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="91f8a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="91f8a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="91f8a-112">Area:</span></span>  <br/> |<span data-ttu-id="91f8a-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="91f8a-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91f8a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="91f8a-114">Remarks</span></span>

<span data-ttu-id="91f8a-115">El propósito de esta propiedad es proporcionar un icono u otra representación gráfica que se puede mostrar dentro del mensaje primario en el punto de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="91f8a-115">The purpose of this property is to provide an icon or other pictorial representation that can be displayed within the parent message at the point of attachment.</span></span> <span data-ttu-id="91f8a-116">La representación normalmente incluye el nombre de los datos adjuntos, si lo hay y la naturaleza de los datos adjuntos, como un documento de Microsoft Office Word.</span><span class="sxs-lookup"><span data-stu-id="91f8a-116">Such representation typically includes the name of the attachment, if any, and the nature of the attachment, such as a Microsoft Office Word document.</span></span> <span data-ttu-id="91f8a-117">Una aplicación cliente puede utilizar esta representación en la visualización del mensaje.</span><span class="sxs-lookup"><span data-stu-id="91f8a-117">A client application can use this representation in the display of the message.</span></span> 
  
<span data-ttu-id="91f8a-118">Para un archivo adjunto, esta propiedad normalmente representa un icono para el archivo.</span><span class="sxs-lookup"><span data-stu-id="91f8a-118">For an attached file, this property usually portrays an icon for the file.</span></span> 
  
<span data-ttu-id="91f8a-119">Para un mensaje adjunto, esta propiedad no se establece normalmente.</span><span class="sxs-lookup"><span data-stu-id="91f8a-119">For an attached message, this property is typically not set.</span></span> <span data-ttu-id="91f8a-120">Una aplicación de cliente que se necesitan representar un mensaje adjunto debe obtener su propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), llame a [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) para un puntero al objeto de información de formulario correspondiente, Abra la interfaz de [IMAPIFormInfo](imapiforminfoimapiprop.md) en ese objeto y use **GetProps** para recuperar la propiedad de **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) o **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="91f8a-120">A client application needing to render an attached message should obtain its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) for a pointer to the corresponding form information object, open the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface on that object, and use **GetProps** to retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="91f8a-121">Para un objeto OLE incrustado estático, esta propiedad contiene un metarchivo de Microsoft Windows que se puede usar para dibujar la representación de datos adjuntos en una ventana.</span><span class="sxs-lookup"><span data-stu-id="91f8a-121">For an embedded static OLE object, this property contains a Microsoft Windows metafile that can be used to draw the attachment representation in a window.</span></span> 
  
<span data-ttu-id="91f8a-122">Para un objeto OLE incrustado dinámico, el cliente debe utilizar los datos OLE para generar la información de representación.</span><span class="sxs-lookup"><span data-stu-id="91f8a-122">For an embedded dynamic OLE object, the client should use the OLE data to generate the rendering information.</span></span> 
  
<span data-ttu-id="91f8a-123">En todos los casos, la aplicación cliente deben tener en cuenta que esta propiedad suele ser varios cientos de bytes en tamaño y está sujeta a truncamiento en la tabla de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="91f8a-123">In all cases, the client application should be aware that this property is usually several hundred bytes in size and is subject to truncation in the attachment table.</span></span> <span data-ttu-id="91f8a-124">Si un cliente desea representar los datos adjuntos de esta propiedad sin abrir los datos adjuntos del propio, debe trabajar dentro de la regla de truncamiento de tabla.</span><span class="sxs-lookup"><span data-stu-id="91f8a-124">If a client wishes to render the attachment from this property without opening the attachment itself, it must work within the table truncation rule.</span></span> <span data-ttu-id="91f8a-125">Para obtener más información, vea [trabajar con columnas de gran tamaño](working-with-large-columns.md).</span><span class="sxs-lookup"><span data-stu-id="91f8a-125">For more information, see [Working with Large Columns](working-with-large-columns.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="91f8a-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="91f8a-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="91f8a-127">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="91f8a-127">Protocol specifications</span></span>

<span data-ttu-id="91f8a-128">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91f8a-128">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91f8a-129">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="91f8a-129">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="91f8a-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="91f8a-130">Header files</span></span>

<span data-ttu-id="91f8a-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="91f8a-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="91f8a-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="91f8a-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="91f8a-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="91f8a-133">Mapitags.h</span></span>
  
> <span data-ttu-id="91f8a-134">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="91f8a-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91f8a-135">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="91f8a-135">See also</span></span>



[<span data-ttu-id="91f8a-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="91f8a-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="91f8a-137">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="91f8a-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="91f8a-138">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="91f8a-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="91f8a-139">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="91f8a-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

