---
title: Propiedad canónica PidTagResolveMethod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResolveMethod
api_type:
- COM
ms.assetid: 30d23c19-e0da-4511-9361-761153259216
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 14bb31ae9aebbb6441948b5756b426508107c9f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331405"
---
# <a name="pidtagresolvemethod-canonical-property"></a><span data-ttu-id="f85e8-103">Propiedad canónica PidTagResolveMethod</span><span class="sxs-lookup"><span data-stu-id="f85e8-103">PidTagResolveMethod Canonical Property</span></span>

  
  
<span data-ttu-id="f85e8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f85e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f85e8-105">Contiene el valor de resolución de conflictos de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="f85e8-105">Contains a folder's conflict resolution value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f85e8-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f85e8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f85e8-107">PR_RESOLVE_METHOD</span><span class="sxs-lookup"><span data-stu-id="f85e8-107">PR_RESOLVE_METHOD</span></span>  <br/> |
|<span data-ttu-id="f85e8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f85e8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f85e8-109">0x3FE7</span><span class="sxs-lookup"><span data-stu-id="f85e8-109">0x3FE7</span></span>  <br/> |
|<span data-ttu-id="f85e8-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f85e8-110">Data type:</span></span>  <br/> |<span data-ttu-id="f85e8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f85e8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f85e8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f85e8-112">Area:</span></span>  <br/> |<span data-ttu-id="f85e8-113">Estado de MAPI</span><span class="sxs-lookup"><span data-stu-id="f85e8-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f85e8-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f85e8-114">Remarks</span></span>

<span data-ttu-id="f85e8-115">Esta propiedad de la carpeta que contiene el mensaje de resolución de conflictos indicará cómo se debe resolver el conflicto.</span><span class="sxs-lookup"><span data-stu-id="f85e8-115">This property on the folder containing the conflict resolution message will indicate how to resolve the conflict.</span></span> <span data-ttu-id="f85e8-116">Esta propiedad no es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="f85e8-116">This property is not required.</span></span> <span data-ttu-id="f85e8-117">Sin embargo, si se establece, las marcas que no sean las siguientes no deben estar presentes:</span><span class="sxs-lookup"><span data-stu-id="f85e8-117">However, if it is set, flags other than the following must not be present:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f85e8-118">RESOLVE_METHOD_DEFAULT (0x00000000)</span><span class="sxs-lookup"><span data-stu-id="f85e8-118">RESOLVE_METHOD_DEFAULT (0x00000000)</span></span>  <br/> |<span data-ttu-id="f85e8-119">Debe generarse el mensaje de resolución de conflictos.</span><span class="sxs-lookup"><span data-stu-id="f85e8-119">Conflict resolve message should be generated.</span></span>  <br/> |
|<span data-ttu-id="f85e8-120">RESOLVE_METHOD_LAST_WRITER_WINS (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="f85e8-120">RESOLVE_METHOD_LAST_WRITER_WINS (0x00000001)</span></span>  <br/> |<span data-ttu-id="f85e8-121">Sobrescribir el mensaje de destino con los cambios actuales que se están aplicando.</span><span class="sxs-lookup"><span data-stu-id="f85e8-121">Overwrite target message with current changes being applied.</span></span>  <br/> |
|<span data-ttu-id="f85e8-122">RESOLVE_NO_CONFLICT_NOTIFICATION (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="f85e8-122">RESOLVE_NO_CONFLICT_NOTIFICATION (0x00000002)</span></span>  <br/> |<span data-ttu-id="f85e8-123">No enviar mensaje de notificación de conflictos al generar un mensaje de conflictos de resolución en la carpeta pública.</span><span class="sxs-lookup"><span data-stu-id="f85e8-123">Do not send conflict notification message when generating conflict resolve message in public folder.</span></span>  <br/> |
   
<span data-ttu-id="f85e8-124">Un cliente o un servidor no debe generar un mensaje de resolución de conflictos para los mensajes asociados.</span><span class="sxs-lookup"><span data-stu-id="f85e8-124">A client or server must not generate a conflict resolve message for associated messages.</span></span> <span data-ttu-id="f85e8-125">Estos mensajes deben resolverse mediante la semántica **RESOLVE_METHOD_LAST_WRITER_WINS** .</span><span class="sxs-lookup"><span data-stu-id="f85e8-125">These messages must be resolved by using **RESOLVE_METHOD_LAST_WRITER_WINS** semantics.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f85e8-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f85e8-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f85e8-127">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f85e8-127">Protocol specifications</span></span>

<span data-ttu-id="f85e8-128">[[MS-OXCSYNC]](https://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f85e8-128">[[MS-OXCSYNC]](https://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f85e8-129">Controla los datos de objetos de mensajería que se sincronizan entre un servidor y un cliente.</span><span class="sxs-lookup"><span data-stu-id="f85e8-129">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="f85e8-130">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f85e8-130">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f85e8-131">Define las estructuras de datos básicas que se usan en las operaciones remotas.</span><span class="sxs-lookup"><span data-stu-id="f85e8-131">Defines the basic data structures that are used in remote operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f85e8-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f85e8-132">Header files</span></span>

<span data-ttu-id="f85e8-133">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f85e8-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="f85e8-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f85e8-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="f85e8-135">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f85e8-135">Mapitags.h</span></span>
  
> <span data-ttu-id="f85e8-136">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f85e8-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f85e8-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="f85e8-137">See also</span></span>



[<span data-ttu-id="f85e8-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f85e8-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f85e8-139">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="f85e8-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f85e8-140">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f85e8-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f85e8-141">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="f85e8-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

