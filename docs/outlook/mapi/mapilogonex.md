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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9f2ec8f0ec00f7314982e9b112415f69901c358c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424122"
---
# <a name="mapilogonex"></a><span data-ttu-id="ef929-103">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="ef929-103">MAPILogonEx</span></span>

  
  
<span data-ttu-id="ef929-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef929-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef929-105">Registra una aplicación cliente en una sesión con el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="ef929-105">Logs a client application on to a session with the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ef929-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="ef929-106">Header file:</span></span>  <br/> |<span data-ttu-id="ef929-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="ef929-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="ef929-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="ef929-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ef929-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ef929-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ef929-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="ef929-110">Called by:</span></span>  <br/> |<span data-ttu-id="ef929-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="ef929-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPILogonEx(
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  FLAGS flFlags,
  LPMAPISESSION FAR * lppSession
);
```

## <a name="parameters"></a><span data-ttu-id="ef929-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="ef929-112">Parameters</span></span>

 <span data-ttu-id="ef929-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ef929-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="ef929-114">[in] Controla la ventana en la que el cuadro de diálogo de inicio de sesión es modal.</span><span class="sxs-lookup"><span data-stu-id="ef929-114">[in] Handle to the window to which the logon dialog box is modal.</span></span> <span data-ttu-id="ef929-115">Si no aparece ningún cuadro de diálogo durante la llamada, se omite el parámetro _ulUIParam._</span><span class="sxs-lookup"><span data-stu-id="ef929-115">If no dialog box appears during the call, the  _ulUIParam_ parameter is ignored.</span></span> <span data-ttu-id="ef929-116">Este parámetro puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="ef929-116">This parameter can be zero.</span></span> 
    
 <span data-ttu-id="ef929-117">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="ef929-117">_lpszProfileName_</span></span>
  
> <span data-ttu-id="ef929-118">[in] Puntero a una cadena que contiene el nombre del perfil que se usará cuando el usuario inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="ef929-118">[in] Pointer to a string that contains the name of the profile to use when the user logs on.</span></span> <span data-ttu-id="ef929-119">Esta cadena está limitada a 64 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ef929-119">This string is limited to 64 characters.</span></span>
    
 <span data-ttu-id="ef929-120">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="ef929-120">_lpszPassword_</span></span>
  
> <span data-ttu-id="ef929-121">[in] Puntero a una cadena que contiene la contraseña del perfil.</span><span class="sxs-lookup"><span data-stu-id="ef929-121">[in] Pointer to a string that contains the password of the profile.</span></span> <span data-ttu-id="ef929-122">El  _parámetro lpszPassword_ debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="ef929-122">The  _lpszPassword_ parameter must be NULL.</span></span> 
    
 <span data-ttu-id="ef929-123">_flFlags_</span><span class="sxs-lookup"><span data-stu-id="ef929-123">_flFlags_</span></span>
  
> <span data-ttu-id="ef929-124">[in] Máscara de bits de las marcas que se usan para controlar cómo se realiza el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="ef929-124">[in] Bitmask of flags used to control how logon is performed.</span></span> <span data-ttu-id="ef929-125">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="ef929-125">The following flags can be set:</span></span>
    
<span data-ttu-id="ef929-126">MAPI_ALLOW_OTHERS</span><span class="sxs-lookup"><span data-stu-id="ef929-126">MAPI_ALLOW_OTHERS</span></span> 
  
> <span data-ttu-id="ef929-127">Se debe devolver la sesión compartida, lo que permite a los clientes posteriores obtener la sesión sin proporcionar credenciales de usuario.</span><span class="sxs-lookup"><span data-stu-id="ef929-127">The shared session should be returned, which allows later clients to obtain the session without providing any user credentials.</span></span> 
    
<span data-ttu-id="ef929-128">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="ef929-128">MAPI_BG_SESSION</span></span>
  
> <span data-ttu-id="ef929-129">Inicie sesión en una sesión y ejecute cualquier operación en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="ef929-129">Log on to a session and run any operations in the background.</span></span> <span data-ttu-id="ef929-130">En general, si un cliente tiene la intención de realizar el procesamiento en un subproceso en segundo plano o en un proceso independiente de una manera discreta para el subproceso en primer plano, debe llamar con la marca MAPI_BG_SESSION.</span><span class="sxs-lookup"><span data-stu-id="ef929-130">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call with the MAPI_BG_SESSION flag.</span></span> <span data-ttu-id="ef929-131">Una aplicación cliente como un motor de indización o abrir un archivo de carpetas personales (PST) para el acceso de tipo en segundo plano son algunos ejemplos de dónde usar MAPI_BG_SESSION. MAPILogonEx.</span><span class="sxs-lookup"><span data-stu-id="ef929-131">A client application such as an indexing engine or opening a Personal Folders File (PST) for background type access are some examples of where to use MAPI_BG_SESSION.MAPILogonEx.</span></span>
    
<span data-ttu-id="ef929-132">MAPI_EXPLICIT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="ef929-132">MAPI_EXPLICIT_PROFILE</span></span> 
  
> <span data-ttu-id="ef929-133">El perfil predeterminado no debe usarse y el usuario debe ser necesario para proporcionar un perfil.</span><span class="sxs-lookup"><span data-stu-id="ef929-133">The default profile should not be used and the user should be required to supply a profile.</span></span> 
    
<span data-ttu-id="ef929-134">MAPI_EXTENDED</span><span class="sxs-lookup"><span data-stu-id="ef929-134">MAPI_EXTENDED</span></span> 
  
> <span data-ttu-id="ef929-135">Inicie sesión con funcionalidades extendidas.</span><span class="sxs-lookup"><span data-stu-id="ef929-135">Log on with extended capabilities.</span></span> <span data-ttu-id="ef929-136">Esta marca siempre debe establecerse.</span><span class="sxs-lookup"><span data-stu-id="ef929-136">This flag should always be set.</span></span>
    
<span data-ttu-id="ef929-137">MAPI_FORCE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="ef929-137">MAPI_FORCE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="ef929-138">Se debe intentar descargar todos los mensajes del usuario antes de devolverlos.</span><span class="sxs-lookup"><span data-stu-id="ef929-138">An attempt should be made to download all of the user's messages before returning.</span></span> <span data-ttu-id="ef929-139">Si no MAPI_FORCE_DOWNLOAD marca, los mensajes se pueden descargar en segundo plano después de que la llamada a MAPILogonEx devuelva.</span><span class="sxs-lookup"><span data-stu-id="ef929-139">If the MAPI_FORCE_DOWNLOAD flag is not set, messages can be downloaded in the background after the call to MAPILogonEx returns.</span></span> 
    
<span data-ttu-id="ef929-140">MAPI_LOGON_UI</span><span class="sxs-lookup"><span data-stu-id="ef929-140">MAPI_LOGON_UI</span></span> 
  
> <span data-ttu-id="ef929-141">Si es necesario, se debe mostrar un cuadro de diálogo para solicitar al usuario información de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="ef929-141">A dialog box should be displayed to prompt the user for logon information if required.</span></span> <span data-ttu-id="ef929-142">Cuando no MAPI_LOGON_UI marca de inicio de sesión, el cliente que llama no muestra un cuadro de diálogo de inicio de sesión y devuelve un valor de error si el usuario no ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="ef929-142">When the MAPI_LOGON_UI flag is not set, the calling client does not display a logon dialog box and returns an error value if the user is not logged on.</span></span>
    
<span data-ttu-id="ef929-143">MAPI_NEW_SESSION</span><span class="sxs-lookup"><span data-stu-id="ef929-143">MAPI_NEW_SESSION</span></span> 
  
> <span data-ttu-id="ef929-144">Se debe intentar crear una nueva sesión MAPI en lugar de adquirir la sesión compartida.</span><span class="sxs-lookup"><span data-stu-id="ef929-144">An attempt should be made to create a new MAPI session instead of acquiring the shared session.</span></span> <span data-ttu-id="ef929-145">Si no MAPI_NEW_SESSION marca, MAPILogonEx usa una sesión compartida existente incluso si el parámetro  _lpszprofileName_ no es NULL.</span><span class="sxs-lookup"><span data-stu-id="ef929-145">If the MAPI_NEW_SESSION flag is not set, MAPILogonEx uses an existing shared session even if the  _lpszprofileName_ parameter is not NULL.</span></span> 
    
<span data-ttu-id="ef929-146">MAPI_NO_MAIL</span><span class="sxs-lookup"><span data-stu-id="ef929-146">MAPI_NO_MAIL</span></span> 
  
> <span data-ttu-id="ef929-147">MAPI no debe informar a la cola MAPI de la existencia de la sesión.</span><span class="sxs-lookup"><span data-stu-id="ef929-147">MAPI should not inform the MAPI spooler of the session's existence.</span></span> <span data-ttu-id="ef929-148">El resultado es que no se pueden enviar ni recibir mensajes en la sesión excepto a través de un par de almacenamiento y transporte estrechamente acoplados.</span><span class="sxs-lookup"><span data-stu-id="ef929-148">The result is that no messages can be sent or received in the session except through a tightly coupled store and transport pair.</span></span> <span data-ttu-id="ef929-149">Un cliente que llama establece esta marca si actúa como agente, si se debe realizar el trabajo de configuración o si el cliente está explorando los almacenes de mensajes disponibles.</span><span class="sxs-lookup"><span data-stu-id="ef929-149">A calling client sets this flag if it is acting as an agent, if configuration work must be done, or if the client is browsing the available message stores.</span></span> 
    
<span data-ttu-id="ef929-150">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="ef929-150">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="ef929-151">El autor de la llamada se ejecuta como Windows servicio.</span><span class="sxs-lookup"><span data-stu-id="ef929-151">The caller is running as a Windows service.</span></span> <span data-ttu-id="ef929-152">Los autores de llamadas que no se ejecutan como servicio Windows no deben establecer esta marca; Los autores de llamadas que se ejecutan como servicio deben establecer esta marca.</span><span class="sxs-lookup"><span data-stu-id="ef929-152">Callers that are not running as a Windows service should not set this flag; callers that are running as a service must set this flag.</span></span> 
    
<span data-ttu-id="ef929-153">MAPI_SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="ef929-153">MAPI_SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="ef929-154">MAPILogonEx debe mostrar un cuadro de diálogo de configuración para cada servicio de mensajes del perfil.</span><span class="sxs-lookup"><span data-stu-id="ef929-154">MAPILogonEx should display a configuration dialog box for each message service in the profile.</span></span> <span data-ttu-id="ef929-155">Los cuadros de diálogo se muestran después de elegir el perfil, pero antes de iniciar sesión en cualquier servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ef929-155">The dialog boxes are displayed after the profile has been chosen but before any message service is logged on.</span></span> <span data-ttu-id="ef929-156">El cuadro de diálogo común MAPI para el inicio de sesión también contiene una casilla que solicita la misma operación.</span><span class="sxs-lookup"><span data-stu-id="ef929-156">The MAPI common dialog box for logon also contains a check box that requests the same operation.</span></span> 
    
<span data-ttu-id="ef929-157">MAPI_TIMEOUT_SHORT</span><span class="sxs-lookup"><span data-stu-id="ef929-157">MAPI_TIMEOUT_SHORT</span></span> 
  
> <span data-ttu-id="ef929-158">El inicio de sesión debe producir un error si se bloquea durante más de unos segundos.</span><span class="sxs-lookup"><span data-stu-id="ef929-158">The logon should fail if blocked for more than a few seconds.</span></span> 
    
<span data-ttu-id="ef929-159">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ef929-159">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ef929-160">Las cadenas pasadas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="ef929-160">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="ef929-161">Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="ef929-161">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="ef929-162">MAPI_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="ef929-162">MAPI_USE_DEFAULT</span></span> 
  
> <span data-ttu-id="ef929-163">El subsistema de mensajería debe sustituir el nombre de perfil del perfil predeterminado para el _parámetro lpszProfileName._</span><span class="sxs-lookup"><span data-stu-id="ef929-163">The messaging subsystem should substitute the profile name of the default profile for the  _lpszProfileName_ parameter.</span></span> <span data-ttu-id="ef929-164">El MAPI_EXPLICIT_PROFILE se omite a menos  _que lpszProfileName_ sea NULL o vacío.</span><span class="sxs-lookup"><span data-stu-id="ef929-164">The MAPI_EXPLICIT_PROFILE flag is ignored unless  _lpszProfileName_ is NULL or empty.</span></span> 
    
 <span data-ttu-id="ef929-165">_lppSession_</span><span class="sxs-lookup"><span data-stu-id="ef929-165">_lppSession_</span></span>
  
> <span data-ttu-id="ef929-166">[salida] Puntero a un puntero a la interfaz de sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="ef929-166">[out] Pointer to a pointer to the MAPI session interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ef929-167">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef929-167">Return value</span></span>

<span data-ttu-id="ef929-168">S_OK</span><span class="sxs-lookup"><span data-stu-id="ef929-168">S_OK</span></span> 
  
> <span data-ttu-id="ef929-169">El inicio de sesión se ha correcto.</span><span class="sxs-lookup"><span data-stu-id="ef929-169">The logon succeeded.</span></span>
    
<span data-ttu-id="ef929-170">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="ef929-170">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="ef929-171">El inicio de sesión no se ha hecho correctamente, ya sea porque uno o varios de los parámetros de MAPILogonEx no eran válidos o porque ya había demasiadas sesiones abiertas.</span><span class="sxs-lookup"><span data-stu-id="ef929-171">The logon was unsuccessful, either because one or more of the parameters to MAPILogonEx were invalid or because there were too many sessions open already.</span></span>
    
<span data-ttu-id="ef929-172">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="ef929-172">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="ef929-173">MAPI serializa todos los inicios de sesión a través de un mutex.</span><span class="sxs-lookup"><span data-stu-id="ef929-173">MAPI serializes all logons through a mutex.</span></span> <span data-ttu-id="ef929-174">Esto se devuelve si se MAPI_TIMEOUT_SHORT marca y otro subproceso mantiene la función mutex.</span><span class="sxs-lookup"><span data-stu-id="ef929-174">This is returned if the MAPI_TIMEOUT_SHORT flag was set and another thread held the mutex.</span></span> 
    
<span data-ttu-id="ef929-175">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="ef929-175">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="ef929-176">El usuario canceló la operación, normalmente haciendo clic en el **botón Cancelar** de un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ef929-176">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ef929-177">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ef929-177">Remarks</span></span>

<span data-ttu-id="ef929-178">Las aplicaciones cliente MAPI llaman a la función MAPILogonEx para iniciar sesión en una sesión con el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="ef929-178">MAPI client applications call the MAPILogonEx function to log on to a session with the messaging system.</span></span> <span data-ttu-id="ef929-179">Todas las cadenas que se pasan y devuelven a y desde llamadas MAPI terminan en null y deben especificarse en el conjunto de caracteres actual o en la página de código del sistema operativo del proveedor o cliente de llamadas.</span><span class="sxs-lookup"><span data-stu-id="ef929-179">All strings that are passed in and returned to and from MAPI calls are null-terminated and must be specified in the current character set or code page of the calling client or provider's operating system.</span></span>
  
<span data-ttu-id="ef929-180">El  _parámetro lpszProfileName_ se omite si hay una sesión anterior existente que llamó a MapiLogonEx con el conjunto de marcas MAPI_ALLOW_OTHERS y si no se establece la marca MAPI_NEW_SESSION.</span><span class="sxs-lookup"><span data-stu-id="ef929-180">The  _lpszProfileName_ parameter is ignored if there is an existing previous session that called MapiLogonEx with the MAPI_ALLOW_OTHERS flag set and if the flag MAPI_NEW_SESSION is not set.</span></span> <span data-ttu-id="ef929-181">Si el parámetro  _lpszProfileName_ es NULL o apunta a una cadena vacía y el parámetro  _flFlags_ incluye la marca MAPI_LOGON_UI, la función MAPILogonEx genera un cuadro de diálogo de inicio de sesión que tiene un campo vacío para el nombre del perfil.</span><span class="sxs-lookup"><span data-stu-id="ef929-181">If the  _lpszProfileName_ parameter is NULL or points to an empty string, and the  _flFlags_ parameter includes the MAPI_LOGON_UI flag, the MAPILogonEx function generates a logon dialog box that has an empty field for the profile name.</span></span> 
  
<span data-ttu-id="ef929-182">Al iniciar sesión en un perfil específico, un cliente debe pasar la marca MAPI_NEW_SESSION a MAPILogonEx además del nombre del perfil.</span><span class="sxs-lookup"><span data-stu-id="ef929-182">When logging on to a specific profile, a client should pass the MAPI_NEW_SESSION flag into MAPILogonEx in addition to the profile name.</span></span> <span data-ttu-id="ef929-183">De lo contrario, si otro cliente ha establecido una sesión compartida iniciando sesión con MAPI_ALLOW_OTHERS, el cliente iniciará sesión en la sesión compartida en lugar del perfil solicitado.</span><span class="sxs-lookup"><span data-stu-id="ef929-183">Otherwise, if another client has established a shared session by logging on with MAPI_ALLOW_OTHERS, the client will be logged on to the shared session instead of to the profile requested.</span></span> 
  
<span data-ttu-id="ef929-184">La MAPI_EXPLICIT_PROFILE no hace que se use el nombre de perfil predeterminado cuando  _lpszProfileName_ es NULL o está vacío a menos que la marca MAPI_USE_DEFAULT esté presente.</span><span class="sxs-lookup"><span data-stu-id="ef929-184">The MAPI_EXPLICIT_PROFILE flag does not cause the default profile name to be used when  _lpszProfileName_ is NULL or empty unless the MAPI_USE_DEFAULT flag is also present.</span></span> 
  
<span data-ttu-id="ef929-185">La MAPI_NO_MAIL tiene varios efectos que provocan lo siguiente cuando no se usa la cola MAPI:</span><span class="sxs-lookup"><span data-stu-id="ef929-185">The MAPI_NO_MAIL flag has several effects that cause the following when not using the MAPI spooler:</span></span>
  
- <span data-ttu-id="ef929-186">La cola MAPI no puede enviar ni entregar mensajes durante esta sesión.</span><span class="sxs-lookup"><span data-stu-id="ef929-186">No messages can be sent or delivered by the MAPI spooler during this session.</span></span> <span data-ttu-id="ef929-187">Solo los proveedores de almacenamiento y transporte estrechamente acoplados pueden enviar y entregar mensajes.</span><span class="sxs-lookup"><span data-stu-id="ef929-187">Only tightly coupled store and transport providers can send and deliver messages.</span></span> 
    
- <span data-ttu-id="ef929-188">Es posible que los almacenes basados en el servidor aún envíen o entreguen mensajes.</span><span class="sxs-lookup"><span data-stu-id="ef929-188">Server based stores might still send or deliver messages.</span></span> 
    
- <span data-ttu-id="ef929-189">Los mensajes enviados o entregados por almacenes basados en servidor no son procesados por ningún proveedor de enlaces.</span><span class="sxs-lookup"><span data-stu-id="ef929-189">Messages sent or delivered by server based stores are not processed by any hook providers.</span></span> 
    
- <span data-ttu-id="ef929-190">Las opciones por mensaje y por destinatario para transportes no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="ef929-190">Per-message and per-recipient options for transports are not available.</span></span> 
    
- <span data-ttu-id="ef929-191">La tabla de estado no contiene entradas para proveedores de transporte y ninguna funcionalidad de transporte dependiente de objetos de estado (como la configuración) no está disponible.</span><span class="sxs-lookup"><span data-stu-id="ef929-191">The status table does not contain entries for transport providers, and any transport functionality dependent on status objects (such as configuration) is not available.</span></span> 
    
- <span data-ttu-id="ef929-192">La fila de cola de mensajes de la tabla de estado contiene STATUS_FAILURE valor.</span><span class="sxs-lookup"><span data-stu-id="ef929-192">The message spooler row in the status table contains the STATUS_FAILURE value.</span></span> 
    
- <span data-ttu-id="ef929-193">Se permiten los inicios de sesión con piggybacked, pero esos inicios de sesión no hacen que el inicio de sesión anterior reciba actualizaciones de objetos de estado.</span><span class="sxs-lookup"><span data-stu-id="ef929-193">Piggybacked logons are allowed, but those logons do not cause the previous logon to receive status object updates.</span></span> 
    
<span data-ttu-id="ef929-194">Un servicio siempre debe iniciar sesión con la MAPI_NO_MAIL marca.</span><span class="sxs-lookup"><span data-stu-id="ef929-194">A service should always log on using the MAPI_NO_MAIL flag.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ef929-195">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ef929-195">MFCMAPI reference</span></span>

<span data-ttu-id="ef929-196">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ef929-196">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ef929-197">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="ef929-197">**File**</span></span>|<span data-ttu-id="ef929-198">**Función**</span><span class="sxs-lookup"><span data-stu-id="ef929-198">**Function**</span></span>|<span data-ttu-id="ef929-199">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="ef929-199">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ef929-200">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="ef929-200">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="ef929-201">CMapiObjects::MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="ef929-201">CMapiObjects::MAPILogonEx</span></span>  <br/> |<span data-ttu-id="ef929-202">MFCMAPI usa el método MAPILogonEx para iniciar sesión en MAPI.</span><span class="sxs-lookup"><span data-stu-id="ef929-202">MFCMAPI uses the MAPILogonEx method to log on to MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ef929-203">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef929-203">See also</span></span>



[<span data-ttu-id="ef929-204">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="ef929-204">IMAPISession::GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md)
  
[<span data-ttu-id="ef929-205">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="ef929-205">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="ef929-206">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="ef929-206">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

