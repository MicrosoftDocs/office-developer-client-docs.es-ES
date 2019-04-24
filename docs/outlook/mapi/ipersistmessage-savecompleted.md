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
# <a name="ipersistmessagesavecompleted"></a><span data-ttu-id="fb627-103">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="fb627-103">IPersistMessage::SaveCompleted</span></span>

<span data-ttu-id="fb627-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb627-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb627-105">Notifica al formulario que se ha completado una operación de guardado.</span><span class="sxs-lookup"><span data-stu-id="fb627-105">Notifies the form that a save operation has been completed.</span></span> 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="fb627-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="fb627-106">Parameters</span></span>

<span data-ttu-id="fb627-107">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="fb627-107">_pMessage_</span></span>
  
> <span data-ttu-id="fb627-108">a Un puntero al mensaje que acaba de guardar.</span><span class="sxs-lookup"><span data-stu-id="fb627-108">[in] A pointer to the newly saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fb627-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb627-109">Return value</span></span>

<span data-ttu-id="fb627-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="fb627-110">S_OK</span></span> 
  
> <span data-ttu-id="fb627-111">La notificación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="fb627-111">The notification was successful.</span></span>
    
<span data-ttu-id="fb627-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="fb627-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="fb627-113">El parámetro _pMessage_ es NULL y el formulario está en el estado [HandsOffFromNormal](handsofffromnormal-state.md) o [HandsOffAfterSave](handsoffaftersave-state.md) .</span><span class="sxs-lookup"><span data-stu-id="fb627-113">The  _pMessage_ parameter is NULL and the form is either in the [HandsOffFromNormal](handsofffromnormal-state.md) or [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> 
    
<span data-ttu-id="fb627-114">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="fb627-114">E_UNEXPECTED</span></span> 
  
> <span data-ttu-id="fb627-115">El formulario no está en uno de los siguientes Estados:</span><span class="sxs-lookup"><span data-stu-id="fb627-115">The form is not in one of the following states:</span></span>
    
   - <span data-ttu-id="fb627-116">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="fb627-116">HandsOffFromNormal</span></span>
    
   - <span data-ttu-id="fb627-117">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="fb627-117">HandsOffAfterSave</span></span>
    
   - [<span data-ttu-id="fb627-118">NoScribble</span><span class="sxs-lookup"><span data-stu-id="fb627-118">NoScribble</span></span>](noscribble-state.md)
    
## <a name="remarks"></a><span data-ttu-id="fb627-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fb627-119">Remarks</span></span>

<span data-ttu-id="fb627-120">Un visor de formularios llama al método **IPersistMessage:: SaveCompleted** para notificar al formulario que se han guardado todos los cambios pendientes.</span><span class="sxs-lookup"><span data-stu-id="fb627-120">The **IPersistMessage::SaveCompleted** method is called by a form viewer to notify the form that all pending changes have been saved.</span></span> <span data-ttu-id="fb627-121">**SaveCompleted** solo se debe llamar cuando el formulario está en uno de los siguientes Estados:</span><span class="sxs-lookup"><span data-stu-id="fb627-121">**SaveCompleted** should be called only when the form is in one of the following states:</span></span> 
  
- <span data-ttu-id="fb627-122">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="fb627-122">HandsOffFromNormal</span></span>
    
- <span data-ttu-id="fb627-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="fb627-123">HandsOffAfterSave</span></span>
    
- <span data-ttu-id="fb627-124">NoScribble</span><span class="sxs-lookup"><span data-stu-id="fb627-124">NoScribble</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="fb627-125">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="fb627-125">Notes to implementers</span></span>

<span data-ttu-id="fb627-126">Hay varias acciones posibles que puede realizar el método **SaveCompleted** , en función de lo que contenga el parámetro de puntero de mensaje y el estado en el que se encuentra el mensaje.</span><span class="sxs-lookup"><span data-stu-id="fb627-126">There are several possible actions that the **SaveCompleted** method can perform, depending on what the message pointer parameter contains, and what state the message is in.</span></span> <span data-ttu-id="fb627-127">Sin embargo, cuando una acción se realiza correctamente, guarde siempre el estado actual del mensaje al que apunta el parámetro _pMessage_ y cambie el formulario a su estado [normal](normal-state.md) .</span><span class="sxs-lookup"><span data-stu-id="fb627-127">However, when an action is successful, always save the current state of the message that the  _pMessage_ parameter points to and transition the form to its [Normal](normal-state.md) state.</span></span> 
  
<span data-ttu-id="fb627-128">En la tabla siguiente se describen las condiciones que afectan a las acciones que debe realizar en la implementación de **SaveCompleted**.</span><span class="sxs-lookup"><span data-stu-id="fb627-128">The following table describes the conditions that affect the actions you should take in your implementation of **SaveCompleted**.</span></span>
  
|<span data-ttu-id="fb627-129">**Condición**</span><span class="sxs-lookup"><span data-stu-id="fb627-129">**Condition**</span></span>|<span data-ttu-id="fb627-130">**Acción**</span><span class="sxs-lookup"><span data-stu-id="fb627-130">**Action**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fb627-131">El parámetro _pMessage_ es NULL y el parámetro _FSameAsLoad_ del método [IPersistMessage:: Save](ipersistmessage-save.md) está establecido en true.</span><span class="sxs-lookup"><span data-stu-id="fb627-131">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the [IPersistMessage::Save](ipersistmessage-save.md) method is set to TRUE.</span></span>  <br/> |<span data-ttu-id="fb627-132">Llame al método [IMAPIViewAdviseSink:: onSave](imapiviewadvisesink-onsaved.md) de todos los visores registrados, marque el formulario como limpio y devuelva S_OK.</span><span class="sxs-lookup"><span data-stu-id="fb627-132">Call the [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="fb627-133">El parámetro _pMessage_ es NULL y el parámetro _FSameAsLoad_ del método **IPersistMessage:: Save** está establecido en false.</span><span class="sxs-lookup"><span data-stu-id="fb627-133">The  _pMessage_ parameter is NULL and the  _fSameAsLoad_ parameter of the **IPersistMessage::Save** method is set to FALSE.</span></span>  <br/> |<span data-ttu-id="fb627-134">Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="fb627-134">Return S_OK.</span></span>  <br/> |
|<span data-ttu-id="fb627-135">El formulario está en estado HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="fb627-135">The form is in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="fb627-136">Libere el mensaje actual y reemplácelo por el mensaje al que señala el parámetro _pMessage_ .</span><span class="sxs-lookup"><span data-stu-id="fb627-136">Release the current message and replace it with the message pointed to by the  _pMessage_ parameter.</span></span> <span data-ttu-id="fb627-137">Llame al método [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) del mensaje de reemplazo y devuelva S_OK.</span><span class="sxs-lookup"><span data-stu-id="fb627-137">Call the replacement message's [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="fb627-138">El formulario está en estado HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="fb627-138">The form is in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="fb627-139">Llame al método **IMAPIViewAdviseSink:: onSave** de todos los visores registrados, marque el formulario como limpio y devuelva S_OK.</span><span class="sxs-lookup"><span data-stu-id="fb627-139">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="fb627-140">El formulario está en estado [noscribble](noscribble-state.md) .</span><span class="sxs-lookup"><span data-stu-id="fb627-140">The form is in the [NoScribble](noscribble-state.md) state.</span></span>  <br/> |<span data-ttu-id="fb627-141">Libere el mensaje actual y reemplácelo por el mensaje al que se apunta por _pMessage_.</span><span class="sxs-lookup"><span data-stu-id="fb627-141">Release the current message and replace it with the message pointed to by  _pMessage_.</span></span> <span data-ttu-id="fb627-142">Llame al método **IUnknown:: AddRef** del mensaje de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="fb627-142">Call the replacement message's **IUnknown::AddRef** method.</span></span> <span data-ttu-id="fb627-143">Llame al método **IMAPIViewAdviseSink:: onSave** de todos los visores registrados, marque el formulario como limpio y devuelva S_OK.</span><span class="sxs-lookup"><span data-stu-id="fb627-143">Call the **IMAPIViewAdviseSink::OnSaved** method of all registered viewers, mark the form as clean, and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="fb627-144">El formulario está en uno de los Estados HandsOff y el parámetro _pMessage_ se establece en NULL.</span><span class="sxs-lookup"><span data-stu-id="fb627-144">The form is in one of the HandsOff states and the  _pMessage_ parameter is set to NULL.</span></span>  <br/> |<span data-ttu-id="fb627-145">Devuelve E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="fb627-145">Return E_INVALIDARG.</span></span>  <br/> |
|<span data-ttu-id="fb627-146">El formulario está en un estado que no es ninguno de los Estados HandsOff o el estado noScribble.</span><span class="sxs-lookup"><span data-stu-id="fb627-146">The form is in a state other than one of the HandsOff states or the NoScribble state.</span></span>  <br/> |<span data-ttu-id="fb627-147">Devuelve E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="fb627-147">Return E_UNEXPECTED.</span></span>  <br/> |
   
<span data-ttu-id="fb627-148">Para obtener más información sobre cómo guardar objetos de almacenamiento, consulte la documentación de los métodos [IPersistStorage:: SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) o [IPersistFile:: SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) .</span><span class="sxs-lookup"><span data-stu-id="fb627-148">For more information about saving storage objects, see the documentation for the [IPersistStorage::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) or [IPersistFile::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fb627-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb627-149">See also</span></span>

- [<span data-ttu-id="fb627-150">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fb627-150">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
- [<span data-ttu-id="fb627-151">Estados de formulario</span><span class="sxs-lookup"><span data-stu-id="fb627-151">Form States</span></span>](form-states.md)
