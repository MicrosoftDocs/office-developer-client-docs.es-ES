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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436338"
---
# <a name="pidtagresourcemethods-canonical-property"></a><span data-ttu-id="75ba1-103">Propiedad canónica PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="75ba1-103">PidTagResourceMethods Canonical Property</span></span>

  
  
<span data-ttu-id="75ba1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75ba1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75ba1-105">Contiene una máscara de bits de marcas que indican los métodos de la interfaz **IMAPIStatus** que son compatibles con el objeto status.</span><span class="sxs-lookup"><span data-stu-id="75ba1-105">Contains a bitmask of flags that indicate the methods in the **IMAPIStatus** interface that are supported by the status object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="75ba1-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="75ba1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="75ba1-107">PR_RESOURCE_METHODS</span><span class="sxs-lookup"><span data-stu-id="75ba1-107">PR_RESOURCE_METHODS</span></span>  <br/> |
|<span data-ttu-id="75ba1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="75ba1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="75ba1-109">0x3E02</span><span class="sxs-lookup"><span data-stu-id="75ba1-109">0x3E02</span></span>  <br/> |
|<span data-ttu-id="75ba1-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="75ba1-110">Data type:</span></span>  <br/> |<span data-ttu-id="75ba1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="75ba1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="75ba1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="75ba1-112">Area:</span></span>  <br/> |<span data-ttu-id="75ba1-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="75ba1-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75ba1-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="75ba1-114">Remarks</span></span>

<span data-ttu-id="75ba1-115">Esta propiedad indica cuál de los métodos de la implementación de **IMAPIStatus** de un objeto de estado es compatible.</span><span class="sxs-lookup"><span data-stu-id="75ba1-115">This property indicates which of the methods in a status object's implementation of **IMAPIStatus** are supported.</span></span> <span data-ttu-id="75ba1-116">Los objetos status pueden devolver MAPI_E_NO_SUPPORT de métodos no admitidos.</span><span class="sxs-lookup"><span data-stu-id="75ba1-116">Status objects are allowed to return MAPI_E_NO_SUPPORT from unsupported methods.</span></span> 
  
<span data-ttu-id="75ba1-117">Los clientes usan la propiedad PR_RESOURCE_METHODS de un objeto **de** estado para evitar realizar llamadas a métodos no compatibles.</span><span class="sxs-lookup"><span data-stu-id="75ba1-117">Clients use a status object's **PR_RESOURCE_METHODS** property to avoid making calls to unsupported methods.</span></span> <span data-ttu-id="75ba1-118">Si se establece la marca que corresponde a un método determinado, el método existe y se puede llamar.</span><span class="sxs-lookup"><span data-stu-id="75ba1-118">If the flag that corresponds to a particular method is set, the method exists and can be called.</span></span> <span data-ttu-id="75ba1-119">Si esa marca está clara, no se debe llamar al método.</span><span class="sxs-lookup"><span data-stu-id="75ba1-119">If that flag is clear, the method should not be called.</span></span> 
  
<span data-ttu-id="75ba1-120">Los objetos de estado implementados por MAPI admiten los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="75ba1-120">The status objects implemented by MAPI support the following methods:</span></span>
  
|<span data-ttu-id="75ba1-121">**Status (objeto)**</span><span class="sxs-lookup"><span data-stu-id="75ba1-121">**Status object**</span></span>|<span data-ttu-id="75ba1-122">**Métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="75ba1-122">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="75ba1-123">Subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="75ba1-123">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="75ba1-124">**ValidateState** only</span><span class="sxs-lookup"><span data-stu-id="75ba1-124">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="75ba1-125">Libreta de direcciones MAPI</span><span class="sxs-lookup"><span data-stu-id="75ba1-125">MAPI address book</span></span>  <br/> |<span data-ttu-id="75ba1-126">**ValidateState** only</span><span class="sxs-lookup"><span data-stu-id="75ba1-126">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="75ba1-127">Cola MAPI</span><span class="sxs-lookup"><span data-stu-id="75ba1-127">MAPI spooler</span></span>  <br/> |<span data-ttu-id="75ba1-128">**ValidateState** y **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="75ba1-128">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="75ba1-129">Una o varias de las siguientes marcas se pueden establecer en **PR_RESOURCE_METHODS**:</span><span class="sxs-lookup"><span data-stu-id="75ba1-129">One or more of the following flags can be set in **PR_RESOURCE_METHODS**:</span></span>
  
<span data-ttu-id="75ba1-130">STATUS_CHANGE_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="75ba1-130">STATUS_CHANGE_PASSWORD</span></span> 
  
> <span data-ttu-id="75ba1-131">Indica que se admite [el método IMAPIStatus::ChangePassword.](imapistatus-changepassword.md)</span><span class="sxs-lookup"><span data-stu-id="75ba1-131">Indicates that the [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) method is supported.</span></span> 
    
<span data-ttu-id="75ba1-132">STATUS_FLUSH_QUEUES</span><span class="sxs-lookup"><span data-stu-id="75ba1-132">STATUS_FLUSH_QUEUES</span></span> 
  
> <span data-ttu-id="75ba1-133">Indica que se admite [el método IMAPIStatus::FlushQueues.](imapistatus-flushqueues.md)</span><span class="sxs-lookup"><span data-stu-id="75ba1-133">Indicates that the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method is supported.</span></span> 
    
<span data-ttu-id="75ba1-134">STATUS_SETTINGS_DIALOG</span><span class="sxs-lookup"><span data-stu-id="75ba1-134">STATUS_SETTINGS_DIALOG</span></span> 
  
> <span data-ttu-id="75ba1-135">Indica que se admite [el método IMAPIStatus::SettingsDialog.](imapistatus-settingsdialog.md)</span><span class="sxs-lookup"><span data-stu-id="75ba1-135">Indicates that the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method is supported.</span></span> 
    
<span data-ttu-id="75ba1-136">STATUS_VALIDATE_STATE</span><span class="sxs-lookup"><span data-stu-id="75ba1-136">STATUS_VALIDATE_STATE</span></span> 
  
> <span data-ttu-id="75ba1-137">Indica que se admite [el método IMAPIStatus::ValidateState.](imapistatus-validatestate.md)</span><span class="sxs-lookup"><span data-stu-id="75ba1-137">Indicates that the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is supported.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="75ba1-138">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="75ba1-138">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="75ba1-139">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="75ba1-139">Header files</span></span>

<span data-ttu-id="75ba1-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="75ba1-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="75ba1-141">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="75ba1-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="75ba1-142">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="75ba1-142">Mapitags.h</span></span>
  
> <span data-ttu-id="75ba1-143">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="75ba1-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75ba1-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="75ba1-144">See also</span></span>



[<span data-ttu-id="75ba1-145">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="75ba1-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="75ba1-146">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="75ba1-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="75ba1-147">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="75ba1-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="75ba1-148">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="75ba1-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

