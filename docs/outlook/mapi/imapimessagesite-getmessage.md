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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321283"
---
# <a name="imapimessagesitegetmessage"></a><span data-ttu-id="02a16-103">IMAPIMessageSite::GetMessage</span><span class="sxs-lookup"><span data-stu-id="02a16-103">IMAPIMessageSite::GetMessage</span></span>

  
  
<span data-ttu-id="02a16-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02a16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02a16-105">Devuelve el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="02a16-105">Returns the current message.</span></span>
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="02a16-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="02a16-106">Parameters</span></span>

 <span data-ttu-id="02a16-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="02a16-107">_ppmsg_</span></span>
  
> <span data-ttu-id="02a16-108">contempla Un puntero a un puntero a la interfaz devuelta para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="02a16-108">[out] A pointer to a pointer to the returned interface for the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="02a16-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02a16-109">Return value</span></span>

<span data-ttu-id="02a16-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="02a16-110">S_OK</span></span> 
  
> <span data-ttu-id="02a16-111">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="02a16-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="02a16-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="02a16-112">S_FALSE</span></span> 
  
> <span data-ttu-id="02a16-113">Actualmente no existe ningún mensaje para el formulario de llamada.</span><span class="sxs-lookup"><span data-stu-id="02a16-113">No message currently exists for the calling form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="02a16-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="02a16-114">Remarks</span></span>

<span data-ttu-id="02a16-115">Los formularios llaman al método **IMAPIMessageSite:: GetMessage** para obtener una interfaz de mensaje para el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="02a16-115">Forms call the **IMAPIMessageSite::GetMessage** method to obtain a message interface for the current message.</span></span> <span data-ttu-id="02a16-116">El mensaje actual es el mismo mensaje que se pasó anteriormente en el método [IPersistMessage:: InitNew](ipersistmessage-initnew.md), [IPersistMessage:: Load](ipersistmessage-load.md)o [IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="02a16-116">The current message is the same message as was previously passed in the [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md), or [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method.</span></span> 
  
 <span data-ttu-id="02a16-117">**GetMessage** devuelve S_FALSE si no existe ningún mensaje actualmente.</span><span class="sxs-lookup"><span data-stu-id="02a16-117">**GetMessage** returns S_FALSE if no message currently exists.</span></span> <span data-ttu-id="02a16-118">Este estado se puede producir después de llamar al método [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md) o antes de la siguiente llamada a **IPersistMessage:: Load** o **IPersistMessage:: SaveCompleted** se realiza.</span><span class="sxs-lookup"><span data-stu-id="02a16-118">This state can occur after calls to the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method or before the next call to **IPersistMessage::Load** or **IPersistMessage::SaveCompleted** is made.</span></span> 
  
<span data-ttu-id="02a16-119">Para obtener una lista de las interfaces relacionadas con los servidores de formularios, consulte [MAPI Form interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="02a16-119">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="02a16-120">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="02a16-120">MFCMAPI reference</span></span>

<span data-ttu-id="02a16-121">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="02a16-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="02a16-122">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="02a16-122">**File**</span></span>|<span data-ttu-id="02a16-123">**Función**</span><span class="sxs-lookup"><span data-stu-id="02a16-123">**Function**</span></span>|<span data-ttu-id="02a16-124">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="02a16-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="02a16-125">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="02a16-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="02a16-126">CMyMAPIFormViewer:: GetSession</span><span class="sxs-lookup"><span data-stu-id="02a16-126">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="02a16-127">MFCMAPI usa el método **IMAPIMessageSite:: GetMessage** para devolver el puntero de mensaje actualmente almacenado en caché, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="02a16-127">MFCMAPI uses the **IMAPIMessageSite::GetMessage** method to return the currently cached message pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="02a16-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="02a16-128">See also</span></span>



[<span data-ttu-id="02a16-129">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="02a16-129">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="02a16-130">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="02a16-130">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="02a16-131">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="02a16-131">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="02a16-132">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="02a16-132">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="02a16-133">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="02a16-133">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="02a16-134">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="02a16-134">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="02a16-135">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="02a16-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="02a16-136">Interfaces de formulario de MAPI</span><span class="sxs-lookup"><span data-stu-id="02a16-136">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

