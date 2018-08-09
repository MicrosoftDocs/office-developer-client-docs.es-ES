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
ms.openlocfilehash: e8d0e79e01040c1cc3d46e73a7e6a456a915a67f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820117"
---
# <a name="pidtagrowid-canonical-property"></a><span data-ttu-id="0e7bf-103">Propiedad canónica PidTagRowid</span><span class="sxs-lookup"><span data-stu-id="0e7bf-103">PidTagRowid Canonical Property</span></span>

  
  
<span data-ttu-id="0e7bf-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0e7bf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0e7bf-105">Contiene un identificador único para un destinatario de una tabla de destinatarios o la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="0e7bf-105">Contains a unique identifier for a recipient in a recipient table or status table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0e7bf-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="0e7bf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0e7bf-107">PR_ROWID</span><span class="sxs-lookup"><span data-stu-id="0e7bf-107">PR_ROWID</span></span>  <br/> |
|<span data-ttu-id="0e7bf-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0e7bf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0e7bf-109">0 x 3000</span><span class="sxs-lookup"><span data-stu-id="0e7bf-109">0x3000</span></span>  <br/> |
|<span data-ttu-id="0e7bf-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="0e7bf-110">Data type:</span></span>  <br/> |<span data-ttu-id="0e7bf-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0e7bf-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0e7bf-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0e7bf-112">Area:</span></span>  <br/> |<span data-ttu-id="0e7bf-113">MAPI comunes</span><span class="sxs-lookup"><span data-stu-id="0e7bf-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e7bf-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0e7bf-114">Remarks</span></span>

<span data-ttu-id="0e7bf-115">Esta propiedad es un valor temporal que sólo es válido para la vida del objeto que es propietario de la tabla.</span><span class="sxs-lookup"><span data-stu-id="0e7bf-115">This property is a temporary value that is valid only for the life of the object that owns the table.</span></span> <span data-ttu-id="0e7bf-116">Aparece como una columna de la tabla pero no se almacena.</span><span class="sxs-lookup"><span data-stu-id="0e7bf-116">It appears as a column of the table but is not stored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0e7bf-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e7bf-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0e7bf-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="0e7bf-118">Protocol specifications</span></span>

<span data-ttu-id="0e7bf-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e7bf-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e7bf-120">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="0e7bf-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0e7bf-121">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e7bf-121">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e7bf-122">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="0e7bf-122">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0e7bf-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="0e7bf-123">Header files</span></span>

<span data-ttu-id="0e7bf-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0e7bf-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="0e7bf-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0e7bf-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="0e7bf-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0e7bf-126">Mapitags.h</span></span>
  
> <span data-ttu-id="0e7bf-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="0e7bf-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0e7bf-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e7bf-128">See also</span></span>



[<span data-ttu-id="0e7bf-129">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="0e7bf-129">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="0e7bf-130">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="0e7bf-130">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)


[<span data-ttu-id="0e7bf-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0e7bf-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0e7bf-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="0e7bf-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0e7bf-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="0e7bf-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0e7bf-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="0e7bf-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

