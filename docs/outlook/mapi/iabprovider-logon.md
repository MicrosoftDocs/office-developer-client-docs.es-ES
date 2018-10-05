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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384111"
---
# <a name="iabproviderlogon"></a><span data-ttu-id="c0eb6-103">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="c0eb6-103">IABProvider::Logon</span></span>

  
  
<span data-ttu-id="c0eb6-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0eb6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0eb6-105">Establece una conexión a una sesión activa.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-105">Establishes a connection to an active session.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="c0eb6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c0eb6-106">Parameters</span></span>

 <span data-ttu-id="c0eb6-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="c0eb6-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="c0eb6-108">[entrada] Un puntero al objeto de soporte técnico del proveedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-108">[in] A pointer to the address book provider's support object.</span></span>
    
 <span data-ttu-id="c0eb6-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c0eb6-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="c0eb6-110">[entrada] Identificador de la ventana primaria para el cuadro de diálogo de inicio de sesión que muestra el método de **Inicio de sesión** , si se permite.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-110">[in] A handle to the parent window for the logon dialog box that the **Logon** method displays, if permitted.</span></span> <span data-ttu-id="c0eb6-111">El parámetro _ulUIParam_ contiene el valor del parámetro el mismo nombre que se pasan a MAPI en la llamada a la función [MAPILogonEx](mapilogonex.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-111">The  _ulUIParam_ parameter contains the value of the parameter of the same name passed to MAPI in the previous call to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
    
 <span data-ttu-id="c0eb6-112">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="c0eb6-112">_lpszProfileName_</span></span>
  
> <span data-ttu-id="c0eb6-113">[entrada] Un puntero al nombre del perfil de la sesión.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-113">[in] A pointer to the name of the session profile.</span></span>
    
 <span data-ttu-id="c0eb6-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c0eb6-114">_ulFlags_</span></span>
  
> <span data-ttu-id="c0eb6-115">[entrada] Una máscara de bits de indicadores que controla cómo se realiza el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-115">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="c0eb6-116">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="c0eb6-116">The following flags can be set:</span></span>
    
<span data-ttu-id="c0eb6-117">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="c0eb6-117">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="c0eb6-118">El proveedor no debe mostrar un cuadro de diálogo durante el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-118">The provider should not display a dialog box during logon.</span></span> <span data-ttu-id="c0eb6-119">Si no se establece este indicador, el proveedor puede mostrar un cuadro de diálogo para preguntar al usuario para que falta información de configuración.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-119">If this flag is not set, the provider can display a dialog box to prompt the user for missing configuration information.</span></span>
    
<span data-ttu-id="c0eb6-120">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="c0eb6-120">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="c0eb6-121">Permite el **Inicio de sesión** devolver de correctamente, posiblemente antes de que finalice el proceso de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-121">Enables **Logon** to return successfully, possibly before the logon process is finished.</span></span> 
    
<span data-ttu-id="c0eb6-122">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-122">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c0eb6-123">Todas las cadenas deben estar en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-123">All strings should be in Unicode format.</span></span> <span data-ttu-id="c0eb6-124">Si no está establecido el indicador MAPI_UNICODE., las cadenas deben estar en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-124">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="c0eb6-125">_lpulcbSecurity_</span><span class="sxs-lookup"><span data-stu-id="c0eb6-125">_lpulcbSecurity_</span></span>
  
> <span data-ttu-id="c0eb6-126">[entrada, salida] Un puntero al tamaño, en bytes, de la estructura de las credenciales de seguridad indicada por el parámetro _lppbSecurity_ .</span><span class="sxs-lookup"><span data-stu-id="c0eb6-126">[in, out] A pointer to the size, in bytes, of the security credentials structure pointed to by the  _lppbSecurity_ parameter.</span></span> <span data-ttu-id="c0eb6-127">En la entrada, el valor debe ser distinto de cero; en la salida, el valor debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-127">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="c0eb6-128">En ambos casos, los punteros deben ser válidos.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-128">In both cases, the pointers must be valid.</span></span> 
    
 <span data-ttu-id="c0eb6-129">_lppbSecurity_</span><span class="sxs-lookup"><span data-stu-id="c0eb6-129">_lppbSecurity_</span></span>
  
> <span data-ttu-id="c0eb6-130">[entrada, salida] Un puntero a un puntero a las credenciales de seguridad.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-130">[in, out] A pointer to a pointer to security credentials.</span></span> <span data-ttu-id="c0eb6-131">En la entrada, el valor debe ser distinto de cero; en la salida, el valor debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-131">On input, the value must be nonzero; on output, the value must be zero.</span></span> <span data-ttu-id="c0eb6-132">En ambos casos, el puntero debe ser válido.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-132">In both cases the pointer must be valid.</span></span>
    
 <span data-ttu-id="c0eb6-133">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="c0eb6-133">_lppMAPIError_</span></span>
  
> <span data-ttu-id="c0eb6-134">[out] Un puntero a un puntero a una estructura [MAPIERROR](mapierror.md) .</span><span class="sxs-lookup"><span data-stu-id="c0eb6-134">[out] A pointer to a pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="c0eb6-135">El parámetro _lppMAPIError_ se puede establecer en NULL si no hay ninguna estructura **MAPIERROR** para devolver.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-135">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="c0eb6-136">_lppABLogon_</span><span class="sxs-lookup"><span data-stu-id="c0eb6-136">_lppABLogon_</span></span>
  
> <span data-ttu-id="c0eb6-137">[out] Un puntero a un puntero al objeto de inicio de sesión del proveedor.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-137">[out] A pointer to a pointer to the provider's logon object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c0eb6-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0eb6-138">Return value</span></span>

<span data-ttu-id="c0eb6-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="c0eb6-139">S_OK</span></span> 
  
> <span data-ttu-id="c0eb6-140">Se estableció correctamente una conexión a una sesión activa.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-140">A connection to an active session was successfully established.</span></span>
    
<span data-ttu-id="c0eb6-141">MAPI_E_FAILONEPROVIDER</span><span class="sxs-lookup"><span data-stu-id="c0eb6-141">MAPI_E_FAILONEPROVIDER</span></span> 
  
> <span data-ttu-id="c0eb6-142">El proveedor no puede iniciar sesión, pero puede seguir los otros proveedores en el servicio de mensajes a la que pertenece el proveedor de inicio de sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-142">The provider cannot log on, but MAPI can continue to log on the other providers in the message service to which the provider belongs.</span></span> 
    
<span data-ttu-id="c0eb6-143">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="c0eb6-143">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="c0eb6-144">El proveedor tiene información suficiente para completar el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-144">The provider has insufficient information to complete the logon.</span></span> <span data-ttu-id="c0eb6-145">MAPI llama a la función de entrada de servicio de mensajes del proveedor.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-145">MAPI calls the provider's message service entry function.</span></span>
    
<span data-ttu-id="c0eb6-146">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="c0eb6-146">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="c0eb6-147">El servidor no está configurado para admitir la página de códigos del cliente.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-147">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="c0eb6-148">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="c0eb6-148">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="c0eb6-149">El servidor no está configurado para admitir la información de configuración regional del cliente.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-149">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="c0eb6-150">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="c0eb6-150">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="c0eb6-151">El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en el cuadro de diálogo de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-151">The user canceled the operation, typically by clicking the **Cancel** button in the logon dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c0eb6-152">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c0eb6-152">Remarks</span></span>

<span data-ttu-id="c0eb6-153">Las conexiones se establecen con cada proveedor de la libreta de direcciones en el perfil de sesión cuando un cliente llama al método [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) .</span><span class="sxs-lookup"><span data-stu-id="c0eb6-153">Connections are established with each address book provider in the session profile when a client calls the [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) method.</span></span> <span data-ttu-id="c0eb6-154">**OpenAddressBook** , a continuación, llama el método de **Inicio de sesión** de cada proveedor.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-154">**OpenAddressBook** then calls each provider's **Logon** method.</span></span> 
  
<span data-ttu-id="c0eb6-155">El nombre del perfil que apunta el parámetro _lpszProfileName_ se muestra en el juego de caracteres del cliente del usuario como se indica por la presencia o ausencia de la marca MAPI_UNICODE en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="c0eb6-155">The profile name pointed to by the  _lpszProfileName_ parameter is displayed in the character set of the user's client as indicated by the presence or absence of the MAPI_UNICODE flag in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c0eb6-156">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="c0eb6-156">Notes to implementers</span></span>

<span data-ttu-id="c0eb6-157">En la implementación del método de **Inicio de sesión** , llame al método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) para registrar un identificador único o la estructura [MAPIUID](mapiuid.md) .</span><span class="sxs-lookup"><span data-stu-id="c0eb6-157">In your implementation of the **Logon** method, call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method to register a unique identifier, or [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="c0eb6-158">Cada uno de los objetos tendrá un identificador de entrada que incluye este **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-158">Each of your objects will have an entry identifier that includes this **MAPIUID**.</span></span> <span data-ttu-id="c0eb6-159">MAPI utiliza el **MAPIUID** para que coincida con un objeto con su proveedor.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-159">MAPI uses the **MAPIUID** to match an object with its provider.</span></span> <span data-ttu-id="c0eb6-160">Por ejemplo, cuando un cliente llama al método [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir un usuario de mensajería, **OpenEntry** examina la parte **MAPIUID** del identificador de entrada que se pasó y coincide con un **MAPIUID** registrado por un proveedor de libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-160">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open a messaging user, **OpenEntry** examines the **MAPIUID** portion of the entry identifier that was passed in and matches it with a **MAPIUID** registered by an address book provider.</span></span> 
  
<span data-ttu-id="c0eb6-161">Si un cliente inicia sesión en su proveedor de más de una vez, es posible que desee registrar un **MAPIUID** de diferentes para cada inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-161">If a client logs on to your provider more than once, you may want to register a different **MAPIUID** for each logon.</span></span> <span data-ttu-id="c0eb6-162">Registrar las estructuras **MAPIUID** únicas permite MAPI enrutar correctamente las solicitudes a la instancia de proveedor adecuado.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-162">Registering unique **MAPIUID** structures enables MAPI to correctly route requests to the appropriate provider instance.</span></span> <span data-ttu-id="c0eb6-163">Sin embargo, es posible que desea que tengan cada objeto de inicio de sesión compartir uno **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-163">However, you may want to have every logon object share one **MAPIUID**.</span></span> <span data-ttu-id="c0eb6-164">En este caso, debe ser capaz de controlar el enrutamiento de sí mismo en lugar de depender de la MAPI.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-164">In this case, you must be able to handle the routing yourself instead of relying on MAPI.</span></span> <span data-ttu-id="c0eb6-165">Para obtener más información acerca de cómo crear un **MAPIUID**, vea [Identificadores únicos proveedor de servicio de registro](registering-service-provider-unique-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="c0eb6-165">For more information about how to create a **MAPIUID**, see [Registering Service Provider Unique Identifiers](registering-service-provider-unique-identifiers.md).</span></span>
  
<span data-ttu-id="c0eb6-166">El objeto de soporte técnico que MAPI se pasa al método de **Inicio de sesión** en el parámetro _lpMAPISup_ proporciona acceso a muchos de los métodos incluidos en la [IMAPISupport: IUnknown](imapisupportiunknown.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-166">The support object that MAPI passes to your **Logon** method in the  _lpMAPISup_ parameter provides access to many of the methods included in the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="c0eb6-167">MAPI crea un objeto de soporte técnico personalizado para el tipo de proveedor.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-167">MAPI creates a support object that is customized to your type of provider.</span></span> <span data-ttu-id="c0eb6-168">Por ejemplo, si necesita iniciar sesión en un sistema de mensajería subyacente o el servicio de directorio al establecer la conexión, puede llamar al método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para recuperar las credenciales de seguridad para esta sesión de inicio de sesión determinado.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-168">For example, if you need to log on to an underlying messaging system or directory service when you establish your connection, you can call the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to retrieve security credentials for this particular logon session.</span></span> 
  
<span data-ttu-id="c0eb6-169">Si el **Inicio de sesión** es correcta, asegúrese de que llame al método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) del objeto de soporte técnico para incrementar su recuento de referencia.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-169">If **Logon** is successful, be sure that you call the support object's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> <span data-ttu-id="c0eb6-170">Esto permite a su proveedor retener el puntero del objeto de soporte técnico para el resto de la sesión.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-170">This enables your provider to hold onto the support object pointer for the rest of the session.</span></span> <span data-ttu-id="c0eb6-171">Si no se llama a este método **AddRef** , MAPI descargará su proveedor.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-171">If you do not call this **AddRef** method, MAPI will unload your provider.</span></span> 
  
<span data-ttu-id="c0eb6-172">Puede incluir el nombre de perfil que se pasa en el parámetro _lpszProfileName_ en otras interfaces de usuario, pantallas de inicio de sesión o cuadros de diálogo de error.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-172">You can include the profile name passed in the  _lpszProfileName_ parameter in error dialog boxes, logon screens, or other user interfaces.</span></span> <span data-ttu-id="c0eb6-173">Para usar el nombre del perfil, cópielo en el almacenamiento que haya asignado.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-173">To use the profile name, copy it to storage that you have allocated.</span></span> 
  
<span data-ttu-id="c0eb6-174">Crear un objeto de inicio de sesión y devolver un puntero a ella en el parámetro _lppABLogon_ .</span><span class="sxs-lookup"><span data-stu-id="c0eb6-174">Create a logon object and return a pointer to it in the  _lppABLogon_ parameter.</span></span> <span data-ttu-id="c0eb6-175">MAPI utiliza este objeto de inicio de sesión para realizar llamadas a los métodos en su implementación [IABLogon](iablogoniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="c0eb6-175">MAPI uses this logon object to make calls to the methods in your [IABLogon](iablogoniunknown.md) implementation.</span></span> 
  
<span data-ttu-id="c0eb6-176">Si necesita una contraseña durante el inicio de sesión, mostrar un cuadro de diálogo de inicio de sesión sólo si no se establece la marca AB_NO_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-176">If you require a password during logon, display a logon dialog box only if the AB_NO_DIALOG flag is not set.</span></span> <span data-ttu-id="c0eb6-177">Si el usuario cancela el proceso de inicio de sesión, normalmente haciendo clic en el botón **Cancelar** en el cuadro de diálogo devolver MAPI_E_USER_CANCEL de **Inicio de sesión**.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-177">If the user cancels the logon process, typically by clicking the **Cancel** button in the dialog box, return MAPI_E_USER_CANCEL from **Logon**.</span></span>
  
<span data-ttu-id="c0eb6-178">Normalmente, cuando un proveedor de la libreta de direcciones no puede iniciar sesión, MAPI deshabilita el servicio de mensajes a la que pertenece el proveedor con errores, es decir, MAPI no intentará establecer conexiones para cualquiera de los otros proveedores que pertenecen al servicio para el resto de la sesión período de duración.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-178">Typically, when an address book provider cannot log on, MAPI disables the message service to which the failing provider belongs—that is, MAPI will not try to establish connections for any of the other providers that belong to the service for the rest of the session's lifetime.</span></span> <span data-ttu-id="c0eb6-179">Sin embargo, si el proveedor no puede establecer una conexión y no desea deshabilitar todo el servicio, devolver MAPI_E_FAILONEPROVIDER o MAPI_E_UNCONFIGURED.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-179">However, if your provider cannot establish a connection and you want not to disable the entire service, return either MAPI_E_FAILONEPROVIDER or MAPI_E_UNCONFIGURED.</span></span> <span data-ttu-id="c0eb6-180">MAPI no deshabilita el servicio de mensajes a la que pertenece el proveedor.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-180">MAPI will not disable the message service to which the provider belongs.</span></span> 
  
<span data-ttu-id="c0eb6-181">Retorno MAPI_E_FAILONEPROVIDER si produce un error no es lo suficientemente grave como para impedir que los otros proveedores en el servicio de mensajes establecer conexiones.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-181">Return MAPI_E_FAILONEPROVIDER if an error occurs that is not serious enough to prevent the other providers in the message service from establishing connections.</span></span> <span data-ttu-id="c0eb6-182">Devolver MAPI_E_UNCONFIGURED si falta la información de configuración necesaria desde el perfil y no se puede mostrar un cuadro de diálogo para preguntar al usuario.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-182">Return MAPI_E_UNCONFIGURED if the necessary configuration information is missing from the profile and you cannot display a dialog box to prompt the user.</span></span> <span data-ttu-id="c0eb6-183">MAPI responderá al llamar a la función de punto de entrada de servicio del su proveedor mensaje con MSG_SERVICE_CONFIGURE establecido como el parámetro _ulContext_ para proporcionar el servicio de una oportunidad para configurarse a sí mismo, ya sea mediante programación o mediante una hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-183">MAPI will respond by calling your provider's message service entry point function with MSG_SERVICE_CONFIGURE set as the  _ulContext_ parameter to give the service a chance to configure itself, either programmatically or using a property sheet.</span></span> <span data-ttu-id="c0eb6-184">Cuando elija la entrada de mensajes de servicio finalizado (función), el inicio de sesión de reintentos de MAPI.</span><span class="sxs-lookup"><span data-stu-id="c0eb6-184">When the message service entry point function has finished, MAPI retries the logon.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c0eb6-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0eb6-185">See also</span></span>



[<span data-ttu-id="c0eb6-186">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="c0eb6-186">IABLogon::Logoff</span></span>](iablogon-logoff.md)
  
[<span data-ttu-id="c0eb6-187">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="c0eb6-187">IABLogon::OpenEntry</span></span>](iablogon-openentry.md)
  
[<span data-ttu-id="c0eb6-188">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="c0eb6-188">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)
  
[<span data-ttu-id="c0eb6-189">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="c0eb6-189">IMAPISupport::SetProviderUID</span></span>](imapisupport-setprovideruid.md)
  
[<span data-ttu-id="c0eb6-190">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="c0eb6-190">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="c0eb6-191">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c0eb6-191">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

