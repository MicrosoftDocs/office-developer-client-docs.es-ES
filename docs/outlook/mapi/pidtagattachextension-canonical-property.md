---
title: Propiedad canónica PidTagAttachExtension
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachExtension
api_type:
- HeaderDef
ms.assetid: 667da30b-e11c-4040-aecf-bb35eed23722
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 71ad53880c400d924d73c903bd77f7b447a69d8b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577726"
---
# <a name="pidtagattachextension-canonical-property"></a><span data-ttu-id="29ddd-103">Propiedad canónica PidTagAttachExtension</span><span class="sxs-lookup"><span data-stu-id="29ddd-103">PidTagAttachExtension Canonical Property</span></span>

  
  
<span data-ttu-id="29ddd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29ddd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29ddd-105">Contiene una extensión de nombre de archivo que indica el tipo de documento de un archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="29ddd-105">Contains a file name extension that indicates the document type of an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="29ddd-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="29ddd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="29ddd-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span><span class="sxs-lookup"><span data-stu-id="29ddd-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span></span>  <br/> |
|<span data-ttu-id="29ddd-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="29ddd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="29ddd-109">0x3703</span><span class="sxs-lookup"><span data-stu-id="29ddd-109">0x3703</span></span>  <br/> |
|<span data-ttu-id="29ddd-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="29ddd-110">Data type:</span></span>  <br/> |<span data-ttu-id="29ddd-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="29ddd-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="29ddd-112">Área:</span><span class="sxs-lookup"><span data-stu-id="29ddd-112">Area:</span></span>  <br/> |<span data-ttu-id="29ddd-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="29ddd-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29ddd-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="29ddd-114">Remarks</span></span>

<span data-ttu-id="29ddd-115">Estas propiedades se establecen mediante la aplicación de cliente en tiempo de envío.</span><span class="sxs-lookup"><span data-stu-id="29ddd-115">These properties are set by the client application at submission time.</span></span> 
  
<span data-ttu-id="29ddd-116">La mensajería usos del sistema **PR_ATTACH_EXTENSION** al convertir los datos adjuntos de mensajes (en la ruta de conversión) o el inicio de aplicaciones en función de los datos adjuntos en los mensajes recibidos.</span><span class="sxs-lookup"><span data-stu-id="29ddd-116">The messaging system uses **PR_ATTACH_EXTENSION** when converting message attachments (in-route conversion) or launching applications based on attachments in received messages.</span></span> <span data-ttu-id="29ddd-117">Si el cliente de envío no proporciona un valor para estas propiedades, el almacén de mensajes de tratamiento de los datos adjuntos no está obligado a generarlo.</span><span class="sxs-lookup"><span data-stu-id="29ddd-117">If the sending client does not provide a value for these properties, the message store handling the attachment is not obligated to generate it.</span></span> <span data-ttu-id="29ddd-118">El cliente receptor debe comprobar **PR_ATTACH_EXTENSION**y, si no se proporciona, debe analizar la extensión de nombre de archivo de los datos de adjuntos **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) o **PR_ATTACH_LONG_FILENAME **([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) (propiedad).</span><span class="sxs-lookup"><span data-stu-id="29ddd-118">The receiving client should first check for **PR_ATTACH_EXTENSION**, and if it is not provided, should parse the file name extension from the attachment's **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) or **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="29ddd-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="29ddd-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="29ddd-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="29ddd-120">Protocol specifications</span></span>

<span data-ttu-id="29ddd-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="29ddd-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="29ddd-122">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="29ddd-122">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="29ddd-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="29ddd-123">Header files</span></span>

<span data-ttu-id="29ddd-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="29ddd-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="29ddd-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="29ddd-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="29ddd-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="29ddd-126">Mapitags.h</span></span>
  
> <span data-ttu-id="29ddd-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="29ddd-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="29ddd-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="29ddd-128">See also</span></span>



[<span data-ttu-id="29ddd-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="29ddd-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="29ddd-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="29ddd-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="29ddd-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="29ddd-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="29ddd-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="29ddd-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

