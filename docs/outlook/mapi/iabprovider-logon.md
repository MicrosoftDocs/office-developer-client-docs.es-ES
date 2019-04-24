---
title: IABProviderLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Logon
api_type:
- COM
ms.assetid: f9468715-1674-4d14-81c8-2f24dbaa0453
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 59c6d4a05c91511ad8c481fd4ddbe42396442190
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348786"
---
# <a name="iabproviderlogon"></a><span data-ttu-id="8cf3e-103">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="8cf3e-103">IABProvider::Logon</span></span>

  
  
<span data-ttu-id="8cf3e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8cf3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8cf3e-105">Establece una conexión a una sesión activa.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-105">Establishes a connection to an active session.</span></span>
  
```cpp
HRESULT Logon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG ulFlags,
  ULONG FAR * lpulcbSecurity,
  LPBYTE FAR * lppbSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPABLOGON FAR * lppABLogon
);
```

## <a name="parameters"></a><span data-ttu-id="8cf3e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="8cf3e-106">Parameters</span></span>

 <span data-ttu-id="8cf3e-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="8cf3e-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="8cf3e-108">a Un puntero al objeto de compatibilidad del proveedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-108">[in] A pointer to the address book provider's support object.</span></span>
    
 <span data-ttu-id="8cf3e-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="8cf3e-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="8cf3e-110">a Identificador de la ventana primaria para el cuadro de diálogo de inicio de sesión que muestra el método de **Inicio de sesión** , si se permite.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-110">[in] A handle to the parent window for the logon dialog box that the **Logon** method displays, if permitted.</span></span> <span data-ttu-id="8cf3e-111">El parámetro _ulUIParam_ contiene el valor del parámetro del mismo nombre pasado a MAPI en la llamada anterior a la función [MAPILogonEx](mapilogonex.md) .</span><span class="sxs-lookup"><span data-stu-id="8cf3e-111">The  _ulUIParam_ parameter contains the value of the parameter of the same name passed to MAPI in the previous call to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
    
 <span data-ttu-id="8cf3e-112">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="8cf3e-112">_lpszProfileName_</span></span>
  
> <span data-ttu-id="8cf3e-113">a Un puntero al nombre del perfil de sesión.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-113">[in] A pointer to the name of the session profile.</span></span>
    
 <span data-ttu-id="8cf3e-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8cf3e-114">_ulFlags_</span></span>
  
> <span data-ttu-id="8cf3e-115">a Una máscara de máscara de marcadores que controla cómo se realiza el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-115">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="8cf3e-116">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="8cf3e-116">The following flags can be set:</span></span>
    
<span data-ttu-id="8cf3e-117">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="8cf3e-117">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="8cf3e-118">El proveedor no debe mostrar un cuadro de diálogo durante el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-118">The provider should not display a dialog box during logon.</span></span> <span data-ttu-id="8cf3e-119">Si no se establece esta marca, el proveedor puede mostrar un cuadro de diálogo para pedir al usuario que falta información de configuración.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-119">If this flag is not set, the provider can display a dialog box to prompt the user for missing configuration information.</span></span>
    
<span data-ttu-id="8cf3e-120">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="8cf3e-120">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="8cf3e-121">Permite que el **Inicio de sesión** vuelva correctamente, probablemente antes de que finalice el proceso de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-121">Enables **Logon** to return successfully, possibly before the logon process is finished.</span></span> 
    
<span data-ttu-id="8cf3e-122">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8cf3e-122">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8cf3e-123">Todas las cadenas deben estar en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-123">All strings should be in Unicode format.</span></span> <span data-ttu-id="8cf3e-124">Si no se establece la marca MAPI_UNICODE, las cadenas deben estar en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-124">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="8cf3e-125">_lpulcbSecurity_</span><span class="sxs-lookup"><span data-stu-id="8cf3e-125">_lpulcbSecurity_</span></span>
  
> <span data-ttu-id="8cf3e-126">[in, out] Un puntero al tamaño, en bytes, de la estructura de credenciales de seguridad apuntado por el parámetro _lppbSecurity_ .</span><span class="sxs-lookup"><span data-stu-id="8cf3e-126">[in, out] A pointer to the size, in bytes, of the security credentials structure pointed to by the  _lppbSecurity_ parameter.</span></span> <span data-ttu-id="8cf3e-127">En la entrada, el valor debe ser distinto de cero; en la salida, el valor debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-127">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="8cf3e-128">En ambos casos, los punteros deben ser válidos.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-128">In both cases, the pointers must be valid.</span></span> 
    
 <span data-ttu-id="8cf3e-129">_lppbSecurity_</span><span class="sxs-lookup"><span data-stu-id="8cf3e-129">_lppbSecurity_</span></span>
  
