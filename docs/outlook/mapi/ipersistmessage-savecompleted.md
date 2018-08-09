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
ms.openlocfilehash: 7a82ce9a46017993adfc6c4c755b6c97b847e579
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817879"
---
# <a name="ipersistmessagesavecompleted"></a><span data-ttu-id="ced88-103">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="ced88-103">IPersistMessage::SaveCompleted</span></span>

<span data-ttu-id="ced88-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ced88-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ced88-105">Se notifica el formulario que guarda una operación se ha completado.</span><span class="sxs-lookup"><span data-stu-id="ced88-105">Notifies the form that a save operation has been completed.</span></span> 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="ced88-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ced88-106">Parameters</span></span>

<span data-ttu-id="ced88-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="ced88-107">_pMessage_</span></span>
  
> <span data-ttu-id="ced88-108">[entrada] Un puntero al mensaje recién guardado.</span><span class="sxs-lookup"><span data-stu-id="ced88-108">[in] A pointer to the newly saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ced88-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ced88-109">Return value</span></span>

<span data-ttu-id="ced88-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ced88-110">S_OK</span></span> 
  
> <span data-ttu-id="ced88-111">La notificación fue correcta.</span><span class="sxs-lookup"><span data-stu-id="ced88-111">The notification was successful.</span></span>
    
<span data-ttu-id="ced88-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ced88-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="ced88-113">El parámetro _pMessage_ es NULL y el formulario está en el estado [HandsOffFromNormal](handsofffromnormal-state.md) o [HandsOffAfterSave](handsoffaftersave-state.md) .</span><span class="sxs-lookup"><span data-stu-id="ced88-113">The  _pMessage_ parameter is NULL and the form is either in the [HandsOffFromNormal](handsofffromnormal-state.md) or [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> 
    
<span data-ttu-id="ced88-114">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="ced88-114">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="ced88-115">El formulario no está en uno de los siguientes estados:</span><span class="sxs-lookup"><span data-stu-id="ced88-115">The form is not in one of the following states:</span></span>
    
   - <span data-ttu-id="ced88-116">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="ced88-116">HandsOffFromNormal</span></span>
    
   - <span data-ttu-id="ced88-117">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="ced88-117">HandsOffAfterSave</span></span>
    
   - [<span data-ttu-id="ced88-118">NoScribble</span><span class="sxs-lookup"><span data-stu-id="ced88-118">NoScribble</span></span>](noscribble-state.md)
    
## <a name="remarks"></a><span data-ttu-id="ced88-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ced88-119">Remarks</span></span>

<span data-ttu-id="ced88-120">Se llama al método de **IPersistMessage::SaveCompleted** por un visor de formulario para notificar el formulario que se han guardado todos los cambios pendientes.</span><span class="sxs-lookup"><span data-stu-id="ced88-120">The **IPersistMessage::SaveCompleted** method is called by a form viewer to notify the form that all pending changes have been saved.</span></span> <span data-ttu-id="ced88-121">**SaveCompleted** debe llamarse sólo cuando el formulario está en uno de los siguientes estados:</span><span class="sxs-lookup"><span data-stu-id="ced88-121">**SaveCompleted** should be called only when the form is in one of the following states:</span></span> 
  
- <span data-ttu-id="ced88-122">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="ced88-122">HandsOffFromNormal</span></span>
    
- <span data-ttu-id="ced88-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="ced88-123">HandsOffAfterSave</span></span>
    
- <span data-ttu-id="ced88-124">NoScribble</span><span class="sxs-lookup"><span data-stu-id="ced88-124">NoScribble</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="ced88-125">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="ced88-125">Notes to implementers</span></span>

<span data-ttu-id="ced88-126">Existen varias acciones posibles que puede realizar el método **SaveCompleted** , dependiendo de qué el mensaje contiene el parámetro de puntero y estado en que el mensaje está en.</span><span class="sxs-lookup"><span data-stu-id="ced88-126">There are several possible actions that the **SaveCompleted** method can perform, depending on what the message pointer parameter contains, and what state the message is in.</span></span> <span data-ttu-id="ced88-127">Sin embargo, cuando una acción es correcta, siempre guarde el estado actual del mensaje que señala el parámetro _pMessage_ y transición el formulario a su estado [Normal](normal-state.md) .</span><span class="sxs-lookup"><span data-stu-id="ced88-127">However, when an action is successful, always save the current state of the message that the  _pMessage_ parameter points to and transition the form to its [Normal](normal-state.md) state.</span></span> 
  
<span data-ttu-id="ced88-128">En la siguiente tabla se describe las condiciones que afectan a las acciones que debe realizar en su implementación de **SaveCompleted**.</span><span class="sxs-lookup"><span data-stu-id="ced88-128">The following table describes the conditions that affect the actions you should take in your implementation of **SaveCompleted**.</span></span>
  
