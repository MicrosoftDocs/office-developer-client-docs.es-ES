---
title: IMSProviderSpoolerLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.SpoolerLogon
api_type:
- COM
ms.assetid: 79d5af23-efad-4013-a330-56babfb2bb0f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 794674df38266743cac8c947ec93dc1fcfff438b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430577"
---
# <a name="imsproviderspoolerlogon"></a><span data-ttu-id="a8dc3-103">IMSProvider::SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="a8dc3-103">IMSProvider::SpoolerLogon</span></span>

  
  
<span data-ttu-id="a8dc3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8dc3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8dc3-105">Registra la cola MAPI en un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-105">Logs the MAPI spooler on to a message store.</span></span>
  
```cpp
HRESULT SpoolerLogon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  LPCIID lpInterface,
  ULONG cbSpoolSecurity,
  LPBYTE lpbSpoolSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPMSLOGON FAR * lppMSLogon,
  LPMDB FAR * lppMDB     
);
```

## <a name="parameters"></a><span data-ttu-id="a8dc3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8dc3-106">Parameters</span></span>

 <span data-ttu-id="a8dc3-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="a8dc3-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="a8dc3-108">[entrada] Puntero al objeto de soporte MAPI para el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-108">[in] A pointer to the MAPI support object for the message store.</span></span>
    
 <span data-ttu-id="a8dc3-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a8dc3-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="a8dc3-110">[entrada] Identificador de la ventana primaria de cualquier cuadro de diálogo o ventana que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-110">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> 
    
 <span data-ttu-id="a8dc3-111">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="a8dc3-111">_lpszProfileName_</span></span>
  
> <span data-ttu-id="a8dc3-112">[entrada] Puntero a una cadena que contiene el nombre del perfil que se usa para el inicio de sesión de cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-112">[in] A pointer to a string that contains the name of the profile being used for the MAPI spooler logon.</span></span> <span data-ttu-id="a8dc3-113">Esta cadena puede mostrarse en cuadros de diálogo, escribirse en un archivo de registro o simplemente omitirse.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-113">This string can be displayed in dialog boxes, written out to a log file, or simply ignored.</span></span> <span data-ttu-id="a8dc3-114">Debe estar en formato Unicode si la marca MAPI_UNICODE está establecida en el _parámetro ulFlags._</span><span class="sxs-lookup"><span data-stu-id="a8dc3-114">It must be in Unicode format if the MAPI_UNICODE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="a8dc3-115">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a8dc3-115">_cbEntryID_</span></span>
  
> <span data-ttu-id="a8dc3-116">[entrada] Tamaño, en bytes, del identificador de entrada al que apunta el _parámetro lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="a8dc3-116">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a8dc3-117">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="a8dc3-117">_lpEntryID_</span></span>
  
> <span data-ttu-id="a8dc3-118">[entrada] Puntero al identificador de entrada del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-118">[in] A pointer to the entry identifier for the message store.</span></span> <span data-ttu-id="a8dc3-119">Pasar NULL en el parámetro  _lpEntryID_ indica que aún no se ha seleccionado un almacén de mensajes y que se pueden presentar los cuadros de diálogo que permiten al usuario seleccionar un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-119">Passing NULL in the  _lpEntryID_ parameter indicates that a message store has not yet been selected and that dialog boxes that enable the user to select a message store can be presented.</span></span> 
    
 <span data-ttu-id="a8dc3-120">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a8dc3-120">_ulFlags_</span></span>
  
> <span data-ttu-id="a8dc3-121">[entrada] Máscara de bits de marcas que controla cómo se realiza el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-121">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="a8dc3-122">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="a8dc3-122">The following flags can be set:</span></span>
    
<span data-ttu-id="a8dc3-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="a8dc3-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="a8dc3-124">La llamada puede ser correcta incluso si el objeto subyacente no está disponible para la implementación de llamada.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-124">The call is allowed to succeed even if the underlying object is not available to the calling implementation.</span></span> <span data-ttu-id="a8dc3-125">Si el objeto no está disponible, una llamada posterior al objeto podría generar un error.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-125">If the object is not available, a subsequent call to the object might raise an error.</span></span>
    