> <span data-ttu-id="8cf3e-130">[in, out] Un puntero a un puntero a credenciales de seguridad.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-130">[in, out] A pointer to a pointer to security credentials.</span></span> <span data-ttu-id="8cf3e-131">En la entrada, el valor debe ser distinto de cero; en la salida, el valor debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-131">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="8cf3e-132">En ambos casos, el puntero debe ser válido.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-132">In both cases the pointer must be valid.</span></span>
    
 <span data-ttu-id="8cf3e-133">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="8cf3e-133">_lppMAPIError_</span></span>
  
> <span data-ttu-id="8cf3e-134">contempla Un puntero a un puntero a una estructura [MAPIERROR](mapierror.md) .</span><span class="sxs-lookup"><span data-stu-id="8cf3e-134">[out] A pointer to a pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="8cf3e-135">El parámetro _lppMAPIError_ puede establecerse en NULL si no hay ninguna estructura **MAPIERROR** para devolver.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-135">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="8cf3e-136">_lppABLogon_</span><span class="sxs-lookup"><span data-stu-id="8cf3e-136">_lppABLogon_</span></span>
  
> <span data-ttu-id="8cf3e-137">contempla Un puntero a un puntero al objeto de inicio de sesión del proveedor.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-137">[out] A pointer to a pointer to the provider's logon object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8cf3e-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8cf3e-138">Return value</span></span>

<span data-ttu-id="8cf3e-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cf3e-139">S_OK</span></span> 
  
> <span data-ttu-id="8cf3e-140">Se estableció correctamente una conexión a una sesión activa.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-140">A connection to an active session was successfully established.</span></span>
    
<span data-ttu-id="8cf3e-141">MAPI_E_FAILONEPROVIDER</span><span class="sxs-lookup"><span data-stu-id="8cf3e-141">MAPI_E_FAILONEPROVIDER</span></span> 
  
> <span data-ttu-id="8cf3e-142">El proveedor no puede iniciar sesión, pero MAPI puede seguir iniciando sesión en los demás proveedores del servicio de mensajes al que pertenece el proveedor.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-142">The provider cannot log on, but MAPI can continue to log on the other providers in the message service to which the provider belongs.</span></span> 
    
<span data-ttu-id="8cf3e-143">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="8cf3e-143">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="8cf3e-144">El proveedor no tiene suficiente información para completar el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-144">The provider has insufficient information to complete the logon.</span></span> <span data-ttu-id="8cf3e-145">MAPI llama a la función de entrada del servicio de mensajes del proveedor.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-145">MAPI calls the provider's message service entry function.</span></span>
    
<span data-ttu-id="8cf3e-146">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="8cf3e-146">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="8cf3e-147">El servidor no está configurado para admitir la página de códigos del cliente.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-147">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="8cf3e-148">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="8cf3e-148">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="8cf3e-149">El servidor no está configurado para admitir la información de la configuración regional del cliente.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-149">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="8cf3e-150">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="8cf3e-150">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="8cf3e-151">El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** del cuadro de diálogo de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-151">The user canceled the operation, typically by clicking the **Cancel** button in the logon dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8cf3e-152">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8cf3e-152">Remarks</span></span>

<span data-ttu-id="8cf3e-153">Las conexiones se establecen con cada proveedor de la libreta de direcciones en el perfil de sesión cuando un cliente llama al método [IMAPISession:: OpenAddressBook](imapisession-openaddressbook.md) .</span><span class="sxs-lookup"><span data-stu-id="8cf3e-153">Connections are established with each address book provider in the session profile when a client calls the [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) method.</span></span> <span data-ttu-id="8cf3e-154">A continuación, **OpenAddressBook** llama al método de **Inicio de sesión** de cada proveedor.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-154">**OpenAddressBook** then calls each provider's **Logon** method.</span></span> 
  
<span data-ttu-id="8cf3e-155">El nombre de perfil señalado por el parámetro _lpszProfileName_ se muestra en el juego de caracteres del cliente del usuario como indica la presencia o ausencia del indicador MAPI_UNICODE en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="8cf3e-155">The profile name pointed to by the  _lpszProfileName_ parameter is displayed in the character set of the user's client as indicated by the presence or absence of the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8cf3e-156">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="8cf3e-156">Notes to implementers</span></span>

