---
title: IPersistMessageLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Load
api_type:
- COM
ms.assetid: bd4646d2-8229-499d-91aa-3cbec72b9445
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 5024c2f8b88b54051e4b8400f4b3f14374b10c23
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317132"
---
# <a name="ipersistmessageload"></a><span data-ttu-id="782ae-103">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="782ae-103">IPersistMessage::Load</span></span>

  
  
<span data-ttu-id="782ae-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="782ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="782ae-105">Carga el formulario para un mensaje especificado.</span><span class="sxs-lookup"><span data-stu-id="782ae-105">Loads the form for a specified message.</span></span>
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a><span data-ttu-id="782ae-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="782ae-106">Parameters</span></span>

 <span data-ttu-id="782ae-107">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="782ae-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="782ae-108">[entrada] Puntero al sitio del mensaje para el formulario que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="782ae-108">[in] A pointer to the message site for the form to be loaded.</span></span>
    
 <span data-ttu-id="782ae-109">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="782ae-109">_pMessage_</span></span>
  
> <span data-ttu-id="782ae-110">[entrada] Puntero al mensaje para el que se debe cargar el formulario.</span><span class="sxs-lookup"><span data-stu-id="782ae-110">[in] A pointer to the message for which the form should be loaded.</span></span>
    
 <span data-ttu-id="782ae-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="782ae-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="782ae-112">[entrada] Máscara de bits de marcas definidas por el cliente o definidas por el proveedor, copiadas de la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) del mensaje, que proporcionan información sobre el estado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="782ae-112">[in] A bitmask of client-defined or provider-defined flags, copied from the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property, that provide information about the state of the message.</span></span>
    
 <span data-ttu-id="782ae-113">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="782ae-113">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="782ae-114">[entrada] Máscara de bits de marcas, copiada de la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje, que proporcionan más información sobre el estado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="782ae-114">[in] A bitmask of flags, copied from the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property, that provide further information about the state of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="782ae-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="782ae-115">Return value</span></span>

<span data-ttu-id="782ae-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="782ae-116">S_OK</span></span> 
  
> <span data-ttu-id="782ae-117">El formulario se cargó correctamente.</span><span class="sxs-lookup"><span data-stu-id="782ae-117">The form was successfully loaded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="782ae-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="782ae-118">Remarks</span></span>

<span data-ttu-id="782ae-119">Los visores de formularios llaman al **método IPersistMessage::Load** para cargar un formulario para un mensaje existente.</span><span class="sxs-lookup"><span data-stu-id="782ae-119">Form viewers call the **IPersistMessage::Load** method to load a form for an existing message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="782ae-120">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="782ae-120">Notes to implementers</span></span>

 <span data-ttu-id="782ae-121">**Sólo** se llama a Load cuando un formulario se encuentra en uno de los siguientes estados:</span><span class="sxs-lookup"><span data-stu-id="782ae-121">**Load** is called only when a form is in one of the following states:</span></span> 
  
- [<span data-ttu-id="782ae-122">Sin inicializar</span><span class="sxs-lookup"><span data-stu-id="782ae-122">Uninitialized</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="782ae-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="782ae-123">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="782ae-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="782ae-124">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="782ae-125">Si un visor de formulario llama **a Load** mientras el formulario está en cualquier otro estado, el método devuelve E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="782ae-125">If a form viewer calls **Load** while the form is in any other state, the method returns E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="782ae-126">Si el formulario tiene una referencia a un sitio de mensajes activo distinto del que se pasa a **Load**, libere el sitio original porque ya no se usará.</span><span class="sxs-lookup"><span data-stu-id="782ae-126">If your form has a reference to an active message site other than the one that is passed into **Load**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="782ae-127">Almacene los punteros al sitio y al mensaje del mensaje desde los parámetros  _pMessageSite_ y  _pMessage,_ y llame a los métodos [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) de ambos objetos para incrementar sus recuentos de referencia.</span><span class="sxs-lookup"><span data-stu-id="782ae-127">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="782ae-128">Una **vez completado AddRef,** almacene las propiedades de los parámetros  _ulMessageStatus_ y  _ulMessageFlags_ en el formulario.</span><span class="sxs-lookup"><span data-stu-id="782ae-128">After **AddRef** has completed, store the properties from the  _ulMessageStatus_ and  _ulMessageFlags_ parameters into the form.</span></span> <span data-ttu-id="782ae-129">Haga la transición del formulario a su estado [Normal](normal-state.md) antes de mostrarlo y notifique a los visores registrados llamando a sus métodos [IMAPIViewAdviseSink::OnNewMessage.](imapiviewadvisesink-onnewmessage.md)</span><span class="sxs-lookup"><span data-stu-id="782ae-129">Transition the form to its [Normal](normal-state.md) state before displaying it, and notify registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods.</span></span> 
  
<span data-ttu-id="782ae-130">Si no se produce ningún error, devuelva S_OK.</span><span class="sxs-lookup"><span data-stu-id="782ae-130">If no errors occur, return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="782ae-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="782ae-131">See also</span></span>



[<span data-ttu-id="782ae-132">Propiedad canónica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="782ae-132">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="782ae-133">Propiedad canónica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="782ae-133">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="782ae-134">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="782ae-134">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="782ae-135">Estado no inicializado</span><span class="sxs-lookup"><span data-stu-id="782ae-135">Uninitialized State</span></span>](uninitialized-state.md)
  
[<span data-ttu-id="782ae-136">Estado HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="782ae-136">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
  
[<span data-ttu-id="782ae-137">Estado HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="782ae-137">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
  
[<span data-ttu-id="782ae-138">Estados de formulario</span><span class="sxs-lookup"><span data-stu-id="782ae-138">Form States</span></span>](form-states.md)


[<span data-ttu-id="782ae-139">IPersistStorage::Load</span><span class="sxs-lookup"><span data-stu-id="782ae-139">IPersistStorage::Load</span></span>](https://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[<span data-ttu-id="782ae-140">IPersistStream::Load</span><span class="sxs-lookup"><span data-stu-id="782ae-140">IPersistStream::Load</span></span>](https://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[<span data-ttu-id="782ae-141">IPersistFile::Load</span><span class="sxs-lookup"><span data-stu-id="782ae-141">IPersistFile::Load</span></span>](https://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

