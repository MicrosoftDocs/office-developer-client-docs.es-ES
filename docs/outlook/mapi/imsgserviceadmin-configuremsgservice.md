---
title: IMsgServiceAdminConfigureMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.ConfigureMsgService
api_type:
- COM
ms.assetid: a08f5905-2585-49ca-abb7-a77f2736f604
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a599a6fe5093e52e50d33a1761df5689b7335138
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568297"
---
# <a name="imsgserviceadminconfiguremsgservice"></a><span data-ttu-id="87d04-103">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="87d04-103">IMsgServiceAdmin::ConfigureMsgService</span></span>

  
  
<span data-ttu-id="87d04-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87d04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87d04-105">Vuelve a configurar un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="87d04-105">Reconfigures a message service.</span></span>
  
```cpp
HRESULT ConfigureMsgService(
  LPMAPIUID lpUID,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="87d04-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="87d04-106">Parameters</span></span>

 <span data-ttu-id="87d04-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="87d04-107">_lpUID_</span></span>
  
> <span data-ttu-id="87d04-108">[entrada] Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único para el servicio de mensajes configurar.</span><span class="sxs-lookup"><span data-stu-id="87d04-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to configure.</span></span> 
    
 <span data-ttu-id="87d04-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="87d04-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="87d04-110">[entrada] Identificador de la ventana principal de la hoja de propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="87d04-110">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="87d04-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="87d04-111">_ulFlags_</span></span>
  
> <span data-ttu-id="87d04-112">[entrada] Una máscara de bits de indicadores que controla la presentación de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="87d04-112">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="87d04-113">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="87d04-113">The following flags can be set:</span></span>
    
<span data-ttu-id="87d04-114">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="87d04-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="87d04-115">Las cadenas que se pasan en están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="87d04-115">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="87d04-116">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="87d04-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="87d04-117">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="87d04-117">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="87d04-118">El servicio de mensajes debe mostrar su hoja de propiedades de configuración, pero no permitir que el usuario que la cambie.</span><span class="sxs-lookup"><span data-stu-id="87d04-118">The message service should display its configuration property sheet but not enable the user to change it.</span></span> <span data-ttu-id="87d04-119">La mayoría de los servicios de mensaje pase por alto esta marca.</span><span class="sxs-lookup"><span data-stu-id="87d04-119">Most message services ignore this flag.</span></span>
    
<span data-ttu-id="87d04-120">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="87d04-120">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="87d04-121">El servicio de mensajes debe mostrar su hoja de propiedades de configuración sólo si el servicio no está configurado completamente.</span><span class="sxs-lookup"><span data-stu-id="87d04-121">The message service should display its configuration property sheet only if the service is not completely configured.</span></span>
    
<span data-ttu-id="87d04-122">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="87d04-122">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="87d04-123">El servicio de mensajes siempre debe mostrar su hoja de propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="87d04-123">The message service must always display its configuration property sheet.</span></span> <span data-ttu-id="87d04-124">Si no se establece SERVICE_UI_ALWAYS, una hoja de propiedades de configuración aún puede mostrarse si se establece SERVICE_UI_ALLOWED y no está disponible desde la matriz de valores de propiedad en el parámetro _lpProps_ información de configuración válido.</span><span class="sxs-lookup"><span data-stu-id="87d04-124">If SERVICE_UI_ALWAYS is not set, a configuration property sheet can still be displayed if SERVICE_UI_ALLOWED is set and valid configuration information is not available from the property value array in the  _lpProps_ parameter.</span></span> <span data-ttu-id="87d04-125">SERVICE_UI_ALLOWED o SERVICE_UI_ALWAYS se debe establecer para que una hoja de propiedades que se mostrará.</span><span class="sxs-lookup"><span data-stu-id="87d04-125">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set for a property sheet to be displayed.</span></span> 
    
 <span data-ttu-id="87d04-126">_cValues_</span><span class="sxs-lookup"><span data-stu-id="87d04-126">_cValues_</span></span>
  
> <span data-ttu-id="87d04-127">[entrada] El recuento de valores de propiedad en la estructura [SPropValue](spropvalue.md) apunta a _lpProps_.</span><span class="sxs-lookup"><span data-stu-id="87d04-127">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by  _lpProps_.</span></span> 
    
 <span data-ttu-id="87d04-128">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="87d04-128">_lpProps_</span></span>
  
> <span data-ttu-id="87d04-129">[entrada] Un puntero a una matriz de valores de propiedad que se describen las propiedades que se muestra en la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="87d04-129">[in] A pointer to an array of property values that describe the properties to display in the property sheet.</span></span> <span data-ttu-id="87d04-130">El parámetro _lpProps_ no debe ser NULL si el servicio de mensajes debe configurarse sin necesidad de una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="87d04-130">The  _lpProps_ parameter should not be NULL if the message service should be configured without a user interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="87d04-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87d04-131">Return value</span></span>

<span data-ttu-id="87d04-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="87d04-132">S_OK</span></span> 
  
> <span data-ttu-id="87d04-133">El servicio de mensajes se ha configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="87d04-133">The message service was successfully configured.</span></span>
    
<span data-ttu-id="87d04-134">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="87d04-134">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="87d04-135">Un error específico a un servicio de mensaje.</span><span class="sxs-lookup"><span data-stu-id="87d04-135">An error specific to a message service.</span></span> <span data-ttu-id="87d04-136">Para obtener la estructura [MAPIERROR](mapierror.md) que describe el error, la aplicación cliente debe llamar al método de [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="87d04-136">To get the [MAPIERROR](mapierror.md) structure that describes the error, the client application should call the [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="87d04-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="87d04-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="87d04-138">El **MAPIUID** que señala _lpUID_ no coincide con el de un servicio de mensaje existente.</span><span class="sxs-lookup"><span data-stu-id="87d04-138">The **MAPIUID** pointed to by  _lpUID_ does not match that of an existing message service.</span></span> 
    
<span data-ttu-id="87d04-139">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="87d04-139">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="87d04-140">El servicio de mensajes no tiene una entrada de función de punto.</span><span class="sxs-lookup"><span data-stu-id="87d04-140">The message service does not have an entry point function.</span></span>
    
<span data-ttu-id="87d04-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="87d04-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="87d04-142">El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="87d04-142">The user canceled the operation, typically by clicking the **Cancel** button in the property sheet.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="87d04-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="87d04-143">Remarks</span></span>

<span data-ttu-id="87d04-144">El método **IMsgServiceAdmin::ConfigureMsgService** permite un servicio de mensajes que desea configurar, con o sin una hoja de propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="87d04-144">The **IMsgServiceAdmin::ConfigureMsgService** method enables a message service to be configured, with or without a configuration property sheet.</span></span> 
  
<span data-ttu-id="87d04-145">Para permitir la configuración sin una presentación de hoja de propiedades, servicios de mensajes normalmente preparan un archivo de encabezado que incluya las constantes de todas las propiedades opcionales y obligatorios y sus valores.</span><span class="sxs-lookup"><span data-stu-id="87d04-145">To allow configuration without a property sheet display, message services typically prepare a header file that includes constants for all the required and optional properties and their values.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="87d04-146">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="87d04-146">Notes to callers</span></span>

<span data-ttu-id="87d04-147">Para recuperar la estructura **MAPIUID** para el servicio de mensajes configurar, recuperar la columna **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) de la fila del servicio de mensajes en la tabla de servicios de mensaje.</span><span class="sxs-lookup"><span data-stu-id="87d04-147">To retrieve the **MAPIUID** structure for the message service to configure, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column from the message service's row in the message service table.</span></span> <span data-ttu-id="87d04-148">Para obtener más información, vea el procedimiento descrito en el método [IMsgServiceAdmin::](imsgserviceadmin-createmsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="87d04-148">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
<span data-ttu-id="87d04-149">Puede configurar un servicio de mensajes sin mostrar una hoja de propiedades a un usuario sólo si tienen información avanzada acerca de los valores de propiedad va a establecer.</span><span class="sxs-lookup"><span data-stu-id="87d04-149">You can configure a message service without displaying a property sheet to a user only if you have advance information about the property values to be set.</span></span> <span data-ttu-id="87d04-150">Si va a configurar un servicio de mensajes sin mostrar una hoja de propiedades, pase los valores de propiedad válido en el parámetro _lpProps_ y no se establece los indicadores MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED o SERVICE_UI_ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="87d04-150">If you are configuring a message service without displaying a property sheet, pass valid property values in the  _lpProps_ parameter and do not set the MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED, or SERVICE_UI_ALWAYS flags.</span></span> 
  
<span data-ttu-id="87d04-151">Si recibe todo o parte de la información de configuración del usuario por medio de una hoja de propiedades, establezca SERVICE_UI_ALLOWED en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="87d04-151">If you receive all or some of the configuration information from the user by way of a property sheet, set SERVICE_UI_ALLOWED in  _ulFlags_.</span></span> <span data-ttu-id="87d04-152">Si utiliza información de la propiedad existente sólo para establecer la configuración predeterminada y el usuario tiene permiso Cambiar la configuración, establezca SERVICE_UI_ALWAYS en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="87d04-152">If you use existing property information only to establish default settings and the user is able to change the settings, set SERVICE_UI_ALWAYS in  _ulFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="87d04-153">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="87d04-153">MFCMAPI reference</span></span>

<span data-ttu-id="87d04-154">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="87d04-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="87d04-155">**File**</span><span class="sxs-lookup"><span data-stu-id="87d04-155">**File**</span></span>|<span data-ttu-id="87d04-156">**Función**</span><span class="sxs-lookup"><span data-stu-id="87d04-156">**Function**</span></span>|<span data-ttu-id="87d04-157">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="87d04-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="87d04-158">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="87d04-158">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="87d04-159">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="87d04-159">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="87d04-160">MFCMAPI usa el método **IMsgServiceAdmin::ConfigureMsgService** para configurar un servicio que se ha agregado a un perfil.</span><span class="sxs-lookup"><span data-stu-id="87d04-160">MFCMAPI uses the **IMsgServiceAdmin::ConfigureMsgService** method to configure a service that has been added to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="87d04-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="87d04-161">See also</span></span>



[<span data-ttu-id="87d04-162">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="87d04-162">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="87d04-163">SPropValue</span><span class="sxs-lookup"><span data-stu-id="87d04-163">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="87d04-164">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="87d04-164">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="87d04-165">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="87d04-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

