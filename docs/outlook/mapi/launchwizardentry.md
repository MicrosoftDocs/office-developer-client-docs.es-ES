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
ms.openlocfilehash: f2cc9a6f97fa51a255f8c24c2bb52c912aef7718
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566253"
---
# <a name="launchwizardentry"></a><span data-ttu-id="96c80-103">LAUNCHWIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="96c80-103">LAUNCHWIZARDENTRY</span></span>

  
  
<span data-ttu-id="96c80-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96c80-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96c80-105">Define una función que inicia la aplicación de Asistente para perfiles con el fin de agregar uno o más servicios de mensaje a un perfil.</span><span class="sxs-lookup"><span data-stu-id="96c80-105">Defines a function that starts the Profile Wizard application for the purpose of adding one or more message services to a profile.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96c80-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="96c80-106">Header file:</span></span>  <br/> |<span data-ttu-id="96c80-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="96c80-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="96c80-108">Función definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="96c80-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="96c80-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="96c80-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="96c80-110">Llamado por una función definida:</span><span class="sxs-lookup"><span data-stu-id="96c80-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="96c80-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="96c80-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT LAUNCHWIZARDENTRY(
  HWND hParentWnd,
  ULONG ulFlags,
  LPCSTR FAR * lppszServiceNameToAdd,
  ULONG cbBufferMax,
  LPSTR lpszNewProfileName
);
```

## <a name="parameters"></a><span data-ttu-id="96c80-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96c80-112">Parameters</span></span>

 <span data-ttu-id="96c80-113">_hParentWnd_</span><span class="sxs-lookup"><span data-stu-id="96c80-113">_hParentWnd_</span></span>
  
> <span data-ttu-id="96c80-114">[entrada] Identificador de ventana primario del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="96c80-114">[in] A handle to the caller's parent window.</span></span> <span data-ttu-id="96c80-115">Si el autor de la llamada no tiene una ventana principal, el parámetro _hParentWnd_ debe ser nulo.</span><span class="sxs-lookup"><span data-stu-id="96c80-115">If the caller does not have a parent window, the  _hParentWnd_ parameter should be NULL.</span></span> 
    
 <span data-ttu-id="96c80-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="96c80-116">_ulFlags_</span></span>
  
> <span data-ttu-id="96c80-117">[entrada] Máscara de bits de marcadores que indica las opciones para el Asistente para perfiles.</span><span class="sxs-lookup"><span data-stu-id="96c80-117">[in] Bitmask of flags indicating options for the Profile Wizard.</span></span> <span data-ttu-id="96c80-118">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="96c80-118">The following flags can be set:</span></span>
    
<span data-ttu-id="96c80-119">MAPI_PW_ADD_SERVICE_ONLY</span><span class="sxs-lookup"><span data-stu-id="96c80-119">MAPI_PW_ADD_SERVICE_ONLY</span></span> 
  
> <span data-ttu-id="96c80-120">El Asistente para perfiles es agregar sólo los servicios de mensaje que aparecen a través del parámetro _lppszServiceNameToAdd_ y no mostrar su página de selección de servicios de mensaje.</span><span class="sxs-lookup"><span data-stu-id="96c80-120">The Profile Wizard is to add only the message services listed through the  _lppszServiceNameToAdd_ parameter, and not display its page for selecting message services.</span></span> 
    
<span data-ttu-id="96c80-121">MAPI_PW_FIRST_PROFILE</span><span class="sxs-lookup"><span data-stu-id="96c80-121">MAPI_PW_FIRST_PROFILE</span></span> 
  
> <span data-ttu-id="96c80-122">El perfil que se va a crear es el primero para esta estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="96c80-122">The profile to be created is the first one for this workstation.</span></span> 
    
<span data-ttu-id="96c80-123">MAPI_PW_HIDE_SERVICES_LIST</span><span class="sxs-lookup"><span data-stu-id="96c80-123">MAPI_PW_HIDE_SERVICES_LIST</span></span> 
  
> <span data-ttu-id="96c80-124">Página de perfil del Asistente para seleccionar servicios de mensajes no debe mostrarse.</span><span class="sxs-lookup"><span data-stu-id="96c80-124">The Profile Wizard's page for selecting message services should not be displayed.</span></span> 
    
<span data-ttu-id="96c80-125">MAPI_PW_LAUNCHED_BY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="96c80-125">MAPI_PW_LAUNCHED_BY_CONFIG</span></span> 
  
> <span data-ttu-id="96c80-126">El Asistente para perfiles se inició la aplicación de configuración del Panel de Control.</span><span class="sxs-lookup"><span data-stu-id="96c80-126">The Profile Wizard was launched by the Control Panel configuration application.</span></span> 
    
<span data-ttu-id="96c80-127">MAPI_PW_PROVIDER_UI_ONLY</span><span class="sxs-lookup"><span data-stu-id="96c80-127">MAPI_PW_PROVIDER_UI_ONLY</span></span> 
  
> <span data-ttu-id="96c80-128">Se deben mostrar cuadros de diálogo de configuración a sólo de los proveedores de servicios y las páginas del Asistente de perfiles no deben aparecer.</span><span class="sxs-lookup"><span data-stu-id="96c80-128">Only the service providers's configuration dialog boxes should be displayed and the Profile Wizard's pages should not appear.</span></span> <span data-ttu-id="96c80-129">Esta marca sólo se puede establecer si se establece la marca MAPI_PW_ADD_SERVICE_ONLY.</span><span class="sxs-lookup"><span data-stu-id="96c80-129">This flag can only be set if the MAPI_PW_ADD_SERVICE_ONLY flag is set.</span></span> 
    
 <span data-ttu-id="96c80-130">_lppszServiceNameToAdd_</span><span class="sxs-lookup"><span data-stu-id="96c80-130">_lppszServiceNameToAdd_</span></span>
  
> <span data-ttu-id="96c80-131">[entrada] Puntero a una matriz de cadenas que contiene los nombres de los servicios de mensaje que se agregará al perfil.</span><span class="sxs-lookup"><span data-stu-id="96c80-131">[in] Pointer to an array of strings that contains the names of the message services to be added to the profile.</span></span> <span data-ttu-id="96c80-132">La matriz debe terminar con un valor NULL.</span><span class="sxs-lookup"><span data-stu-id="96c80-132">The array must terminate with a NULL value.</span></span> 
    
 <span data-ttu-id="96c80-133">_cbBufferMax_</span><span class="sxs-lookup"><span data-stu-id="96c80-133">_cbBufferMax_</span></span>
  
> <span data-ttu-id="96c80-134">[entrada] Tamaño del búfer que señala el parámetro _lpszNewProfileName_ .</span><span class="sxs-lookup"><span data-stu-id="96c80-134">[in] Size of the buffer pointed to by the  _lpszNewProfileName_ parameter.</span></span> 
    
 <span data-ttu-id="96c80-135">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="96c80-135">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="96c80-136">[out] Puntero a un búfer de cadena donde la función basada en **LAUNCHWIZARDENTRY** devuelve el nombre del perfil creado.</span><span class="sxs-lookup"><span data-stu-id="96c80-136">[out] Pointer to a string buffer where the function based on **LAUNCHWIZARDENTRY** returns the name of the created profile.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="96c80-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96c80-137">Return value</span></span>

<span data-ttu-id="96c80-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="96c80-138">S_OK</span></span> 
  
> <span data-ttu-id="96c80-139">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="96c80-139">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="96c80-140">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="96c80-140">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="96c80-141">Un error de origen desconocido o inesperado no puede completar la operación.</span><span class="sxs-lookup"><span data-stu-id="96c80-141">An error of unexpected or unknown origin prevented the operation from completing.</span></span> <span data-ttu-id="96c80-142">Las posibilidades incluyen error al inicializar el subsistema MAPI para el Asistente para perfiles, incapacidad para tener acceso el perfil predeterminado y un error a devolver desde el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="96c80-142">Possibilities include failure to initialize the MAPI subsystem for the Profile Wizard, inability to access the default profile, and an error return from the dialog box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="96c80-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="96c80-143">Remarks</span></span>

<span data-ttu-id="96c80-144">La implementación de MAPI del prototipo de la función **LAUNCHWIZARDENTRY** es el punto de entrada a la aplicación del Asistente para el perfil MAPI.</span><span class="sxs-lookup"><span data-stu-id="96c80-144">The MAPI implementation of the **LAUNCHWIZARDENTRY** function prototype is the entry point into the MAPI Profile Wizard application.</span></span> <span data-ttu-id="96c80-145">En este punto de entrada **LaunchWizard**nombres de MAPI.</span><span class="sxs-lookup"><span data-stu-id="96c80-145">MAPI names this entry point **LaunchWizard**.</span></span> 
  
<span data-ttu-id="96c80-146">Cuando se establece la marca MAPI_PW_ADD_SERVICE_ONLY en el parámetro _ulFlags_ , se aplican las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="96c80-146">When the MAPI_PW_ADD_SERVICE_ONLY flag is set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="96c80-147">El indicador MAPI_PW_LAUNCHED_BY_CONFIG desactiva la página de bienvenida que no se muestren.</span><span class="sxs-lookup"><span data-stu-id="96c80-147">The MAPI_PW_LAUNCHED_BY_CONFIG flag inhibits the welcome page from being displayed.</span></span> 
    
- <span data-ttu-id="96c80-148">Los indicadores MAPI_PW_HIDE_SERVICES_LIST y MAPI_PW_PROVIDER_UI_ONLY son útiles sólo cuando no hay ningún perfil predeterminado.</span><span class="sxs-lookup"><span data-stu-id="96c80-148">The MAPI_PW_HIDE_SERVICES_LIST and MAPI_PW_PROVIDER_UI_ONLY flags are useful only when there is no default profile.</span></span> <span data-ttu-id="96c80-149">En este caso, estos marcadores determinan qué perfil de Asistente para la página que se mostrará.</span><span class="sxs-lookup"><span data-stu-id="96c80-149">In this case these flags determine which Profile Wizard page is to be displayed.</span></span> 
    
- <span data-ttu-id="96c80-150">Si existe un perfil de forma predeterminada, ninguna de las páginas del Asistente de perfiles son que se mostrará.</span><span class="sxs-lookup"><span data-stu-id="96c80-150">If a default profile exists, none of the Profile Wizard pages are to be displayed.</span></span> 
    
- <span data-ttu-id="96c80-151">Si existe un perfil predeterminado, servicio de un solo mensaje está en la lista a través del parámetro _lppszServiceNameToAdd_ , y el servicio de mensajes ya está en el perfil predeterminado, el Asistente para perfiles devuelve S_OK sin agregar nada para el perfil.</span><span class="sxs-lookup"><span data-stu-id="96c80-151">If a default profile exists, only one message service is listed through the  _lppszServiceNameToAdd_ parameter, and that message service is already in the default profile, the Profile Wizard returns S_OK without adding anything to the profile.</span></span> 
    
<span data-ttu-id="96c80-152">Para que cada servicio de mensajes que se agregará al perfil, el Asistente para perfiles de llamadas de función de punto de entrada del servicio basada en el prototipo [MSGSERVICEENTRY](msgserviceentry.md) .</span><span class="sxs-lookup"><span data-stu-id="96c80-152">For every message service to be added to the profile, the Profile Wizard calls the service's entry point function based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="96c80-153">Para cada proveedor de servicios seleccionado en un servicio de mensajes que se agregará al perfil, el Asistente para perfiles llama a función de punto de entrada del proveedor según el prototipo [WIZARDENTRY](wizardentry.md) .</span><span class="sxs-lookup"><span data-stu-id="96c80-153">For each service provider selected from a message service to be added to the profile, the Profile Wizard calls the provider's entry point function based on the [WIZARDENTRY](wizardentry.md) prototype.</span></span> <span data-ttu-id="96c80-154">Durante la configuración interactiva, cada evento de usuario en las páginas de propiedades hace que el Asistente para perfiles llamar a la función de devolución de llamada del proveedor según el prototipo [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) .</span><span class="sxs-lookup"><span data-stu-id="96c80-154">During interactive configuration, every user event in the property pages causes the Profile Wizard to call the provider's callback function based on the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
  
<span data-ttu-id="96c80-155">Si va a agregar al perfil de un proveedor de servicios es compatible con las páginas del Asistente de perfiles, debe permitir la configuración mediante programación del perfil.</span><span class="sxs-lookup"><span data-stu-id="96c80-155">If a service provider being added to the profile supports the Profile Wizard pages, it must allow programmatic configuration of the profile.</span></span>
  

