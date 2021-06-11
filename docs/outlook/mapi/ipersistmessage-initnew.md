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
# <a name="ipersistmessageinitnew"></a><span data-ttu-id="d3013-103">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="d3013-103">IPersistMessage::InitNew</span></span>

  
  
<span data-ttu-id="d3013-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3013-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3013-105">Inicializa un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="d3013-105">Initializes a new message.</span></span>
  
```cpp
HRESULT InitNew(
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a><span data-ttu-id="d3013-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d3013-106">Parameters</span></span>

 <span data-ttu-id="d3013-107">_pMessageSite_</span><span class="sxs-lookup"><span data-stu-id="d3013-107">_pMessageSite_</span></span>
  
> <span data-ttu-id="d3013-108">[in] Puntero al sitio del mensaje que usará el formulario para trabajar con el mensaje en el visor.</span><span class="sxs-lookup"><span data-stu-id="d3013-108">[in] A pointer to the message site that the form will use to work with the message in the viewer.</span></span>
    
 <span data-ttu-id="d3013-109">_pMessage_</span><span class="sxs-lookup"><span data-stu-id="d3013-109">_pMessage_</span></span>
  
> <span data-ttu-id="d3013-110">[in] Puntero al nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="d3013-110">[in] A pointer to the new message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d3013-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3013-111">Return value</span></span>

<span data-ttu-id="d3013-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="d3013-112">S_OK</span></span> 
  
> <span data-ttu-id="d3013-113">El nuevo mensaje se inicializó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d3013-113">The new message was successfully initialized.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d3013-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d3013-114">Remarks</span></span>

<span data-ttu-id="d3013-115">Los visores de formularios llaman al método **IPersistMessage::InitNew** cuando el usuario escribe un nuevo mensaje que pertenece a una clase de mensaje que controla el formulario.</span><span class="sxs-lookup"><span data-stu-id="d3013-115">Form viewers call the **IPersistMessage::InitNew** method when the user writes a new message that belongs to a message class that the form handles.</span></span> <span data-ttu-id="d3013-116">Si el objeto de formulario tiene un puntero de interfaz de usuario válido, se debe mostrar la interfaz de usuario del objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="d3013-116">If the form object has a valid user interface pointer, the user interface for the message object should be displayed.</span></span> 
  
 <span data-ttu-id="d3013-117">No se debe llamar a **InitNew** cuando el formulario está en cualquier estado excepto el [estado Uninitialized.](uninitialized-state.md)</span><span class="sxs-lookup"><span data-stu-id="d3013-117">**InitNew** should not be called when your form is in any state except the [Uninitialized](uninitialized-state.md) state.</span></span> <span data-ttu-id="d3013-118">Si el formulario está en uno de los otros estados cuando se llama a **InitNew,** devuelva E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="d3013-118">If the form is in one of the other states when **InitNew** is called, return E_UNEXPECTED.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d3013-119">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="d3013-119">Notes to implementers</span></span>

<span data-ttu-id="d3013-120">Normalmente, los mensajes que tienen propiedades no guardadas se marcan como modificados para que el cliente pueda mostrar un cuadro de diálogo que pida al usuario si estas propiedades deben guardarse.</span><span class="sxs-lookup"><span data-stu-id="d3013-120">Typically, messages that have unsaved properties are marked as modified so that the client can display a dialog box that prompts the user whether these properties should be saved.</span></span> <span data-ttu-id="d3013-121">Si el usuario indica que se debe guardar un mensaje, guarde los datos, marque el mensaje como limpio y salga normalmente.</span><span class="sxs-lookup"><span data-stu-id="d3013-121">If the user indicates that a message should be saved, save the data, mark the message as clean, and exit normally.</span></span>
  
<span data-ttu-id="d3013-122">Sin embargo, si el procesamiento de los mensajes recién inicializados incluye establecer una o más propiedades calculadas y es importante que esas propiedades se guarden, no marque los mensajes como modificados.</span><span class="sxs-lookup"><span data-stu-id="d3013-122">However, if processing for your newly initialized messages includes setting one or more computed properties, and it is important for those properties to be saved, do not mark the messages as modified.</span></span> <span data-ttu-id="d3013-123">Dado que las propiedades calculadas deben ser invisibles para los usuarios, no se debe mostrar ningún cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d3013-123">Because computed properties should be invisible to users, no dialog box should be displayed.</span></span>
  
<span data-ttu-id="d3013-124">Si el formulario tiene una referencia a un sitio de mensaje activo distinto del que se pasa a **InitNew**, libere el sitio original porque ya no se usará.</span><span class="sxs-lookup"><span data-stu-id="d3013-124">If your form has a reference to an active message site other than the one that is passed into **InitNew**, release the original site because it will no longer be used.</span></span> <span data-ttu-id="d3013-125">Almacene los punteros al sitio y al mensaje del mensaje desde los parámetros  _pMessageSite_ y  _pMessage_ y llame a los métodos [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) de ambos objetos para incrementar sus recuentos de referencias.</span><span class="sxs-lookup"><span data-stu-id="d3013-125">Store the pointers to the message site and message from the  _pMessageSite_ and  _pMessage_ parameters and call both objects' [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) methods to increment their reference counts.</span></span> 
  
<span data-ttu-id="d3013-126">Establezca las **propiedades PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) y **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) para el nuevo mensaje en algo apropiado para la clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="d3013-126">Set the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) and **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) properties for the new message to something appropriate for your message class.</span></span> <span data-ttu-id="d3013-127">Muchas clases de mensajes, por ejemplo, **PR_MESSAGE_FLAGS** en MSGFLAG_UNSENT para los mensajes nuevos.</span><span class="sxs-lookup"><span data-stu-id="d3013-127">Many message classes, for example, set **PR_MESSAGE_FLAGS** to MSGFLAG_UNSENT for new messages.</span></span> 
  
<span data-ttu-id="d3013-128">Antes de devolver, transime el formulario al [estado Normal](normal-state.md) si no se han producido errores.</span><span class="sxs-lookup"><span data-stu-id="d3013-128">Before returning, transition the form to the [Normal](normal-state.md) state if no errors have occurred.</span></span> <span data-ttu-id="d3013-129">Envíe una nueva notificación de mensaje a todos los visores registrados llamando a sus [métodos IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) y devuelva S_OK.</span><span class="sxs-lookup"><span data-stu-id="d3013-129">Send a new message notification to all registered viewers by calling their [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) methods and return S_OK.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d3013-130">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="d3013-130">Notes to callers</span></span>

<span data-ttu-id="d3013-131">Después de realizar una llamada correcta a **InitNew**, puede suponer que las siguientes propiedades necesarias, y ninguna otra, se han establecido para el formulario:</span><span class="sxs-lookup"><span data-stu-id="d3013-131">After you have made a successful call to **InitNew**, you can assume that the following required properties, and no others, have been set for the form:</span></span>
  
 <span data-ttu-id="d3013-132">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d3013-132">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))</span></span>
  
 <span data-ttu-id="d3013-133">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d3013-133">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
  
 <span data-ttu-id="d3013-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d3013-134">**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="d3013-135">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d3013-135">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
  
 <span data-ttu-id="d3013-136">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d3013-136">**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))</span></span>
  
 <span data-ttu-id="d3013-137">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d3013-137">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
  
 <span data-ttu-id="d3013-138">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d3013-138">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))</span></span>
  
<span data-ttu-id="d3013-139">Para obtener más información acerca de los estados de los formularios, vea [Estados del formulario](form-states.md).</span><span class="sxs-lookup"><span data-stu-id="d3013-139">For more information about the states of forms, see [Form States](form-states.md).</span></span> <span data-ttu-id="d3013-140">Para obtener más información sobre cómo se inicializan los objetos de almacenamiento, vea el [método IPersistStorage::InitNew.](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3013-140">For more information about how storage objects are initialized, see the [IPersistStorage::InitNew](https://msdn.microsoft.com/library/79caf1f6-d974-4aee-8563-eda4876a0a90%28Office.15%29.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d3013-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3013-141">See also</span></span>



[<span data-ttu-id="d3013-142">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d3013-142">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

