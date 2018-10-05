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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395395"
---
# <a name="pidtagcreationtime-canonical-property"></a><span data-ttu-id="7b563-103">Propiedad canónica PidTagCreationTime</span><span class="sxs-lookup"><span data-stu-id="7b563-103">PidTagCreationTime Canonical Property</span></span>

  
  
<span data-ttu-id="7b563-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b563-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b563-105">Contiene la fecha de creación y la hora de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="7b563-105">Contains the creation date and time of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b563-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="7b563-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7b563-107">PR_CREATION_TIME</span><span class="sxs-lookup"><span data-stu-id="7b563-107">PR_CREATION_TIME</span></span>  <br/> |
|<span data-ttu-id="7b563-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7b563-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7b563-109">0x3007</span><span class="sxs-lookup"><span data-stu-id="7b563-109">0x3007</span></span>  <br/> |
|<span data-ttu-id="7b563-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="7b563-110">Data type:</span></span>  <br/> |<span data-ttu-id="7b563-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="7b563-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="7b563-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7b563-112">Area:</span></span>  <br/> |<span data-ttu-id="7b563-113">Hora del mensaje</span><span class="sxs-lookup"><span data-stu-id="7b563-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b563-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7b563-114">Remarks</span></span>

<span data-ttu-id="7b563-115">Un almacén de mensajes establece esta propiedad para cada mensaje que crea.</span><span class="sxs-lookup"><span data-stu-id="7b563-115">A message store sets this property for each message that it creates.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7b563-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7b563-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7b563-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="7b563-117">Protocol specifications</span></span>

<span data-ttu-id="7b563-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b563-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b563-119">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="7b563-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="7b563-120">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b563-120">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b563-121">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="7b563-121">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7b563-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="7b563-122">Header files</span></span>

<span data-ttu-id="7b563-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7b563-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="7b563-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7b563-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="7b563-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7b563-125">Mapitags.h</span></span>
  
> <span data-ttu-id="7b563-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="7b563-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b563-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b563-127">See also</span></span>



[<span data-ttu-id="7b563-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7b563-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7b563-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="7b563-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7b563-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="7b563-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7b563-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="7b563-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

