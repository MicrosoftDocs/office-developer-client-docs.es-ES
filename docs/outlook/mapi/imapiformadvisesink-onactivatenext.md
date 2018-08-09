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
ms.openlocfilehash: 3ce4d57ab4837f40ffbc898fde68e44cc802676f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817258"
---
# <a name="imapiformadvisesinkonactivatenext"></a><span data-ttu-id="14cad-103">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="14cad-103">IMAPIFormAdviseSink::OnActivateNext</span></span>

  
  
<span data-ttu-id="14cad-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="14cad-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="14cad-105">Indica si el formulario puede controlar la clase de mensaje del mensaje siguiente para mostrar.</span><span class="sxs-lookup"><span data-stu-id="14cad-105">Indicates whether the form can handle the message class of the next message to display.</span></span>
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a><span data-ttu-id="14cad-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14cad-106">Parameters</span></span>

 <span data-ttu-id="14cad-107">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="14cad-107">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="14cad-108">[entrada] Un puntero a la clase de mensaje del mensaje siguiente.</span><span class="sxs-lookup"><span data-stu-id="14cad-108">[in] A pointer to the message class of the next message.</span></span>
    
 <span data-ttu-id="14cad-109">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="14cad-109">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="14cad-110">[entrada] Una máscara de bits de indicadores definidas por el cliente o definidas por el proveedor, copiada desde la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) del mensaje siguiente para mostrar, que proporciona información de estado con respecto a la tabla de contenido que se incluye el mensaje en.</span><span class="sxs-lookup"><span data-stu-id="14cad-110">[in] A bitmask of client-defined or provider-defined flags, copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the next message to display, that provides status information regarding the contents table that the message is included in.</span></span>
    
 <span data-ttu-id="14cad-111">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="14cad-111">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="14cad-112">[entrada] Un puntero a una máscara de bits de indicadores que se copió desde la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje siguiente para mostrar indica el estado actual del mensaje.</span><span class="sxs-lookup"><span data-stu-id="14cad-112">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the next message to display that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="14cad-113">_ppPersistMessage_</span><span class="sxs-lookup"><span data-stu-id="14cad-113">_ppPersistMessage_</span></span>
  
> <span data-ttu-id="14cad-114">[out] Un puntero a un puntero a la implementación de [IPersistMessage](ipersistmessageiunknown.md) para el objeto de formulario utilizado para el nuevo formulario, si es necesario un nuevo formulario.</span><span class="sxs-lookup"><span data-stu-id="14cad-114">[out] A pointer to a pointer to the [IPersistMessage](ipersistmessageiunknown.md) implementation for the form object used for the new form, if a new form is required.</span></span> <span data-ttu-id="14cad-115">Puede ser devuelve un puntero en NULL si el objeto de formulario actual se puede usar para mostrar y guardar el mensaje siguiente.</span><span class="sxs-lookup"><span data-stu-id="14cad-115">A pointer to NULL can be returned if the current form object can be used to display and save the next message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="14cad-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14cad-116">Return value</span></span>

<span data-ttu-id="14cad-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="14cad-117">S_OK</span></span> 
  
> <span data-ttu-id="14cad-118">La notificación se realizó correctamente y el formulario puede administrar el mensaje siguiente.</span><span class="sxs-lookup"><span data-stu-id="14cad-118">The notification was successful and the form can handle the next message.</span></span>
    
<span data-ttu-id="14cad-119">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="14cad-119">S_FALSE</span></span> 
  
> <span data-ttu-id="14cad-120">El formulario no controla la clase de mensaje del mensaje siguiente.</span><span class="sxs-lookup"><span data-stu-id="14cad-120">The form does not handle the message class of the next message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="14cad-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="14cad-121">Remarks</span></span>

<span data-ttu-id="14cad-122">Visores de formulario llamar al método **IMAPIFormAdviseSink::OnActivateNext** para determinar el formulario si puede mostrar el siguiente mensaje en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="14cad-122">Form viewers call the **IMAPIFormAdviseSink::OnActivateNext** method to help the form determine whether it can display the next message in a folder.</span></span> <span data-ttu-id="14cad-123">El siguiente mensaje podría ser un mensaje de cualquier clase, pero normalmente es de la misma clase o una clase relacionada.</span><span class="sxs-lookup"><span data-stu-id="14cad-123">The next message could be a message of any class, but typically it is of the same class or a related class.</span></span> <span data-ttu-id="14cad-124">Esto hace que el proceso de lectura de varios mensajes de la misma clase más eficaz mediante la habilitación de las aplicaciones de cliente volver a usar los objetos de formulario siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="14cad-124">This makes the process of reading multiple messages of the same class more efficient by enabling client applications to reuse form objects whenever possible.</span></span> 
  
