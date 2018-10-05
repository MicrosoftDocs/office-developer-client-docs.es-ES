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
ms.openlocfilehash: 0cbcc8185f6f46a1bfceb2dd6d0aaf9c5d7cab2e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385168"
---
# <a name="pidtagdefaultstore-canonical-property"></a><span data-ttu-id="12e9b-103">Propiedad canónica PidTagDefaultStore</span><span class="sxs-lookup"><span data-stu-id="12e9b-103">PidTagDefaultStore Canonical Property</span></span>

  
  
<span data-ttu-id="12e9b-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12e9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12e9b-105">Contiene TRUE si un almacén de mensajes es el almacén de mensajes de forma predeterminada en la tabla de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="12e9b-105">Contains TRUE if a message store is the default message store in the message store table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="12e9b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="12e9b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="12e9b-107">PR_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="12e9b-107">PR_DEFAULT_STORE</span></span>  <br/> |
|<span data-ttu-id="12e9b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="12e9b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="12e9b-109">0x3400</span><span class="sxs-lookup"><span data-stu-id="12e9b-109">0x3400</span></span>  <br/> |
|<span data-ttu-id="12e9b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="12e9b-110">Data type:</span></span>  <br/> |<span data-ttu-id="12e9b-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="12e9b-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="12e9b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="12e9b-112">Area:</span></span>  <br/> |<span data-ttu-id="12e9b-113">Almacén de mensajes MAPI</span><span class="sxs-lookup"><span data-stu-id="12e9b-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12e9b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="12e9b-114">Remarks</span></span>

<span data-ttu-id="12e9b-115">Esta propiedad aparece como una columna en la tabla de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="12e9b-115">This property appears as a column in the message store table.</span></span> <span data-ttu-id="12e9b-116">El valor se basa en **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="12e9b-116">The value is based on **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="12e9b-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="12e9b-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="12e9b-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="12e9b-118">Protocol specifications</span></span>

<span data-ttu-id="12e9b-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12e9b-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12e9b-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="12e9b-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="12e9b-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="12e9b-121">Header files</span></span>

<span data-ttu-id="12e9b-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="12e9b-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="12e9b-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="12e9b-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="12e9b-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="12e9b-124">Mapitags.h</span></span>
  
> <span data-ttu-id="12e9b-125">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="12e9b-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="12e9b-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="12e9b-126">See also</span></span>



[<span data-ttu-id="12e9b-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="12e9b-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="12e9b-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="12e9b-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="12e9b-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="12e9b-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="12e9b-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="12e9b-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

