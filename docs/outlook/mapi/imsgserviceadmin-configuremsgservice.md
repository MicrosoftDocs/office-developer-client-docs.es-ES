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
ms.openlocfilehash: 87ac394f9ab77b092cdfcd44f65b040a039319e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317412"
---
# <a name="imsgserviceadminconfiguremsgservice"></a><span data-ttu-id="5e600-103">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="5e600-103">IMsgServiceAdmin::ConfigureMsgService</span></span>

  
  
<span data-ttu-id="5e600-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e600-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e600-105">Reconfigura un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="5e600-105">Reconfigures a message service.</span></span>
  
```cpp
HRESULT ConfigureMsgService(
  LPMAPIUID lpUID,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="5e600-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="5e600-106">Parameters</span></span>

 <span data-ttu-id="5e600-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="5e600-107">_lpUID_</span></span>
  
> <span data-ttu-id="5e600-108">a Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador único para el servicio de mensaje que se va a configurar.</span><span class="sxs-lookup"><span data-stu-id="5e600-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to configure.</span></span> 
    
 <span data-ttu-id="5e600-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="5e600-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="5e600-110">a Identificador de la ventana primaria de la hoja de propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="5e600-110">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="5e600-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5e600-111">_ulFlags_</span></span>
  
> <span data-ttu-id="5e600-112">a Máscara de máscara de marcadores que controla la presentación de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="5e600-112">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="5e600-113">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="5e600-113">The following flags can be set:</span></span>
    
<span data-ttu-id="5e600-114">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5e600-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5e600-115">Las cadenas pasadas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="5e600-115">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="5e600-116">Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="5e600-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="5e600-117">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="5e600-117">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="5e600-118">El servicio de mensajes debe mostrar su hoja de propiedades de configuración, pero no permitir que el usuario lo cambie.</span><span class="sxs-lookup"><span data-stu-id="5e600-118">The message service should display its configuration property sheet but not enable the user to change it.</span></span> <span data-ttu-id="5e600-119">La mayoría de los servicios de mensajes ignoran esta marca.</span><span class="sxs-lookup"><span data-stu-id="5e600-119">Most message services ignore this flag.</span></span>
    
<span data-ttu-id="5e600-120">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="5e600-120">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="5e600-121">El servicio de mensajes debería mostrar su hoja de propiedades de configuración solo si el servicio no está configurado completamente.</span><span class="sxs-lookup"><span data-stu-id="5e600-121">The message service should display its configuration property sheet only if the service is not completely configured.</span></span>
    
<span data-ttu-id="5e600-122">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="5e600-122">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="5e600-123">El servicio de mensajes siempre debe mostrar su hoja de propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="5e600-123">The message service must always display its configuration property sheet.</span></span> <span data-ttu-id="5e600-124">Si no se establece SERVICE_UI_ALWAYS, se podrá seguir mostrando una hoja de propiedades de configuración si se establece SERVICE_UI_ALLOWED y la información de configuración válida no está disponible en la matriz de valores de propiedad en el parámetro _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="5e600-124">If SERVICE_UI_ALWAYS is not set, a configuration property sheet can still be displayed if SERVICE_UI_ALLOWED is set and valid configuration information is not available from the property value array in the  _lpProps_ parameter.</span></span> <span data-ttu-id="5e600-125">Se debe establecer SERVICE_UI_ALLOWED o SERVICE_UI_ALWAYS para que se muestre una hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="5e600-125">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set for a property sheet to be displayed.</span></span> 
    
 <span data-ttu-id="5e600-126">_cValues_</span><span class="sxs-lookup"><span data-stu-id="5e600-126">_cValues_</span></span>
  
> <span data-ttu-id="5e600-127">a El número de valores de propiedad en la estructura [SPropValue](spropvalue.md) apuntado por _lpProps_.</span><span class="sxs-lookup"><span data-stu-id="5e600-127">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by  _lpProps_.</span></span> 
    
 <span data-ttu-id="5e600-128">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="5e600-128">_lpProps_</span></span>
  
> <span data-ttu-id="5e600-129">a Un puntero a una matriz de valores de propiedad que describen las propiedades que se van a mostrar en la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="5e600-129">[in] A pointer to an array of property values that describe the properties to display in the property sheet.</span></span> <span data-ttu-id="5e600-130">El parámetro _lpProps_ no debe ser null si el servicio de mensajes debe configurarse sin una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5e600-130">The  _lpProps_ parameter should not be NULL if the message service should be configured without a user interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5e600-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e600-131">Return value</span></span>

<span data-ttu-id="5e600-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="5e600-132">S_OK</span></span> 
  
> <span data-ttu-id="5e600-133">El servicio de mensajes se configuró correctamente.</span><span class="sxs-lookup"><span data-stu-id="5e600-133">The message service was successfully configured.</span></span>
    
<span data-ttu-id="5e600-134">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="5e600-134">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="5e600-135">Un error específico de un servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="5e600-135">An error specific to a message service.</span></span> <span data-ttu-id="5e600-136">Para obtener la estructura [MAPIERROR](mapierror.md) que describe el error, la aplicación cliente debe llamar al método [IMsgServiceAdmin:: GetLastError](imsgserviceadmin-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="5e600-136">To get the [MAPIERROR](mapierror.md) structure that describes the error, the client application should call the [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="5e600-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="5e600-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="5e600-138">La **MAPIUID** a la que apunta _lpUID_ no coincide con la de un servicio de mensajes existente.</span><span class="sxs-lookup"><span data-stu-id="5e600-138">The **MAPIUID** pointed to by  _lpUID_ does not match that of an existing message service.</span></span> 
    
<span data-ttu-id="5e600-139">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="5e600-139">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="5e600-140">El servicio de mensajes no tiene una función de punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="5e600-140">The message service does not have an entry point function.</span></span>
    
<span data-ttu-id="5e600-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="5e600-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="5e600-142">El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="5e600-142">The user canceled the operation, typically by clicking the **Cancel** button in the property sheet.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5e600-143">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5e600-143">Remarks</span></span>

<span data-ttu-id="5e600-144">El método **IMsgServiceAdmin:: ConfigureMsgService** permite configurar un servicio de mensajes, con o sin una hoja de propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="5e600-144">The **IMsgServiceAdmin::ConfigureMsgService** method enables a message service to be configured, with or without a configuration property sheet.</span></span> 
  
<span data-ttu-id="5e600-145">Para permitir la configuración sin mostrar hojas de propiedades, los servicios de mensajes suelen preparar un archivo de encabezado que incluye constantes para todas las propiedades obligatorias y opcionales y sus valores.</span><span class="sxs-lookup"><span data-stu-id="5e600-145">To allow configuration without a property sheet display, message services typically prepare a header file that includes constants for all the required and optional properties and their values.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="5e600-146">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="5e600-146">Notes to callers</span></span>

<span data-ttu-id="5e600-147">Para recuperar la estructura **MAPIUID** del servicio de mensajes que se va a configurar, recupere la columna **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) de la fila del servicio de mensajes en la tabla de servicios de mensajes.</span><span class="sxs-lookup"><span data-stu-id="5e600-147">To retrieve the **MAPIUID** structure for the message service to configure, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column from the message service's row in the message service table.</span></span> <span data-ttu-id="5e600-148">Para obtener más información, vea el procedimiento descrito en el método [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="5e600-148">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
<span data-ttu-id="5e600-149">Puede configurar un servicio de mensajes sin mostrar una hoja de propiedades a un usuario sólo si tiene información avanzada sobre los valores de propiedad que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="5e600-149">You can configure a message service without displaying a property sheet to a user only if you have advance information about the property values to be set.</span></span> <span data-ttu-id="5e600-150">Si está configurando un servicio de mensajes sin mostrar una hoja de propiedades, pase los valores de propiedad válidos en el parámetro _lpProps_ y no establezca los marcadores MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED o SERVICE_UI_ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="5e600-150">If you are configuring a message service without displaying a property sheet, pass valid property values in the  _lpProps_ parameter and do not set the MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED, or SERVICE_UI_ALWAYS flags.</span></span> 
  
<span data-ttu-id="5e600-151">Si recibe toda o parte de la información de configuración del usuario por medio de una hoja de propiedades, establezca SERVICE_UI_ALLOWED en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="5e600-151">If you receive all or some of the configuration information from the user by way of a property sheet, set SERVICE_UI_ALLOWED in  _ulFlags_.</span></span> <span data-ttu-id="5e600-152">Si usa la información de propiedad existente solo para establecer la configuración predeterminada y el usuario puede cambiar la configuración, establezca SERVICE_UI_ALWAYS en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="5e600-152">If you use existing property information only to establish default settings and the user is able to change the settings, set SERVICE_UI_ALWAYS in  _ulFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5e600-153">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5e600-153">MFCMAPI reference</span></span>

<span data-ttu-id="5e600-154">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="5e600-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5e600-155">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="5e600-155">**File**</span></span>|<span data-ttu-id="5e600-156">**Función**</span><span class="sxs-lookup"><span data-stu-id="5e600-156">**Function**</span></span>|<span data-ttu-id="5e600-157">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="5e600-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5e600-158">MAPIProfileFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="5e600-158">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="5e600-159">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="5e600-159">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="5e600-160">MFCMAPI usa el método **IMsgServiceAdmin:: ConfigureMsgService** para configurar un servicio que se ha agregado a un perfil.</span><span class="sxs-lookup"><span data-stu-id="5e600-160">MFCMAPI uses the **IMsgServiceAdmin::ConfigureMsgService** method to configure a service that has been added to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5e600-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e600-161">See also</span></span>



[<span data-ttu-id="5e600-162">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="5e600-162">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="5e600-163">SPropValue</span><span class="sxs-lookup"><span data-stu-id="5e600-163">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="5e600-164">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5e600-164">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="5e600-165">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="5e600-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

