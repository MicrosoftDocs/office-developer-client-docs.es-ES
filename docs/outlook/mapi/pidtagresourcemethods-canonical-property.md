---
title: Propiedad canónica PidTagResourceMethods
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceMethods
api_type:
- COM
ms.assetid: 60ebbcd5-b758-4c96-b8ec-089e0aae1a5f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e9aee3280edbed60e97ef6e00e61f3086f6f07ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330145"
---
# <a name="pidtagresourcemethods-canonical-property"></a><span data-ttu-id="a7729-103">Propiedad canónica PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="a7729-103">PidTagResourceMethods Canonical Property</span></span>

  
  
<span data-ttu-id="a7729-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7729-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7729-105">Contiene una máscara de máscara de marcadores que indica los métodos de la interfaz **IMAPIStatus** que son compatibles con el objeto status.</span><span class="sxs-lookup"><span data-stu-id="a7729-105">Contains a bitmask of flags that indicate the methods in the **IMAPIStatus** interface that are supported by the status object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a7729-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a7729-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a7729-107">PR_RESOURCE_METHODS</span><span class="sxs-lookup"><span data-stu-id="a7729-107">PR_RESOURCE_METHODS</span></span>  <br/> |
|<span data-ttu-id="a7729-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a7729-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a7729-109">0x3E02</span><span class="sxs-lookup"><span data-stu-id="a7729-109">0x3E02</span></span>  <br/> |
|<span data-ttu-id="a7729-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a7729-110">Data type:</span></span>  <br/> |<span data-ttu-id="a7729-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a7729-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a7729-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a7729-112">Area:</span></span>  <br/> |<span data-ttu-id="a7729-113">Estado de MAPI</span><span class="sxs-lookup"><span data-stu-id="a7729-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7729-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a7729-114">Remarks</span></span>

<span data-ttu-id="a7729-115">Esta propiedad indica qué métodos de la implementación de **IMAPIStatus** de un objeto de estado son compatibles.</span><span class="sxs-lookup"><span data-stu-id="a7729-115">This property indicates which of the methods in a status object's implementation of **IMAPIStatus** are supported.</span></span> <span data-ttu-id="a7729-116">Los objetos de estado pueden devolver MAPI_E_NO_SUPPORT de métodos no admitidos.</span><span class="sxs-lookup"><span data-stu-id="a7729-116">Status objects are allowed to return MAPI_E_NO_SUPPORT from unsupported methods.</span></span> 
  
<span data-ttu-id="a7729-117">Los clientes usan la propiedad **PR_RESOURCE_METHODS** de un objeto de estado para evitar realizar llamadas a métodos no admitidos.</span><span class="sxs-lookup"><span data-stu-id="a7729-117">Clients use a status object's **PR_RESOURCE_METHODS** property to avoid making calls to unsupported methods.</span></span> <span data-ttu-id="a7729-118">Si se establece la marca que corresponde a un método en particular, el método existe y se puede llamar.</span><span class="sxs-lookup"><span data-stu-id="a7729-118">If the flag that corresponds to a particular method is set, the method exists and can be called.</span></span> <span data-ttu-id="a7729-119">Si la marca está desactivada, no se debe llamar al método.</span><span class="sxs-lookup"><span data-stu-id="a7729-119">If that flag is clear, the method should not be called.</span></span> 
  
<span data-ttu-id="a7729-120">Los objetos de estado implementados por MAPI admiten los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a7729-120">The status objects implemented by MAPI support the following methods:</span></span>
  
|<span data-ttu-id="a7729-121">**Status (objeto)**</span><span class="sxs-lookup"><span data-stu-id="a7729-121">**Status object**</span></span>|<span data-ttu-id="a7729-122">**Métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="a7729-122">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a7729-123">Subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="a7729-123">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="a7729-124">Solo **ValidateState**</span><span class="sxs-lookup"><span data-stu-id="a7729-124">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="a7729-125">Libreta de direcciones MAPI</span><span class="sxs-lookup"><span data-stu-id="a7729-125">MAPI address book</span></span>  <br/> |<span data-ttu-id="a7729-126">Solo **ValidateState**</span><span class="sxs-lookup"><span data-stu-id="a7729-126">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="a7729-127">Cola MAPI</span><span class="sxs-lookup"><span data-stu-id="a7729-127">MAPI spooler</span></span>  <br/> |<span data-ttu-id="a7729-128">**ValidateState** y **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="a7729-128">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="a7729-129">Se pueden establecer uno o varios de los siguientes indicadores en **PR_RESOURCE_METHODS**:</span><span class="sxs-lookup"><span data-stu-id="a7729-129">One or more of the following flags can be set in **PR_RESOURCE_METHODS**:</span></span>
  
<span data-ttu-id="a7729-130">STATUS_CHANGE_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="a7729-130">STATUS_CHANGE_PASSWORD</span></span> 
  
> <span data-ttu-id="a7729-131">Indica que se admite el método [IMAPIStatus:: ChangePassword](imapistatus-changepassword.md) .</span><span class="sxs-lookup"><span data-stu-id="a7729-131">Indicates that the [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) method is supported.</span></span> 
    
<span data-ttu-id="a7729-132">STATUS_FLUSH_QUEUES</span><span class="sxs-lookup"><span data-stu-id="a7729-132">STATUS_FLUSH_QUEUES</span></span> 
  
> <span data-ttu-id="a7729-133">Indica que se admite el método [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) .</span><span class="sxs-lookup"><span data-stu-id="a7729-133">Indicates that the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method is supported.</span></span> 
    
<span data-ttu-id="a7729-134">STATUS_SETTINGS_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a7729-134">STATUS_SETTINGS_DIALOG</span></span> 
  
> <span data-ttu-id="a7729-135">Indica que se admite el método [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="a7729-135">Indicates that the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method is supported.</span></span> 
    
<span data-ttu-id="a7729-136">STATUS_VALIDATE_STATE</span><span class="sxs-lookup"><span data-stu-id="a7729-136">STATUS_VALIDATE_STATE</span></span> 
  
> <span data-ttu-id="a7729-137">Indica que se admite el método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="a7729-137">Indicates that the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is supported.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="a7729-138">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a7729-138">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a7729-139">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a7729-139">Header files</span></span>

<span data-ttu-id="a7729-140">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a7729-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="a7729-141">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a7729-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="a7729-142">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="a7729-142">Mapitags.h</span></span>
  
> <span data-ttu-id="a7729-143">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="a7729-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a7729-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7729-144">See also</span></span>



[<span data-ttu-id="a7729-145">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a7729-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a7729-146">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="a7729-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a7729-147">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a7729-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a7729-148">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="a7729-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

