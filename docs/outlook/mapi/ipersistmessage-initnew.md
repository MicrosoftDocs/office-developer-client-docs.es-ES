---
title: IPersistMessageInitNew
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.InitNew
api_type:
- COM
ms.assetid: 4bf37c35-4f72-438a-912c-402f3711a5ea
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9f70b178e7c30e1cdf94b485c77f80374113211c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317153"
---
# <a name="ipersistmessageinitnew"></a><span data-ttu-id="2d8d0-103">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="2d8d0-103">IPersistMessage::InitNew</span></span>

  
  
<span data-ttu-id="2d8d0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d8d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d8d0-105">Inicializa un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-105">Initializes a new message.</span></span>
  
```cpp
HRESULT InitNew(
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="2d8d0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2d8d0-106">Parameters</span></span>

 <span data-ttu-id="2d8d0-107">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="2d8d0-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="2d8d0-108">[entrada] Puntero al sitio del mensaje que el formulario usará para trabajar con el mensaje en el visor.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-108">[in] A pointer to the message site that the form will use to work with the message in the viewer.</span></span>
    
 <span data-ttu-id="2d8d0-109">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="2d8d0-109">_pMessage_</span></span>
  
> <span data-ttu-id="2d8d0-110">[entrada] Un puntero al nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-110">[in] A pointer to the new message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2d8d0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2d8d0-111">Return value</span></span>

<span data-ttu-id="2d8d0-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="2d8d0-112">S_OK</span></span> 
  
> <span data-ttu-id="2d8d0-113">El nuevo mensaje se inicializó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-113">The new message was successfully initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2d8d0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2d8d0-114">Remarks</span></span>

<span data-ttu-id="2d8d0-115">Los visores de formularios llaman al método **IPersistMessage::InitNew** cuando el usuario escribe un nuevo mensaje que pertenece a una clase de mensaje que controla el formulario.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-115">Form viewers call the **IPersistMessage::InitNew** method when the user writes a new message that belongs to a message class that the form handles.</span></span> <span data-ttu-id="2d8d0-116">Si el objeto de formulario tiene un puntero de interfaz de usuario válido, se debe mostrar la interfaz de usuario del objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-116">If the form object has a valid user interface pointer, the user interface for the message object should be displayed.</span></span> 
  
 <span data-ttu-id="2d8d0-117">No se debe llamar a **InitNew** cuando el formulario está en cualquier estado excepto el [estado Sin inicializar.](uninitialized-state.md)</span><span class="sxs-lookup"><span data-stu-id="2d8d0-117">**InitNew** should not be called when your form is in any state except the [Uninitialized](uninitialized-state.md) state.</span></span> <span data-ttu-id="2d8d0-118">Si el formulario se encuentra en uno de los demás estados cuando se llama **a InitNew,** E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-118">If the form is in one of the other states when **InitNew** is called, return E_UNEXPECTED.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2d8d0-119">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="2d8d0-119">Notes to implementers</span></span>

<span data-ttu-id="2d8d0-120">Normalmente, los mensajes que tienen propiedades no guardadas se marcan como modificados para que el cliente pueda mostrar un cuadro de diálogo que pregunta al usuario si estas propiedades deben guardarse.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-120">Typically, messages that have unsaved properties are marked as modified so that the client can display a dialog box that prompts the user whether these properties should be saved.</span></span> <span data-ttu-id="2d8d0-121">Si el usuario indica que se debe guardar un mensaje, guarde los datos, marque el mensaje como limpio y salga normalmente.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-121">If the user indicates that a message should be saved, save the data, mark the message as clean, and exit normally.</span></span>
  
<span data-ttu-id="2d8d0-122">Sin embargo, si el procesamiento de los mensajes recién inicializados incluye establecer una o más propiedades calculadas y es importante que esas propiedades se guarden, no marque los mensajes como modificados.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-122">However, if processing for your newly initialized messages includes setting one or more computed properties, and it is important for those properties to be saved, do not mark the messages as modified.</span></span> <span data-ttu-id="2d8d0-123">Dado que las propiedades calculadas deben ser invisibles para los usuarios, no debe mostrarse ningún cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-123">Because computed properties should be invisible to users, no dialog box should be displayed.</span></span>
  
<span data-ttu-id="2d8d0-124">Si el formulario tiene una referencia a un sitio de mensaje activo distinto del que se pasa a **InitNew**, libere el sitio original porque ya no se usará.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-124">If your form has a reference to an active message site other than the one that is passed into **InitNew**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="2d8d0-125">Almacene los punteros al sitio y al mensaje del mensaje desde los parámetros  _pMessageSite_ y  _pMessage,_ y llame a los métodos [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) de ambos objetos para incrementar sus recuentos de referencia.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-125">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="2d8d0-126">Establezca las **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) y **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) del nuevo mensaje en algo apropiado para la clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-126">Set the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) and **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) properties for the new message to something appropriate for your message class.</span></span> <span data-ttu-id="2d8d0-127">Muchas clases de mensajes, por ejemplo, **PR_MESSAGE_FLAGS** en MSGFLAG_UNSENT para mensajes nuevos.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-127">Many message classes, for example, set **PR_MESSAGE_FLAGS** to MSGFLAG_UNSENT for new messages.</span></span> 
  
<span data-ttu-id="2d8d0-128">Antes de volver, haga la transición del formulario al [estado Normal](normal-state.md) si no se han producido errores.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-128">Before returning, transition the form to the [Normal](normal-state.md) state if no errors have occurred.</span></span> <span data-ttu-id="2d8d0-129">Envíe una nueva notificación de mensaje a todos los visores registrados llamando a sus métodos [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) y devuelva S_OK.</span><span class="sxs-lookup"><span data-stu-id="2d8d0-129">Send a new message notification to all registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods and return S_OK.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2d8d0-130">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="2d8d0-130">Notes to callers</span></span>

<span data-ttu-id="2d8d0-131">Después de realizar una llamada correcta a **InitNew**, puede suponer que se han establecido las siguientes propiedades necesarias y ninguna otra para el formulario:</span><span class="sxs-lookup"><span data-stu-id="2d8d0-131">After you have made a successful call to **InitNew**, you can assume that the following required properties, and no others, have been set for the form:</span></span>
  
 <span data-ttu-id="2d8d0-132">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2d8d0-132">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span>
  
 <span data-ttu-id="2d8d0-133">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2d8d0-133">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
  
 <span data-ttu-id="2d8d0-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2d8d0-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="2d8d0-135">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2d8d0-135">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
  
 <span data-ttu-id="2d8d0-136">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2d8d0-136">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="2d8d0-137">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2d8d0-137">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
  
 <span data-ttu-id="2d8d0-138">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2d8d0-138">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="2d8d0-139">Para obtener más información acerca de los estados de los formularios, vea [Estados de formulario.](form-states.md)</span><span class="sxs-lookup"><span data-stu-id="2d8d0-139">For more information about the states of forms, see [Form States](form-states.md).</span></span> <span data-ttu-id="2d8d0-140">Para obtener más información acerca de cómo se inicializan los objetos de almacenamiento, vea el método [IPersistStorage::InitNew.](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2d8d0-140">For more information about how storage objects are initialized, see the [IPersistStorage::InitNew](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2d8d0-141">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2d8d0-141">See also</span></span>



[<span data-ttu-id="2d8d0-142">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2d8d0-142">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

