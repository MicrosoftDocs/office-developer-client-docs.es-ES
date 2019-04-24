---
title: Propiedad canónica PidTagBody
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBody
api_type:
- HeaderDef
ms.assetid: 47c0d0fe-4d57-4b81-bdb5-336de85c194c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 243a59798980d8c0cfaf1a726d6408dbd66ebba8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326638"
---
# <a name="pidtagbody-canonical-property"></a><span data-ttu-id="bf327-103">Propiedad canónica PidTagBody</span><span class="sxs-lookup"><span data-stu-id="bf327-103">PidTagBody Canonical Property</span></span>

  
  
<span data-ttu-id="bf327-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf327-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf327-105">Contiene el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="bf327-105">Contains the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bf327-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="bf327-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bf327-107">PR_BODY, PR_BODY_A, PR_BODY_W</span><span class="sxs-lookup"><span data-stu-id="bf327-107">PR_BODY, PR_BODY_A, PR_BODY_W</span></span>  <br/> |
|<span data-ttu-id="bf327-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="bf327-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bf327-109">0x1000</span><span class="sxs-lookup"><span data-stu-id="bf327-109">0x1000</span></span>  <br/> |
|<span data-ttu-id="bf327-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="bf327-110">Data type:</span></span>  <br/> |<span data-ttu-id="bf327-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="bf327-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="bf327-112">Área:</span><span class="sxs-lookup"><span data-stu-id="bf327-112">Area:</span></span>  <br/> |<span data-ttu-id="bf327-113">Mensajes generales</span><span class="sxs-lookup"><span data-stu-id="bf327-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf327-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bf327-114">Remarks</span></span>

<span data-ttu-id="bf327-115">Normalmente, estas propiedades solo se usan en un mensaje interpersonal (IPM).</span><span class="sxs-lookup"><span data-stu-id="bf327-115">These properties are typically used only in an interpersonal message (IPM).</span></span> 
  
<span data-ttu-id="bf327-116">Los almacenes de mensajes que admiten el formato de texto enriquecido (RTF) omiten los cambios en el espacio en blanco del texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="bf327-116">Message stores that support Rich Text Format (RTF) ignore any changes to white space in the message text.</span></span> <span data-ttu-id="bf327-117">Cuando **PR_BODY** se almacena por primera vez, el almacén de mensajes también genera y almacena la propiedad **PR_RTF_COMPRESSED** ([PIDTAGRTFCOMPRESSED](pidtagrtfcompressed-canonical-property.md)), la versión rtf del texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="bf327-117">When **PR_BODY** is stored for the first time, the message store also generates and stores the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the RTF version of the message text.</span></span> <span data-ttu-id="bf327-118">Si se llama al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) posteriormente y se ha modificado **PR_BODY** , el almacén de mensajes llama a la función [RTFSync](rtfsync.md) para garantizar la sincronización con la versión rtf.</span><span class="sxs-lookup"><span data-stu-id="bf327-118">If the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is subsequently called and **PR_BODY** has been modified, the message store calls the [RTFSync](rtfsync.md) function to ensure synchronization with the RTF version.</span></span> <span data-ttu-id="bf327-119">Si solo se ha cambiado el espacio en blanco, las propiedades permanecen sin cambios.</span><span class="sxs-lookup"><span data-stu-id="bf327-119">If only white space has been changed, the properties are left unchanged.</span></span> <span data-ttu-id="bf327-120">Esto conserva todo el formato RTF no trivial cuando el mensaje se desplaza a través de clientes no compatibles con RTF y sistemas de mensajería.</span><span class="sxs-lookup"><span data-stu-id="bf327-120">This preserves any nontrivial RTF formatting when the message travels through non-RTF-aware clients and messaging systems.</span></span> 
  
<span data-ttu-id="bf327-121">El valor de esta propiedad debe expresarse en la página de códigos del sistema operativo en el que se está ejecutando MAPI.</span><span class="sxs-lookup"><span data-stu-id="bf327-121">The value for this property must be expressed in the code page of the operating system that MAPI is running on.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bf327-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bf327-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bf327-123">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="bf327-123">Protocol specifications</span></span>

<span data-ttu-id="bf327-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf327-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf327-125">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="bf327-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bf327-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf327-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bf327-127">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="bf327-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bf327-128">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="bf327-128">Header files</span></span>

<span data-ttu-id="bf327-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bf327-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="bf327-130">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="bf327-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="bf327-131">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="bf327-131">Mapitags.h</span></span>
  
> <span data-ttu-id="bf327-132">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="bf327-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bf327-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf327-133">See also</span></span>



[<span data-ttu-id="bf327-134">Propiedad canónica PidTagRtfInSync</span><span class="sxs-lookup"><span data-stu-id="bf327-134">PidTagRtfInSync Canonical Property</span></span>](pidtagrtfinsync-canonical-property.md)


[<span data-ttu-id="bf327-135">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bf327-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bf327-136">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="bf327-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bf327-137">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="bf327-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bf327-138">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="bf327-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

