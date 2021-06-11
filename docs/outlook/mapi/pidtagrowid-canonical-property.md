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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359538"
---
# <a name="pidtagrowid-canonical-property"></a><span data-ttu-id="26d10-103">Propiedad canónica PidTagRowid</span><span class="sxs-lookup"><span data-stu-id="26d10-103">PidTagRowid Canonical Property</span></span>

  
  
<span data-ttu-id="26d10-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26d10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26d10-105">Contiene un identificador único para un destinatario en una tabla de destinatarios o tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="26d10-105">Contains a unique identifier for a recipient in a recipient table or status table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="26d10-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="26d10-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="26d10-107">PR_ROWID</span><span class="sxs-lookup"><span data-stu-id="26d10-107">PR_ROWID</span></span>  <br/> |
|<span data-ttu-id="26d10-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="26d10-108">Identifier:</span></span>  <br/> |<span data-ttu-id="26d10-109">0x3000</span><span class="sxs-lookup"><span data-stu-id="26d10-109">0x3000</span></span>  <br/> |
|<span data-ttu-id="26d10-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="26d10-110">Data type:</span></span>  <br/> |<span data-ttu-id="26d10-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="26d10-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="26d10-112">Área:</span><span class="sxs-lookup"><span data-stu-id="26d10-112">Area:</span></span>  <br/> |<span data-ttu-id="26d10-113">MAPI común</span><span class="sxs-lookup"><span data-stu-id="26d10-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26d10-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="26d10-114">Remarks</span></span>

<span data-ttu-id="26d10-115">Esta propiedad es un valor temporal que solo es válido para la vida del objeto propietario de la tabla.</span><span class="sxs-lookup"><span data-stu-id="26d10-115">This property is a temporary value that is valid only for the life of the object that owns the table.</span></span> <span data-ttu-id="26d10-116">Aparece como una columna de la tabla, pero no se almacena.</span><span class="sxs-lookup"><span data-stu-id="26d10-116">It appears as a column of the table but is not stored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="26d10-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="26d10-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="26d10-118">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="26d10-118">Protocol specifications</span></span>

<span data-ttu-id="26d10-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="26d10-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="26d10-120">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="26d10-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="26d10-121">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="26d10-121">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="26d10-122">Controla el orden y el flujo de las transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="26d10-122">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="26d10-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="26d10-123">Header files</span></span>

<span data-ttu-id="26d10-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="26d10-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="26d10-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="26d10-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="26d10-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="26d10-126">Mapitags.h</span></span>
  
> <span data-ttu-id="26d10-127">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="26d10-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="26d10-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="26d10-128">See also</span></span>



[<span data-ttu-id="26d10-129">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="26d10-129">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="26d10-130">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="26d10-130">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)


[<span data-ttu-id="26d10-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="26d10-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="26d10-132">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="26d10-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="26d10-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="26d10-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="26d10-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="26d10-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

