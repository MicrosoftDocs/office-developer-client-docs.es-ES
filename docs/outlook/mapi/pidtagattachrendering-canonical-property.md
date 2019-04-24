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
ms.openlocfilehash: 22d3e649641dbe688912ecece7fde73a555f4a88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361099"
---
# <a name="pidtagattachrendering-canonical-property"></a><span data-ttu-id="68991-103">Propiedad canónica PidTagAttachRendering</span><span class="sxs-lookup"><span data-stu-id="68991-103">PidTagAttachRendering Canonical Property</span></span>

  
  
<span data-ttu-id="68991-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68991-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68991-105">Contiene un metarchivo de Microsoft Windows con información de representación de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="68991-105">Contains a Microsoft Windows metafile with rendering information for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="68991-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="68991-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="68991-107">PR_ATTACH_RENDERING</span><span class="sxs-lookup"><span data-stu-id="68991-107">PR_ATTACH_RENDERING</span></span>  <br/> |
|<span data-ttu-id="68991-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="68991-108">Identifier:</span></span>  <br/> |<span data-ttu-id="68991-109">0x3709</span><span class="sxs-lookup"><span data-stu-id="68991-109">0x3709</span></span>  <br/> |
|<span data-ttu-id="68991-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="68991-110">Data type:</span></span>  <br/> |<span data-ttu-id="68991-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="68991-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="68991-112">Área:</span><span class="sxs-lookup"><span data-stu-id="68991-112">Area:</span></span>  <br/> |<span data-ttu-id="68991-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="68991-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68991-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="68991-114">Remarks</span></span>

<span data-ttu-id="68991-115">La finalidad de esta propiedad es proporcionar un icono u otra representación gráfica que puede mostrarse dentro del mensaje primario en el punto de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="68991-115">The purpose of this property is to provide an icon or other pictorial representation that can be displayed within the parent message at the point of attachment.</span></span> <span data-ttu-id="68991-116">Esta representación suele incluir el nombre de los datos adjuntos, si los hay, y la naturaleza de los datos adjuntos, como un documento de Microsoft Office Word.</span><span class="sxs-lookup"><span data-stu-id="68991-116">Such representation typically includes the name of the attachment, if any, and the nature of the attachment, such as a Microsoft Office Word document.</span></span> <span data-ttu-id="68991-117">Una aplicación cliente puede usar esta representación para mostrar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="68991-117">A client application can use this representation in the display of the message.</span></span> 
  
<span data-ttu-id="68991-118">Para un archivo adjunto, esta propiedad suele ilustrar un icono para el archivo.</span><span class="sxs-lookup"><span data-stu-id="68991-118">For an attached file, this property usually portrays an icon for the file.</span></span> 
  
<span data-ttu-id="68991-119">Para un mensaje adjunto, esta propiedad no suele establecerse.</span><span class="sxs-lookup"><span data-stu-id="68991-119">For an attached message, this property is typically not set.</span></span> <span data-ttu-id="68991-120">Una aplicación cliente que necesita representar un mensaje adjunto debe obtener su propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), llamar a [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) para un puntero al objeto de información de formulario correspondiente, Abra la interfaz [IMAPIFormInfo](imapiforminfoimapiprop.md) en ese objeto y use **GetProps** para recuperar la propiedad **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) o **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="68991-120">A client application needing to render an attached message should obtain its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) for a pointer to the corresponding form information object, open the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface on that object, and use **GetProps** to retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="68991-121">Para un objeto OLE estático incrustado, esta propiedad contiene un metarchivo de Microsoft Windows que se puede utilizar para dibujar la representación de datos adjuntos en una ventana.</span><span class="sxs-lookup"><span data-stu-id="68991-121">For an embedded static OLE object, this property contains a Microsoft Windows metafile that can be used to draw the attachment representation in a window.</span></span> 
  
<span data-ttu-id="68991-122">Para un objeto OLE dinámico incrustado, el cliente debe usar los datos OLE para generar la información de representación.</span><span class="sxs-lookup"><span data-stu-id="68991-122">For an embedded dynamic OLE object, the client should use the OLE data to generate the rendering information.</span></span> 
  
<span data-ttu-id="68991-123">En todos los casos, la aplicación cliente debe tener en cuenta que esta propiedad suele tener un tamaño de varios cientos de bytes y está sujeta a truncamiento en la tabla de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="68991-123">In all cases, the client application should be aware that this property is usually several hundred bytes in size and is subject to truncation in the attachment table.</span></span> <span data-ttu-id="68991-124">Si un cliente desea representar los datos adjuntos desde esta propiedad sin abrir los datos adjuntos en sí, debe funcionar dentro de la regla de truncamiento de tablas.</span><span class="sxs-lookup"><span data-stu-id="68991-124">If a client wishes to render the attachment from this property without opening the attachment itself, it must work within the table truncation rule.</span></span> <span data-ttu-id="68991-125">Para obtener más información, vea [trabajar con columnas de gran tamaño](working-with-large-columns.md).</span><span class="sxs-lookup"><span data-stu-id="68991-125">For more information, see [Working with Large Columns](working-with-large-columns.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="68991-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="68991-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="68991-127">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="68991-127">Protocol specifications</span></span>

<span data-ttu-id="68991-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="68991-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="68991-129">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="68991-129">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="68991-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="68991-130">Header files</span></span>

<span data-ttu-id="68991-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="68991-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="68991-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="68991-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="68991-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="68991-133">Mapitags.h</span></span>
  
> <span data-ttu-id="68991-134">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="68991-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="68991-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="68991-135">See also</span></span>



[<span data-ttu-id="68991-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="68991-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="68991-137">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="68991-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="68991-138">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="68991-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="68991-139">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="68991-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

