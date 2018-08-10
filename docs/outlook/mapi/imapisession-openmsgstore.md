---
title: IMAPISessionOpenMsgStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenMsgStore
api_type:
- COM
ms.assetid: 7f73b5cf-7093-42e9-8acc-63d73df77cf5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 983c22772acfea7837e85d409b7928a35aed91ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817453"
---
# <a name="imapisessionopenmsgstore"></a><span data-ttu-id="b86a4-103">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="b86a4-103">IMAPISession::OpenMsgStore</span></span>

<span data-ttu-id="b86a4-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b86a4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b86a4-105">Se abre un almacén de mensajes y devuelve un puntero [IMsgStore](imsgstoreimapiprop.md) para aún más el acceso.</span><span class="sxs-lookup"><span data-stu-id="b86a4-105">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenMsgStore(
  ULONG_PTR ulUIParam,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMDB FAR * lppMDB
);
```

## <a name="parameters"></a><span data-ttu-id="b86a4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b86a4-106">Parameters</span></span>

<span data-ttu-id="b86a4-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b86a4-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="b86a4-108">[entrada] Un identificador de la ventana primaria del cuadro de diálogo dirección común y otros relacionados con la muestra.</span><span class="sxs-lookup"><span data-stu-id="b86a4-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
<span data-ttu-id="b86a4-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b86a4-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="b86a4-110">[entrada] El número de bytes en el identificador de entrada indicado por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b86a4-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="b86a4-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="b86a4-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="b86a4-112">[entrada] Un puntero al identificador de entrada del almacén de mensajes que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="b86a4-112">[in] A pointer to the entry identifier of the message store to be opened.</span></span> <span data-ttu-id="b86a4-113">El parámetro _lpEntryID_ no debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="b86a4-113">The  _lpEntryID_ parameter must not be NULL.</span></span> 
    
<span data-ttu-id="b86a4-114">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="b86a4-114">_lpInterface_</span></span>
  
> <span data-ttu-id="b86a4-115">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para obtener acceso al almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b86a4-115">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message store.</span></span> <span data-ttu-id="b86a4-116">Pasando NULL hace que el parámetro _lppMDB_ devolver un puntero a la interfaz estándar para un almacén de mensajes (**IMsgStore**).</span><span class="sxs-lookup"><span data-stu-id="b86a4-116">Passing NULL causes the  _lppMDB_ parameter to return a pointer to the standard interface for a message store (**IMsgStore**).</span></span>
    
<span data-ttu-id="b86a4-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b86a4-117">_ulFlags_</span></span>
  
> <span data-ttu-id="b86a4-118">[entrada] Una máscara de bits de indicadores que controla cómo se abre el objeto.</span><span class="sxs-lookup"><span data-stu-id="b86a4-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="b86a4-119">Se pueden usar los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="b86a4-119">The following flags can be used:</span></span>
    
  - <span data-ttu-id="b86a4-120">MAPI_BEST_ACCESS: Las solicitudes que se abre el almacén de mensajes con los permisos de red máximo permiten para el usuario y el número máximo de clientes permisos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b86a4-120">MAPI_BEST_ACCESS: Requests that the message store be opened with the maximum network permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="b86a4-121">Por ejemplo, si el cliente no tiene permiso de lectura y escritura, se debe abrir el almacén de mensajes con permiso de lectura y escritura; Si el cliente no tiene permiso de sólo lectura, se debe abrir el almacén de mensajes con permiso de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="b86a4-121">For example, if the client has read/write permission, the message store should be opened with read/write permission; if the client has read-only permission, the message store should be opened with read-only permission.</span></span> 
      
  - <span data-ttu-id="b86a4-122">MAPI_DEFERRED_ERRORS: Permite **OpenMsgStore** devolver correctamente, posiblemente antes de que el mensaje almacén es completamente disponible para el cliente de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b86a4-122">MAPI_DEFERRED_ERRORS: Allows **OpenMsgStore** to return successfully, possibly before the message store is fully available to the calling client.</span></span> <span data-ttu-id="b86a4-123">Si el almacén de mensajes no está disponible, realizar una llamada de objeto posteriores puede provocar un error.</span><span class="sxs-lookup"><span data-stu-id="b86a4-123">If the message store is not available, making a subsequent object call can raise an error.</span></span> 
      
  - <span data-ttu-id="b86a4-124">MDB\_NO_DIALOG: impide que la presentación de cuadros de diálogo de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="b86a4-124">MDB\_NO_DIALOG: Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="b86a4-125">Si se establece este indicador y **OpenMsgStore** dispone de información de configuración incompleta para abrir el almacén de mensajes sin ayuda del usuario, devuelve MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="b86a4-125">If this flag is set, and **OpenMsgStore** has insufficient configuration information to open the message store without the user's help, it returns MAPI_E_LOGON_FAILED.</span></span> <span data-ttu-id="b86a4-126">Si no se establece este indicador, el proveedor de almacenamiento de mensajes puede preguntar al usuario para corregir un nombre o una contraseña o para llevar a cabo otras acciones que son necesarios para establecer una conexión con el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b86a4-126">If this flag is not set, the message store provider can prompt the user to correct a name or password or to perform other actions that are needed to establish a connection to the message store.</span></span> 
      
  - <span data-ttu-id="b86a4-127">MDB\_NO_MAIL: el almacén de mensajes no se debe usar para enviar o recibir correo.</span><span class="sxs-lookup"><span data-stu-id="b86a4-127">MDB\_NO_MAIL: The message store should not be used for sending or receiving mail.</span></span> <span data-ttu-id="b86a4-128">Cuando se establece este marcador, MAPI no notifica a la cola MAPI que se va a abrir este almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b86a4-128">When this flag is set, MAPI does not notify the MAPI spooler that this message store is being opened.</span></span>
      
  - <span data-ttu-id="b86a4-129">MDB\_ONLINE: en modo caché de Exchange, un proveedor de servicio o cliente puede llamar a este método con MDB_ONLINE para reemplazar la conexión con el almacén de mensajes local y abrir el almacén en el servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="b86a4-129">MDB\_ONLINE: In Cached Exchange Mode, a client or service provider can call this method with MDB_ONLINE to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="b86a4-130">No se puede abrir un almacén de Exchange en modo de caché y en modo sin caché al mismo tiempo en la misma sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="b86a4-130">You cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="b86a4-131">Si ya ha abierto el almacén de mensajes almacenados en caché, ya sea debe cerrar el almacén antes de que se abra con esta marca, o se abre una nueva sesión MAPI donde puede abrir el almacén de Exchange en el servidor remoto mediante el uso de esta marca.</span><span class="sxs-lookup"><span data-stu-id="b86a4-131">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>
      
  - <span data-ttu-id="b86a4-132">MDB_TEMPORARY: Indica a MAPI que el almacén de mensajes no es permanente y no se debe agregar a la tabla de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b86a4-132">MDB_TEMPORARY: Instructs MAPI that the message store is not permanent and should not be added to the message store table.</span></span> <span data-ttu-id="b86a4-133">Este indicador se utiliza para iniciar sesión en el almacén de mensajes, por lo que la información se puede recuperar mediante programación desde la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="b86a4-133">This flag is used to log on to the message store so information can be retrieved programmatically from the profile section.</span></span> 
      
  - <span data-ttu-id="b86a4-134">MDB_WRITE: Las solicitudes de lectura y escritura permiso para el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b86a4-134">MDB_WRITE: Requests read/write permission to the message store.</span></span>
    
<span data-ttu-id="b86a4-135">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="b86a4-135">_lppMDB_</span></span>
  
> <span data-ttu-id="b86a4-136">[out] Puntero a un puntero del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b86a4-136">[out] Pointer to a pointer of the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b86a4-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b86a4-137">Return value</span></span>

<span data-ttu-id="b86a4-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="b86a4-138">S_OK</span></span> 
  
> <span data-ttu-id="b86a4-139">El almacén de mensajes se abrió correctamente.</span><span class="sxs-lookup"><span data-stu-id="b86a4-139">The message store was successfully opened.</span></span>
    
<span data-ttu-id="b86a4-140">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b86a4-140">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="b86a4-141">Se ha intentado tener acceso a un almacén de mensajes para los que el usuario no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="b86a4-141">An attempt was made to access a message store for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="b86a4-142">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b86a4-142">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="b86a4-143">El almacén de mensajes indicado por _lpEntryID_ no existe.</span><span class="sxs-lookup"><span data-stu-id="b86a4-143">The message store indicated by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="b86a4-144">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="b86a4-144">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="b86a4-145">El servidor no está configurado para admitir la página de códigos del cliente.</span><span class="sxs-lookup"><span data-stu-id="b86a4-145">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="b86a4-146">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="b86a4-146">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="b86a4-147">El servidor no está configurado para admitir la información de configuración regional del cliente.</span><span class="sxs-lookup"><span data-stu-id="b86a4-147">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="b86a4-148">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="b86a4-148">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="b86a4-149">La llamada se ha realizado correctamente, pero el proveedor de almacén de mensajes tiene información de error disponible.</span><span class="sxs-lookup"><span data-stu-id="b86a4-149">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="b86a4-150">Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="b86a4-150">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="b86a4-151">Para obtener la información de error desde el proveedor, llame al método [IMAPISession::GetLastError](imapisession-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="b86a4-151">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> <span data-ttu-id="b86a4-152">Para probar esta advertencia, utilice la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="b86a4-152">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="b86a4-153">Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="b86a4-153">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b86a4-154">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b86a4-154">Remarks</span></span>

<span data-ttu-id="b86a4-155">El método **IMAPISession::OpenMsgStore** abre un almacén de mensajes determinado.</span><span class="sxs-lookup"><span data-stu-id="b86a4-155">The **IMAPISession::OpenMsgStore** method opens a particular message store.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b86a4-156">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="b86a4-156">Notes to callers</span></span>

<span data-ttu-id="b86a4-157">El nivel de permisos predeterminado para los almacenes de mensajes es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="b86a4-157">The default permission level for message stores is read-only.</span></span> <span data-ttu-id="b86a4-158">Si se establece la marca MDB_WRITE, que aún es posible que no se concedido permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b86a4-158">If you set the MDB_WRITE flag, you still might not be granted read/write permission.</span></span> <span data-ttu-id="b86a4-159">El nivel final de acceso que se asigna MAPI para el almacén de mensajes depende de su nivel de permiso, el mensaje almacén propio y el proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b86a4-159">The final level of access that MAPI assigns to the message store depends on your permission level, the message store itself, and the message store provider.</span></span> 
  
<span data-ttu-id="b86a4-160">Si se llama **OpenMsgStore** para abrir un almacén de mensajes con permiso de sólo lectura, ocurrirá lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b86a4-160">If you call **OpenMsgStore** to open a message store with read-only permission, the following will occur:</span></span> 
  
- <span data-ttu-id="b86a4-161">El almacén **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) (propiedad) no tendrá su almacén de\_MODIFY_OK y almacén de\_CREATE_OK bits conjunto.</span><span class="sxs-lookup"><span data-stu-id="b86a4-161">The store's **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property will not have its STORE\_MODIFY_OK and STORE\_CREATE_OK bits set.</span></span> 
    
- <span data-ttu-id="b86a4-162">Se producirá un error en las llamadas para abrir uno de los mensajes o las carpetas del almacén de mensajes mediante el uso de [IMAPISession::OpenEntry](imapisession-openentry.md) con el conjunto de marca MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="b86a4-162">Calls to open one of the message store's messages or folders by using [IMAPISession::OpenEntry](imapisession-openentry.md) with the MAPI_MODIFY flag set will fail.</span></span> 
    
- <span data-ttu-id="b86a4-163">Se producirá un error en las llamadas para abrir una de las propiedades de los mensajes o las carpetas del almacén de mensajes mediante el uso de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) con la marca MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="b86a4-163">Calls to open one of the properties of the message store's messages or folders by using [IMAPIProp::OpenProperty](imapiprop-openproperty.md) with the MAPI_MODIFY flag will fail.</span></span> 
    
- <span data-ttu-id="b86a4-164">Se producirá un error en las llamadas a cualquiera de los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="b86a4-164">Calls to any of the following methods will fail:</span></span> 
    
  - [<span data-ttu-id="b86a4-165">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="b86a4-165">IMAPIFolder::CreateMessage</span></span>](imapifolder-createmessage.md)
    
  - [<span data-ttu-id="b86a4-166">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="b86a4-166">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
    
  - [<span data-ttu-id="b86a4-167">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="b86a4-167">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
    
  - [<span data-ttu-id="b86a4-168">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="b86a4-168">IMAPIFolder::DeleteFolder</span></span>](imapifolder-deletefolder.md)
    
  - [<span data-ttu-id="b86a4-169">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="b86a4-169">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
    
  - [<span data-ttu-id="b86a4-170">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="b86a4-170">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
  - [<span data-ttu-id="b86a4-171">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="b86a4-171">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
  
- <span data-ttu-id="b86a4-172">Las llamadas a los métodos siguientes se producirá un error si el destino del mensaje copiado de es de sólo lectura, si el destino es el mismo que el almacén de mensajes de origen o es otro almacén de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="b86a4-172">Calls to the following methods will fail if the destination for the copied message is read-only, whether the destination is the same as the source message store or is another read-only store.</span></span>
    
  - [<span data-ttu-id="b86a4-173">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="b86a4-173">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
  - [<span data-ttu-id="b86a4-174">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="b86a4-174">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
  - [<span data-ttu-id="b86a4-175">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="b86a4-175">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b86a4-176">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b86a4-176">MFCMAPI reference</span></span>

<span data-ttu-id="b86a4-177">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="b86a4-177">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b86a4-178">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="b86a4-178">**File**</span></span>|<span data-ttu-id="b86a4-179">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="b86a4-179">**Function**</span></span>|<span data-ttu-id="b86a4-180">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="b86a4-180">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b86a4-181">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="b86a4-181">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="b86a4-182">CallOpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="b86a4-182">CallOpenMsgStore</span></span>  <br/> |<span data-ttu-id="b86a4-183">MFCMAPI utiliza el método **IMAPISession::OpenMsgStore** para abrir un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b86a4-183">MFCMAPI uses the **IMAPISession::OpenMsgStore** method to open a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b86a4-184">Vea también</span><span class="sxs-lookup"><span data-stu-id="b86a4-184">See also</span></span>

- [<span data-ttu-id="b86a4-185">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b86a4-185">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
- [<span data-ttu-id="b86a4-186">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b86a4-186">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
- [<span data-ttu-id="b86a4-187">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="b86a4-187">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
- [<span data-ttu-id="b86a4-188">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="b86a4-188">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
- [<span data-ttu-id="b86a4-189">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b86a4-189">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)
- [<span data-ttu-id="b86a4-190">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="b86a4-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
- [<span data-ttu-id="b86a4-191">Uso de macros para el control de errores</span><span class="sxs-lookup"><span data-stu-id="b86a4-191">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

