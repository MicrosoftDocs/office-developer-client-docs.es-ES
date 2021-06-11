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
ms.openlocfilehash: 56a5f153dbd563397b9216af32a715692d0876d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427881"
---
# <a name="msgserviceentry"></a><span data-ttu-id="1e003-103">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="1e003-103">MSGSERVICEENTRY</span></span>

  
  
<span data-ttu-id="1e003-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e003-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e003-105">Define un prototipo de una función de punto de entrada de servicio de mensajes para admitir la configuración del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1e003-105">Defines a prototype for a message service entry point function to support message service configuration.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1e003-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="1e003-106">Header file:</span></span>  <br/> |<span data-ttu-id="1e003-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="1e003-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="1e003-108">Función definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="1e003-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="1e003-109">Servicios de mensajes</span><span class="sxs-lookup"><span data-stu-id="1e003-109">Message services</span></span>  <br/> |
|<span data-ttu-id="1e003-110">Función definida llamada por:</span><span class="sxs-lookup"><span data-stu-id="1e003-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="1e003-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="1e003-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="1e003-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="1e003-112">Parameters</span></span>

 <span data-ttu-id="1e003-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="1e003-113">_hInstance_</span></span>
  
> <span data-ttu-id="1e003-114">[in] Identificador de la instancia del proveedor de serviciosDLL.</span><span class="sxs-lookup"><span data-stu-id="1e003-114">[in] Handle of the instance of the service providerDLL.</span></span> <span data-ttu-id="1e003-115">El identificador se usa normalmente para recuperar recursos.</span><span class="sxs-lookup"><span data-stu-id="1e003-115">The handle is typically used to retrieve resources.</span></span> 
    
 <span data-ttu-id="1e003-116">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="1e003-116">_lpMalloc_</span></span>
  
> <span data-ttu-id="1e003-117">[in] Puntero a un objeto de asignador de memoria que expone la **interfaz OLE IMalloc.**</span><span class="sxs-lookup"><span data-stu-id="1e003-117">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="1e003-118">Es posible que el servicio de mensajes necesite usar este método de asignación al trabajar con determinadas interfaces como **IStream**.</span><span class="sxs-lookup"><span data-stu-id="1e003-118">The message service may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="1e003-119">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="1e003-119">_lpMAPISup_</span></span>
  
