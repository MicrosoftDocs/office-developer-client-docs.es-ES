---
title: Uso de CSISyncClient para controlar la memoria caché de documentos de Office (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Obtenga información sobre cómo usar CSISyncClient para controlar la memoria caché de documentos de Office (ODC).
ms.openlocfilehash: ce33063f88492bcd6f9682a4a6431fb36f138d55
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399455"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a><span data-ttu-id="47599-103">Uso de CSISyncClient para controlar la memoria caché de documentos de Office (ODC)</span><span class="sxs-lookup"><span data-stu-id="47599-103">Using CSISyncClient to control the Office Document Cache (ODC)</span></span>

<span data-ttu-id="47599-104">Obtenga información sobre cómo usar CSISyncClient para controlar la memoria caché de documentos de Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="47599-104">Learn how to use CSISyncClient to control the Office Document Cache (ODC).</span></span>
  
<span data-ttu-id="47599-105">CSISyncClient es un servidor COM fuera de proceso (CsiSyncClient.exe) que permite que Microsoft OneDrive controlar el comportamiento de la memoria caché de documentos de Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="47599-105">CSISyncClient is an out-of-proc COM server (CsiSyncClient.exe) that allows Microsoft OneDrive to control the behavior of the Office Document Cache (ODC).</span></span> <span data-ttu-id="47599-106">Por ejemplo, OneDrive puede recurrir a la ODC a través de CSISyncClient para cargar y descargar archivos a y desde los extremos habilitado MS-FSSHTTP.</span><span class="sxs-lookup"><span data-stu-id="47599-106">For example, OneDrive may call upon the ODC via CSISyncClient to upload and download files to and from MS-FSSHTTP enabled endpoints.</span></span> <span data-ttu-id="47599-107">Esto habilita características avanzadas de seguridad de servicio en Office, como las transiciones de co-autoría y perfecta de sin conexión a en línea.</span><span class="sxs-lookup"><span data-stu-id="47599-107">This enables advanced service-backed features in Office, such as co-authoring and seamless transitions from offline to online.</span></span>
  
<span data-ttu-id="47599-108">CsiSyncClient está disponible en el escritorio de Office (x86 y x64).</span><span class="sxs-lookup"><span data-stu-id="47599-108">CsiSyncClient is available in Office Desktop (both x86 and x64).</span></span> <span data-ttu-id="47599-109">Nota: Mientras que las versiones más recientes de Office es posible que se suministran con CsiSyncClient, el proceso se usará para la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="47599-109">Note: While newer versions of Office may ship with CsiSyncClient, the process will be used for backward compatibility only.</span></span> <span data-ttu-id="47599-110">La interfaz de CsiSyncClient y la metodología de controlar la ODC cambiará en futuras versiones de Office.</span><span class="sxs-lookup"><span data-stu-id="47599-110">The CsiSyncClient interface and the methodology of controlling the ODC will change in future versions of Office.</span></span>
  
<span data-ttu-id="47599-111">Actualmente se establece el identificador de clase para responder sólo a OneDrive.</span><span class="sxs-lookup"><span data-stu-id="47599-111">The class ID is currently set to respond only to OneDrive.</span></span>
  
<span data-ttu-id="47599-112">El objeto COM es fácil de usar como servidor COM fuera de proceso y se ejecuta en CsiSyncClient.exe.</span><span class="sxs-lookup"><span data-stu-id="47599-112">The COM object is usable as an out-of-proc COM server and runs in CsiSyncClient.exe.</span></span> <span data-ttu-id="47599-113">Debido a las limitaciones con acceso (que utiliza la ODC), se distribuye con el tipo de bits que se incluye Office en x64 es así Office significa un x64 objeto COM o x86 Office significa un x86 objeto COM.</span><span class="sxs-lookup"><span data-stu-id="47599-113">Due to limitations with Access (which the ODC uses), it ships with the bit type that Office comes in, so x64 Office means an x64 COM object, or x86 Office means an x86 COM object.</span></span> <span data-ttu-id="47599-114">Para evitar esta limitación, especificar CLSCTX_LOCAL_SERVER como parte de la CoCreateInstance tendrá el objeto COM se hospeda como un servidor de COM fuera de proceso, lo que permite la compatibilidad de bits cruzados.</span><span class="sxs-lookup"><span data-stu-id="47599-114">To get around this limitation, specifying CLSCTX_LOCAL_SERVER as part of the CoCreateInstance will have the COM object be hosted as an out-of-proc COM server, allowing cross-bitness compatibility.</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="47599-115">Interfaces</span><span class="sxs-lookup"><span data-stu-id="47599-115">Interfaces</span></span>

<span data-ttu-id="47599-116">CSISyncClient usa las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="47599-116">CSISyncClient uses the following interfaces.</span></span>
  
### <a name="interface-ilsclocalsyncclient"></a><span data-ttu-id="47599-117">Interfaz ILSCLocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="47599-117">Interface ILSCLocalSyncClient</span></span>

<span data-ttu-id="47599-118">Esto es la interfaz principal que se usa para sincronizar los archivos de Office.</span><span class="sxs-lookup"><span data-stu-id="47599-118">This is the primary interface used to synchronize files in Office.</span></span>
  
- <span data-ttu-id="47599-119">ProgID: Office.LocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="47599-119">ProgID: Office.LocalSyncClient</span></span>
- <span data-ttu-id="47599-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span><span class="sxs-lookup"><span data-stu-id="47599-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span></span>
- <span data-ttu-id="47599-121">Biblioteca de tipos: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span><span class="sxs-lookup"><span data-stu-id="47599-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span></span>
   
<span data-ttu-id="47599-122">Se utiliza el objeto COM que se expone como un servidor fuera de proceso.</span><span class="sxs-lookup"><span data-stu-id="47599-122">The COM object that is exposed is used as an out-of-proc server.</span></span> <span data-ttu-id="47599-123">Especificar CLSCTX_LOCAL_SERVER como parte de CoCreateInstance permite la compatibilidad entre los procesos de 32 bits y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="47599-123">Specifying CLSCTX_LOCAL_SERVER as part of CoCreateInstance allows compatability between 64bit and 32bit processes.</span></span>
  
<span data-ttu-id="47599-124">Una vez co-autoría que ha creado el objeto COM, se debe llamar a [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) .</span><span class="sxs-lookup"><span data-stu-id="47599-124">Once you've co-created the COM object, you MUST call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) first.</span></span> <span data-ttu-id="47599-125">Una vez [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) haya finalizado correctamente, se puede llamar a cualquier API tantas veces como desee y en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="47599-125">Once [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has completed successfully, you may call any API as often as you wish and in any order.</span></span> <span data-ttu-id="47599-126">También puede llamar a [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) en un objeto ya inicializado, pero esto no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="47599-126">You may also call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) on an already initialized object, but this does nothing.</span></span> 
  
<span data-ttu-id="47599-127">Las excepciones al párrafo anterior son [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) y [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="47599-127">The exceptions to the previous paragraph are [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) and [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="47599-128">Después de llamar a [ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) en el objeto COM, debe destruir ese objeto y crear una nueva.</span><span class="sxs-lookup"><span data-stu-id="47599-128">After you call [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) on the COM object, you MUST destroy that object and create a new one.</span></span> <span data-ttu-id="47599-129">[ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) eliminar su subcache, eliminar toda la información de archivo asociado en la memoria caché, pero dejar los documentos en el disco.</span><span class="sxs-lookup"><span data-stu-id="47599-129">[ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) will delete your subcache, delete all associated file information in the cache, but leave the documents on disk.</span></span> <span data-ttu-id="47599-130">También deja intacta para comunicarse con la memoria caché el estado.</span><span class="sxs-lookup"><span data-stu-id="47599-130">It also leaves the state intact for communicating with the cache.</span></span> <span data-ttu-id="47599-131">Esto le permite llamar a [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) nuevo para crear una nueva memoria caché sin tener que destruir y volver a crear el objeto COM.</span><span class="sxs-lookup"><span data-stu-id="47599-131">This allows you to call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) again to create a new cache without having to destroy and recreate the COM object.</span></span> 
  
<span data-ttu-id="47599-132">**Funciones miembro públicas**</span><span class="sxs-lookup"><span data-stu-id="47599-132">**Public member functions**</span></span>

#### <a name="ilsclocalsyncclientdeletefile"></a><span data-ttu-id="47599-133">ILSCLocalSyncClient::DeleteFile</span><span class="sxs-lookup"><span data-stu-id="47599-133">ILSCLocalSyncClient::DeleteFile</span></span>

<span data-ttu-id="47599-134">DeleteFile se usa para quitar la información del archivo de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="47599-134">DeleteFile is used to remove the file information from the cache.</span></span> <span data-ttu-id="47599-135">Sin embargo, este método para dejar el archivo asociado en el disco y en el servidor.</span><span class="sxs-lookup"><span data-stu-id="47599-135">However, this method will leave the associated file on disk and on the server.</span></span>
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="47599-136">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-136">Parameters</span></span>

 <span data-ttu-id="47599-137">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="47599-137">_bstrResourceID_</span></span>
  
<span data-ttu-id="47599-138">La cadena que identifica el ResourceID del archivo.</span><span class="sxs-lookup"><span data-stu-id="47599-138">The string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="47599-139">Este valor debe ser no vacía con un máximo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="47599-139">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="47599-140">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-140">Return values</span></span>

|<span data-ttu-id="47599-141">Valor</span><span class="sxs-lookup"><span data-stu-id="47599-141">Value</span></span>|<span data-ttu-id="47599-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="47599-142">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="47599-143">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="47599-143">E_FAIL</span></span>  <br/> |<span data-ttu-id="47599-144">La llamada ha fallado.</span><span class="sxs-lookup"><span data-stu-id="47599-144">The call failed.</span></span>  <br/> |
|<span data-ttu-id="47599-145">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="47599-145">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="47599-146">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="47599-146">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="47599-147">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="47599-147">E_FAIL</span></span>  <br/> |<span data-ttu-id="47599-148">La llamada ha fallado.</span><span class="sxs-lookup"><span data-stu-id="47599-148">The call failed.</span></span>  <br/> |
|<span data-ttu-id="47599-149">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="47599-149">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="47599-150">El ResourceID determinado no está en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="47599-150">The given ResourceID is not in the cache.</span></span>  <br/> |
|<span data-ttu-id="47599-151">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="47599-151">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="47599-152">Initialize no se ha llamado correctamente en el pasado.</span><span class="sxs-lookup"><span data-stu-id="47599-152">Initialize has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="47599-153">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="47599-153">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="47599-154">El archivo se está sincronizando o abrir y no se puede eliminar.</span><span class="sxs-lookup"><span data-stu-id="47599-154">The file is currently synchronizing or open and cannot be deleted.</span></span>  <br/> |
|<span data-ttu-id="47599-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="47599-155">S_OK</span></span>  <br/> |<span data-ttu-id="47599-156">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="47599-156">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a><span data-ttu-id="47599-157">ILSCLocalSyncClient::GetChanges</span><span class="sxs-lookup"><span data-stu-id="47599-157">ILSCLocalSyncClient::GetChanges</span></span>
<span data-ttu-id="47599-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span><span class="sxs-lookup"><span data-stu-id="47599-158"></span></span>

<span data-ttu-id="47599-159">GetChanges devuelve un enumerador de objetos de ILSCEvent y también devuelve un token que se asignó a la siguiente llamada para GetChanges, suponiendo que el consumidor ha procesado el conjunto de eventos anterior.</span><span class="sxs-lookup"><span data-stu-id="47599-159">GetChanges returns an enumerator of ILSCEvent objects, and also returns a token that is given to the next call to GetChanges, assuming the consumer has processed the previous set of events.</span></span> <span data-ttu-id="47599-160">Eventos antes de que el _nPreviousChangesToken_ especificado será eliminado y no está disponible.</span><span class="sxs-lookup"><span data-stu-id="47599-160">Events before the  _nPreviousChangesToken_ specified will be deleted and unavailable.</span></span> <span data-ttu-id="47599-161">Si no hay ningún evento que va a procesar, _pnCurrentChangesToken_ debe ser el mismo valor que _nPreviousChangesToken_, pero aún se establecerá _ppiEvents_ .</span><span class="sxs-lookup"><span data-stu-id="47599-161">If there are no events to be processed,  _pnCurrentChangesToken_ should be the same value as  _nPreviousChangesToken_, but  _ppiEvents_ will still be set.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a><span data-ttu-id="47599-162">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-162">Parameters</span></span>

 <span data-ttu-id="47599-163">_nPreviousChangesToken_</span><span class="sxs-lookup"><span data-stu-id="47599-163">_nPreviousChangesToken_</span></span>
  
<span data-ttu-id="47599-164">Identifica el evento que se procesó por última vez por el consumidor.</span><span class="sxs-lookup"><span data-stu-id="47599-164">Identifies which event was last processed by the consumer.</span></span> 
  
 <span data-ttu-id="47599-165">_pnCurrentChangesToken_</span><span class="sxs-lookup"><span data-stu-id="47599-165">_pnCurrentChangesToken_</span></span>
  
<span data-ttu-id="47599-166">Identifica el evento más reciente que se pasa al consumidor.</span><span class="sxs-lookup"><span data-stu-id="47599-166">Identifies the most recent event being handed to the consumer.</span></span> <span data-ttu-id="47599-167">No debe ser null.</span><span class="sxs-lookup"><span data-stu-id="47599-167">Must not be null.</span></span>
  
 <span data-ttu-id="47599-168">_ppiEvents_</span><span class="sxs-lookup"><span data-stu-id="47599-168">_ppiEvents_</span></span>
  
<span data-ttu-id="47599-169">Enumerador para los eventos que se pasa al consumidor.</span><span class="sxs-lookup"><span data-stu-id="47599-169">An enumerator for the events handed to the consumer.</span></span> <span data-ttu-id="47599-170">No debe ser null.</span><span class="sxs-lookup"><span data-stu-id="47599-170">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="47599-171">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-171">Return values</span></span>

|<span data-ttu-id="47599-172">Valor</span><span class="sxs-lookup"><span data-stu-id="47599-172">Value</span></span>|<span data-ttu-id="47599-173">Descripción</span><span class="sxs-lookup"><span data-stu-id="47599-173">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="47599-174">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="47599-174">E_FAIL</span></span>  <br/> |<span data-ttu-id="47599-175">La llamada ha fallado.</span><span class="sxs-lookup"><span data-stu-id="47599-175">The call failed.</span></span>  <br/> |
|<span data-ttu-id="47599-176">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="47599-176">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="47599-177">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="47599-177">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="47599-178">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="47599-178">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="47599-179">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.</span><span class="sxs-lookup"><span data-stu-id="47599-179">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="47599-180">S_OK</span><span class="sxs-lookup"><span data-stu-id="47599-180">S_OK</span></span>  <br/> |<span data-ttu-id="47599-181">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="47599-181">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a><span data-ttu-id="47599-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="47599-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span></span>

<span data-ttu-id="47599-183">GetClientNetworkSyncPermission se utiliza para consultar si heurística de sincronización de la oficina para el costo de red y se reemplaza el uso de la energía.</span><span class="sxs-lookup"><span data-stu-id="47599-183">GetClientNetworkSyncPermission is used to query whether Office's synchronizing heuristics for network cost and power usage are overridden.</span></span> <span data-ttu-id="47599-184">Cuando en una 3G u otra red de alto costo, o cuando se ejecuta en batería frente a que se conecta, Office puede elegir esta opción Bloquear el tráfico de red hasta un momento más oportuno.</span><span class="sxs-lookup"><span data-stu-id="47599-184">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span>
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a><span data-ttu-id="47599-185">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-185">Parameters</span></span>

 <span data-ttu-id="47599-186">_nspType_</span><span class="sxs-lookup"><span data-stu-id="47599-186">_nspType_</span></span>
  
<span data-ttu-id="47599-187">Marca que define qué heurística de costo a la consulta.</span><span class="sxs-lookup"><span data-stu-id="47599-187">A flag which defines which cost heuristic to query.</span></span> <span data-ttu-id="47599-188">Vea la [Enumeración LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="47599-188">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span> 
  
 <span data-ttu-id="47599-189">_pfSyncEnabled_</span><span class="sxs-lookup"><span data-stu-id="47599-189">_pfSyncEnabled_</span></span>
  
<span data-ttu-id="47599-190">Especifica si la heurística de costo solicitado actualmente se reemplaza o no.</span><span class="sxs-lookup"><span data-stu-id="47599-190">Specifies whether the requested cost heuristic is currently overridden or not.</span></span> <span data-ttu-id="47599-191">No debe ser null.</span><span class="sxs-lookup"><span data-stu-id="47599-191">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="47599-192">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-192">Return values</span></span>

|<span data-ttu-id="47599-193">Valor</span><span class="sxs-lookup"><span data-stu-id="47599-193">Value</span></span>|<span data-ttu-id="47599-194">Descripción</span><span class="sxs-lookup"><span data-stu-id="47599-194">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="47599-195">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="47599-195">E_FAIL</span></span>  <br/> |<span data-ttu-id="47599-196">La llamada ha fallado.</span><span class="sxs-lookup"><span data-stu-id="47599-196">The call failed.</span></span>  <br/> |
|<span data-ttu-id="47599-197">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="47599-197">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="47599-198">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="47599-198">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="47599-199">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="47599-199">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="47599-200">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.</span><span class="sxs-lookup"><span data-stu-id="47599-200">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="47599-201">S_OK</span><span class="sxs-lookup"><span data-stu-id="47599-201">S_OK</span></span>  <br/> |<span data-ttu-id="47599-202">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="47599-202">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a><span data-ttu-id="47599-203">ILSCLocalSyncClient::GetFileStatus</span><span class="sxs-lookup"><span data-stu-id="47599-203">ILSCLocalSyncClient::GetFileStatus</span></span>

<span data-ttu-id="47599-204">GetFileStatus se usa para recopilar información para un archivo específico: si existe en la memoria caché, si tiene pendientes de comunicación con la copia del servidor y, si tiene Office 2013 más hasta los datos de fecha de la copia local.</span><span class="sxs-lookup"><span data-stu-id="47599-204">GetFileStatus is used to gather information for a specific file: whether it exists in the cache, if it has pending communication with the server copy, and if Office 2013 has the most up to date data from the local copy.</span></span> <span data-ttu-id="47599-205">Requiere un indicador de bit a bit de los valores de [Enumeración LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) para determinar qué información es el objeto COM CsiSyncClient de consulta para.</span><span class="sxs-lookup"><span data-stu-id="47599-205">It requires a bitwise flag of [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) values to determine what information the CsiSyncClient COM object is to query for.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a><span data-ttu-id="47599-206">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-206">Parameters</span></span>

 <span data-ttu-id="47599-207">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="47599-207">_bstrResourceID_</span></span>
  
<span data-ttu-id="47599-208">La cadena que identifica el archivo en el cliente.</span><span class="sxs-lookup"><span data-stu-id="47599-208">The string which identifies the file on the client.</span></span> <span data-ttu-id="47599-209">Este valor debe ser no vacías, con un máximo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="47599-209">This value must be non-empty, with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="47599-210">_sfRequestedStatus_</span><span class="sxs-lookup"><span data-stu-id="47599-210">_sfRequestedStatus_</span></span>
  
<span data-ttu-id="47599-211">Marca que define la información que debe devolver.</span><span class="sxs-lookup"><span data-stu-id="47599-211">A flag which defines what information to return.</span></span> <span data-ttu-id="47599-212">Vea la [Enumeración LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="47599-212">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
 <span data-ttu-id="47599-213">_pbstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="47599-213">_pbstrFileSystemPath_</span></span>
  
<span data-ttu-id="47599-214">La cadena que identifica la ubicación del archivo identificado por _bstrResourceID_ en el cliente.</span><span class="sxs-lookup"><span data-stu-id="47599-214">The string which identifies the location of the file identified by  _bstrResourceID_ on the client.</span></span> <span data-ttu-id="47599-215">No debe ser null.</span><span class="sxs-lookup"><span data-stu-id="47599-215">Must not be null.</span></span> 
  
 <span data-ttu-id="47599-216">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="47599-216">_pbstrETag_</span></span>
  
<span data-ttu-id="47599-217">Una cadena que va a contener el valor eTag para el archivo identificado por _bstrResourceID_.</span><span class="sxs-lookup"><span data-stu-id="47599-217">A string which will contain the eTag for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="47599-218">No debe ser null.</span><span class="sxs-lookup"><span data-stu-id="47599-218">Must not be null.</span></span> 
  
 <span data-ttu-id="47599-219">_psfFileStatus_</span><span class="sxs-lookup"><span data-stu-id="47599-219">_psfFileStatus_</span></span>
  
<span data-ttu-id="47599-220">Marca que contendrá el estado solicitado a través de _sfRequestedStatus_ para el archivo identificado por _bstrResourceID_.</span><span class="sxs-lookup"><span data-stu-id="47599-220">A flag which will contain the status requested via  _sfRequestedStatus_ for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="47599-221">No debe ser null.</span><span class="sxs-lookup"><span data-stu-id="47599-221">Must not be null.</span></span> <span data-ttu-id="47599-222">Vea la [Enumeración LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="47599-222">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="47599-223">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-223">Return values</span></span>

|<span data-ttu-id="47599-224">Valor</span><span class="sxs-lookup"><span data-stu-id="47599-224">Value</span></span>|<span data-ttu-id="47599-225">Descripción</span><span class="sxs-lookup"><span data-stu-id="47599-225">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="47599-226">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="47599-226">E_FAIL</span></span>  <br/> |<span data-ttu-id="47599-227">La llamada ha fallado.</span><span class="sxs-lookup"><span data-stu-id="47599-227">The call failed.</span></span>  <br/> |
|<span data-ttu-id="47599-228">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="47599-228">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="47599-229">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="47599-229">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="47599-230">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="47599-230">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="47599-231">La información del archivo especificada por _bstrResourceID_ no existe en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="47599-231">The file information specified by  _bstrResourceID_ does not exist in the cache.</span></span>  <br/> |
|<span data-ttu-id="47599-232">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="47599-232">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="47599-233">Se ha solicitado LSCStatusFlag_LocalFileUnchanged o el archivo especificado por _bstrResourceID_ está bloqueado o que faltan.</span><span class="sxs-lookup"><span data-stu-id="47599-233">LSCStatusFlag_LocalFileUnchanged was requested or the file specified by  _bstrResourceID_ is locked or missing.</span></span>  <br/> |
|<span data-ttu-id="47599-234">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="47599-234">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="47599-235">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.</span><span class="sxs-lookup"><span data-stu-id="47599-235">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="47599-236">S_OK</span><span class="sxs-lookup"><span data-stu-id="47599-236">S_OK</span></span>  <br/> |<span data-ttu-id="47599-237">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="47599-237">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a><span data-ttu-id="47599-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="47599-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span></span>
<span data-ttu-id="47599-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span><span class="sxs-lookup"><span data-stu-id="47599-239"></span></span>

<span data-ttu-id="47599-240">GetSupportedFileExtensions devuelve una lista delimitada de extensiones de archivo que son compatibles actualmente con el objeto COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="47599-240">GetSupportedFileExtensions returns a list of pipe-delimited file extensions which are currently supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="47599-241">Tenga en cuenta que esta lista puede cambiar, y el consumidor recibirá una notificación de un cambio a través del objeto IPartnerActivityCallback proporcionado en [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (vea EventOccured).</span><span class="sxs-lookup"><span data-stu-id="47599-241">Note that this list may change, and the consumer will be notified of a change via the IPartnerActivityCallback object provided on [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (See EventOccured).</span></span> 
  
<span data-ttu-id="47599-242">Un ejemplo de la cadena devuelta es como sigue: "| docx | docm | pptx |"</span><span class="sxs-lookup"><span data-stu-id="47599-242">An example of the string returned is as follows: "|docx|docm|pptx|"</span></span>
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a><span data-ttu-id="47599-243">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-243">Parameters</span></span>

 <span data-ttu-id="47599-244">_pbstrSupportedFileExtensions_</span><span class="sxs-lookup"><span data-stu-id="47599-244">_pbstrSupportedFileExtensions_</span></span>
  
<span data-ttu-id="47599-245">Una cadena que se va a establecer con un conjunto delimitado por canalización de extensiones de archivo admitidas por el objeto COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="47599-245">A string to be set with a pipe-delimited set of file extensions supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="47599-246">No debe ser null.</span><span class="sxs-lookup"><span data-stu-id="47599-246">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="47599-247">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-247">Return values</span></span>

|<span data-ttu-id="47599-248">Valor</span><span class="sxs-lookup"><span data-stu-id="47599-248">Value</span></span>|<span data-ttu-id="47599-249">Descripción</span><span class="sxs-lookup"><span data-stu-id="47599-249">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="47599-250">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="47599-250">E_FAIL</span></span>  <br/> |<span data-ttu-id="47599-251">La llamada ha fallado.</span><span class="sxs-lookup"><span data-stu-id="47599-251">The call failed.</span></span>  <br/> |
|<span data-ttu-id="47599-252">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="47599-252">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="47599-253">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="47599-253">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="47599-254">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="47599-254">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="47599-255">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.</span><span class="sxs-lookup"><span data-stu-id="47599-255">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="47599-256">S_OK</span><span class="sxs-lookup"><span data-stu-id="47599-256">S_OK</span></span>  <br/> |<span data-ttu-id="47599-257">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="47599-257">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a><span data-ttu-id="47599-258">ILSCLocalSyncClient::Initialize</span><span class="sxs-lookup"><span data-stu-id="47599-258">ILSCLocalSyncClient::Initialize</span></span>
<span data-ttu-id="47599-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span><span class="sxs-lookup"><span data-stu-id="47599-259"></span></span>

<span data-ttu-id="47599-260">Initialize debe ser el primer método que se llama.</span><span class="sxs-lookup"><span data-stu-id="47599-260">Initialize must be the first method called.</span></span> <span data-ttu-id="47599-261">De lo contrario, todas las otras API devolverá E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="47599-261">Otherwise, all other APIs will return E_LSC_NOTINITIALIZED.</span></span> <span data-ttu-id="47599-262">Al llamar a Initialize en un objeto ya inicializado devuelve S_OK y no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="47599-262">Calling Initialize on an already initialized object returns S_OK and does nothing.</span></span> <span data-ttu-id="47599-263">Si se devuelve E_LSC_CACHEMISMATCH, el llamador puede llamar a [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) para eliminar la memoria caché asociada con el SuppliedID determinado.</span><span class="sxs-lookup"><span data-stu-id="47599-263">If E_LSC_CACHEMISMATCH is returned, the caller may call [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) to delete the cache associated with the given SuppliedID.</span></span> <span data-ttu-id="47599-264">Sin embargo, en este caso otras API devolverá E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="47599-264">However, in this case other APIs will still return E_LSC_NOTINITIALIZED.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a><span data-ttu-id="47599-265">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-265">Parameters</span></span>

 <span data-ttu-id="47599-266">_bstrSuppliedID_</span><span class="sxs-lookup"><span data-stu-id="47599-266">_bstrSuppliedID_</span></span>
  
<span data-ttu-id="47599-267">Identifica el consumidor y que la memoria caché para usar.</span><span class="sxs-lookup"><span data-stu-id="47599-267">Identifies the consumer and which cache to use.</span></span> <span data-ttu-id="47599-268">Debe ser no vacía con un máximo de 32 caracteres.</span><span class="sxs-lookup"><span data-stu-id="47599-268">Must be non-empty with a maximum of 32 characters.</span></span> 
  
 <span data-ttu-id="47599-269">_bstrProgID_</span><span class="sxs-lookup"><span data-stu-id="47599-269">_bstrProgID_</span></span>
  
<span data-ttu-id="47599-270">Identifica el objeto de COM del consumidor para la comunicación bidireccional.</span><span class="sxs-lookup"><span data-stu-id="47599-270">Identifies the consumer's COM object for two-way communication.</span></span> <span data-ttu-id="47599-271">Debe ser no vacía con un máximo de 39 caracteres.</span><span class="sxs-lookup"><span data-stu-id="47599-271">Must be non-empty with a maximum of 39 characters.</span></span> <span data-ttu-id="47599-272">Vea [ \<ProgID\> clave](https://docs.microsoft.com/windows/desktop/com/-progid--key) para obtener más información acerca de ProgIDs.</span><span class="sxs-lookup"><span data-stu-id="47599-272">See [\<ProgID\> Key](https://docs.microsoft.com/windows/desktop/com/-progid--key) for more information about ProgIDs.</span></span> 
  
 <span data-ttu-id="47599-273">_bstrFileSystemDirectoryHint_</span><span class="sxs-lookup"><span data-stu-id="47599-273">_bstrFileSystemDirectoryHint_</span></span>
  
<span data-ttu-id="47599-274">Identifica la raíz del directorio en el que se almacenarán los archivos locales.</span><span class="sxs-lookup"><span data-stu-id="47599-274">Identifies the directory root in which local files will be stored.</span></span> <span data-ttu-id="47599-275">Debe ser no vacía con un máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="47599-275">Must be non-empty with a maximum of 256 characters.</span></span> <span data-ttu-id="47599-276">El directorio ya debe existir.</span><span class="sxs-lookup"><span data-stu-id="47599-276">The directory must already exist.</span></span> 
  
 <span data-ttu-id="47599-277">_pEventCallback_</span><span class="sxs-lookup"><span data-stu-id="47599-277">_pEventCallback_</span></span>
  
<span data-ttu-id="47599-278">La interfaz de devolución de llamada que le notificará CsiSyncClient en los cambios.</span><span class="sxs-lookup"><span data-stu-id="47599-278">The callback interface which CsiSyncClient will notify on changes.</span></span> <span data-ttu-id="47599-279">Vea IPartnerActivityCallback::EventOccurred.</span><span class="sxs-lookup"><span data-stu-id="47599-279">See IPartnerActivityCallback::EventOccurred.</span></span> <span data-ttu-id="47599-280">Este valor no debe ser null.</span><span class="sxs-lookup"><span data-stu-id="47599-280">This value must not be null.</span></span> 
  
 <span data-ttu-id="47599-281">_pfCreatedNewCache_</span><span class="sxs-lookup"><span data-stu-id="47599-281">_pfCreatedNewCache_</span></span>
  
<span data-ttu-id="47599-282">Devuelve si se ha creado una nueva memoria caché.</span><span class="sxs-lookup"><span data-stu-id="47599-282">Returns whether a new cache was created.</span></span> <span data-ttu-id="47599-283">Si no hay memoria caché está asociada con la SuppliedID, se creará uno.</span><span class="sxs-lookup"><span data-stu-id="47599-283">If no cache is associated with the SuppliedID, one will be created.</span></span> <span data-ttu-id="47599-284">Este valor no debe ser null.</span><span class="sxs-lookup"><span data-stu-id="47599-284">This value must not be null.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="47599-285">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-285">Return values</span></span>

|<span data-ttu-id="47599-286">Valor</span><span class="sxs-lookup"><span data-stu-id="47599-286">Value</span></span>|<span data-ttu-id="47599-287">Descripción</span><span class="sxs-lookup"><span data-stu-id="47599-287">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="47599-288">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="47599-288">E_FAIL</span></span>  <br/> |<span data-ttu-id="47599-289">La llamada ha fallado.</span><span class="sxs-lookup"><span data-stu-id="47599-289">The call failed.</span></span>  <br/> |
|<span data-ttu-id="47599-290">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="47599-290">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="47599-291">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="47599-291">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="47599-292">E_LSC_CACHEMISMATCH</span><span class="sxs-lookup"><span data-stu-id="47599-292">E_LSC_CACHEMISMATCH</span></span>  <br/> |<span data-ttu-id="47599-293">Un SuppliedID ya tiene una memoria caché asociada, pero tiene un ProgId o FileSystemDirectoryHint diferentes a los archivos proporcionados.</span><span class="sxs-lookup"><span data-stu-id="47599-293">A SuppliedID already has a cache associated with it, but has a different ProgId or FileSystemDirectoryHint than the ones provided.</span></span>  <br/> |
|<span data-ttu-id="47599-294">E_LSC_DIRECTORYHINTCONFLICT</span><span class="sxs-lookup"><span data-stu-id="47599-294">E_LSC_DIRECTORYHINTCONFLICT</span></span>  <br/> |<span data-ttu-id="47599-295">El FileSystemDirectoryHint (o en una subcarpeta) ya existe en una caché diferente.</span><span class="sxs-lookup"><span data-stu-id="47599-295">The FileSystemDirectoryHint (or a subfolder) already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="47599-296">E_LAC_PROGIDCONFLICT</span><span class="sxs-lookup"><span data-stu-id="47599-296">E_LAC_PROGIDCONFLICT</span></span>  <br/> |<span data-ttu-id="47599-297">El ProgID ya existe en una caché diferente.</span><span class="sxs-lookup"><span data-stu-id="47599-297">The ProgID already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="47599-298">S_OK</span><span class="sxs-lookup"><span data-stu-id="47599-298">S_OK</span></span>  <br/> |<span data-ttu-id="47599-299">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="47599-299">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a><span data-ttu-id="47599-300">ILSCLocalSyncClient::LocalFileChange</span><span class="sxs-lookup"><span data-stu-id="47599-300">ILSCLocalSyncClient::LocalFileChange</span></span>
<span data-ttu-id="47599-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="47599-301"></span></span>

<span data-ttu-id="47599-302">LocalFileChange se usa para indicar el objeto COM CsiSyncClient para intentar cargar el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="47599-302">LocalFileChange is used to tell the CsiSyncClient COM object to attempt to upload the specified file.</span></span> <span data-ttu-id="47599-303">El método preparará el archivo para cargar, incluida la lectura del contenido del archivo actual.</span><span class="sxs-lookup"><span data-stu-id="47599-303">The method will prepare the file for upload, including reading the file's current contents.</span></span> <span data-ttu-id="47599-304">Si una carga ya está pendiente, se descartará la carga anterior y el nuevo contenido preparado para carga.</span><span class="sxs-lookup"><span data-stu-id="47599-304">If an upload is already pending, the previous upload will be discarded and the new contents prepared for upload.</span></span> <span data-ttu-id="47599-305">Si el archivo está abierto para su edición en una aplicación, este método devuelve S_OK sin preparar el archivo de carga (debe hacer la aplicación ya este paso si hay cambios).</span><span class="sxs-lookup"><span data-stu-id="47599-305">If the file is open for editing in an application, this method will return S_OK without preparing the file for upload (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="47599-306">Este método le permitirá cargas si se marcó como carga bloqueados anteriormente (vea [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span><span class="sxs-lookup"><span data-stu-id="47599-306">This method will allow uploads if it was marked as uploads blocked previously (see [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span></span>
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="47599-307">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-307">Parameters</span></span>

 <span data-ttu-id="47599-308">_bstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="47599-308">_bstrFileSystemPath_</span></span>
  
<span data-ttu-id="47599-309">Una cadena que identifica el archivo en el cliente.</span><span class="sxs-lookup"><span data-stu-id="47599-309">A string which identifies the file on the client.</span></span> <span data-ttu-id="47599-310">Este valor debe ser una ruta de acceso local no vacía con un máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="47599-310">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="47599-311">Esta ruta de acceso debe estar en el árbol del directorio especificado por la FileSystemDirectoryHint cuando se realizó la llamada a [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) .</span><span class="sxs-lookup"><span data-stu-id="47599-311">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was made.</span></span> 
  
 <span data-ttu-id="47599-312">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="47599-312">_bstrResourceID_</span></span>
  
<span data-ttu-id="47599-313">Una cadena que identifica el ResourceID del archivo.</span><span class="sxs-lookup"><span data-stu-id="47599-313">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="47599-314">Este valor debe ser no vacía con un máximo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="47599-314">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="47599-315">_bstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="47599-315">_bstrWebPath_</span></span>
  
<span data-ttu-id="47599-316">Una cadena que identifica el archivo en el servidor.</span><span class="sxs-lookup"><span data-stu-id="47599-316">A string which identifies the file on the server.</span></span> <span data-ttu-id="47599-317">Este valor debe ser la dirección URL no vacía, válido, pero no puede superar los INTERNET_MAX_URL_LENGTH, tal como se define por https://support.microsoft.com/kb/208427.</span><span class="sxs-lookup"><span data-stu-id="47599-317">This value must be non-empty, valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="47599-318">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-318">Return values</span></span>

|<span data-ttu-id="47599-319">Valor</span><span class="sxs-lookup"><span data-stu-id="47599-319">Value</span></span>|<span data-ttu-id="47599-320">Descripción</span><span class="sxs-lookup"><span data-stu-id="47599-320">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="47599-321">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="47599-321">E_FAIL</span></span>  <br/> |<span data-ttu-id="47599-322">La llamada ha fallado.</span><span class="sxs-lookup"><span data-stu-id="47599-322">The call failed.</span></span>  <br/> |
|<span data-ttu-id="47599-323">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="47599-323">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="47599-324">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="47599-324">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="47599-325">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="47599-325">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="47599-326">El archivo especificado por _bstrFileSystemPath_ tiene un ResourceID diferente del especificado.</span><span class="sxs-lookup"><span data-stu-id="47599-326">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span> <span data-ttu-id="47599-327">Un evento de tipo LSCEventType_OnFilePathConflict se envía cuando se devuelve este error.</span><span class="sxs-lookup"><span data-stu-id="47599-327">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="47599-328">Vea [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="47599-328">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="47599-329">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="47599-329">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="47599-330">El archivo fue eliminado operación intermedio.</span><span class="sxs-lookup"><span data-stu-id="47599-330">The file was deleted mid-operation.</span></span>  <br/> |
|<span data-ttu-id="47599-331">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="47599-331">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="47599-332">No se admite la extensión de archivo determinada por el objeto COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="47599-332">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="47599-333">Vea [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span><span class="sxs-lookup"><span data-stu-id="47599-333">See [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span></span>  <br/> |
|<span data-ttu-id="47599-334">E_LSC_FILEUPTODATE</span><span class="sxs-lookup"><span data-stu-id="47599-334">E_LSC_FILEUPTODATE</span></span>  <br/> |<span data-ttu-id="47599-335">El objeto COM no ha programado una carga debido a que el archivo en la memoria caché tenía los cambios más recientes desde el disco.</span><span class="sxs-lookup"><span data-stu-id="47599-335">The COM object did not schedule an upload because the file in the cache had the most recent changes from the disk.</span></span>  <br/> |
|<span data-ttu-id="47599-336">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="47599-336">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="47599-337">El archivo especificado por _bstrFileSystemPath_ falta o está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="47599-337">The file specified by  _bstrFileSystemPath_ is missing or locked.</span></span>  <br/> |
|<span data-ttu-id="47599-338">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="47599-338">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="47599-339">El FileSystemPath determinado no está bajo la raíz del directorio especificada por la FileSystemDirectoryHint cuando se realizó la llamada a Initialize.</span><span class="sxs-lookup"><span data-stu-id="47599-339">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="47599-340">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="47599-340">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="47599-341">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.</span><span class="sxs-lookup"><span data-stu-id="47599-341">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="47599-342">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="47599-342">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="47599-343">El archivo especificado por _bstrResourceID_ tiene un FileSystemPath diferente del especificado.</span><span class="sxs-lookup"><span data-stu-id="47599-343">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="47599-344">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="47599-344">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="47599-345">El archivo especificado ya tiene cambios pendientes en una caché diferente y aún no se puede asociar con la memoria caché del consumidor.</span><span class="sxs-lookup"><span data-stu-id="47599-345">The file specified already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="47599-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="47599-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="47599-347">El WebPath proporcionado entra en una caché diferente.</span><span class="sxs-lookup"><span data-stu-id="47599-347">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="47599-348">S_OK</span><span class="sxs-lookup"><span data-stu-id="47599-348">S_OK</span></span>  <br/> |<span data-ttu-id="47599-349">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="47599-349">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a><span data-ttu-id="47599-350">ILSCLocalSyncClient::RenameFile</span><span class="sxs-lookup"><span data-stu-id="47599-350">ILSCLocalSyncClient::RenameFile</span></span>
<span data-ttu-id="47599-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span><span class="sxs-lookup"><span data-stu-id="47599-351"></span></span>

<span data-ttu-id="47599-352">RenameFile asocie una nueva dirección URL y la ruta de acceso local para un determinado ResourceID.</span><span class="sxs-lookup"><span data-stu-id="47599-352">RenameFile will associate a new URL and local path for a given ResourceID.</span></span> <span data-ttu-id="47599-353">Si el archivo especificado por el ResourceID ya no existe en la memoria caché, un intento de estarán para crearla y marcar para su descarga.</span><span class="sxs-lookup"><span data-stu-id="47599-353">If the file specified by the ResourceID doesn't already exist in the cache, an attempt will be made to create it and mark it for download.</span></span>
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a><span data-ttu-id="47599-354">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-354">Parameters</span></span>

 <span data-ttu-id="47599-355">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="47599-355">_bstrResourceID_</span></span>
  
<span data-ttu-id="47599-356">Una cadena que identifica el ResourceID del archivo.</span><span class="sxs-lookup"><span data-stu-id="47599-356">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="47599-357">Este valor debe ser no vacía con un máximo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="47599-357">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="47599-358">_bstrNewFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="47599-358">_bstrNewFileSystemPath_</span></span>
  
<span data-ttu-id="47599-359">Una cadena que especifica la nueva ruta de acceso local para el archivo.</span><span class="sxs-lookup"><span data-stu-id="47599-359">A string which specifies the new local path for the file.</span></span> <span data-ttu-id="47599-360">Este valor debe ser una ruta de acceso local no vacía con un máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="47599-360">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="47599-361">Esta ruta de acceso debe estar en el árbol del directorio especificado por la FileSystemDirectoryHint cuando se realizó la llamada a Initialize.</span><span class="sxs-lookup"><span data-stu-id="47599-361">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span> 
  
 <span data-ttu-id="47599-362">_bstrNewWebPath_</span><span class="sxs-lookup"><span data-stu-id="47599-362">_bstrNewWebPath_</span></span>
  
<span data-ttu-id="47599-363">Una cadena que especifica la nueva dirección URL para el archivo.</span><span class="sxs-lookup"><span data-stu-id="47599-363">A string which specifies the new URL for the file.</span></span> <span data-ttu-id="47599-364">Este valor debe ser no vacías dirección URL válida, pero no puede superar los INTERNET_MAX_URL_LENGTH, tal como se define por https://support.microsoft.com/kb/208427.</span><span class="sxs-lookup"><span data-stu-id="47599-364">This value must be non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
 <span data-ttu-id="47599-365">_fBlockUploads_</span><span class="sxs-lookup"><span data-stu-id="47599-365">_fBlockUploads_</span></span>
  
<span data-ttu-id="47599-366">Especifica si se permite la carga en la nueva ubicación actualmente.</span><span class="sxs-lookup"><span data-stu-id="47599-366">Specifies whether uploads to the new location are allowed currently.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="47599-367">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-367">Return values</span></span>

|<span data-ttu-id="47599-368">Valor</span><span class="sxs-lookup"><span data-stu-id="47599-368">Value</span></span>|<span data-ttu-id="47599-369">Descripción</span><span class="sxs-lookup"><span data-stu-id="47599-369">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="47599-370">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="47599-370">E_FAIL</span></span>  <br/> |<span data-ttu-id="47599-371">La llamada ha fallado.</span><span class="sxs-lookup"><span data-stu-id="47599-371">The call failed.</span></span>  <br/> |
|<span data-ttu-id="47599-372">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="47599-372">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="47599-373">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="47599-373">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="47599-374">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="47599-374">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="47599-375">Las _bstrNewFileSystemPath_ o _bstrNewWebPath_ ya existen en otro archivo en cualquier caché.</span><span class="sxs-lookup"><span data-stu-id="47599-375">The  _bstrNewFileSystemPath_ or  _bstrNewWebPath_ already exist on another file in any cache.</span></span> <span data-ttu-id="47599-376">Un evento de tipo LSCEventType_OnFilePathConflict se envía cuando se devuelve este error.</span><span class="sxs-lookup"><span data-stu-id="47599-376">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="47599-377">Vea [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="47599-377">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="47599-378">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="47599-378">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="47599-379">La información del archivo se ha eliminado de la memoria caché mientras se ejecuta este método.</span><span class="sxs-lookup"><span data-stu-id="47599-379">The file information was deleted from the cache while this method was running.</span></span>  <br/> |
|<span data-ttu-id="47599-380">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="47599-380">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="47599-381">El FileSystemPath determinado no está bajo la raíz del directorio especificada por la FileSystemDirectoryHint cuando se realizó la llamada a Initialize.</span><span class="sxs-lookup"><span data-stu-id="47599-381">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="47599-382">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="47599-382">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="47599-383">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.</span><span class="sxs-lookup"><span data-stu-id="47599-383">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="47599-384">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="47599-384">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="47599-385">El archivo especificado se está sincronizando en una aplicación de Office.</span><span class="sxs-lookup"><span data-stu-id="47599-385">The file specified is currently synchronizing in an Office application.</span></span>  <br/> |
|<span data-ttu-id="47599-386">S_OK</span><span class="sxs-lookup"><span data-stu-id="47599-386">S_OK</span></span>  <br/> |<span data-ttu-id="47599-387">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="47599-387">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a><span data-ttu-id="47599-388">ILSCLocalSyncClient::ResetCache</span><span class="sxs-lookup"><span data-stu-id="47599-388">ILSCLocalSyncClient::ResetCache</span></span>
<span data-ttu-id="47599-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span><span class="sxs-lookup"><span data-stu-id="47599-389"></span></span>

<span data-ttu-id="47599-390">ResetCache, se eliminará de la memoria caché asociada con el SuppliedID que le ha proporcionado en Initialize.</span><span class="sxs-lookup"><span data-stu-id="47599-390">ResetCache will delete the cache associated with the SuppliedID that was provided on Initialize.</span></span> <span data-ttu-id="47599-391">Esto incluye toda la información de archivo, pero dejará los archivos en el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="47599-391">This includes all of the file information, but will leave the files on both the client and the server.</span></span> <span data-ttu-id="47599-392">Este método también deja el objeto en un estado parcialmente no inicializado.</span><span class="sxs-lookup"><span data-stu-id="47599-392">This method also leaves the object in a partially uninitialized state.</span></span> <span data-ttu-id="47599-393">Las llamadas sólo es válidas después de esto son [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) o [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="47599-393">The only valid calls after this are [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) or [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="47599-394">Es posible que se llama a este método si Initialize se produce un error y devuelve E_LSC_CACHEMISMATCH y va a eliminar la memoria caché asociada con el SuppliedID que le ha proporcionado con la llamada con errores.</span><span class="sxs-lookup"><span data-stu-id="47599-394">This method MAY be called if Initialize fails and returns E_LSC_CACHEMISMATCH, and will delete the cache associated with the SuppliedID that was provided with the failing call.</span></span>
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a><span data-ttu-id="47599-395">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-395">Parameters</span></span>

<span data-ttu-id="47599-396">Ninguno</span><span class="sxs-lookup"><span data-stu-id="47599-396">None</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="47599-397">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-397">Return values</span></span>

|<span data-ttu-id="47599-398">Valor</span><span class="sxs-lookup"><span data-stu-id="47599-398">Value</span></span>|<span data-ttu-id="47599-399">Descripción</span><span class="sxs-lookup"><span data-stu-id="47599-399">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="47599-400">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="47599-400">E_FAIL</span></span>  <br/> |<span data-ttu-id="47599-401">La llamada ha fallado.</span><span class="sxs-lookup"><span data-stu-id="47599-401">The call failed.</span></span>  <br/> |
|<span data-ttu-id="47599-402">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="47599-402">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="47599-403">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.</span><span class="sxs-lookup"><span data-stu-id="47599-403">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was not successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="47599-404">S_OK</span><span class="sxs-lookup"><span data-stu-id="47599-404">S_OK</span></span>  <br/> |<span data-ttu-id="47599-405">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="47599-405">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a><span data-ttu-id="47599-406">ILSCLocalSyncClient::ServerFileChange</span><span class="sxs-lookup"><span data-stu-id="47599-406">ILSCLocalSyncClient::ServerFileChange</span></span>
<span data-ttu-id="47599-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="47599-407"></span></span>

<span data-ttu-id="47599-408">ServerFileChange indica que el objeto COM CsiSyncClient para marcar el archivo especificado para su descarga.</span><span class="sxs-lookup"><span data-stu-id="47599-408">ServerFileChange tells the CsiSyncClient COM object to mark the specified file for download.</span></span> <span data-ttu-id="47599-409">Si el archivo está abierto en una aplicación de Office para su edición, este método devuelve S_OK sin marcar el archivo para su descarga (la aplicación debe ya realice este paso si hay cambios).</span><span class="sxs-lookup"><span data-stu-id="47599-409">If the file is open in an Office application for edit, this method will return S_OK without marking the file for download (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="47599-410">Este método le permitirá descargas si se marcó como descargas bloqueados anteriormente (vea RenameFile).</span><span class="sxs-lookup"><span data-stu-id="47599-410">This method will allow downloads if it was marked as downloads blocked previously (see RenameFile).</span></span>
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="47599-411">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-411">Parameters</span></span>

|<span data-ttu-id="47599-412">Parámetro</span><span class="sxs-lookup"><span data-stu-id="47599-412">Parameter</span></span>|<span data-ttu-id="47599-413">Descripción</span><span class="sxs-lookup"><span data-stu-id="47599-413">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="47599-414">bstrFileSystemPath</span><span class="sxs-lookup"><span data-stu-id="47599-414">bstrFileSystemPath</span></span>  <br/> |<span data-ttu-id="47599-415">Una cadena que identifica el archivo en el cliente.</span><span class="sxs-lookup"><span data-stu-id="47599-415">A string which identifies the file on the client.</span></span> <span data-ttu-id="47599-416">Este valor debe ser una ruta de acceso local no vacía con un máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="47599-416">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="47599-417">Esta ruta de acceso debe estar en el árbol del directorio especificado por la FileSystemDirectoryHint cuando se realizó la llamada a Initialize.</span><span class="sxs-lookup"><span data-stu-id="47599-417">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="47599-418">bstrResourceID</span><span class="sxs-lookup"><span data-stu-id="47599-418">bstrResourceID</span></span>  <br/> |<span data-ttu-id="47599-419">Una cadena que identifica el ResourceID del archivo.</span><span class="sxs-lookup"><span data-stu-id="47599-419">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="47599-420">Este valor debe ser no vacía con un máximo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="47599-420">This value must be non-empty with a maximum of 128 characters.</span></span>  <br/> |
|<span data-ttu-id="47599-421">bstrWebPath</span><span class="sxs-lookup"><span data-stu-id="47599-421">bstrWebPath</span></span>  <br/> |<span data-ttu-id="47599-422">Una cadena que identifica el archivo en el servidor.</span><span class="sxs-lookup"><span data-stu-id="47599-422">A string which identifies the file on the server.</span></span> <span data-ttu-id="47599-423">Este valor debe ser una no vacías dirección URL válida, pero no puede superar los INTERNET_MAX_URL_LENGTH, tal como se define por https://support.microsoft.com/kb/208427.</span><span class="sxs-lookup"><span data-stu-id="47599-423">This value must be a non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span>  <br/> |
   
##### <a name="return-values"></a><span data-ttu-id="47599-424">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-424">Return values</span></span>

|<span data-ttu-id="47599-425">Valor</span><span class="sxs-lookup"><span data-stu-id="47599-425">Value</span></span>|<span data-ttu-id="47599-426">Descripción</span><span class="sxs-lookup"><span data-stu-id="47599-426">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="47599-427">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="47599-427">E_FAIL</span></span>  <br/> |<span data-ttu-id="47599-428">Error al establecer el estado de la conectividad de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="47599-428">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="47599-429">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="47599-429">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="47599-430">El archivo especificado por _bstrFileSystemPath_ tiene un ResourceID diferente del especificado.</span><span class="sxs-lookup"><span data-stu-id="47599-430">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span>  <br/> |
|<span data-ttu-id="47599-431">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="47599-431">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="47599-432">No se admite la extensión de archivo determinada por el objeto COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="47599-432">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="47599-433">Vea GetSupportedFileExtensions.</span><span class="sxs-lookup"><span data-stu-id="47599-433">See GetSupportedFileExtensions.</span></span>  <br/> |
|<span data-ttu-id="47599-434">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="47599-434">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="47599-435">El archivo se ha eliminado en operación intermedio.</span><span class="sxs-lookup"><span data-stu-id="47599-435">The file was deleted in mid-operation.</span></span>  <br/> |
|<span data-ttu-id="47599-436">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="47599-436">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="47599-437">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="47599-437">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="47599-438">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="47599-438">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="47599-439">El FileSystemPath determinado no está bajo la raíz del directorio especificada por la FileSystemDirectoryHint cuando se realizó la llamada a Initialize.</span><span class="sxs-lookup"><span data-stu-id="47599-439">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="47599-440">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="47599-440">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="47599-441">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.</span><span class="sxs-lookup"><span data-stu-id="47599-441">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="47599-442">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="47599-442">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="47599-443">El archivo especificado por _bstrResourceID_ tiene un FileSystemPath diferente del especificado.</span><span class="sxs-lookup"><span data-stu-id="47599-443">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="47599-444">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="47599-444">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="47599-445">El archivo especificado ya tiene cambios pendientes en una caché diferente y aún no se puede asociar con la memoria caché del consumidor.</span><span class="sxs-lookup"><span data-stu-id="47599-445">The specified file already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="47599-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="47599-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="47599-447">El WebPath proporcionado entra en una caché diferente.</span><span class="sxs-lookup"><span data-stu-id="47599-447">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="47599-448">S_OK</span><span class="sxs-lookup"><span data-stu-id="47599-448">S_OK</span></span>  <br/> |<span data-ttu-id="47599-449">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="47599-449">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a><span data-ttu-id="47599-450">ILSCLocalSyncClient::SetClientConnectivityState</span><span class="sxs-lookup"><span data-stu-id="47599-450">ILSCLocalSyncClient::SetClientConnectivityState</span></span>
<span data-ttu-id="47599-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="47599-451"></span></span>

<span data-ttu-id="47599-452">Establece la memoria caché en un estado en línea o sin conexión.</span><span class="sxs-lookup"><span data-stu-id="47599-452">Sets the cache into an online or offline state.</span></span> <span data-ttu-id="47599-453">Si están desconectados, Office no intenta comunicarse con el servidor para todos los archivos en esa memoria caché, independientemente de la configuración de _fBlockUploads_ de cada archivo individual.</span><span class="sxs-lookup"><span data-stu-id="47599-453">If offline, Office will not attempt to communicate with the server for any files in that cache, regardless of each individual file's  _fBlockUploads_ setting.</span></span> 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a><span data-ttu-id="47599-454">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-454">Parameters</span></span>

 <span data-ttu-id="47599-455">_fIsOnline_</span><span class="sxs-lookup"><span data-stu-id="47599-455">_fIsOnline_</span></span>
  
<span data-ttu-id="47599-456">Un valor booleano cómo determinar el estado de la conectividad de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="47599-456">A boolean determining the connectivity state of the cache.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="47599-457">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-457">Return values</span></span>

|<span data-ttu-id="47599-458">Valor</span><span class="sxs-lookup"><span data-stu-id="47599-458">Value</span></span>|<span data-ttu-id="47599-459">Descripción</span><span class="sxs-lookup"><span data-stu-id="47599-459">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="47599-460">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="47599-460">E_FAIL</span></span>  <br/> |<span data-ttu-id="47599-461">Error al establecer el estado de la conectividad de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="47599-461">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="47599-462">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="47599-462">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="47599-463">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="47599-463">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="47599-464">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="47599-464">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="47599-465">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.</span><span class="sxs-lookup"><span data-stu-id="47599-465">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="47599-466">S_OK</span><span class="sxs-lookup"><span data-stu-id="47599-466">S_OK</span></span>  <br/> |<span data-ttu-id="47599-467">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="47599-467">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a><span data-ttu-id="47599-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="47599-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span></span>
<span data-ttu-id="47599-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="47599-469"></span></span>

<span data-ttu-id="47599-470">SetClientNetworkSyncPermission se usa para override o heurística de sincronización del restoreOffice para uso de costo y de la alimentación de la red.</span><span class="sxs-lookup"><span data-stu-id="47599-470">SetClientNetworkSyncPermission is used to either override or restoreOffice's synchronizing heuristics for network cost and power usage.</span></span> <span data-ttu-id="47599-471">Cuando en una 3G u otra red de alto costo, o cuando se ejecuta en batería frente a que se conecta, Office puede elegir esta opción Bloquear el tráfico de red hasta un momento más oportuno.</span><span class="sxs-lookup"><span data-stu-id="47599-471">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span> <span data-ttu-id="47599-472">El consumidor de esta API puede usarla para reemplazar heurística de la oficina y forzar la sincronización para que se produzcan.</span><span class="sxs-lookup"><span data-stu-id="47599-472">The consumer of this API can use it to override Office's heuristics and force synchronizing to occur.</span></span>
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a><span data-ttu-id="47599-473">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-473">Parameters</span></span>

 <span data-ttu-id="47599-474">_nspType_</span><span class="sxs-lookup"><span data-stu-id="47599-474">_nspType_</span></span>
  
<span data-ttu-id="47599-475">Marca que define qué heurística de costo para invalidar.</span><span class="sxs-lookup"><span data-stu-id="47599-475">A flag which defines which cost heuristic to override.</span></span> <span data-ttu-id="47599-476">Vea la [Enumeración LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="47599-476">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span>
  
 <span data-ttu-id="47599-477">_fEnableSync_</span><span class="sxs-lookup"><span data-stu-id="47599-477">_fEnableSync_</span></span>
  
<span data-ttu-id="47599-478">Especifica si para forzar la sincronización en, por lo tanto reemplazar esa heurística de costo, o ya no invalidarla.</span><span class="sxs-lookup"><span data-stu-id="47599-478">Specifies whether to force synchronizing on, thus overriding that cost heuristic, or to no longer override it.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="47599-479">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-479">Return values</span></span>

|<span data-ttu-id="47599-480">Valor</span><span class="sxs-lookup"><span data-stu-id="47599-480">Value</span></span>|<span data-ttu-id="47599-481">Descripción</span><span class="sxs-lookup"><span data-stu-id="47599-481">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="47599-482">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="47599-482">E_FAIL</span></span>  <br/> |<span data-ttu-id="47599-483">Error al reemplazar heurística de sincronización.</span><span class="sxs-lookup"><span data-stu-id="47599-483">Failure to override synchronizing heuristics.</span></span>  <br/> |
|<span data-ttu-id="47599-484">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="47599-484">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="47599-485">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.</span><span class="sxs-lookup"><span data-stu-id="47599-485">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="47599-486">S_OK</span><span class="sxs-lookup"><span data-stu-id="47599-486">S_OK</span></span>  <br/> |<span data-ttu-id="47599-487">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="47599-487">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a><span data-ttu-id="47599-488">ILSCLocalSyncClient::Uninitialize</span><span class="sxs-lookup"><span data-stu-id="47599-488">ILSCLocalSyncClient::Uninitialize</span></span>
<span data-ttu-id="47599-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span><span class="sxs-lookup"><span data-stu-id="47599-489"></span></span>

<span data-ttu-id="47599-490">Descarga de la memoria caché desde el objeto COM y llevar a cabo operaciones de cierre.</span><span class="sxs-lookup"><span data-stu-id="47599-490">Unloads the cache from the COM object and perform closing operations.</span></span> <span data-ttu-id="47599-491">[ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) DEBE llamarse antes de destruir el objeto COM.</span><span class="sxs-lookup"><span data-stu-id="47599-491">[ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUST be called before destroying the COM object.</span></span> <span data-ttu-id="47599-492">Después de llamar, no se puede llamar a ningún otras API, el objeto COM debe ser destruye y crea una nueva si desea continuar con las operaciones.</span><span class="sxs-lookup"><span data-stu-id="47599-492">Once called, no other APIs can be called, the COM object MUST be destroyed and a new one created if you wish to continue operations.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a><span data-ttu-id="47599-493">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-493">Parameters</span></span>

<span data-ttu-id="47599-494">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="47599-494">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="47599-495">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-495">Return values</span></span>

|<span data-ttu-id="47599-496">Valor</span><span class="sxs-lookup"><span data-stu-id="47599-496">Value</span></span>|<span data-ttu-id="47599-497">Descripción</span><span class="sxs-lookup"><span data-stu-id="47599-497">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="47599-498">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="47599-498">E_FAIL</span></span>  <br/> |<span data-ttu-id="47599-499">Error al cancelar la inicialización.</span><span class="sxs-lookup"><span data-stu-id="47599-499">Failure to uninitialize.</span></span>  <br/> |
|<span data-ttu-id="47599-500">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="47599-500">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="47599-501">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.</span><span class="sxs-lookup"><span data-stu-id="47599-501">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="47599-502">S_OK</span><span class="sxs-lookup"><span data-stu-id="47599-502">S_OK</span></span>  <br/> |<span data-ttu-id="47599-503">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="47599-503">The call succeeded.</span></span>  <br/> |
   
### <a name="interface-ienumlscevent"></a><span data-ttu-id="47599-504">Interfaz IEnumLSCEvent</span><span class="sxs-lookup"><span data-stu-id="47599-504">Interface IEnumLSCEvent</span></span>

<span data-ttu-id="47599-505">Esta interfaz representa una lista de eventos de ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="47599-505">This interface represents a list of ILSCEvent events.</span></span>
  
<span data-ttu-id="47599-506">**Funciones miembro públicas**</span><span class="sxs-lookup"><span data-stu-id="47599-506">**Public member functions**</span></span>

#### <a name="ienumlsceventfnext"></a><span data-ttu-id="47599-507">IEnumLSCEvent::FNext</span><span class="sxs-lookup"><span data-stu-id="47599-507">IEnumLSCEvent::FNext</span></span>

<span data-ttu-id="47599-508">Recupera el siguiente evento de la lista de eventos.</span><span class="sxs-lookup"><span data-stu-id="47599-508">Retrieves the next event from the list of events.</span></span>
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a><span data-ttu-id="47599-509">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-509">Parameters</span></span>

 <span data-ttu-id="47599-510">_ppiLSCEvent_</span><span class="sxs-lookup"><span data-stu-id="47599-510">_ppiLSCEvent_</span></span>
  
<span data-ttu-id="47599-511">Un puntero a una interfaz ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="47599-511">A pointer to an ILSCEvent interface.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="47599-512">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-512">Return values</span></span>

|<span data-ttu-id="47599-513">Valor</span><span class="sxs-lookup"><span data-stu-id="47599-513">Value</span></span>|<span data-ttu-id="47599-514">Descripción</span><span class="sxs-lookup"><span data-stu-id="47599-514">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="47599-515">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="47599-515">E_FAIL</span></span>  <br/> |<span data-ttu-id="47599-516">No existen más eventos.</span><span class="sxs-lookup"><span data-stu-id="47599-516">There are no more events.</span></span>  <br/> |
|<span data-ttu-id="47599-517">S_OK</span><span class="sxs-lookup"><span data-stu-id="47599-517">S_OK</span></span>  <br/> |<span data-ttu-id="47599-518">La llamada tuvo éxito.</span><span class="sxs-lookup"><span data-stu-id="47599-518">The call was successful.</span></span>  <br/> |
   
#### <a name="ienumlsceventreset"></a><span data-ttu-id="47599-519">IEnumLSCEvent::Reset</span><span class="sxs-lookup"><span data-stu-id="47599-519">IEnumLSCEvent::Reset</span></span>

<span data-ttu-id="47599-520">Restablece el enumerador al primer evento.</span><span class="sxs-lookup"><span data-stu-id="47599-520">Resets the enumerator to the first event.</span></span>
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a><span data-ttu-id="47599-521">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-521">Parameters</span></span>

<span data-ttu-id="47599-522">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="47599-522">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="47599-523">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-523">Return values</span></span>

<span data-ttu-id="47599-524">Siempre devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="47599-524">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent"></a><span data-ttu-id="47599-525">Interfaz ILSCEvent</span><span class="sxs-lookup"><span data-stu-id="47599-525">Interface ILSCEvent</span></span>

<span data-ttu-id="47599-526">Esta interfaz representa un evento de sincronización.</span><span class="sxs-lookup"><span data-stu-id="47599-526">This interface represents a synchronizing event.</span></span> <span data-ttu-id="47599-527">Toda la información sobre el evento se puede recuperar desde la interfaz.</span><span class="sxs-lookup"><span data-stu-id="47599-527">All information about the event can be retrieved from the interface.</span></span>
  
<span data-ttu-id="47599-528">**Funciones miembro públicas**</span><span class="sxs-lookup"><span data-stu-id="47599-528">**Public member functions**</span></span>

#### <a name="ilsceventgetconflictstatus"></a><span data-ttu-id="47599-529">ILSCEvent::GetConflictStatus</span><span class="sxs-lookup"><span data-stu-id="47599-529">ILSCEvent::GetConflictStatus</span></span>

<span data-ttu-id="47599-530">Tenga en cuenta que este valor se rellena cuando [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) se llama, no cuando se creó el evento, por lo que sólo tendrá el estado actual del archivo, no el estado del archivo cuando cambia el estado de conflicto.</span><span class="sxs-lookup"><span data-stu-id="47599-530">Note that this value is populated when [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) is called, not when the event was created, so you will only have the current status of the file, not the status of the file when the conflict status changed.</span></span> 
  
<span data-ttu-id="47599-531">Este valor sólo se llena cuando la [Enumeración LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento es LSCEventType_OnLocalConflictStateChanged.</span><span class="sxs-lookup"><span data-stu-id="47599-531">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnLocalConflictStateChanged.</span></span> 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a><span data-ttu-id="47599-532">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-532">Parameters</span></span>

 <span data-ttu-id="47599-533">_pfIsInConflict_</span><span class="sxs-lookup"><span data-stu-id="47599-533">_pfIsInConflict_</span></span>
  
<span data-ttu-id="47599-534">El estado actual de conflicto del archivo asociado con el evento.</span><span class="sxs-lookup"><span data-stu-id="47599-534">The current conflict status of the file associated with the event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="47599-535">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-535">Return values</span></span>

<span data-ttu-id="47599-536">Siempre devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="47599-536">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeterror"></a><span data-ttu-id="47599-537">ILSCEvent::GetError</span><span class="sxs-lookup"><span data-stu-id="47599-537">ILSCEvent::GetError</span></span>

<span data-ttu-id="47599-538">Este valor sólo se rellena cuando la [Enumeración LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento es LSCEventType_OnServerChangesDownloaded o LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="47599-538">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a><span data-ttu-id="47599-539">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-539">Parameters</span></span>

 <span data-ttu-id="47599-540">_pnError_</span><span class="sxs-lookup"><span data-stu-id="47599-540">_pnError_</span></span>
  
<span data-ttu-id="47599-541">El error asociado con este evento.</span><span class="sxs-lookup"><span data-stu-id="47599-541">The error associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="47599-542">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-542">Return values</span></span>

<span data-ttu-id="47599-543">Siempre devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="47599-543">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetetag"></a><span data-ttu-id="47599-544">ILSCEvent::GetETag</span><span class="sxs-lookup"><span data-stu-id="47599-544">ILSCEvent::GetETag</span></span>

<span data-ttu-id="47599-545">Este valor sólo se rellena cuando la [Enumeración LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento es LSCEventType_OnServerChangesDownloaded o LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="47599-545">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a><span data-ttu-id="47599-546">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-546">Parameters</span></span>

 <span data-ttu-id="47599-547">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="47599-547">_pbstrETag_</span></span>
  
<span data-ttu-id="47599-548">El valor de ETag asociado a este evento</span><span class="sxs-lookup"><span data-stu-id="47599-548">The ETag associated with this event</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="47599-549">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-549">Return values</span></span>

<span data-ttu-id="47599-550">Siempre devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="47599-550">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeteventtype"></a><span data-ttu-id="47599-551">ILSCEvent::GetEventType</span><span class="sxs-lookup"><span data-stu-id="47599-551">ILSCEvent::GetEventType</span></span>

<span data-ttu-id="47599-552">Obtiene el tipo de este evento.</span><span class="sxs-lookup"><span data-stu-id="47599-552">Gets the type for this event.</span></span>
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a><span data-ttu-id="47599-553">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-553">Parameters</span></span>

 <span data-ttu-id="47599-554">_pnEventType_</span><span class="sxs-lookup"><span data-stu-id="47599-554">_pnEventType_</span></span>
  
<span data-ttu-id="47599-555">El tipo de evento de este evento.</span><span class="sxs-lookup"><span data-stu-id="47599-555">The event type of this event.</span></span> <span data-ttu-id="47599-556">Vea [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) para los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="47599-556">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for valid values.</span></span> <span data-ttu-id="47599-557">No debe ser null.</span><span class="sxs-lookup"><span data-stu-id="47599-557">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="47599-558">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-558">Return values</span></span>

|<span data-ttu-id="47599-559">Valor</span><span class="sxs-lookup"><span data-stu-id="47599-559">Value</span></span>|<span data-ttu-id="47599-560">Descripción</span><span class="sxs-lookup"><span data-stu-id="47599-560">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="47599-561">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="47599-561">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="47599-562">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="47599-562">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="47599-563">S_OK</span><span class="sxs-lookup"><span data-stu-id="47599-563">S_OK</span></span>  <br/> |<span data-ttu-id="47599-564">La llamada tuvo éxito.</span><span class="sxs-lookup"><span data-stu-id="47599-564">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a><span data-ttu-id="47599-565">ILSCEvent::GetLocalWorkingPath</span><span class="sxs-lookup"><span data-stu-id="47599-565">ILSCEvent::GetLocalWorkingPath</span></span>

<span data-ttu-id="47599-566">Obtiene la ruta de acceso local de trabajo para este evento.</span><span class="sxs-lookup"><span data-stu-id="47599-566">Gets the local working path for this event.</span></span>
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a><span data-ttu-id="47599-567">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-567">Parameters</span></span>

 <span data-ttu-id="47599-568">_pbstrLocalWorkingPath_</span><span class="sxs-lookup"><span data-stu-id="47599-568">_pbstrLocalWorkingPath_</span></span>
  
<span data-ttu-id="47599-569">La ruta de acceso local del archivo al que pertenece este evento.</span><span class="sxs-lookup"><span data-stu-id="47599-569">The local path of the file to which this event pertains.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="47599-570">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-570">Return values</span></span>

<span data-ttu-id="47599-571">Siempre devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="47599-571">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceid"></a><span data-ttu-id="47599-572">ILSCEvent::GetResourceID</span><span class="sxs-lookup"><span data-stu-id="47599-572">ILSCEvent::GetResourceID</span></span>

<span data-ttu-id="47599-573">Obtiene el identificador de recurso para el evento.</span><span class="sxs-lookup"><span data-stu-id="47599-573">Gets the resource ID for the event.</span></span>
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="47599-574">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-574">Parameters</span></span>

 <span data-ttu-id="47599-575">_pbstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="47599-575">_pbstrResourceID_</span></span>
  
<span data-ttu-id="47599-576">ResourceID del archivo asociado con este evento.</span><span class="sxs-lookup"><span data-stu-id="47599-576">The ResourceID of the file associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="47599-577">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-577">Return values</span></span>

<span data-ttu-id="47599-578">Siempre devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="47599-578">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceidattempted"></a><span data-ttu-id="47599-579">ILSCEvent::GetResourceIDAttempted</span><span class="sxs-lookup"><span data-stu-id="47599-579">ILSCEvent::GetResourceIDAttempted</span></span>

<span data-ttu-id="47599-580">Este valor sólo se llena cuando la [Enumeración LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento es LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="47599-580">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> <span data-ttu-id="47599-581">Cuando una llamada a [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)o [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) provocaría un conflicto de ruta de acceso Web o la ruta de acceso Local con otro archivo en la memoria caché de archivos de Office, esto se genera el evento.</span><span class="sxs-lookup"><span data-stu-id="47599-581">When a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) would cause a Web Path or Local Path collision with another file in the Office file cache, this event is generated.</span></span> 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a><span data-ttu-id="47599-582">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-582">Parameters</span></span>

 <span data-ttu-id="47599-583">_pbstrResourceIDAttempted_</span><span class="sxs-lookup"><span data-stu-id="47599-583">_pbstrResourceIDAttempted_</span></span>
  
<span data-ttu-id="47599-584">El ResourceID que causó este evento obtener generado.</span><span class="sxs-lookup"><span data-stu-id="47599-584">The ResourceID that caused this event to get generated.</span></span> <span data-ttu-id="47599-585">No debe ser null.</span><span class="sxs-lookup"><span data-stu-id="47599-585">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="47599-586">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-586">Return values</span></span>

<span data-ttu-id="47599-587">Siempre devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="47599-587">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetsyncerrortype"></a><span data-ttu-id="47599-588">ILSCEvent::GetSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="47599-588">ILSCEvent::GetSyncErrorType</span></span>

<span data-ttu-id="47599-589">Este valor sólo se rellena cuando la [Enumeración LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento es LSCEventType_OnServerChangesDownloaded o LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="47599-589">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a><span data-ttu-id="47599-590">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-590">Parameters</span></span>

 <span data-ttu-id="47599-591">_pnSyncErrorType_</span><span class="sxs-lookup"><span data-stu-id="47599-591">_pnSyncErrorType_</span></span>
  
<span data-ttu-id="47599-592">El tipo de error asociado con este evento.</span><span class="sxs-lookup"><span data-stu-id="47599-592">The error type associated with this event.</span></span> <span data-ttu-id="47599-593">Los valores posibles, vea [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) .</span><span class="sxs-lookup"><span data-stu-id="47599-593">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for potential values.</span></span> <span data-ttu-id="47599-594">No debe ser null.</span><span class="sxs-lookup"><span data-stu-id="47599-594">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="47599-595">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-595">Return values</span></span>

|<span data-ttu-id="47599-596">Valor</span><span class="sxs-lookup"><span data-stu-id="47599-596">Value</span></span>|<span data-ttu-id="47599-597">Descripción</span><span class="sxs-lookup"><span data-stu-id="47599-597">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="47599-598">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="47599-598">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="47599-599">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="47599-599">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="47599-600">S_OK</span><span class="sxs-lookup"><span data-stu-id="47599-600">S_OK</span></span>  <br/> |<span data-ttu-id="47599-601">La llamada tuvo éxito.</span><span class="sxs-lookup"><span data-stu-id="47599-601">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetwebpath"></a><span data-ttu-id="47599-602">ILSCEvent::GetWebPath</span><span class="sxs-lookup"><span data-stu-id="47599-602">ILSCEvent::GetWebPath</span></span>

<span data-ttu-id="47599-603">Este valor sólo se llena cuando la [Enumeración LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento es LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="47599-603">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a><span data-ttu-id="47599-604">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-604">Parameters</span></span>

 <span data-ttu-id="47599-605">_pbstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="47599-605">_pbstrWebPath_</span></span>
  
<span data-ttu-id="47599-606">Especifica la ruta de acceso Web asociado con este evento.</span><span class="sxs-lookup"><span data-stu-id="47599-606">Specifies the Web Path associated with this event.</span></span> <span data-ttu-id="47599-607">No debe ser null.</span><span class="sxs-lookup"><span data-stu-id="47599-607">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="47599-608">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-608">Return values</span></span>

<span data-ttu-id="47599-609">Siempre devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="47599-609">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent2"></a><span data-ttu-id="47599-610">Interfaz ILSCEvent2</span><span class="sxs-lookup"><span data-stu-id="47599-610">Interface ILSCEvent2</span></span>

<span data-ttu-id="47599-611">Esta interfaz contiene información adicional acerca de un evento de sincronización.</span><span class="sxs-lookup"><span data-stu-id="47599-611">This interface holds additional information about a synchronizing event.</span></span>
  
<span data-ttu-id="47599-612">**Funciones miembro públicas**</span><span class="sxs-lookup"><span data-stu-id="47599-612">**Public member functions**</span></span>

#### <a name="ilscevent2geterrorchain"></a><span data-ttu-id="47599-613">ILSCEvent2::GetErrorChain</span><span class="sxs-lookup"><span data-stu-id="47599-613">ILSCEvent2::GetErrorChain</span></span>

<span data-ttu-id="47599-614">Obtiene la información de la cadena de error sobre un evento de sincronización.</span><span class="sxs-lookup"><span data-stu-id="47599-614">Gets the error chain information about a synchronizing event.</span></span>
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a><span data-ttu-id="47599-615">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-615">Parameters</span></span>

 <span data-ttu-id="47599-616">_pbstrErrorChain_</span><span class="sxs-lookup"><span data-stu-id="47599-616">_pbstrErrorChain_</span></span>
  
<span data-ttu-id="47599-617">Una cadena que contenga la información de la cadena de error.</span><span class="sxs-lookup"><span data-stu-id="47599-617">A string to hold the error chain information.</span></span> <span data-ttu-id="47599-618">No debe ser null.</span><span class="sxs-lookup"><span data-stu-id="47599-618">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="47599-619">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-619">Return values</span></span>

|<span data-ttu-id="47599-620">Valor</span><span class="sxs-lookup"><span data-stu-id="47599-620">Value</span></span>|<span data-ttu-id="47599-621">Descripción</span><span class="sxs-lookup"><span data-stu-id="47599-621">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="47599-622">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="47599-622">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="47599-623">La versión instalada de Office no admite esta interfaz</span><span class="sxs-lookup"><span data-stu-id="47599-623">The installed version of Office does not support this interface</span></span>  <br/> |
|<span data-ttu-id="47599-624">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="47599-624">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="47599-625">Uno o varios de los valores de parámetro no son válidos.</span><span class="sxs-lookup"><span data-stu-id="47599-625">One or more of the parameter values are invalid.</span></span>  <br/> |
|<span data-ttu-id="47599-626">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="47599-626">E_FAIL</span></span>  <br/> |<span data-ttu-id="47599-627">La información de la cadena de error no está disponible.</span><span class="sxs-lookup"><span data-stu-id="47599-627">The error chain information is not available.</span></span>  <br/> |
|<span data-ttu-id="47599-628">S_OK</span><span class="sxs-lookup"><span data-stu-id="47599-628">S_OK</span></span>  <br/> |<span data-ttu-id="47599-629">La llamada tuvo éxito.</span><span class="sxs-lookup"><span data-stu-id="47599-629">The call was successful.</span></span>  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a><span data-ttu-id="47599-630">Interfaz IPartnerActivityCallback</span><span class="sxs-lookup"><span data-stu-id="47599-630">Interface IPartnerActivityCallback</span></span>

<span data-ttu-id="47599-631">Esta interfaz proporciona una función de devolución de llamada para el objeto COM CSISyncClient.</span><span class="sxs-lookup"><span data-stu-id="47599-631">This interface provides a callback function to the CSISyncClient COM object.</span></span>
  
<span data-ttu-id="47599-632">**Funciones miembro públicas**</span><span class="sxs-lookup"><span data-stu-id="47599-632">**Public member functions**</span></span>

#### <a name="ipartneractivitycallbackeventoccurred"></a><span data-ttu-id="47599-633">IPartnerActivityCallback::EventOccurred</span><span class="sxs-lookup"><span data-stu-id="47599-633">IPartnerActivityCallback::EventOccurred</span></span>

<span data-ttu-id="47599-634">Esto es una función de devolución de llamada en el objeto dado al objeto COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="47599-634">This is a callback function on the object given to the CsiSyncClient COM object.</span></span> <span data-ttu-id="47599-635">Se espera que cuando se produce un evento (vea la [Enumeración LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) para tipos de eventos válido), el objeto COM CsiSyncClient llamará a este método, el consumidor de señalización.</span><span class="sxs-lookup"><span data-stu-id="47599-635">It's expected that when an Event occurs (see [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid event types), the CsiSyncClient COM object will call this method, signalling the consumer.</span></span> 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a><span data-ttu-id="47599-636">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47599-636">Parameters</span></span>

 <span data-ttu-id="47599-637">_eEventTypeOccurred_</span><span class="sxs-lookup"><span data-stu-id="47599-637">_eEventTypeOccurred_</span></span>
  
<span data-ttu-id="47599-638">El tipo de evento de este evento.</span><span class="sxs-lookup"><span data-stu-id="47599-638">The event type of this event.</span></span> <span data-ttu-id="47599-639">Vea [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) para los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="47599-639">See [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid values.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="47599-640">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="47599-640">Return values</span></span>

<span data-ttu-id="47599-641">Siempre devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="47599-641">Always returns S_OK.</span></span>
  
## <a name="enumerations"></a><span data-ttu-id="47599-642">Enumeraciones</span><span class="sxs-lookup"><span data-stu-id="47599-642">Enumerations</span></span>

<span data-ttu-id="47599-643">CSISyncClient usa las siguientes enumeraciones.</span><span class="sxs-lookup"><span data-stu-id="47599-643">CSISyncClient uses the following enumerations.</span></span>
  
### <a name="enum-lsceventsyncerrortype"></a><span data-ttu-id="47599-644">Enumeración LSCEventSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="47599-644">Enum LSCEventSyncErrorType</span></span>
<span data-ttu-id="47599-645"><a name="Enum_LSCEventSyncErrorType"> </a></span><span class="sxs-lookup"><span data-stu-id="47599-645"></span></span>

<span data-ttu-id="47599-646">Esta enumeración especifica las categorías de errores que pueden producirse durante la sincronización de un archivo.</span><span class="sxs-lookup"><span data-stu-id="47599-646">This enumeration specifies the categories of errors that can occur while synchronizing a file.</span></span>
  
|<span data-ttu-id="47599-647">Enumerador</span><span class="sxs-lookup"><span data-stu-id="47599-647">Enumerator</span></span>|<span data-ttu-id="47599-648">Descripción</span><span class="sxs-lookup"><span data-stu-id="47599-648">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="47599-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span><span class="sxs-lookup"><span data-stu-id="47599-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span></span>  <br/> |<span data-ttu-id="47599-650">El error de sincronización de este evento no se esperaba y es posible que requieren una consideración especial.</span><span class="sxs-lookup"><span data-stu-id="47599-650">The synchronizing error of this event was unexpected, and may require special consideration.</span></span> <span data-ttu-id="47599-651">De forma predeterminada, el usuario deba intervenir.</span><span class="sxs-lookup"><span data-stu-id="47599-651">By default, the user may have to intervene.</span></span>  <br/> |
|<span data-ttu-id="47599-652">LSCEventSyncErrorType_NoInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="47599-652">LSCEventSyncErrorType_NoInterventionRequired</span></span>  <br/> |<span data-ttu-id="47599-653">El error de sincronización de este evento no necesitan una consideración especial.</span><span class="sxs-lookup"><span data-stu-id="47599-653">The synchronizing error of this event does not need special consideration.</span></span> <span data-ttu-id="47599-654">Office controla automáticamente.</span><span class="sxs-lookup"><span data-stu-id="47599-654">Office will handle it automatically.</span></span>  <br/> |
|<span data-ttu-id="47599-655">LSCEventSyncErrorType_UserInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="47599-655">LSCEventSyncErrorType_UserInterventionRequired</span></span>  <br/> |<span data-ttu-id="47599-656">El error de sincronización de este evento requiere que un usuario resolverlo.</span><span class="sxs-lookup"><span data-stu-id="47599-656">The synchronizing error of this event requires a user to resolve it.</span></span> <span data-ttu-id="47599-657">Por ejemplo, error de conflicto de combinación requiere que un usuario abrir el documento y combinar.</span><span class="sxs-lookup"><span data-stu-id="47599-657">For example, merge conflict error requires a user to open the document and merge it.</span></span>  <br/> |
|<span data-ttu-id="47599-658">LSCEventSyncErrorType_WaitingOnClient</span><span class="sxs-lookup"><span data-stu-id="47599-658">LSCEventSyncErrorType_WaitingOnClient</span></span>  <br/> |<span data-ttu-id="47599-659">El error de sincronización de este evento requiere el consumidor intervenir, pero no debe requieren una consideración especial por el usuario.</span><span class="sxs-lookup"><span data-stu-id="47599-659">The synchronizing error of this event requires the consumer to intervene, but should not require special consideration by the user.</span></span>  <br/> |
|<span data-ttu-id="47599-660">LSCEventSyncErrorType_ClientInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="47599-660">LSCEventSyncErrorType_ClientInterventionRequired</span></span>  <br/> |<span data-ttu-id="47599-661">El error de sincronización de este evento requiere el consumidor a intervenir como un caso especial.</span><span class="sxs-lookup"><span data-stu-id="47599-661">The synchronizing error of this event requires the consumer to intervene as a special case.</span></span>  <br/> |
|<span data-ttu-id="47599-662">LSCEventSyncErrorType_Max</span><span class="sxs-lookup"><span data-stu-id="47599-662">LSCEventSyncErrorType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtype"></a><span data-ttu-id="47599-663">Enumeración LSCEventType</span><span class="sxs-lookup"><span data-stu-id="47599-663">Enum LSCEventType</span></span>
<span data-ttu-id="47599-664"><a name="Enum_LSCEventType"> </a></span><span class="sxs-lookup"><span data-stu-id="47599-664"></span></span>

<span data-ttu-id="47599-665">Esta enumeración especifica el tipo de eventos que se pueden producir por un archivo determinado.</span><span class="sxs-lookup"><span data-stu-id="47599-665">This enumeration specifies the type of events that can occur for a particular file.</span></span>
  
|<span data-ttu-id="47599-666">Enumerador</span><span class="sxs-lookup"><span data-stu-id="47599-666">Enumerator</span></span>|<span data-ttu-id="47599-667">Descripción</span><span class="sxs-lookup"><span data-stu-id="47599-667">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="47599-668">LSCEventType_None</span><span class="sxs-lookup"><span data-stu-id="47599-668">LSCEventType_None</span></span>  <br/> ||
|<span data-ttu-id="47599-669">LSCEventType_OnLocalChanges</span><span class="sxs-lookup"><span data-stu-id="47599-669">LSCEventType_OnLocalChanges</span></span>  <br/> |<span data-ttu-id="47599-670">Los cambios realizados en un archivo local.</span><span class="sxs-lookup"><span data-stu-id="47599-670">Changes were made to a local file.</span></span>  <br/> |
|<span data-ttu-id="47599-671">LSCEventType_OnOpenedByUser</span><span class="sxs-lookup"><span data-stu-id="47599-671">LSCEventType_OnOpenedByUser</span></span>  <br/> |<span data-ttu-id="47599-672">Un usuario abre un archivo.</span><span class="sxs-lookup"><span data-stu-id="47599-672">A user opened a file.</span></span>  <br/> |
|<span data-ttu-id="47599-673">LSCEventType_OnServerChangesDownloaded</span><span class="sxs-lookup"><span data-stu-id="47599-673">LSCEventType_OnServerChangesDownloaded</span></span>  <br/> |<span data-ttu-id="47599-674">Terminado de descargar los cambios del archivo desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="47599-674">Finished downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="47599-675">LSCEventType_OnLocalChangesUploaded</span><span class="sxs-lookup"><span data-stu-id="47599-675">LSCEventType_OnLocalChangesUploaded</span></span>  <br/> |<span data-ttu-id="47599-676">Terminado de cargar los cambios de archivo en el servidor.</span><span class="sxs-lookup"><span data-stu-id="47599-676">Finished uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="47599-677">LSCEventType_OnLocalConflictStateChanged</span><span class="sxs-lookup"><span data-stu-id="47599-677">LSCEventType_OnLocalConflictStateChanged</span></span>  <br/> |<span data-ttu-id="47599-678">El estado de conflicto de combinación de un archivo ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="47599-678">The merge conflict state of a file has changed.</span></span>  <br/> |
|<span data-ttu-id="47599-679">LSCEventType_OnFileAdded</span><span class="sxs-lookup"><span data-stu-id="47599-679">LSCEventType_OnFileAdded</span></span>  <br/> |<span data-ttu-id="47599-680">Se ha agregado un archivo.</span><span class="sxs-lookup"><span data-stu-id="47599-680">A file was added.</span></span>  <br/> |
|<span data-ttu-id="47599-681">LSCEventType_OnFileDeleted</span><span class="sxs-lookup"><span data-stu-id="47599-681">LSCEventType_OnFileDeleted</span></span>  <br/> |<span data-ttu-id="47599-682">Se eliminó un archivo.</span><span class="sxs-lookup"><span data-stu-id="47599-682">A file was deleted.</span></span>  <br/> |
|<span data-ttu-id="47599-683">LSCEventType_OnSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="47599-683">LSCEventType_OnSyncEnabled</span></span>  <br/> |<span data-ttu-id="47599-684">Se habilitó la sincronización para los archivos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="47599-684">Synchronizing was enabled for a user's files.</span></span>  <br/> |
|<span data-ttu-id="47599-685">LSCEventType_OnServerChangesDownloadStarted</span><span class="sxs-lookup"><span data-stu-id="47599-685">LSCEventType_OnServerChangesDownloadStarted</span></span>  <br/> |<span data-ttu-id="47599-686">Comienza a descargar los cambios del archivo desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="47599-686">Started downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="47599-687">LSCEventType_OnLocalChangesUploadStarted</span><span class="sxs-lookup"><span data-stu-id="47599-687">LSCEventType_OnLocalChangesUploadStarted</span></span>  <br/> |<span data-ttu-id="47599-688">Cargar los cambios de archivo en el servidor se inició.</span><span class="sxs-lookup"><span data-stu-id="47599-688">Started uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="47599-689">LSCEventType_OnFilePathConflict</span><span class="sxs-lookup"><span data-stu-id="47599-689">LSCEventType_OnFilePathConflict</span></span>  <br/> |<span data-ttu-id="47599-690">Este evento se genera cuando una llamada a [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), o [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) hace que una ruta de acceso Web o la ruta de acceso Local colisión con otro archivo en el Memoria caché de archivos de Office.</span><span class="sxs-lookup"><span data-stu-id="47599-690">This event is generated when a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) causes a Web Path or Local Path collision with another file in the Office file cache.</span></span>  <br/> |
|<span data-ttu-id="47599-691">LSCEventType_OnFileForked</span><span class="sxs-lookup"><span data-stu-id="47599-691">LSCEventType_OnFileForked</span></span>  <br/> ||
|<span data-ttu-id="47599-692">LSCEventType_Max</span><span class="sxs-lookup"><span data-stu-id="47599-692">LSCEventType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a><span data-ttu-id="47599-693">Enumeración LSCEventTypeOccurred</span><span class="sxs-lookup"><span data-stu-id="47599-693">Enum LSCEventTypeOccurred</span></span>
<span data-ttu-id="47599-694"><a name="Enum_LSCEventTypeOccurred"> </a></span><span class="sxs-lookup"><span data-stu-id="47599-694"></span></span>

<span data-ttu-id="47599-695">Esta enumeración especifica el tipo de eventos que se pueden producir.</span><span class="sxs-lookup"><span data-stu-id="47599-695">This enumeration specifies the type of events that can occur.</span></span> <span data-ttu-id="47599-696">El consumidor debe llamar a funciones específicas de ILSCLocalSyncClient según el tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="47599-696">The consumer needs to call specific ILSCLocalSyncClient functions based on the event type.</span></span>
  
|<span data-ttu-id="47599-697">Enumerador</span><span class="sxs-lookup"><span data-stu-id="47599-697">Enumerator</span></span>|<span data-ttu-id="47599-698">Descripción</span><span class="sxs-lookup"><span data-stu-id="47599-698">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="47599-699">LSCEventTypeOccurred_GetChanges</span><span class="sxs-lookup"><span data-stu-id="47599-699">LSCEventTypeOccurred_GetChanges</span></span>  <br/> |<span data-ttu-id="47599-700">Se ha producido un ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="47599-700">An ILSCEvent has occurred.</span></span> <span data-ttu-id="47599-701">El consumidor debe llamar a [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) para recuperar los datos.</span><span class="sxs-lookup"><span data-stu-id="47599-701">The consumer should call [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) to retrieve the data.</span></span>  <br/> |
|<span data-ttu-id="47599-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="47599-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span></span>  <br/> |<span data-ttu-id="47599-703">Han cambiado las extensiones de archivo compatibles.</span><span class="sxs-lookup"><span data-stu-id="47599-703">The supported file extensions have changed.</span></span> <span data-ttu-id="47599-704">El consumidor debe llamar a [ILSCLocalSyncClient::GetSupportedFileExtensions](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) para recuperar la nueva lista de extensiones admitidas.</span><span class="sxs-lookup"><span data-stu-id="47599-704">The consumer should call [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) to retrieve the new list of supported extensions.</span></span>  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a><span data-ttu-id="47599-705">Enumeración LSCNetworkSyncPermissionType</span><span class="sxs-lookup"><span data-stu-id="47599-705">Enum LSCNetworkSyncPermissionType</span></span>
<span data-ttu-id="47599-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span><span class="sxs-lookup"><span data-stu-id="47599-706"></span></span>

<span data-ttu-id="47599-707">Esta enumeración especifica los indicadores que se utilizan para una heurística de costo de la red.</span><span class="sxs-lookup"><span data-stu-id="47599-707">This enumeration specifies the flags used for a network cost heuristic.</span></span> 

|<span data-ttu-id="47599-708">Enumerador</span><span class="sxs-lookup"><span data-stu-id="47599-708">Enumerator</span></span>|<span data-ttu-id="47599-709">Descripción</span><span class="sxs-lookup"><span data-stu-id="47599-709">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="47599-710">LSCNetworkSyncPermissionType_HighCost</span><span class="sxs-lookup"><span data-stu-id="47599-710">LSCNetworkSyncPermissionType_HighCost</span></span>  <br/> |<span data-ttu-id="47599-711">True si se invalida la heurística de costo para redes costosas (por ejemplo, 3 G).</span><span class="sxs-lookup"><span data-stu-id="47599-711">True if the cost heuristic for expensive networks (such as 3G) is overridden.</span></span>  <br/> |
|<span data-ttu-id="47599-712">LSCNetworkSyncPermissionType_HighPowerUsage</span><span class="sxs-lookup"><span data-stu-id="47599-712">LSCNetworkSyncPermissionType_HighPowerUsage</span></span>  <br/> |<span data-ttu-id="47599-713">True si se invalida la heurística de costo para el uso de la energía (por ejemplo, una batería).</span><span class="sxs-lookup"><span data-stu-id="47599-713">True if the cost heuristic for power usage (such as a battery) is overridden.</span></span>  <br/> |
   
### <a name="enum-lscstatusflag"></a><span data-ttu-id="47599-714">Enumeración LSCStatusFlag</span><span class="sxs-lookup"><span data-stu-id="47599-714">Enum LSCStatusFlag</span></span>
<span data-ttu-id="47599-715"><a name="Enum_LSCStatusFlag"> </a></span><span class="sxs-lookup"><span data-stu-id="47599-715"></span></span>

<span data-ttu-id="47599-716">Esta enumeración se usa para representar el estado de sincronización de un archivo.</span><span class="sxs-lookup"><span data-stu-id="47599-716">This enumeration is used to represent the synchronize status of a file.</span></span> 
  
|<span data-ttu-id="47599-717">Enumerador</span><span class="sxs-lookup"><span data-stu-id="47599-717">Enumerator</span></span>|<span data-ttu-id="47599-718">Descripción</span><span class="sxs-lookup"><span data-stu-id="47599-718">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="47599-719">LCSStatusFlag_None</span><span class="sxs-lookup"><span data-stu-id="47599-719">LCSStatusFlag_None</span></span>  <br/> ||
|<span data-ttu-id="47599-720">LSCStatusFlag_UploadPending</span><span class="sxs-lookup"><span data-stu-id="47599-720">LSCStatusFlag_UploadPending</span></span>  <br/> |<span data-ttu-id="47599-721">Es True si no hay datos para enviar al archivo del servidor pendientes.</span><span class="sxs-lookup"><span data-stu-id="47599-721">True if there is pending data to send to the server file.</span></span>  <br/> |
|<span data-ttu-id="47599-722">LSCStatusFlag_DownloadPending</span><span class="sxs-lookup"><span data-stu-id="47599-722">LSCStatusFlag_DownloadPending</span></span>  <br/> |<span data-ttu-id="47599-723">Es True si no hay datos para descargar desde el archivo del servidor pendientes.</span><span class="sxs-lookup"><span data-stu-id="47599-723">True if there is pending data to download from the server file.</span></span>  <br/> |
|<span data-ttu-id="47599-724">LSCStatusFlag_LocalFileUnchanged</span><span class="sxs-lookup"><span data-stu-id="47599-724">LSCStatusFlag_LocalFileUnchanged</span></span>  <br/> |<span data-ttu-id="47599-725">Es True si los datos de Office tiene en el archivo en su memoria caché es la copia más reciente de los datos en el disco.</span><span class="sxs-lookup"><span data-stu-id="47599-725">True if the data Office has on the file in its cache is the most recent copy of the data on disk.</span></span>  <br/> |
   

