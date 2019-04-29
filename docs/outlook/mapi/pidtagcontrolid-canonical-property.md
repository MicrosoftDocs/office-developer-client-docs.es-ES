---
title: Propiedad canónica PidTagControlId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlId
api_type:
- HeaderDef
ms.assetid: 281bc3e0-7c69-461b-bf09-4281abbb5e1b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b27f59e0bfdcac8eca1751af2f07139f12e2b3a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416023"
---
# <a name="pidtagcontrolid-canonical-property"></a><span data-ttu-id="e8ff9-103">Propiedad canónica PidTagControlId</span><span class="sxs-lookup"><span data-stu-id="e8ff9-103">PidTagControlId Canonical Property</span></span>

  
  
<span data-ttu-id="e8ff9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8ff9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8ff9-105">Contiene un identificador único para un control utilizado en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e8ff9-105">Contains a unique identifier for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e8ff9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e8ff9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e8ff9-107">PR_CONTROL_ID</span><span class="sxs-lookup"><span data-stu-id="e8ff9-107">PR_CONTROL_ID</span></span>  <br/> |
|<span data-ttu-id="e8ff9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e8ff9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e8ff9-109">0x3F07</span><span class="sxs-lookup"><span data-stu-id="e8ff9-109">0x3F07</span></span>  <br/> |
|<span data-ttu-id="e8ff9-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e8ff9-110">Data type:</span></span>  <br/> |<span data-ttu-id="e8ff9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e8ff9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e8ff9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e8ff9-112">Area:</span></span>  <br/> |<span data-ttu-id="e8ff9-113">Tabla de visualización de MAPI</span><span class="sxs-lookup"><span data-stu-id="e8ff9-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8ff9-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e8ff9-114">Remarks</span></span>

<span data-ttu-id="e8ff9-115">Esta propiedad contiene un identificador único para el control.</span><span class="sxs-lookup"><span data-stu-id="e8ff9-115">This property contains a unique identifier for the control.</span></span> <span data-ttu-id="e8ff9-116">Este identificador debe contener una estructura [GUID](guid.md) y un valor binario de tipo **Long**.</span><span class="sxs-lookup"><span data-stu-id="e8ff9-116">This identifier should contain a [GUID](guid.md) structure and a binary value of type **LONG**.</span></span> <span data-ttu-id="e8ff9-117">Todos los controles del cuadro de diálogo deben usar el mismo **GUID** para identificar el proveedor de servicios, y cada control debe usar un valor de **tipo Long** único para garantizar que los controles no entren en colisión.</span><span class="sxs-lookup"><span data-stu-id="e8ff9-117">All controls in the dialog box should use the same **GUID** to identify the service provider, and each control should use a unique **LONG** value to ensure that the controls do not collide.</span></span> 
  
<span data-ttu-id="e8ff9-118">Esta propiedad se usa en las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="e8ff9-118">This property is used in notifications.</span></span> <span data-ttu-id="e8ff9-119">Por ejemplo, las notificaciones enviadas en la tabla de presentación deben establecer esta propiedad para identificar de forma exclusiva el control que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="e8ff9-119">For example, notifications sent on the display table must set this property to uniquely identify the control to update.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e8ff9-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e8ff9-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e8ff9-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e8ff9-121">Header files</span></span>

<span data-ttu-id="e8ff9-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e8ff9-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="e8ff9-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e8ff9-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="e8ff9-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e8ff9-124">Mapitags.h</span></span>
  
> <span data-ttu-id="e8ff9-125">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="e8ff9-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e8ff9-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="e8ff9-126">See also</span></span>



[<span data-ttu-id="e8ff9-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e8ff9-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e8ff9-128">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="e8ff9-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e8ff9-129">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e8ff9-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e8ff9-130">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="e8ff9-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

