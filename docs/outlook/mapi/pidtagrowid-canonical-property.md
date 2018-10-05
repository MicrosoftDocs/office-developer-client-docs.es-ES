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
ms.openlocfilehash: 8d58342e0460352bd9d260cb6e73de358cb2fc23
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387723"
---
# <a name="pidtagrowid-canonical-property"></a><span data-ttu-id="e28e6-103">Propiedad canónica PidTagRowid</span><span class="sxs-lookup"><span data-stu-id="e28e6-103">PidTagRowid Canonical Property</span></span>

  
  
<span data-ttu-id="e28e6-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e28e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e28e6-105">Contiene un identificador único para un destinatario de una tabla de destinatarios o la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="e28e6-105">Contains a unique identifier for a recipient in a recipient table or status table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e28e6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e28e6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e28e6-107">PR_ROWID</span><span class="sxs-lookup"><span data-stu-id="e28e6-107">PR_ROWID</span></span>  <br/> |
|<span data-ttu-id="e28e6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e28e6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e28e6-109">0 x 3000</span><span class="sxs-lookup"><span data-stu-id="e28e6-109">0x3000</span></span>  <br/> |
|<span data-ttu-id="e28e6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e28e6-110">Data type:</span></span>  <br/> |<span data-ttu-id="e28e6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e28e6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e28e6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e28e6-112">Area:</span></span>  <br/> |<span data-ttu-id="e28e6-113">MAPI comunes</span><span class="sxs-lookup"><span data-stu-id="e28e6-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e28e6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e28e6-114">Remarks</span></span>

<span data-ttu-id="e28e6-115">Esta propiedad es un valor temporal que sólo es válido para la vida del objeto que es propietario de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e28e6-115">This property is a temporary value that is valid only for the life of the object that owns the table.</span></span> <span data-ttu-id="e28e6-116">Aparece como una columna de la tabla pero no se almacena.</span><span class="sxs-lookup"><span data-stu-id="e28e6-116">It appears as a column of the table but is not stored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e28e6-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e28e6-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e28e6-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e28e6-118">Protocol specifications</span></span>

<span data-ttu-id="e28e6-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e28e6-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e28e6-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e28e6-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e28e6-121">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e28e6-121">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e28e6-122">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="e28e6-122">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e28e6-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e28e6-123">Header files</span></span>

<span data-ttu-id="e28e6-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e28e6-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="e28e6-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e28e6-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="e28e6-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e28e6-126">Mapitags.h</span></span>
  
> <span data-ttu-id="e28e6-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="e28e6-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e28e6-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e28e6-128">See also</span></span>



[<span data-ttu-id="e28e6-129">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="e28e6-129">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="e28e6-130">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="e28e6-130">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)


[<span data-ttu-id="e28e6-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e28e6-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e28e6-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e28e6-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e28e6-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e28e6-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e28e6-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="e28e6-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

