---
title: IProfAdminCreateProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CreateProfile
api_type:
- COM
ms.assetid: 10cda14a-8f93-41e0-b1fb-500098bdc392
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b104c62eb617e6c68f85dea4ef6379c831733844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404403"
---
# <a name="iprofadmincreateprofile"></a><span data-ttu-id="49887-103">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="49887-103">IProfAdmin::CreateProfile</span></span>

  
  
<span data-ttu-id="49887-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49887-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49887-105">Crea un nuevo perfil.</span><span class="sxs-lookup"><span data-stu-id="49887-105">Creates a new profile.</span></span>
  
```cpp
HRESULT CreateProfile(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="49887-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="49887-106">Parameters</span></span>

 <span data-ttu-id="49887-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="49887-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="49887-108">[in] Puntero al nombre del nuevo perfil.</span><span class="sxs-lookup"><span data-stu-id="49887-108">[in] A pointer to the name of the new profile.</span></span>
    
 <span data-ttu-id="49887-109">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="49887-109">_lpszPassword_</span></span>
  
> <span data-ttu-id="49887-110">[in] Puntero a la contraseña del nuevo perfil.</span><span class="sxs-lookup"><span data-stu-id="49887-110">[in] A pointer to the password of the new profile.</span></span> 
    
 <span data-ttu-id="49887-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="49887-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="49887-112">[in] Identificador de la ventana principal de los cuadros de diálogo o ventanas que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="49887-112">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="49887-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="49887-113">_ulFlags_</span></span>
  
> <span data-ttu-id="49887-114">[in] Máscara de bits de marcas que controla cómo se crea el perfil.</span><span class="sxs-lookup"><span data-stu-id="49887-114">[in] A bitmask of flags that controls how the profile is created.</span></span> <span data-ttu-id="49887-115">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="49887-115">The following flags can be set:</span></span>
    
<span data-ttu-id="49887-116">MAPI_DEFAULT_SERVICES</span><span class="sxs-lookup"><span data-stu-id="49887-116">MAPI_DEFAULT_SERVICES</span></span> 
  
> <span data-ttu-id="49887-117">MAPI debe rellenar el nuevo perfil con los servicios de mensajes que se incluyen en la sección [Servicios predeterminados] del archivo Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="49887-117">MAPI should populate the new profile with the message services that are included in the [Default Services] section of the Mapisvc.inf file.</span></span>
    
<span data-ttu-id="49887-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="49887-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="49887-119">Se pueden mostrar las hojas de propiedades de configuración de cada uno de los proveedores de los servicios de mensajes que se van a agregar.</span><span class="sxs-lookup"><span data-stu-id="49887-119">The configuration property sheets of each of the providers in the message services to be added can be displayed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="49887-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49887-120">Return value</span></span>

<span data-ttu-id="49887-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="49887-121">S_OK</span></span> 
  
> <span data-ttu-id="49887-122">Se creó el nuevo perfil.</span><span class="sxs-lookup"><span data-stu-id="49887-122">The new profile was created.</span></span>
    
<span data-ttu-id="49887-123">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="49887-123">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="49887-124">El nuevo perfil especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="49887-124">The specified new profile already exists.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="49887-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="49887-125">Remarks</span></span>

<span data-ttu-id="49887-126">El **método IProfAdmin::CreateProfile** crea un nuevo perfil.</span><span class="sxs-lookup"><span data-stu-id="49887-126">The **IProfAdmin::CreateProfile** method creates a new profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="49887-127">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="49887-127">Notes to callers</span></span>

<span data-ttu-id="49887-128">Puede llamar a **CreateProfile en** el momento de la instalación de la aplicación o en cualquier momento durante una sesión.</span><span class="sxs-lookup"><span data-stu-id="49887-128">You can call **CreateProfile** at application installation time or at any time during a session.</span></span> <span data-ttu-id="49887-129">Cuando se llama a este método en el momento de la instalación, muchas de las opciones de configuración proceden del archivo de configuración Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="49887-129">When this method is called at installation time, many of the configuration settings come from the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="49887-130">Cuando se llama a este método durante una sesión activa, la configuración procede del usuario al que se le pide una serie de hojas de propiedades.</span><span class="sxs-lookup"><span data-stu-id="49887-130">When this method is called during an active session, the settings come from the user who is prompted through a series of property sheets.</span></span> 
  
<span data-ttu-id="49887-131">Si la marca MAPI_DEFAULT_SERVICES se establece en el parámetro  _ulFlags,_ **CreateProfile** llama a la función de punto de entrada del servicio de mensajes para cada servicio de mensajes en la sección [Servicios predeterminados] del archivo Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="49887-131">If the MAPI_DEFAULT_SERVICES flag is set in the  _ulFlags_ parameter, **CreateProfile** calls the message service entry point function for each message service in the [Default Services] section in the Mapisvc.inf file.</span></span> <span data-ttu-id="49887-132">Se llama a cada función de punto de entrada del servicio de mensajes con el parámetro  _ulContext_ establecido en MSG_SERVICE_CREATE.</span><span class="sxs-lookup"><span data-stu-id="49887-132">Each message service entry point function is called with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
  
<span data-ttu-id="49887-133">Si se establecen las marcas MAPI_DIALOG y MAPI_DEFAULT_SERVICES, los valores de los parámetros  _ulUIParam_ y  _ulFlags_ también se pasan a la función de punto de entrada del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="49887-133">If both the MAPI_DIALOG and MAPI_DEFAULT_SERVICES flags are set, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the message service entry point function.</span></span> <span data-ttu-id="49887-134">Solo se llama a las funciones de punto de entrada del servicio de mensajes después de que toda la información disponible del archivo Mapisvc.inf se haya agregado al perfil.</span><span class="sxs-lookup"><span data-stu-id="49887-134">The message service entry point functions are called only after all available information from the Mapisvc.inf file has been added to the profile.</span></span> 
  
<span data-ttu-id="49887-135">El nombre del nuevo perfil y su contraseña pueden tener hasta 64 caracteres y pueden incluir los siguientes caracteres:</span><span class="sxs-lookup"><span data-stu-id="49887-135">The name of the new profile and its password can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="49887-136">Todos los caracteres alfanuméricos, incluidos los caracteres de énfrica y el carácter de subrayado.</span><span class="sxs-lookup"><span data-stu-id="49887-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="49887-137">Espacios incrustados, pero no espacios iniciales o finales.</span><span class="sxs-lookup"><span data-stu-id="49887-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="49887-138">El  _parámetro lpszPassword_ debe ser NULL o un puntero a una cadena de longitud cero.</span><span class="sxs-lookup"><span data-stu-id="49887-138">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="49887-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="49887-139">See also</span></span>



[<span data-ttu-id="49887-140">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="49887-140">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="49887-141">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="49887-141">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="49887-142">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="49887-142">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="49887-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="49887-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

