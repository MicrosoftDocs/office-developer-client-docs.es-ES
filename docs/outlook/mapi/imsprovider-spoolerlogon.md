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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: eaf84e1b2a747b313f1534eb66b190d86cf89df9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817820"
---
# <a name="imsproviderspoolerlogon"></a><span data-ttu-id="7d9ff-103">IMSProvider::SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="7d9ff-103">IMSProvider::SpoolerLogon</span></span>

  
  
<span data-ttu-id="7d9ff-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7d9ff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7d9ff-105">Inicie sesión en un almacén de mensajes en la cola de MAPI.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-105">Logs the MAPI spooler on to a message store.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="7d9ff-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d9ff-106">Parameters</span></span>

 <span data-ttu-id="7d9ff-107">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="7d9ff-107">_lpMAPISup_</span></span>
  
> <span data-ttu-id="7d9ff-108">[entrada] Un puntero a la interfaz MAPI admite el objeto para el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-108">[in] A pointer to the MAPI support object for the message store.</span></span>
    
 <span data-ttu-id="7d9ff-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="7d9ff-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="7d9ff-110">[entrada] Un identificador de la ventana principal de windows o cuadros de diálogo que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-110">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> 
    
 <span data-ttu-id="7d9ff-111">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="7d9ff-111">_lpszProfileName_</span></span>
  
> <span data-ttu-id="7d9ff-112">[entrada] Un puntero a una cadena que contiene el nombre del perfil que se utiliza para el inicio de sesión de cola de impresión MAPI.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-112">[in] A pointer to a string that contains the name of the profile being used for the MAPI spooler logon.</span></span> <span data-ttu-id="7d9ff-113">Esta cadena se puede que se muestra en los cuadros de diálogo, escriben en un archivo de registro o simplemente se omite.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-113">This string can be displayed in dialog boxes, written out to a log file, or simply ignored.</span></span> <span data-ttu-id="7d9ff-114">Debe estar en formato Unicode si está establecido el indicador MAPI_UNICODE en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="7d9ff-114">It must be in Unicode format if the MAPI_UNICODE flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="7d9ff-115">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="7d9ff-115">_cbEntryID_</span></span>
  
> <span data-ttu-id="7d9ff-116">[entrada] El tamaño, en bytes, del identificador de entrada indicada por el parámetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="7d9ff-116">[in] The size, in bytes, of the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="7d9ff-117">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="7d9ff-117">_lpEntryID_</span></span>
  
> <span data-ttu-id="7d9ff-118">[entrada] Un puntero al identificador de entrada para el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-118">[in] A pointer to the entry identifier for the message store.</span></span> <span data-ttu-id="7d9ff-119">Pasar NULL en el parámetro _lpEntryID_ indica que no se ha seleccionado aún un almacén de mensajes y que se pueden presentar cuadros de diálogo que permiten al usuario seleccionar un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-119">Passing NULL in the  _lpEntryID_ parameter indicates that a message store has not yet been selected and that dialog boxes that enable the user to select a message store can be presented.</span></span> 
    
 <span data-ttu-id="7d9ff-120">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7d9ff-120">_ulFlags_</span></span>
  
> <span data-ttu-id="7d9ff-121">[entrada] Una máscara de bits de indicadores que controla cómo se realiza el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-121">[in] A bitmask of flags that controls how the logon is performed.</span></span> <span data-ttu-id="7d9ff-122">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="7d9ff-122">The following flags can be set:</span></span>
    
<span data-ttu-id="7d9ff-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="7d9ff-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="7d9ff-124">Se autoriza la llamada se realice correctamente, incluso si el objeto subyacente no está disponible para la implementación de la llamada.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-124">The call is allowed to succeed even if the underlying object is not available to the calling implementation.</span></span> <span data-ttu-id="7d9ff-125">Si el objeto no está disponible, una llamada posterior al objeto podría provocar un error.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-125">If the object is not available, a subsequent call to the object might raise an error.</span></span>
    
<span data-ttu-id="7d9ff-126">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-126">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7d9ff-127">Las cadenas que se pasan en están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-127">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="7d9ff-128">Si no se establece MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-128">If MAPI_UNICODE is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="7d9ff-129">MDB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="7d9ff-129">MDB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="7d9ff-130">Impide la presentación de cuadros de diálogo de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-130">Prevents the display of logon dialog boxes.</span></span> <span data-ttu-id="7d9ff-131">Si se establece este marcador, se devuelve el valor de error MAPI_E_LOGON_FAILED si el inicio de sesión se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-131">If this flag is set, the error value MAPI_E_LOGON_FAILED is returned if the logon is unsuccessful.</span></span> <span data-ttu-id="7d9ff-132">Si no se establece este indicador, el proveedor de almacenamiento de mensaje puede solicitar al usuario para corregir un nombre o una contraseña, para insertar un disco, o para llevar a cabo otras acciones necesarias para establecer la conexión con el almacén.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-132">If this flag is not set, the message store provider can prompt the user to correct a name or password, to insert a disk, or to perform other actions necessary to establish connection to the store.</span></span>
    