<span data-ttu-id="8cf3e-157">En la implementación del método **Logon** , llame al método [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) para registrar un identificador único o una estructura [MAPIUID](mapiuid.md) .</span><span class="sxs-lookup"><span data-stu-id="8cf3e-157">In your implementation of the **Logon** method, call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="8cf3e-158">Cada uno de los objetos tendrá un identificador de entrada que incluye este **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-158">Each of your objects will have an entry identifier that includes this **MAPIUID**.</span></span> <span data-ttu-id="8cf3e-159">MAPI usa **MAPIUID** para hacer coincidir un objeto con su proveedor.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-159">MAPI uses the **MAPIUID** to match an object with its provider.</span></span> <span data-ttu-id="8cf3e-160">Por ejemplo, cuando un cliente llama al método [IMAPISession:: OpenEntry](imapisession-openentry.md) para abrir un usuario de mensajería, **OpenEntry** examina la parte **MAPIUID** del identificador de entrada que se ha pasado y lo hace coincidir con un **MAPIUID** registrado por un proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-160">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open a messaging user, **OpenEntry** examines the **MAPIUID** portion of the entry identifier that was passed in and matches it with a **MAPIUID** registered by an address book provider.</span></span> 
  
<span data-ttu-id="8cf3e-161">Si un cliente inicia sesión en el proveedor más de una vez, es posible que desee registrar una **MAPIUID** diferente para cada inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-161">If a client logs on to your provider more than once, you may want to register a different **MAPIUID** for each logon.</span></span> <span data-ttu-id="8cf3e-162">El registro de estructuras **MAPIUID** únicas permite a MAPI enrutar correctamente las solicitudes a la instancia del proveedor adecuada.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-162">Registering unique **MAPIUID** structures enables MAPI to correctly route requests to the appropriate provider instance.</span></span> <span data-ttu-id="8cf3e-163">Sin embargo, es posible que quiera que cada objeto de inicio de sesión comparta un **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-163">However, you may want to have every logon object share one **MAPIUID**.</span></span> <span data-ttu-id="8cf3e-164">En este caso, debe ser capaz de controlar el enrutamiento personalmente en lugar de confiar en MAPI.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-164">In this case, you must be able to handle the routing yourself instead of relying on MAPI.</span></span> <span data-ttu-id="8cf3e-165">Para obtener más información acerca de cómo crear una **MAPIUID**, consulte [Registrating Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="8cf3e-165">For more information about how to create a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
  
<span data-ttu-id="8cf3e-166">El objeto de compatibilidad que MAPI pasa a su método de **Inicio de sesión** en el parámetro _lpMAPISup_ proporciona acceso a muchos de los métodos incluidos en la interfaz [IMAPISupport: IUnknown](imapisupportiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="8cf3e-166">The support object that MAPI passes to your **Logon** method in the  _lpMAPISup_ parameter provides access to many of the methods included in the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="8cf3e-167">MAPI crea un objeto de soporte que se personaliza para el tipo de proveedor.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-167">MAPI creates a support object that is customized to your type of provider.</span></span> <span data-ttu-id="8cf3e-168">Por ejemplo, si necesita iniciar sesión en un sistema de mensajería o servicio de directorio subyacente al establecer la conexión, puede llamar al método [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) para recuperar las credenciales de seguridad para este inicio de sesión en particular.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-168">For example, if you need to log on to an underlying messaging system or directory service when you establish your connection, you can call the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to retrieve security credentials for this particular logon session.</span></span> 
  
<span data-ttu-id="8cf3e-169">Si el **Inicio de sesión** es correcto, asegúrese de llamar al método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) del objeto support para incrementar su recuento de referencia.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-169">If **Logon** is successful, be sure that you call the support object's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> <span data-ttu-id="8cf3e-170">Esto permite que su proveedor conserve el puntero de objeto de soporte para el resto de la sesión.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-170">This enables your provider to hold onto the support object pointer for the rest of the session.</span></span> <span data-ttu-id="8cf3e-171">Si no llama a este método **AddRef** , MAPI descargará el proveedor.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-171">If you do not call this **AddRef** method, MAPI will unload your provider.</span></span> 
  
<span data-ttu-id="8cf3e-172">Puede incluir el nombre de perfil que se ha pasado en el parámetro _lpszProfileName_ en cuadros de diálogo de error, pantallas de inicio de sesión u otras interfaces de usuario.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-172">You can include the profile name passed in the  _lpszProfileName_ parameter in error dialog boxes, logon screens, or other user interfaces.</span></span> <span data-ttu-id="8cf3e-173">Para usar el nombre del perfil, cópielo en el almacén que ha asignado.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-173">To use the profile name, copy it to storage that you have allocated.</span></span> 
  
<span data-ttu-id="8cf3e-174">Cree un objeto de inicio de sesión y devuelva un puntero al mismo en el parámetro _lppABLogon_ .</span><span class="sxs-lookup"><span data-stu-id="8cf3e-174">Create a logon object and return a pointer to it in the  _lppABLogon_ parameter.</span></span> <span data-ttu-id="8cf3e-175">MAPI usa este objeto de inicio de sesión para realizar llamadas a los métodos en la implementación de [IABLogon](iablogoniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="8cf3e-175">MAPI uses this logon object to make calls to the methods in your [IABLogon](iablogoniunknown.md) implementation.</span></span> 
  
<span data-ttu-id="8cf3e-176">Si necesita una contraseña durante el inicio de sesión, muestre un cuadro de diálogo de inicio de sesión sólo si no se ha establecido la marca AB_NO_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-176">If you require a password during logon, display a logon dialog box only if the AB_NO_DIALOG flag is not set.</span></span> <span data-ttu-id="8cf3e-177">Si el usuario cancela el proceso de inicio de sesión, normalmente haciendo clic en el botón **Cancelar** del cuadro de diálogo, se devuelve MAPI_E_USER_CANCEL desde el **Inicio de sesión**.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-177">If the user cancels the logon process, typically by clicking the **Cancel** button in the dialog box, return MAPI_E_USER_CANCEL from **Logon**.</span></span>
  
<span data-ttu-id="8cf3e-178">Normalmente, cuando un proveedor de libretas de direcciones no puede iniciar sesión, MAPI deshabilita el servicio de mensajes al que pertenece el proveedor, es decir, MAPI no intentará establecer conexiones para ninguno de los demás proveedores que pertenezcan al servicio para el resto de la sesión dura.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-178">Typically, when an address book provider cannot log on, MAPI disables the message service to which the failing provider belongs—that is, MAPI will not try to establish connections for any of the other providers that belong to the service for the rest of the session's lifetime.</span></span> <span data-ttu-id="8cf3e-179">Sin embargo, si el proveedor no puede establecer una conexión y no desea deshabilitar todo el servicio, devuelva MAPI_E_FAILONEPROVIDER o MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-179">However, if your provider cannot establish a connection and you want not to disable the entire service, return either MAPI_E_FAILONEPROVIDER or MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="8cf3e-180">MAPI no deshabilitará el servicio de mensajes al que pertenece el proveedor.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-180">MAPI will not disable the message service to which the provider belongs.</span></span> 
  
<span data-ttu-id="8cf3e-181">Devuelve MAPI_E_FAILONEPROVIDER si se produce un error que no es lo suficientemente grave como para evitar que los otros proveedores del servicio de mensajes establezcan conexiones.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-181">Return MAPI_E_FAILONEPROVIDER if an error occurs that is not serious enough to prevent the other providers in the message service from establishing connections.</span></span> <span data-ttu-id="8cf3e-182">Devuelve MAPI_E_UNCONFIGURED si falta la información de configuración necesaria del perfil y no se puede mostrar un cuadro de diálogo para preguntarle al usuario.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-182">Return MAPI_E_UNCONFIGURED if the necessary configuration information is missing from the profile and you cannot display a dialog box to prompt the user.</span></span> <span data-ttu-id="8cf3e-183">MAPI responderá llamando a la función de punto de entrada del servicio de mensajes de su proveedor con MSG_SERVICE_CONFIGURE set como el parámetro _ulContext_ para dar al servicio una oportunidad de configurarse a sí mismo, ya sea mediante programación o mediante una hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-183">MAPI will respond by calling your provider's message service entry point function with MSG_SERVICE_CONFIGURE set as the  _ulContext_ parameter to give the service a chance to configure itself, either programmatically or using a property sheet.</span></span> <span data-ttu-id="8cf3e-184">Cuando la función de punto de entrada del servicio de mensajes haya finalizado, MAPI reintentará el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="8cf3e-184">When the message service entry point function has finished, MAPI retries the logon.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8cf3e-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="8cf3e-185">See also</span></span>



[<span data-ttu-id="8cf3e-186">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="8cf3e-186">IABLogon::Logoff</span></span>](iablogon-logoff.md)
  
[<span data-ttu-id="8cf3e-187">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="8cf3e-187">IABLogon::OpenEntry</span></span>](iablogon-openentry.md)
  
[<span data-ttu-id="8cf3e-188">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="8cf3e-188">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="8cf3e-189">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="8cf3e-189">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="8cf3e-190">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="8cf3e-190">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="8cf3e-191">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8cf3e-191">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

