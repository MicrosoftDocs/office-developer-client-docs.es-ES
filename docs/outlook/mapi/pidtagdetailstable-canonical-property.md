---
title: Propiedad canónico PidTagDetailsTable
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: a267f9a9fb8d97256cf7a448b453d04db2118180
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819432"
---
# <a name="pidtagdetailstable-canonical-property"></a><span data-ttu-id="4c7ec-103">Propiedad canónico PidTagDetailsTable</span><span class="sxs-lookup"><span data-stu-id="4c7ec-103">PidTagDetailsTable Canonical Property</span></span>

  
  
<span data-ttu-id="4c7ec-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4c7ec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4c7ec-105">Contiene un objeto de la tabla de presentación incrustada.</span><span class="sxs-lookup"><span data-stu-id="4c7ec-105">Contains an embedded display table object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4c7ec-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4c7ec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4c7ec-107">PR_DETAILS_TABLE</span><span class="sxs-lookup"><span data-stu-id="4c7ec-107">PR_DETAILS_TABLE</span></span>  <br/> |
|<span data-ttu-id="4c7ec-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4c7ec-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4c7ec-109">0x3605</span><span class="sxs-lookup"><span data-stu-id="4c7ec-109">0x3605</span></span>  <br/> |
|<span data-ttu-id="4c7ec-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4c7ec-110">Data type:</span></span>  <br/> |<span data-ttu-id="4c7ec-111">PT OBJECT</span><span class="sxs-lookup"><span data-stu-id="4c7ec-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="4c7ec-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4c7ec-112">Area:</span></span>  <br/> |<span data-ttu-id="4c7ec-113">Contenedor MAPI</span><span class="sxs-lookup"><span data-stu-id="4c7ec-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c7ec-114">Notas</span><span class="sxs-lookup"><span data-stu-id="4c7ec-114">Remarks</span></span>

<span data-ttu-id="4c7ec-115">Pasa esta propiedad para el método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) para el objeto devuelve una interfaz [IMAPITable](imapitableiunknown.md) que permite la creación de la tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="4c7ec-115">Passing this property to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method for the object returns an [IMAPITable](imapitableiunknown.md) interface that allows creation of the display table.</span></span> <span data-ttu-id="4c7ec-116">MAPI utiliza esta tabla para mostrar las hojas de propiedades para un objeto de la libreta de direcciones en respuesta a una llamada de [IAddrBook::Details](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="4c7ec-116">MAPI uses this table to display property sheets for an address book object in response to an [IAddrBook::Details](iaddrbook-details.md) call.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4c7ec-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4c7ec-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4c7ec-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4c7ec-118">Header files</span></span>

<span data-ttu-id="4c7ec-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4c7ec-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="4c7ec-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4c7ec-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="4c7ec-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4c7ec-121">Mapitags.h</span></span>
  
> <span data-ttu-id="4c7ec-122">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="4c7ec-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4c7ec-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="4c7ec-123">See also</span></span>



[<span data-ttu-id="4c7ec-124">Propiedad canónico PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="4c7ec-124">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="4c7ec-125">Propiedad canónico PidTagSearch</span><span class="sxs-lookup"><span data-stu-id="4c7ec-125">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)


[<span data-ttu-id="4c7ec-126">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4c7ec-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4c7ec-127">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="4c7ec-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4c7ec-128">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="4c7ec-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4c7ec-129">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="4c7ec-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

