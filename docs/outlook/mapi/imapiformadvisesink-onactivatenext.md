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
# <a name="imapiformadvisesinkonactivatenext"></a><span data-ttu-id="892ce-103">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="892ce-103">IMAPIFormAdviseSink::OnActivateNext</span></span>

  
  
<span data-ttu-id="892ce-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="892ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="892ce-105">Indica si el formulario puede controlar la clase de mensaje del siguiente mensaje que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="892ce-105">Indicates whether the form can handle the message class of the next message to display.</span></span>
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a><span data-ttu-id="892ce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="892ce-106">Parameters</span></span>

 <span data-ttu-id="892ce-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="892ce-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="892ce-108">[entrada] Puntero a la clase de mensaje del siguiente mensaje.</span><span class="sxs-lookup"><span data-stu-id="892ce-108">[in] A pointer to the message class of the next message.</span></span>
    
 <span data-ttu-id="892ce-109">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="892ce-109">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="892ce-110">[entrada] Máscara de bits de marcas definidas por el cliente o definidas por el proveedor, copiadas de la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) del siguiente mensaje que se va a mostrar, que proporciona información de estado sobre la tabla de contenido en la que se incluye el mensaje.</span><span class="sxs-lookup"><span data-stu-id="892ce-110">[in] A bitmask of client-defined or provider-defined flags, copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the next message to display, that provides status information regarding the contents table that the message is included in.</span></span>
    
 <span data-ttu-id="892ce-111">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="892ce-111">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="892ce-112">[entrada] Puntero a una máscara de bits de marcas copiadas de la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del siguiente mensaje para mostrar que indica el estado actual del mensaje.</span><span class="sxs-lookup"><span data-stu-id="892ce-112">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the next message to display that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="892ce-113">_ppPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="892ce-113">_ppPersistMessage_</span></span>
  
> <span data-ttu-id="892ce-114">[salida] Puntero a un puntero a la implementación [de IPersistMessage](ipersistmessageiunknown.md) para el objeto de formulario usado para el nuevo formulario, si es necesario un nuevo formulario.</span><span class="sxs-lookup"><span data-stu-id="892ce-114">[out] A pointer to a pointer to the [IPersistMessage](ipersistmessageiunknown.md) implementation for the form object used for the new form, if a new form is required.</span></span> <span data-ttu-id="892ce-115">Se puede devolver un puntero a NULL si se puede usar el objeto de formulario actual para mostrar y guardar el siguiente mensaje.</span><span class="sxs-lookup"><span data-stu-id="892ce-115">A pointer to NULL can be returned if the current form object can be used to display and save the next message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="892ce-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="892ce-116">Return value</span></span>

<span data-ttu-id="892ce-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="892ce-117">S_OK</span></span> 
  
> <span data-ttu-id="892ce-118">La notificación se ha realizado correctamente y el formulario puede controlar el siguiente mensaje.</span><span class="sxs-lookup"><span data-stu-id="892ce-118">The notification was successful and the form can handle the next message.</span></span>
    
<span data-ttu-id="892ce-119">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="892ce-119">S_FALSE</span></span> 
  
> <span data-ttu-id="892ce-120">El formulario no controla la clase de mensaje del siguiente mensaje.</span><span class="sxs-lookup"><span data-stu-id="892ce-120">The form does not handle the message class of the next message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="892ce-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="892ce-121">Remarks</span></span>

<span data-ttu-id="892ce-122">Los visores de formularios llaman al método **IMAPIFormAdviseSink::OnActivateNext** para ayudar al formulario a determinar si puede mostrar el siguiente mensaje en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="892ce-122">Form viewers call the **IMAPIFormAdviseSink::OnActivateNext** method to help the form determine whether it can display the next message in a folder.</span></span> <span data-ttu-id="892ce-123">El siguiente mensaje podría ser un mensaje de cualquier clase, pero normalmente es de la misma clase o una clase relacionada.</span><span class="sxs-lookup"><span data-stu-id="892ce-123">The next message could be a message of any class, but typically it is of the same class or a related class.</span></span> <span data-ttu-id="892ce-124">Esto hace que el proceso de lectura de varios mensajes de la misma clase sea más eficaz al permitir que las aplicaciones cliente reutilicen objetos de formulario siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="892ce-124">This makes the process of reading multiple messages of the same class more efficient by enabling client applications to reuse form objects whenever possible.</span></span> 
  
