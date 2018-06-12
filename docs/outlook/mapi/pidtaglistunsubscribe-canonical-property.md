---
title: Propiedad canónico PidTagListUnsubscribe
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 87f5c3fc8475f9795847e4680babb26682608a5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819701"
---
# <a name="pidtaglistunsubscribe-canonical-property"></a><span data-ttu-id="36af5-103">Propiedad canónico PidTagListUnsubscribe</span><span class="sxs-lookup"><span data-stu-id="36af5-103">PidTagListUnsubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="36af5-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="36af5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="36af5-105">Contiene el valor del campo de encabezado de un mensaje de extensiones multipropósito de correo Internet (MIME) cancelar su suscripción de lista.</span><span class="sxs-lookup"><span data-stu-id="36af5-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Unsubscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="36af5-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="36af5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="36af5-107">PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="36af5-107">PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="36af5-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="36af5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="36af5-109">0x1045</span><span class="sxs-lookup"><span data-stu-id="36af5-109">0x1045</span></span>  <br/> |
|<span data-ttu-id="36af5-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="36af5-110">Data type:</span></span>  <br/> |<span data-ttu-id="36af5-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="36af5-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="36af5-112">Área:</span><span class="sxs-lookup"><span data-stu-id="36af5-112">Area:</span></span>  <br/> |<span data-ttu-id="36af5-113">Varios</span><span class="sxs-lookup"><span data-stu-id="36af5-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="36af5-114">Notas</span><span class="sxs-lookup"><span data-stu-id="36af5-114">Remarks</span></span>

<span data-ttu-id="36af5-115">Para generar un campo de encabezado cancelar su suscripción de lista, los clientes deben establecer estas propiedades en el valor deseado.</span><span class="sxs-lookup"><span data-stu-id="36af5-115">To generate a List-Unsubscribe header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="36af5-116">Los escritores MIME deben copiar el valor de estas propiedades en el campo de encabezado de cancelar su suscripción de lista.</span><span class="sxs-lookup"><span data-stu-id="36af5-116">MIME writers must copy the value of these properties to the List-Unsubscribe header field.</span></span>
  
<span data-ttu-id="36af5-117">Para establecer el valor de estas propiedades relacionadas con el servidor de lista, los clientes MIME deben escribir los campos de encabezado tal como se especifica en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="36af5-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="36af5-118">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="36af5-118">**Property**</span></span>|<span data-ttu-id="36af5-119">**Nombre de campo de encabezado preferido**</span><span class="sxs-lookup"><span data-stu-id="36af5-119">**Preferred header field name**</span></span>|<span data-ttu-id="36af5-120">**Nombre de campo de encabezado alternativo**</span><span class="sxs-lookup"><span data-stu-id="36af5-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="36af5-121">**PR_LIST_UNSUBSCRIBE**</span><span class="sxs-lookup"><span data-stu-id="36af5-121">**PR_LIST_UNSUBSCRIBE**</span></span> <br/> |<span data-ttu-id="36af5-122">Cancelar su suscripción de lista</span><span class="sxs-lookup"><span data-stu-id="36af5-122">List-Unsubscribe</span></span>  <br/> |<span data-ttu-id="36af5-123">Anular la suscripción X-lista</span><span class="sxs-lookup"><span data-stu-id="36af5-123">X-List-Unsubscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="36af5-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="36af5-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="36af5-125">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="36af5-125">Protocol specifications</span></span>

<span data-ttu-id="36af5-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="36af5-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="36af5-127">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="36af5-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="36af5-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="36af5-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="36af5-129">Convierte de las convenciones de correo electrónico estándar de Internet a objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="36af5-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="36af5-130">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="36af5-130">Header files</span></span>

<span data-ttu-id="36af5-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="36af5-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="36af5-132">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="36af5-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="36af5-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="36af5-133">Mapitags.h</span></span>
  
> <span data-ttu-id="36af5-134">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="36af5-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="36af5-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="36af5-135">See also</span></span>



[<span data-ttu-id="36af5-136">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="36af5-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="36af5-137">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="36af5-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="36af5-138">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="36af5-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="36af5-139">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="36af5-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