<span data-ttu-id="7d9ff-133">MDB_WRITE</span><span class="sxs-lookup"><span data-stu-id="7d9ff-133">MDB_WRITE</span></span> 
  
> <span data-ttu-id="7d9ff-134">Las solicitudes de permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-134">Requests read/write permission.</span></span>
    
 <span data-ttu-id="7d9ff-135">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="7d9ff-135">_lpInterface_</span></span>
  
> <span data-ttu-id="7d9ff-136">[entrada] Un puntero para el identificador de interfaz (IID) para iniciar sesión en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-136">[in] A pointer to the interface identifier (IID) for the message store to log on to.</span></span> <span data-ttu-id="7d9ff-137">Paso de NULL indica que se devuelve la interfaz de MAPI para el almacén de mensajes ([IMsgStore](imsgstoreimapiprop.md)).</span><span class="sxs-lookup"><span data-stu-id="7d9ff-137">Passing NULL indicates the MAPI interface for the message store ([IMsgStore](imsgstoreimapiprop.md)) is returned.</span></span> <span data-ttu-id="7d9ff-138">El parámetro _lpInterface_ también se puede establecer en un identificador para una interfaz adecuada para el almacén de mensajes (por ejemplo IID_IUnknown o IID_IMAPIProp).</span><span class="sxs-lookup"><span data-stu-id="7d9ff-138">The  _lpInterface_ parameter can also be set to an identifier for an appropriate interface for the message store (for example IID_IUnknown or IID_IMAPIProp).</span></span> 
    
 <span data-ttu-id="7d9ff-139">_cbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="7d9ff-139">_cbSpoolSecurity_</span></span>
  
> <span data-ttu-id="7d9ff-140">[entrada] Un puntero al tamaño, en bytes, de los datos de validación en el parámetro _lppbSpoolSecurity_ .</span><span class="sxs-lookup"><span data-stu-id="7d9ff-140">[in] A pointer to the size, in bytes, of validation data in the  _lppbSpoolSecurity_ parameter.</span></span> 
    
 <span data-ttu-id="7d9ff-141">_lpbSpoolSecurity_</span><span class="sxs-lookup"><span data-stu-id="7d9ff-141">_lpbSpoolSecurity_</span></span>
  
> <span data-ttu-id="7d9ff-142">[entrada] Un puntero a un puntero a los datos de validación.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-142">[in] A pointer to a pointer to validation data.</span></span> <span data-ttu-id="7d9ff-143">El método **SpoolerLogon** utiliza estos datos para iniciar sesión en el mismo almacén de la cola de MAPI como el proveedor de almacenamiento de mensaje que inició sesión anteriormente en mediante el método [IMSProvider::Logon](imsprovider-logon.md) .</span><span class="sxs-lookup"><span data-stu-id="7d9ff-143">The **SpoolerLogon** method uses this data to log the MAPI spooler on to the same store as the message store provider previously logged on to by using the [IMSProvider::Logon](imsprovider-logon.md) method.</span></span> 
    
 <span data-ttu-id="7d9ff-144">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="7d9ff-144">_lppMAPIError_</span></span>
  
> <span data-ttu-id="7d9ff-145">[out] Un puntero a un puntero a la [MAPIERROR](mapierror.md) estructura devuelta, si lo hay, que contiene información de versión, el componente y el contexto de un error.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-145">[out] A pointer to a pointer to the returned [MAPIERROR](mapierror.md) structure, if any, that contains version, component, and context information for an error.</span></span> <span data-ttu-id="7d9ff-146">El parámetro _lppMAPIError_ se puede establecer en NULL si no hay ninguna estructura **MAPIERROR** para devolver.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-146">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
 <span data-ttu-id="7d9ff-147">_lppMSLogon_</span><span class="sxs-lookup"><span data-stu-id="7d9ff-147">_lppMSLogon_</span></span>
  
> <span data-ttu-id="7d9ff-148">[out] Un puntero al puntero para el mensaje almacena el objeto de inicio de sesión de MAPI iniciar sesión en.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-148">[out] A pointer to the pointer to the message store logon object for MAPI to log on to.</span></span>
    
 <span data-ttu-id="7d9ff-149">_lppMDB_</span><span class="sxs-lookup"><span data-stu-id="7d9ff-149">_lppMDB_</span></span>
  
> <span data-ttu-id="7d9ff-150">[out] Un puntero al puntero para el mensaje almacena el objeto de la cola MAPI y las aplicaciones de cliente para iniciar sesión en.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-150">[out] A pointer to the pointer to the message store object for the MAPI spooler and client applications to log on to.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7d9ff-151">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d9ff-151">Return value</span></span>

