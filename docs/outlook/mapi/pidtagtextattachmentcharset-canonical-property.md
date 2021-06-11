---
title: Propiedad canónica PidTagTextAttachmentCharset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTextAttachmentCharset
api_type:
- COM
ms.assetid: d347c949-d0c3-4a36-8447-3fa01111cdc1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1db41bc5c7ea71d65d892da520d4258354eb53cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358817"
---
# <a name="pidtagtextattachmentcharset-canonical-property"></a><span data-ttu-id="fc208-103">Propiedad canónica PidTagTextAttachmentCharset</span><span class="sxs-lookup"><span data-stu-id="fc208-103">PidTagTextAttachmentCharset Canonical Property</span></span>

  
  
<span data-ttu-id="fc208-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc208-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc208-105">Contiene el valor del conjunto de caracteres de un archivo adjunto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="fc208-105">Contains a message attachment's character set value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fc208-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fc208-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fc208-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="fc208-107">None</span></span>  <br/> |
|<span data-ttu-id="fc208-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fc208-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fc208-109">0x371B</span><span class="sxs-lookup"><span data-stu-id="fc208-109">0x371B</span></span>  <br/> |
|<span data-ttu-id="fc208-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fc208-110">Data type:</span></span>  <br/> |<span data-ttu-id="fc208-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fc208-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fc208-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fc208-112">Area:</span></span>  <br/> |<span data-ttu-id="fc208-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="fc208-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc208-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fc208-114">Remarks</span></span>

<span data-ttu-id="fc208-115">Los datos de esta propiedad se derivan de un campo de encabezado MIME de tipo de contenido que comienza por "text/", si hay un parámetro "charset".</span><span class="sxs-lookup"><span data-stu-id="fc208-115">This property's data is derived from a Content-Type MIME header field that starts with "text/", if a "charset" parameter is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fc208-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc208-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fc208-117">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="fc208-117">Protocol specifications</span></span>

<span data-ttu-id="fc208-118">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc208-118">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc208-119">Convierte de convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="fc208-119">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fc208-120">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fc208-120">Header files</span></span>

<span data-ttu-id="fc208-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fc208-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="fc208-122">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fc208-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="fc208-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fc208-123">Mapitags.h</span></span>
  
> <span data-ttu-id="fc208-124">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="fc208-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fc208-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc208-125">See also</span></span>



[<span data-ttu-id="fc208-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fc208-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fc208-127">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="fc208-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fc208-128">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="fc208-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fc208-129">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="fc208-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

