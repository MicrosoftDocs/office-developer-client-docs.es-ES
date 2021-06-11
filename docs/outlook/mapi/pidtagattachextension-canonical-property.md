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
ms.openlocfilehash: 26efa868de29bc8a6a180b717230951b76da26a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319764"
---
# <a name="pidtagattachextension-canonical-property"></a><span data-ttu-id="92eca-103">Propiedad canónica PidTagAttachExtension</span><span class="sxs-lookup"><span data-stu-id="92eca-103">PidTagAttachExtension Canonical Property</span></span>

  
  
<span data-ttu-id="92eca-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92eca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92eca-105">Contiene una extensión de nombre de archivo que indica el tipo de documento de un archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="92eca-105">Contains a file name extension that indicates the document type of an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="92eca-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="92eca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="92eca-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span><span class="sxs-lookup"><span data-stu-id="92eca-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span></span>  <br/> |
|<span data-ttu-id="92eca-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="92eca-108">Identifier:</span></span>  <br/> |<span data-ttu-id="92eca-109">0x3703</span><span class="sxs-lookup"><span data-stu-id="92eca-109">0x3703</span></span>  <br/> |
|<span data-ttu-id="92eca-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="92eca-110">Data type:</span></span>  <br/> |<span data-ttu-id="92eca-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="92eca-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="92eca-112">Área:</span><span class="sxs-lookup"><span data-stu-id="92eca-112">Area:</span></span>  <br/> |<span data-ttu-id="92eca-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="92eca-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92eca-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="92eca-114">Remarks</span></span>

<span data-ttu-id="92eca-115">La aplicación cliente establece estas propiedades en el momento del envío.</span><span class="sxs-lookup"><span data-stu-id="92eca-115">These properties are set by the client application at submission time.</span></span> 
  
<span data-ttu-id="92eca-116">El sistema de mensajería usa **PR_ATTACH_EXTENSION** al convertir datos adjuntos de mensajes (conversión en ruta) o iniciar aplicaciones basadas en datos adjuntos en mensajes recibidos.</span><span class="sxs-lookup"><span data-stu-id="92eca-116">The messaging system uses **PR_ATTACH_EXTENSION** when converting message attachments (in-route conversion) or launching applications based on attachments in received messages.</span></span> <span data-ttu-id="92eca-117">Si el cliente de envío no proporciona un valor para estas propiedades, el almacén de mensajes que administra los datos adjuntos no está obligado a generarlo.</span><span class="sxs-lookup"><span data-stu-id="92eca-117">If the sending client does not provide a value for these properties, the message store handling the attachment is not obligated to generate it.</span></span> <span data-ttu-id="92eca-118">El cliente receptor debe comprobar primero si **PR_ATTACH_EXTENSION** y, si no se proporciona, debe analizar la extensión de nombre de archivo de la propiedad **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) o **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="92eca-118">The receiving client should first check for **PR_ATTACH_EXTENSION**, and if it is not provided, should parse the file name extension from the attachment's **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) or **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="92eca-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="92eca-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="92eca-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="92eca-120">Protocol specifications</span></span>

<span data-ttu-id="92eca-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92eca-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92eca-122">Controla objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="92eca-122">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="92eca-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="92eca-123">Header files</span></span>

<span data-ttu-id="92eca-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="92eca-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="92eca-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="92eca-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="92eca-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="92eca-126">Mapitags.h</span></span>
  
> <span data-ttu-id="92eca-127">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="92eca-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="92eca-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="92eca-128">See also</span></span>



[<span data-ttu-id="92eca-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="92eca-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="92eca-130">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="92eca-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="92eca-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="92eca-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="92eca-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="92eca-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

