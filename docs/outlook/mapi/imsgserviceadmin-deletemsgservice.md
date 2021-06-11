---
title: IMsgServiceAdminDeleteMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.DeleteMsgService
api_type:
- COM
ms.assetid: 3a6b34eb-9d46-488f-8d02-91b27c35de67
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6cef03e33abab81a407698b73a007f247ef88194
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407385"
---
# <a name="imsgserviceadmindeletemsgservice"></a><span data-ttu-id="c349a-103">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="c349a-103">IMsgServiceAdmin::DeleteMsgService</span></span>

  
  
<span data-ttu-id="c349a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c349a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c349a-105">Elimina un servicio de mensajes de un perfil.</span><span class="sxs-lookup"><span data-stu-id="c349a-105">Deletes a message service from a profile.</span></span>
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a><span data-ttu-id="c349a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="c349a-106">Parameters</span></span>

 <span data-ttu-id="c349a-107">_lpuid_</span><span class="sxs-lookup"><span data-stu-id="c349a-107">_lpuid_</span></span>
  
> <span data-ttu-id="c349a-108">[in] Puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único del servicio de mensajes que se debe eliminar.</span><span class="sxs-lookup"><span data-stu-id="c349a-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c349a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c349a-109">Return value</span></span>

<span data-ttu-id="c349a-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="c349a-110">S_OK</span></span> 
  
> <span data-ttu-id="c349a-111">Se eliminó el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c349a-111">The message service was deleted.</span></span>
    
<span data-ttu-id="c349a-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c349a-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="c349a-113">El **MAPIUID** señalado por  _lpuid_ no coincide con un servicio de mensajes existente.</span><span class="sxs-lookup"><span data-stu-id="c349a-113">The **MAPIUID** pointed to by  _lpuid_ does not match an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c349a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c349a-114">Remarks</span></span>

<span data-ttu-id="c349a-115">El **método IMsgServiceAdmin::D eleteMsgService** elimina un servicio de mensajes de un perfil.</span><span class="sxs-lookup"><span data-stu-id="c349a-115">The **IMsgServiceAdmin::DeleteMsgService** method deletes a message service from a profile.</span></span> <span data-ttu-id="c349a-116">**DeleteMsgService** quita todas las secciones de perfil relacionadas con el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c349a-116">**DeleteMsgService** removes all profile sections related to the message service.</span></span> 
  
 <span data-ttu-id="c349a-117">**DeleteMsgService** realiza los siguientes pasos para eliminar el servicio de mensajes:</span><span class="sxs-lookup"><span data-stu-id="c349a-117">**DeleteMsgService** performs the following steps to delete the message service:</span></span> 
  
1. <span data-ttu-id="c349a-118">Llama a la función de punto de entrada del servicio de mensajes con el parámetro  _ulContext_ establecido en MSG_SERVICE_DELETE antes de que se quiten las secciones de perfil.</span><span class="sxs-lookup"><span data-stu-id="c349a-118">Calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE before the profile sections are removed.</span></span> <span data-ttu-id="c349a-119">Esto permite al servicio realizar tareas específicas del servicio.</span><span class="sxs-lookup"><span data-stu-id="c349a-119">This allows the service to perform any service-specific tasks.</span></span> 
    
2. <span data-ttu-id="c349a-120">Elimina el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c349a-120">Deletes the message service.</span></span>
    
3. <span data-ttu-id="c349a-121">Elimina la sección de perfil del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c349a-121">Deletes the message service's profile section.</span></span>
    
<span data-ttu-id="c349a-122">No se vuelve a llamar a la función de punto de entrada del servicio de mensajes después de eliminar el servicio.</span><span class="sxs-lookup"><span data-stu-id="c349a-122">The message service's entry point function is not called again after the service has been deleted.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="c349a-123">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="c349a-123">Notes to callers</span></span>

<span data-ttu-id="c349a-124">Para recuperar la estructura **MAPIUID** para que el servicio de mensajes elimine, recupere la columna de propiedad **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) de la fila del servicio de mensajes de la tabla de servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c349a-124">To retrieve the **MAPIUID** structure for the message service to delete, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="c349a-125">Para obtener más información, vea el procedimiento descrito en el [método IMsgServiceAdmin::CreateMsgService.](imsgserviceadmin-createmsgservice.md)</span><span class="sxs-lookup"><span data-stu-id="c349a-125">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c349a-126">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c349a-126">MFCMAPI reference</span></span>

<span data-ttu-id="c349a-127">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="c349a-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c349a-128">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="c349a-128">**File**</span></span>|<span data-ttu-id="c349a-129">**Función**</span><span class="sxs-lookup"><span data-stu-id="c349a-129">**Function**</span></span>|<span data-ttu-id="c349a-130">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="c349a-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c349a-131">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="c349a-131">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="c349a-132">CMsgServiceTableDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="c349a-132">CMsgServiceTableDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="c349a-133">MFCMAPI usa el **método IMsgServiceAdmin::D eleteMsgService** para eliminar el servicio seleccionado.</span><span class="sxs-lookup"><span data-stu-id="c349a-133">MFCMAPI uses the **IMsgServiceAdmin::DeleteMsgService** method to delete the selected service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c349a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="c349a-134">See also</span></span>



[<span data-ttu-id="c349a-135">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="c349a-135">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="c349a-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c349a-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="c349a-137">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="c349a-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

