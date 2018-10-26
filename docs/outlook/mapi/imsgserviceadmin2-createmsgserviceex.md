---
title: IMsgServiceAdmin2CreateMsgServiceEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin2.CreateMsgServiceEx
api_type:
- COM
ms.assetid: 4910dabd-9380-4fde-a440-5c64d74c0bba
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f700389315ca7bd184a9d6defb0b44eaec99a38e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574779"
---
# <a name="imsgserviceadmin2createmsgserviceex"></a><span data-ttu-id="3a5d9-103">IMsgServiceAdmin2::CreateMsgServiceEx</span><span class="sxs-lookup"><span data-stu-id="3a5d9-103">IMsgServiceAdmin2::CreateMsgServiceEx</span></span>

  
  
<span data-ttu-id="3a5d9-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a5d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a5d9-105">Agrega un servicio de mensajes para el perfil actual y devuelve que acaba de agregar UID de servicio.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-105">Adds a message service to the current profile and returns that newly added service UID.</span></span>
  
```cpp
HRESULT CreateMsgServiceEx(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,    
  LPMAPIUID lpuidService
);
```

## <a name="parameters"></a><span data-ttu-id="3a5d9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3a5d9-106">Parameters</span></span>

 <span data-ttu-id="3a5d9-107">_lpszService_</span><span class="sxs-lookup"><span data-stu-id="3a5d9-107">_lpszService_</span></span>
  
> <span data-ttu-id="3a5d9-108">[entrada] Un puntero al nombre del servicio de mensajes para agregar.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-108">[in] A pointer to the name of the message service to add.</span></span> <span data-ttu-id="3a5d9-109">Este nombre de servicio de mensajes debe aparecer en la sección **[Services]** del archivo MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-109">This message service name must appear in the **[Services]** section of the MapiSvc.inf file.</span></span> 
    
 <span data-ttu-id="3a5d9-110">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="3a5d9-110">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="3a5d9-111">[entrada] Un puntero para el nombre para mostrar del servicio de mensajes para agregar.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-111">[in] A pointer to the display name of the message service to add.</span></span> <span data-ttu-id="3a5d9-112">El parámetro _lpszDisplayName_ se omite si el servicio de mensajes ha establecido la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) en el archivo MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-112">The  _lpszDisplayName_ parameter is ignored if the message service has set the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MapiSvc.inf file.</span></span>
    
 <span data-ttu-id="3a5d9-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="3a5d9-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="3a5d9-114">[entrada] Un identificador de la ventana principal de windows o cuadros de diálogo que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="3a5d9-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3a5d9-115">_ulFlags_</span></span>
  
> <span data-ttu-id="3a5d9-116">[entrada] Una máscara de bits de indicadores que controla cómo se instala el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-116">[in] A bitmask of flags that controls how the message service is installed.</span></span> <span data-ttu-id="3a5d9-117">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="3a5d9-117">The following flags can be set:</span></span>
    
<span data-ttu-id="3a5d9-118">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3a5d9-118">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="3a5d9-119">El lpszService y los parámetros de lpszDisplayName deben convertirse a LPWSTR e interpreta como cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-119">The lpszService and the lpszDisplayName parameters should be cast to LPWSTR and interpreted as Unicode strings.</span></span>
    
<span data-ttu-id="3a5d9-120">SERVICE_NO_RESTART_WARNING</span><span class="sxs-lookup"><span data-stu-id="3a5d9-120">SERVICE_NO_RESTART_WARNING</span></span>
  
