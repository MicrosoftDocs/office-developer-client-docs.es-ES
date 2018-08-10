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
ms.openlocfilehash: b3cdd9994de3e2a02a5302068881abce57a632a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817340"
---
# <a name="imapimessagesitegetmessage"></a><span data-ttu-id="0eada-103">IMAPIMessageSite::GetMessage</span><span class="sxs-lookup"><span data-stu-id="0eada-103">IMAPIMessageSite::GetMessage</span></span>

  
  
<span data-ttu-id="0eada-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0eada-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0eada-105">Devuelve el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="0eada-105">Returns the current message.</span></span>
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="0eada-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0eada-106">Parameters</span></span>

 <span data-ttu-id="0eada-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="0eada-107">_ppmsg_</span></span>
  
> <span data-ttu-id="0eada-108">[out] Un puntero a un puntero a la interfaz devuelta para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="0eada-108">[out] A pointer to a pointer to the returned interface for the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0eada-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0eada-109">Return value</span></span>

<span data-ttu-id="0eada-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="0eada-110">S_OK</span></span> 
  
> <span data-ttu-id="0eada-111">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="0eada-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="0eada-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="0eada-112">S_FALSE</span></span> 
  
> <span data-ttu-id="0eada-113">Actualmente no existe ningún mensaje para el formulario de llamada.</span><span class="sxs-lookup"><span data-stu-id="0eada-113">No message currently exists for the calling form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0eada-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0eada-114">Remarks</span></span>

<span data-ttu-id="0eada-115">Formularios de llamar al método **IMAPIMessageSite::GetMessage** para obtener una interfaz de mensaje para el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="0eada-115">Forms call the **IMAPIMessageSite::GetMessage** method to obtain a message interface for the current message.</span></span> <span data-ttu-id="0eada-116">El mensaje actual es el mismo mensaje tal y como se pasó anteriormente en el método [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md)o [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="0eada-116">The current message is the same message as was previously passed in the [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md), or [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method.</span></span> 
  
 <span data-ttu-id="0eada-117">**GetMessage** devuelve S_FALSE si actualmente no existe ningún mensaje.</span><span class="sxs-lookup"><span data-stu-id="0eada-117">**GetMessage** returns S_FALSE if no message currently exists.</span></span> <span data-ttu-id="0eada-118">Este estado puede producirse después de las llamadas al método [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) o antes de la siguiente llamada a **IPersistMessage::Load** o **IPersistMessage::SaveCompleted** se realiza.</span><span class="sxs-lookup"><span data-stu-id="0eada-118">This state can occur after calls to the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method or before the next call to **IPersistMessage::Load** or **IPersistMessage::SaveCompleted** is made.</span></span> 
  
<span data-ttu-id="0eada-119">Para obtener una lista de las interfaces relacionadas con los servidores de formulario, vea [Interfaces de formulario MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="0eada-119">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0eada-120">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0eada-120">MFCMAPI reference</span></span>

<span data-ttu-id="0eada-121">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="0eada-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0eada-122">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="0eada-122">**File**</span></span>|<span data-ttu-id="0eada-123">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="0eada-123">**Function**</span></span>|<span data-ttu-id="0eada-124">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="0eada-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0eada-125">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="0eada-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="0eada-126">CMyMAPIFormViewer::GetSession</span><span class="sxs-lookup"><span data-stu-id="0eada-126">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="0eada-127">MFCMAPI usa el método **IMAPIMessageSite::GetMessage** para devolver el puntero de mensaje actualmente en caché, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="0eada-127">MFCMAPI uses the **IMAPIMessageSite::GetMessage** method to return the currently cached message pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0eada-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0eada-128">See also</span></span>



[<span data-ttu-id="0eada-129">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="0eada-129">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="0eada-130">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="0eada-130">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="0eada-131">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0eada-131">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="0eada-132">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="0eada-132">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="0eada-133">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="0eada-133">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="0eada-134">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0eada-134">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="0eada-135">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="0eada-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="0eada-136">Interfaces de formulario de MAPI</span><span class="sxs-lookup"><span data-stu-id="0eada-136">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

