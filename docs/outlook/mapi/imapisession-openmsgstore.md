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
ms.openlocfilehash: 19d3df004676a71e2bf6243d9288efd824d99c33
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418025"
---
# <a name="imapisessionopenmsgstore"></a><span data-ttu-id="7705d-103">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="7705d-103">IMAPISession::OpenMsgStore</span></span>

<span data-ttu-id="7705d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7705d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7705d-105">Abre un almacén de mensajes y devuelve un puntero [IMsgStore](imsgstoreimapiprop.md) para obtener más acceso.</span><span class="sxs-lookup"><span data-stu-id="7705d-105">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="7705d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7705d-106">Parameters</span></span>

<span data-ttu-id="7705d-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="7705d-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="7705d-108">[entrada] Identificador de la ventana principal del cuadro de diálogo de dirección común y otras pantallas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="7705d-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
<span data-ttu-id="7705d-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="7705d-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="7705d-110">[entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="7705d-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="7705d-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="7705d-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="7705d-112">[entrada] Puntero al identificador de entrada del almacén de mensajes que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="7705d-112">[in] A pointer to the entry identifier of the message store to be opened.</span></span> <span data-ttu-id="7705d-113">El  _parámetro lpEntryID_ no debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="7705d-113">The  _lpEntryID_ parameter must not be NULL.</span></span> 
    
<span data-ttu-id="7705d-114">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="7705d-114">_lpInterface_</span></span>
  
> <span data-ttu-id="7705d-115">[entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7705d-115">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message store.</span></span> <span data-ttu-id="7705d-116">Pasar NULL hace que  _el parámetro lppMDB_ devuelva un puntero a la interfaz estándar de un almacén de mensajes (**IMsgStore**).</span><span class="sxs-lookup"><span data-stu-id="7705d-116">Passing NULL causes the  _lppMDB_ parameter to return a pointer to the standard interface for a message store (**IMsgStore**).</span></span>
    
<span data-ttu-id="7705d-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7705d-117">_ulFlags_</span></span>
  
> <span data-ttu-id="7705d-118">[entrada] Máscara de bits de marcas que controla cómo se abre el objeto.</span><span class="sxs-lookup"><span data-stu-id="7705d-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="7705d-119">Se pueden usar las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="7705d-119">The following flags can be used:</span></span>
    
  - <span data-ttu-id="7705d-120">MAPI_BEST_ACCESS: solicita que el almacén de mensajes se abra con los permisos de red máximos permitidos para el usuario y los permisos máximos de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="7705d-120">MAPI_BEST_ACCESS: Requests that the message store be opened with the maximum network permissions allowed for the user and the maximum client application permissions.</span></span> <span data-ttu-id="7705d-121">Por ejemplo, si el cliente tiene permiso de lectura y escritura, el almacén de mensajes debe abrirse con permiso de lectura y escritura; si el cliente tiene permiso de solo lectura, el almacén de mensajes debe abrirse con permiso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7705d-121">For example, if the client has read/write permission, the message store should be opened with read/write permission; if the client has read-only permission, the message store should be opened with read-only permission.</span></span> 
      
  - <span data-ttu-id="7705d-122">MAPI_DEFERRED_ERRORS: permite que **OpenMsgStore** vuelva correctamente, posiblemente antes de que el almacén de mensajes esté totalmente disponible para el cliente que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="7705d-122">MAPI_DEFERRED_ERRORS: Allows **OpenMsgStore** to return successfully, possibly before the message store is fully available to the calling client.</span></span> <span data-ttu-id="7705d-123">Si el almacén de mensajes no está disponible, realizar una llamada a objeto posterior puede generar un error.</span><span class="sxs-lookup"><span data-stu-id="7705d-123">If the message store is not available, making a subsequent object call can raise an error.</span></span> 
      
  - <span data-ttu-id="7705d-124">MDB \_ NO_DIALOG: impide que se muestren cuadros de diálogo de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="7705d-124">MDB\_NO_DIALOG: Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="7705d-125">Si se establece esta marca y **OpenMsgStore** no tiene suficiente información de configuración para abrir el almacén de mensajes sin la ayuda del usuario, devuelve MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="7705d-125">If this flag is set, and **OpenMsgStore** has insufficient configuration information to open the message store without the user's help, it returns MAPI_E_LOGON_FAILED.</span></span> <span data-ttu-id="7705d-126">Si no se establece esta marca, el proveedor del almacén de mensajes puede pedir al usuario que corrija un nombre o contraseña o que realice otras acciones necesarias para establecer una conexión con el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7705d-126">If this flag is not set, the message store provider can prompt the user to correct a name or password or to perform other actions that are needed to establish a connection to the message store.</span></span> 
      
  - <span data-ttu-id="7705d-127">MDB \_ NO_MAIL: el almacén de mensajes no debe usarse para enviar o recibir correo.</span><span class="sxs-lookup"><span data-stu-id="7705d-127">MDB\_NO_MAIL: The message store should not be used for sending or receiving mail.</span></span> <span data-ttu-id="7705d-128">Cuando se establece esta marca, MAPI no notifica a la cola MAPI que se está abierto este almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7705d-128">When this flag is set, MAPI does not notify the MAPI spooler that this message store is being opened.</span></span>
      
  - <span data-ttu-id="7705d-129">MDB ONLINE: en modo caché de Exchange, un cliente o proveedor de servicios puede llamar a este método con MDB_ONLINE para invalidar la conexión al almacén de mensajes local y abrir el almacén en el \_ servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="7705d-129">MDB\_ONLINE: In Cached Exchange Mode, a client or service provider can call this method with MDB_ONLINE to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="7705d-130">No puede abrir un almacén de Exchange en modo almacenado en caché y en modo no almacenado en caché al mismo tiempo en la misma sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="7705d-130">You cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="7705d-131">Si ya ha abierto el almacén de mensajes en modo caché, debe cerrar el almacén antes de abrirlo con esta marca o abrir una nueva sesión MAPI donde puede abrir el almacén de Exchange en el servidor remoto mediante este marcador.</span><span class="sxs-lookup"><span data-stu-id="7705d-131">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>
      
  - <span data-ttu-id="7705d-132">MDB_TEMPORARY: indica a MAPI que el almacén de mensajes no es permanente y no debe agregarse a la tabla del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7705d-132">MDB_TEMPORARY: Instructs MAPI that the message store is not permanent and should not be added to the message store table.</span></span> <span data-ttu-id="7705d-133">Esta marca se usa para iniciar sesión en el almacén de mensajes de modo que la información se pueda recuperar mediante programación desde la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="7705d-133">This flag is used to log on to the message store so information can be retrieved programmatically from the profile section.</span></span> 
      
  - <span data-ttu-id="7705d-134">MDB_WRITE: solicita permiso de lectura y escritura en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7705d-134">MDB_WRITE: Requests read/write permission to the message store.</span></span>
    
<span data-ttu-id="7705d-135">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="7705d-135">_lppMDB_</span></span>
  
> <span data-ttu-id="7705d-136">[salida] Puntero a un puntero del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7705d-136">[out] Pointer to a pointer of the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7705d-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7705d-137">Return value</span></span>

<span data-ttu-id="7705d-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="7705d-138">S_OK</span></span> 
  
> <span data-ttu-id="7705d-139">El almacén de mensajes se abrió correctamente.</span><span class="sxs-lookup"><span data-stu-id="7705d-139">The message store was successfully opened.</span></span>
    
<span data-ttu-id="7705d-140">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="7705d-140">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="7705d-141">Se intentó obtener acceso a un almacén de mensajes para el que el usuario no tiene permisos suficientes.</span><span class="sxs-lookup"><span data-stu-id="7705d-141">An attempt was made to access a message store for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="7705d-142">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="7705d-142">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="7705d-143">El almacén de mensajes indicado por  _lpEntryID_ no existe.</span><span class="sxs-lookup"><span data-stu-id="7705d-143">The message store indicated by  _lpEntryID_ does not exist.</span></span> 
    
<span data-ttu-id="7705d-144">MAPI_E_UNKNOWN_CPID</span><span class="sxs-lookup"><span data-stu-id="7705d-144">MAPI_E_UNKNOWN_CPID</span></span> 
  
> <span data-ttu-id="7705d-145">El servidor no está configurado para admitir la página de códigos del cliente.</span><span class="sxs-lookup"><span data-stu-id="7705d-145">The server is not configured to support the client's code page.</span></span>
    
<span data-ttu-id="7705d-146">MAPI_E_UNKNOWN_LCID</span><span class="sxs-lookup"><span data-stu-id="7705d-146">MAPI_E_UNKNOWN_LCID</span></span> 
  
> <span data-ttu-id="7705d-147">El servidor no está configurado para admitir la información de configuración regional del cliente.</span><span class="sxs-lookup"><span data-stu-id="7705d-147">The server is not configured to support the client's locale information.</span></span>
    
<span data-ttu-id="7705d-148">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="7705d-148">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="7705d-149">La llamada se ha hecho correctamente, pero el proveedor del almacén de mensajes tiene información de error disponible.</span><span class="sxs-lookup"><span data-stu-id="7705d-149">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="7705d-150">Cuando se devuelve esta advertencia, la llamada debe tratarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="7705d-150">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="7705d-151">Para obtener la información de error del proveedor, llame al [método IMAPISession::GetLastError.](imapisession-getlasterror.md)</span><span class="sxs-lookup"><span data-stu-id="7705d-151">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> <span data-ttu-id="7705d-152">Para probar esta advertencia, use la **macro HR_FAILED** datos.</span><span class="sxs-lookup"><span data-stu-id="7705d-152">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="7705d-153">Para obtener más información, vea [Usar macros para el control de errores.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="7705d-153">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7705d-154">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7705d-154">Remarks</span></span>

<span data-ttu-id="7705d-155">El **método IMAPISession::OpenMsgStore** abre un almacén de mensajes determinado.</span><span class="sxs-lookup"><span data-stu-id="7705d-155">The **IMAPISession::OpenMsgStore** method opens a particular message store.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7705d-156">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="7705d-156">Notes to callers</span></span>

<span data-ttu-id="7705d-157">El nivel de permisos predeterminado para los almacenes de mensajes es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7705d-157">The default permission level for message stores is read-only.</span></span> <span data-ttu-id="7705d-158">Si establece la marca MDB_WRITE, es posible que aún no se le conceda permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="7705d-158">If you set the MDB_WRITE flag, you still might not be granted read/write permission.</span></span> <span data-ttu-id="7705d-159">El nivel final de acceso que MAPI asigna al almacén de mensajes depende del nivel de permisos, del propio almacén de mensajes y del proveedor del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7705d-159">The final level of access that MAPI assigns to the message store depends on your permission level, the message store itself, and the message store provider.</span></span> 
  
<span data-ttu-id="7705d-160">Si llama a **OpenMsgStore para** abrir un almacén de mensajes con permiso de solo lectura, se producirá lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7705d-160">If you call **OpenMsgStore** to open a message store with read-only permission, the following will occur:</span></span> 
  
- <span data-ttu-id="7705d-161">La propiedad **PR \_ STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) del almacén no tendrá los bits MODIFY_OK \_ y STORE CREATE_OK \_ bits.</span><span class="sxs-lookup"><span data-stu-id="7705d-161">The store's **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property will not have its STORE\_MODIFY_OK and STORE\_CREATE_OK bits set.</span></span> 
    
- <span data-ttu-id="7705d-162">Las llamadas para abrir uno de los mensajes o carpetas del almacén de mensajes mediante [IMAPISession::OpenEntry](imapisession-openentry.md) con la marca MAPI_MODIFY se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="7705d-162">Calls to open one of the message store's messages or folders by using [IMAPISession::OpenEntry](imapisession-openentry.md) with the MAPI_MODIFY flag set will fail.</span></span> 
    
- <span data-ttu-id="7705d-163">Las llamadas para abrir una de las propiedades de los mensajes o carpetas del almacén de mensajes mediante [IMAPIProp::OpenProperty](imapiprop-openproperty.md) con la marca MAPI_MODIFY error.</span><span class="sxs-lookup"><span data-stu-id="7705d-163">Calls to open one of the properties of the message store's messages or folders by using [IMAPIProp::OpenProperty](imapiprop-openproperty.md) with the MAPI_MODIFY flag will fail.</span></span> 
    
- <span data-ttu-id="7705d-164">Se producirá un error en las llamadas a cualquiera de los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="7705d-164">Calls to any of the following methods will fail:</span></span> 
    
  - [<span data-ttu-id="7705d-165">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="7705d-165">IMAPIFolder::CreateMessage</span></span>](imapifolder-createmessage.md)
    
  - [<span data-ttu-id="7705d-166">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="7705d-166">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
    
  - [<span data-ttu-id="7705d-167">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="7705d-167">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
    
  - [<span data-ttu-id="7705d-168">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="7705d-168">IMAPIFolder::DeleteFolder</span></span>](imapifolder-deletefolder.md)
    
  - [<span data-ttu-id="7705d-169">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="7705d-169">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
    
  - [<span data-ttu-id="7705d-170">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="7705d-170">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
  - [<span data-ttu-id="7705d-171">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="7705d-171">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
  
- <span data-ttu-id="7705d-172">Las llamadas a los métodos siguientes producirán un error si el destino del mensaje copiado es de solo lectura, si el destino es el mismo que el almacén de mensajes de origen o si es otro almacén de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7705d-172">Calls to the following methods will fail if the destination for the copied message is read-only, whether the destination is the same as the source message store or is another read-only store.</span></span>
    
  - [<span data-ttu-id="7705d-173">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="7705d-173">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
  - [<span data-ttu-id="7705d-174">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="7705d-174">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
  - [<span data-ttu-id="7705d-175">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="7705d-175">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7705d-176">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7705d-176">MFCMAPI reference</span></span>

<span data-ttu-id="7705d-177">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="7705d-177">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7705d-178">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="7705d-178">**File**</span></span>|<span data-ttu-id="7705d-179">**Función**</span><span class="sxs-lookup"><span data-stu-id="7705d-179">**Function**</span></span>|<span data-ttu-id="7705d-180">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="7705d-180">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7705d-181">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="7705d-181">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="7705d-182">CallOpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="7705d-182">CallOpenMsgStore</span></span>  <br/> |<span data-ttu-id="7705d-183">MFCMAPI usa el **método IMAPISession::OpenMsgStore** para abrir un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7705d-183">MFCMAPI uses the **IMAPISession::OpenMsgStore** method to open a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7705d-184">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7705d-184">See also</span></span>

- [<span data-ttu-id="7705d-185">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7705d-185">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)
- [<span data-ttu-id="7705d-186">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7705d-186">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
- [<span data-ttu-id="7705d-187">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="7705d-187">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)
- [<span data-ttu-id="7705d-188">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="7705d-188">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
- [<span data-ttu-id="7705d-189">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7705d-189">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)
- [<span data-ttu-id="7705d-190">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="7705d-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
- [<span data-ttu-id="7705d-191">Uso de macros para el control de errores</span><span class="sxs-lookup"><span data-stu-id="7705d-191">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

