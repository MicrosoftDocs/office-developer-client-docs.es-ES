---
title: Propiedad canónica PidTagRowid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRowid
api_type:
- COM
ms.assetid: 0fdcb55a-2971-4c7d-b61e-7ada2d19d0e6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: efa778f51ac047c911deb6a3c4d5d9e718dc33fb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565042"
---
# <a name="pidtagrowid-canonical-property"></a><span data-ttu-id="93133-103">Propiedad canónica PidTagRowid</span><span class="sxs-lookup"><span data-stu-id="93133-103">PidTagRowid Canonical Property</span></span>

  
  
<span data-ttu-id="93133-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93133-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93133-105">Contiene un identificador único para un destinatario de una tabla de destinatarios o la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="93133-105">Contains a unique identifier for a recipient in a recipient table or status table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="93133-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="93133-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="93133-107">PR_ROWID</span><span class="sxs-lookup"><span data-stu-id="93133-107">PR_ROWID</span></span>  <br/> |
|<span data-ttu-id="93133-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="93133-108">Identifier:</span></span>  <br/> |<span data-ttu-id="93133-109">0 x 3000</span><span class="sxs-lookup"><span data-stu-id="93133-109">0x3000</span></span>  <br/> |
|<span data-ttu-id="93133-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="93133-110">Data type:</span></span>  <br/> |<span data-ttu-id="93133-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="93133-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="93133-112">Área:</span><span class="sxs-lookup"><span data-stu-id="93133-112">Area:</span></span>  <br/> |<span data-ttu-id="93133-113">MAPI comunes</span><span class="sxs-lookup"><span data-stu-id="93133-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93133-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="93133-114">Remarks</span></span>

<span data-ttu-id="93133-115">Esta propiedad es un valor temporal que sólo es válido para la vida del objeto que es propietario de la tabla.</span><span class="sxs-lookup"><span data-stu-id="93133-115">This property is a temporary value that is valid only for the life of the object that owns the table.</span></span> <span data-ttu-id="93133-116">Aparece como una columna de la tabla pero no se almacena.</span><span class="sxs-lookup"><span data-stu-id="93133-116">It appears as a column of the table but is not stored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="93133-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="93133-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="93133-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="93133-118">Protocol specifications</span></span>

<span data-ttu-id="93133-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93133-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93133-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="93133-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="93133-121">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93133-121">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93133-122">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="93133-122">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="93133-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="93133-123">Header files</span></span>

<span data-ttu-id="93133-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="93133-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="93133-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="93133-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="93133-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="93133-126">Mapitags.h</span></span>
  
> <span data-ttu-id="93133-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="93133-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93133-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="93133-128">See also</span></span>



[<span data-ttu-id="93133-129">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="93133-129">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="93133-130">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="93133-130">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)


[<span data-ttu-id="93133-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="93133-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="93133-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="93133-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="93133-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="93133-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="93133-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="93133-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