|<span data-ttu-id="ced88-129">**Condición**</span><span class="sxs-lookup"><span data-stu-id="ced88-129">**Condition**</span></span>|<span data-ttu-id="ced88-130">**Acción**</span><span class="sxs-lookup"><span data-stu-id="ced88-130">**Action**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ced88-131">El parámetro _pMessage_ es NULL y el parámetro _fSameAsLoad_ del método [IPersistMessage::Save](ipersistmessage-save.md) se establece en TRUE.</span><span class="sxs-lookup"><span data-stu-id="ced88-131">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the [IPersistMessage::Save](ipersistmessage-save.md) method is set to TRUE.</span></span>  <br/> |<span data-ttu-id="ced88-132">Llame al método [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) de todos los visores registrados, marcar el formulario como S_OK limpia y devolución.</span><span class="sxs-lookup"><span data-stu-id="ced88-132">Call the [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="ced88-133">El parámetro _pMessage_ es NULL y el parámetro _fSameAsLoad_ del método **IPersistMessage::Save** se establece en FALSE.</span><span class="sxs-lookup"><span data-stu-id="ced88-133">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the **IPersistMessage::Save** method is set to FALSE.</span></span>  <br/> |<span data-ttu-id="ced88-134">Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="ced88-134">Return S_OK.</span></span>  <br/> |
|<span data-ttu-id="ced88-135">El formulario está en el estado de HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="ced88-135">The form is in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="ced88-136">Liberar el mensaje actual y reemplácelo con el mensaje que apunta el parámetro _pMessage_ .</span><span class="sxs-lookup"><span data-stu-id="ced88-136">Release the current message and replace it with the message pointed to by the  _pMessage_ parameter.</span></span> <span data-ttu-id="ced88-137">Llamar al método [IUnknown:: AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) del mensaje de reemplazo y devolver S_OK.</span><span class="sxs-lookup"><span data-stu-id="ced88-137">Call the replacement message's [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="ced88-138">El formulario está en el estado de HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="ced88-138">The form is in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="ced88-139">Llame al método **IMAPIViewAdviseSink::OnSaved** de todos los visores registrados, marcar el formulario como S_OK limpia y devolución.</span><span class="sxs-lookup"><span data-stu-id="ced88-139">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="ced88-140">El formulario está en el estado de [NoScribble](noscribble-state.md) .</span><span class="sxs-lookup"><span data-stu-id="ced88-140">The form is in the [NoScribble](noscribble-state.md) state.</span></span>  <br/> |<span data-ttu-id="ced88-141">Liberar el mensaje actual y reemplácelo con el mensaje que apunta _pMessage_.</span><span class="sxs-lookup"><span data-stu-id="ced88-141">Release the current message and replace it with the message pointed to by  _pMessage_.</span></span> <span data-ttu-id="ced88-142">Llamar al método **IUnknown:: AddRef** del mensaje de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="ced88-142">Call the replacement message's **IUnknown::AddRef** method.</span></span> <span data-ttu-id="ced88-143">Llame al método **IMAPIViewAdviseSink::OnSaved** de todos los visores registrados, marcar el formulario como S_OK limpia y devolución.</span><span class="sxs-lookup"><span data-stu-id="ced88-143">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="ced88-144">El formulario está en uno de los Estados de HandsOff y el parámetro _pMessage_ se establece en NULL.</span><span class="sxs-lookup"><span data-stu-id="ced88-144">The form is in one of the HandsOff states and the  _pMessage_ parameter is set to NULL.</span></span>  <br/> |<span data-ttu-id="ced88-145">Devolver E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="ced88-145">Return E_INVALIDARG.</span></span>  <br/> |
|<span data-ttu-id="ced88-146">El formulario está en un estado que no sea uno de los Estados de HandsOff o el estado de NoScribble.</span><span class="sxs-lookup"><span data-stu-id="ced88-146">The form is in a state other than one of the HandsOff states or the NoScribble state.</span></span>  <br/> |<span data-ttu-id="ced88-147">Devolver E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="ced88-147">Return E_UNEXPECTED.</span></span>  <br/> |
   
<span data-ttu-id="ced88-148">Para obtener más información acerca de cómo guardar objetos de almacenamiento, vea la documentación de los métodos [IPersistStorage::SaveCompleted](http://msdn.microsoft.com/library/_com_ipersiststorage_savecompleted%28Office.15%29.aspx) o [:: SaveCompleted](http://msdn.microsoft.com/library/_com_ipersistfile_savecompleted%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ced88-148">For more information about saving storage objects, see the documentation for the [IPersistStorage::SaveCompleted](http://msdn.microsoft.com/library/_com_ipersiststorage_savecompleted%28Office.15%29.aspx) or [IPersistFile::SaveCompleted](http://msdn.microsoft.com/library/_com_ipersistfile_savecompleted%28Office.15%29.aspx) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ced88-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="ced88-149">See also</span></span>



[<span data-ttu-id="ced88-150">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ced88-150">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="ced88-151">Estados de formulario</span><span class="sxs-lookup"><span data-stu-id="ced88-151">Form States</span></span>](form-states.md)


[<span data-ttu-id="ced88-152">IPersistStorage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="ced88-152">IPersistStorage::SaveCompleted</span></span>](http://msdn.microsoft.com/library/_com_ipersiststorage_savecompleted%28Office.15%29.aspx)
  
[<span data-ttu-id="ced88-153">:: SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="ced88-153">IPersistFile::SaveCompleted</span></span>](http://msdn.microsoft.com/library/_com_ipersistfile_savecompleted%28Office.15%29.aspx)

