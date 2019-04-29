---
title: IMAPIFormAdviseSinkOnActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnActivateNext
api_type:
- COM
ms.assetid: db621dfd-c6ad-42d2-8089-db40a63cab36
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d647b41018afbade91dffb2818b48b0738148855
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411767"
---
# <a name="imapiformadvisesinkonactivatenext"></a><span data-ttu-id="38dc1-103">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="38dc1-103">IMAPIFormAdviseSink::OnActivateNext</span></span>

  
  
<span data-ttu-id="38dc1-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38dc1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38dc1-105">Indica si el formulario puede controlar la clase de mensaje del siguiente mensaje que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="38dc1-105">Indicates whether the form can handle the message class of the next message to display.</span></span>
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a><span data-ttu-id="38dc1-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="38dc1-106">Parameters</span></span>

 <span data-ttu-id="38dc1-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="38dc1-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="38dc1-108">a Un puntero a la clase de mensaje del siguiente mensaje.</span><span class="sxs-lookup"><span data-stu-id="38dc1-108">[in] A pointer to the message class of the next message.</span></span>
    
 <span data-ttu-id="38dc1-109">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="38dc1-109">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="38dc1-110">a Una máscara de bits de indicadores definidos por el cliente o definidos por el proveedor, copiado de la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) del siguiente mensaje que se va a mostrar, que proporciona información de estado relativa a la tabla de contenido en la que se incluye el mensaje. a.</span><span class="sxs-lookup"><span data-stu-id="38dc1-110">[in] A bitmask of client-defined or provider-defined flags, copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the next message to display, that provides status information regarding the contents table that the message is included in.</span></span>
    
 <span data-ttu-id="38dc1-111">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="38dc1-111">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="38dc1-112">a Un puntero a una máscara de máscara de marcas copiadas de la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del siguiente mensaje para mostrar que indica el estado actual del mensaje.</span><span class="sxs-lookup"><span data-stu-id="38dc1-112">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the next message to display that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="38dc1-113">_ppPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="38dc1-113">_ppPersistMessage_</span></span>
  
> <span data-ttu-id="38dc1-114">contempla Un puntero a un puntero a la implementación de [IPersistMessage](ipersistmessageiunknown.md) para el objeto de formulario usado para el nuevo formulario, si se requiere un nuevo formulario.</span><span class="sxs-lookup"><span data-stu-id="38dc1-114">[out] A pointer to a pointer to the [IPersistMessage](ipersistmessageiunknown.md) implementation for the form object used for the new form, if a new form is required.</span></span> <span data-ttu-id="38dc1-115">Se puede devolver un puntero a NULL si el objeto Form actual puede usarse para mostrar y guardar el siguiente mensaje.</span><span class="sxs-lookup"><span data-stu-id="38dc1-115">A pointer to NULL can be returned if the current form object can be used to display and save the next message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="38dc1-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="38dc1-116">Return value</span></span>

<span data-ttu-id="38dc1-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="38dc1-117">S_OK</span></span> 
  
> <span data-ttu-id="38dc1-118">La notificación se ha realizado correctamente y el formulario puede controlar el siguiente mensaje.</span><span class="sxs-lookup"><span data-stu-id="38dc1-118">The notification was successful and the form can handle the next message.</span></span>
    
<span data-ttu-id="38dc1-119">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="38dc1-119">S_FALSE</span></span> 
  
> <span data-ttu-id="38dc1-120">El formulario no controla la clase de mensaje del siguiente mensaje.</span><span class="sxs-lookup"><span data-stu-id="38dc1-120">The form does not handle the message class of the next message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="38dc1-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="38dc1-121">Remarks</span></span>

<span data-ttu-id="38dc1-122">Los visores de formularios llaman al método **IMAPIFormAdviseSink:: OnActivateNext** para ayudar a que el formulario determine si puede mostrar el siguiente mensaje en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="38dc1-122">Form viewers call the **IMAPIFormAdviseSink::OnActivateNext** method to help the form determine whether it can display the next message in a folder.</span></span> <span data-ttu-id="38dc1-123">El siguiente mensaje puede ser un mensaje de cualquier clase, pero suele ser de la misma clase o de una clase relacionada.</span><span class="sxs-lookup"><span data-stu-id="38dc1-123">The next message could be a message of any class, but typically it is of the same class or a related class.</span></span> <span data-ttu-id="38dc1-124">Esto hace que el proceso de lectura de varios mensajes de la misma clase sea más eficaz al permitir a las aplicaciones cliente volver a usar objetos de formulario siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="38dc1-124">This makes the process of reading multiple messages of the same class more efficient by enabling client applications to reuse form objects whenever possible.</span></span> 
  
