---
title: LAUNCHWIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LAUNCHWIZARDENTRY
api_type:
- COM
ms.assetid: 5778dffa-f01b-46b3-9c19-862793740918
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c1509918eb587c17deebf95317cf57b4ab19928a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270192"
---
# <a name="launchwizardentry"></a><span data-ttu-id="4bff7-103">LAUNCHWIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="4bff7-103">LAUNCHWIZARDENTRY</span></span>

  
  
<span data-ttu-id="4bff7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4bff7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4bff7-105">Define una función que inicia la aplicación del Asistente para perfiles con el fin de agregar uno o más servicios de mensajes a un perfil.</span><span class="sxs-lookup"><span data-stu-id="4bff7-105">Defines a function that starts the Profile Wizard application for the purpose of adding one or more message services to a profile.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4bff7-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="4bff7-106">Header file:</span></span>  <br/> |<span data-ttu-id="4bff7-107">Mapiwz. h</span><span class="sxs-lookup"><span data-stu-id="4bff7-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="4bff7-108">Función definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="4bff7-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="4bff7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4bff7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4bff7-110">Función definida llamada por:</span><span class="sxs-lookup"><span data-stu-id="4bff7-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="4bff7-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="4bff7-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT LAUNCHWIZARDENTRY(
  HWND hParentWnd,
  ULONG ulFlags,
  LPCSTR FAR * lppszServiceNameToAdd,
  ULONG cbBufferMax,
  LPSTR lpszNewProfileName
);
```

## <a name="parameters"></a><span data-ttu-id="4bff7-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="4bff7-112">Parameters</span></span>

 <span data-ttu-id="4bff7-113">_hParentWnd_</span><span class="sxs-lookup"><span data-stu-id="4bff7-113">_hParentWnd_</span></span>
  
> <span data-ttu-id="4bff7-114">a Identificador de la ventana primaria del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="4bff7-114">[in] A handle to the caller's parent window.</span></span> <span data-ttu-id="4bff7-115">Si el autor de la llamada no tiene una ventana primaria, el parámetro _hParentWnd_ debe ser nulo.</span><span class="sxs-lookup"><span data-stu-id="4bff7-115">If the caller does not have a parent window, the  _hParentWnd_ parameter should be NULL.</span></span> 
    
 <span data-ttu-id="4bff7-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4bff7-116">_ulFlags_</span></span>
  
> <span data-ttu-id="4bff7-117">a Máscara de máscara de los indicadores que indican opciones para el Asistente para perfiles.</span><span class="sxs-lookup"><span data-stu-id="4bff7-117">[in] Bitmask of flags indicating options for the Profile Wizard.</span></span> <span data-ttu-id="4bff7-118">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="4bff7-118">The following flags can be set:</span></span>
    
<span data-ttu-id="4bff7-119">MAPI_PW_ADD_SERVICE_ONLY</span><span class="sxs-lookup"><span data-stu-id="4bff7-119">MAPI_PW_ADD_SERVICE_ONLY</span></span> 
  
> <span data-ttu-id="4bff7-120">El Asistente para perfiles es agregar únicamente los servicios de mensajes enumerados mediante el parámetro _lppszServiceNameToAdd_ y no mostrar su página para seleccionar los servicios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4bff7-120">The Profile Wizard is to add only the message services listed through the  _lppszServiceNameToAdd_ parameter, and not display its page for selecting message services.</span></span> 
    
<span data-ttu-id="4bff7-121">MAPI_PW_FIRST_PROFILE</span><span class="sxs-lookup"><span data-stu-id="4bff7-121">MAPI_PW_FIRST_PROFILE</span></span> 
  
> <span data-ttu-id="4bff7-122">El perfil que se creará es el primero de esta estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="4bff7-122">The profile to be created is the first one for this workstation.</span></span> 
    
<span data-ttu-id="4bff7-123">MAPI_PW_HIDE_SERVICES_LIST</span><span class="sxs-lookup"><span data-stu-id="4bff7-123">MAPI_PW_HIDE_SERVICES_LIST</span></span> 
  
> <span data-ttu-id="4bff7-124">No debe mostrarse la página del Asistente para perfiles para la selección de servicios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="4bff7-124">The Profile Wizard's page for selecting message services should not be displayed.</span></span> 
    
<span data-ttu-id="4bff7-125">MAPI_PW_LAUNCHED_BY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="4bff7-125">MAPI_PW_LAUNCHED_BY_CONFIG</span></span> 
  
> <span data-ttu-id="4bff7-126">El Asistente para perfiles fue iniciado por la aplicación de configuración del panel de control.</span><span class="sxs-lookup"><span data-stu-id="4bff7-126">The Profile Wizard was launched by the Control Panel configuration application.</span></span> 
    
<span data-ttu-id="4bff7-127">MAPI_PW_PROVIDER_UI_ONLY</span><span class="sxs-lookup"><span data-stu-id="4bff7-127">MAPI_PW_PROVIDER_UI_ONLY</span></span> 
  
> <span data-ttu-id="4bff7-128">Solo se mostrarán los cuadros de diálogo Configuración de los proveedores de servicios y las páginas del Asistente para perfiles no deben aparecer.</span><span class="sxs-lookup"><span data-stu-id="4bff7-128">Only the service providers's configuration dialog boxes should be displayed and the Profile Wizard's pages should not appear.</span></span> <span data-ttu-id="4bff7-129">Esta marca solo se puede establecer si está establecida la marca MAPI_PW_ADD_SERVICE_ONLY.</span><span class="sxs-lookup"><span data-stu-id="4bff7-129">This flag can only be set if the MAPI_PW_ADD_SERVICE_ONLY flag is set.</span></span> 
    
 <span data-ttu-id="4bff7-130">_lppszServiceNameToAdd_</span><span class="sxs-lookup"><span data-stu-id="4bff7-130">_lppszServiceNameToAdd_</span></span>
  
> <span data-ttu-id="4bff7-131">a Puntero a una matriz de cadenas que contiene los nombres de los servicios de mensaje que se van a agregar al perfil.</span><span class="sxs-lookup"><span data-stu-id="4bff7-131">[in] Pointer to an array of strings that contains the names of the message services to be added to the profile.</span></span> <span data-ttu-id="4bff7-132">La matriz debe terminar con un valor NULL.</span><span class="sxs-lookup"><span data-stu-id="4bff7-132">The array must terminate with a NULL value.</span></span> 
    
 <span data-ttu-id="4bff7-133">_cbBufferMax_</span><span class="sxs-lookup"><span data-stu-id="4bff7-133">_cbBufferMax_</span></span>
  
> <span data-ttu-id="4bff7-134">a Tamaño del búfer al que señala el parámetro _lpszNewProfileName_ .</span><span class="sxs-lookup"><span data-stu-id="4bff7-134">[in] Size of the buffer pointed to by the  _lpszNewProfileName_ parameter.</span></span> 
    
 <span data-ttu-id="4bff7-135">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="4bff7-135">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="4bff7-136">contempla Puntero a un búfer de cadena donde la función basada en **LAUNCHWIZARDENTRY** devuelve el nombre del perfil creado.</span><span class="sxs-lookup"><span data-stu-id="4bff7-136">[out] Pointer to a string buffer where the function based on **LAUNCHWIZARDENTRY** returns the name of the created profile.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4bff7-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4bff7-137">Return value</span></span>

<span data-ttu-id="4bff7-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="4bff7-138">S_OK</span></span> 
  
> <span data-ttu-id="4bff7-139">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="4bff7-139">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="4bff7-140">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="4bff7-140">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="4bff7-141">Un error de origen inesperado o desconocido impidió que se completara la operación.</span><span class="sxs-lookup"><span data-stu-id="4bff7-141">An error of unexpected or unknown origin prevented the operation from completing.</span></span> <span data-ttu-id="4bff7-142">Entre las posibilidades se incluye el error al inicializar el subsistema MAPI para el Asistente para perfiles, la incapacidad para obtener acceso al perfil predeterminado y un error de devolución del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4bff7-142">Possibilities include failure to initialize the MAPI subsystem for the Profile Wizard, inability to access the default profile, and an error return from the dialog box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4bff7-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4bff7-143">Remarks</span></span>

<span data-ttu-id="4bff7-144">La implementación de MAPI del prototipo de función **LAUNCHWIZARDENTRY** es el punto de entrada a la aplicación Asistente para perfiles MAPI.</span><span class="sxs-lookup"><span data-stu-id="4bff7-144">The MAPI implementation of the **LAUNCHWIZARDENTRY** function prototype is the entry point into the MAPI Profile Wizard application.</span></span> <span data-ttu-id="4bff7-145">MAPI denomina este punto de entrada **LaunchWizard**.</span><span class="sxs-lookup"><span data-stu-id="4bff7-145">MAPI names this entry point **LaunchWizard**.</span></span> 
  
<span data-ttu-id="4bff7-146">Cuando se establece la marca MAPI_PW_ADD_SERVICE_ONLY en el parámetro _ulFlags_ , se aplican las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="4bff7-146">When the MAPI_PW_ADD_SERVICE_ONLY flag is set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="4bff7-147">La marca MAPI_PW_LAUNCHED_BY_CONFIG impide que se muestre la página de bienvenida.</span><span class="sxs-lookup"><span data-stu-id="4bff7-147">The MAPI_PW_LAUNCHED_BY_CONFIG flag inhibits the welcome page from being displayed.</span></span> 
    
- <span data-ttu-id="4bff7-148">Los indicadores MAPI_PW_HIDE_SERVICES_LIST y MAPI_PW_PROVIDER_UI_ONLY solo son útiles cuando no hay un perfil predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4bff7-148">The MAPI_PW_HIDE_SERVICES_LIST and MAPI_PW_PROVIDER_UI_ONLY flags are useful only when there is no default profile.</span></span> <span data-ttu-id="4bff7-149">En este caso, estos indicadores determinan qué página del asistente de perfil se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="4bff7-149">In this case these flags determine which Profile Wizard page is to be displayed.</span></span> 
    
- <span data-ttu-id="4bff7-150">Si existe un perfil predeterminado, no se mostrará ninguna de las páginas del Asistente para perfiles.</span><span class="sxs-lookup"><span data-stu-id="4bff7-150">If a default profile exists, none of the Profile Wizard pages are to be displayed.</span></span> 
    
- <span data-ttu-id="4bff7-151">Si existe un perfil predeterminado, solo se muestra un servicio de mensajes a través del parámetro _lppszServiceNameToAdd_ y ese servicio de mensajes ya se encuentra en el perfil predeterminado, el Asistente para perfiles Devuelve S_OK sin agregar nada al perfil.</span><span class="sxs-lookup"><span data-stu-id="4bff7-151">If a default profile exists, only one message service is listed through the  _lppszServiceNameToAdd_ parameter, and that message service is already in the default profile, the Profile Wizard returns S_OK without adding anything to the profile.</span></span> 
    
<span data-ttu-id="4bff7-152">Por cada servicio de mensajes que se va a agregar al perfil, el Asistente de perfiles llama a la función de punto de entrada del servicio en función del prototipo [MSGSERVICEENTRY](msgserviceentry.md) .</span><span class="sxs-lookup"><span data-stu-id="4bff7-152">For every message service to be added to the profile, the Profile Wizard calls the service's entry point function based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="4bff7-153">Para cada proveedor de servicios seleccionado de un servicio de mensajes que se va a agregar al perfil, el Asistente de perfiles llama a la función de punto de entrada del proveedor en función del prototipo [WIZARDENTRY](wizardentry.md) .</span><span class="sxs-lookup"><span data-stu-id="4bff7-153">For each service provider selected from a message service to be added to the profile, the Profile Wizard calls the provider's entry point function based on the [WIZARDENTRY](wizardentry.md) prototype.</span></span> <span data-ttu-id="4bff7-154">Durante la configuración interactiva, todos los eventos de usuario en las páginas de propiedades hacen que el Asistente para perfiles llame a la función de devolución de llamada del proveedor en función del prototipo [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) .</span><span class="sxs-lookup"><span data-stu-id="4bff7-154">During interactive configuration, every user event in the property pages causes the Profile Wizard to call the provider's callback function based on the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
  
<span data-ttu-id="4bff7-155">Si un proveedor de servicios que se va a agregar al perfil admite las páginas del Asistente para perfiles, debe permitir la configuración mediante programación del perfil.</span><span class="sxs-lookup"><span data-stu-id="4bff7-155">If a service provider being added to the profile supports the Profile Wizard pages, it must allow programmatic configuration of the profile.</span></span>
  

