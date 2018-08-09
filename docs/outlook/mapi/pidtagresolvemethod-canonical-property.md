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
ms.openlocfilehash: 7f55b85e21f007be7c1b9d42d42473e3a8d2becb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820115"
---
# <a name="pidtagresolvemethod-canonical-property"></a><span data-ttu-id="5895a-103">Propiedad canónica PidTagResolveMethod</span><span class="sxs-lookup"><span data-stu-id="5895a-103">PidTagResolveMethod Canonical Property</span></span>

  
  
<span data-ttu-id="5895a-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5895a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5895a-105">Contiene el valor de resolución de conflicto de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="5895a-105">Contains a folder's conflict resolution value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5895a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5895a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5895a-107">PR_RESOLVE_METHOD</span><span class="sxs-lookup"><span data-stu-id="5895a-107">PR_RESOLVE_METHOD</span></span>  <br/> |
|<span data-ttu-id="5895a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5895a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5895a-109">0x3FE7</span><span class="sxs-lookup"><span data-stu-id="5895a-109">0x3FE7</span></span>  <br/> |
|<span data-ttu-id="5895a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5895a-110">Data type:</span></span>  <br/> |<span data-ttu-id="5895a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5895a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5895a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5895a-112">Area:</span></span>  <br/> |<span data-ttu-id="5895a-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="5895a-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5895a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5895a-114">Remarks</span></span>

<span data-ttu-id="5895a-115">Esta propiedad en la carpeta que contiene el mensaje de resolución de conflicto indicará cómo resolver el conflicto.</span><span class="sxs-lookup"><span data-stu-id="5895a-115">This property on the folder containing the conflict resolution message will indicate how to resolve the conflict.</span></span> <span data-ttu-id="5895a-116">Esta propiedad no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="5895a-116">This property is not required.</span></span> <span data-ttu-id="5895a-117">Sin embargo, si se establece, marcas que no sea el siguiente no deben estar presentes:</span><span class="sxs-lookup"><span data-stu-id="5895a-117">However, if it is set, flags other than the following must not be present:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5895a-118">RESOLVE_METHOD_DEFAULT (0 X 00000000)</span><span class="sxs-lookup"><span data-stu-id="5895a-118">RESOLVE_METHOD_DEFAULT (0x00000000)</span></span>  <br/> |<span data-ttu-id="5895a-119">Conflicto resolver se debería generar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="5895a-119">Conflict resolve message should be generated.</span></span>  <br/> |
|<span data-ttu-id="5895a-120">RESOLVE_METHOD_LAST_WRITER_WINS (0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="5895a-120">RESOLVE_METHOD_LAST_WRITER_WINS (0x00000001)</span></span>  <br/> |<span data-ttu-id="5895a-121">Sobrescribir el mensaje de destino con los cambios actuales que se aplican.</span><span class="sxs-lookup"><span data-stu-id="5895a-121">Overwrite target message with current changes being applied.</span></span>  <br/> |
|<span data-ttu-id="5895a-122">RESOLVE_NO_CONFLICT_NOTIFICATION (0 X 00000002)</span><span class="sxs-lookup"><span data-stu-id="5895a-122">RESOLVE_NO_CONFLICT_NOTIFICATION (0x00000002)</span></span>  <br/> |<span data-ttu-id="5895a-123">No enviar mensaje de notificación de conflicto al generar conflicto resolver el mensaje en la carpeta pública.</span><span class="sxs-lookup"><span data-stu-id="5895a-123">Do not send conflict notification message when generating conflict resolve message in public folder.</span></span>  <br/> |
   
<span data-ttu-id="5895a-124">Un cliente o servidor no debe generar un mensaje de resolución de conflicto para mensajes asociados.</span><span class="sxs-lookup"><span data-stu-id="5895a-124">A client or server must not generate a conflict resolve message for associated messages.</span></span> <span data-ttu-id="5895a-125">Estos mensajes se deben resolver mediante el uso de la semántica **RESOLVE_METHOD_LAST_WRITER_WINS** .</span><span class="sxs-lookup"><span data-stu-id="5895a-125">These messages must be resolved by using **RESOLVE_METHOD_LAST_WRITER_WINS** semantics.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5895a-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5895a-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5895a-127">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="5895a-127">Protocol specifications</span></span>

<span data-ttu-id="5895a-128">[[MS-OXCSYNC]](http://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5895a-128">[[MS-OXCSYNC]](http://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5895a-129">Controla la sincronización de datos de objeto mensajería entre un servidor y un cliente.</span><span class="sxs-lookup"><span data-stu-id="5895a-129">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="5895a-130">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5895a-130">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5895a-131">Define las estructuras de datos básicos que se usan en las operaciones remotas.</span><span class="sxs-lookup"><span data-stu-id="5895a-131">Defines the basic data structures that are used in remote operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5895a-132">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5895a-132">Header files</span></span>

<span data-ttu-id="5895a-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5895a-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="5895a-134">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5895a-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="5895a-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5895a-135">Mapitags.h</span></span>
  
> <span data-ttu-id="5895a-136">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="5895a-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5895a-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="5895a-137">See also</span></span>



[<span data-ttu-id="5895a-138">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5895a-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5895a-139">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="5895a-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5895a-140">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5895a-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5895a-141">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="5895a-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

