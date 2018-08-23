---
title: IPersistMessageSaveCompleted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.SaveCompleted
api_type:
- COM
ms.assetid: 83161011-90b4-49cb-9bcd-153a21a10977
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7813636abc1c4d6ad756c7cf670e21d4acb7f540
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592748"
---
# <a name="ipersistmessagesavecompleted"></a><span data-ttu-id="102cb-103">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="102cb-103">IPersistMessage::SaveCompleted</span></span>

<span data-ttu-id="102cb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="102cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="102cb-105">Se notifica el formulario que guarda una operación se ha completado.</span><span class="sxs-lookup"><span data-stu-id="102cb-105">Notifies the form that a save operation has been completed.</span></span> 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="102cb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="102cb-106">Parameters</span></span>

<span data-ttu-id="102cb-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="102cb-107">_pMessage_</span></span>
  
> <span data-ttu-id="102cb-108">[entrada] Un puntero al mensaje recién guardado.</span><span class="sxs-lookup"><span data-stu-id="102cb-108">[in] A pointer to the newly saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="102cb-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="102cb-109">Return value</span></span>

<span data-ttu-id="102cb-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="102cb-110">S_OK</span></span> 
  
> <span data-ttu-id="102cb-111">La notificación fue correcta.</span><span class="sxs-lookup"><span data-stu-id="102cb-111">The notification was successful.</span></span>
    
