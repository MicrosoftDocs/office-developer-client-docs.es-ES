---
title: IProfAdminAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.AdminServices
api_type:
- COM
ms.assetid: 87235fd2-6527-41a1-98ba-b951632a1c81
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7566bb075c2ef9903b5a376fd90f209c8683c31e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817888"
---
# <a name="iprofadminadminservices"></a><span data-ttu-id="7ab36-103">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="7ab36-103">IProfAdmin::AdminServices</span></span>

  
  
<span data-ttu-id="7ab36-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7ab36-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7ab36-105">Proporciona acceso a un objeto de administración del servicio de mensajes para realizar cambios en los servicios de mensaje en un perfil.</span><span class="sxs-lookup"><span data-stu-id="7ab36-105">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>
  
```cpp
HRESULT AdminServices(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="7ab36-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7ab36-106">Parameters</span></span>

 <span data-ttu-id="7ab36-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="7ab36-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="7ab36-108">[entrada] Un puntero al nombre del perfil que desea modificar.</span><span class="sxs-lookup"><span data-stu-id="7ab36-108">[in] A pointer to the name of the profile to be modified.</span></span> <span data-ttu-id="7ab36-109">El parámetro _lpszProfileName_ no debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="7ab36-109">The  _lpszProfileName_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="7ab36-110">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="7ab36-110">_lpszPassword_</span></span>
  
> <span data-ttu-id="7ab36-111">[entrada] Siempre es NULL.</span><span class="sxs-lookup"><span data-stu-id="7ab36-111">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="7ab36-112">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="7ab36-112">_ulUIParam_</span></span>
  
> <span data-ttu-id="7ab36-113">[entrada] Identificador de la ventana principal de los cuadros de diálogo o windows que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="7ab36-113">[in] A handle of the parent window for any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="7ab36-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7ab36-114">_ulFlags_</span></span>
  
> <span data-ttu-id="7ab36-115">[entrada] Una máscara de bits de indicadores que controla la recuperación del objeto de administración de servicio de mensaje.</span><span class="sxs-lookup"><span data-stu-id="7ab36-115">[in] A bitmask of flags that controls the retrieval of the message service administration object.</span></span> <span data-ttu-id="7ab36-116">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="7ab36-116">The following flags can be set:</span></span>
    
<span data-ttu-id="7ab36-117">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="7ab36-117">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="7ab36-118">Habilita la presentación de una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="7ab36-118">Enables the display of a user interface.</span></span> 
    
<span data-ttu-id="7ab36-119">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="7ab36-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7ab36-120">El nombre del perfil está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="7ab36-120">The profile name is in Unicode format.</span></span> <span data-ttu-id="7ab36-121">Si no está establecido el indicador MAPI_UNICODE., el nombre está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="7ab36-121">If the MAPI_UNICODE flag is not set, the name is in ANSI format.</span></span>
    
 <span data-ttu-id="7ab36-122">_lppServiceAdmin_</span><span class="sxs-lookup"><span data-stu-id="7ab36-122">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="7ab36-123">[out] Un puntero a un puntero a un objeto de administración del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7ab36-123">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7ab36-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7ab36-124">Return value</span></span>

<span data-ttu-id="7ab36-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="7ab36-125">S_OK</span></span> 
  
> <span data-ttu-id="7ab36-126">El objeto de administración del servicio de mensajes se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="7ab36-126">The message service administration object was successfully returned.</span></span>
    
<span data-ttu-id="7ab36-127">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="7ab36-127">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="7ab36-128">El perfil especificado no existe, o la contraseña es incorrecta y no se pudo mostrar un cuadro de diálogo al usuario para solicitar la contraseña correcta debido a que no se estableció en MAPI_DIALOG en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="7ab36-128">The specified profile does not exist, or the password was wrong and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in  _ulFlags_.</span></span>
    
<span data-ttu-id="7ab36-129">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="7ab36-129">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="7ab36-130">El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7ab36-130">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7ab36-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7ab36-131">Remarks</span></span>

<span data-ttu-id="7ab36-132">El método **IProfAdmin::AdminServices** proporciona acceso a un objeto de administración del servicio de mensajes para realizar cambios en los servicios de mensaje en un perfil de configuración.</span><span class="sxs-lookup"><span data-stu-id="7ab36-132">The **IProfAdmin::AdminServices** method provides access to a message service administration object for making configuration changes to the message services in a profile.</span></span> 
  
 <span data-ttu-id="7ab36-133">El parámetro _lpszPassword_ debe ser NULL o un puntero a una cadena de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="7ab36-133">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7ab36-134">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="7ab36-134">Notes to callers</span></span>

<span data-ttu-id="7ab36-135">Aunque puede recuperar un puntero [IMsgServiceAdmin](imsgserviceadminiunknown.md) mediante una llamada a este método o el [IMAPISession::AdminServices](imapisession-adminservices.md), llamar a **IProfAdmin::AdminServices** si tiene un cliente de configuración de manera estricta y ofrecer no hay características de mensajería.</span><span class="sxs-lookup"><span data-stu-id="7ab36-135">Although you can retrieve an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer by calling either this method or [IMAPISession::AdminServices](imapisession-adminservices.md), call **IProfAdmin::AdminServices** if you have strictly a configuration client and offer no messaging features.</span></span> <span data-ttu-id="7ab36-136">**IProfAdmin::AdminServices** no crea un objeto de sesión y no se carga ningún proveedor de servicios, que mejora el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="7ab36-136">**IProfAdmin::AdminServices** does not create a session object and does not load any service providers, which enhances performance.</span></span> 
  
<span data-ttu-id="7ab36-137">No se puede usar **IProfAdmin::AdminServices** para crear un perfil.</span><span class="sxs-lookup"><span data-stu-id="7ab36-137">You cannot use **IProfAdmin::AdminServices** to create a profile.</span></span> <span data-ttu-id="7ab36-138">Por lo tanto, debe especificar un perfil existente válido en _lpszProfileName_.</span><span class="sxs-lookup"><span data-stu-id="7ab36-138">Therefore, you must specify an existing valid profile in  _lpszProfileName_.</span></span> <span data-ttu-id="7ab36-139">Si no existe el perfil especificado, **IProfAdmin::AdminServices** devuelve MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="7ab36-139">If the specified profile does not exist, **IProfAdmin::AdminServices** returns MAPI_E_LOGON_FAILED.</span></span> 
  
<span data-ttu-id="7ab36-140">El nombre del perfil puede tener hasta 64 caracteres de longitud y puede incluir los siguientes caracteres:</span><span class="sxs-lookup"><span data-stu-id="7ab36-140">The name of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="7ab36-141">Todos los caracteres alfanuméricos, incluidos los caracteres de énfasis y el carácter de subrayado.</span><span class="sxs-lookup"><span data-stu-id="7ab36-141">All alphanumeric characters, including accent characters and the underscore character.</span></span> 
    
- <span data-ttu-id="7ab36-142">Espacios incrustados, pero no espacios al principio o al final.</span><span class="sxs-lookup"><span data-stu-id="7ab36-142">Embedded spaces, but not leading or trailing spaces.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="7ab36-143">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7ab36-143">MFCMAPI reference</span></span>

<span data-ttu-id="7ab36-144">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="7ab36-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7ab36-145">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="7ab36-145">**File**</span></span>|<span data-ttu-id="7ab36-146">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="7ab36-146">**Function**</span></span>|<span data-ttu-id="7ab36-147">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="7ab36-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7ab36-148">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="7ab36-148">MAPIProfileFunctions.cpp</span></span>  <br/> | <span data-ttu-id="7ab36-149">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="7ab36-149">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="7ab36-150">MFCMAPI utiliza el método **IProfAdmin::AdminServices** para abrir un objeto de administración del servicio de mensajes para el perfil seleccionado agregar servicios.</span><span class="sxs-lookup"><span data-stu-id="7ab36-150">MFCMAPI uses the **IProfAdmin::AdminServices** method to open a message service administration object for the selected profile to add services.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7ab36-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ab36-151">See also</span></span>



[<span data-ttu-id="7ab36-152">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="7ab36-152">IMAPISession::AdminServices</span></span>](imapisession-adminservices.md)
  
[<span data-ttu-id="7ab36-153">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7ab36-153">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="7ab36-154">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="7ab36-154">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
