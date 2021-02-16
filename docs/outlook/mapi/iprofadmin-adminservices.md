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
ms.openlocfilehash: 2c504f98655e35af62810dd428e8e04878a36dec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422085"
---
# <a name="iprofadminadminservices"></a><span data-ttu-id="a236a-103">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="a236a-103">IProfAdmin::AdminServices</span></span>

  
  
<span data-ttu-id="a236a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a236a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a236a-105">Proporciona acceso a un objeto de administración del servicio de mensajes para realizar cambios en los servicios de mensajes de un perfil.</span><span class="sxs-lookup"><span data-stu-id="a236a-105">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>
  
```cpp
HRESULT AdminServices(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="a236a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a236a-106">Parameters</span></span>

 <span data-ttu-id="a236a-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="a236a-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="a236a-108">[entrada] Puntero al nombre del perfil que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="a236a-108">[in] A pointer to the name of the profile to be modified.</span></span> <span data-ttu-id="a236a-109">El  _parámetro lpszProfileName_ no debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="a236a-109">The  _lpszProfileName_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="a236a-110">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="a236a-110">_lpszPassword_</span></span>
  
> <span data-ttu-id="a236a-111">[entrada] Siempre NULL.</span><span class="sxs-lookup"><span data-stu-id="a236a-111">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="a236a-112">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a236a-112">_ulUIParam_</span></span>
  
> <span data-ttu-id="a236a-113">[entrada] Identificador de la ventana primaria para los cuadros de diálogo o ventanas que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="a236a-113">[in] A handle of the parent window for any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="a236a-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a236a-114">_ulFlags_</span></span>
  
> <span data-ttu-id="a236a-115">[entrada] Máscara de bits de marcas que controla la recuperación del objeto de administración del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a236a-115">[in] A bitmask of flags that controls the retrieval of the message service administration object.</span></span> <span data-ttu-id="a236a-116">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="a236a-116">The following flags can be set:</span></span>
    
<span data-ttu-id="a236a-117">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a236a-117">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="a236a-118">Habilita la visualización de una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="a236a-118">Enables the display of a user interface.</span></span> 
    
<span data-ttu-id="a236a-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a236a-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a236a-120">El nombre del perfil está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a236a-120">The profile name is in Unicode format.</span></span> <span data-ttu-id="a236a-121">Si no MAPI_UNICODE marca, el nombre está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="a236a-121">If the MAPI_UNICODE flag is not set, the name is in ANSI format.</span></span>
    
 <span data-ttu-id="a236a-122">_lppServiceAdmin_</span><span class="sxs-lookup"><span data-stu-id="a236a-122">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="a236a-123">[salida] Puntero a un puntero a un objeto de administración del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a236a-123">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a236a-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a236a-124">Return value</span></span>

<span data-ttu-id="a236a-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="a236a-125">S_OK</span></span> 
  
> <span data-ttu-id="a236a-126">El objeto de administración del servicio de mensajes se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="a236a-126">The message service administration object was successfully returned.</span></span>
    
<span data-ttu-id="a236a-127">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="a236a-127">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="a236a-128">El perfil especificado no existe o la contraseña fue incorrecta y no se pudo mostrar un cuadro de diálogo al usuario para solicitar la contraseña correcta porque MAPI_DIALOG no se estableció en  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="a236a-128">The specified profile does not exist, or the password was wrong and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in  _ulFlags_.</span></span>
    
<span data-ttu-id="a236a-129">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="a236a-129">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="a236a-130">El usuario canceló la operación, normalmente haciendo clic en el **botón** Cancelar de un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a236a-130">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a236a-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a236a-131">Remarks</span></span>

<span data-ttu-id="a236a-132">El **método IProfAdmin::AdminServices** proporciona acceso a un objeto de administración del servicio de mensajes para realizar cambios en la configuración de los servicios de mensajes en un perfil.</span><span class="sxs-lookup"><span data-stu-id="a236a-132">The **IProfAdmin::AdminServices** method provides access to a message service administration object for making configuration changes to the message services in a profile.</span></span> 
  
 <span data-ttu-id="a236a-133">El  _parámetro lpszPassword_ debe ser NULL o un puntero a una cadena de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="a236a-133">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a236a-134">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="a236a-134">Notes to callers</span></span>

<span data-ttu-id="a236a-135">Aunque puede recuperar un puntero [IMsgServiceAdmin](imsgserviceadminiunknown.md) llamando a este método o [IMAPISession::AdminServices,](imapisession-adminservices.md)llame a **IProfAdmin::AdminServices** si tiene estrictamente un cliente de configuración y no ofrece características de mensajería.</span><span class="sxs-lookup"><span data-stu-id="a236a-135">Although you can retrieve an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer by calling either this method or [IMAPISession::AdminServices](imapisession-adminservices.md), call **IProfAdmin::AdminServices** if you have strictly a configuration client and offer no messaging features.</span></span> <span data-ttu-id="a236a-136">**IProfAdmin::AdminServices** no crea un objeto de sesión y no carga ningún proveedor de servicios, lo que mejora el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a236a-136">**IProfAdmin::AdminServices** does not create a session object and does not load any service providers, which enhances performance.</span></span> 
  
<span data-ttu-id="a236a-137">No puede usar **IProfAdmin::AdminServices** para crear un perfil.</span><span class="sxs-lookup"><span data-stu-id="a236a-137">You cannot use **IProfAdmin::AdminServices** to create a profile.</span></span> <span data-ttu-id="a236a-138">Por lo tanto, debe especificar un perfil válido existente  _en lpszProfileName_.</span><span class="sxs-lookup"><span data-stu-id="a236a-138">Therefore, you must specify an existing valid profile in  _lpszProfileName_.</span></span> <span data-ttu-id="a236a-139">Si el perfil especificado no existe, **IProfAdmin::AdminServices** devuelve MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="a236a-139">If the specified profile does not exist, **IProfAdmin::AdminServices** returns MAPI_E_LOGON_FAILED.</span></span> 
  
<span data-ttu-id="a236a-140">El nombre del perfil puede tener hasta 64 caracteres de longitud y puede incluir los siguientes caracteres:</span><span class="sxs-lookup"><span data-stu-id="a236a-140">The name of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="a236a-141">Todos los caracteres alfanuméricos, incluidos los caracteres de énfrica y el carácter de subrayado.</span><span class="sxs-lookup"><span data-stu-id="a236a-141">All alphanumeric characters, including accent characters and the underscore character.</span></span> 
    
- <span data-ttu-id="a236a-142">Espacios incrustados, pero no espacios iniciales o finales.</span><span class="sxs-lookup"><span data-stu-id="a236a-142">Embedded spaces, but not leading or trailing spaces.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="a236a-143">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a236a-143">MFCMAPI reference</span></span>

<span data-ttu-id="a236a-144">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="a236a-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a236a-145">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="a236a-145">**File**</span></span>|<span data-ttu-id="a236a-146">**Función**</span><span class="sxs-lookup"><span data-stu-id="a236a-146">**Function**</span></span>|<span data-ttu-id="a236a-147">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="a236a-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a236a-148">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="a236a-148">MAPIProfileFunctions.cpp</span></span>  <br/> | <span data-ttu-id="a236a-149">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="a236a-149">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="a236a-150">MFCMAPI usa el **método IProfAdmin::AdminServices** para abrir un objeto de administración de servicio de mensajes para el perfil seleccionado para agregar servicios.</span><span class="sxs-lookup"><span data-stu-id="a236a-150">MFCMAPI uses the **IProfAdmin::AdminServices** method to open a message service administration object for the selected profile to add services.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a236a-151">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a236a-151">See also</span></span>



[<span data-ttu-id="a236a-152">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="a236a-152">IMAPISession::AdminServices</span></span>](imapisession-adminservices.md)
  
[<span data-ttu-id="a236a-153">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a236a-153">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="a236a-154">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="a236a-154">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

