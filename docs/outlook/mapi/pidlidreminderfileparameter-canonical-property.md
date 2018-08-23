---
title: Propiedad canónica PidLidReminderFileParameter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderFileParameter
api_type:
- COM
ms.assetid: 1009f0ea-6f35-484d-b04d-5b6e844c14dd
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 07653bea747e6e697cb1edb5669ae106c9e213fe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591481"
---
# <a name="pidlidreminderfileparameter-canonical-property"></a><span data-ttu-id="d39cc-103">Propiedad canónica PidLidReminderFileParameter</span><span class="sxs-lookup"><span data-stu-id="d39cc-103">PidLidReminderFileParameter Canonical Property</span></span>

  
  
<span data-ttu-id="d39cc-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d39cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d39cc-105">Especifica el nombre de archivo del archivo de sonido que se debe reproducir un cliente cuando el aviso para ese objeto se convierte en vencidas.</span><span class="sxs-lookup"><span data-stu-id="d39cc-105">Specifies the filename of the sound that a client should play when the reminder for that object becomes overdue.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d39cc-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d39cc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d39cc-107">dispidReminderFileParam</span><span class="sxs-lookup"><span data-stu-id="d39cc-107">dispidReminderFileParam</span></span>  <br/> |
|<span data-ttu-id="d39cc-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="d39cc-108">Property set:</span></span>  <br/> |<span data-ttu-id="d39cc-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="d39cc-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="d39cc-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="d39cc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d39cc-111">0x0000851F</span><span class="sxs-lookup"><span data-stu-id="d39cc-111">0x0000851F</span></span>  <br/> |
|<span data-ttu-id="d39cc-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d39cc-112">Data type:</span></span>  <br/> |<span data-ttu-id="d39cc-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d39cc-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d39cc-114">Área:</span><span class="sxs-lookup"><span data-stu-id="d39cc-114">Area:</span></span>  <br/> |<span data-ttu-id="d39cc-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="d39cc-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d39cc-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d39cc-116">Remarks</span></span>

<span data-ttu-id="d39cc-117">Si esta propiedad no está presente, el cliente puede utilizar un valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d39cc-117">If this property is not present, the client may use a default value.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d39cc-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d39cc-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d39cc-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d39cc-119">Protocol specifications</span></span>

<span data-ttu-id="d39cc-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d39cc-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d39cc-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d39cc-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d39cc-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d39cc-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d39cc-123">Especifica las propiedades y el modelo de interacción para correo electrónico y otros avisos de objeto.</span><span class="sxs-lookup"><span data-stu-id="d39cc-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d39cc-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d39cc-124">Header files</span></span>

<span data-ttu-id="d39cc-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d39cc-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d39cc-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d39cc-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d39cc-127">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="d39cc-127">See also</span></span>



[<span data-ttu-id="d39cc-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d39cc-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d39cc-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d39cc-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d39cc-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d39cc-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d39cc-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="d39cc-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

