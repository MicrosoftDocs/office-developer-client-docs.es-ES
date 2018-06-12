---
title: MAPILogonEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPILogonEx
api_type:
- HeaderDef
ms.assetid: 98091e5b-1abd-4814-9c7a-583b420ee11d
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 08782fe616fe260388cff8982dfbb09951453a00
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818247"
---
# <a name="mapilogonex"></a><span data-ttu-id="b1288-103">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="b1288-103">MAPILogonEx</span></span>

  
  
<span data-ttu-id="b1288-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b1288-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b1288-105">Los registros de una aplicación cliente de sesión en una sesión con el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="b1288-105">Logs a client application on to a session with the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b1288-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b1288-106">Header file:</span></span>  <br/> |<span data-ttu-id="b1288-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="b1288-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="b1288-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="b1288-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b1288-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b1288-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b1288-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="b1288-110">Called by:</span></span>  <br/> |<span data-ttu-id="b1288-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="b1288-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPILogonEx(
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  FLAGS flFlags,
  LPMAPISESSION FAR * lppSession
);
```

## <a name="parameters"></a><span data-ttu-id="b1288-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1288-112">Parameters</span></span>

 <span data-ttu-id="b1288-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b1288-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="b1288-114">[entrada] Identificador de la ventana a la que el cuadro de diálogo de inicio de sesión es modal.</span><span class="sxs-lookup"><span data-stu-id="b1288-114">[in] Handle to the window to which the logon dialog box is modal.</span></span> <span data-ttu-id="b1288-115">Si no aparece ningún cuadro de diálogo durante la llamada, se omite el parámetro _ulUIParam_ .</span><span class="sxs-lookup"><span data-stu-id="b1288-115">If no dialog box appears during the call, the  _ulUIParam_ parameter is ignored.</span></span> <span data-ttu-id="b1288-116">Este parámetro puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="b1288-116">This parameter can be zero.</span></span> 
    
 <span data-ttu-id="b1288-117">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="b1288-117">_lpszProfileName_</span></span>
  
> <span data-ttu-id="b1288-118">[entrada] Puntero a una cadena que contiene el nombre del perfil que desea usar cuando el usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="b1288-118">[in] Pointer to a string that contains the name of the profile to use when the user logs on.</span></span> <span data-ttu-id="b1288-119">Esta cadena está limitada a 64 caracteres.</span><span class="sxs-lookup"><span data-stu-id="b1288-119">This string is limited to 64 characters.</span></span>
    
 <span data-ttu-id="b1288-120">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="b1288-120">_lpszPassword_</span></span>
  
> <span data-ttu-id="b1288-121">[entrada] Puntero a una cadena que contiene la contraseña del perfil.</span><span class="sxs-lookup"><span data-stu-id="b1288-121">[in] Pointer to a string that contains the password of the profile.</span></span> <span data-ttu-id="b1288-122">El parámetro _lpszPassword_ debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="b1288-122">The  _lpszPassword_ parameter must be NULL.</span></span> 
    
 <span data-ttu-id="b1288-123">_flFlags_</span><span class="sxs-lookup"><span data-stu-id="b1288-123">_flFlags_</span></span>
  
> <span data-ttu-id="b1288-124">[entrada] Máscara de bits de indicadores que se utilizan para controlar cómo se realiza el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="b1288-124">[in] Bitmask of flags used to control how logon is performed.</span></span> <span data-ttu-id="b1288-125">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="b1288-125">The following flags can be set:</span></span>
    
<span data-ttu-id="b1288-126">MAPI_ALLOW_OTHERS</span><span class="sxs-lookup"><span data-stu-id="b1288-126">MAPI_ALLOW_OTHERS</span></span> 
  
> <span data-ttu-id="b1288-127">Debe devolverse la sesión compartida, lo que permite a los clientes posteriores para obtener la sesión sin tener que proporcionar las credenciales de usuario.</span><span class="sxs-lookup"><span data-stu-id="b1288-127">The shared session should be returned, which allows later clients to obtain the session without providing any user credentials.</span></span> 
    
<span data-ttu-id="b1288-128">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="b1288-128">MAPI_BG_SESSION</span></span>
  
> <span data-ttu-id="b1288-129">Inicie sesión en una sesión y ejecutar las operaciones en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="b1288-129">Log on to a session and run any operations in the background.</span></span> <span data-ttu-id="b1288-130">En general, si un cliente se va a realizar el procesamiento en un subproceso de fondo o en un proceso independiente de manera que sea discreto al subproceso de primer plano, debe llamar con el indicador MAPI_BG_SESSION.</span><span class="sxs-lookup"><span data-stu-id="b1288-130">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call with the MAPI_BG_SESSION flag.</span></span> <span data-ttu-id="b1288-131">Una aplicación cliente como un motor de indización o abrir un archivo de carpetas personales (PST) para el acceso de tipo de fondo son algunos ejemplos que se va a usar MAPI_BG_SESSION. MAPILogonEx.</span><span class="sxs-lookup"><span data-stu-id="b1288-131">A client application such as an indexing engine or opening a Personal Folders File (PST) for background type access are some examples of where to use MAPI_BG_SESSION.MAPILogonEx.</span></span>
    
<span data-ttu-id="b1288-132">MAPI_EXPLICIT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="b1288-132">MAPI_EXPLICIT_PROFILE</span></span> 
  
> <span data-ttu-id="b1288-133">No se debe usar el perfil predeterminado y el usuario debe ser necesarios para proporcionar un perfil.</span><span class="sxs-lookup"><span data-stu-id="b1288-133">The default profile should not be used and the user should be required to supply a profile.</span></span> 
    
<span data-ttu-id="b1288-134">MAPI_EXTENDED</span><span class="sxs-lookup"><span data-stu-id="b1288-134">MAPI_EXTENDED</span></span> 
  
> <span data-ttu-id="b1288-135">Inicie sesión con capacidades extendidas.</span><span class="sxs-lookup"><span data-stu-id="b1288-135">Log on with extended capabilities.</span></span> <span data-ttu-id="b1288-136">Siempre se debe establecer este indicador.</span><span class="sxs-lookup"><span data-stu-id="b1288-136">This flag should always be set.</span></span>
    
<span data-ttu-id="b1288-137">MAPI_FORCE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="b1288-137">MAPI_FORCE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="b1288-138">Se debe realizar un intento descargar todos los mensajes del usuario antes de devolverlo.</span><span class="sxs-lookup"><span data-stu-id="b1288-138">An attempt should be made to download all of the user's messages before returning.</span></span> <span data-ttu-id="b1288-139">Si no está establecido el indicador MAPI_FORCE_DOWNLOAD, se pueden descargar los mensajes en segundo plano después de la llamada a MAPILogonEx devuelve.</span><span class="sxs-lookup"><span data-stu-id="b1288-139">If the MAPI_FORCE_DOWNLOAD flag is not set, messages can be downloaded in the background after the call to MAPILogonEx returns.</span></span> 
    
<span data-ttu-id="b1288-140">MAPI_LOGON_UI</span><span class="sxs-lookup"><span data-stu-id="b1288-140">MAPI_LOGON_UI</span></span> 
  
> <span data-ttu-id="b1288-141">Debe mostrarse un cuadro de diálogo para preguntar al usuario para obtener información de inicio de sesión si es necesario.</span><span class="sxs-lookup"><span data-stu-id="b1288-141">A dialog box should be displayed to prompt the user for logon information if required.</span></span> <span data-ttu-id="b1288-142">Cuando no está establecido el indicador MAPI_LOGON_UI, el cliente de la llamada no muestra un cuadro de diálogo de inicio de sesión y devuelve un valor de error si el usuario no ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="b1288-142">When the MAPI_LOGON_UI flag is not set, the calling client does not display a logon dialog box and returns an error value if the user is not logged on.</span></span>
    
<span data-ttu-id="b1288-143">MAPI_NEW_SESSION</span><span class="sxs-lookup"><span data-stu-id="b1288-143">MAPI_NEW_SESSION</span></span> 
  
> <span data-ttu-id="b1288-144">Para crear una nueva sesión MAPI en lugar de adquisición de la sesión compartida, se debe realizar un intento.</span><span class="sxs-lookup"><span data-stu-id="b1288-144">An attempt should be made to create a new MAPI session instead of acquiring the shared session.</span></span> <span data-ttu-id="b1288-145">Si no está establecido el indicador MAPI_NEW_SESSION, MAPILogonEx usa una sesión compartida existente, incluso si el parámetro _lpszprofileName_ no es nulo.</span><span class="sxs-lookup"><span data-stu-id="b1288-145">If the MAPI_NEW_SESSION flag is not set, MAPILogonEx uses an existing shared session even if the  _lpszprofileName_ parameter is not NULL.</span></span> 
    
<span data-ttu-id="b1288-146">MAPI_NO_MAIL</span><span class="sxs-lookup"><span data-stu-id="b1288-146">MAPI_NO_MAIL</span></span> 
  
> <span data-ttu-id="b1288-147">MAPI no debe informar a la cola MAPI de la existencia de la sesión.</span><span class="sxs-lookup"><span data-stu-id="b1288-147">MAPI should not inform the MAPI spooler of the session's existence.</span></span> <span data-ttu-id="b1288-148">El resultado es que no hay mensajes pueden ser enviados o recibidos en la sesión excepto a través de un acoplado almacenar y par de transporte.</span><span class="sxs-lookup"><span data-stu-id="b1288-148">The result is that no messages can be sent or received in the session except through a tightly coupled store and transport pair.</span></span> <span data-ttu-id="b1288-149">Un cliente de la llamada establece esta marca si actúa como un agente, si el trabajo de configuración debe llevarse a cabo, o si el cliente está explorando los almacenes de mensajes disponibles.</span><span class="sxs-lookup"><span data-stu-id="b1288-149">A calling client sets this flag if it is acting as an agent, if configuration work must be done, or if the client is browsing the available message stores.</span></span> 
    
<span data-ttu-id="b1288-150">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="b1288-150">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="b1288-151">El autor de la llamada se ejecuta como un servicio de Windows.</span><span class="sxs-lookup"><span data-stu-id="b1288-151">The caller is running as a Windows service.</span></span> <span data-ttu-id="b1288-152">Autores de llamadas que no se ejecutan como un servicio de Windows no debe establecer esta marca; autores de llamadas que se ejecutan como un servicio debe establecer este indicador.</span><span class="sxs-lookup"><span data-stu-id="b1288-152">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span> 
    
<span data-ttu-id="b1288-153">MAPI_SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="b1288-153">MAPI_SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="b1288-154">MAPILogonEx debe mostrar un cuadro de diálogo de configuración para cada servicio de mensajes en el perfil.</span><span class="sxs-lookup"><span data-stu-id="b1288-154">MAPILogonEx should display a configuration dialog box for each message service in the profile.</span></span> <span data-ttu-id="b1288-155">Una vez que se ha seleccionado el perfil, pero antes de cualquier mensaje de servicio se registra, se muestran los cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b1288-155">The dialog boxes are displayed after the profile has been chosen but before any message service is logged on.</span></span> <span data-ttu-id="b1288-156">El cuadro de diálogo comunes de MAPI para el inicio de sesión también contiene una casilla de verificación que solicita la misma operación.</span><span class="sxs-lookup"><span data-stu-id="b1288-156">The MAPI common dialog box for logon also contains a check box that requests the same operation.</span></span> 
    
<span data-ttu-id="b1288-157">MAPI_TIMEOUT_SHORT</span><span class="sxs-lookup"><span data-stu-id="b1288-157">MAPI_TIMEOUT_SHORT</span></span> 
  
> <span data-ttu-id="b1288-158">El inicio de sesión debe producirá un error si bloqueado durante más de unos segundos.</span><span class="sxs-lookup"><span data-stu-id="b1288-158">The logon should fail if blocked for more than a few seconds.</span></span> 
    
<span data-ttu-id="b1288-159">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="b1288-159">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b1288-160">Las cadenas que se pasan en están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="b1288-160">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="b1288-161">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="b1288-161">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="b1288-162">MAPI_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="b1288-162">MAPI_USE_DEFAULT</span></span> 
  
> <span data-ttu-id="b1288-163">El subsistema de mensajería debe sustituir el nombre del perfil del perfil predeterminado para el parámetro _lpszProfileName_ .</span><span class="sxs-lookup"><span data-stu-id="b1288-163">The messaging subsystem should substitute the profile name of the default profile for the  _lpszProfileName_ parameter.</span></span> <span data-ttu-id="b1288-164">El indicador MAPI_EXPLICIT_PROFILE se omite a menos que _lpszProfileName_ es NULL o está vacío.</span><span class="sxs-lookup"><span data-stu-id="b1288-164">The MAPI_EXPLICIT_PROFILE flag is ignored unless  _lpszProfileName_ is NULL or empty.</span></span> 
    
 <span data-ttu-id="b1288-165">_lppSession_</span><span class="sxs-lookup"><span data-stu-id="b1288-165">_lppSession_</span></span>
  
> <span data-ttu-id="b1288-166">[out] Puntero a un puntero a la interfaz de sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="b1288-166">[out] Pointer to a pointer to the MAPI session interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b1288-167">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1288-167">Return value</span></span>

<span data-ttu-id="b1288-168">S_OK</span><span class="sxs-lookup"><span data-stu-id="b1288-168">S_OK</span></span> 
  
> <span data-ttu-id="b1288-169">El inicio de sesión se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b1288-169">The logon succeeded.</span></span>
    
<span data-ttu-id="b1288-170">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="b1288-170">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="b1288-171">El inicio de sesión era incorrecta, porque uno o varios de los parámetros a MAPILogonEx no eran válidos o porque ya había demasiadas sesiones abiertas.</span><span class="sxs-lookup"><span data-stu-id="b1288-171">The logon was unsuccessful, either because one or more of the parameters to MAPILogonEx were invalid or because there were too many sessions open already.</span></span>
    
<span data-ttu-id="b1288-172">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b1288-172">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="b1288-173">MAPI serializa todos los inicios de sesión a través de una exclusión mutua.</span><span class="sxs-lookup"><span data-stu-id="b1288-173">MAPI serializes all logons through a mutex.</span></span> <span data-ttu-id="b1288-174">Esto se devuelve si se ha establecido el indicador MAPI_TIMEOUT_SHORT y otro subproceso conserva la exclusión mutua.</span><span class="sxs-lookup"><span data-stu-id="b1288-174">This is returned if the MAPI_TIMEOUT_SHORT flag was set and another thread held the mutex.</span></span> 
    
<span data-ttu-id="b1288-175">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="b1288-175">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="b1288-176">El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b1288-176">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b1288-177">Notas</span><span class="sxs-lookup"><span data-stu-id="b1288-177">Remarks</span></span>

<span data-ttu-id="b1288-178">Las aplicaciones cliente MAPI llaman a la función MAPILogonEx para iniciar sesión en una sesión con el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="b1288-178">MAPI client applications call the MAPILogonEx function to log on to a session with the messaging system.</span></span> <span data-ttu-id="b1288-179">Todas las cadenas que se pasan en y son devueltas a y desde las llamadas MAPI están terminada en null y deben especificarse en el juego de caracteres actual o de código de página del sistema operativo cliente o del proveedor de llamada.</span><span class="sxs-lookup"><span data-stu-id="b1288-179">All strings that are passed in and returned to and from MAPI calls are null-terminated and must be specified in the current character set or code page of the calling client or provider's operating system.</span></span>
  
<span data-ttu-id="b1288-180">Si hay una sesión anterior existente que se llama a MapiLogonEx con el conjunto de marca MAPI_ALLOW_OTHERS y si la marca MAPI_NEW_SESSION no está establecida, se omite el parámetro _lpszProfileName_ .</span><span class="sxs-lookup"><span data-stu-id="b1288-180">The  _lpszProfileName_ parameter is ignored if there is an existing previous session that called MapiLogonEx with the MAPI_ALLOW_OTHERS flag set and if the flag MAPI_NEW_SESSION is not set.</span></span> <span data-ttu-id="b1288-181">Si el parámetro _lpszProfileName_ es NULL o apunta a una cadena vacía y el parámetro _flFlags_ incluye el indicador MAPI_LOGON_UI, la función MAPILogonEx genera un cuadro de diálogo de inicio de sesión que tiene un campo vacío para el nombre del perfil.</span><span class="sxs-lookup"><span data-stu-id="b1288-181">If the  _lpszProfileName_ parameter is NULL or points to an empty string, and the  _flFlags_ parameter includes the MAPI_LOGON_UI flag, the MAPILogonEx function generates a logon dialog box that has an empty field for the profile name.</span></span> 
  
<span data-ttu-id="b1288-182">Al iniciar sesión en un perfil específico, un cliente debe pasar la marca MAPI_NEW_SESSION a MAPILogonEx además del nombre de perfil.</span><span class="sxs-lookup"><span data-stu-id="b1288-182">When logging on to a specific profile, a client should pass the MAPI_NEW_SESSION flag into MAPILogonEx in addition to the profile name.</span></span> <span data-ttu-id="b1288-183">De lo contrario, si otro cliente ha establecido una sesión compartida por inicio de sesión con MAPI_ALLOW_OTHERS, el cliente se registrará a la sesión compartida en lugar de hacerlo en el perfil solicitada.</span><span class="sxs-lookup"><span data-stu-id="b1288-183">Otherwise, if another client has established a shared session by logging on with MAPI_ALLOW_OTHERS, the client will be logged on to the shared session instead of to the profile requested.</span></span> 
  
<span data-ttu-id="b1288-184">El indicador MAPI_EXPLICIT_PROFILE no hace que el nombre de perfil predeterminado que se utilizará cuando _lpszProfileName_ es NULL o vacío a menos que el indicador MAPI_USE_DEFAULT también está presente.</span><span class="sxs-lookup"><span data-stu-id="b1288-184">The MAPI_EXPLICIT_PROFILE flag does not cause the default profile name to be used when  _lpszProfileName_ is NULL or empty unless the MAPI_USE_DEFAULT flag is also present.</span></span> 
  
<span data-ttu-id="b1288-185">El indicador MAPI_NO_MAIL tiene varios efectos que hacen lo siguiente cuando no se utiliza a la cola MAPI:</span><span class="sxs-lookup"><span data-stu-id="b1288-185">The MAPI_NO_MAIL flag has several effects that cause the following when not using the MAPI spooler:</span></span>
  
- <span data-ttu-id="b1288-186">Puede enviar ningún mensaje o emitido por la cola MAPI durante esta sesión.</span><span class="sxs-lookup"><span data-stu-id="b1288-186">No messages can be sent or delivered by the MAPI spooler during this session.</span></span> <span data-ttu-id="b1288-187">Sólo los proveedores de almacén y transporte acoplados pueden enviar y entregar mensajes.</span><span class="sxs-lookup"><span data-stu-id="b1288-187">Only tightly coupled store and transport providers can send and deliver messages.</span></span> 
    
- <span data-ttu-id="b1288-188">Almacenes en función de servidor aún es posible que enviar o entregar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="b1288-188">Server based stores might still send or deliver messages.</span></span> 
    
- <span data-ttu-id="b1288-189">No se procesan los mensajes enviados o entregados por almacenes en función de servidor por todos los proveedores de enlace.</span><span class="sxs-lookup"><span data-stu-id="b1288-189">Messages sent or delivered by server based stores are not processed by any hook providers.</span></span> 
    
- <span data-ttu-id="b1288-190">Opciones de cada mensaje y por destinatario para los transportes no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="b1288-190">Per-message and per-recipient options for transports are not available.</span></span> 
    
- <span data-ttu-id="b1288-191">La tabla de estado no contiene entradas para los proveedores de transporte y cualquier funcionalidad de transporte dependientes en objetos de estado (por ejemplo, configuración) no está disponible.</span><span class="sxs-lookup"><span data-stu-id="b1288-191">The status table does not contain entries for transport providers, and any transport functionality dependent on status objects (such as configuration) is not available.</span></span> 
    
- <span data-ttu-id="b1288-192">La fila de la cola de mensajes en la tabla de estado contiene el valor STATUS_FAILURE.</span><span class="sxs-lookup"><span data-stu-id="b1288-192">The message spooler row in the status table contains the STATUS_FAILURE value.</span></span> 
    
- <span data-ttu-id="b1288-193">Se permiten los inicios de sesión superpuestos, pero los inicios de sesión no hacen que el inicio de sesión anterior recibir actualizaciones de objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="b1288-193">Piggybacked logons are allowed, but those logons do not cause the previous logon to receive status object updates.</span></span> 
    
<span data-ttu-id="b1288-194">Un servicio siempre debe iniciar sesión con la marca MAPI_NO_MAIL.</span><span class="sxs-lookup"><span data-stu-id="b1288-194">A service should always log on using the MAPI_NO_MAIL flag.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b1288-195">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b1288-195">MFCMAPI reference</span></span>

<span data-ttu-id="b1288-196">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="b1288-196">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b1288-197">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="b1288-197">**File**</span></span>|<span data-ttu-id="b1288-198">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="b1288-198">**Function**</span></span>|<span data-ttu-id="b1288-199">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="b1288-199">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b1288-200">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="b1288-200">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="b1288-201">CMapiObjects::MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="b1288-201">CMapiObjects::MAPILogonEx</span></span>  <br/> |<span data-ttu-id="b1288-202">MFCMAPI usa el método MAPILogonEx para iniciar sesión en MAPI.</span><span class="sxs-lookup"><span data-stu-id="b1288-202">MFCMAPI uses the MAPILogonEx method to log on to MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b1288-203">Ver también</span><span class="sxs-lookup"><span data-stu-id="b1288-203">See also</span></span>



[<span data-ttu-id="b1288-204">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="b1288-204">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="b1288-205">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="b1288-205">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="b1288-206">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="b1288-206">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