<span data-ttu-id="14cad-125">La mayoría de los objetos de formulario usará la clase de mensaje que apunta el parámetro _lpszMessageClass_ para determinar si pueden procesar el mensaje siguiente.</span><span class="sxs-lookup"><span data-stu-id="14cad-125">Most form objects will use the message class pointed to by the  _lpszMessageClass_ parameter to determine whether they can handle the next message.</span></span> <span data-ttu-id="14cad-126">Normalmente, un formulario puede administrar los mensajes que pertenecen a las clases de que la clase del formulario de forma predeterminada es una subclase, además de los mensajes que pertenecen a la clase predeterminada.</span><span class="sxs-lookup"><span data-stu-id="14cad-126">Usually a form can handle messages that belong to classes of which the form's default class is a subclass, in addition to messages that belong to the default class.</span></span> <span data-ttu-id="14cad-127">Sin embargo, un formulario puede usar otros factores para determinar sin pregunta si un mensaje puede ser controlado, como el estado enviado y no enviado del mensaje siguiente.</span><span class="sxs-lookup"><span data-stu-id="14cad-127">However, a form can use other factors to determine without question whether a message can be handled, such as the sent or unsent status of the next message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="14cad-128">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="14cad-128">Notes to implementers</span></span>

<span data-ttu-id="14cad-129">Devolver S_OK y NULL en el parámetro _ppPersistMessage_ si el formulario puede controlar la clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="14cad-129">Return S_OK and NULL in the  _ppPersistMessage_ parameter if the form can handle the message class.</span></span> <span data-ttu-id="14cad-130">Si el formulario puede crear un nuevo formulario que puede administrar el mensaje que el formulario no puede controlar, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="14cad-130">If the form can create a new form that can handle the message that the form is unable to handle, follow these steps:</span></span> 
  
1. <span data-ttu-id="14cad-131">Llamar a fábrica de clase del formulario para crear una instancia de un nuevo objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="14cad-131">Call your form's class factory to create an instance of a new form object.</span></span>
    
2. <span data-ttu-id="14cad-132">Almacenar esa instancia en el contenido del parámetro de puntero _ppPersistMessage_ .</span><span class="sxs-lookup"><span data-stu-id="14cad-132">Store that instance in the contents of the  _ppPersistMessage_ pointer parameter.</span></span> 
    
3. <span data-ttu-id="14cad-133">Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="14cad-133">Return S_OK.</span></span>
    
<span data-ttu-id="14cad-134">El Visor de formulario cargará el mensaje mediante el método [IPersistMessage::Load](ipersistmessage-load.md) que pertenece el objeto al que señala por _ppPersistMessage_.</span><span class="sxs-lookup"><span data-stu-id="14cad-134">The form viewer will load the message by using the [IPersistMessage::Load](ipersistmessage-load.md) method that belongs to the object pointed to by  _ppPersistMessage_.</span></span>
  
<span data-ttu-id="14cad-135">Si ni el formulario ni en un formulario que se puede crear puede controlar el mensaje siguiente, devuelve S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="14cad-135">If neither the form nor a form that you can create can handle the next message, return S_FALSE.</span></span> <span data-ttu-id="14cad-136">Sin embargo, en general, formularios no deben devolver que este valor porque hace disminución del rendimiento en el Visor de formulario.</span><span class="sxs-lookup"><span data-stu-id="14cad-136">However, in general, forms should not return this value because it causes decreased performance in the form viewer.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="14cad-137">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="14cad-137">MFCMAPI reference</span></span>

<span data-ttu-id="14cad-138">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="14cad-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="14cad-139">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="14cad-139">**File**</span></span>|<span data-ttu-id="14cad-140">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="14cad-140">**Function**</span></span>|<span data-ttu-id="14cad-141">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="14cad-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="14cad-142">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="14cad-142">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="14cad-143">CMyMAPIFormViewer::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="14cad-143">CMyMAPIFormViewer::ActivateNext</span></span>  <br/> |<span data-ttu-id="14cad-144">MFCMAPI utiliza el método **IMAPIFormAdviseSink::OnActivateNext** para implementar el método [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) .</span><span class="sxs-lookup"><span data-stu-id="14cad-144">MFCMAPI uses the **IMAPIFormAdviseSink::OnActivateNext** method to implement the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="14cad-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="14cad-145">See also</span></span>



[<span data-ttu-id="14cad-146">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="14cad-146">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="14cad-147">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="14cad-147">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="14cad-148">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="14cad-148">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="14cad-149">Propiedad canónica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="14cad-149">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="14cad-150">Propiedad canónica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="14cad-150">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="14cad-151">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="14cad-151">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)


[<span data-ttu-id="14cad-152">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="14cad-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

