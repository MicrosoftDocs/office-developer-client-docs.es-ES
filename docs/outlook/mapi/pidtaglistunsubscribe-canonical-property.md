---
title: Propiedad canónica PidTagListUnsubscribe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListUnsubscribe
api_type:
- HeaderDef
ms.assetid: 4e6bfbc7-7586-43cc-9380-daa0fe3d85a5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e057ab2ca0c75d5c0d749ebde8f1bdfb4f1ae66a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278882"
---
# <a name="pidtaglistunsubscribe-canonical-property"></a><span data-ttu-id="43a9e-103">Propiedad canónica PidTagListUnsubscribe</span><span class="sxs-lookup"><span data-stu-id="43a9e-103">PidTagListUnsubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="43a9e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43a9e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43a9e-105">Contiene el valor del campo de encabezado de un mensaje Multipurpose Internet Mail Extensions (MIME List-Unsubscribe).</span><span class="sxs-lookup"><span data-stu-id="43a9e-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Unsubscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43a9e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="43a9e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="43a9e-107">PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="43a9e-107">PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="43a9e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="43a9e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="43a9e-109">0x1045</span><span class="sxs-lookup"><span data-stu-id="43a9e-109">0x1045</span></span>  <br/> |
|<span data-ttu-id="43a9e-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="43a9e-110">Data type:</span></span>  <br/> |<span data-ttu-id="43a9e-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="43a9e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="43a9e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="43a9e-112">Area:</span></span>  <br/> |<span data-ttu-id="43a9e-113">Varios</span><span class="sxs-lookup"><span data-stu-id="43a9e-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43a9e-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="43a9e-114">Remarks</span></span>

<span data-ttu-id="43a9e-115">Para generar un campo List-Unsubscribe encabezado, los clientes deben establecer estas propiedades en el valor deseado.</span><span class="sxs-lookup"><span data-stu-id="43a9e-115">To generate a List-Unsubscribe header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="43a9e-116">Los escritores MIME deben copiar el valor de estas propiedades en el List-Unsubscribe de encabezado.</span><span class="sxs-lookup"><span data-stu-id="43a9e-116">MIME writers must copy the value of these properties to the List-Unsubscribe header field.</span></span>
  
<span data-ttu-id="43a9e-117">Para establecer el valor de estas propiedades relacionadas con el servidor de lista, los clientes MIME deben escribir los campos de encabezado como se especifica en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="43a9e-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="43a9e-118">**Property**</span><span class="sxs-lookup"><span data-stu-id="43a9e-118">**Property**</span></span>|<span data-ttu-id="43a9e-119">**Nombre de campo de encabezado preferido**</span><span class="sxs-lookup"><span data-stu-id="43a9e-119">**Preferred header field name**</span></span>|<span data-ttu-id="43a9e-120">**Nombre de campo de encabezado alternativo**</span><span class="sxs-lookup"><span data-stu-id="43a9e-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="43a9e-121">**PR_LIST_UNSUBSCRIBE**</span><span class="sxs-lookup"><span data-stu-id="43a9e-121">**PR_LIST_UNSUBSCRIBE**</span></span> <br/> |<span data-ttu-id="43a9e-122">List-Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="43a9e-122">List-Unsubscribe</span></span>  <br/> |<span data-ttu-id="43a9e-123">X-List-Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="43a9e-123">X-List-Unsubscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="43a9e-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="43a9e-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="43a9e-125">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="43a9e-125">Protocol specifications</span></span>

<span data-ttu-id="43a9e-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43a9e-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43a9e-127">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="43a9e-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="43a9e-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43a9e-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43a9e-129">Convierte de convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="43a9e-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="43a9e-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="43a9e-130">Header files</span></span>

<span data-ttu-id="43a9e-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="43a9e-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="43a9e-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="43a9e-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="43a9e-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="43a9e-133">Mapitags.h</span></span>
  
> <span data-ttu-id="43a9e-134">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="43a9e-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43a9e-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="43a9e-135">See also</span></span>



[<span data-ttu-id="43a9e-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="43a9e-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="43a9e-137">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="43a9e-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="43a9e-138">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="43a9e-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="43a9e-139">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="43a9e-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