<span data-ttu-id="102cb-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="102cb-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="102cb-113">El parámetro _pMessage_ es NULL y el formulario está en el estado [HandsOffFromNormal](handsofffromnormal-state.md) o [HandsOffAfterSave](handsoffaftersave-state.md) .</span><span class="sxs-lookup"><span data-stu-id="102cb-113">The  _pMessage_ parameter is NULL and the form is either in the [HandsOffFromNormal](handsofffromnormal-state.md) or [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> 
    
<span data-ttu-id="102cb-114">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="102cb-114">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="102cb-115">El formulario no está en uno de los siguientes estados:</span><span class="sxs-lookup"><span data-stu-id="102cb-115">The form is not in one of the following states:</span></span>
    
   - <span data-ttu-id="102cb-116">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="102cb-116">HandsOffFromNormal</span></span>
    
   - <span data-ttu-id="102cb-117">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="102cb-117">HandsOffAfterSave</span></span>
    
   - [<span data-ttu-id="102cb-118">NoScribble</span><span class="sxs-lookup"><span data-stu-id="102cb-118">NoScribble</span></span>](noscribble-state.md)
    
## <a name="remarks"></a><span data-ttu-id="102cb-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="102cb-119">Remarks</span></span>

<span data-ttu-id="102cb-120">Se llama al método de **IPersistMessage::SaveCompleted** por un visor de formulario para notificar el formulario que se han guardado todos los cambios pendientes.</span><span class="sxs-lookup"><span data-stu-id="102cb-120">The **IPersistMessage::SaveCompleted** method is called by a form viewer to notify the form that all pending changes have been saved.</span></span> <span data-ttu-id="102cb-121">**SaveCompleted** debe llamarse sólo cuando el formulario está en uno de los siguientes estados:</span><span class="sxs-lookup"><span data-stu-id="102cb-121">**SaveCompleted** should be called only when the form is in one of the following states:</span></span> 
  
- <span data-ttu-id="102cb-122">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="102cb-122">HandsOffFromNormal</span></span>
    
- <span data-ttu-id="102cb-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="102cb-123">HandsOffAfterSave</span></span>
    
- <span data-ttu-id="102cb-124">NoScribble</span><span class="sxs-lookup"><span data-stu-id="102cb-124">NoScribble</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="102cb-125">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="102cb-125">Notes to implementers</span></span>

<span data-ttu-id="102cb-126">Existen varias acciones posibles que puede realizar el método **SaveCompleted** , dependiendo de qué el mensaje contiene el parámetro de puntero y estado en que el mensaje está en.</span><span class="sxs-lookup"><span data-stu-id="102cb-126">There are several possible actions that the **SaveCompleted** method can perform, depending on what the message pointer parameter contains, and what state the message is in.</span></span> <span data-ttu-id="102cb-127">Sin embargo, cuando una acción es correcta, siempre guarde el estado actual del mensaje que señala el parámetro _pMessage_ y transición el formulario a su estado [Normal](normal-state.md) .</span><span class="sxs-lookup"><span data-stu-id="102cb-127">However, when an action is successful, always save the current state of the message that the  _pMessage_ parameter points to and transition the form to its [Normal](normal-state.md) state.</span></span> 
  
<span data-ttu-id="102cb-128">En la siguiente tabla se describe las condiciones que afectan a las acciones que debe realizar en su implementación de **SaveCompleted**.</span><span class="sxs-lookup"><span data-stu-id="102cb-128">The following table describes the conditions that affect the actions you should take in your implementation of **SaveCompleted**.</span></span>
  
|<span data-ttu-id="102cb-129">**Condición**</span><span class="sxs-lookup"><span data-stu-id="102cb-129">**Condition**</span></span>|<span data-ttu-id="102cb-130">**Acción**</span><span class="sxs-lookup"><span data-stu-id="102cb-130">**Action**</span></span>|
|:-----|:-----|
|<span data-ttu-id="102cb-131">El parámetro _pMessage_ es NULL y el parámetro _fSameAsLoad_ del método [IPersistMessage::Save](ipersistmessage-save.md) se establece en TRUE.</span><span class="sxs-lookup"><span data-stu-id="102cb-131">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the [IPersistMessage::Save](ipersistmessage-save.md) method is set to TRUE.</span></span>  <br/> |<span data-ttu-id="102cb-132">Llame al método [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) de todos los visores registrados, marcar el formulario como S_OK limpia y devolución.</span><span class="sxs-lookup"><span data-stu-id="102cb-132">Call the [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="102cb-133">El parámetro _pMessage_ es NULL y el parámetro _fSameAsLoad_ del método **IPersistMessage::Save** se establece en FALSE.</span><span class="sxs-lookup"><span data-stu-id="102cb-133">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the **IPersistMessage::Save** method is set to FALSE.</span></span>  <br/> |<span data-ttu-id="102cb-134">Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="102cb-134">Return S_OK.</span></span>  <br/> |
|<span data-ttu-id="102cb-135">El formulario está en el estado de HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="102cb-135">The form is in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="102cb-136">Liberar el mensaje actual y reemplácelo con el mensaje que apunta el parámetro _pMessage_ .</span><span class="sxs-lookup"><span data-stu-id="102cb-136">Release the current message and replace it with the message pointed to by the  _pMessage_ parameter.</span></span> <span data-ttu-id="102cb-137">Llamar al método [IUnknown:: AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) del mensaje de reemplazo y devolver S_OK.</span><span class="sxs-lookup"><span data-stu-id="102cb-137">Call the replacement message's [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="102cb-138">El formulario está en el estado de HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="102cb-138">The form is in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="102cb-139">Llame al método **IMAPIViewAdviseSink::OnSaved** de todos los visores registrados, marcar el formulario como S_OK limpia y devolución.</span><span class="sxs-lookup"><span data-stu-id="102cb-139">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="102cb-140">El formulario está en el estado de [NoScribble](noscribble-state.md) .</span><span class="sxs-lookup"><span data-stu-id="102cb-140">The form is in the [NoScribble](noscribble-state.md) state.</span></span>  <br/> |<span data-ttu-id="102cb-141">Liberar el mensaje actual y reemplácelo con el mensaje que apunta _pMessage_.</span><span class="sxs-lookup"><span data-stu-id="102cb-141">Release the current message and replace it with the message pointed to by  _pMessage_.</span></span> <span data-ttu-id="102cb-142">Llamar al método **IUnknown:: AddRef** del mensaje de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="102cb-142">Call the replacement message's **IUnknown::AddRef** method.</span></span> <span data-ttu-id="102cb-143">Llame al método **IMAPIViewAdviseSink::OnSaved** de todos los visores registrados, marcar el formulario como S_OK limpia y devolución.</span><span class="sxs-lookup"><span data-stu-id="102cb-143">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="102cb-144">El formulario está en uno de los Estados de HandsOff y el parámetro _pMessage_ se establece en NULL.</span><span class="sxs-lookup"><span data-stu-id="102cb-144">The form is in one of the HandsOff states and the  _pMessage_ parameter is set to NULL.</span></span>  <br/> |<span data-ttu-id="102cb-145">Devolver E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="102cb-145">Return E_INVALIDARG.</span></span>  <br/> |
|<span data-ttu-id="102cb-146">El formulario está en un estado que no sea uno de los Estados de HandsOff o el estado de NoScribble.</span><span class="sxs-lookup"><span data-stu-id="102cb-146">The form is in a state other than one of the HandsOff states or the NoScribble state.</span></span>  <br/> |<span data-ttu-id="102cb-147">Devolver E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="102cb-147">Return E_UNEXPECTED.</span></span>  <br/> |
   
<span data-ttu-id="102cb-148">Para obtener más información acerca de cómo guardar objetos de almacenamiento, vea la documentación de los métodos [IPersistStorage::SaveCompleted](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) o [:: SaveCompleted](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) .</span><span class="sxs-lookup"><span data-stu-id="102cb-148">For more information about saving storage objects, see the documentation for the [IPersistStorage::SaveCompleted](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) or [IPersistFile::SaveCompleted](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="102cb-149">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="102cb-149">See also</span></span>

- [<span data-ttu-id="102cb-150">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="102cb-150">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
- [<span data-ttu-id="102cb-151">Estados de formulario</span><span class="sxs-lookup"><span data-stu-id="102cb-151">Form States</span></span>](form-states.md)
