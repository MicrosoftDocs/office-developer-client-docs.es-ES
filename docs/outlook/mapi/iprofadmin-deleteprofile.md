---
title: IProfAdminDeleteProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.DeleteProfile
api_type:
- COM
ms.assetid: 730af2da-4c4a-42a7-9d52-56d914107d64
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8aafb849a98028efb37646752a7b49fa5e6ef2ff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419593"
---
# <a name="iprofadmindeleteprofile"></a><span data-ttu-id="29a57-103">IProfAdmin::DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="29a57-103">IProfAdmin::DeleteProfile</span></span>

  
  
<span data-ttu-id="29a57-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29a57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29a57-105">Elimina un perfil.</span><span class="sxs-lookup"><span data-stu-id="29a57-105">Deletes a profile.</span></span>
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="29a57-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="29a57-106">Parameters</span></span>

 <span data-ttu-id="29a57-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="29a57-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="29a57-108">a Un puntero al nombre del perfil que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="29a57-108">[in] A pointer to the name of the profile to be deleted.</span></span>
    
 <span data-ttu-id="29a57-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="29a57-109">_ulFlags_</span></span>
  
> <span data-ttu-id="29a57-110">a Siempre NULL.</span><span class="sxs-lookup"><span data-stu-id="29a57-110">[in] Always NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="29a57-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="29a57-111">Return value</span></span>

<span data-ttu-id="29a57-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="29a57-112">S_OK</span></span> 
  
> <span data-ttu-id="29a57-113">El perfil se eliminó correctamente.</span><span class="sxs-lookup"><span data-stu-id="29a57-113">The profile was successfully deleted.</span></span>
    
<span data-ttu-id="29a57-114">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="29a57-114">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="29a57-115">El perfil especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="29a57-115">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="29a57-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="29a57-116">Remarks</span></span>

<span data-ttu-id="29a57-117">El método **IProfAdmin::D eleteprofile** elimina un perfil.</span><span class="sxs-lookup"><span data-stu-id="29a57-117">The **IProfAdmin::DeleteProfile** method deletes a profile.</span></span> <span data-ttu-id="29a57-118">Si el perfil que se va a eliminar está en uso cuando se llama a **DeleteProfile** , **DeleteProfile** Devuelve S_OK pero no elimina el perfil inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="29a57-118">If the profile to delete is in use when **DeleteProfile** is called, **DeleteProfile** returns S_OK but does not delete the profile immediately.</span></span> <span data-ttu-id="29a57-119">En su lugar, **DeleteProfile** marca el perfil para su eliminación y lo elimina una vez que ya no se usa, cuando todas sus sesiones activas han finalizado.</span><span class="sxs-lookup"><span data-stu-id="29a57-119">Instead, **DeleteProfile** marks the profile for deletion and deletes it after it is no longer being used, when all of its active sessions have ended.</span></span> 
  
<span data-ttu-id="29a57-120">La función de punto de entrada de cada servicio de mensajes del perfil se llama con el valor MSG_SERVICE_DELETE establecido en el parámetro _ulContext_ .</span><span class="sxs-lookup"><span data-stu-id="29a57-120">The entry point function for each message service in the profile is called with the MSG_SERVICE_DELETE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="29a57-121">En primer lugar, la función elimina el servicio y, a continuación, elimina la sección del perfil del servicio.</span><span class="sxs-lookup"><span data-stu-id="29a57-121">First, the function deletes the service, and then it deletes the service's profile section.</span></span> <span data-ttu-id="29a57-122">No se llama de nuevo a la función de punto de entrada del servicio de mensajes después de que se haya eliminado el servicio.</span><span class="sxs-lookup"><span data-stu-id="29a57-122">The message service entry point function is not called again after the service has been deleted.</span></span> 
  
<span data-ttu-id="29a57-123">No es necesaria ninguna contraseña para eliminar un perfil.</span><span class="sxs-lookup"><span data-stu-id="29a57-123">No password is required to delete a profile.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="29a57-124">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="29a57-124">MFCMAPI reference</span></span>

<span data-ttu-id="29a57-125">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="29a57-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="29a57-126">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="29a57-126">**File**</span></span>|<span data-ttu-id="29a57-127">**Función**</span><span class="sxs-lookup"><span data-stu-id="29a57-127">**Function**</span></span>|<span data-ttu-id="29a57-128">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="29a57-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="29a57-129">MAPIProfileFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="29a57-129">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="29a57-130">HrRemoveProfile</span><span class="sxs-lookup"><span data-stu-id="29a57-130">HrRemoveProfile</span></span>  <br/> |<span data-ttu-id="29a57-131">MFCMAPI usa el método **IProfAdmin::D eleteprofile** para eliminar el perfil seleccionado.</span><span class="sxs-lookup"><span data-stu-id="29a57-131">MFCMAPI uses the **IProfAdmin::DeleteProfile** method to delete the selected profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="29a57-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="29a57-132">See also</span></span>



[<span data-ttu-id="29a57-133">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="29a57-133">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="29a57-134">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="29a57-134">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="29a57-135">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="29a57-135">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="29a57-136">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="29a57-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