> <span data-ttu-id="1e003-120">[in] Puntero a una [implementación de interfaz IMAPISupport: IUnknown.](imapisupportiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="1e003-120">[in] Pointer to an [IMAPISupport : IUnknown](imapisupportiunknown.md) interface implementation.</span></span> 
    
 <span data-ttu-id="1e003-121">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1e003-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="1e003-122">[in] Valor específico de la implementación que se usa para pasar información de la interfaz de usuario a una función o cero.</span><span class="sxs-lookup"><span data-stu-id="1e003-122">[in] An implementation-specific value used for passing user interface information to a function or zero.</span></span> <span data-ttu-id="1e003-123">El  _parámetro ulUIParam_ es el controlador de ventana principal del cuadro de diálogo de configuración y es de tipo HWND (se convierte en un ULONG_PTR).</span><span class="sxs-lookup"><span data-stu-id="1e003-123">The  _ulUIParam_ parameter is the parent window handle for the configuration dialog box and is of type HWND (cast to a ULONG_PTR).</span></span> <span data-ttu-id="1e003-124">Un valor de cero indica que no hay ninguna ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="1e003-124">A value of zero indicates that there is no parent window.</span></span> 
    
 <span data-ttu-id="1e003-125">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1e003-125">_ulFlags_</span></span>
  
> <span data-ttu-id="1e003-126">[in] Máscara de bits de marcas que indican las opciones de la función de entrada de servicio.</span><span class="sxs-lookup"><span data-stu-id="1e003-126">[in] Bitmask of flags indicating options for the service entry function.</span></span> <span data-ttu-id="1e003-127">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="1e003-127">The following flags can be set:</span></span>
    
<span data-ttu-id="1e003-128">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1e003-128">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1e003-129">Las cadenas pasadas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="1e003-129">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="1e003-130">Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="1e003-130">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="1e003-131">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="1e003-131">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="1e003-132">La interfaz de usuario de configuración del servicio debe mostrar la configuración actual, pero no permitir que el usuario la cambie.</span><span class="sxs-lookup"><span data-stu-id="1e003-132">The service's configuration user interface should display the current configuration but not allow the user to change it.</span></span> 
    
<span data-ttu-id="1e003-133">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="1e003-133">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="1e003-134">Permite mostrar un cuadro de diálogo de configuración si es necesario.</span><span class="sxs-lookup"><span data-stu-id="1e003-134">Permits a configuration dialog box to be displayed if necessary.</span></span> <span data-ttu-id="1e003-135">Cuando se SERVICE_UI_ALLOWED marca, el cuadro de diálogo solo debe mostrarse si la matriz de valores de la propiedad  _lpProps_ está vacía o no contiene una configuración válida.</span><span class="sxs-lookup"><span data-stu-id="1e003-135">When the SERVICE_UI_ALLOWED flag is set, the dialog box should be displayed only if the  _lpProps_ property value array is empty or does not contain a valid configuration.</span></span> <span data-ttu-id="1e003-136">Si SERVICE_UI_ALLOWED no está establecido, es posible que se muestre un cuadro de diálogo si se SERVICE_UI_ALWAYS marca.</span><span class="sxs-lookup"><span data-stu-id="1e003-136">If SERVICE_UI_ALLOWED is not set, a dialog box might still be displayed if the SERVICE_UI_ALWAYS flag is set.</span></span> 
    
<span data-ttu-id="1e003-137">UI_CURRENT_PROVIDER_FIRST</span><span class="sxs-lookup"><span data-stu-id="1e003-137">UI_CURRENT_PROVIDER_FIRST</span></span> 
  
> <span data-ttu-id="1e003-138">Solicita que el cuadro de diálogo de configuración del proveedor activo se muestre encima de otros cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1e003-138">Requests that the configuration dialog box for the active provider be displayed on top of other dialog boxes.</span></span> 
    
<span data-ttu-id="1e003-139">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="1e003-139">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="1e003-140">Requiere que el servicio de mensajes muestre un cuadro de diálogo de configuración.</span><span class="sxs-lookup"><span data-stu-id="1e003-140">Requires the message service to display a configuration dialog box.</span></span> <span data-ttu-id="1e003-141">Si la marca SERVICE_UI_ALWAYS no está establecida, es posible que se muestre un cuadro de diálogo de configuración si se establece la marca SERVICE_UI_ALLOWED y la información de configuración válida no está disponible en la matriz de valores de la propiedad _lpProps._</span><span class="sxs-lookup"><span data-stu-id="1e003-141">If the SERVICE_UI_ALWAYS flag is not set, a configuration dialog box might still be displayed if the SERVICE_UI_ALLOWED flag is set and valid configuration information is not available from the  _lpProps_ property value array.</span></span> <span data-ttu-id="1e003-142">Debe SERVICE_UI_ALLOWED o SERVICE_UI_ALWAYS para permitir que se muestre una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1e003-142">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set to allow a user interface to be displayed.</span></span> 
    
 <span data-ttu-id="1e003-143">_ulContext_</span><span class="sxs-lookup"><span data-stu-id="1e003-143">_ulContext_</span></span>
  
> <span data-ttu-id="1e003-144">[in] La operación de configuración que MAPI está realizando actualmente.</span><span class="sxs-lookup"><span data-stu-id="1e003-144">[in] The configuration operation that MAPI is currently performing.</span></span> <span data-ttu-id="1e003-145">El  _parámetro ulContext_ contendrá uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="1e003-145">The  _ulContext_ parameter will contain one of the following values:</span></span> 
    
<span data-ttu-id="1e003-146">MSG_SERVICE_CONFIGURE</span><span class="sxs-lookup"><span data-stu-id="1e003-146">MSG_SERVICE_CONFIGURE</span></span> 
  
> <span data-ttu-id="1e003-147">Los cambios en la configuración del servicio deben realizarse en el perfil.</span><span class="sxs-lookup"><span data-stu-id="1e003-147">Changes to the service's configuration should be made in the profile.</span></span> <span data-ttu-id="1e003-148">Si se SERVICE_UI_ALWAYS marca, el servicio debe mostrar su cuadro de diálogo de configuración.</span><span class="sxs-lookup"><span data-stu-id="1e003-148">If the SERVICE_UI_ALWAYS flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="1e003-149">El cuadro de diálogo también debe mostrarse si se establece la marca SERVICE_UI_ALLOWED y el parámetro  _lpProps_ está vacío o no contiene datos de configuración válidos.</span><span class="sxs-lookup"><span data-stu-id="1e003-149">The dialog box should also be displayed if the SERVICE_UI_ALLOWED flag is set and the  _lpProps_ parameter is empty or does not contain valid configuration data.</span></span> <span data-ttu-id="1e003-150">Si lpProps contiene datos  _válidos,_ no se debe mostrar ningún cuadro de diálogo y el servicio debe usar estos datos para realizar el cambio de configuración.</span><span class="sxs-lookup"><span data-stu-id="1e003-150">If  _lpProps_ contains valid data, no dialog box should be displayed and the service should use this data for making the configuration change.</span></span> 
    
<span data-ttu-id="1e003-151">MSG_SERVICE_CREATE</span><span class="sxs-lookup"><span data-stu-id="1e003-151">MSG_SERVICE_CREATE</span></span> 
  
> <span data-ttu-id="1e003-152">El servicio se está agregando a un perfil.</span><span class="sxs-lookup"><span data-stu-id="1e003-152">The service is being added to a profile.</span></span> <span data-ttu-id="1e003-153">Si se establece SERVICE_UI_ALWAYS o SERVICE_UI_ALLOWED marca, el servicio debe mostrar su cuadro de diálogo de configuración.</span><span class="sxs-lookup"><span data-stu-id="1e003-153">If either the SERVICE_UI_ALWAYS or SERVICE_UI_ALLOWED flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="1e003-154">Si no se establece ninguna marca, el servicio debe producir un error.</span><span class="sxs-lookup"><span data-stu-id="1e003-154">If neither flag is set, the service should fail.</span></span> 
    
<span data-ttu-id="1e003-155">MSG_SERVICE_DELETE</span><span class="sxs-lookup"><span data-stu-id="1e003-155">MSG_SERVICE_DELETE</span></span> 
  
> <span data-ttu-id="1e003-156">El servicio se está quitando de un perfil.</span><span class="sxs-lookup"><span data-stu-id="1e003-156">The service is being removed from a profile.</span></span> <span data-ttu-id="1e003-157">Después de recibir este evento, el servicio debe devolver S_OK.</span><span class="sxs-lookup"><span data-stu-id="1e003-157">After receiving this event, the service should return S_OK.</span></span>
    
<span data-ttu-id="1e003-158">MSG_SERVICE_INSTALL</span><span class="sxs-lookup"><span data-stu-id="1e003-158">MSG_SERVICE_INSTALL</span></span> 
  
> <span data-ttu-id="1e003-159">El servicio se ha instalado en la estación de trabajo del usuario desde una red, un disquete u otro medio externo.</span><span class="sxs-lookup"><span data-stu-id="1e003-159">The service has been installed to the user's workstation from a network, floppy disk, or other external medium.</span></span> <span data-ttu-id="1e003-160">Después de recibir este evento, el servicio normalmente devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="1e003-160">After receiving this event, the service usually returns S_OK.</span></span> 
    
<span data-ttu-id="1e003-161">MSG_SERVICE_PROVIDER_CREATE</span><span class="sxs-lookup"><span data-stu-id="1e003-161">MSG_SERVICE_PROVIDER_CREATE</span></span> 
  
> <span data-ttu-id="1e003-162">Solicita que el servicio cree una instancia adicional de un proveedor.</span><span class="sxs-lookup"><span data-stu-id="1e003-162">Requests that the service create an additional instance of a provider.</span></span> <span data-ttu-id="1e003-163">Si el servicio admite esta operación, debe llamar a [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md).</span><span class="sxs-lookup"><span data-stu-id="1e003-163">If the service supports this operation, it should call [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md).</span></span> <span data-ttu-id="1e003-164">Si el servicio no admite esta operación, puede devolver MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="1e003-164">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="1e003-165">MSG_SERVICE_PROVIDER_DELETE</span><span class="sxs-lookup"><span data-stu-id="1e003-165">MSG_SERVICE_PROVIDER_DELETE</span></span> 
  
> <span data-ttu-id="1e003-166">Solicita que el servicio elimine una instancia de proveedor.</span><span class="sxs-lookup"><span data-stu-id="1e003-166">Requests that the service delete a provider instance.</span></span> <span data-ttu-id="1e003-167">Si el servicio admite esta operación, debe llamar a [IProviderAdmin::D eleteProvider](iprovideradmin-deleteprovider.md).</span><span class="sxs-lookup"><span data-stu-id="1e003-167">If the service supports this operation, it should call [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md).</span></span> <span data-ttu-id="1e003-168">Si el servicio no admite esta operación, puede devolver MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="1e003-168">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span>
    
<span data-ttu-id="1e003-169">MSG_SERVICE_UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="1e003-169">MSG_SERVICE_UNINSTALL</span></span> 
  
> <span data-ttu-id="1e003-170">Se está quitando el servicio.</span><span class="sxs-lookup"><span data-stu-id="1e003-170">The service is being removed.</span></span> <span data-ttu-id="1e003-171">Después de recibir este evento, el servicio puede realizar las tareas de limpieza que deben realizarse antes de que finalice el servicio y, a continuación, devolver con un valor correcto.</span><span class="sxs-lookup"><span data-stu-id="1e003-171">After receiving this event, the service can perform any cleanup tasks that should be done before the service ends and then return with a success value.</span></span> <span data-ttu-id="1e003-172">Si el usuario cancela la eliminación, el servicio debe devolver MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="1e003-172">If the user cancels the removal, the service should return MAPI_E_USER_CANCEL.</span></span> 
    
 <span data-ttu-id="1e003-173">_cValues_</span><span class="sxs-lookup"><span data-stu-id="1e003-173">_cValues_</span></span>
  
> <span data-ttu-id="1e003-174">[in] Recuento de valores de propiedad en la matriz apuntada por el _parámetro lpProps._</span><span class="sxs-lookup"><span data-stu-id="1e003-174">[in] Count of property values in the array pointed to by the  _lpProps_ parameter.</span></span> <span data-ttu-id="1e003-175">El valor del parámetro  _cValues_ es cero si MAPI no pasa ningún valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="1e003-175">The value of the  _cValues_ parameter is zero if MAPI is passing no property values.</span></span> 
    
 <span data-ttu-id="1e003-176">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="1e003-176">_lpProps_</span></span>
  
> <span data-ttu-id="1e003-177">[in] Puntero a una matriz opcional de [estructuras SPropValue](spropvalue.md) que indica los valores de las propiedades admitidas por el proveedor que la función usará en la configuración del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1e003-177">[in] Pointer to an optional array of [SPropValue](spropvalue.md) structures indicating values for provider-supported properties that the function will use in configuring the message service.</span></span> <span data-ttu-id="1e003-178">La función solo usa este parámetro si  _el parámetro ulContext_ está establecido en MSG_SERVICE_CONFIGURE.</span><span class="sxs-lookup"><span data-stu-id="1e003-178">The function only uses this parameter if the  _ulContext_ parameter is set to MSG_SERVICE_CONFIGURE.</span></span> <span data-ttu-id="1e003-179">Este parámetro se usa normalmente para pasar la ruta de acceso a un archivo de un servicio basado en archivos, como un servicio de libreta de direcciones personal.</span><span class="sxs-lookup"><span data-stu-id="1e003-179">This parameter is commonly used to pass the path to a file for a file-based service, such as a personal address book service.</span></span> <span data-ttu-id="1e003-180">Si el MSG_SERVICE_CONFIGURE no se pasa en el  _parámetro ulFlags,_ el parámetro  _lpProps_ debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1e003-180">If the MSG_SERVICE_CONFIGURE flag is not passed in the  _ulFlags_ parameter, the  _lpProps_ parameter must be zero.</span></span> 
    
 <span data-ttu-id="1e003-181">_lpProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="1e003-181">_lpProviderAdmin_</span></span>
  
> <span data-ttu-id="1e003-182">[in] Puntero a una [interfaz IProviderAdmin:IUnknown](iprovideradminiunknown.md) que la función puede usar para buscar secciones de perfil para un proveedor específico en el servicio de mensajes actual.</span><span class="sxs-lookup"><span data-stu-id="1e003-182">[in] Pointer to an [IProviderAdmin:IUnknown](iprovideradminiunknown.md) interface that the function can use to locate profile sections for a specific provider in the current message service.</span></span> 
    
 <span data-ttu-id="1e003-183">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="1e003-183">_lppMapiError_</span></span>
  
> <span data-ttu-id="1e003-184">[salida] Puntero a una [estructura MAPIERROR.](mapierror.md)</span><span class="sxs-lookup"><span data-stu-id="1e003-184">[out] Pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="1e003-185">La estructura se asigna con la [función MAPIAllocateBuffer.](mapiallocatebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="1e003-185">The structure is allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> <span data-ttu-id="1e003-186">Todos los miembros son opcionales, aunque la mayoría de las estructuras contendrán una cadena de mensaje de error válida en el _miembro lpszError._</span><span class="sxs-lookup"><span data-stu-id="1e003-186">All members are optional, although most structures will contain a valid error message string in the  _lpszError_ member.</span></span> <span data-ttu-id="1e003-187">Si  _los miembros lpszComponent_ o  _lpszError_ de la estructura están presentes, su memoria debe liberarse con una sola llamada a [MAPIFreeBuffer](mapifreebuffer.md) en la estructura base.</span><span class="sxs-lookup"><span data-stu-id="1e003-187">If the  _lpszComponent_ or  _lpszError_ members of the structure are present, their memory must eventually be freed by a single call to [MAPIFreeBuffer](mapifreebuffer.md) on the base structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1e003-188">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e003-188">Return value</span></span>

<span data-ttu-id="1e003-189">S_OK</span><span class="sxs-lookup"><span data-stu-id="1e003-189">S_OK</span></span> 
  
> <span data-ttu-id="1e003-190">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="1e003-190">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="1e003-191">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="1e003-191">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="1e003-192">El proveedor de servicios no se ha configurado.</span><span class="sxs-lookup"><span data-stu-id="1e003-192">The service provider has not been configured.</span></span> 
    
<span data-ttu-id="1e003-193">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="1e003-193">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="1e003-194">El usuario canceló la operación, normalmente haciendo clic en el **botón Cancelar** de un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1e003-194">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
<span data-ttu-id="1e003-195">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="1e003-195">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="1e003-196">El proveedor no admite cambios en sus objetos o no admite la notificación de cambios.</span><span class="sxs-lookup"><span data-stu-id="1e003-196">The provider either does not support changes to its objects or does not support notification of changes.</span></span> 
    
<span data-ttu-id="1e003-197">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="1e003-197">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="1e003-198">La marca MAPI_UNICODE se estableció y la implementación no admite Unicode, o MAPI_UNICODE no se estableció y la implementación solo admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="1e003-198">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1e003-199">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1e003-199">Remarks</span></span>

<span data-ttu-id="1e003-200">Una función definida mediante el prototipo de función **MSGSERVICEENTRY** permite a los servicios de mensajes configurarse a sí mismos o realizar otras acciones específicas del servicio.</span><span class="sxs-lookup"><span data-stu-id="1e003-200">A function defined using the **MSGSERVICEENTRY** function prototype enables message services to configure themselves or to perform other service-specific actions.</span></span> <span data-ttu-id="1e003-201">La función proporciona principalmente un cuadro de diálogo en el que el usuario puede cambiar la configuración específica del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1e003-201">The function primarily furnishes a dialog box in which the user can change settings specific to the message service.</span></span> <span data-ttu-id="1e003-202">También puede admitir la configuración mediante programación mediante la matriz de valores de propiedad pasada en el _parámetro lpProps._</span><span class="sxs-lookup"><span data-stu-id="1e003-202">It can also support programmatic configuration by using the property value array passed in the  _lpProps_ parameter.</span></span> <span data-ttu-id="1e003-203">La configuración mediante programación es opcional a menos que el servicio admita el Asistente para perfiles, para el que es necesario.</span><span class="sxs-lookup"><span data-stu-id="1e003-203">Programmatic configuration is optional unless the service supports the Profile Wizard, for which it is required.</span></span> 
  
<span data-ttu-id="1e003-204">MAPI llama a este punto de entrada desde la aplicación del Panel de control o en respuesta a una aplicación cliente que llama a [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) o [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="1e003-204">MAPI calls this entry point from the Control Panel application or in response to a client application calling [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) or [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="1e003-205">MAPI no establece ninguna restricción en el nombre de función que un servicio de mensajes usa para el prototipo **MSGSERVICEENTRY,** pero prefiere el nombre **ServiceEntry**.</span><span class="sxs-lookup"><span data-stu-id="1e003-205">MAPI places no restriction on the function name that a message service uses for the **MSGSERVICEENTRY** prototype but prefers the name **ServiceEntry**.</span></span> <span data-ttu-id="1e003-206">No hay ninguna restricción en el ordinal para la función y un único DLL de proveedor puede contener más de una función.</span><span class="sxs-lookup"><span data-stu-id="1e003-206">There is no restriction on the ordinal for the function, and a single provider DLL can contain more than one function.</span></span> <span data-ttu-id="1e003-207">Sin embargo, solo una de las funciones se puede **denominar ServiceEntry**.</span><span class="sxs-lookup"><span data-stu-id="1e003-207">However, only one of the functions can be named **ServiceEntry**.</span></span> 
  
<span data-ttu-id="1e003-208">Un servicio de mensajes puede usar [la función BuildDisplayTable](builddisplaytable.md) y el método [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) para simplificar la implementación del cuadro de diálogo de configuración.</span><span class="sxs-lookup"><span data-stu-id="1e003-208">A message service can use the [BuildDisplayTable](builddisplaytable.md) function and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to simplify configuration dialog box implementation.</span></span> 
  
<span data-ttu-id="1e003-209">Es posible que un usuario cancele una MSG_SERVICE_UNINSTALL operación.</span><span class="sxs-lookup"><span data-stu-id="1e003-209">It is possible for a user to cancel a MSG_SERVICE_UNINSTALL operation.</span></span> <span data-ttu-id="1e003-210">En este caso, la función **ServiceEntry** debe comprobar con el usuario que no se debe quitar el servicio y devolver MAPI_E_USER_CANCEL si el servicio permanece instalado.</span><span class="sxs-lookup"><span data-stu-id="1e003-210">In this case, the **ServiceEntry** function should check with the user to verify that the service should not be removed and return MAPI_E_USER_CANCEL if the service remains installed.</span></span> 
  
<span data-ttu-id="1e003-211">Una función basada en el **prototipo MSGSERVICEENTRY** devuelve uno de los valores HRESULT enumerados.</span><span class="sxs-lookup"><span data-stu-id="1e003-211">A function based on the **MSGSERVICEENTRY** prototype returns one of the HRESULT values listed.</span></span> <span data-ttu-id="1e003-212">MAPI reenvía este valor al responder a la llamada de un cliente a [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="1e003-212">MAPI forwards this value when responding to a client's call to [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="1e003-213">Los servicios de mensajes que exportan una función de entrada de servicio deben incluir las propiedades **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) y **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) en la sección de servicio de mensajes de MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="1e003-213">Message services that export a service entry function must include the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) and **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) properties in the message service section of MAPISVC.INF.</span></span> 
  