<span data-ttu-id="7d9ff-152">S_OK</span><span class="sxs-lookup"><span data-stu-id="7d9ff-152">S_OK</span></span> 
  
> <span data-ttu-id="7d9ff-153">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-153">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="7d9ff-154">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="7d9ff-154">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="7d9ff-155">El perfil no contiene información suficiente para el inicio de sesión para llevar a cabo.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-155">The profile does not contain enough information for the logon to complete.</span></span> <span data-ttu-id="7d9ff-156">Cuando se devuelve este valor, MAPI llama la función de punto de entrada de servicio de mensajes del proveedor de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-156">When this value is returned, MAPI calls the message store provider's message service entry point function.</span></span>
    
<span data-ttu-id="7d9ff-157">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="7d9ff-157">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="7d9ff-158">La llamada se ha realizado correctamente, pero el proveedor de almacén de mensajes tiene información de error disponible.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-158">The call succeeded, but the message store provider has error information available.</span></span> <span data-ttu-id="7d9ff-159">Cuando se devuelve esta advertencia, la llamada se debe controlarse como correcta.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="7d9ff-160">Para probar esta advertencia, utilice la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="7d9ff-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="7d9ff-161">Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="7d9ff-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span> <span data-ttu-id="7d9ff-162">Para obtener la información de error desde el proveedor, llame al método [IMAPISession::GetLastError](imapisession-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="7d9ff-162">To get the error information from the provider, call the [IMAPISession::GetLastError](imapisession-getlasterror.md) method.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7d9ff-163">Notas</span><span class="sxs-lookup"><span data-stu-id="7d9ff-163">Remarks</span></span>

<span data-ttu-id="7d9ff-164">La cola MAPI llama al método de **IMSProvider::SpoolerLogon** para iniciar sesión en un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-164">The MAPI spooler calls the **IMSProvider::SpoolerLogon** method to log on to a message store.</span></span> <span data-ttu-id="7d9ff-165">La cola MAPI debe usar el objeto de almacén de mensaje devuelto por el proveedor de almacén de mensajes en el parámetro _lppMDB_ durante y después de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-165">The MAPI spooler should use the message store object returned by the message store provider in the  _lppMDB_ parameter during and after logon.</span></span> 
  
<span data-ttu-id="7d9ff-166">Para mantener la coherencia con el método [IMSProvider::Logon](imsprovider-logon.md) , el proveedor también devuelve un objeto de inicio de sesión del almacén de mensajes en el parámetro _lppMSLogon_ .</span><span class="sxs-lookup"><span data-stu-id="7d9ff-166">For consistency with the [IMSProvider::Logon](imsprovider-logon.md) method, the provider also returns a message store logon object in the  _lppMSLogon_ parameter.</span></span> <span data-ttu-id="7d9ff-167">El uso del objeto de almacenamiento y el objeto de inicio de sesión son idénticos para inicio de sesión de almacenamiento habitual; debe haber una correspondencia uno a uno entre el objeto de inicio de sesión y el objeto de almacén de manera que los objetos que actúe como si fueran un único objeto que expone dos interfaces.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-167">The use of the store object and the logon object are identical for usual store logon; there should be a one-to-one correspondence between the logon object and the store object such that the objects act as if they are one object that exposes two interfaces.</span></span> <span data-ttu-id="7d9ff-168">Los dos objetos se crean juntos y liberado juntos.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-168">The two objects are created together and freed together.</span></span> 
  
<span data-ttu-id="7d9ff-169">El proveedor de almacenamiento debe marcar internamente el objeto de almacén de mensaje devuelto para indicar que se está utilizando el almacén de la cola de MAPI.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-169">The store provider should internally mark the returned message store object to indicate that the store is being used by the MAPI spooler.</span></span> <span data-ttu-id="7d9ff-170">Algunos de los métodos de este objeto de almacenamiento se comportan de forma diferente para el mensaje de almacenar el objeto proporcionado a las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-170">Some of the methods for this store object behave differently than for the message store object provided to client applications.</span></span> <span data-ttu-id="7d9ff-171">Mantener esta marca interna es la manera más común de desencadenar el comportamiento específico de la cola de MAPI.</span><span class="sxs-lookup"><span data-stu-id="7d9ff-171">Keeping this internal mark is the most common way of triggering the behavior specific to the MAPI spooler.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7d9ff-172">Ver también</span><span class="sxs-lookup"><span data-stu-id="7d9ff-172">See also</span></span>



[<span data-ttu-id="7d9ff-173">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="7d9ff-173">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="7d9ff-174">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="7d9ff-174">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="7d9ff-175">IMSProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7d9ff-175">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

