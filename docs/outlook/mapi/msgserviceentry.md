---
title: MSGSERVICEENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MSGSERVICEENTRY
api_type:
- COM
ms.assetid: 655774a6-588c-44c7-903b-4497b7eccbc2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 954609cbc62039c0d60874bde83fde50d1d11c30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591670"
---
# <a name="msgserviceentry"></a><span data-ttu-id="a7dc4-103">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="a7dc4-103">MSGSERVICEENTRY</span></span>

  
  
<span data-ttu-id="a7dc4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7dc4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7dc4-105">Define un prototipo de una función de punto de entrada del servicio de mensaje admitir la configuración del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-105">Defines a prototype for a message service entry point function to support message service configuration.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a7dc4-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a7dc4-106">Header file:</span></span>  <br/> |<span data-ttu-id="a7dc4-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="a7dc4-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="a7dc4-108">Función definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="a7dc4-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="a7dc4-109">Servicios de mensajes</span><span class="sxs-lookup"><span data-stu-id="a7dc4-109">Message services</span></span>  <br/> |
|<span data-ttu-id="a7dc4-110">Llamado por una función definida:</span><span class="sxs-lookup"><span data-stu-id="a7dc4-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="a7dc4-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="a7dc4-111">MAPI</span></span>  <br/> |
   
