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
ms.openlocfilehash: 2868533e0383309e013bb82aaa4300a0a40e335a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577516"
---
# <a name="pidtagcontrolid-canonical-property"></a><span data-ttu-id="fc0cb-103">Propiedad canónica PidTagControlId</span><span class="sxs-lookup"><span data-stu-id="fc0cb-103">PidTagControlId Canonical Property</span></span>

  
  
<span data-ttu-id="fc0cb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc0cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc0cb-105">Contiene un identificador único para un control que se utiliza en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="fc0cb-105">Contains a unique identifier for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fc0cb-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="fc0cb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fc0cb-107">PR_CONTROL_ID</span><span class="sxs-lookup"><span data-stu-id="fc0cb-107">PR_CONTROL_ID</span></span>  <br/> |
|<span data-ttu-id="fc0cb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fc0cb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fc0cb-109">0x3F07</span><span class="sxs-lookup"><span data-stu-id="fc0cb-109">0x3F07</span></span>  <br/> |
|<span data-ttu-id="fc0cb-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fc0cb-110">Data type:</span></span>  <br/> |<span data-ttu-id="fc0cb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fc0cb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fc0cb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fc0cb-112">Area:</span></span>  <br/> |<span data-ttu-id="fc0cb-113">Tabla MAPI para mostrar</span><span class="sxs-lookup"><span data-stu-id="fc0cb-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc0cb-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fc0cb-114">Remarks</span></span>

<span data-ttu-id="fc0cb-115">Esta propiedad contiene un identificador único para el control.</span><span class="sxs-lookup"><span data-stu-id="fc0cb-115">This property contains a unique identifier for the control.</span></span> <span data-ttu-id="fc0cb-116">Este identificador debe contener una estructura [GUID](guid.md) y un valor de tipo **LONG**binary.</span><span class="sxs-lookup"><span data-stu-id="fc0cb-116">This identifier should contain a [GUID](guid.md) structure and a binary value of type **LONG**.</span></span> <span data-ttu-id="fc0cb-117">Todos los controles en el cuadro de diálogo deben usar el mismo **GUID** para identificar el proveedor de servicios, y cada control debe usar un único valor de **tipo LONG** para asegurarse de que los controles no entrar en conflicto.</span><span class="sxs-lookup"><span data-stu-id="fc0cb-117">All controls in the dialog box should use the same **GUID** to identify the service provider, and each control should use a unique **LONG** value to ensure that the controls do not collide.</span></span> 
  
<span data-ttu-id="fc0cb-118">Esta propiedad se usa en las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="fc0cb-118">This property is used in notifications.</span></span> <span data-ttu-id="fc0cb-119">Por ejemplo, las notificaciones enviadas en la tabla para mostrar deben establecer esta propiedad para identificar de forma única el control que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="fc0cb-119">For example, notifications sent on the display table must set this property to uniquely identify the control to update.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fc0cb-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc0cb-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="fc0cb-121">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fc0cb-121">Header files</span></span>

<span data-ttu-id="fc0cb-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fc0cb-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="fc0cb-123">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fc0cb-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="fc0cb-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fc0cb-124">Mapitags.h</span></span>
  
> <span data-ttu-id="fc0cb-125">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="fc0cb-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fc0cb-126">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="fc0cb-126">See also</span></span>



[<span data-ttu-id="fc0cb-127">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fc0cb-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fc0cb-128">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="fc0cb-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fc0cb-129">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="fc0cb-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fc0cb-130">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="fc0cb-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

