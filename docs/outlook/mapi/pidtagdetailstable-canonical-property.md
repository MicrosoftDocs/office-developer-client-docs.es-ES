---
title: Propiedad canónica PidTagDetailsTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDetailsTable
api_type:
- HeaderDef
ms.assetid: 7a0ccad3-f497-4871-b733-771e6cb8ef6a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 74eae4a4ed742c3bb90496f5975ad7dac6ff798f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419257"
---
# <a name="pidtagdetailstable-canonical-property"></a><span data-ttu-id="55869-103">Propiedad canónica PidTagDetailsTable</span><span class="sxs-lookup"><span data-stu-id="55869-103">PidTagDetailsTable Canonical Property</span></span>

  
  
<span data-ttu-id="55869-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55869-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55869-105">Contiene un objeto de tabla para mostrar incrustado.</span><span class="sxs-lookup"><span data-stu-id="55869-105">Contains an embedded display table object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="55869-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="55869-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="55869-107">PR_DETAILS_TABLE</span><span class="sxs-lookup"><span data-stu-id="55869-107">PR_DETAILS_TABLE</span></span>  <br/> |
|<span data-ttu-id="55869-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="55869-108">Identifier:</span></span>  <br/> |<span data-ttu-id="55869-109">0x3605</span><span class="sxs-lookup"><span data-stu-id="55869-109">0x3605</span></span>  <br/> |
|<span data-ttu-id="55869-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="55869-110">Data type:</span></span>  <br/> |<span data-ttu-id="55869-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="55869-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="55869-112">Área:</span><span class="sxs-lookup"><span data-stu-id="55869-112">Area:</span></span>  <br/> |<span data-ttu-id="55869-113">Contenedor MAPI</span><span class="sxs-lookup"><span data-stu-id="55869-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55869-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="55869-114">Remarks</span></span>

<span data-ttu-id="55869-115">Pasar esta propiedad al [método IMAPIProp::OpenProperty](imapiprop-openproperty.md) para el objeto devuelve una interfaz [IMAPITable](imapitableiunknown.md) que permite la creación de la tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="55869-115">Passing this property to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the object returns an [IMAPITable](imapitableiunknown.md) interface that allows creation of the display table.</span></span> <span data-ttu-id="55869-116">MAPI usa esta tabla para mostrar hojas de propiedades para un objeto de libreta de direcciones en respuesta a una [llamada IAddrBook::D etails.](iaddrbook-details.md)</span><span class="sxs-lookup"><span data-stu-id="55869-116">MAPI uses this table to display property sheets for an address book object in response to an [IAddrBook::Details](iaddrbook-details.md) call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="55869-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="55869-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="55869-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="55869-118">Header files</span></span>

<span data-ttu-id="55869-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="55869-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="55869-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="55869-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="55869-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="55869-121">Mapitags.h</span></span>
  
> <span data-ttu-id="55869-122">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="55869-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="55869-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="55869-123">See also</span></span>



[<span data-ttu-id="55869-124">Propiedad canónica PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="55869-124">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="55869-125">Propiedad canónica PidTagSearch</span><span class="sxs-lookup"><span data-stu-id="55869-125">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)


[<span data-ttu-id="55869-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="55869-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="55869-127">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="55869-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="55869-128">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="55869-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="55869-129">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="55869-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