```cpp
HRESULT MSGSERVICEENTRY(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulContext,
  ULONG cValues,
  LPSPropValue lpProps,
  LPPROVIDERADMIN lpProviderAdmin,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a><span data-ttu-id="a7dc4-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7dc4-112">Parameters</span></span>

 <span data-ttu-id="a7dc4-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="a7dc4-113">_hInstance_</span></span>
  
> <span data-ttu-id="a7dc4-114">[entrada] Identificador de la instancia de la providerDLL de servicio.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-114">[in] Handle of the instance of the service providerDLL.</span></span> <span data-ttu-id="a7dc4-115">El controlador se suele usar para recuperar recursos.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-115">The handle is typically used to retrieve resources.</span></span> 
    
 <span data-ttu-id="a7dc4-116">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="a7dc4-116">_lpMalloc_</span></span>
  
> <span data-ttu-id="a7dc4-117">[entrada] Puntero a un objeto del asignador de memoria exposición de la interfaz de OLE **IMalloc** .</span><span class="sxs-lookup"><span data-stu-id="a7dc4-117">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="a7dc4-118">El servicio de mensajes es posible que necesite utilizar este método de asignación cuando se trabaja con ciertas interfaces como **IStream**.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-118">The message service may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="a7dc4-119">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="a7dc4-119">_lpMAPISup_</span></span>
  
> <span data-ttu-id="a7dc4-120">[entrada] Puntero a un [IMAPISupport: IUnknown](imapisupportiunknown.md) implementación de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-120">[in] Pointer to an [IMAPISupport : IUnknown](imapisupportiunknown.md) interface implementation.</span></span> 
    
 <span data-ttu-id="a7dc4-121">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a7dc4-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="a7dc4-122">[entrada] Un valor específico de la implementación utilizado para pasar información de interfaz de usuario a una función o un valor cero.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-122">[in] An implementation-specific value used for passing user interface information to a function or zero.</span></span> <span data-ttu-id="a7dc4-123">El parámetro _ulUIParam_ es el identificador de ventana primario para el cuadro de diálogo de configuración y es de tipo HWND (conversión a un ULONG_PTR).</span><span class="sxs-lookup"><span data-stu-id="a7dc4-123">The  _ulUIParam_ parameter is the parent window handle for the configuration dialog box and is of type HWND (cast to a ULONG_PTR).</span></span> <span data-ttu-id="a7dc4-124">Un valor de cero indica que no hay ninguna ventana primario.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-124">A value of zero indicates that there is no parent window.</span></span> 
    
 <span data-ttu-id="a7dc4-125">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a7dc4-125">_ulFlags_</span></span>
  
> <span data-ttu-id="a7dc4-126">[entrada] Máscara de bits de marcadores que indica las opciones para la función de entrada de servicio.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-126">[in] Bitmask of flags indicating options for the service entry function.</span></span> <span data-ttu-id="a7dc4-127">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="a7dc4-127">The following flags can be set:</span></span>
    
<span data-ttu-id="a7dc4-128">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-128">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a7dc4-129">Las cadenas que se pasan en están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-129">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="a7dc4-130">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-130">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="a7dc4-131">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="a7dc4-131">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="a7dc4-132">Interfaz de usuario de configuración del servicio debe mostrar la configuración actual, pero no permitir que el usuario que la cambie.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-132">The service's configuration user interface should display the current configuration but not allow the user to change it.</span></span> 
    
<span data-ttu-id="a7dc4-133">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="a7dc4-133">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="a7dc4-134">Permite a un cuadro de diálogo de configuración que se mostrará si es necesario.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-134">Permits a configuration dialog box to be displayed if necessary.</span></span> <span data-ttu-id="a7dc4-135">Cuando se establece la marca SERVICE_UI_ALLOWED, se debe mostrar el cuadro de diálogo sólo si la matriz de valores de propiedad _lpProps_ está vacía o no contiene una configuración válida.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-135">When the SERVICE_UI_ALLOWED flag is set, the dialog box should be displayed only if the  _lpProps_ property value array is empty or does not contain a valid configuration.</span></span> <span data-ttu-id="a7dc4-136">Si no se establece SERVICE_UI_ALLOWED, aún es posible que mostrará un cuadro de diálogo si se establece la marca SERVICE_UI_ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-136">If SERVICE_UI_ALLOWED is not set, a dialog box might still be displayed if the SERVICE_UI_ALWAYS flag is set.</span></span> 
    
<span data-ttu-id="a7dc4-137">UI_CURRENT_PROVIDER_FIRST</span><span class="sxs-lookup"><span data-stu-id="a7dc4-137">UI_CURRENT_PROVIDER_FIRST</span></span> 
  
> <span data-ttu-id="a7dc4-138">Solicitudes que se muestre el cuadro de diálogo de configuración para el proveedor activo encima de otros cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-138">Requests that the configuration dialog box for the active provider be displayed on top of other dialog boxes.</span></span> 
    
<span data-ttu-id="a7dc4-139">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="a7dc4-139">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="a7dc4-140">Requiere el servicio de mensajes para mostrar un cuadro de diálogo de configuración.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-140">Requires the message service to display a configuration dialog box.</span></span> <span data-ttu-id="a7dc4-141">Si no está establecido el indicador SERVICE_UI_ALWAYS, aún es posible que mostrará un cuadro de diálogo Configuración si se establece la marca SERVICE_UI_ALLOWED y no está disponible desde la matriz de valores de propiedad de _lpProps_ información de configuración válido.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-141">If the SERVICE_UI_ALWAYS flag is not set, a configuration dialog box might still be displayed if the SERVICE_UI_ALLOWED flag is set and valid configuration information is not available from the  _lpProps_ property value array.</span></span> <span data-ttu-id="a7dc4-142">SERVICE_UI_ALLOWED o SERVICE_UI_ALWAYS se debe establecer para permitir una interfaz de usuario que se mostrará.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-142">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set to allow a user interface to be displayed.</span></span> 
    
 <span data-ttu-id="a7dc4-143">_ulContext_</span><span class="sxs-lookup"><span data-stu-id="a7dc4-143">_ulContext_</span></span>
  
> <span data-ttu-id="a7dc4-144">[entrada] La operación de configuración que MAPI está realizando actualmente.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-144">[in] The configuration operation that MAPI is currently performing.</span></span> <span data-ttu-id="a7dc4-145">El parámetro _ulContext_ contendrá uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="a7dc4-145">The  _ulContext_ parameter will contain one of the following values:</span></span> 
    
<span data-ttu-id="a7dc4-146">MSG_SERVICE_CONFIGURE</span><span class="sxs-lookup"><span data-stu-id="a7dc4-146">MSG_SERVICE_CONFIGURE</span></span> 
  
> <span data-ttu-id="a7dc4-147">Se deben realizar cambios a la configuración del servicio en el perfil.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-147">Changes to the service's configuration should be made in the profile.</span></span> <span data-ttu-id="a7dc4-148">Si se establece la marca SERVICE_UI_ALWAYS, el servicio debe mostrar su cuadro de diálogo de configuración.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-148">If the SERVICE_UI_ALWAYS flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="a7dc4-149">También se debe mostrar el cuadro de diálogo si se establece la marca SERVICE_UI_ALLOWED y el parámetro _lpProps_ está vacío o no contiene datos de configuración válida.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-149">The dialog box should also be displayed if the SERVICE_UI_ALLOWED flag is set and the  _lpProps_ parameter is empty or does not contain valid configuration data.</span></span> <span data-ttu-id="a7dc4-150">Si _lpProps_ contiene datos válidos, no se debería mostrar ningún cuadro de diálogo y el servicio debe utilizar estos datos para realizar el cambio de configuración.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-150">If  _lpProps_ contains valid data, no dialog box should be displayed and the service should use this data for making the configuration change.</span></span> 
    
<span data-ttu-id="a7dc4-151">MSG_SERVICE_CREATE</span><span class="sxs-lookup"><span data-stu-id="a7dc4-151">MSG_SERVICE_CREATE</span></span> 
  
> <span data-ttu-id="a7dc4-152">El servicio se agrega a un perfil.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-152">The service is being added to a profile.</span></span> <span data-ttu-id="a7dc4-153">Si se establece la marca de la SERVICE_UI_ALWAYS o SERVICE_UI_ALLOWED, el servicio debe mostrar su cuadro de diálogo de configuración.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-153">If either the SERVICE_UI_ALWAYS or SERVICE_UI_ALLOWED flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="a7dc4-154">Si se establece ninguna marca, debería producirá un error en el servicio.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-154">If neither flag is set, the service should fail.</span></span> 
    
<span data-ttu-id="a7dc4-155">MSG_SERVICE_DELETE</span><span class="sxs-lookup"><span data-stu-id="a7dc4-155">MSG_SERVICE_DELETE</span></span> 
  
> <span data-ttu-id="a7dc4-156">El servicio se está quitando de un perfil.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-156">The service is being removed from a profile.</span></span> <span data-ttu-id="a7dc4-157">Después de recibir este evento, el servicio debe devolver S_OK.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-157">After receiving this event, the service should return S_OK.</span></span>
    
<span data-ttu-id="a7dc4-158">MSG_SERVICE_INSTALL</span><span class="sxs-lookup"><span data-stu-id="a7dc4-158">MSG_SERVICE_INSTALL</span></span> 
  
> <span data-ttu-id="a7dc4-159">El servicio se ha instalado en estación de trabajo del usuario de una red, disquete u otro medio externo.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-159">The service has been installed to the user's workstation from a network, floppy disk, or other external medium.</span></span> <span data-ttu-id="a7dc4-160">Después de recibir este evento, el servicio normalmente devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-160">After receiving this event, the service usually returns S_OK.</span></span> 
    
<span data-ttu-id="a7dc4-161">MSG_SERVICE_PROVIDER_CREATE</span><span class="sxs-lookup"><span data-stu-id="a7dc4-161">MSG_SERVICE_PROVIDER_CREATE</span></span> 
  
> <span data-ttu-id="a7dc4-162">Solicitudes que el servicio de creación de una instancia adicional de un proveedor.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-162">Requests that the service create an additional instance of a provider.</span></span> <span data-ttu-id="a7dc4-163">Si el servicio admite esta operación, debe llamar a [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md).</span><span class="sxs-lookup"><span data-stu-id="a7dc4-163">If the service supports this operation, it should call [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md).</span></span> <span data-ttu-id="a7dc4-164">Si el servicio no es compatible con esta operación, puede devolver MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-164">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="a7dc4-165">MSG_SERVICE_PROVIDER_DELETE</span><span class="sxs-lookup"><span data-stu-id="a7dc4-165">MSG_SERVICE_PROVIDER_DELETE</span></span> 
  
> <span data-ttu-id="a7dc4-166">Solicitudes que el servicio de eliminación de una instancia del proveedor.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-166">Requests that the service delete a provider instance.</span></span> <span data-ttu-id="a7dc4-167">Si el servicio admite esta operación, debe llamar a [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md).</span><span class="sxs-lookup"><span data-stu-id="a7dc4-167">If the service supports this operation, it should call [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md).</span></span> <span data-ttu-id="a7dc4-168">Si el servicio no es compatible con esta operación, puede devolver MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-168">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span>
    
<span data-ttu-id="a7dc4-169">MSG_SERVICE_UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="a7dc4-169">MSG_SERVICE_UNINSTALL</span></span> 
  
> <span data-ttu-id="a7dc4-170">El servicio se está eliminando.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-170">The service is being removed.</span></span> <span data-ttu-id="a7dc4-171">Después de recibir este evento, el servicio puede realizar las tareas de limpieza que deben llevarse a cabo antes de que el servicio termina y, a continuación, devolver con un valor de éxito.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-171">After receiving this event, the service can perform any cleanup tasks that should be done before the service ends and then return with a success value.</span></span> <span data-ttu-id="a7dc4-172">Si el usuario cancela la eliminación, el servicio debe devolver MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-172">If the user cancels the removal, the service should return MAPI_E_USER_CANCEL.</span></span> 
    
 <span data-ttu-id="a7dc4-173">_cValues_</span><span class="sxs-lookup"><span data-stu-id="a7dc4-173">_cValues_</span></span>
  
> <span data-ttu-id="a7dc4-174">[entrada] Recuento de valores de propiedad en la matriz indicada por el parámetro _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="a7dc4-174">[in] Count of property values in the array pointed to by the  _lpProps_ parameter.</span></span> <span data-ttu-id="a7dc4-175">El valor del parámetro _cValues_ es cero si MAPI no está pasando valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-175">The value of the  _cValues_ parameter is zero if MAPI is passing no property values.</span></span> 
    
 <span data-ttu-id="a7dc4-176">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="a7dc4-176">_lpProps_</span></span>
  
> <span data-ttu-id="a7dc4-177">[entrada] Puntero a una matriz opcional de [SPropValue](spropvalue.md) de las estructuras que indica los valores de propiedades compatibles con el proveedor que se va a usar la función en la configuración del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-177">[in] Pointer to an optional array of [SPropValue](spropvalue.md) structures indicating values for provider-supported properties that the function will use in configuring the message service.</span></span> <span data-ttu-id="a7dc4-178">La función sólo usa este parámetro si el parámetro _ulContext_ se establece en MSG_SERVICE_CONFIGURE.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-178">The function only uses this parameter if the  _ulContext_ parameter is set to MSG_SERVICE_CONFIGURE.</span></span> <span data-ttu-id="a7dc4-179">Este parámetro se usa con frecuencia para pasar la ruta de acceso a un archivo para un servicio basado en archivos, como un servicio de libreta de direcciones personales.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-179">This parameter is commonly used to pass the path to a file for a file-based service, such as a personal address book service.</span></span> <span data-ttu-id="a7dc4-180">Si no se pasa el indicador MSG_SERVICE_CONFIGURE en el parámetro _ulFlags_ , el parámetro _lpProps_ debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-180">If the MSG_SERVICE_CONFIGURE flag is not passed in the  _ulFlags_ parameter, the  _lpProps_ parameter must be zero.</span></span> 
    
 <span data-ttu-id="a7dc4-181">_lpProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="a7dc4-181">_lpProviderAdmin_</span></span>
  
> <span data-ttu-id="a7dc4-182">[entrada] Puntero a una interfaz [IProviderAdmin:IUnknown](iprovideradminiunknown.md) que puede usar la función para localizar las secciones de perfil para un proveedor específico en el servicio de mensajes actual.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-182">[in] Pointer to an [IProviderAdmin:IUnknown](iprovideradminiunknown.md) interface that the function can use to locate profile sections for a specific provider in the current message service.</span></span> 
    
 <span data-ttu-id="a7dc4-183">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="a7dc4-183">_lppMapiError_</span></span>
  
> <span data-ttu-id="a7dc4-184">[out] Puntero a una estructura [MAPIERROR](mapierror.md) .</span><span class="sxs-lookup"><span data-stu-id="a7dc4-184">[out] Pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="a7dc4-185">Se asigna la estructura con la función [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="a7dc4-185">The structure is allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> <span data-ttu-id="a7dc4-186">Todos los miembros son opcionales, aunque la mayoría de las estructuras contendrá una cadena de mensaje de error válido en el miembro _lpszError_ .</span><span class="sxs-lookup"><span data-stu-id="a7dc4-186">All members are optional, although most structures will contain a valid error message string in the  _lpszError_ member.</span></span> <span data-ttu-id="a7dc4-187">Si están presentes los miembros _lpszComponent_ o _lpszError_ de la estructura, su memoria finalmente se debe liberar mediante una simple llamada a [MAPIFreeBuffer](mapifreebuffer.md) en la estructura de base.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-187">If the  _lpszComponent_ or  _lpszError_ members of the structure are present, their memory must eventually be freed by a single call to [MAPIFreeBuffer](mapifreebuffer.md) on the base structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a7dc4-188">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7dc4-188">Return value</span></span>

<span data-ttu-id="a7dc4-189">S_OK</span><span class="sxs-lookup"><span data-stu-id="a7dc4-189">S_OK</span></span> 
  
> <span data-ttu-id="a7dc4-190">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-190">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="a7dc4-191">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="a7dc4-191">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="a7dc4-192">No se ha configurado el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-192">The service provider has not been configured.</span></span> 
    
<span data-ttu-id="a7dc4-193">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="a7dc4-193">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="a7dc4-194">El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-194">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
<span data-ttu-id="a7dc4-195">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="a7dc4-195">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="a7dc4-196">El proveedor no admite los cambios realizados en sus objetos o no admite la notificación de cambios.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-196">The provider either does not support changes to its objects or does not support notification of changes.</span></span> 
    
<span data-ttu-id="a7dc4-197">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="a7dc4-197">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="a7dc4-198">Se ha establecido el indicador MAPI_UNICODE y la implementación no es compatible con Unicode, o bien, no se ha establecido MAPI_UNICODE y la implementación sólo es compatible con Unicode.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-198">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a7dc4-199">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a7dc4-199">Remarks</span></span>

<span data-ttu-id="a7dc4-200">Una función definida mediante el prototipo de función **MSGSERVICEENTRY** habilita los servicios de mensaje para configurar ellos mismos o para llevar a cabo otras acciones específicas al servicio.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-200">A function defined using the **MSGSERVICEENTRY** function prototype enables message services to configure themselves or to perform other service-specific actions.</span></span> <span data-ttu-id="a7dc4-201">La función principalmente proporciona un cuadro de diálogo en el que el usuario puede cambiar valores de configuración específicos para el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-201">The function primarily furnishes a dialog box in which the user can change settings specific to the message service.</span></span> <span data-ttu-id="a7dc4-202">También puede admitir configuración mediante programación mediante el uso de la matriz de valores de propiedad pasada en el parámetro _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="a7dc4-202">It can also support programmatic configuration by using the property value array passed in the  _lpProps_ parameter.</span></span> <span data-ttu-id="a7dc4-203">Configuración mediante programación es opcional, a menos que el servicio admite al Asistente para perfiles, para la que se requiere.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-203">Programmatic configuration is optional unless the service supports the Profile Wizard, for which it is required.</span></span> 
  
<span data-ttu-id="a7dc4-204">MAPI llama a este punto de entrada de la aplicación de Panel de Control o en respuesta a una aplicación cliente de una llamada a [IMsgServiceAdmin::](imsgserviceadmin-createmsgservice.md) o [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="a7dc4-204">MAPI calls this entry point from the Control Panel application or in response to a client application calling [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) or [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="a7dc4-205">MAPI no coloca ninguna restricción en el nombre de la función que un servicio de mensajes se usa para el prototipo **MSGSERVICEENTRY** pero prefiere el nombre de la **entrada de servicio**.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-205">MAPI places no restriction on the function name that a message service uses for the **MSGSERVICEENTRY** prototype but prefers the name **ServiceEntry**.</span></span> <span data-ttu-id="a7dc4-206">No hay ninguna restricción en el ordinal de la función y un único proveedor DLL puede contener más de una función.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-206">There is no restriction on the ordinal for the function, and a single provider DLL can contain more than one function.</span></span> <span data-ttu-id="a7dc4-207">Sin embargo, se puede denominar sólo una de las funciones de **entrada de servicio**.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-207">However, only one of the functions can be named **ServiceEntry**.</span></span> 
  
<span data-ttu-id="a7dc4-208">Un servicio de mensaje puede usar la función [BuildDisplayTable](builddisplaytable.md) y el método [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) para simplificar la implementación de cuadro de diálogo de configuración.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-208">A message service can use the [BuildDisplayTable](builddisplaytable.md) function and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to simplify configuration dialog box implementation.</span></span> 
  
<span data-ttu-id="a7dc4-209">Es posible que un usuario cancelar una operación de MSG_SERVICE_UNINSTALL.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-209">It is possible for a user to cancel a MSG_SERVICE_UNINSTALL operation.</span></span> <span data-ttu-id="a7dc4-210">En este caso, la función de **entrada de servicio** debe comprobar con el usuario para comprobar que el servicio no debe quitarse y devolver MAPI_E_USER_CANCEL si el servicio permanecerá instalado.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-210">In this case, the **ServiceEntry** function should check with the user to verify that the service should not be removed and return MAPI_E_USER_CANCEL if the service remains installed.</span></span> 
  
<span data-ttu-id="a7dc4-211">Una función según el prototipo **MSGSERVICEENTRY** devuelve uno de los valores HRESULT enumerados.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-211">A function based on the **MSGSERVICEENTRY** prototype returns one of the HRESULT values listed.</span></span> <span data-ttu-id="a7dc4-212">MAPI reenvía este valor al responder a una llamada del cliente a [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="a7dc4-212">MAPI forwards this value when responding to a client's call to [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="a7dc4-213">Servicios de mensaje que exportan una función de entrada de servicio deben incluir las propiedades de **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) y **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) en la sección servicio de mensajes de MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="a7dc4-213">Message services that export a service entry function must include the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) and **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) properties in the message service section of MAPISVC.INF.</span></span> 
  

