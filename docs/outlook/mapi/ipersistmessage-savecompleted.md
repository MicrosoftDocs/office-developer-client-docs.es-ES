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
ms.openlocfilehash: 021be209a2b2c891b668fa401500d6220619f9bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317139"
---
# <a name="ipersistmessagesavecompleted"></a><span data-ttu-id="d172c-103">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="d172c-103">IPersistMessage::SaveCompleted</span></span>

<span data-ttu-id="d172c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d172c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d172c-105">Notifica al formulario que se ha completado una operación de guardado.</span><span class="sxs-lookup"><span data-stu-id="d172c-105">Notifies the form that a save operation has been completed.</span></span> 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="d172c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d172c-106">Parameters</span></span>

<span data-ttu-id="d172c-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="d172c-107">_pMessage_</span></span>
  
> <span data-ttu-id="d172c-108">[entrada] Un puntero al mensaje recién guardado.</span><span class="sxs-lookup"><span data-stu-id="d172c-108">[in] A pointer to the newly saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d172c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d172c-109">Return value</span></span>

<span data-ttu-id="d172c-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="d172c-110">S_OK</span></span> 
  
> <span data-ttu-id="d172c-111">La notificación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d172c-111">The notification was successful.</span></span>
    
<span data-ttu-id="d172c-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d172c-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="d172c-113">El _parámetro pMessage_ es NULL y el formulario está en el estado [HandsOffFromNormal](handsofffromnormal-state.md) o [HandsOffAfterSave.](handsoffaftersave-state.md)</span><span class="sxs-lookup"><span data-stu-id="d172c-113">The  _pMessage_ parameter is NULL and the form is either in the [HandsOffFromNormal](handsofffromnormal-state.md) or [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> 
    
<span data-ttu-id="d172c-114">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="d172c-114">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="d172c-115">El formulario no está en uno de los siguientes estados:</span><span class="sxs-lookup"><span data-stu-id="d172c-115">The form is not in one of the following states:</span></span>
    
   - <span data-ttu-id="d172c-116">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="d172c-116">HandsOffFromNormal</span></span>
    
   - <span data-ttu-id="d172c-117">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="d172c-117">HandsOffAfterSave</span></span>
    
   - [<span data-ttu-id="d172c-118">NoScribble</span><span class="sxs-lookup"><span data-stu-id="d172c-118">NoScribble</span></span>](noscribble-state.md)
    
## <a name="remarks"></a><span data-ttu-id="d172c-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d172c-119">Remarks</span></span>

<span data-ttu-id="d172c-120">Un visor de formulario llama al método **IPersistMessage::SaveCompleted** para notificar al formulario que se han guardado todos los cambios pendientes.</span><span class="sxs-lookup"><span data-stu-id="d172c-120">The **IPersistMessage::SaveCompleted** method is called by a form viewer to notify the form that all pending changes have been saved.</span></span> <span data-ttu-id="d172c-121">Solo se debe llamar a **SaveCompleted** cuando el formulario se encuentra en uno de los siguientes estados:</span><span class="sxs-lookup"><span data-stu-id="d172c-121">**SaveCompleted** should be called only when the form is in one of the following states:</span></span> 
  
- <span data-ttu-id="d172c-122">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="d172c-122">HandsOffFromNormal</span></span>
    
- <span data-ttu-id="d172c-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="d172c-123">HandsOffAfterSave</span></span>
    
- <span data-ttu-id="d172c-124">NoScribble</span><span class="sxs-lookup"><span data-stu-id="d172c-124">NoScribble</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="d172c-125">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="d172c-125">Notes to implementers</span></span>

<span data-ttu-id="d172c-126">Hay varias acciones posibles que puede realizar el método **SaveCompleted,** en función de lo que contenga el parámetro de puntero del mensaje y del estado en que se encuentra el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d172c-126">There are several possible actions that the **SaveCompleted** method can perform, depending on what the message pointer parameter contains, and what state the message is in.</span></span> <span data-ttu-id="d172c-127">Sin embargo, cuando una acción se realiza correctamente, guarde siempre el estado actual del mensaje al que apunta el parámetro _pMessage_ y haga la transición del formulario a [su estado Normal.](normal-state.md)</span><span class="sxs-lookup"><span data-stu-id="d172c-127">However, when an action is successful, always save the current state of the message that the  _pMessage_ parameter points to and transition the form to its [Normal](normal-state.md) state.</span></span> 
  
<span data-ttu-id="d172c-128">En la tabla siguiente se describen las condiciones que afectan a las acciones que debe realizar en la implementación de **SaveCompleted**.</span><span class="sxs-lookup"><span data-stu-id="d172c-128">The following table describes the conditions that affect the actions you should take in your implementation of **SaveCompleted**.</span></span>
  
