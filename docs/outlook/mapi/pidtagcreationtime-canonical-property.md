---
title: Propiedad canónica PidTagCreationTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCreationTime
api_type:
- HeaderDef
ms.assetid: 13122af2-06c8-4342-983d-e38178743d8f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: de853c66f0ef4270f4c443881bfa163d4abfa3e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357900"
---
# <a name="pidtagcreationtime-canonical-property"></a><span data-ttu-id="795a7-103">Propiedad canónica PidTagCreationTime</span><span class="sxs-lookup"><span data-stu-id="795a7-103">PidTagCreationTime Canonical Property</span></span>

  
  
<span data-ttu-id="795a7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="795a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="795a7-105">Contiene la fecha y hora de creación de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="795a7-105">Contains the creation date and time of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="795a7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="795a7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="795a7-107">PR_CREATION_TIME</span><span class="sxs-lookup"><span data-stu-id="795a7-107">PR_CREATION_TIME</span></span>  <br/> |
|<span data-ttu-id="795a7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="795a7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="795a7-109">0x3007</span><span class="sxs-lookup"><span data-stu-id="795a7-109">0x3007</span></span>  <br/> |
|<span data-ttu-id="795a7-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="795a7-110">Data type:</span></span>  <br/> |<span data-ttu-id="795a7-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="795a7-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="795a7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="795a7-112">Area:</span></span>  <br/> |<span data-ttu-id="795a7-113">Hora del mensaje</span><span class="sxs-lookup"><span data-stu-id="795a7-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="795a7-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="795a7-114">Remarks</span></span>

<span data-ttu-id="795a7-115">Un almacén de mensajes establece esta propiedad para cada mensaje que crea.</span><span class="sxs-lookup"><span data-stu-id="795a7-115">A message store sets this property for each message that it creates.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="795a7-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="795a7-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="795a7-117">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="795a7-117">Protocol specifications</span></span>

<span data-ttu-id="795a7-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="795a7-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="795a7-119">Controla objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="795a7-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="795a7-120">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="795a7-120">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="795a7-121">Especifica las propiedades y las operaciones de listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="795a7-121">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="795a7-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="795a7-122">Header files</span></span>

<span data-ttu-id="795a7-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="795a7-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="795a7-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="795a7-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="795a7-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="795a7-125">Mapitags.h</span></span>
  
> <span data-ttu-id="795a7-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="795a7-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="795a7-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="795a7-127">See also</span></span>



[<span data-ttu-id="795a7-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="795a7-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="795a7-129">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="795a7-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="795a7-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="795a7-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="795a7-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="795a7-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

