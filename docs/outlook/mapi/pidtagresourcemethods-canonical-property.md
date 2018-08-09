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
ms.openlocfilehash: f346baf303db9da765eec183d168b370547ec2de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820096"
---
# <a name="pidtagresourcemethods-canonical-property"></a><span data-ttu-id="af659-103">Propiedad canónica PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="af659-103">PidTagResourceMethods Canonical Property</span></span>

  
  
<span data-ttu-id="af659-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="af659-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="af659-105">Contiene una máscara de bits de marcadores que indican los métodos en la interfaz de **IMAPIStatus** que son compatibles con el objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="af659-105">Contains a bitmask of flags that indicate the methods in the **IMAPIStatus** interface that are supported by the status object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="af659-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="af659-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="af659-107">PR_RESOURCE_METHODS</span><span class="sxs-lookup"><span data-stu-id="af659-107">PR_RESOURCE_METHODS</span></span>  <br/> |
|<span data-ttu-id="af659-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="af659-108">Identifier:</span></span>  <br/> |<span data-ttu-id="af659-109">0x3E02</span><span class="sxs-lookup"><span data-stu-id="af659-109">0x3E02</span></span>  <br/> |
|<span data-ttu-id="af659-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="af659-110">Data type:</span></span>  <br/> |<span data-ttu-id="af659-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="af659-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="af659-112">Área:</span><span class="sxs-lookup"><span data-stu-id="af659-112">Area:</span></span>  <br/> |<span data-ttu-id="af659-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="af659-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af659-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="af659-114">Remarks</span></span>

<span data-ttu-id="af659-115">Esta propiedad indica cuál de los métodos de implementación de un objeto de estado de **IMAPIStatus** son compatibles.</span><span class="sxs-lookup"><span data-stu-id="af659-115">This property indicates which of the methods in a status object's implementation of **IMAPIStatus** are supported.</span></span> <span data-ttu-id="af659-116">Se permiten los objetos de estado para devolver MAPI_E_NO_SUPPORT de métodos no admitidos.</span><span class="sxs-lookup"><span data-stu-id="af659-116">Status objects are allowed to return MAPI_E_NO_SUPPORT from unsupported methods.</span></span> 
  
<span data-ttu-id="af659-117">Los clientes utilizan la propiedad **PR_RESOURCE_METHODS** de un objeto estado para evitar la realización de llamadas a métodos no admitidos.</span><span class="sxs-lookup"><span data-stu-id="af659-117">Clients use a status object's **PR_RESOURCE_METHODS** property to avoid making calls to unsupported methods.</span></span> <span data-ttu-id="af659-118">Si se establece la marca que corresponde a un método concreto, el método existe y se puede llamar.</span><span class="sxs-lookup"><span data-stu-id="af659-118">If the flag that corresponds to a particular method is set, the method exists and can be called.</span></span> <span data-ttu-id="af659-119">Si esa marca está desactivada, no se debe llamar al método.</span><span class="sxs-lookup"><span data-stu-id="af659-119">If that flag is clear, the method should not be called.</span></span> 
  
<span data-ttu-id="af659-120">Los objetos de estado implementan mediante la compatibilidad con MAPI los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="af659-120">The status objects implemented by MAPI support the following methods:</span></span>
  
|<span data-ttu-id="af659-121">**Objeto de estado**</span><span class="sxs-lookup"><span data-stu-id="af659-121">**Status object**</span></span>|<span data-ttu-id="af659-122">**Métodos admitidos**</span><span class="sxs-lookup"><span data-stu-id="af659-122">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="af659-123">Subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="af659-123">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="af659-124">**ValidateState**</span><span class="sxs-lookup"><span data-stu-id="af659-124">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="af659-125">Libreta de direcciones MAPI</span><span class="sxs-lookup"><span data-stu-id="af659-125">MAPI address book</span></span>  <br/> |<span data-ttu-id="af659-126">**ValidateState**</span><span class="sxs-lookup"><span data-stu-id="af659-126">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="af659-127">Cola MAPI</span><span class="sxs-lookup"><span data-stu-id="af659-127">MAPI spooler</span></span>  <br/> |<span data-ttu-id="af659-128">**ValidateState** y **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="af659-128">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="af659-129">Uno o varios de los siguientes indicadores se pueden establecer en **PR_RESOURCE_METHODS**:</span><span class="sxs-lookup"><span data-stu-id="af659-129">One or more of the following flags can be set in **PR_RESOURCE_METHODS**:</span></span>
  
<span data-ttu-id="af659-130">STATUS_CHANGE_PASSWORD</span><span class="sxs-lookup"><span data-stu-id="af659-130">STATUS_CHANGE_PASSWORD</span></span> 
  
> <span data-ttu-id="af659-131">Indica que se admite el método [IMAPIStatus](imapistatus-changepassword.md) .</span><span class="sxs-lookup"><span data-stu-id="af659-131">Indicates that the [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) method is supported.</span></span> 
    
<span data-ttu-id="af659-132">STATUS_FLUSH_QUEUES</span><span class="sxs-lookup"><span data-stu-id="af659-132">STATUS_FLUSH_QUEUES</span></span> 
  
> <span data-ttu-id="af659-133">Indica que se admite el método [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) .</span><span class="sxs-lookup"><span data-stu-id="af659-133">Indicates that the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method is supported.</span></span> 
    
<span data-ttu-id="af659-134">STATUS_SETTINGS_DIALOG</span><span class="sxs-lookup"><span data-stu-id="af659-134">STATUS_SETTINGS_DIALOG</span></span> 
  
> <span data-ttu-id="af659-135">Indica que se admite el método [SettingsDialog](imapistatus-settingsdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="af659-135">Indicates that the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method is supported.</span></span> 
    
<span data-ttu-id="af659-136">STATUS_VALIDATE_STATE</span><span class="sxs-lookup"><span data-stu-id="af659-136">STATUS_VALIDATE_STATE</span></span> 
  
> <span data-ttu-id="af659-137">Indica que se admite el método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="af659-137">Indicates that the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is supported.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="af659-138">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="af659-138">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="af659-139">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="af659-139">Header files</span></span>

<span data-ttu-id="af659-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="af659-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="af659-141">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="af659-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="af659-142">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="af659-142">Mapitags.h</span></span>
  
> <span data-ttu-id="af659-143">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="af659-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af659-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="af659-144">See also</span></span>



[<span data-ttu-id="af659-145">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="af659-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="af659-146">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="af659-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="af659-147">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="af659-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="af659-148">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="af659-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