|<span data-ttu-id="d172c-129">**Condición**</span><span class="sxs-lookup"><span data-stu-id="d172c-129">**Condition**</span></span>|<span data-ttu-id="d172c-130">**Acción**</span><span class="sxs-lookup"><span data-stu-id="d172c-130">**Action**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d172c-131">El  _parámetro pMessage_ es NULL y el parámetro  _fSameAsLoad_ del [método IPersistMessage::Save](ipersistmessage-save.md) se establece en TRUE.</span><span class="sxs-lookup"><span data-stu-id="d172c-131">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the [IPersistMessage::Save](ipersistmessage-save.md) method is set to TRUE.</span></span>  <br/> |<span data-ttu-id="d172c-132">Llame al [método IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) de todos los visores registrados, marque el formulario como limpio y devuelva S_OK.</span><span class="sxs-lookup"><span data-stu-id="d172c-132">Call the [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="d172c-133">El  _parámetro pMessage_ es NULL y el parámetro  _fSameAsLoad_ del **método IPersistMessage::Save** se establece en FALSE.</span><span class="sxs-lookup"><span data-stu-id="d172c-133">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the **IPersistMessage::Save** method is set to FALSE.</span></span>  <br/> |<span data-ttu-id="d172c-134">Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="d172c-134">Return S_OK.</span></span>  <br/> |
|<span data-ttu-id="d172c-135">El formulario está en estado HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="d172c-135">The form is in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="d172c-136">Libere el mensaje actual y reemplácela por el mensaje al que apunta el _parámetro pMessage._</span><span class="sxs-lookup"><span data-stu-id="d172c-136">Release the current message and replace it with the message pointed to by the  _pMessage_ parameter.</span></span> <span data-ttu-id="d172c-137">Llame al método [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) del mensaje de reemplazo y devuelva S_OK.</span><span class="sxs-lookup"><span data-stu-id="d172c-137">Call the replacement message's [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="d172c-138">El formulario está en estado HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="d172c-138">The form is in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="d172c-139">Llame al **método IMAPIViewAdviseSink::OnSaved** de todos los visores registrados, marque el formulario como limpio y devuelva S_OK.</span><span class="sxs-lookup"><span data-stu-id="d172c-139">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="d172c-140">El formulario está en estado [NoScribable.](noscribble-state.md)</span><span class="sxs-lookup"><span data-stu-id="d172c-140">The form is in the [NoScribble](noscribble-state.md) state.</span></span>  <br/> |<span data-ttu-id="d172c-141">Libere el mensaje actual y reemplácela por el mensaje que apunta  _pMessage_.</span><span class="sxs-lookup"><span data-stu-id="d172c-141">Release the current message and replace it with the message pointed to by  _pMessage_.</span></span> <span data-ttu-id="d172c-142">Llame al método **IUnknown::AddRef** del mensaje de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="d172c-142">Call the replacement message's **IUnknown::AddRef** method.</span></span> <span data-ttu-id="d172c-143">Llame al **método IMAPIViewAdviseSink::OnSaved** de todos los visores registrados, marque el formulario como limpio y devuelva S_OK.</span><span class="sxs-lookup"><span data-stu-id="d172c-143">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="d172c-144">El formulario se encuentra en uno de los estados HandsOff y el  _parámetro pMessage_ se establece en NULL.</span><span class="sxs-lookup"><span data-stu-id="d172c-144">The form is in one of the HandsOff states and the  _pMessage_ parameter is set to NULL.</span></span>  <br/> |<span data-ttu-id="d172c-145">Devuelve E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="d172c-145">Return E_INVALIDARG.</span></span>  <br/> |
|<span data-ttu-id="d172c-146">El formulario está en un estado distinto de uno de los estados HandsOff o NoScribble.</span><span class="sxs-lookup"><span data-stu-id="d172c-146">The form is in a state other than one of the HandsOff states or the NoScribble state.</span></span>  <br/> |<span data-ttu-id="d172c-147">Devuelve E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="d172c-147">Return E_UNEXPECTED.</span></span>  <br/> |
   
<span data-ttu-id="d172c-148">Para obtener más información acerca de cómo guardar objetos de almacenamiento, vea la documentación de los [métodos IPersistStorage::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) o [IPersistFile::SaveCompleted.](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted)</span><span class="sxs-lookup"><span data-stu-id="d172c-148">For more information about saving storage objects, see the documentation for the [IPersistStorage::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) or [IPersistFile::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d172c-149">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d172c-149">See also</span></span>

- [<span data-ttu-id="d172c-150">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d172c-150">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
- [<span data-ttu-id="d172c-151">Estados de formulario</span><span class="sxs-lookup"><span data-stu-id="d172c-151">Form States</span></span>](form-states.md)