<span data-ttu-id="a8dc3-126">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a8dc3-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a8dc3-127">Las cadenas pasadas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-127">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="a8dc3-128">Si MAPI_UNICODE no se establece, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-128">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="a8dc3-129">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a8dc3-129">MDB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="a8dc3-130">Impide que se muestren cuadros de diálogo de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-130">Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="a8dc3-131">Si se establece esta marca, se devuelve el valor MAPI_E_LOGON_FAILED error si el inicio de sesión no se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-131">If this flag is set, the error value MAPI_E_LOGON_FAILED is returned if the logon is unsuccessful.</span></span> <span data-ttu-id="a8dc3-132">Si no se establece esta marca, el proveedor del almacén de mensajes puede pedir al usuario que corrija un nombre o contraseña, que inserte un disco o que realice otras acciones necesarias para establecer una conexión con el almacén.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-132">If this flag is not set, the message store provider can prompt the user to correct a name or password, to insert a disk, or to perform other actions necessary to establish connection to the store.</span></span>
    
<span data-ttu-id="a8dc3-133">MDB_WRITE</span><span class="sxs-lookup"><span data-stu-id="a8dc3-133">MDB_WRITE</span></span> 
  
> <span data-ttu-id="a8dc3-134">Solicita permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-134">Requests read/write permission.</span></span>
    
 <span data-ttu-id="a8dc3-135">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a8dc3-135">_lpInterface_</span></span>
  
> <span data-ttu-id="a8dc3-136">[entrada] Puntero al identificador de interfaz (IID) en el que se debe iniciar sesión en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-136">[in] A pointer to the interface identifier (IID) for the message store to log on to.</span></span> <span data-ttu-id="a8dc3-137">Pasar NULL indica que se devuelve la interfaz MAPI para el almacén de mensajes ([IMsgStore](imsgstoreimapiprop.md)).</span><span class="sxs-lookup"><span data-stu-id="a8dc3-137">Passing NULL indicates the MAPI interface for the message store ([IMsgStore](imsgstoreimapiprop.md)) is returned.</span></span> <span data-ttu-id="a8dc3-138">El  _parámetro lpInterface_ también se puede establecer en un identificador para una interfaz adecuada para el almacén de mensajes (por ejemplo, IID_IUnknown o IID_IMAPIProp).</span><span class="sxs-lookup"><span data-stu-id="a8dc3-138">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the message store (for example IID_IUnknown or IID_IMAPIProp).</span></span> 
    
 <span data-ttu-id="a8dc3-139">_cbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="a8dc3-139">_cbSpoolSecurity_</span></span>
  
> <span data-ttu-id="a8dc3-140">[entrada] Puntero al tamaño, en bytes, de los datos de validación en el parámetro _lppbSpoolSecurity._</span><span class="sxs-lookup"><span data-stu-id="a8dc3-140">[in] A pointer to the size, in bytes, of validation data in the  _lppbSpoolSecurity_ parameter.</span></span> 
    
 <span data-ttu-id="a8dc3-141">_lpbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="a8dc3-141">_lpbSpoolSecurity_</span></span>
  
> <span data-ttu-id="a8dc3-142">[entrada] Puntero a un puntero a datos de validación.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-142">[in] A pointer to a pointer to validation data.</span></span> <span data-ttu-id="a8dc3-143">El **método SpoolerLogon** usa estos datos para iniciar sesión en la cola MAPI en el mismo almacén en el que el proveedor del almacén de mensajes inició sesión anteriormente mediante el método [IMSProvider::Logon.](imsprovider-logon.md)</span><span class="sxs-lookup"><span data-stu-id="a8dc3-143">The **SpoolerLogon** method uses this data to log the MAPI spooler on to the same store as the message store provider previously logged on to by using the [IMSProvider::Logon](imsprovider-logon.md) method.</span></span> 
    
 <span data-ttu-id="a8dc3-144">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="a8dc3-144">_lppMAPIError_</span></span>
  
> <span data-ttu-id="a8dc3-145">[salida] Puntero a un puntero a la estructura [MAPIERROR](mapierror.md) devuelta, si existe, que contiene información de versión, componente y contexto de un error.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-145">[out] A pointer to a pointer to the returned [MAPIERROR](mapierror.md) structure, if any, that contains version, component, and context information for an error.</span></span> <span data-ttu-id="a8dc3-146">El  _parámetro lppMAPIError_ se puede establecer en NULL si no hay ninguna **estructura MAPIERROR** que devolver.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-146">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="a8dc3-147">_lppMSLogon_</span><span class="sxs-lookup"><span data-stu-id="a8dc3-147">_lppMSLogon_</span></span>
  
> <span data-ttu-id="a8dc3-148">[salida] Puntero al puntero al objeto de inicio de sesión del almacén de mensajes para que MAPI inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-148">[out] A pointer to the pointer to the message store logon object for MAPI to log on to.</span></span>
    
 <span data-ttu-id="a8dc3-149">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="a8dc3-149">_lppMDB_</span></span>
  
