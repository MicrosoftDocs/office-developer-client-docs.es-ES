---
title: IMAPIMessageSiteGetMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetMessage
api_type:
- COM
ms.assetid: 49d12c49-84f8-44ac-bc4a-2ee44a46f8c1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 03dd0553d0203585850ac5c4f8c91c86ef60236a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409030"
---
# <a name="imapimessagesitegetmessage"></a><span data-ttu-id="b8a7b-103">IMAPIMessageSite::GetMessage</span><span class="sxs-lookup"><span data-stu-id="b8a7b-103">IMAPIMessageSite::GetMessage</span></span>

  
  
<span data-ttu-id="b8a7b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8a7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8a7b-105">Devuelve el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="b8a7b-105">Returns the current message.</span></span>
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="b8a7b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8a7b-106">Parameters</span></span>

 <span data-ttu-id="b8a7b-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="b8a7b-107">_ppmsg_</span></span>
  
> <span data-ttu-id="b8a7b-108">[salida] Puntero a un puntero a la interfaz devuelta para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="b8a7b-108">[out] A pointer to a pointer to the returned interface for the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b8a7b-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8a7b-109">Return value</span></span>

<span data-ttu-id="b8a7b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="b8a7b-110">S_OK</span></span> 
  
> <span data-ttu-id="b8a7b-111">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="b8a7b-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b8a7b-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="b8a7b-112">S_FALSE</span></span> 
  
> <span data-ttu-id="b8a7b-113">Actualmente no existe ningún mensaje para el formulario de llamada.</span><span class="sxs-lookup"><span data-stu-id="b8a7b-113">No message currently exists for the calling form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b8a7b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b8a7b-114">Remarks</span></span>

<span data-ttu-id="b8a7b-115">Los formularios llaman **al método IMAPIMessageSite::GetMessage** para obtener una interfaz de mensaje para el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="b8a7b-115">Forms call the **IMAPIMessageSite::GetMessage** method to obtain a message interface for the current message.</span></span> <span data-ttu-id="b8a7b-116">El mensaje actual es el mismo mensaje que se pasó anteriormente en el método [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md)o [IPersistMessage::SaveCompleted.](ipersistmessage-savecompleted.md)</span><span class="sxs-lookup"><span data-stu-id="b8a7b-116">The current message is the same message as was previously passed in the [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md), or [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method.</span></span> 
  
 <span data-ttu-id="b8a7b-117">**GetMessage** devuelve S_FALSE si no existe ningún mensaje actualmente.</span><span class="sxs-lookup"><span data-stu-id="b8a7b-117">**GetMessage** returns S_FALSE if no message currently exists.</span></span> <span data-ttu-id="b8a7b-118">Este estado puede producirse después de realizar llamadas al método [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) o antes de realizar la siguiente llamada a **IPersistMessage::Load** o **IPersistMessage::SaveCompleted.**</span><span class="sxs-lookup"><span data-stu-id="b8a7b-118">This state can occur after calls to the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method or before the next call to **IPersistMessage::Load** or **IPersistMessage::SaveCompleted** is made.</span></span> 
  
<span data-ttu-id="b8a7b-119">Para obtener una lista de interfaces relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="b8a7b-119">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b8a7b-120">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b8a7b-120">MFCMAPI reference</span></span>

<span data-ttu-id="b8a7b-121">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="b8a7b-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b8a7b-122">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="b8a7b-122">**File**</span></span>|<span data-ttu-id="b8a7b-123">**Función**</span><span class="sxs-lookup"><span data-stu-id="b8a7b-123">**Function**</span></span>|<span data-ttu-id="b8a7b-124">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="b8a7b-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b8a7b-125">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="b8a7b-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="b8a7b-126">CMyMAPIFormViewer::GetSession</span><span class="sxs-lookup"><span data-stu-id="b8a7b-126">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="b8a7b-127">MFCMAPI usa el **método IMAPIMessageSite::GetMessage** para devolver el puntero de mensaje almacenado actualmente en caché, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="b8a7b-127">MFCMAPI uses the **IMAPIMessageSite::GetMessage** method to return the currently cached message pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b8a7b-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b8a7b-128">See also</span></span>



[<span data-ttu-id="b8a7b-129">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="b8a7b-129">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="b8a7b-130">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="b8a7b-130">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="b8a7b-131">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b8a7b-131">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="b8a7b-132">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="b8a7b-132">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="b8a7b-133">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="b8a7b-133">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="b8a7b-134">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b8a7b-134">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="b8a7b-135">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="b8a7b-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="b8a7b-136">Interfaces de formulario MAPI</span><span class="sxs-lookup"><span data-stu-id="b8a7b-136">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

