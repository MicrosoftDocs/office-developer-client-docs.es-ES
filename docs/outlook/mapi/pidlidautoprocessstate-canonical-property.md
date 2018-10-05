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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397621"
---
# <a name="pidlidautoprocessstate-canonical-property"></a><span data-ttu-id="81e11-103">Propiedad canónica PidLidAutoProcessState</span><span class="sxs-lookup"><span data-stu-id="81e11-103">PidLidAutoProcessState Canonical Property</span></span>

  
  
<span data-ttu-id="81e11-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81e11-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81e11-105">Especifica las opciones que se usan en el procesamiento automático de los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="81e11-105">Specifies the options that are used in automatic processing of email messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="81e11-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="81e11-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="81e11-107">dispidSniffState</span><span class="sxs-lookup"><span data-stu-id="81e11-107">dispidSniffState</span></span>  <br/> |
|<span data-ttu-id="81e11-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="81e11-108">Property set:</span></span>  <br/> |<span data-ttu-id="81e11-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="81e11-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="81e11-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="81e11-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="81e11-111">0x0000851A</span><span class="sxs-lookup"><span data-stu-id="81e11-111">0x0000851A</span></span>  <br/> |
|<span data-ttu-id="81e11-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="81e11-112">Data type:</span></span>  <br/> |<span data-ttu-id="81e11-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="81e11-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="81e11-114">Área:</span><span class="sxs-lookup"><span data-stu-id="81e11-114">Area:</span></span>  <br/> |<span data-ttu-id="81e11-115">General de mensajería</span><span class="sxs-lookup"><span data-stu-id="81e11-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81e11-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="81e11-116">Remarks</span></span>

<span data-ttu-id="81e11-117">La propiedad puede estar ausente, en cuyo caso se utiliza el valor predeterminado de "0 x 00000000".</span><span class="sxs-lookup"><span data-stu-id="81e11-117">The property may be absent, in which case the default value of "0x00000000" is used.</span></span> <span data-ttu-id="81e11-118">Si se establece, esta propiedad debe establecerse en uno de los valores en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="81e11-118">If set, this property must be set to one of the values in the following table.</span></span>
  
|<span data-ttu-id="81e11-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="81e11-119">**Value**</span></span>|<span data-ttu-id="81e11-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="81e11-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="81e11-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81e11-121">0x00000000</span></span>  <br/> |<span data-ttu-id="81e11-122">No se debe procesar automáticamente el mensaje.</span><span class="sxs-lookup"><span data-stu-id="81e11-122">Do not automatically process the message.</span></span>  <br/> |
|<span data-ttu-id="81e11-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="81e11-123">0x00000001</span></span>  <br/> |<span data-ttu-id="81e11-124">Procesar el mensaje automáticamente o cuando se abre el mensaje.</span><span class="sxs-lookup"><span data-stu-id="81e11-124">Process the message automatically or when the message is opened.</span></span>  <br/> |
|<span data-ttu-id="81e11-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="81e11-125">0x00000002</span></span>  <br/> |<span data-ttu-id="81e11-126">Procesar el mensaje sólo cuando se abre el mensaje.</span><span class="sxs-lookup"><span data-stu-id="81e11-126">Process the message only when the message is opened.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="81e11-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="81e11-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="81e11-128">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="81e11-128">Protocol specifications</span></span>

<span data-ttu-id="81e11-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81e11-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81e11-130">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="81e11-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="81e11-131">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81e11-131">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81e11-132">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="81e11-132">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="81e11-133">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="81e11-133">Header files</span></span>

<span data-ttu-id="81e11-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="81e11-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="81e11-135">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="81e11-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="81e11-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="81e11-136">See also</span></span>



[<span data-ttu-id="81e11-137">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="81e11-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="81e11-138">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="81e11-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="81e11-139">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="81e11-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="81e11-140">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="81e11-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

