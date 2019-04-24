---
title: Propiedad canónica PidLidAutoProcessState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAutoProcessState
api_type:
- COM
ms.assetid: 9e724af6-5b56-4eb3-a94c-1015ebce197c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0918c15d87219c1ee20b177ae21e718e0289cf04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342066"
---
# <a name="pidlidautoprocessstate-canonical-property"></a><span data-ttu-id="06f9b-103">Propiedad canónica PidLidAutoProcessState</span><span class="sxs-lookup"><span data-stu-id="06f9b-103">PidLidAutoProcessState Canonical Property</span></span>

  
  
<span data-ttu-id="06f9b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06f9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06f9b-105">Especifica las opciones que se usan en el procesamiento automático de mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="06f9b-105">Specifies the options that are used in automatic processing of email messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="06f9b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="06f9b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="06f9b-107">dispidSniffState</span><span class="sxs-lookup"><span data-stu-id="06f9b-107">dispidSniffState</span></span>  <br/> |
|<span data-ttu-id="06f9b-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="06f9b-108">Property set:</span></span>  <br/> |<span data-ttu-id="06f9b-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="06f9b-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="06f9b-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="06f9b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="06f9b-111">0x0000851A</span><span class="sxs-lookup"><span data-stu-id="06f9b-111">0x0000851A</span></span>  <br/> |
|<span data-ttu-id="06f9b-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="06f9b-112">Data type:</span></span>  <br/> |<span data-ttu-id="06f9b-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="06f9b-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="06f9b-114">Área:</span><span class="sxs-lookup"><span data-stu-id="06f9b-114">Area:</span></span>  <br/> |<span data-ttu-id="06f9b-115">Mensajes generales</span><span class="sxs-lookup"><span data-stu-id="06f9b-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06f9b-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="06f9b-116">Remarks</span></span>

<span data-ttu-id="06f9b-117">Es posible que la propiedad no esté presente, en cuyo caso se utiliza el valor predeterminado de "0x00000000".</span><span class="sxs-lookup"><span data-stu-id="06f9b-117">The property may be absent, in which case the default value of "0x00000000" is used.</span></span> <span data-ttu-id="06f9b-118">Si se establece, esta propiedad debe establecerse en uno de los valores de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="06f9b-118">If set, this property must be set to one of the values in the following table.</span></span>
  
|<span data-ttu-id="06f9b-119">**Value**</span><span class="sxs-lookup"><span data-stu-id="06f9b-119">**Value**</span></span>|<span data-ttu-id="06f9b-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="06f9b-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="06f9b-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06f9b-121">0x00000000</span></span>  <br/> |<span data-ttu-id="06f9b-122">No procesar automáticamente el mensaje.</span><span class="sxs-lookup"><span data-stu-id="06f9b-122">Do not automatically process the message.</span></span>  <br/> |
|<span data-ttu-id="06f9b-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="06f9b-123">0x00000001</span></span>  <br/> |<span data-ttu-id="06f9b-124">Procesar el mensaje automáticamente o cuando se abre el mensaje.</span><span class="sxs-lookup"><span data-stu-id="06f9b-124">Process the message automatically or when the message is opened.</span></span>  <br/> |
|<span data-ttu-id="06f9b-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="06f9b-125">0x00000002</span></span>  <br/> |<span data-ttu-id="06f9b-126">Procesar el mensaje solo cuando se abre el mensaje.</span><span class="sxs-lookup"><span data-stu-id="06f9b-126">Process the message only when the message is opened.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="06f9b-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="06f9b-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="06f9b-128">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="06f9b-128">Protocol specifications</span></span>

<span data-ttu-id="06f9b-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06f9b-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06f9b-130">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="06f9b-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="06f9b-131">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="06f9b-131">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="06f9b-132">Especifica las propiedades y operaciones que se admiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="06f9b-132">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="06f9b-133">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="06f9b-133">Header files</span></span>

<span data-ttu-id="06f9b-134">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="06f9b-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="06f9b-135">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="06f9b-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="06f9b-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="06f9b-136">See also</span></span>



[<span data-ttu-id="06f9b-137">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="06f9b-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="06f9b-138">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="06f9b-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="06f9b-139">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="06f9b-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="06f9b-140">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="06f9b-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