<span data-ttu-id="38dc1-125">La mayoría de los objetos de formulario usarán la clase de mensaje señalada por el parámetro _lpszMessageClass_ para determinar si pueden controlar el siguiente mensaje.</span><span class="sxs-lookup"><span data-stu-id="38dc1-125">Most form objects will use the message class pointed to by the  _lpszMessageClass_ parameter to determine whether they can handle the next message.</span></span> <span data-ttu-id="38dc1-126">Normalmente, un formulario puede controlar mensajes que pertenecen a clases de las que la clase predeterminada del formulario es una subclase, además de los mensajes que pertenecen a la clase predeterminada.</span><span class="sxs-lookup"><span data-stu-id="38dc1-126">Usually a form can handle messages that belong to classes of which the form's default class is a subclass, in addition to messages that belong to the default class.</span></span> <span data-ttu-id="38dc1-127">Sin embargo, un formulario puede usar otros factores para determinar sin duda si se puede controlar un mensaje, como el estado enviado o no enviado del siguiente mensaje.</span><span class="sxs-lookup"><span data-stu-id="38dc1-127">However, a form can use other factors to determine without question whether a message can be handled, such as the sent or unsent status of the next message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="38dc1-128">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="38dc1-128">Notes to implementers</span></span>

<span data-ttu-id="38dc1-129">Devuelve S_OK y NULL en el parámetro _ppPersistMessage_ si el formulario puede controlar la clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="38dc1-129">Return S_OK and NULL in the  _ppPersistMessage_ parameter if the form can handle the message class.</span></span> <span data-ttu-id="38dc1-130">Si el formulario puede crear un nuevo formulario que pueda controlar el mensaje que el formulario no puede controlar, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="38dc1-130">If the form can create a new form that can handle the message that the form is unable to handle, follow these steps:</span></span> 
  
1. <span data-ttu-id="38dc1-131">Llame al generador de clases del formulario para crear una instancia de un nuevo objeto Form.</span><span class="sxs-lookup"><span data-stu-id="38dc1-131">Call your form's class factory to create an instance of a new form object.</span></span>
    
2. <span data-ttu-id="38dc1-132">Almacene esa instancia en el contenido del parámetro de puntero _ppPersistMessage_ .</span><span class="sxs-lookup"><span data-stu-id="38dc1-132">Store that instance in the contents of the  _ppPersistMessage_ pointer parameter.</span></span> 
    
3. <span data-ttu-id="38dc1-133">Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="38dc1-133">Return S_OK.</span></span>
    
<span data-ttu-id="38dc1-134">El visor del formulario cargará el mensaje mediante el método [IPersistMessage:: Load](ipersistmessage-load.md) que pertenece al objeto al que apunta _ppPersistMessage_.</span><span class="sxs-lookup"><span data-stu-id="38dc1-134">The form viewer will load the message by using the [IPersistMessage::Load](ipersistmessage-load.md) method that belongs to the object pointed to by  _ppPersistMessage_.</span></span>
  
<span data-ttu-id="38dc1-135">Si ni el formulario ni el formulario que se pueden crear pueden controlar el siguiente mensaje, se devuelve S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="38dc1-135">If neither the form nor a form that you can create can handle the next message, return S_FALSE.</span></span> <span data-ttu-id="38dc1-136">Sin embargo, en general, los formularios no deben devolver este valor porque provoca un rendimiento reducido en el visor de formularios.</span><span class="sxs-lookup"><span data-stu-id="38dc1-136">However, in general, forms should not return this value because it causes decreased performance in the form viewer.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="38dc1-137">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="38dc1-137">MFCMAPI reference</span></span>

<span data-ttu-id="38dc1-138">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="38dc1-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="38dc1-139">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="38dc1-139">**File**</span></span>|<span data-ttu-id="38dc1-140">**Función**</span><span class="sxs-lookup"><span data-stu-id="38dc1-140">**Function**</span></span>|<span data-ttu-id="38dc1-141">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="38dc1-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="38dc1-142">MAPIFormFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="38dc1-142">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="38dc1-143">CMyMAPIFormViewer:: ActivateNext</span><span class="sxs-lookup"><span data-stu-id="38dc1-143">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="38dc1-144">MFCMAPI usa el método **IMAPIFormAdviseSink:: OnActivateNext** para implementar el método [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md) .</span><span class="sxs-lookup"><span data-stu-id="38dc1-144">MFCMAPI uses the **IMAPIFormAdviseSink::OnActivateNext** method to implement the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38dc1-145">Ver también</span><span class="sxs-lookup"><span data-stu-id="38dc1-145">See also</span></span>



[<span data-ttu-id="38dc1-146">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="38dc1-146">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="38dc1-147">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="38dc1-147">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="38dc1-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="38dc1-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="38dc1-149">Propiedad canónica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="38dc1-149">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="38dc1-150">Propiedad canónica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="38dc1-150">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="38dc1-151">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="38dc1-151">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)


[<span data-ttu-id="38dc1-152">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="38dc1-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