> <span data-ttu-id="3a5d9-121">Al agregar un nuevo servicio de mensajes para el perfil, el subsistema MAPI, en función de diversos criterios y circunstancias a menudo determina que esta acción requiere un reinicio de Outlook.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-121">When adding a new message service to the profile, the MAPI subsystem, based on various circumstances and criteria, often determines that this action requires a restart of Outlook.</span></span> <span data-ttu-id="3a5d9-122">Si no se incluye la marca SERVICE_NO_RESTART_WARNING y se permite la interfaz de usuario - según los indicadores SERVICE_UI_ALWAYS y SERVICE_UI_ALLOWED - y al menos un proceso ha iniciado sesión en el perfil actual, esta función muestra el mensaje "debe reiniciar Outlook para estos cambios surtan efecto."</span><span class="sxs-lookup"><span data-stu-id="3a5d9-122">If the SERVICE_NO_RESTART_WARNING flag is not included and UI is allowed - based on the SERVICE_UI_ALWAYS and SERVICE_UI_ALLOWED flags - and at least one process is logged onto the current profile, this function displays the message "You must restart Outlook for these changes to take effect."</span></span> <span data-ttu-id="3a5d9-123">Incluido el indicador de SERVICE_NO_RESTART_WARNING suprime la visualización de ese mensaje de advertencia.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-123">Including the SERVICE_NO_RESTART_WARNING flag suppresses the display of that warning message.</span></span>
    
<span data-ttu-id="3a5d9-124">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="3a5d9-124">SERVICE_UI_ALLOWED</span></span>
  
> <span data-ttu-id="3a5d9-125">La configuración del servicio de mensajes que se permite la interfaz de usuario si es necesario.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-125">The message service configuration UI is allowed if needed.</span></span>
    
<span data-ttu-id="3a5d9-126">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="3a5d9-126">SERVICE_UI_ALWAYS</span></span>
  
> <span data-ttu-id="3a5d9-127">El servicio de mensajes muestra su hoja de propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-127">The message service displays its configuration property sheet.</span></span>
    
 <span data-ttu-id="3a5d9-128">_lpuidService_</span><span class="sxs-lookup"><span data-stu-id="3a5d9-128">_lpuidService_</span></span>
  
> <span data-ttu-id="3a5d9-129">[out] El puntero para el UID del servicio de mensajes agregado.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-129">[out] The pointer to the UID of the message service added.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3a5d9-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3a5d9-130">Return value</span></span>

<span data-ttu-id="3a5d9-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="3a5d9-131">S_OK</span></span>
  
> <span data-ttu-id="3a5d9-132">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-132">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="3a5d9-133">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="3a5d9-133">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="3a5d9-134">El nombre del servicio de mensajes no está en la sección **[Services]** de MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-134">The message service name is not in the **[Services]** section of MapiSvc.inf.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3a5d9-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3a5d9-135">Remarks</span></span>

<span data-ttu-id="3a5d9-136">El método **IMsgServiceAdmin2::CreateMsgServiceEx** agrega un servicio de mensajes para el perfil actual.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-136">The **IMsgServiceAdmin2::CreateMsgServiceEx** method adds a message service to the current profile.</span></span> <span data-ttu-id="3a5d9-137">**CreateMsgServiceEx** llama a la función de punto de entrada del servicio de mensajes para realizar las tareas de configuración específica de cada servicio.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-137">**CreateMsgServiceEx** calls the message service's entry point function to perform any service-specific configuration tasks.</span></span> <span data-ttu-id="3a5d9-138">Si se establece la marca SERVICE_UI_ALLOWED en el parámetro _ulFlags_ , el servicio de mensajes que se va a instalar puede mostrar una hoja de propiedades que permite al usuario configurar su configuración.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-138">If the SERVICE_UI_ALLOWED flag is set in the  _ulFlags_ parameter, the message service being installed can display a property sheet enabling the user to configure its settings.</span></span> 
  
<span data-ttu-id="3a5d9-139">El archivo MapiSvc.inf contiene la lista de proveedores que componen un servicio de mensajes y las propiedades para cada uno.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-139">The MapiSvc.inf file contains the list of providers that make up a message service and the properties for each.</span></span> <span data-ttu-id="3a5d9-140">**CreateMsgServiceEx** primero se crea una nueva sección de perfil para el servicio de mensajes y, a continuación, copia toda la información de ese servicio desde el archivo MapiSvc.inf en el perfil, crear nuevas secciones para cada proveedor.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-140">**CreateMsgServiceEx** first creates a new profile section for the message service and then copies all of the information for that service from the MapiSvc.inf file into the profile, creating new sections for each provider.</span></span> 
  
