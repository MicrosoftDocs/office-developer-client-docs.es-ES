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
ms.openlocfilehash: eff192b0d2b5cde51a2909452b19ffe1a47b2c04
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817868"
---
# <a name="ipersistmessageload"></a><span data-ttu-id="61f47-103">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="61f47-103">IPersistMessage::Load</span></span>

  
  
<span data-ttu-id="61f47-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="61f47-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="61f47-105">Carga el formulario para un mensaje especificado.</span><span class="sxs-lookup"><span data-stu-id="61f47-105">Loads the form for a specified message.</span></span>
  
```cpp
HRESULT Load(
  LPMESSAGESITE pMessageSite,
  LPMESSAGE pMessage,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags
);
```

## <a name="parameters"></a><span data-ttu-id="61f47-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61f47-106">Parameters</span></span>

 <span data-ttu-id="61f47-107">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="61f47-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="61f47-108">[entrada] Un puntero al sitio de mensaje del formulario al que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="61f47-108">[in] A pointer to the message site for the form to be loaded.</span></span>
    
 <span data-ttu-id="61f47-109">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="61f47-109">_pMessage_</span></span>
  
> <span data-ttu-id="61f47-110">[entrada] Un puntero al mensaje para el que se debe cargar el formulario.</span><span class="sxs-lookup"><span data-stu-id="61f47-110">[in] A pointer to the message for which the form should be loaded.</span></span>
    
 <span data-ttu-id="61f47-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="61f47-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="61f47-112">[entrada] Una máscara de bits de indicadores definidas por el cliente o definidas por el proveedor, copiada desde la propiedad del mensaje **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)), que proporcionan información sobre el estado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="61f47-112">[in] A bitmask of client-defined or provider-defined flags, copied from the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property, that provide information about the state of the message.</span></span>
    
 <span data-ttu-id="61f47-113">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="61f47-113">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="61f47-114">[entrada] Una máscara de bits de indicadores, que se copió desde la propiedad del mensaje **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)), que proporcionar más información sobre el estado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="61f47-114">[in] A bitmask of flags, copied from the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property, that provide further information about the state of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="61f47-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61f47-115">Return value</span></span>

<span data-ttu-id="61f47-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="61f47-116">S_OK</span></span> 
  
> <span data-ttu-id="61f47-117">El formulario se cargó correctamente.</span><span class="sxs-lookup"><span data-stu-id="61f47-117">The form was successfully loaded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="61f47-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="61f47-118">Remarks</span></span>

<span data-ttu-id="61f47-119">Visores de formulario llamar al método **IPersistMessage::Load** para cargar un formulario para un mensaje existente.</span><span class="sxs-lookup"><span data-stu-id="61f47-119">Form viewers call the **IPersistMessage::Load** method to load a form for an existing message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="61f47-120">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="61f47-120">Notes to implementers</span></span>

 <span data-ttu-id="61f47-121">**Carga** sólo se llama cuando un formulario está en uno de los siguientes estados:</span><span class="sxs-lookup"><span data-stu-id="61f47-121">**Load** is called only when a form is in one of the following states:</span></span> 
  
- [<span data-ttu-id="61f47-122">No inicializado</span><span class="sxs-lookup"><span data-stu-id="61f47-122">Uninitialized</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="61f47-123">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="61f47-123">HandsOffAfterSave</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="61f47-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="61f47-124">HandsOffFromNormal</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="61f47-125">Si un visor de formulario llama **carga** mientras el formulario está en cualquier otro estado, el método devuelve E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="61f47-125">If a form viewer calls **Load** while the form is in any other state, the method returns E_UNEXPECTED.</span></span> 
  
<span data-ttu-id="61f47-126">Si el formulario tiene una referencia a un sitio de mensaje activo distinto del que se pasó a la **carga**, la versión del sitio original debido a que ya no se usará.</span><span class="sxs-lookup"><span data-stu-id="61f47-126">If your form has a reference to an active message site other than the one that is passed into **Load**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="61f47-127">Almacenar los punteros para el sitio de mensaje y el mensaje de los parámetros _pMessageSite_ y _pMessage_ y llamar a métodos de [IUnknown:: AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) de ambos objetos para incrementar sus recuentos de referencia.</span><span class="sxs-lookup"><span data-stu-id="61f47-127">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="61f47-128">Una vez haya finalizado **AddRef** , almacenar las propiedades de los parámetros _ulMessageStatus_ y _ulMessageFlags_ en el formulario.</span><span class="sxs-lookup"><span data-stu-id="61f47-128">After **AddRef** has completed, store the properties from the  _ulMessageStatus_ and  _ulMessageFlags_ parameters into the form.</span></span> <span data-ttu-id="61f47-129">Realizar la transición del formulario a su estado [Normal](normal-state.md) antes de mostrarla y notificar a los visores registrados llamando a sus métodos [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="61f47-129">Transition the form to its [Normal](normal-state.md) state before displaying it, and notify registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods.</span></span> 
  
<span data-ttu-id="61f47-130">Si no se producen errores, devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="61f47-130">If no errors occur, return S_OK.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="61f47-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="61f47-131">See also</span></span>



[<span data-ttu-id="61f47-132">Propiedad canónica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="61f47-132">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="61f47-133">Propiedad canónica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="61f47-133">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="61f47-134">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="61f47-134">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)


[<span data-ttu-id="61f47-135">Estado sin inicializar</span><span class="sxs-lookup"><span data-stu-id="61f47-135">Uninitialized State</span></span>](uninitialized-state.md)
  
[<span data-ttu-id="61f47-136">Estado HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="61f47-136">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
  
[<span data-ttu-id="61f47-137">Estado HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="61f47-137">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
  
[<span data-ttu-id="61f47-138">Estados de formulario</span><span class="sxs-lookup"><span data-stu-id="61f47-138">Form States</span></span>](form-states.md)


[<span data-ttu-id="61f47-139">IPersistStorage:: Load</span><span class="sxs-lookup"><span data-stu-id="61f47-139">IPersistStorage::Load</span></span>](http://msdn.microsoft.com/library/34379b8d-4e00-49cd-9fd1-65f88746c61a.aspx)
  
[<span data-ttu-id="61f47-140">IPersistStream:: Load</span><span class="sxs-lookup"><span data-stu-id="61f47-140">IPersistStream::Load</span></span>](http://msdn.microsoft.com/library/351e1187-9959-4542-8778-925457c3b8e3.aspx)
  
[<span data-ttu-id="61f47-141">IPersistFile:: Load</span><span class="sxs-lookup"><span data-stu-id="61f47-141">IPersistFile::Load</span></span>](http://msdn.microsoft.com/library/8391aa5c-fe6e-4b03-9eef-7958f75910a5.aspx)

