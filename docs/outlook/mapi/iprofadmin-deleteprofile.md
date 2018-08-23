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
ms.openlocfilehash: aa3c010eafeba7908498965bc0491c993a4a9120
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572096"
---
# <a name="iprofadmindeleteprofile"></a><span data-ttu-id="26b5b-103">IProfAdmin::DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="26b5b-103">IProfAdmin::DeleteProfile</span></span>

  
  
<span data-ttu-id="26b5b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26b5b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26b5b-105">Elimina un perfil.</span><span class="sxs-lookup"><span data-stu-id="26b5b-105">Deletes a profile.</span></span>
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="26b5b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26b5b-106">Parameters</span></span>

 <span data-ttu-id="26b5b-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="26b5b-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="26b5b-108">[entrada] Un puntero al nombre del perfil que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="26b5b-108">[in] A pointer to the name of the profile to be deleted.</span></span>
    
 <span data-ttu-id="26b5b-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="26b5b-109">_ulFlags_</span></span>
  
> <span data-ttu-id="26b5b-110">[entrada] Siempre es NULL.</span><span class="sxs-lookup"><span data-stu-id="26b5b-110">[in] Always NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="26b5b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26b5b-111">Return value</span></span>

<span data-ttu-id="26b5b-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="26b5b-112">S_OK</span></span> 
  
> <span data-ttu-id="26b5b-113">El perfil se eliminó correctamente.</span><span class="sxs-lookup"><span data-stu-id="26b5b-113">The profile was successfully deleted.</span></span>
    
<span data-ttu-id="26b5b-114">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="26b5b-114">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="26b5b-115">No existe el perfil especificado.</span><span class="sxs-lookup"><span data-stu-id="26b5b-115">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="26b5b-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="26b5b-116">Remarks</span></span>

<span data-ttu-id="26b5b-117">El método **IProfAdmin::DeleteProfile** elimina un perfil.</span><span class="sxs-lookup"><span data-stu-id="26b5b-117">The **IProfAdmin::DeleteProfile** method deletes a profile.</span></span> <span data-ttu-id="26b5b-118">Si el perfil que desea eliminar está en uso cuando se llama a **DeleteProfile** , **DeleteProfile** devuelve S_OK, pero no se elimina inmediatamente el perfil.</span><span class="sxs-lookup"><span data-stu-id="26b5b-118">If the profile to delete is in use when **DeleteProfile** is called, **DeleteProfile** returns S_OK but does not delete the profile immediately.</span></span> <span data-ttu-id="26b5b-119">En su lugar, **DeleteProfile** marca el perfil para su eliminación y se elimina después de ya no se usa, cuando todos sus sesiones activas han finalizado.</span><span class="sxs-lookup"><span data-stu-id="26b5b-119">Instead, **DeleteProfile** marks the profile for deletion and deletes it after it is no longer being used, when all of its active sessions have ended.</span></span> 
  
<span data-ttu-id="26b5b-120">La función de punto de entrada para cada servicio de mensajes en el perfil se llama con el valor MSG_SERVICE_DELETE establecido en el parámetro _ulContext_ .</span><span class="sxs-lookup"><span data-stu-id="26b5b-120">The entry point function for each message service in the profile is called with the MSG_SERVICE_DELETE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="26b5b-121">En primer lugar, la función elimina el servicio y, a continuación, elimina la sección de perfil del servicio.</span><span class="sxs-lookup"><span data-stu-id="26b5b-121">First, the function deletes the service, and then it deletes the service's profile section.</span></span> <span data-ttu-id="26b5b-122">La función de punto de entrada de servicio de mensajes no se llama de nuevo después de que se ha eliminado el servicio.</span><span class="sxs-lookup"><span data-stu-id="26b5b-122">The message service entry point function is not called again after the service has been deleted.</span></span> 
  
<span data-ttu-id="26b5b-123">Para eliminar un perfil no se requiere ninguna contraseña.</span><span class="sxs-lookup"><span data-stu-id="26b5b-123">No password is required to delete a profile.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="26b5b-124">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="26b5b-124">MFCMAPI reference</span></span>

<span data-ttu-id="26b5b-125">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="26b5b-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="26b5b-126">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="26b5b-126">**File**</span></span>|<span data-ttu-id="26b5b-127">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="26b5b-127">**Function**</span></span>|<span data-ttu-id="26b5b-128">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="26b5b-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="26b5b-129">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="26b5b-129">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="26b5b-130">HrRemoveProfile</span><span class="sxs-lookup"><span data-stu-id="26b5b-130">HrRemoveProfile</span></span>  <br/> |<span data-ttu-id="26b5b-131">MFCMAPI usa el método **IProfAdmin::DeleteProfile** para eliminar el perfil seleccionado.</span><span class="sxs-lookup"><span data-stu-id="26b5b-131">MFCMAPI uses the **IProfAdmin::DeleteProfile** method to delete the selected profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="26b5b-132">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="26b5b-132">See also</span></span>



[<span data-ttu-id="26b5b-133">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="26b5b-133">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="26b5b-134">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="26b5b-134">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="26b5b-135">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="26b5b-135">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="26b5b-136">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="26b5b-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

