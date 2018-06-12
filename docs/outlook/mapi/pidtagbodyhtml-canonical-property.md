---
title: Propiedad canónico PidTagBodyHtml
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyHtml
api_type:
- HeaderDef
ms.assetid: 93b9215a-5900-411c-a0ae-6bba62cd5a1e
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 19f0398d5e36cce13467a4fae86c4ea1d4019dd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819275"
---
# <a name="pidtagbodyhtml-canonical-property"></a><span data-ttu-id="cbaf6-103">Propiedad canónico PidTagBodyHtml</span><span class="sxs-lookup"><span data-stu-id="cbaf6-103">PidTagBodyHtml Canonical Property</span></span>

  
  
<span data-ttu-id="cbaf6-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cbaf6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cbaf6-105">Contiene la versión de lenguaje de marcado de hipertexto (HTML) del texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="cbaf6-105">Contains the Hypertext Markup Language (HTML) version of the message text.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cbaf6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="cbaf6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cbaf6-107">PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W</span><span class="sxs-lookup"><span data-stu-id="cbaf6-107">PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W</span></span>  <br/> |
|<span data-ttu-id="cbaf6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cbaf6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cbaf6-109">0x1013</span><span class="sxs-lookup"><span data-stu-id="cbaf6-109">0x1013</span></span>  <br/> |
|<span data-ttu-id="cbaf6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="cbaf6-110">Data type:</span></span>  <br/> |<span data-ttu-id="cbaf6-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="cbaf6-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="cbaf6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cbaf6-112">Area:</span></span>  <br/> |<span data-ttu-id="cbaf6-113">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="cbaf6-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cbaf6-114">Notas</span><span class="sxs-lookup"><span data-stu-id="cbaf6-114">Remarks</span></span>

<span data-ttu-id="cbaf6-115">Estas propiedades contienen el mismo texto del mensaje como **PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), pero en HTML.</span><span class="sxs-lookup"><span data-stu-id="cbaf6-115">These properties contain the same message text as the **PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), but in HTML.</span></span> 
  
<span data-ttu-id="cbaf6-116">Un almacén de mensajes que admite HTML indica que esta estableciendo el indicador **STORE_HTML_OK** en su **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cbaf6-116">A message store that supports HTML indicates this by setting the **STORE_HTML_OK** flag in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span></span> 
  
 <span data-ttu-id="cbaf6-117">**Nota** **STORE_HTML_OK** no está definido en las versiones de Mapidefs.h que se incluye con Microsoft® Exchange 2000 Server y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="cbaf6-117">**Note** **STORE_HTML_OK** is not defined in versions of Mapidefs.h included with Microsoft® Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="cbaf6-118">Si **STORE_HTML_OK** no está definido, use el valor 0 x 00010000 en su lugar.</span><span class="sxs-lookup"><span data-stu-id="cbaf6-118">If **STORE_HTML_OK** is undefined, use the value 0x00010000 instead.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cbaf6-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cbaf6-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cbaf6-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="cbaf6-120">Protocol specifications</span></span>

<span data-ttu-id="cbaf6-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cbaf6-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cbaf6-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="cbaf6-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cbaf6-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cbaf6-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cbaf6-124">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="cbaf6-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cbaf6-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="cbaf6-125">Header files</span></span>

<span data-ttu-id="cbaf6-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cbaf6-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="cbaf6-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="cbaf6-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="cbaf6-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cbaf6-128">Mapitags.h</span></span>
  
> <span data-ttu-id="cbaf6-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="cbaf6-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cbaf6-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="cbaf6-130">See also</span></span>



[<span data-ttu-id="cbaf6-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cbaf6-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cbaf6-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="cbaf6-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cbaf6-133">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="cbaf6-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cbaf6-134">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="cbaf6-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

