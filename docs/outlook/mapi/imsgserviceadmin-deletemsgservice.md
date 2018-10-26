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
# <a name="imsgserviceadmindeletemsgservice"></a><span data-ttu-id="9f307-103">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="9f307-103">IMsgServiceAdmin::DeleteMsgService</span></span>

  
  
<span data-ttu-id="9f307-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f307-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f307-105">Elimina un servicio de mensajes de un perfil.</span><span class="sxs-lookup"><span data-stu-id="9f307-105">Deletes a message service from a profile.</span></span>
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a><span data-ttu-id="9f307-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f307-106">Parameters</span></span>

 <span data-ttu-id="9f307-107">_lpuid_</span><span class="sxs-lookup"><span data-stu-id="9f307-107">_lpuid_</span></span>
  
> <span data-ttu-id="9f307-108">[entrada] Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único para el servicio de mensajes eliminar.</span><span class="sxs-lookup"><span data-stu-id="9f307-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9f307-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f307-109">Return value</span></span>

<span data-ttu-id="9f307-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="9f307-110">S_OK</span></span> 
  
> <span data-ttu-id="9f307-111">Se ha eliminado el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9f307-111">The message service was deleted.</span></span>
    
<span data-ttu-id="9f307-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="9f307-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="9f307-113">El **MAPIUID** que señala _lpuid_ no coincide con un servicio de mensaje existente.</span><span class="sxs-lookup"><span data-stu-id="9f307-113">The **MAPIUID** pointed to by  _lpuid_ does not match an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9f307-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9f307-114">Remarks</span></span>

<span data-ttu-id="9f307-115">El método **IMsgServiceAdmin::DeleteMsgService** elimina un servicio de mensajes de un perfil.</span><span class="sxs-lookup"><span data-stu-id="9f307-115">The **IMsgServiceAdmin::DeleteMsgService** method deletes a message service from a profile.</span></span> <span data-ttu-id="9f307-116">**DeleteMsgService** quita todos los perfiles en las secciones relacionadas con el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9f307-116">**DeleteMsgService** removes all profile sections related to the message service.</span></span> 
  
 <span data-ttu-id="9f307-117">**DeleteMsgService** realiza los siguientes pasos para eliminar el servicio de mensajes:</span><span class="sxs-lookup"><span data-stu-id="9f307-117">**DeleteMsgService** performs the following steps to delete the message service:</span></span> 
  
1. <span data-ttu-id="9f307-118">Llamadas de función de punto de entrada del servicio de mensajes con el parámetro de _ulContext_ establecido en MSG_SERVICE_DELETE antes de que se han quitado las secciones del perfil.</span><span class="sxs-lookup"><span data-stu-id="9f307-118">Calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE before the profile sections are removed.</span></span> <span data-ttu-id="9f307-119">Esto permite que el servicio realizar las tareas específicas de servicio.</span><span class="sxs-lookup"><span data-stu-id="9f307-119">This allows the service to perform any service-specific tasks.</span></span> 
    
2. <span data-ttu-id="9f307-120">Elimina el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9f307-120">Deletes the message service.</span></span>
    
3. <span data-ttu-id="9f307-121">Elimina la sección de perfil de servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9f307-121">Deletes the message service's profile section.</span></span>
    
<span data-ttu-id="9f307-122">Función de punto de entrada del servicio de mensajes no se llama de nuevo después de que se ha eliminado el servicio.</span><span class="sxs-lookup"><span data-stu-id="9f307-122">The message service's entry point function is not called again after the service has been deleted.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="9f307-123">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="9f307-123">Notes to callers</span></span>

<span data-ttu-id="9f307-124">Para recuperar la estructura **MAPIUID** para el servicio de mensajes eliminar, recuperar la columna de propiedad **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) de la fila del servicio de mensajes en la tabla de servicios de mensaje.</span><span class="sxs-lookup"><span data-stu-id="9f307-124">To retrieve the **MAPIUID** structure for the message service to delete, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="9f307-125">Para obtener más información, vea el procedimiento descrito en el método [IMsgServiceAdmin::](imsgserviceadmin-createmsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="9f307-125">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9f307-126">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9f307-126">MFCMAPI reference</span></span>

<span data-ttu-id="9f307-127">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="9f307-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9f307-128">**File**</span><span class="sxs-lookup"><span data-stu-id="9f307-128">**File**</span></span>|<span data-ttu-id="9f307-129">**Función**</span><span class="sxs-lookup"><span data-stu-id="9f307-129">**Function**</span></span>|<span data-ttu-id="9f307-130">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="9f307-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9f307-131">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="9f307-131">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="9f307-132">CMsgServiceTableDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="9f307-132">CMsgServiceTableDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="9f307-133">MFCMAPI usa el método **IMsgServiceAdmin::DeleteMsgService** para eliminar el servicio seleccionado.</span><span class="sxs-lookup"><span data-stu-id="9f307-133">MFCMAPI uses the **IMsgServiceAdmin::DeleteMsgService** method to delete the selected service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9f307-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f307-134">See also</span></span>



[<span data-ttu-id="9f307-135">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="9f307-135">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="9f307-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9f307-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="9f307-137">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="9f307-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

