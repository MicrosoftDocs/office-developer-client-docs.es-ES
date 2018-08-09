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
ms.openlocfilehash: 249d2dcf3a298abde85bdc53620680146d43c168
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817898"
---
# <a name="iprofadmindeleteprofile"></a><span data-ttu-id="72042-103">IProfAdmin::DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="72042-103">IProfAdmin::DeleteProfile</span></span>

  
  
<span data-ttu-id="72042-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="72042-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="72042-105">Elimina un perfil.</span><span class="sxs-lookup"><span data-stu-id="72042-105">Deletes a profile.</span></span>
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="72042-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72042-106">Parameters</span></span>

 <span data-ttu-id="72042-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="72042-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="72042-108">[entrada] Un puntero al nombre del perfil que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="72042-108">[in] A pointer to the name of the profile to be deleted.</span></span>
    
 <span data-ttu-id="72042-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="72042-109">_ulFlags_</span></span>
  
> <span data-ttu-id="72042-110">[entrada] Siempre es NULL.</span><span class="sxs-lookup"><span data-stu-id="72042-110">[in] Always NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="72042-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72042-111">Return value</span></span>

<span data-ttu-id="72042-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="72042-112">S_OK</span></span> 
  
> <span data-ttu-id="72042-113">El perfil se eliminó correctamente.</span><span class="sxs-lookup"><span data-stu-id="72042-113">The profile was successfully deleted.</span></span>
    
<span data-ttu-id="72042-114">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="72042-114">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="72042-115">No existe el perfil especificado.</span><span class="sxs-lookup"><span data-stu-id="72042-115">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="72042-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="72042-116">Remarks</span></span>

<span data-ttu-id="72042-117">El método **IProfAdmin::DeleteProfile** elimina un perfil.</span><span class="sxs-lookup"><span data-stu-id="72042-117">The **IProfAdmin::DeleteProfile** method deletes a profile.</span></span> <span data-ttu-id="72042-118">Si el perfil que desea eliminar está en uso cuando se llama a **DeleteProfile** , **DeleteProfile** devuelve S_OK, pero no se elimina inmediatamente el perfil.</span><span class="sxs-lookup"><span data-stu-id="72042-118">If the profile to delete is in use when **DeleteProfile** is called, **DeleteProfile** returns S_OK but does not delete the profile immediately.</span></span> <span data-ttu-id="72042-119">En su lugar, **DeleteProfile** marca el perfil para su eliminación y se elimina después de ya no se usa, cuando todos sus sesiones activas han finalizado.</span><span class="sxs-lookup"><span data-stu-id="72042-119">Instead, **DeleteProfile** marks the profile for deletion and deletes it after it is no longer being used, when all of its active sessions have ended.</span></span> 
  
<span data-ttu-id="72042-120">La función de punto de entrada para cada servicio de mensajes en el perfil se llama con el valor MSG_SERVICE_DELETE establecido en el parámetro _ulContext_ .</span><span class="sxs-lookup"><span data-stu-id="72042-120">The entry point function for each message service in the profile is called with the MSG_SERVICE_DELETE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="72042-121">En primer lugar, la función elimina el servicio y, a continuación, elimina la sección de perfil del servicio.</span><span class="sxs-lookup"><span data-stu-id="72042-121">First, the function deletes the service, and then it deletes the service's profile section.</span></span> <span data-ttu-id="72042-122">La función de punto de entrada de servicio de mensajes no se llama de nuevo después de que se ha eliminado el servicio.</span><span class="sxs-lookup"><span data-stu-id="72042-122">The message service entry point function is not called again after the service has been deleted.</span></span> 
  
<span data-ttu-id="72042-123">Para eliminar un perfil no se requiere ninguna contraseña.</span><span class="sxs-lookup"><span data-stu-id="72042-123">No password is required to delete a profile.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="72042-124">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="72042-124">MFCMAPI reference</span></span>

<span data-ttu-id="72042-125">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="72042-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="72042-126">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="72042-126">**File**</span></span>|<span data-ttu-id="72042-127">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="72042-127">**Function**</span></span>|<span data-ttu-id="72042-128">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="72042-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="72042-129">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="72042-129">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="72042-130">HrRemoveProfile</span><span class="sxs-lookup"><span data-stu-id="72042-130">HrRemoveProfile</span></span>  <br/> |<span data-ttu-id="72042-131">MFCMAPI usa el método **IProfAdmin::DeleteProfile** para eliminar el perfil seleccionado.</span><span class="sxs-lookup"><span data-stu-id="72042-131">MFCMAPI uses the **IProfAdmin::DeleteProfile** method to delete the selected profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="72042-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="72042-132">See also</span></span>



[<span data-ttu-id="72042-133">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="72042-133">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="72042-134">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="72042-134">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="72042-135">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="72042-135">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="72042-136">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="72042-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

