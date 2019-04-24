---
title: Propiedad canónica PidTagMessageSecurityLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSecurityLabel
api_type:
- HeaderDef
ms.assetid: aae41f1b-19bb-40c7-8564-0c87a5a4e47c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b6900cbacc2bea6c5519efdc4281ca98629b23bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355681"
---
# <a name="pidtagmessagesecuritylabel-canonical-property"></a><span data-ttu-id="1c863-103">Propiedad canónica PidTagMessageSecurityLabel</span><span class="sxs-lookup"><span data-stu-id="1c863-103">PidTagMessageSecurityLabel Canonical Property</span></span>

  
  
<span data-ttu-id="1c863-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c863-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c863-105">Contiene una etiqueta de seguridad para un mensaje.</span><span class="sxs-lookup"><span data-stu-id="1c863-105">Contains a security label for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1c863-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1c863-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1c863-107">PR_MESSAGE_SECURITY_LABEL</span><span class="sxs-lookup"><span data-stu-id="1c863-107">PR_MESSAGE_SECURITY_LABEL</span></span>  <br/> |
|<span data-ttu-id="1c863-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1c863-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1c863-109">0x001E</span><span class="sxs-lookup"><span data-stu-id="1c863-109">0x001E</span></span>  <br/> |
|<span data-ttu-id="1c863-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1c863-110">Data type:</span></span>  <br/> |<span data-ttu-id="1c863-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1c863-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1c863-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1c863-112">Area:</span></span>  <br/> |<span data-ttu-id="1c863-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="1c863-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c863-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1c863-114">Remarks</span></span>

<span data-ttu-id="1c863-115">Esta propiedad proporciona la base sobre la que la propiedad **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) protege un mensaje.</span><span class="sxs-lookup"><span data-stu-id="1c863-115">This property provides the basis on which the **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) property protects a message.</span></span> <span data-ttu-id="1c863-116">La asociación con el contenido del mensaje está garantizada por el token.</span><span class="sxs-lookup"><span data-stu-id="1c863-116">Its association with the message content is guaranteed by the token.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1c863-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1c863-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1c863-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1c863-118">Header files</span></span>

<span data-ttu-id="1c863-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1c863-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="1c863-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1c863-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="1c863-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="1c863-121">Mapitags.h</span></span>
  
> <span data-ttu-id="1c863-122">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="1c863-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1c863-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c863-123">See also</span></span>



[<span data-ttu-id="1c863-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1c863-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1c863-125">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="1c863-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1c863-126">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="1c863-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1c863-127">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="1c863-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

