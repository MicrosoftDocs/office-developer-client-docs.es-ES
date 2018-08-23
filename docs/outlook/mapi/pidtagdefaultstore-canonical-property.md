---
title: Propiedad canónica PidTagDefaultStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultStore
api_type:
- HeaderDef
ms.assetid: 6314d91c-4948-4fd1-bacc-932d4bb2c22f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d544c741685d401aaf36fe19be50ab402c9e5604
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592685"
---
# <a name="pidtagdefaultstore-canonical-property"></a><span data-ttu-id="fd575-103">Propiedad canónica PidTagDefaultStore</span><span class="sxs-lookup"><span data-stu-id="fd575-103">PidTagDefaultStore Canonical Property</span></span>

  
  
<span data-ttu-id="fd575-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd575-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd575-105">Contiene TRUE si un almacén de mensajes es el almacén de mensajes de forma predeterminada en la tabla de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="fd575-105">Contains TRUE if a message store is the default message store in the message store table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fd575-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fd575-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fd575-107">PR_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="fd575-107">PR_DEFAULT_STORE</span></span>  <br/> |
|<span data-ttu-id="fd575-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fd575-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fd575-109">0x3400</span><span class="sxs-lookup"><span data-stu-id="fd575-109">0x3400</span></span>  <br/> |
|<span data-ttu-id="fd575-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fd575-110">Data type:</span></span>  <br/> |<span data-ttu-id="fd575-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="fd575-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="fd575-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fd575-112">Area:</span></span>  <br/> |<span data-ttu-id="fd575-113">Almacén de mensajes MAPI</span><span class="sxs-lookup"><span data-stu-id="fd575-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd575-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fd575-114">Remarks</span></span>

<span data-ttu-id="fd575-115">Esta propiedad aparece como una columna en la tabla de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="fd575-115">This property appears as a column in the message store table.</span></span> <span data-ttu-id="fd575-116">El valor se basa en **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="fd575-116">The value is based on **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fd575-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fd575-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fd575-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="fd575-118">Protocol specifications</span></span>

<span data-ttu-id="fd575-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd575-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd575-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="fd575-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fd575-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fd575-121">Header files</span></span>

<span data-ttu-id="fd575-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fd575-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="fd575-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fd575-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="fd575-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fd575-124">Mapitags.h</span></span>
  
> <span data-ttu-id="fd575-125">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="fd575-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fd575-126">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="fd575-126">See also</span></span>



[<span data-ttu-id="fd575-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fd575-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fd575-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="fd575-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fd575-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="fd575-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fd575-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="fd575-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