<span data-ttu-id="892ce-125">La mayoría de los objetos de formulario usarán la clase de mensaje a la que apunta el parámetro  _lpszMessageClass_ para determinar si pueden controlar el siguiente mensaje.</span><span class="sxs-lookup"><span data-stu-id="892ce-125">Most form objects will use the message class pointed to by the  _lpszMessageClass_ parameter to determine whether they can handle the next message.</span></span> <span data-ttu-id="892ce-126">Normalmente, un formulario puede controlar mensajes que pertenecen a clases de las que la clase predeterminada del formulario es una subclase, además de los mensajes que pertenecen a la clase predeterminada.</span><span class="sxs-lookup"><span data-stu-id="892ce-126">Usually a form can handle messages that belong to classes of which the form's default class is a subclass, in addition to messages that belong to the default class.</span></span> <span data-ttu-id="892ce-127">Sin embargo, un formulario puede usar otros factores para determinar sin duda si se puede controlar un mensaje, como el estado enviado o no enviado del siguiente mensaje.</span><span class="sxs-lookup"><span data-stu-id="892ce-127">However, a form can use other factors to determine without question whether a message can be handled, such as the sent or unsent status of the next message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="892ce-128">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="892ce-128">Notes to implementers</span></span>

<span data-ttu-id="892ce-129">Devuelve S_OK y NULL en el  _parámetro ppPersistMessage_ si el formulario puede controlar la clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="892ce-129">Return S_OK and NULL in the  _ppPersistMessage_ parameter if the form can handle the message class.</span></span> <span data-ttu-id="892ce-130">Si el formulario puede crear un formulario nuevo que pueda controlar el mensaje que el formulario no puede controlar, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="892ce-130">If the form can create a new form that can handle the message that the form is unable to handle, follow these steps:</span></span> 
  
1. <span data-ttu-id="892ce-131">Llame a la fábrica de clases del formulario para crear una instancia de un nuevo objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="892ce-131">Call your form's class factory to create an instance of a new form object.</span></span>
    
2. <span data-ttu-id="892ce-132">Almacene esa instancia en el contenido del parámetro de puntero _ppPersistMessage._</span><span class="sxs-lookup"><span data-stu-id="892ce-132">Store that instance in the contents of the  _ppPersistMessage_ pointer parameter.</span></span> 
    
3. <span data-ttu-id="892ce-133">Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="892ce-133">Return S_OK.</span></span>
    
<span data-ttu-id="892ce-134">El visor de formularios cargará el mensaje mediante el método [IPersistMessage::Load](ipersistmessage-load.md) que pertenece al objeto al que apunta  _ppPersistMessage_.</span><span class="sxs-lookup"><span data-stu-id="892ce-134">The form viewer will load the message by using the [IPersistMessage::Load](ipersistmessage-load.md) method that belongs to the object pointed to by  _ppPersistMessage_.</span></span>
  
<span data-ttu-id="892ce-135">Si ni el formulario ni el formulario que puede crear pueden controlar el siguiente mensaje, S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="892ce-135">If neither the form nor a form that you can create can handle the next message, return S_FALSE.</span></span> <span data-ttu-id="892ce-136">Sin embargo, en general, los formularios no deben devolver este valor porque provoca una disminución del rendimiento en el visor de formularios.</span><span class="sxs-lookup"><span data-stu-id="892ce-136">However, in general, forms should not return this value because it causes decreased performance in the form viewer.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="892ce-137">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="892ce-137">MFCMAPI reference</span></span>

<span data-ttu-id="892ce-138">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="892ce-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="892ce-139">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="892ce-139">**File**</span></span>|<span data-ttu-id="892ce-140">**Función**</span><span class="sxs-lookup"><span data-stu-id="892ce-140">**Function**</span></span>|<span data-ttu-id="892ce-141">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="892ce-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="892ce-142">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="892ce-142">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="892ce-143">CMyMAPIFormViewer::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="892ce-143">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="892ce-144">MFCMAPI usa el método **IMAPIFormAdviseSink::OnActivateNext** para implementar el método [IMAPIViewContext::ActivateNext.](imapiviewcontext-activatenext.md)</span><span class="sxs-lookup"><span data-stu-id="892ce-144">MFCMAPI uses the **IMAPIFormAdviseSink::OnActivateNext** method to implement the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="892ce-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="892ce-145">See also</span></span>



[<span data-ttu-id="892ce-146">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="892ce-146">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="892ce-147">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="892ce-147">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="892ce-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="892ce-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="892ce-149">Propiedad canónica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="892ce-149">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="892ce-150">Propiedad canónica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="892ce-150">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="892ce-151">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="892ce-151">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)


[<span data-ttu-id="892ce-152">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="892ce-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

