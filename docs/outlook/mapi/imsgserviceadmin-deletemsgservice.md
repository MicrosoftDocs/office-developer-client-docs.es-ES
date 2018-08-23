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
ms.openlocfilehash: e0d3d669982bee309901f913612ac1fb1622e60a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571147"
---
# <a name="imsgserviceadmindeletemsgservice"></a><span data-ttu-id="ce7c9-103">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="ce7c9-103">IMsgServiceAdmin::DeleteMsgService</span></span>

  
  
<span data-ttu-id="ce7c9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce7c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce7c9-105">Elimina un servicio de mensajes de un perfil.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-105">Deletes a message service from a profile.</span></span>
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a><span data-ttu-id="ce7c9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce7c9-106">Parameters</span></span>

 <span data-ttu-id="ce7c9-107">_lpuid_</span><span class="sxs-lookup"><span data-stu-id="ce7c9-107">_lpuid_</span></span>
  
> <span data-ttu-id="ce7c9-108">[entrada] Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único para el servicio de mensajes eliminar.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ce7c9-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce7c9-109">Return value</span></span>

<span data-ttu-id="ce7c9-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ce7c9-110">S_OK</span></span> 
  
> <span data-ttu-id="ce7c9-111">Se ha eliminado el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-111">The message service was deleted.</span></span>
    
<span data-ttu-id="ce7c9-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ce7c9-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ce7c9-113">El **MAPIUID** que señala _lpuid_ no coincide con un servicio de mensaje existente.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-113">The **MAPIUID** pointed to by  _lpuid_ does not match an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ce7c9-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ce7c9-114">Remarks</span></span>

<span data-ttu-id="ce7c9-115">El método **IMsgServiceAdmin::DeleteMsgService** elimina un servicio de mensajes de un perfil.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-115">The **IMsgServiceAdmin::DeleteMsgService** method deletes a message service from a profile.</span></span> <span data-ttu-id="ce7c9-116">**DeleteMsgService** quita todos los perfiles en las secciones relacionadas con el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-116">**DeleteMsgService** removes all profile sections related to the message service.</span></span> 
  
 <span data-ttu-id="ce7c9-117">**DeleteMsgService** realiza los siguientes pasos para eliminar el servicio de mensajes:</span><span class="sxs-lookup"><span data-stu-id="ce7c9-117">**DeleteMsgService** performs the following steps to delete the message service:</span></span> 
  
1. <span data-ttu-id="ce7c9-118">Llamadas de función de punto de entrada del servicio de mensajes con el parámetro de _ulContext_ establecido en MSG_SERVICE_DELETE antes de que se han quitado las secciones del perfil.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-118">Calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE before the profile sections are removed.</span></span> <span data-ttu-id="ce7c9-119">Esto permite que el servicio realizar las tareas específicas de servicio.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-119">This allows the service to perform any service-specific tasks.</span></span> 
    
2. <span data-ttu-id="ce7c9-120">Elimina el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-120">Deletes the message service.</span></span>
    
3. <span data-ttu-id="ce7c9-121">Elimina la sección de perfil de servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-121">Deletes the message service's profile section.</span></span>
    
<span data-ttu-id="ce7c9-122">Función de punto de entrada del servicio de mensajes no se llama de nuevo después de que se ha eliminado el servicio.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-122">The message service's entry point function is not called again after the service has been deleted.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="ce7c9-123">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="ce7c9-123">Notes to callers</span></span>

<span data-ttu-id="ce7c9-124">Para recuperar la estructura **MAPIUID** para el servicio de mensajes eliminar, recuperar la columna de propiedad **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) de la fila del servicio de mensajes en la tabla de servicios de mensaje.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-124">To retrieve the **MAPIUID** structure for the message service to delete, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="ce7c9-125">Para obtener más información, vea el procedimiento descrito en el método [IMsgServiceAdmin::](imsgserviceadmin-createmsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="ce7c9-125">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ce7c9-126">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ce7c9-126">MFCMAPI reference</span></span>

<span data-ttu-id="ce7c9-127">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ce7c9-128">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="ce7c9-128">**File**</span></span>|<span data-ttu-id="ce7c9-129">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="ce7c9-129">**Function**</span></span>|<span data-ttu-id="ce7c9-130">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="ce7c9-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ce7c9-131">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ce7c9-131">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="ce7c9-132">CMsgServiceTableDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="ce7c9-132">CMsgServiceTableDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="ce7c9-133">MFCMAPI usa el método **IMsgServiceAdmin::DeleteMsgService** para eliminar el servicio seleccionado.</span><span class="sxs-lookup"><span data-stu-id="ce7c9-133">MFCMAPI uses the **IMsgServiceAdmin::DeleteMsgService** method to delete the selected service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce7c9-134">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="ce7c9-134">See also</span></span>



[<span data-ttu-id="ce7c9-135">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="ce7c9-135">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="ce7c9-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ce7c9-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="ce7c9-137">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="ce7c9-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