> <span data-ttu-id="a8dc3-150">[salida] Puntero al puntero al objeto de almacén de mensajes para que la cola MAPI y las aplicaciones cliente inicien sesión.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-150">[out] A pointer to the pointer to the message store object for the MAPI spooler and client applications to log on to.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a8dc3-151">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8dc3-151">Return value</span></span>

<span data-ttu-id="a8dc3-152">S_OK</span><span class="sxs-lookup"><span data-stu-id="a8dc3-152">S_OK</span></span> 
  
> <span data-ttu-id="a8dc3-153">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-153">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a8dc3-154">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="a8dc3-154">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="a8dc3-155">El perfil no contiene información suficiente para que se complete el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-155">The profile does not contain enough information for the logon to complete.</span></span> <span data-ttu-id="a8dc3-156">Cuando se devuelve este valor, MAPI llama a la función de punto de entrada del servicio de mensajes del proveedor del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-156">When this value is returned, MAPI calls the message store provider's message service entry point function.</span></span>
    
<span data-ttu-id="a8dc3-157">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="a8dc3-157">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="a8dc3-158">La llamada se ha hecho correctamente, pero el proveedor del almacén de mensajes tiene información de error disponible.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-158">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="a8dc3-159">Cuando se devuelve esta advertencia, la llamada debe tratarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="a8dc3-160">Para probar esta advertencia, use la **macro HR_FAILED** datos.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="a8dc3-161">Para obtener más información, vea [Usar macros para el control de errores.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="a8dc3-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> <span data-ttu-id="a8dc3-162">Para obtener la información de error del proveedor, llame al [método IMAPISession::GetLastError.](imapisession-getlasterror.md)</span><span class="sxs-lookup"><span data-stu-id="a8dc3-162">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a8dc3-163">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a8dc3-163">Remarks</span></span>

<span data-ttu-id="a8dc3-164">La cola MAPI llama al método **IMSProvider::SpoolerLogon** para iniciar sesión en un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-164">The MAPI spooler calls the **IMSProvider::SpoolerLogon** method to log on to a message store.</span></span> <span data-ttu-id="a8dc3-165">La cola MAPI debe usar el objeto de almacén de mensajes devuelto por el proveedor de al almacenamiento de mensajes en el parámetro  _lppMDB_ durante y después del inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-165">The MAPI spooler should use the message store object returned by the message store provider in the  _lppMDB_ parameter during and after logon.</span></span> 
  
<span data-ttu-id="a8dc3-166">Por coherencia con el [método IMSProvider::Logon,](imsprovider-logon.md) el proveedor también devuelve un objeto de inicio de sesión del almacén de mensajes en el parámetro _lppMSLogon._</span><span class="sxs-lookup"><span data-stu-id="a8dc3-166">For consistency with the [IMSProvider::Logon](imsprovider-logon.md) method, the provider also returns a message store logon object in the  _lppMSLogon_ parameter.</span></span> <span data-ttu-id="a8dc3-167">El uso del objeto de almacén y el objeto de inicio de sesión son idénticos para el inicio de sesión habitual del almacén; debe haber una correspondencia uno a uno entre el objeto de inicio de sesión y el objeto de almacén, de forma que los objetos actúen como si fuera un objeto que exponga dos interfaces.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-167">The use of the store object and the logon object are identical for usual store logon; there should be a one-to-one correspondence between the logon object and the store object such that the objects act as if they are one object that exposes two interfaces.</span></span> <span data-ttu-id="a8dc3-168">Los dos objetos se crean juntos y se liberan juntos.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-168">The two objects are created together and freed together.</span></span> 
  
<span data-ttu-id="a8dc3-169">El proveedor de almacenamiento debe marcar internamente el objeto de almacén de mensajes devuelto para indicar que la cola MAPI está utilizando el almacén.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-169">The store provider should internally mark the returned message store object to indicate that the store is being used by the MAPI spooler.</span></span> <span data-ttu-id="a8dc3-170">Algunos de los métodos para este objeto de almacén se comportan de forma diferente que para el objeto de almacén de mensajes proporcionado a las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-170">Some of the methods for this store object behave differently than for the message store object provided to client applications.</span></span> <span data-ttu-id="a8dc3-171">Mantener esta marca interna es la forma más común de desencadenar el comportamiento específico de la cola MAPI.</span><span class="sxs-lookup"><span data-stu-id="a8dc3-171">Keeping this internal mark is the most common way of triggering the behavior specific to the MAPI spooler.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a8dc3-172">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a8dc3-172">See also</span></span>



[<span data-ttu-id="a8dc3-173">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="a8dc3-173">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="a8dc3-174">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="a8dc3-174">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="a8dc3-175">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a8dc3-175">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

