---
title: IMsgServiceAdminCreateMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CreateMsgService
api_type:
- COM
ms.assetid: 0135f049-0311-45e5-9685-78597d599a4e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6e0bdd7108bacd17134592ac05ba71510fde76d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817765"
---
# <a name="imsgserviceadmincreatemsgservice"></a><span data-ttu-id="ce0c1-103">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="ce0c1-103">IMsgServiceAdmin::CreateMsgService</span></span>

  
  
<span data-ttu-id="ce0c1-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ce0c1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ce0c1-105">Obsoleto: Se recomienda el uso de [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) .</span><span class="sxs-lookup"><span data-stu-id="ce0c1-105">Deprecated: The use of [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) is recommended.</span></span> <span data-ttu-id="ce0c1-106">Agrega un servicio de mensajes para el perfil actual.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-106">Adds a message service to the current profile.</span></span> 
  
```cpp
HRESULT CreateMsgService(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="ce0c1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce0c1-107">Parameters</span></span>

 <span data-ttu-id="ce0c1-108">_lpszService_</span><span class="sxs-lookup"><span data-stu-id="ce0c1-108">_lpszService_</span></span>
  
> <span data-ttu-id="ce0c1-109">[entrada] Un puntero al nombre del servicio de mensajes para agregar.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-109">[in] A pointer to the name of the message service to add.</span></span> <span data-ttu-id="ce0c1-110">Este nombre de servicio de mensajes debe aparecer en la sección **[Services]** del archivo MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-110">This message service name must appear in the **[Services]** section of the MapiSvc.inf file.</span></span> 
    
 <span data-ttu-id="ce0c1-111">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="ce0c1-111">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="ce0c1-112">[entrada] Un puntero para el nombre para mostrar del servicio de mensajes para agregar.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-112">[in] A pointer to the display name of the message service to add.</span></span> <span data-ttu-id="ce0c1-113">El parámetro _lpszDisplayName_ se omite si el servicio de mensajes ha establecido la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) en el archivo MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-113">The  _lpszDisplayName_ parameter is ignored if the message service has set the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MapiSvc.inf file.</span></span>
    
 <span data-ttu-id="ce0c1-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ce0c1-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="ce0c1-115">[entrada] Un identificador de la ventana principal de windows o cuadros de diálogo que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-115">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="ce0c1-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ce0c1-116">_ulFlags_</span></span>
  
> <span data-ttu-id="ce0c1-117">[entrada] Una máscara de bits de indicadores que controla cómo se instala el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-117">[in] A bitmask of flags that controls how the message service is installed.</span></span> <span data-ttu-id="ce0c1-118">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="ce0c1-118">The following flags can be set:</span></span>
    
<span data-ttu-id="ce0c1-119">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-119">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="ce0c1-120">El lpszService y los parámetros de lpszDisplayName deben convertirse a LPWSTR e interpreta como cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-120">The lpszService and the lpszDisplayName parameters should be cast to LPWSTR and interpreted as Unicode strings.</span></span>
    
<span data-ttu-id="ce0c1-121">SERVICE_NO_RESTART_WARNING</span><span class="sxs-lookup"><span data-stu-id="ce0c1-121">SERVICE_NO_RESTART_WARNING</span></span>
  
> <span data-ttu-id="ce0c1-122">Al agregar un nuevo servicio de mensajes para el perfil, el subsistema MAPI, en función de diversos criterios y circunstancias a menudo determina que esta acción requiere un reinicio de Outlook.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-122">When adding a new message service to the profile, the MAPI subsystem, based on various circumstances and criteria, often determines that this action requires a restart of Outlook.</span></span> <span data-ttu-id="ce0c1-123">Si no se incluye la marca SERVICE_NO_RESTART_WARNING y se permite la interfaz de usuario - según los indicadores SERVICE_UI_ALWAYS y SERVICE_UI_ALLOWED - y al menos un proceso ha iniciado sesión en el perfil actual, esta función muestra el mensaje "debe reiniciar Outlook para estos cambios surtan efecto."</span><span class="sxs-lookup"><span data-stu-id="ce0c1-123">If the SERVICE_NO_RESTART_WARNING flag is not included and UI is allowed - based on the SERVICE_UI_ALWAYS and SERVICE_UI_ALLOWED flags - and at least one process is logged onto the current profile, this function displays the message "You must restart Outlook for these changes to take effect."</span></span> <span data-ttu-id="ce0c1-124">Incluido el indicador de SERVICE_NO_RESTART_WARNING suprime la visualización de ese mensaje de advertencia.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-124">Including the SERVICE_NO_RESTART_WARNING flag suppresses the display of that warning message.</span></span>
    
<span data-ttu-id="ce0c1-125">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="ce0c1-125">SERVICE_UI_ALLOWED</span></span>
  
> <span data-ttu-id="ce0c1-126">La configuración del servicio de mensajes que se permite la interfaz de usuario si es necesario.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-126">The message service configuration UI is allowed if needed.</span></span>
    
<span data-ttu-id="ce0c1-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="ce0c1-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="ce0c1-128">El servicio de mensajes muestra su hoja de propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-128">The message service displays its configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ce0c1-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce0c1-129">Return value</span></span>

<span data-ttu-id="ce0c1-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="ce0c1-130">S_OK</span></span> 
  
> <span data-ttu-id="ce0c1-131">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-131">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="ce0c1-132">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ce0c1-132">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ce0c1-133">El nombre del servicio de mensajes no está en la sección **[Services]** de MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-133">The message service name is not in the **[Services]** section of MapiSvc.inf.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ce0c1-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ce0c1-134">Remarks</span></span>

<span data-ttu-id="ce0c1-135">El método **IMsgServiceAdmin::** agrega un servicio de mensajes para el perfil actual.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-135">The **IMsgServiceAdmin::CreateMsgService** method adds a message service to the current profile.</span></span> <span data-ttu-id="ce0c1-136">**CreateMsgService** llama a la función de punto de entrada del servicio de mensajes para realizar las tareas de configuración específica de cada servicio.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-136">**CreateMsgService** calls the message service's entry point function to perform any service-specific configuration tasks.</span></span> <span data-ttu-id="ce0c1-137">Si se establece la marca SERVICE_UI_ALLOWED en el parámetro _ulFlags_ , el servicio de mensajes que se va a instalar puede mostrar una hoja de propiedades para permitir que el usuario realizar la configuración.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-137">If the SERVICE_UI_ALLOWED flag is set in the  _ulFlags_ parameter, the message service being installed can display a property sheet to enable the user to configure its settings.</span></span> 
  
<span data-ttu-id="ce0c1-138">El archivo MapiSvc.inf contiene la lista de proveedores que componen un servicio de mensajes y las propiedades para cada uno.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-138">The MapiSvc.inf file contains the list of providers that make up a message service and the properties for each.</span></span> <span data-ttu-id="ce0c1-139">**CreateMsgService** primero se crea una nueva sección de perfil para el servicio de mensajes y, a continuación, copia toda la información de ese servicio desde el archivo MapiSvc.inf en el perfil, crear nuevas secciones para cada proveedor.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-139">**CreateMsgService** first creates a new profile section for the message service and then copies all of the information for that service from the MapiSvc.inf file into the profile, creating new sections for each provider.</span></span> 
  
<span data-ttu-id="ce0c1-140">Después de que toda la información se ha copiado desde MapiSvc.inf, se denomina función de punto de entrada del servicio de mensajes con el valor MSG_SERVICE_CREATE establecido en el parámetro _ulContext_ .</span><span class="sxs-lookup"><span data-stu-id="ce0c1-140">After all the information has been copied from MapiSvc.inf, the message service's entry point function is called with the MSG_SERVICE_CREATE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="ce0c1-141">Si se establece la marca SERVICE_UI_ALLOWED en el **CreateMsgService** parámetro del método _ulFlags_ , también se pasan los valores de los parámetros _ulUIParam_ y _ulFlags_ cuando se llama a la función de punto de entrada del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-141">If the SERVICE_UI_ALLOWED flag is set in the **CreateMsgService** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed when the message service's entry point function is called.</span></span> <span data-ttu-id="ce0c1-142">Proveedores de servicios deben mostrar sus hojas de propiedades de configuración, por lo que los usuarios pueden configurar el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-142">Service providers should display their configuration property sheets so users can configure the message service.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ce0c1-143">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="ce0c1-143">Notes to callers</span></span>

 <span data-ttu-id="ce0c1-144">**CreateMsgService** no devuelve la estructura [MAPIUID](mapiuid.md) para el servicio de mensajes que se ha agregado al perfil.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-144">**CreateMsgService** does not return the [MAPIUID](mapiuid.md) structure for the message service that was added to the profile.</span></span> 
  
<span data-ttu-id="ce0c1-145">Para recuperar la **MAPIUID** para el servicio de mensaje de creación, utilice el procedimiento siguiente:</span><span class="sxs-lookup"><span data-stu-id="ce0c1-145">To retrieve the **MAPIUID** for the created message service, use the following procedure:</span></span> 
  
1. <span data-ttu-id="ce0c1-146">Llame al método [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para obtener la tabla de administración del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-146">Call the [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) method to get the message service administration table.</span></span> 
    
2. <span data-ttu-id="ce0c1-147">Busque la fila que representa el servicio de mensajes mediante la colocación de una restricción en la tabla que coincida con la propiedad **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) con el nombre del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-147">Locate the row that represents the message service by placing a restriction on the table that matches the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property with the name of the message service.</span></span> 
    
3. <span data-ttu-id="ce0c1-148">Recupere la propiedad del servicio **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ce0c1-148">Retrieve the service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span> 
    
4. <span data-ttu-id="ce0c1-149">Pasar el valor de la propiedad **PR_SERVICE_UID** en el parámetro _lpUid_ al método [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) para configurar el servicio.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-149">Pass the value of the **PR_SERVICE_UID** property in the  _lpUid_ parameter to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method to configure the service.</span></span> 
    
> [!CAUTION]
> <span data-ttu-id="ce0c1-150">La implementación de Microsoft Outlook 2010 del subsistema MAPI no admite MAPI_UNICODE y se producirá un error si se usa.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-150">The Microsoft Outlook 2010 implementation of the MAPI subsystem does not support MAPI_UNICODE and will fail if it is used.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="ce0c1-151">_UlFlags_ SERVICE_NO_RESTART_WARNING no pueden definirse en el archivo de encabezado que se pueden descargar tiene actualmente, en cuyo caso se puede agregar a su código con el siguiente valor: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`</span><span class="sxs-lookup"><span data-stu-id="ce0c1-151">The  _ulFlags_ SERVICE_NO_RESTART_WARNING might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ce0c1-152">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ce0c1-152">MFCMAPI reference</span></span>

<span data-ttu-id="ce0c1-153">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ce0c1-154">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="ce0c1-154">**File**</span></span>|<span data-ttu-id="ce0c1-155">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="ce0c1-155">**Function**</span></span>|<span data-ttu-id="ce0c1-156">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="ce0c1-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ce0c1-157">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="ce0c1-157">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ce0c1-158">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="ce0c1-158">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="ce0c1-159">MFCMAPI usa el método **IMsgServiceAdmin::** para agregar un servicio a un perfil.</span><span class="sxs-lookup"><span data-stu-id="ce0c1-159">MFCMAPI uses the **IMsgServiceAdmin::CreateMsgService** method to add a service to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce0c1-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce0c1-160">See also</span></span>



[<span data-ttu-id="ce0c1-161">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ce0c1-161">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="ce0c1-162">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="ce0c1-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

