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
ms.openlocfilehash: 86ef98ac7b4084de3a96210298fe0d5509d12103
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818576"
---
# <a name="pidlidautoprocessstate-canonical-property"></a><span data-ttu-id="e7947-103">Propiedad canónica PidLidAutoProcessState</span><span class="sxs-lookup"><span data-stu-id="e7947-103">PidLidAutoProcessState Canonical Property</span></span>

  
  
<span data-ttu-id="e7947-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e7947-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e7947-105">Especifica las opciones que se usan en el procesamiento automático de los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e7947-105">Specifies the options that are used in automatic processing of email messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e7947-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e7947-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e7947-107">dispidSniffState</span><span class="sxs-lookup"><span data-stu-id="e7947-107">dispidSniffState</span></span>  <br/> |
|<span data-ttu-id="e7947-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="e7947-108">Property set:</span></span>  <br/> |<span data-ttu-id="e7947-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="e7947-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="e7947-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="e7947-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e7947-111">0x0000851A</span><span class="sxs-lookup"><span data-stu-id="e7947-111">0x0000851A</span></span>  <br/> |
|<span data-ttu-id="e7947-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e7947-112">Data type:</span></span>  <br/> |<span data-ttu-id="e7947-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e7947-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e7947-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e7947-114">Area:</span></span>  <br/> |<span data-ttu-id="e7947-115">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="e7947-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7947-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e7947-116">Remarks</span></span>

<span data-ttu-id="e7947-117">La propiedad puede estar ausente, en cuyo caso se utiliza el valor predeterminado de "0 x 00000000".</span><span class="sxs-lookup"><span data-stu-id="e7947-117">The property may be absent, in which case the default value of "0x00000000" is used.</span></span> <span data-ttu-id="e7947-118">Si se establece, esta propiedad debe establecerse en uno de los valores en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e7947-118">If set, this property must be set to one of the values in the following table.</span></span>
  
|<span data-ttu-id="e7947-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e7947-119">**Value**</span></span>|<span data-ttu-id="e7947-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e7947-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e7947-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e7947-121">0x00000000</span></span>  <br/> |<span data-ttu-id="e7947-122">No se debe procesar automáticamente el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e7947-122">Do not automatically process the message.</span></span>  <br/> |
|<span data-ttu-id="e7947-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e7947-123">0x00000001</span></span>  <br/> |<span data-ttu-id="e7947-124">Procesar el mensaje automáticamente o cuando se abre el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e7947-124">Process the message automatically or when the message is opened.</span></span>  <br/> |
|<span data-ttu-id="e7947-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e7947-125">0x00000002</span></span>  <br/> |<span data-ttu-id="e7947-126">Procesar el mensaje sólo cuando se abre el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e7947-126">Process the message only when the message is opened.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e7947-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e7947-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e7947-128">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e7947-128">Protocol specifications</span></span>

<span data-ttu-id="e7947-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7947-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7947-130">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e7947-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e7947-131">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7947-131">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7947-132">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e7947-132">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e7947-133">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e7947-133">Header files</span></span>

<span data-ttu-id="e7947-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e7947-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="e7947-135">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e7947-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e7947-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7947-136">See also</span></span>



[<span data-ttu-id="e7947-137">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e7947-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e7947-138">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e7947-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e7947-139">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e7947-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e7947-140">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="e7947-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