<span data-ttu-id="3a5d9-141">Después de que toda la información se ha copiado desde MapiSvc.inf, se denomina función de punto de entrada del servicio de mensajes, **MSGSERVICEENTRY**, con el valor MSG_SERVICE_CREATE establecido en el parámetro _ulContext_ .</span><span class="sxs-lookup"><span data-stu-id="3a5d9-141">After all the information has been copied from MapiSvc.inf, the message service's entry point function, **MSGSERVICEENTRY**, is called with the MSG_SERVICE_CREATE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="3a5d9-142">Si se establece la marca SERVICE_UI_ALLOWED en el **CreateMsgServiceEx** parámetro del método _ulFlags_ , también se pasan los valores de los parámetros _ulUIParam_ y _ulFlags_ cuando se llama a la función de punto de entrada del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-142">If the SERVICE_UI_ALLOWED flag is set in the **CreateMsgServiceEx** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed when the message service's entry point function is called.</span></span> <span data-ttu-id="3a5d9-143">Proveedores de servicios deben mostrar sus hojas de propiedades de configuración, por lo que los usuarios pueden configurar el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-143">Service providers should display their configuration property sheets so users can configure the message service.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3a5d9-144">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="3a5d9-144">Notes to callers</span></span>

<span data-ttu-id="3a5d9-145">Si el argumento de _lpuidService_ **CreateMsgServiceEx** no es nulo, se devuelve la propiedad **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) de la que se ha agregado al perfil de servicio de mensajes en el **GUID** al que señala.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-145">If the **CreateMsgServiceEx** _lpuidService_ argument is not NULL, the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property of the message service that was added to the profile is returned in the **GUID** to which it points.</span></span> 
  
<span data-ttu-id="3a5d9-146">Pasar el valor de la propiedad **PR_SERVICE_UID** en el parámetro _lpuidService_ al método [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) para configurar el servicio.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-146">Pass the value of the **PR_SERVICE_UID** property in the  _lpuidService_ parameter to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method to configure the service.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="3a5d9-147">La implementación de Microsoft Outlook 2010 del subsistema MAPI no admite MAPI_UNICODE y se producirá un error si se usa.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-147">The Microsoft Outlook 2010 implementation of the MAPI subsystem does not support MAPI_UNICODE and will fail if it is used.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="3a5d9-148">La interfaz de IMsgServiceAdmin2 es expuesta por el mismo objeto que implementa la interfaz IMsgServiceAdmin y ha estado disponible mediante la implementación de Outlook del subsistema MAPI desde Outlook 2003.</span><span class="sxs-lookup"><span data-stu-id="3a5d9-148">The IMsgServiceAdmin2 interface is exposed by the same object that implements the IMsgServiceAdmin interface, and has been available using Outlook's implementation of the MAPI subsystem since Outlook 2003.</span></span> <span data-ttu-id="3a5d9-149">Su IID se define como sigue: > `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> _ulFlags_ SERVICE_NO_RESTART_WARNING no pueden definirse en el archivo de encabezado que se pueden descargar tiene actualmente, en cuyo caso se puede agregar a su código con el siguiente valor: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`</span><span class="sxs-lookup"><span data-stu-id="3a5d9-149">Its IID is defined as follows: >  `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)`>  `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> The  _ulFlags_ SERVICE_NO_RESTART_WARNING might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3a5d9-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a5d9-150">See also</span></span>



[<span data-ttu-id="3a5d9-151">IMsgServiceAdmin2 : IMsgServiceAdmin</span><span class="sxs-lookup"><span data-stu-id="3a5d9-151">IMsgServiceAdmin2 : IMsgServiceAdmin</span></span>](imsgserviceadmin2imsgserviceadmin.md)


[<span data-ttu-id="3a5d9-152">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="3a5d9-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

