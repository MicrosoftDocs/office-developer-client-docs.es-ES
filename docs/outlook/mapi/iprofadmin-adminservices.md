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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309600"
---
# <a name="iprofadminadminservices"></a><span data-ttu-id="d00a3-103">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="d00a3-103">IProfAdmin::AdminServices</span></span>

  
  
<span data-ttu-id="d00a3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d00a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d00a3-105">Proporciona acceso a un objeto de administración del servicio de mensajes para realizar cambios en los servicios de mensajes de un perfil.</span><span class="sxs-lookup"><span data-stu-id="d00a3-105">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>
  
```cpp
HRESULT AdminServices(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="d00a3-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d00a3-106">Parameters</span></span>

 <span data-ttu-id="d00a3-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="d00a3-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="d00a3-108">a Un puntero al nombre del perfil que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="d00a3-108">[in] A pointer to the name of the profile to be modified.</span></span> <span data-ttu-id="d00a3-109">El parámetro _lpszProfileName_ no debe ser nulo.</span><span class="sxs-lookup"><span data-stu-id="d00a3-109">The  _lpszProfileName_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="d00a3-110">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="d00a3-110">_lpszPassword_</span></span>
  
> <span data-ttu-id="d00a3-111">a Siempre NULL.</span><span class="sxs-lookup"><span data-stu-id="d00a3-111">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="d00a3-112">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d00a3-112">_ulUIParam_</span></span>
  
> <span data-ttu-id="d00a3-113">a Identificador de la ventana primaria para los cuadros de diálogo o ventanas que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="d00a3-113">[in] A handle of the parent window for any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="d00a3-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d00a3-114">_ulFlags_</span></span>
  
> <span data-ttu-id="d00a3-115">a Una máscara de máscara de marcadores que controla la recuperación del objeto de administración del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d00a3-115">[in] A bitmask of flags that controls the retrieval of the message service administration object.</span></span> <span data-ttu-id="d00a3-116">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="d00a3-116">The following flags can be set:</span></span>
    
<span data-ttu-id="d00a3-117">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="d00a3-117">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="d00a3-118">Habilita la visualización de una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="d00a3-118">Enables the display of a user interface.</span></span> 
    
<span data-ttu-id="d00a3-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d00a3-119">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d00a3-120">El nombre del perfil está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="d00a3-120">The profile name is in Unicode format.</span></span> <span data-ttu-id="d00a3-121">Si no se establece la marca MAPI_UNICODE, el nombre está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="d00a3-121">If the MAPI_UNICODE flag is not set, the name is in ANSI format.</span></span>
    
 <span data-ttu-id="d00a3-122">_lppServiceAdmin_</span><span class="sxs-lookup"><span data-stu-id="d00a3-122">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="d00a3-123">contempla Un puntero a un puntero a un objeto de administración del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d00a3-123">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d00a3-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d00a3-124">Return value</span></span>

<span data-ttu-id="d00a3-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="d00a3-125">S_OK</span></span> 
  
> <span data-ttu-id="d00a3-126">El objeto de administración del servicio de mensajes se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="d00a3-126">The message service administration object was successfully returned.</span></span>
    
<span data-ttu-id="d00a3-127">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="d00a3-127">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="d00a3-128">El perfil especificado no existe o la contraseña era incorrecta y no se pudo mostrar un cuadro de diálogo al usuario para solicitar la contraseña correcta porque MAPI_DIALOG no se estableció en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="d00a3-128">The specified profile does not exist, or the password was wrong and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in  _ulFlags_.</span></span>
    
<span data-ttu-id="d00a3-129">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="d00a3-129">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="d00a3-130">El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d00a3-130">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d00a3-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d00a3-131">Remarks</span></span>

<span data-ttu-id="d00a3-132">El método **IProfAdmin:: AdminServices** proporciona acceso a un objeto de administración del servicio de mensajes para realizar cambios en la configuración de los servicios de mensajes en un perfil.</span><span class="sxs-lookup"><span data-stu-id="d00a3-132">The **IProfAdmin::AdminServices** method provides access to a message service administration object for making configuration changes to the message services in a profile.</span></span> 
  
 <span data-ttu-id="d00a3-133">El parámetro _lpszPassword_ debe ser null o un puntero a una cadena de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="d00a3-133">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d00a3-134">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="d00a3-134">Notes to callers</span></span>

<span data-ttu-id="d00a3-135">Aunque puede recuperar un puntero [IMsgServiceAdmin](imsgserviceadminiunknown.md) llamando a este método o a [IMAPISession:: AdminServices](imapisession-adminservices.md), llamar a **IProfAdmin:: AdminServices** si tiene estrictamente un cliente de configuración y no ofrece características de mensajería.</span><span class="sxs-lookup"><span data-stu-id="d00a3-135">Although you can retrieve an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer by calling either this method or [IMAPISession::AdminServices](imapisession-adminservices.md), call **IProfAdmin::AdminServices** if you have strictly a configuration client and offer no messaging features.</span></span> <span data-ttu-id="d00a3-136">**IProfAdmin:: AdminServices** no crea un objeto Session y no carga ningún proveedor de servicios, lo que mejora el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="d00a3-136">**IProfAdmin::AdminServices** does not create a session object and does not load any service providers, which enhances performance.</span></span> 
  
<span data-ttu-id="d00a3-137">No puede usar **IProfAdmin:: AdminServices** para crear un perfil.</span><span class="sxs-lookup"><span data-stu-id="d00a3-137">You cannot use **IProfAdmin::AdminServices** to create a profile.</span></span> <span data-ttu-id="d00a3-138">Por lo tanto, debe especificar un perfil válido existente en _lpszProfileName_.</span><span class="sxs-lookup"><span data-stu-id="d00a3-138">Therefore, you must specify an existing valid profile in  _lpszProfileName_.</span></span> <span data-ttu-id="d00a3-139">Si el perfil especificado no existe, **IProfAdmin:: AdminServices** devuelve MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="d00a3-139">If the specified profile does not exist, **IProfAdmin::AdminServices** returns MAPI_E_LOGON_FAILED.</span></span> 
  
<span data-ttu-id="d00a3-140">El nombre del perfil puede tener hasta 64 caracteres de longitud y puede incluir los siguientes caracteres:</span><span class="sxs-lookup"><span data-stu-id="d00a3-140">The name of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="d00a3-141">Todos los caracteres alfanuméricos, incluidos los caracteres de énfasis y el carácter de subrayado.</span><span class="sxs-lookup"><span data-stu-id="d00a3-141">All alphanumeric characters, including accent characters and the underscore character.</span></span> 
    
- <span data-ttu-id="d00a3-142">Espacios insertados, pero no espacios iniciales ni finales.</span><span class="sxs-lookup"><span data-stu-id="d00a3-142">Embedded spaces, but not leading or trailing spaces.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="d00a3-143">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d00a3-143">MFCMAPI reference</span></span>

<span data-ttu-id="d00a3-144">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="d00a3-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d00a3-145">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="d00a3-145">**File**</span></span>|<span data-ttu-id="d00a3-146">**Función**</span><span class="sxs-lookup"><span data-stu-id="d00a3-146">**Function**</span></span>|<span data-ttu-id="d00a3-147">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="d00a3-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d00a3-148">MAPIProfileFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="d00a3-148">MAPIProfileFunctions.cpp</span></span>  <br/> | <span data-ttu-id="d00a3-149">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="d00a3-149">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="d00a3-150">MFCMAPI usa el método **IProfAdmin:: AdminServices** para abrir un objeto de administración del servicio de mensajes para el perfil seleccionado para agregar servicios.</span><span class="sxs-lookup"><span data-stu-id="d00a3-150">MFCMAPI uses the **IProfAdmin::AdminServices** method to open a message service administration object for the selected profile to add services.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d00a3-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="d00a3-151">See also</span></span>



[<span data-ttu-id="d00a3-152">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="d00a3-152">IMAPISession::AdminServices</span></span>](imapisession-adminservices.md)
  
[<span data-ttu-id="d00a3-153">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d00a3-153">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="d00a3-154">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="d00a3-154">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

