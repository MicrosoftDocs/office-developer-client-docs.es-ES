---
title: Propiedad canónica PidTagMailPermission
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMailPermission
api_type:
- HeaderDef
ms.assetid: f8270ef2-56d4-4b47-bdda-a39c966bbcba
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fb0b66cbf0de1ac351bb2026a48e0154de779206
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571195"
---
# <a name="pidtagmailpermission-canonical-property"></a><span data-ttu-id="2d7dc-103">Propiedad canónica PidTagMailPermission</span><span class="sxs-lookup"><span data-stu-id="2d7dc-103">PidTagMailPermission Canonical Property</span></span>

  
  
<span data-ttu-id="2d7dc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d7dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d7dc-105">Contiene TRUE si el usuario de mensajería tiene permiso para enviar y recibir mensajes.</span><span class="sxs-lookup"><span data-stu-id="2d7dc-105">Contains TRUE if the messaging user is allowed to send and receive messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2d7dc-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2d7dc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2d7dc-107">PR_MAIL_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="2d7dc-107">PR_MAIL_PERMISSION</span></span>  <br/> |
|<span data-ttu-id="2d7dc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2d7dc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2d7dc-109">0x3A0E</span><span class="sxs-lookup"><span data-stu-id="2d7dc-109">0x3A0E</span></span>  <br/> |
|<span data-ttu-id="2d7dc-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2d7dc-110">Data type:</span></span>  <br/> |<span data-ttu-id="2d7dc-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="2d7dc-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="2d7dc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2d7dc-112">Area:</span></span>  <br/> |<span data-ttu-id="2d7dc-113">Address</span><span class="sxs-lookup"><span data-stu-id="2d7dc-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d7dc-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2d7dc-114">Remarks</span></span>

<span data-ttu-id="2d7dc-115">Si no se establece esta propiedad, MAPI la trata como si tuviera un valor TRUE.</span><span class="sxs-lookup"><span data-stu-id="2d7dc-115">If this property is not set, MAPI treats it as having a TRUE value.</span></span> 
  
<span data-ttu-id="2d7dc-116">Establezca esta propiedad en FALSE en un directorio corporativo donde algunas de las entradas no están habilitados para correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="2d7dc-116">Set this property to FALSE in a corporate directory where some of the entries are not email-enabled.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2d7dc-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2d7dc-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2d7dc-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2d7dc-118">Header files</span></span>

<span data-ttu-id="2d7dc-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2d7dc-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="2d7dc-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2d7dc-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="2d7dc-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2d7dc-121">Mapitags.h</span></span>
  
> <span data-ttu-id="2d7dc-122">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="2d7dc-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2d7dc-123">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="2d7dc-123">See also</span></span>



[<span data-ttu-id="2d7dc-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2d7dc-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2d7dc-125">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="2d7dc-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2d7dc-126">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2d7dc-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2d7dc-127">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="2d7dc-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

