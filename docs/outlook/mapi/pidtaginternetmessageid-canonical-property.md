---
title: Propiedad canónica PidTagInternetMessageId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetMessageId
api_type:
- HeaderDef
ms.assetid: 5c93d00c-a199-4d45-9bf6-87bd2ffe4784
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c2cc0eabd9c329953d9b0d252418549ea1c588a1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391930"
---
# <a name="pidtaginternetmessageid-canonical-property"></a><span data-ttu-id="f032f-103">Propiedad canónica PidTagInternetMessageId</span><span class="sxs-lookup"><span data-stu-id="f032f-103">PidTagInternetMessageId Canonical Property</span></span>

  
  
<span data-ttu-id="f032f-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f032f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f032f-105">Se corresponde con el campo de identificador de mensaje tal como se especifica en [RFC2822].</span><span class="sxs-lookup"><span data-stu-id="f032f-105">Corresponds to the message ID field as specified in [RFC2822].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f032f-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f032f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f032f-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span><span class="sxs-lookup"><span data-stu-id="f032f-107">PR_INTERNET_MESSAGE_ID, PR_INTERNET_MESSAGE_ID_A, PR_INTERNET_MESSAGE_ID_W</span></span>  <br/> |
|<span data-ttu-id="f032f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f032f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f032f-109">0x1035</span><span class="sxs-lookup"><span data-stu-id="f032f-109">0x1035</span></span>  <br/> |
|<span data-ttu-id="f032f-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f032f-110">Data type:</span></span>  <br/> |<span data-ttu-id="f032f-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f032f-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f032f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f032f-112">Area:</span></span>  <br/> |<span data-ttu-id="f032f-113">MIME</span><span class="sxs-lookup"><span data-stu-id="f032f-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f032f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f032f-114">Remarks</span></span>

<span data-ttu-id="f032f-115">Estas propiedades deben estar presentes en todos los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f032f-115">These properties should be present on all email messages.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f032f-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f032f-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f032f-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f032f-117">Protocol specifications</span></span>

<span data-ttu-id="f032f-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f032f-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f032f-119">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f032f-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f032f-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f032f-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f032f-121">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f032f-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f032f-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f032f-122">Header files</span></span>

<span data-ttu-id="f032f-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f032f-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f032f-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f032f-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f032f-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f032f-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f032f-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f032f-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f032f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="f032f-127">See also</span></span>



[<span data-ttu-id="f032f-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f032f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f032f-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f032f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f032f-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f032f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f032f-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="f032f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

