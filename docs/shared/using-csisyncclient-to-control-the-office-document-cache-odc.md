---
title: Uso de CSISyncClient para controlar la caché de documentos de Office (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Aprenda a usar CSISyncClient para controlar la caché de documentos de Office (ODC).
ms.openlocfilehash: ce33063f88492bcd6f9682a4a6431fb36f138d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346259"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a><span data-ttu-id="cd86a-103">Uso de CSISyncClient para controlar la caché de documentos de Office (ODC)</span><span class="sxs-lookup"><span data-stu-id="cd86a-103">Using CSISyncClient to control the Office Document Cache (ODC)</span></span>

<span data-ttu-id="cd86a-104">Aprenda a usar CSISyncClient para controlar la caché de documentos de Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="cd86a-104">Learn how to use CSISyncClient to control the Office Document Cache (ODC).</span></span>
  
<span data-ttu-id="cd86a-105">CSISyncClient es un servidor COM fuera de proceso (CsiSyncClient.exe) que permite a Microsoft OneDrive controlar el comportamiento de la caché de documentos de Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="cd86a-105">CSISyncClient is an out-of-proc COM server (CsiSyncClient.exe) that allows Microsoft OneDrive to control the behavior of the Office Document Cache (ODC).</span></span> <span data-ttu-id="cd86a-106">Por ejemplo, OneDrive puede llamar a la ODC a través de CSISyncClient para cargar y descargar archivos desde y hacia los puntos de conexión habilitados de MS-FSSHTTP.</span><span class="sxs-lookup"><span data-stu-id="cd86a-106">For example, OneDrive may call upon the ODC via CSISyncClient to upload and download files to and from MS-FSSHTTP enabled endpoints.</span></span> <span data-ttu-id="cd86a-107">Esto permite características avanzadas con respaldo de servicios en Office, como la co-autoría y transiciones sin problemas de sin conexión a en línea.</span><span class="sxs-lookup"><span data-stu-id="cd86a-107">This enables advanced service-backed features in Office, such as co-authoring and seamless transitions from offline to online.</span></span>
  
<span data-ttu-id="cd86a-108">CsiSyncClient está disponible en Escritorio de Office (x86 y x64).</span><span class="sxs-lookup"><span data-stu-id="cd86a-108">CsiSyncClient is available in Office Desktop (both x86 and x64).</span></span> <span data-ttu-id="cd86a-109">Nota: Aunque las versiones más recientes de Office pueden enviarse con CsiSyncClient, el proceso se usará solo para la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="cd86a-109">Note: While newer versions of Office may ship with CsiSyncClient, the process will be used for backward compatibility only.</span></span> <span data-ttu-id="cd86a-110">La interfaz CsiSyncClient y la metodología de control de ODC cambiarán en versiones futuras de Office.</span><span class="sxs-lookup"><span data-stu-id="cd86a-110">The CsiSyncClient interface and the methodology of controlling the ODC will change in future versions of Office.</span></span>
  
<span data-ttu-id="cd86a-111">Actualmente, el identificador de clase está configurado para responder solo a OneDrive.</span><span class="sxs-lookup"><span data-stu-id="cd86a-111">The class ID is currently set to respond only to OneDrive.</span></span>
  
<span data-ttu-id="cd86a-112">El objeto COM se puede obtener como un servidor COM fuera del proceso y se ejecuta en CsiSyncClient.exe.</span><span class="sxs-lookup"><span data-stu-id="cd86a-112">The COM object is usable as an out-of-proc COM server and runs in CsiSyncClient.exe.</span></span> <span data-ttu-id="cd86a-113">Debido a las limitaciones de Access (que usa ODC), se incluye con el tipo de bits que office incluye, por lo que x64 Office significa un objeto COM x64 o x86 Office significa un objeto COM x86.</span><span class="sxs-lookup"><span data-stu-id="cd86a-113">Due to limitations with Access (which the ODC uses), it ships with the bit type that Office comes in, so x64 Office means an x64 COM object, or x86 Office means an x86 COM object.</span></span> <span data-ttu-id="cd86a-114">Para evitar esta limitación, al especificar CLSCTX_LOCAL_SERVER como parte de CoCreateInstance, el objeto COM se hospedará como un servidor COM fuera del proceso, lo que permitirá la compatibilidad entre bits.</span><span class="sxs-lookup"><span data-stu-id="cd86a-114">To get around this limitation, specifying CLSCTX_LOCAL_SERVER as part of the CoCreateInstance will have the COM object be hosted as an out-of-proc COM server, allowing cross-bitness compatibility.</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="cd86a-115">Interfaces</span><span class="sxs-lookup"><span data-stu-id="cd86a-115">Interfaces</span></span>

<span data-ttu-id="cd86a-116">CSISyncClient usa las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="cd86a-116">CSISyncClient uses the following interfaces.</span></span>
  
### <a name="interface-ilsclocalsyncclient"></a><span data-ttu-id="cd86a-117">Interfaz ILSCLocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="cd86a-117">Interface ILSCLocalSyncClient</span></span>

<span data-ttu-id="cd86a-118">Esta es la interfaz principal que se usa para sincronizar archivos en Office.</span><span class="sxs-lookup"><span data-stu-id="cd86a-118">This is the primary interface used to synchronize files in Office.</span></span>
  
- <span data-ttu-id="cd86a-119">ProgID: Office.LocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="cd86a-119">ProgID: Office.LocalSyncClient</span></span>
- <span data-ttu-id="cd86a-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span><span class="sxs-lookup"><span data-stu-id="cd86a-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span></span>
- <span data-ttu-id="cd86a-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span><span class="sxs-lookup"><span data-stu-id="cd86a-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span></span>
   
<span data-ttu-id="cd86a-122">El objeto COM que se expone se usa como un servidor fuera del proceso.</span><span class="sxs-lookup"><span data-stu-id="cd86a-122">The COM object that is exposed is used as an out-of-proc server.</span></span> <span data-ttu-id="cd86a-123">La especificación CLSCTX_LOCAL_SERVER como parte de CoCreateInstance permite la compatibilidad entre procesos de 64 bits y 32 bits.</span><span class="sxs-lookup"><span data-stu-id="cd86a-123">Specifying CLSCTX_LOCAL_SERVER as part of CoCreateInstance allows compatability between 64bit and 32bit processes.</span></span>
  
<span data-ttu-id="cd86a-124">Una vez que haya co-creado el objeto COM, debe llamar primero a [ILSCLocalSyncClient::Initialize.](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)</span><span class="sxs-lookup"><span data-stu-id="cd86a-124">Once you've co-created the COM object, you MUST call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) first.</span></span> <span data-ttu-id="cd86a-125">Una [vez que ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) se haya completado correctamente, puede llamar a cualquier API con la frecuencia que desee y en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="cd86a-125">Once [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has completed successfully, you may call any API as often as you wish and in any order.</span></span> <span data-ttu-id="cd86a-126">También puede llamar a [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) en un objeto ya inicializado, pero esto no hace nada.</span><span class="sxs-lookup"><span data-stu-id="cd86a-126">You may also call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) on an already initialized object, but this does nothing.</span></span> 
  
<span data-ttu-id="cd86a-127">Las excepciones al párrafo anterior son [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) e [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="cd86a-127">The exceptions to the previous paragraph are [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) and [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="cd86a-128">Después de llamar a [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) en el objeto COM, debe destruir ese objeto y crear uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="cd86a-128">After you call [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) on the COM object, you MUST destroy that object and create a new one.</span></span> <span data-ttu-id="cd86a-129">[ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) eliminará su subcache, eliminará toda la información de archivo asociada en la memoria caché, pero dejará los documentos en el disco.</span><span class="sxs-lookup"><span data-stu-id="cd86a-129">[ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) will delete your subcache, delete all associated file information in the cache, but leave the documents on disk.</span></span> <span data-ttu-id="cd86a-130">También deja intacto el estado para comunicarse con la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="cd86a-130">It also leaves the state intact for communicating with the cache.</span></span> <span data-ttu-id="cd86a-131">Esto le permite llamar de nuevo a [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) para crear una nueva memoria caché sin tener que destruir y volver a crear el objeto COM.</span><span class="sxs-lookup"><span data-stu-id="cd86a-131">This allows you to call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) again to create a new cache without having to destroy and recreate the COM object.</span></span> 
  
<span data-ttu-id="cd86a-132">**Funciones de miembros públicos**</span><span class="sxs-lookup"><span data-stu-id="cd86a-132">**Public member functions**</span></span>

#### <a name="ilsclocalsyncclientdeletefile"></a><span data-ttu-id="cd86a-133">ILSCLocalSyncClient::D eleteFile</span><span class="sxs-lookup"><span data-stu-id="cd86a-133">ILSCLocalSyncClient::DeleteFile</span></span>

<span data-ttu-id="cd86a-134">DeleteFile se usa para quitar la información del archivo de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="cd86a-134">DeleteFile is used to remove the file information from the cache.</span></span> <span data-ttu-id="cd86a-135">Sin embargo, este método dejará el archivo asociado en el disco y en el servidor.</span><span class="sxs-lookup"><span data-stu-id="cd86a-135">However, this method will leave the associated file on disk and on the server.</span></span>
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="cd86a-136">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-136">Parameters</span></span>

 <span data-ttu-id="cd86a-137">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="cd86a-137">_bstrResourceID_</span></span>
  
<span data-ttu-id="cd86a-138">Cadena que identifica el ResourceID del archivo.</span><span class="sxs-lookup"><span data-stu-id="cd86a-138">The string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="cd86a-139">Este valor no debe estar vacío con un máximo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="cd86a-139">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-140">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-140">Return values</span></span>

|<span data-ttu-id="cd86a-141">Valor</span><span class="sxs-lookup"><span data-stu-id="cd86a-141">Value</span></span>|<span data-ttu-id="cd86a-142">Description</span><span class="sxs-lookup"><span data-stu-id="cd86a-142">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd86a-143">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="cd86a-143">E_FAIL</span></span>  <br/> |<span data-ttu-id="cd86a-144">La llamada ha fallado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-144">The call failed.</span></span>  <br/> |
|<span data-ttu-id="cd86a-145">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="cd86a-145">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="cd86a-146">Uno o varios parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="cd86a-146">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="cd86a-147">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="cd86a-147">E_FAIL</span></span>  <br/> |<span data-ttu-id="cd86a-148">La llamada ha fallado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-148">The call failed.</span></span>  <br/> |
|<span data-ttu-id="cd86a-149">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="cd86a-149">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="cd86a-150">El ResourceID especificado no está en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="cd86a-150">The given ResourceID is not in the cache.</span></span>  <br/> |
|<span data-ttu-id="cd86a-151">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="cd86a-151">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="cd86a-152">No se ha llamado correctamente a initialize en el pasado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-152">Initialize has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="cd86a-153">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="cd86a-153">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="cd86a-154">El archivo está actualmente sincronizado o abierto y no se puede eliminar.</span><span class="sxs-lookup"><span data-stu-id="cd86a-154">The file is currently synchronizing or open and cannot be deleted.</span></span>  <br/> |
|<span data-ttu-id="cd86a-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd86a-155">S_OK</span></span>  <br/> |<span data-ttu-id="cd86a-156">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="cd86a-156">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a><span data-ttu-id="cd86a-157">ILSCLocalSyncClient::GetChanges</span><span class="sxs-lookup"><span data-stu-id="cd86a-157">ILSCLocalSyncClient::GetChanges</span></span>
<span data-ttu-id="cd86a-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span><span class="sxs-lookup"><span data-stu-id="cd86a-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span></span>

<span data-ttu-id="cd86a-159">GetChanges devuelve un enumerador de objetos ILSCEvent y también devuelve un token que se proporciona a la siguiente llamada a GetChanges, suponiendo que el consumidor ha procesado el conjunto de eventos anterior.</span><span class="sxs-lookup"><span data-stu-id="cd86a-159">GetChanges returns an enumerator of ILSCEvent objects, and also returns a token that is given to the next call to GetChanges, assuming the consumer has processed the previous set of events.</span></span> <span data-ttu-id="cd86a-160">Los eventos anteriores  _al nPreviousChangesToken_ especificado se eliminarán y no estarán disponibles.</span><span class="sxs-lookup"><span data-stu-id="cd86a-160">Events before the  _nPreviousChangesToken_ specified will be deleted and unavailable.</span></span> <span data-ttu-id="cd86a-161">Si no hay eventos que procesar, _pnCurrentChangesToken_ debe ser el mismo valor que _nPreviousChangesToken_, pero se seguirá _ppiEvents._</span><span class="sxs-lookup"><span data-stu-id="cd86a-161">If there are no events to be processed,  _pnCurrentChangesToken_ should be the same value as  _nPreviousChangesToken_, but  _ppiEvents_ will still be set.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a><span data-ttu-id="cd86a-162">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-162">Parameters</span></span>

 <span data-ttu-id="cd86a-163">_nPreviousChangesToken_</span><span class="sxs-lookup"><span data-stu-id="cd86a-163">_nPreviousChangesToken_</span></span>
  
<span data-ttu-id="cd86a-164">Identifica qué evento procesó el consumidor por última vez.</span><span class="sxs-lookup"><span data-stu-id="cd86a-164">Identifies which event was last processed by the consumer.</span></span> 
  
 <span data-ttu-id="cd86a-165">_pnCurrentChangesToken_</span><span class="sxs-lookup"><span data-stu-id="cd86a-165">_pnCurrentChangesToken_</span></span>
  
<span data-ttu-id="cd86a-166">Identifica el evento más reciente que se entrega al consumidor.</span><span class="sxs-lookup"><span data-stu-id="cd86a-166">Identifies the most recent event being handed to the consumer.</span></span> <span data-ttu-id="cd86a-167">No debe ser null.</span><span class="sxs-lookup"><span data-stu-id="cd86a-167">Must not be null.</span></span>
  
 <span data-ttu-id="cd86a-168">_ppiEvents_</span><span class="sxs-lookup"><span data-stu-id="cd86a-168">_ppiEvents_</span></span>
  
<span data-ttu-id="cd86a-169">Un enumerador para los eventos entregados al consumidor.</span><span class="sxs-lookup"><span data-stu-id="cd86a-169">An enumerator for the events handed to the consumer.</span></span> <span data-ttu-id="cd86a-170">No debe ser null.</span><span class="sxs-lookup"><span data-stu-id="cd86a-170">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-171">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-171">Return values</span></span>

|<span data-ttu-id="cd86a-172">Valor</span><span class="sxs-lookup"><span data-stu-id="cd86a-172">Value</span></span>|<span data-ttu-id="cd86a-173">Description</span><span class="sxs-lookup"><span data-stu-id="cd86a-173">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd86a-174">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="cd86a-174">E_FAIL</span></span>  <br/> |<span data-ttu-id="cd86a-175">La llamada ha fallado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-175">The call failed.</span></span>  <br/> |
|<span data-ttu-id="cd86a-176">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="cd86a-176">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="cd86a-177">Uno o varios parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="cd86a-177">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="cd86a-178">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="cd86a-178">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="cd86a-179">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-179">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="cd86a-180">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd86a-180">S_OK</span></span>  <br/> |<span data-ttu-id="cd86a-181">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="cd86a-181">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a><span data-ttu-id="cd86a-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="cd86a-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span></span>

<span data-ttu-id="cd86a-183">GetClientNetworkSyncPermission se usa para consultar si se invalida la heurística de sincronización de Office para el costo de red y el uso de energía.</span><span class="sxs-lookup"><span data-stu-id="cd86a-183">GetClientNetworkSyncPermission is used to query whether Office's synchronizing heuristics for network cost and power usage are overridden.</span></span> <span data-ttu-id="cd86a-184">Cuando se encuentra en una 3G u otra red de alto costo, o cuando se ejecuta con batería frente a estar conectado, Office puede optar por bloquear el tráfico de red hasta un momento más oportuno.</span><span class="sxs-lookup"><span data-stu-id="cd86a-184">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span>
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a><span data-ttu-id="cd86a-185">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-185">Parameters</span></span>

 <span data-ttu-id="cd86a-186">_nspType_</span><span class="sxs-lookup"><span data-stu-id="cd86a-186">_nspType_</span></span>
  
<span data-ttu-id="cd86a-187">Marca que define el costo heurístico que se debe consultar.</span><span class="sxs-lookup"><span data-stu-id="cd86a-187">A flag which defines which cost heuristic to query.</span></span> <span data-ttu-id="cd86a-188">Vea [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="cd86a-188">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span> 
  
 <span data-ttu-id="cd86a-189">_pfSyncEnabled_</span><span class="sxs-lookup"><span data-stu-id="cd86a-189">_pfSyncEnabled_</span></span>
  
<span data-ttu-id="cd86a-190">Especifica si el costo heurístico solicitado se invalida actualmente o no.</span><span class="sxs-lookup"><span data-stu-id="cd86a-190">Specifies whether the requested cost heuristic is currently overridden or not.</span></span> <span data-ttu-id="cd86a-191">No debe ser null.</span><span class="sxs-lookup"><span data-stu-id="cd86a-191">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-192">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-192">Return values</span></span>

|<span data-ttu-id="cd86a-193">Valor</span><span class="sxs-lookup"><span data-stu-id="cd86a-193">Value</span></span>|<span data-ttu-id="cd86a-194">Description</span><span class="sxs-lookup"><span data-stu-id="cd86a-194">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd86a-195">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="cd86a-195">E_FAIL</span></span>  <br/> |<span data-ttu-id="cd86a-196">La llamada ha fallado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-196">The call failed.</span></span>  <br/> |
|<span data-ttu-id="cd86a-197">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="cd86a-197">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="cd86a-198">Uno o varios parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="cd86a-198">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="cd86a-199">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="cd86a-199">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="cd86a-200">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-200">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="cd86a-201">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd86a-201">S_OK</span></span>  <br/> |<span data-ttu-id="cd86a-202">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="cd86a-202">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a><span data-ttu-id="cd86a-203">ILSCLocalSyncClient::GetFileStatus</span><span class="sxs-lookup"><span data-stu-id="cd86a-203">ILSCLocalSyncClient::GetFileStatus</span></span>

<span data-ttu-id="cd86a-204">GetFileStatus se usa para recopilar información para un archivo específico: si existe en la memoria caché, si tiene comunicación pendiente con la copia del servidor y si Office 2013 tiene los datos más actualizados de la copia local.</span><span class="sxs-lookup"><span data-stu-id="cd86a-204">GetFileStatus is used to gather information for a specific file: whether it exists in the cache, if it has pending communication with the server copy, and if Office 2013 has the most up to date data from the local copy.</span></span> <span data-ttu-id="cd86a-205">Requiere una marca bit a bit de valores [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) para determinar qué información debe consultar el objeto COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="cd86a-205">It requires a bitwise flag of [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) values to determine what information the CsiSyncClient COM object is to query for.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a><span data-ttu-id="cd86a-206">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-206">Parameters</span></span>

 <span data-ttu-id="cd86a-207">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="cd86a-207">_bstrResourceID_</span></span>
  
<span data-ttu-id="cd86a-208">Cadena que identifica el archivo en el cliente.</span><span class="sxs-lookup"><span data-stu-id="cd86a-208">The string which identifies the file on the client.</span></span> <span data-ttu-id="cd86a-209">Este valor debe estar no vacío, con un máximo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="cd86a-209">This value must be non-empty, with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="cd86a-210">_sfRequestedStatus_</span><span class="sxs-lookup"><span data-stu-id="cd86a-210">_sfRequestedStatus_</span></span>
  
<span data-ttu-id="cd86a-211">Marca que define la información que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="cd86a-211">A flag which defines what information to return.</span></span> <span data-ttu-id="cd86a-212">Vea [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="cd86a-212">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
 <span data-ttu-id="cd86a-213">_pbstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="cd86a-213">_pbstrFileSystemPath_</span></span>
  
<span data-ttu-id="cd86a-214">Cadena que identifica la ubicación del archivo identificado por  _bstrResourceID_ en el cliente.</span><span class="sxs-lookup"><span data-stu-id="cd86a-214">The string which identifies the location of the file identified by  _bstrResourceID_ on the client.</span></span> <span data-ttu-id="cd86a-215">No debe ser null.</span><span class="sxs-lookup"><span data-stu-id="cd86a-215">Must not be null.</span></span> 
  
 <span data-ttu-id="cd86a-216">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="cd86a-216">_pbstrETag_</span></span>
  
<span data-ttu-id="cd86a-217">Cadena que contendrá la eTag del archivo identificado por  _bstrResourceID_.</span><span class="sxs-lookup"><span data-stu-id="cd86a-217">A string which will contain the eTag for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="cd86a-218">No debe ser null.</span><span class="sxs-lookup"><span data-stu-id="cd86a-218">Must not be null.</span></span> 
  
 <span data-ttu-id="cd86a-219">_psfFileStatus_</span><span class="sxs-lookup"><span data-stu-id="cd86a-219">_psfFileStatus_</span></span>
  
<span data-ttu-id="cd86a-220">Marca que contendrá el estado solicitado a través  _de sfRequestedStatus_ para el archivo identificado por  _bstrResourceID_.</span><span class="sxs-lookup"><span data-stu-id="cd86a-220">A flag which will contain the status requested via  _sfRequestedStatus_ for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="cd86a-221">No debe ser null.</span><span class="sxs-lookup"><span data-stu-id="cd86a-221">Must not be null.</span></span> <span data-ttu-id="cd86a-222">Vea [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="cd86a-222">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-223">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-223">Return values</span></span>

|<span data-ttu-id="cd86a-224">Valor</span><span class="sxs-lookup"><span data-stu-id="cd86a-224">Value</span></span>|<span data-ttu-id="cd86a-225">Description</span><span class="sxs-lookup"><span data-stu-id="cd86a-225">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd86a-226">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="cd86a-226">E_FAIL</span></span>  <br/> |<span data-ttu-id="cd86a-227">La llamada ha fallado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-227">The call failed.</span></span>  <br/> |
|<span data-ttu-id="cd86a-228">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="cd86a-228">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="cd86a-229">Uno o varios parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="cd86a-229">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="cd86a-230">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="cd86a-230">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="cd86a-231">La información de archivo especificada por  _bstrResourceID_ no existe en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="cd86a-231">The file information specified by  _bstrResourceID_ does not exist in the cache.</span></span>  <br/> |
|<span data-ttu-id="cd86a-232">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="cd86a-232">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="cd86a-233">LSCStatusFlag_LocalFileUnchanged se solicitó o falta el archivo especificado por _bstrResourceID._</span><span class="sxs-lookup"><span data-stu-id="cd86a-233">LSCStatusFlag_LocalFileUnchanged was requested or the file specified by  _bstrResourceID_ is locked or missing.</span></span>  <br/> |
|<span data-ttu-id="cd86a-234">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="cd86a-234">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="cd86a-235">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-235">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="cd86a-236">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd86a-236">S_OK</span></span>  <br/> |<span data-ttu-id="cd86a-237">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="cd86a-237">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a><span data-ttu-id="cd86a-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="cd86a-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span></span>
<span data-ttu-id="cd86a-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span><span class="sxs-lookup"><span data-stu-id="cd86a-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span></span>

<span data-ttu-id="cd86a-240">GetSupportedFileExtensions devuelve una lista de extensiones de archivo delimitadas por canalización que actualmente son compatibles con el objeto COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="cd86a-240">GetSupportedFileExtensions returns a list of pipe-delimited file extensions which are currently supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="cd86a-241">Tenga en cuenta que esta lista puede cambiar y se notificará al consumidor de un cambio a través del objeto IPartnerActivityCallback proporcionado en [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (vea EventOccured).</span><span class="sxs-lookup"><span data-stu-id="cd86a-241">Note that this list may change, and the consumer will be notified of a change via the IPartnerActivityCallback object provided on [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (See EventOccured).</span></span> 
  
<span data-ttu-id="cd86a-242">Un ejemplo de la cadena devuelta es el siguiente: "|docx|docm|pptx|"</span><span class="sxs-lookup"><span data-stu-id="cd86a-242">An example of the string returned is as follows: "|docx|docm|pptx|"</span></span>
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a><span data-ttu-id="cd86a-243">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-243">Parameters</span></span>

 <span data-ttu-id="cd86a-244">_pbstrSupportedFileExtensions_</span><span class="sxs-lookup"><span data-stu-id="cd86a-244">_pbstrSupportedFileExtensions_</span></span>
  
<span data-ttu-id="cd86a-245">Cadena que se va a establecer con un conjunto delimitado por canalización de extensiones de archivo admitidas por el objeto COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="cd86a-245">A string to be set with a pipe-delimited set of file extensions supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="cd86a-246">No debe ser null.</span><span class="sxs-lookup"><span data-stu-id="cd86a-246">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-247">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-247">Return values</span></span>

|<span data-ttu-id="cd86a-248">Valor</span><span class="sxs-lookup"><span data-stu-id="cd86a-248">Value</span></span>|<span data-ttu-id="cd86a-249">Description</span><span class="sxs-lookup"><span data-stu-id="cd86a-249">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd86a-250">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="cd86a-250">E_FAIL</span></span>  <br/> |<span data-ttu-id="cd86a-251">La llamada ha fallado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-251">The call failed.</span></span>  <br/> |
|<span data-ttu-id="cd86a-252">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="cd86a-252">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="cd86a-253">Uno o varios parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="cd86a-253">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="cd86a-254">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="cd86a-254">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="cd86a-255">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-255">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="cd86a-256">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd86a-256">S_OK</span></span>  <br/> |<span data-ttu-id="cd86a-257">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="cd86a-257">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a><span data-ttu-id="cd86a-258">ILSCLocalSyncClient::Initialize</span><span class="sxs-lookup"><span data-stu-id="cd86a-258">ILSCLocalSyncClient::Initialize</span></span>
<span data-ttu-id="cd86a-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span><span class="sxs-lookup"><span data-stu-id="cd86a-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span></span>

<span data-ttu-id="cd86a-260">Initialize debe ser el primer método al que se llama.</span><span class="sxs-lookup"><span data-stu-id="cd86a-260">Initialize must be the first method called.</span></span> <span data-ttu-id="cd86a-261">De lo contrario, todas las demás API devolverán E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="cd86a-261">Otherwise, all other APIs will return E_LSC_NOTINITIALIZED.</span></span> <span data-ttu-id="cd86a-262">Llamar a Initialize en un objeto ya inicializado devuelve S_OK y no hace nada.</span><span class="sxs-lookup"><span data-stu-id="cd86a-262">Calling Initialize on an already initialized object returns S_OK and does nothing.</span></span> <span data-ttu-id="cd86a-263">Si E_LSC_CACHEMISMATCH se devuelve, el autor de la llamada puede llamar a [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) para eliminar la memoria caché asociada con el SuppliedID determinado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-263">If E_LSC_CACHEMISMATCH is returned, the caller may call [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) to delete the cache associated with the given SuppliedID.</span></span> <span data-ttu-id="cd86a-264">Sin embargo, en este caso, otras API seguirán E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="cd86a-264">However, in this case other APIs will still return E_LSC_NOTINITIALIZED.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a><span data-ttu-id="cd86a-265">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-265">Parameters</span></span>

 <span data-ttu-id="cd86a-266">_bstrSuppliedID_</span><span class="sxs-lookup"><span data-stu-id="cd86a-266">_bstrSuppliedID_</span></span>
  
<span data-ttu-id="cd86a-267">Identifica el consumidor y la memoria caché que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="cd86a-267">Identifies the consumer and which cache to use.</span></span> <span data-ttu-id="cd86a-268">Debe estar no vacío con un máximo de 32 caracteres.</span><span class="sxs-lookup"><span data-stu-id="cd86a-268">Must be non-empty with a maximum of 32 characters.</span></span> 
  
 <span data-ttu-id="cd86a-269">_bstrProgID_</span><span class="sxs-lookup"><span data-stu-id="cd86a-269">_bstrProgID_</span></span>
  
<span data-ttu-id="cd86a-270">Identifica el objeto COM del consumidor para la comunicación bidireccional.</span><span class="sxs-lookup"><span data-stu-id="cd86a-270">Identifies the consumer's COM object for two-way communication.</span></span> <span data-ttu-id="cd86a-271">Debe estar no vacío con un máximo de 39 caracteres.</span><span class="sxs-lookup"><span data-stu-id="cd86a-271">Must be non-empty with a maximum of 39 characters.</span></span> <span data-ttu-id="cd86a-272">Vea [ \< la clave ProgID \> ](https://docs.microsoft.com/windows/desktop/com/-progid--key) para obtener más información acerca de los ProgID.</span><span class="sxs-lookup"><span data-stu-id="cd86a-272">See [\<ProgID\> Key](https://docs.microsoft.com/windows/desktop/com/-progid--key) for more information about ProgIDs.</span></span> 
  
 <span data-ttu-id="cd86a-273">_bstrFileSystemDirectoryHint_</span><span class="sxs-lookup"><span data-stu-id="cd86a-273">_bstrFileSystemDirectoryHint_</span></span>
  
<span data-ttu-id="cd86a-274">Identifica la raíz del directorio en la que se almacenarán los archivos locales.</span><span class="sxs-lookup"><span data-stu-id="cd86a-274">Identifies the directory root in which local files will be stored.</span></span> <span data-ttu-id="cd86a-275">Debe estar no vacío con un máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="cd86a-275">Must be non-empty with a maximum of 256 characters.</span></span> <span data-ttu-id="cd86a-276">El directorio ya debe existir.</span><span class="sxs-lookup"><span data-stu-id="cd86a-276">The directory must already exist.</span></span> 
  
 <span data-ttu-id="cd86a-277">_pEventCallback_</span><span class="sxs-lookup"><span data-stu-id="cd86a-277">_pEventCallback_</span></span>
  
<span data-ttu-id="cd86a-278">Interfaz de devolución de llamada a la que CsiSyncClient notificará los cambios.</span><span class="sxs-lookup"><span data-stu-id="cd86a-278">The callback interface which CsiSyncClient will notify on changes.</span></span> <span data-ttu-id="cd86a-279">Vea IPartnerActivityCallback::EventOccurred.</span><span class="sxs-lookup"><span data-stu-id="cd86a-279">See IPartnerActivityCallback::EventOccurred.</span></span> <span data-ttu-id="cd86a-280">Este valor no debe ser nulo.</span><span class="sxs-lookup"><span data-stu-id="cd86a-280">This value must not be null.</span></span> 
  
 <span data-ttu-id="cd86a-281">_pfCreatedNewCache_</span><span class="sxs-lookup"><span data-stu-id="cd86a-281">_pfCreatedNewCache_</span></span>
  
<span data-ttu-id="cd86a-282">Devuelve si se creó una nueva memoria caché.</span><span class="sxs-lookup"><span data-stu-id="cd86a-282">Returns whether a new cache was created.</span></span> <span data-ttu-id="cd86a-283">Si no hay ninguna memoria caché asociada al SuppliedID, se creará una.</span><span class="sxs-lookup"><span data-stu-id="cd86a-283">If no cache is associated with the SuppliedID, one will be created.</span></span> <span data-ttu-id="cd86a-284">Este valor no debe ser nulo.</span><span class="sxs-lookup"><span data-stu-id="cd86a-284">This value must not be null.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-285">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-285">Return values</span></span>

|<span data-ttu-id="cd86a-286">Valor</span><span class="sxs-lookup"><span data-stu-id="cd86a-286">Value</span></span>|<span data-ttu-id="cd86a-287">Description</span><span class="sxs-lookup"><span data-stu-id="cd86a-287">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd86a-288">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="cd86a-288">E_FAIL</span></span>  <br/> |<span data-ttu-id="cd86a-289">La llamada ha fallado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-289">The call failed.</span></span>  <br/> |
|<span data-ttu-id="cd86a-290">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="cd86a-290">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="cd86a-291">Uno o varios parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="cd86a-291">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="cd86a-292">E_LSC_CACHEMISMATCH</span><span class="sxs-lookup"><span data-stu-id="cd86a-292">E_LSC_CACHEMISMATCH</span></span>  <br/> |<span data-ttu-id="cd86a-293">Un SuppliedID ya tiene una memoria caché asociada, pero tiene un ProgId o FileSystemDirectoryHint diferente de los proporcionados.</span><span class="sxs-lookup"><span data-stu-id="cd86a-293">A SuppliedID already has a cache associated with it, but has a different ProgId or FileSystemDirectoryHint than the ones provided.</span></span>  <br/> |
|<span data-ttu-id="cd86a-294">E_LSC_DIRECTORYHINTCONFLICT</span><span class="sxs-lookup"><span data-stu-id="cd86a-294">E_LSC_DIRECTORYHINTCONFLICT</span></span>  <br/> |<span data-ttu-id="cd86a-295">FileSystemDirectoryHint (o una subcarpeta) ya existe en una memoria caché diferente.</span><span class="sxs-lookup"><span data-stu-id="cd86a-295">The FileSystemDirectoryHint (or a subfolder) already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="cd86a-296">E_LAC_PROGIDCONFLICT</span><span class="sxs-lookup"><span data-stu-id="cd86a-296">E_LAC_PROGIDCONFLICT</span></span>  <br/> |<span data-ttu-id="cd86a-297">El ProgID ya existe en una memoria caché diferente.</span><span class="sxs-lookup"><span data-stu-id="cd86a-297">The ProgID already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="cd86a-298">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd86a-298">S_OK</span></span>  <br/> |<span data-ttu-id="cd86a-299">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="cd86a-299">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a><span data-ttu-id="cd86a-300">ILSCLocalSyncClient::LocalFileChange</span><span class="sxs-lookup"><span data-stu-id="cd86a-300">ILSCLocalSyncClient::LocalFileChange</span></span>
<span data-ttu-id="cd86a-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="cd86a-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span></span>

<span data-ttu-id="cd86a-302">LocalFileChange se usa para decir al objeto COM CsiSyncClient que intente cargar el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-302">LocalFileChange is used to tell the CsiSyncClient COM object to attempt to upload the specified file.</span></span> <span data-ttu-id="cd86a-303">El método preparará el archivo para cargarlo, incluida la lectura del contenido actual del archivo.</span><span class="sxs-lookup"><span data-stu-id="cd86a-303">The method will prepare the file for upload, including reading the file's current contents.</span></span> <span data-ttu-id="cd86a-304">Si ya hay una carga pendiente, se descartará la carga anterior y se preparará el nuevo contenido para la carga.</span><span class="sxs-lookup"><span data-stu-id="cd86a-304">If an upload is already pending, the previous upload will be discarded and the new contents prepared for upload.</span></span> <span data-ttu-id="cd86a-305">Si el archivo está abierto para su edición en una aplicación, este método devolverá S_OK sin preparar el archivo para la carga (la aplicación ya debería realizar este paso si hay cambios).</span><span class="sxs-lookup"><span data-stu-id="cd86a-305">If the file is open for editing in an application, this method will return S_OK without preparing the file for upload (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="cd86a-306">Este método permitirá cargas si se marcó como cargas bloqueadas anteriormente (vea [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span><span class="sxs-lookup"><span data-stu-id="cd86a-306">This method will allow uploads if it was marked as uploads blocked previously (see [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span></span>
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="cd86a-307">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-307">Parameters</span></span>

 <span data-ttu-id="cd86a-308">_bstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="cd86a-308">_bstrFileSystemPath_</span></span>
  
<span data-ttu-id="cd86a-309">Cadena que identifica el archivo en el cliente.</span><span class="sxs-lookup"><span data-stu-id="cd86a-309">A string which identifies the file on the client.</span></span> <span data-ttu-id="cd86a-310">Este valor debe ser una ruta de acceso local no vacía con un máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="cd86a-310">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="cd86a-311">Esta ruta de acceso debe estar en el árbol de directorios especificado por FileSystemDirectoryHint cuando se realizó la llamada a [ILSCLocalSyncClient::Initialize.](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)</span><span class="sxs-lookup"><span data-stu-id="cd86a-311">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was made.</span></span> 
  
 <span data-ttu-id="cd86a-312">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="cd86a-312">_bstrResourceID_</span></span>
  
<span data-ttu-id="cd86a-313">Cadena que identifica el ResourceID del archivo.</span><span class="sxs-lookup"><span data-stu-id="cd86a-313">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="cd86a-314">Este valor no debe estar vacío con un máximo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="cd86a-314">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="cd86a-315">_bstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="cd86a-315">_bstrWebPath_</span></span>
  
<span data-ttu-id="cd86a-316">Cadena que identifica el archivo en el servidor.</span><span class="sxs-lookup"><span data-stu-id="cd86a-316">A string which identifies the file on the server.</span></span> <span data-ttu-id="cd86a-317">Este valor debe ser una dirección URL no vacía y válida, pero no más de INTERNET_MAX_URL_LENGTH, tal como se define en https://support.microsoft.com/kb/208427 .</span><span class="sxs-lookup"><span data-stu-id="cd86a-317">This value must be non-empty, valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-318">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-318">Return values</span></span>

|<span data-ttu-id="cd86a-319">Valor</span><span class="sxs-lookup"><span data-stu-id="cd86a-319">Value</span></span>|<span data-ttu-id="cd86a-320">Description</span><span class="sxs-lookup"><span data-stu-id="cd86a-320">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd86a-321">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="cd86a-321">E_FAIL</span></span>  <br/> |<span data-ttu-id="cd86a-322">La llamada ha fallado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-322">The call failed.</span></span>  <br/> |
|<span data-ttu-id="cd86a-323">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="cd86a-323">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="cd86a-324">Uno o varios parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="cd86a-324">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="cd86a-325">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="cd86a-325">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="cd86a-326">El archivo especificado por  _bstrFileSystemPath_ tiene un ResourceID diferente del especificado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-326">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span> <span data-ttu-id="cd86a-327">Cuando se devuelve este error, se LSCEventType_OnFilePathConflict evento de tipo LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="cd86a-327">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="cd86a-328">Vea [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="cd86a-328">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="cd86a-329">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="cd86a-329">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="cd86a-330">El archivo se eliminó en mitad de la operación.</span><span class="sxs-lookup"><span data-stu-id="cd86a-330">The file was deleted mid-operation.</span></span>  <br/> |
|<span data-ttu-id="cd86a-331">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="cd86a-331">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="cd86a-332">La extensión de archivo determinada no es compatible con el objeto COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="cd86a-332">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="cd86a-333">Vea [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span><span class="sxs-lookup"><span data-stu-id="cd86a-333">See [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span></span>  <br/> |
|<span data-ttu-id="cd86a-334">E_LSC_FILEUPTODATE</span><span class="sxs-lookup"><span data-stu-id="cd86a-334">E_LSC_FILEUPTODATE</span></span>  <br/> |<span data-ttu-id="cd86a-335">El objeto COM no programó una carga porque el archivo de la memoria caché tenía los cambios más recientes del disco.</span><span class="sxs-lookup"><span data-stu-id="cd86a-335">The COM object did not schedule an upload because the file in the cache had the most recent changes from the disk.</span></span>  <br/> |
|<span data-ttu-id="cd86a-336">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="cd86a-336">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="cd86a-337">Falta o se bloquea el _archivo especificado por bstrFileSystemPath._</span><span class="sxs-lookup"><span data-stu-id="cd86a-337">The file specified by  _bstrFileSystemPath_ is missing or locked.</span></span>  <br/> |
|<span data-ttu-id="cd86a-338">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="cd86a-338">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="cd86a-339">El FileSystemPath especificado no se encuentra en la raíz del directorio especificada por FileSystemDirectoryHint cuando se realizó la llamada a Initialize.</span><span class="sxs-lookup"><span data-stu-id="cd86a-339">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="cd86a-340">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="cd86a-340">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="cd86a-341">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-341">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="cd86a-342">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="cd86a-342">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="cd86a-343">El archivo especificado por  _bstrResourceID_ tiene un FileSystemPath diferente del especificado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-343">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="cd86a-344">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="cd86a-344">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="cd86a-345">El archivo especificado ya tiene cambios pendientes en una memoria caché diferente y aún no se puede asociar a la memoria caché del consumidor.</span><span class="sxs-lookup"><span data-stu-id="cd86a-345">The file specified already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="cd86a-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="cd86a-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="cd86a-347">WebPath proporcionado se encuentra en una memoria caché diferente.</span><span class="sxs-lookup"><span data-stu-id="cd86a-347">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="cd86a-348">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd86a-348">S_OK</span></span>  <br/> |<span data-ttu-id="cd86a-349">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="cd86a-349">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a><span data-ttu-id="cd86a-350">ILSCLocalSyncClient::RenameFile</span><span class="sxs-lookup"><span data-stu-id="cd86a-350">ILSCLocalSyncClient::RenameFile</span></span>
<span data-ttu-id="cd86a-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span><span class="sxs-lookup"><span data-stu-id="cd86a-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span></span>

<span data-ttu-id="cd86a-352">RenameFile asociará una nueva dirección URL y una ruta de acceso local para un ResourceID determinado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-352">RenameFile will associate a new URL and local path for a given ResourceID.</span></span> <span data-ttu-id="cd86a-353">Si el archivo especificado por ResourceID aún no existe en la memoria caché, se intentará crearlo y marcarlo para su descarga.</span><span class="sxs-lookup"><span data-stu-id="cd86a-353">If the file specified by the ResourceID doesn't already exist in the cache, an attempt will be made to create it and mark it for download.</span></span>
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a><span data-ttu-id="cd86a-354">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-354">Parameters</span></span>

 <span data-ttu-id="cd86a-355">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="cd86a-355">_bstrResourceID_</span></span>
  
<span data-ttu-id="cd86a-356">Cadena que identifica el ResourceID del archivo.</span><span class="sxs-lookup"><span data-stu-id="cd86a-356">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="cd86a-357">Este valor no debe estar vacío con un máximo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="cd86a-357">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="cd86a-358">_bstrNewFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="cd86a-358">_bstrNewFileSystemPath_</span></span>
  
<span data-ttu-id="cd86a-359">Cadena que especifica la nueva ruta de acceso local para el archivo.</span><span class="sxs-lookup"><span data-stu-id="cd86a-359">A string which specifies the new local path for the file.</span></span> <span data-ttu-id="cd86a-360">Este valor debe ser una ruta de acceso local no vacía con un máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="cd86a-360">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="cd86a-361">Esta ruta de acceso debe estar en el árbol de directorios especificado por FileSystemDirectoryHint cuando se realizó la llamada a Initialize.</span><span class="sxs-lookup"><span data-stu-id="cd86a-361">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span> 
  
 <span data-ttu-id="cd86a-362">_bstrNewWebPath_</span><span class="sxs-lookup"><span data-stu-id="cd86a-362">_bstrNewWebPath_</span></span>
  
<span data-ttu-id="cd86a-363">Cadena que especifica la nueva dirección URL del archivo.</span><span class="sxs-lookup"><span data-stu-id="cd86a-363">A string which specifies the new URL for the file.</span></span> <span data-ttu-id="cd86a-364">Este valor debe ser una dirección URL válida no vacía, pero no más de INTERNET_MAX_URL_LENGTH, tal como se define en https://support.microsoft.com/kb/208427 .</span><span class="sxs-lookup"><span data-stu-id="cd86a-364">This value must be non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
 <span data-ttu-id="cd86a-365">_fBlockUploads_</span><span class="sxs-lookup"><span data-stu-id="cd86a-365">_fBlockUploads_</span></span>
  
<span data-ttu-id="cd86a-366">Especifica si se permiten actualmente las cargas en la nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="cd86a-366">Specifies whether uploads to the new location are allowed currently.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-367">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-367">Return values</span></span>

|<span data-ttu-id="cd86a-368">Valor</span><span class="sxs-lookup"><span data-stu-id="cd86a-368">Value</span></span>|<span data-ttu-id="cd86a-369">Description</span><span class="sxs-lookup"><span data-stu-id="cd86a-369">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd86a-370">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="cd86a-370">E_FAIL</span></span>  <br/> |<span data-ttu-id="cd86a-371">La llamada ha fallado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-371">The call failed.</span></span>  <br/> |
|<span data-ttu-id="cd86a-372">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="cd86a-372">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="cd86a-373">Uno o varios parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="cd86a-373">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="cd86a-374">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="cd86a-374">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="cd86a-375">_BstrNewFileSystemPath_ o _bstrNewWebPath_ ya existen en otro archivo en cualquier caché.</span><span class="sxs-lookup"><span data-stu-id="cd86a-375">The  _bstrNewFileSystemPath_ or  _bstrNewWebPath_ already exist on another file in any cache.</span></span> <span data-ttu-id="cd86a-376">Cuando se devuelve este error, se LSCEventType_OnFilePathConflict evento de tipo LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="cd86a-376">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="cd86a-377">Vea [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="cd86a-377">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="cd86a-378">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="cd86a-378">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="cd86a-379">La información del archivo se eliminó de la memoria caché mientras se ejecutaba este método.</span><span class="sxs-lookup"><span data-stu-id="cd86a-379">The file information was deleted from the cache while this method was running.</span></span>  <br/> |
|<span data-ttu-id="cd86a-380">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="cd86a-380">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="cd86a-381">El FileSystemPath especificado no se encuentra en la raíz del directorio especificada por FileSystemDirectoryHint cuando se realizó la llamada a Initialize.</span><span class="sxs-lookup"><span data-stu-id="cd86a-381">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="cd86a-382">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="cd86a-382">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="cd86a-383">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-383">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="cd86a-384">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="cd86a-384">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="cd86a-385">El archivo especificado se está sincronizando actualmente en una aplicación de Office.</span><span class="sxs-lookup"><span data-stu-id="cd86a-385">The file specified is currently synchronizing in an Office application.</span></span>  <br/> |
|<span data-ttu-id="cd86a-386">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd86a-386">S_OK</span></span>  <br/> |<span data-ttu-id="cd86a-387">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="cd86a-387">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a><span data-ttu-id="cd86a-388">ILSCLocalSyncClient::ResetCache</span><span class="sxs-lookup"><span data-stu-id="cd86a-388">ILSCLocalSyncClient::ResetCache</span></span>
<span data-ttu-id="cd86a-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span><span class="sxs-lookup"><span data-stu-id="cd86a-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span></span>

<span data-ttu-id="cd86a-390">ResetCache eliminará la memoria caché asociada con el SuppliedID que se proporcionó en Initialize.</span><span class="sxs-lookup"><span data-stu-id="cd86a-390">ResetCache will delete the cache associated with the SuppliedID that was provided on Initialize.</span></span> <span data-ttu-id="cd86a-391">Esto incluye toda la información del archivo, pero dejará los archivos en el cliente y en el servidor.</span><span class="sxs-lookup"><span data-stu-id="cd86a-391">This includes all of the file information, but will leave the files on both the client and the server.</span></span> <span data-ttu-id="cd86a-392">Este método también deja el objeto en un estado parcialmente sin inicializar.</span><span class="sxs-lookup"><span data-stu-id="cd86a-392">This method also leaves the object in a partially uninitialized state.</span></span> <span data-ttu-id="cd86a-393">Las únicas llamadas válidas después de esto son [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) o [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="cd86a-393">The only valid calls after this are [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) or [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="cd86a-394">Se puede llamar a este método si se produce un error en Initialize y devuelve E_LSC_CACHEMISMATCH y se eliminará la memoria caché asociada con el SuppliedID que se proporcionó con la llamada con error.</span><span class="sxs-lookup"><span data-stu-id="cd86a-394">This method MAY be called if Initialize fails and returns E_LSC_CACHEMISMATCH, and will delete the cache associated with the SuppliedID that was provided with the failing call.</span></span>
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a><span data-ttu-id="cd86a-395">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-395">Parameters</span></span>

<span data-ttu-id="cd86a-396">Ninguno</span><span class="sxs-lookup"><span data-stu-id="cd86a-396">None</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-397">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-397">Return values</span></span>

|<span data-ttu-id="cd86a-398">Valor</span><span class="sxs-lookup"><span data-stu-id="cd86a-398">Value</span></span>|<span data-ttu-id="cd86a-399">Description</span><span class="sxs-lookup"><span data-stu-id="cd86a-399">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd86a-400">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="cd86a-400">E_FAIL</span></span>  <br/> |<span data-ttu-id="cd86a-401">La llamada ha fallado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-401">The call failed.</span></span>  <br/> |
|<span data-ttu-id="cd86a-402">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="cd86a-402">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="cd86a-403">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-403">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was not successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="cd86a-404">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd86a-404">S_OK</span></span>  <br/> |<span data-ttu-id="cd86a-405">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="cd86a-405">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a><span data-ttu-id="cd86a-406">ILSCLocalSyncClient::ServerFileChange</span><span class="sxs-lookup"><span data-stu-id="cd86a-406">ILSCLocalSyncClient::ServerFileChange</span></span>
<span data-ttu-id="cd86a-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="cd86a-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span></span>

<span data-ttu-id="cd86a-408">ServerFileChange indica al objeto COM CsiSyncClient que marque el archivo especificado para su descarga.</span><span class="sxs-lookup"><span data-stu-id="cd86a-408">ServerFileChange tells the CsiSyncClient COM object to mark the specified file for download.</span></span> <span data-ttu-id="cd86a-409">Si el archivo está abierto en una aplicación de Office para su edición, este método devolverá S_OK sin marcar el archivo para su descarga (la aplicación ya debería realizar este paso si hay cambios).</span><span class="sxs-lookup"><span data-stu-id="cd86a-409">If the file is open in an Office application for edit, this method will return S_OK without marking the file for download (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="cd86a-410">Este método permitirá descargas si se marcó como descargas bloqueadas anteriormente (consulta RenameFile).</span><span class="sxs-lookup"><span data-stu-id="cd86a-410">This method will allow downloads if it was marked as downloads blocked previously (see RenameFile).</span></span>
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="cd86a-411">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-411">Parameters</span></span>

|<span data-ttu-id="cd86a-412">Parámetro</span><span class="sxs-lookup"><span data-stu-id="cd86a-412">Parameter</span></span>|<span data-ttu-id="cd86a-413">Description</span><span class="sxs-lookup"><span data-stu-id="cd86a-413">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd86a-414">bstrFileSystemPath</span><span class="sxs-lookup"><span data-stu-id="cd86a-414">bstrFileSystemPath</span></span>  <br/> |<span data-ttu-id="cd86a-415">Cadena que identifica el archivo en el cliente.</span><span class="sxs-lookup"><span data-stu-id="cd86a-415">A string which identifies the file on the client.</span></span> <span data-ttu-id="cd86a-416">Este valor debe ser una ruta de acceso local no vacía con un máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="cd86a-416">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="cd86a-417">Esta ruta de acceso debe estar en el árbol de directorios especificado por FileSystemDirectoryHint cuando se realizó la llamada a Initialize.</span><span class="sxs-lookup"><span data-stu-id="cd86a-417">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="cd86a-418">bstrResourceID</span><span class="sxs-lookup"><span data-stu-id="cd86a-418">bstrResourceID</span></span>  <br/> |<span data-ttu-id="cd86a-419">Cadena que identifica el ResourceID del archivo.</span><span class="sxs-lookup"><span data-stu-id="cd86a-419">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="cd86a-420">Este valor no debe estar vacío con un máximo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="cd86a-420">This value must be non-empty with a maximum of 128 characters.</span></span>  <br/> |
|<span data-ttu-id="cd86a-421">bstrWebPath</span><span class="sxs-lookup"><span data-stu-id="cd86a-421">bstrWebPath</span></span>  <br/> |<span data-ttu-id="cd86a-422">Cadena que identifica el archivo en el servidor.</span><span class="sxs-lookup"><span data-stu-id="cd86a-422">A string which identifies the file on the server.</span></span> <span data-ttu-id="cd86a-423">Este valor debe ser una dirección URL válida no vacía, pero no más de INTERNET_MAX_URL_LENGTH, tal como se define en https://support.microsoft.com/kb/208427 .</span><span class="sxs-lookup"><span data-stu-id="cd86a-423">This value must be a non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span>  <br/> |
   
##### <a name="return-values"></a><span data-ttu-id="cd86a-424">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-424">Return values</span></span>

|<span data-ttu-id="cd86a-425">Valor</span><span class="sxs-lookup"><span data-stu-id="cd86a-425">Value</span></span>|<span data-ttu-id="cd86a-426">Description</span><span class="sxs-lookup"><span data-stu-id="cd86a-426">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd86a-427">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="cd86a-427">E_FAIL</span></span>  <br/> |<span data-ttu-id="cd86a-428">Error al establecer el estado de conectividad de caché.</span><span class="sxs-lookup"><span data-stu-id="cd86a-428">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="cd86a-429">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="cd86a-429">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="cd86a-430">El archivo especificado por  _bstrFileSystemPath_ tiene un ResourceID diferente del especificado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-430">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span>  <br/> |
|<span data-ttu-id="cd86a-431">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="cd86a-431">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="cd86a-432">La extensión de archivo determinada no es compatible con el objeto COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="cd86a-432">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="cd86a-433">Vea GetSupportedFileExtensions.</span><span class="sxs-lookup"><span data-stu-id="cd86a-433">See GetSupportedFileExtensions.</span></span>  <br/> |
|<span data-ttu-id="cd86a-434">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="cd86a-434">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="cd86a-435">El archivo se eliminó en mitad de la operación.</span><span class="sxs-lookup"><span data-stu-id="cd86a-435">The file was deleted in mid-operation.</span></span>  <br/> |
|<span data-ttu-id="cd86a-436">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="cd86a-436">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="cd86a-437">Uno o varios parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="cd86a-437">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="cd86a-438">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="cd86a-438">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="cd86a-439">El FileSystemPath especificado no se encuentra en la raíz del directorio especificada por FileSystemDirectoryHint cuando se realizó la llamada a Initialize.</span><span class="sxs-lookup"><span data-stu-id="cd86a-439">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="cd86a-440">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="cd86a-440">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="cd86a-441">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-441">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="cd86a-442">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="cd86a-442">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="cd86a-443">El archivo especificado por  _bstrResourceID_ tiene un FileSystemPath diferente del especificado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-443">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="cd86a-444">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="cd86a-444">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="cd86a-445">El archivo especificado ya tiene cambios pendientes en una memoria caché diferente y aún no se puede asociar a la memoria caché del consumidor.</span><span class="sxs-lookup"><span data-stu-id="cd86a-445">The specified file already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="cd86a-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="cd86a-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="cd86a-447">WebPath proporcionado se encuentra en una memoria caché diferente.</span><span class="sxs-lookup"><span data-stu-id="cd86a-447">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="cd86a-448">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd86a-448">S_OK</span></span>  <br/> |<span data-ttu-id="cd86a-449">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="cd86a-449">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a><span data-ttu-id="cd86a-450">ILSCLocalSyncClient::SetClientConnectivityState</span><span class="sxs-lookup"><span data-stu-id="cd86a-450">ILSCLocalSyncClient::SetClientConnectivityState</span></span>
<span data-ttu-id="cd86a-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="cd86a-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span></span>

<span data-ttu-id="cd86a-452">Establece la memoria caché en un estado en línea o sin conexión.</span><span class="sxs-lookup"><span data-stu-id="cd86a-452">Sets the cache into an online or offline state.</span></span> <span data-ttu-id="cd86a-453">Si está sin conexión, Office no intentará comunicarse con el servidor para los archivos de esa memoria caché, independientemente de la configuración  _fBlockUploads_ de cada archivo individual.</span><span class="sxs-lookup"><span data-stu-id="cd86a-453">If offline, Office will not attempt to communicate with the server for any files in that cache, regardless of each individual file's  _fBlockUploads_ setting.</span></span> 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a><span data-ttu-id="cd86a-454">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-454">Parameters</span></span>

 <span data-ttu-id="cd86a-455">_fIsOnline_</span><span class="sxs-lookup"><span data-stu-id="cd86a-455">_fIsOnline_</span></span>
  
<span data-ttu-id="cd86a-456">Booleano que determina el estado de conectividad de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="cd86a-456">A boolean determining the connectivity state of the cache.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-457">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-457">Return values</span></span>

|<span data-ttu-id="cd86a-458">Valor</span><span class="sxs-lookup"><span data-stu-id="cd86a-458">Value</span></span>|<span data-ttu-id="cd86a-459">Description</span><span class="sxs-lookup"><span data-stu-id="cd86a-459">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd86a-460">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="cd86a-460">E_FAIL</span></span>  <br/> |<span data-ttu-id="cd86a-461">Error al establecer el estado de conectividad de caché.</span><span class="sxs-lookup"><span data-stu-id="cd86a-461">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="cd86a-462">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="cd86a-462">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="cd86a-463">Uno o varios parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="cd86a-463">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="cd86a-464">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="cd86a-464">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="cd86a-465">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-465">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="cd86a-466">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd86a-466">S_OK</span></span>  <br/> |<span data-ttu-id="cd86a-467">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="cd86a-467">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a><span data-ttu-id="cd86a-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="cd86a-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span></span>
<span data-ttu-id="cd86a-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="cd86a-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span></span>

<span data-ttu-id="cd86a-470">SetClientNetworkSyncPermission se usa para invalidar o restaurar la heurística de sincronización deOffice para el uso de energía y costo de red.</span><span class="sxs-lookup"><span data-stu-id="cd86a-470">SetClientNetworkSyncPermission is used to either override or restoreOffice's synchronizing heuristics for network cost and power usage.</span></span> <span data-ttu-id="cd86a-471">Cuando se encuentra en una 3G u otra red de alto costo, o cuando se ejecuta con batería frente a estar conectado, Office puede optar por bloquear el tráfico de red hasta un momento más oportuno.</span><span class="sxs-lookup"><span data-stu-id="cd86a-471">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span> <span data-ttu-id="cd86a-472">El consumidor de esta API puede usarla para invalidar la heurística de Office y forzar la sincronización para que se produzca.</span><span class="sxs-lookup"><span data-stu-id="cd86a-472">The consumer of this API can use it to override Office's heuristics and force synchronizing to occur.</span></span>
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a><span data-ttu-id="cd86a-473">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-473">Parameters</span></span>

 <span data-ttu-id="cd86a-474">_nspType_</span><span class="sxs-lookup"><span data-stu-id="cd86a-474">_nspType_</span></span>
  
<span data-ttu-id="cd86a-475">Marca que define el costo heurístico que se va a invalidar.</span><span class="sxs-lookup"><span data-stu-id="cd86a-475">A flag which defines which cost heuristic to override.</span></span> <span data-ttu-id="cd86a-476">Vea [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="cd86a-476">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span>
  
 <span data-ttu-id="cd86a-477">_fEnableSync_</span><span class="sxs-lookup"><span data-stu-id="cd86a-477">_fEnableSync_</span></span>
  
<span data-ttu-id="cd86a-478">Especifica si se debe forzar la sincronización, lo que invalida ese costo heurístico o si ya no se reemplaza.</span><span class="sxs-lookup"><span data-stu-id="cd86a-478">Specifies whether to force synchronizing on, thus overriding that cost heuristic, or to no longer override it.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-479">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-479">Return values</span></span>

|<span data-ttu-id="cd86a-480">Valor</span><span class="sxs-lookup"><span data-stu-id="cd86a-480">Value</span></span>|<span data-ttu-id="cd86a-481">Description</span><span class="sxs-lookup"><span data-stu-id="cd86a-481">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd86a-482">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="cd86a-482">E_FAIL</span></span>  <br/> |<span data-ttu-id="cd86a-483">Error al invalidar la heurística de sincronización.</span><span class="sxs-lookup"><span data-stu-id="cd86a-483">Failure to override synchronizing heuristics.</span></span>  <br/> |
|<span data-ttu-id="cd86a-484">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="cd86a-484">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="cd86a-485">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-485">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="cd86a-486">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd86a-486">S_OK</span></span>  <br/> |<span data-ttu-id="cd86a-487">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="cd86a-487">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a><span data-ttu-id="cd86a-488">ILSCLocalSyncClient::Uninitialize</span><span class="sxs-lookup"><span data-stu-id="cd86a-488">ILSCLocalSyncClient::Uninitialize</span></span>
<span data-ttu-id="cd86a-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span><span class="sxs-lookup"><span data-stu-id="cd86a-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span></span>

<span data-ttu-id="cd86a-490">Descarga la memoria caché del objeto COM y realiza operaciones de cierre.</span><span class="sxs-lookup"><span data-stu-id="cd86a-490">Unloads the cache from the COM object and perform closing operations.</span></span> <span data-ttu-id="cd86a-491">[ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) DEBE llamarse antes de destruir el objeto COM.</span><span class="sxs-lookup"><span data-stu-id="cd86a-491">[ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUST be called before destroying the COM object.</span></span> <span data-ttu-id="cd86a-492">Una vez que se llama, no se puede llamar a ninguna otra API, el objeto COM DEBE destruirse y crearse uno nuevo si desea continuar las operaciones.</span><span class="sxs-lookup"><span data-stu-id="cd86a-492">Once called, no other APIs can be called, the COM object MUST be destroyed and a new one created if you wish to continue operations.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a><span data-ttu-id="cd86a-493">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-493">Parameters</span></span>

<span data-ttu-id="cd86a-494">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cd86a-494">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-495">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-495">Return values</span></span>

|<span data-ttu-id="cd86a-496">Valor</span><span class="sxs-lookup"><span data-stu-id="cd86a-496">Value</span></span>|<span data-ttu-id="cd86a-497">Description</span><span class="sxs-lookup"><span data-stu-id="cd86a-497">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd86a-498">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="cd86a-498">E_FAIL</span></span>  <br/> |<span data-ttu-id="cd86a-499">Error al no inicializar.</span><span class="sxs-lookup"><span data-stu-id="cd86a-499">Failure to uninitialize.</span></span>  <br/> |
|<span data-ttu-id="cd86a-500">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="cd86a-500">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="cd86a-501">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) no se ha llamado correctamente en el pasado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-501">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="cd86a-502">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd86a-502">S_OK</span></span>  <br/> |<span data-ttu-id="cd86a-503">La llamada ha sido correcta.</span><span class="sxs-lookup"><span data-stu-id="cd86a-503">The call succeeded.</span></span>  <br/> |
   
### <a name="interface-ienumlscevent"></a><span data-ttu-id="cd86a-504">Interfaz IEnumLSCEvent</span><span class="sxs-lookup"><span data-stu-id="cd86a-504">Interface IEnumLSCEvent</span></span>

<span data-ttu-id="cd86a-505">Esta interfaz representa una lista de eventos ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="cd86a-505">This interface represents a list of ILSCEvent events.</span></span>
  
<span data-ttu-id="cd86a-506">**Funciones de miembros públicos**</span><span class="sxs-lookup"><span data-stu-id="cd86a-506">**Public member functions**</span></span>

#### <a name="ienumlsceventfnext"></a><span data-ttu-id="cd86a-507">IEnumLSCEvent::FNext</span><span class="sxs-lookup"><span data-stu-id="cd86a-507">IEnumLSCEvent::FNext</span></span>

<span data-ttu-id="cd86a-508">Recupera el siguiente evento de la lista de eventos.</span><span class="sxs-lookup"><span data-stu-id="cd86a-508">Retrieves the next event from the list of events.</span></span>
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a><span data-ttu-id="cd86a-509">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-509">Parameters</span></span>

 <span data-ttu-id="cd86a-510">_ppiLSCEvent_</span><span class="sxs-lookup"><span data-stu-id="cd86a-510">_ppiLSCEvent_</span></span>
  
<span data-ttu-id="cd86a-511">Puntero a una interfaz ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="cd86a-511">A pointer to an ILSCEvent interface.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-512">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-512">Return values</span></span>

|<span data-ttu-id="cd86a-513">Valor</span><span class="sxs-lookup"><span data-stu-id="cd86a-513">Value</span></span>|<span data-ttu-id="cd86a-514">Description</span><span class="sxs-lookup"><span data-stu-id="cd86a-514">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd86a-515">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="cd86a-515">E_FAIL</span></span>  <br/> |<span data-ttu-id="cd86a-516">No hay más eventos.</span><span class="sxs-lookup"><span data-stu-id="cd86a-516">There are no more events.</span></span>  <br/> |
|<span data-ttu-id="cd86a-517">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd86a-517">S_OK</span></span>  <br/> |<span data-ttu-id="cd86a-518">La llamada se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="cd86a-518">The call was successful.</span></span>  <br/> |
   
#### <a name="ienumlsceventreset"></a><span data-ttu-id="cd86a-519">IEnumLSCEvent::Reset</span><span class="sxs-lookup"><span data-stu-id="cd86a-519">IEnumLSCEvent::Reset</span></span>

<span data-ttu-id="cd86a-520">Restablece el enumerador al primer evento.</span><span class="sxs-lookup"><span data-stu-id="cd86a-520">Resets the enumerator to the first event.</span></span>
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a><span data-ttu-id="cd86a-521">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-521">Parameters</span></span>

<span data-ttu-id="cd86a-522">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cd86a-522">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-523">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-523">Return values</span></span>

<span data-ttu-id="cd86a-524">Siempre devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="cd86a-524">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent"></a><span data-ttu-id="cd86a-525">Interfaz ILSCEvent</span><span class="sxs-lookup"><span data-stu-id="cd86a-525">Interface ILSCEvent</span></span>

<span data-ttu-id="cd86a-526">Esta interfaz representa un evento de sincronización.</span><span class="sxs-lookup"><span data-stu-id="cd86a-526">This interface represents a synchronizing event.</span></span> <span data-ttu-id="cd86a-527">Toda la información sobre el evento se puede recuperar desde la interfaz.</span><span class="sxs-lookup"><span data-stu-id="cd86a-527">All information about the event can be retrieved from the interface.</span></span>
  
<span data-ttu-id="cd86a-528">**Funciones de miembros públicos**</span><span class="sxs-lookup"><span data-stu-id="cd86a-528">**Public member functions**</span></span>

#### <a name="ilsceventgetconflictstatus"></a><span data-ttu-id="cd86a-529">ILSCEvent::GetConflictStatus</span><span class="sxs-lookup"><span data-stu-id="cd86a-529">ILSCEvent::GetConflictStatus</span></span>

<span data-ttu-id="cd86a-530">Tenga en cuenta que este valor se rellena cuando se llama a [ILSCLocalSyncClient::GetChanges, ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) no cuando se creó el evento, por lo que solo tendrá el estado actual del archivo, no el estado del archivo cuando cambió el estado del conflicto.</span><span class="sxs-lookup"><span data-stu-id="cd86a-530">Note that this value is populated when [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) is called, not when the event was created, so you will only have the current status of the file, not the status of the file when the conflict status changed.</span></span> 
  
<span data-ttu-id="cd86a-531">Este valor solo se rellena cuando [la enumeración LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento es LSCEventType_OnLocalConflictStateChanged.</span><span class="sxs-lookup"><span data-stu-id="cd86a-531">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnLocalConflictStateChanged.</span></span> 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a><span data-ttu-id="cd86a-532">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-532">Parameters</span></span>

 <span data-ttu-id="cd86a-533">_pfIsInConflict_</span><span class="sxs-lookup"><span data-stu-id="cd86a-533">_pfIsInConflict_</span></span>
  
<span data-ttu-id="cd86a-534">El estado de conflicto actual del archivo asociado al evento.</span><span class="sxs-lookup"><span data-stu-id="cd86a-534">The current conflict status of the file associated with the event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-535">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-535">Return values</span></span>

<span data-ttu-id="cd86a-536">Siempre devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="cd86a-536">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeterror"></a><span data-ttu-id="cd86a-537">ILSCEvent::GetError</span><span class="sxs-lookup"><span data-stu-id="cd86a-537">ILSCEvent::GetError</span></span>

<span data-ttu-id="cd86a-538">Este valor solo se rellena cuando [la enumeración LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento es LSCEventType_OnServerChangesDownloaded o LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="cd86a-538">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a><span data-ttu-id="cd86a-539">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-539">Parameters</span></span>

 <span data-ttu-id="cd86a-540">_pnError_</span><span class="sxs-lookup"><span data-stu-id="cd86a-540">_pnError_</span></span>
  
<span data-ttu-id="cd86a-541">Error asociado a este evento.</span><span class="sxs-lookup"><span data-stu-id="cd86a-541">The error associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-542">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-542">Return values</span></span>

<span data-ttu-id="cd86a-543">Siempre devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="cd86a-543">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetetag"></a><span data-ttu-id="cd86a-544">ILSCEvent::GetETag</span><span class="sxs-lookup"><span data-stu-id="cd86a-544">ILSCEvent::GetETag</span></span>

<span data-ttu-id="cd86a-545">Este valor solo se rellena cuando [la enumeración LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento es LSCEventType_OnServerChangesDownloaded o LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="cd86a-545">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a><span data-ttu-id="cd86a-546">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-546">Parameters</span></span>

 <span data-ttu-id="cd86a-547">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="cd86a-547">_pbstrETag_</span></span>
  
<span data-ttu-id="cd86a-548">ETag asociado a este evento</span><span class="sxs-lookup"><span data-stu-id="cd86a-548">The ETag associated with this event</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-549">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-549">Return values</span></span>

<span data-ttu-id="cd86a-550">Siempre devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="cd86a-550">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeteventtype"></a><span data-ttu-id="cd86a-551">ILSCEvent::GetEventType</span><span class="sxs-lookup"><span data-stu-id="cd86a-551">ILSCEvent::GetEventType</span></span>

<span data-ttu-id="cd86a-552">Obtiene el tipo de este evento.</span><span class="sxs-lookup"><span data-stu-id="cd86a-552">Gets the type for this event.</span></span>
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a><span data-ttu-id="cd86a-553">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-553">Parameters</span></span>

 <span data-ttu-id="cd86a-554">_pnEventType_</span><span class="sxs-lookup"><span data-stu-id="cd86a-554">_pnEventType_</span></span>
  
<span data-ttu-id="cd86a-555">El tipo de evento de este evento.</span><span class="sxs-lookup"><span data-stu-id="cd86a-555">The event type of this event.</span></span> <span data-ttu-id="cd86a-556">Vea [Enum LSCEventType para](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) obtener valores válidos.</span><span class="sxs-lookup"><span data-stu-id="cd86a-556">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for valid values.</span></span> <span data-ttu-id="cd86a-557">No debe ser null.</span><span class="sxs-lookup"><span data-stu-id="cd86a-557">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-558">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-558">Return values</span></span>

|<span data-ttu-id="cd86a-559">Valor</span><span class="sxs-lookup"><span data-stu-id="cd86a-559">Value</span></span>|<span data-ttu-id="cd86a-560">Description</span><span class="sxs-lookup"><span data-stu-id="cd86a-560">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd86a-561">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="cd86a-561">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="cd86a-562">Uno o varios parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="cd86a-562">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="cd86a-563">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd86a-563">S_OK</span></span>  <br/> |<span data-ttu-id="cd86a-564">La llamada se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="cd86a-564">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a><span data-ttu-id="cd86a-565">ILSCEvent::GetLocalWorkingPath</span><span class="sxs-lookup"><span data-stu-id="cd86a-565">ILSCEvent::GetLocalWorkingPath</span></span>

<span data-ttu-id="cd86a-566">Obtiene la ruta de trabajo local para este evento.</span><span class="sxs-lookup"><span data-stu-id="cd86a-566">Gets the local working path for this event.</span></span>
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a><span data-ttu-id="cd86a-567">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-567">Parameters</span></span>

 <span data-ttu-id="cd86a-568">_pbstrLocalWorkingPath_</span><span class="sxs-lookup"><span data-stu-id="cd86a-568">_pbstrLocalWorkingPath_</span></span>
  
<span data-ttu-id="cd86a-569">La ruta de acceso local del archivo al que pertenece este evento.</span><span class="sxs-lookup"><span data-stu-id="cd86a-569">The local path of the file to which this event pertains.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-570">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-570">Return values</span></span>

<span data-ttu-id="cd86a-571">Siempre devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="cd86a-571">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceid"></a><span data-ttu-id="cd86a-572">ILSCEvent::GetResourceID</span><span class="sxs-lookup"><span data-stu-id="cd86a-572">ILSCEvent::GetResourceID</span></span>

<span data-ttu-id="cd86a-573">Obtiene el identificador de recurso para el evento.</span><span class="sxs-lookup"><span data-stu-id="cd86a-573">Gets the resource ID for the event.</span></span>
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="cd86a-574">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-574">Parameters</span></span>

 <span data-ttu-id="cd86a-575">_pbstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="cd86a-575">_pbstrResourceID_</span></span>
  
<span data-ttu-id="cd86a-576">ResourceID del archivo asociado a este evento.</span><span class="sxs-lookup"><span data-stu-id="cd86a-576">The ResourceID of the file associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-577">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-577">Return values</span></span>

<span data-ttu-id="cd86a-578">Siempre devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="cd86a-578">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceidattempted"></a><span data-ttu-id="cd86a-579">ILSCEvent::GetResourceIDAttempted</span><span class="sxs-lookup"><span data-stu-id="cd86a-579">ILSCEvent::GetResourceIDAttempted</span></span>

<span data-ttu-id="cd86a-580">Este valor solo se rellena cuando [el parámetro Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="cd86a-580">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> <span data-ttu-id="cd86a-581">Cuando una llamada a [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)o [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) provocaría una colisión de ruta de acceso web o ruta de acceso local con otro archivo en la memoria caché de archivos de Office, se genera este evento.</span><span class="sxs-lookup"><span data-stu-id="cd86a-581">When a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) would cause a Web Path or Local Path collision with another file in the Office file cache, this event is generated.</span></span> 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a><span data-ttu-id="cd86a-582">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-582">Parameters</span></span>

 <span data-ttu-id="cd86a-583">_pbstrResourceIDAttempted_</span><span class="sxs-lookup"><span data-stu-id="cd86a-583">_pbstrResourceIDAttempted_</span></span>
  
<span data-ttu-id="cd86a-584">ResourceID que provocó que se generara este evento.</span><span class="sxs-lookup"><span data-stu-id="cd86a-584">The ResourceID that caused this event to get generated.</span></span> <span data-ttu-id="cd86a-585">No debe ser null.</span><span class="sxs-lookup"><span data-stu-id="cd86a-585">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-586">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-586">Return values</span></span>

<span data-ttu-id="cd86a-587">Siempre devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="cd86a-587">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetsyncerrortype"></a><span data-ttu-id="cd86a-588">ILSCEvent::GetSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="cd86a-588">ILSCEvent::GetSyncErrorType</span></span>

<span data-ttu-id="cd86a-589">Este valor solo se rellena cuando [la enumeración LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento es LSCEventType_OnServerChangesDownloaded o LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="cd86a-589">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a><span data-ttu-id="cd86a-590">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-590">Parameters</span></span>

 <span data-ttu-id="cd86a-591">_pnSyncErrorType_</span><span class="sxs-lookup"><span data-stu-id="cd86a-591">_pnSyncErrorType_</span></span>
  
<span data-ttu-id="cd86a-592">Tipo de error asociado a este evento.</span><span class="sxs-lookup"><span data-stu-id="cd86a-592">The error type associated with this event.</span></span> <span data-ttu-id="cd86a-593">Vea [Enum LSCEventType para](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) obtener los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="cd86a-593">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for potential values.</span></span> <span data-ttu-id="cd86a-594">No debe ser null.</span><span class="sxs-lookup"><span data-stu-id="cd86a-594">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-595">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-595">Return values</span></span>

|<span data-ttu-id="cd86a-596">Valor</span><span class="sxs-lookup"><span data-stu-id="cd86a-596">Value</span></span>|<span data-ttu-id="cd86a-597">Description</span><span class="sxs-lookup"><span data-stu-id="cd86a-597">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd86a-598">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="cd86a-598">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="cd86a-599">Uno o varios parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="cd86a-599">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="cd86a-600">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd86a-600">S_OK</span></span>  <br/> |<span data-ttu-id="cd86a-601">La llamada se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="cd86a-601">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetwebpath"></a><span data-ttu-id="cd86a-602">ILSCEvent::GetWebPath</span><span class="sxs-lookup"><span data-stu-id="cd86a-602">ILSCEvent::GetWebPath</span></span>

<span data-ttu-id="cd86a-603">Este valor solo se rellena cuando [el parámetro Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) del evento LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="cd86a-603">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a><span data-ttu-id="cd86a-604">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-604">Parameters</span></span>

 <span data-ttu-id="cd86a-605">_pbstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="cd86a-605">_pbstrWebPath_</span></span>
  
<span data-ttu-id="cd86a-606">Especifica la ruta de acceso web asociada a este evento.</span><span class="sxs-lookup"><span data-stu-id="cd86a-606">Specifies the Web Path associated with this event.</span></span> <span data-ttu-id="cd86a-607">No debe ser null.</span><span class="sxs-lookup"><span data-stu-id="cd86a-607">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-608">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-608">Return values</span></span>

<span data-ttu-id="cd86a-609">Siempre devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="cd86a-609">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent2"></a><span data-ttu-id="cd86a-610">Interfaz ILSCEvent2</span><span class="sxs-lookup"><span data-stu-id="cd86a-610">Interface ILSCEvent2</span></span>

<span data-ttu-id="cd86a-611">Esta interfaz contiene información adicional sobre un evento de sincronización.</span><span class="sxs-lookup"><span data-stu-id="cd86a-611">This interface holds additional information about a synchronizing event.</span></span>
  
<span data-ttu-id="cd86a-612">**Funciones de miembros públicos**</span><span class="sxs-lookup"><span data-stu-id="cd86a-612">**Public member functions**</span></span>

#### <a name="ilscevent2geterrorchain"></a><span data-ttu-id="cd86a-613">ILSCEvent2::GetErrorChain</span><span class="sxs-lookup"><span data-stu-id="cd86a-613">ILSCEvent2::GetErrorChain</span></span>

<span data-ttu-id="cd86a-614">Obtiene la información de la cadena de errores acerca de un evento de sincronización.</span><span class="sxs-lookup"><span data-stu-id="cd86a-614">Gets the error chain information about a synchronizing event.</span></span>
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a><span data-ttu-id="cd86a-615">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-615">Parameters</span></span>

 <span data-ttu-id="cd86a-616">_pbstrErrorChain_</span><span class="sxs-lookup"><span data-stu-id="cd86a-616">_pbstrErrorChain_</span></span>
  
<span data-ttu-id="cd86a-617">Cadena que contiene la información de la cadena de errores.</span><span class="sxs-lookup"><span data-stu-id="cd86a-617">A string to hold the error chain information.</span></span> <span data-ttu-id="cd86a-618">No debe ser null.</span><span class="sxs-lookup"><span data-stu-id="cd86a-618">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-619">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-619">Return values</span></span>

|<span data-ttu-id="cd86a-620">Valor</span><span class="sxs-lookup"><span data-stu-id="cd86a-620">Value</span></span>|<span data-ttu-id="cd86a-621">Description</span><span class="sxs-lookup"><span data-stu-id="cd86a-621">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd86a-622">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="cd86a-622">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="cd86a-623">La versión instalada de Office no admite esta interfaz</span><span class="sxs-lookup"><span data-stu-id="cd86a-623">The installed version of Office does not support this interface</span></span>  <br/> |
|<span data-ttu-id="cd86a-624">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="cd86a-624">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="cd86a-625">Uno o varios de los valores de parámetro no son válidos.</span><span class="sxs-lookup"><span data-stu-id="cd86a-625">One or more of the parameter values are invalid.</span></span>  <br/> |
|<span data-ttu-id="cd86a-626">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="cd86a-626">E_FAIL</span></span>  <br/> |<span data-ttu-id="cd86a-627">La información de la cadena de errores no está disponible.</span><span class="sxs-lookup"><span data-stu-id="cd86a-627">The error chain information is not available.</span></span>  <br/> |
|<span data-ttu-id="cd86a-628">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd86a-628">S_OK</span></span>  <br/> |<span data-ttu-id="cd86a-629">La llamada se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="cd86a-629">The call was successful.</span></span>  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a><span data-ttu-id="cd86a-630">Interfaz IPartnerActivityCallback</span><span class="sxs-lookup"><span data-stu-id="cd86a-630">Interface IPartnerActivityCallback</span></span>

<span data-ttu-id="cd86a-631">Esta interfaz proporciona una función de devolución de llamada al objeto COM CSISyncClient.</span><span class="sxs-lookup"><span data-stu-id="cd86a-631">This interface provides a callback function to the CSISyncClient COM object.</span></span>
  
<span data-ttu-id="cd86a-632">**Funciones de miembros públicos**</span><span class="sxs-lookup"><span data-stu-id="cd86a-632">**Public member functions**</span></span>

#### <a name="ipartneractivitycallbackeventoccurred"></a><span data-ttu-id="cd86a-633">IPartnerActivityCallback::EventOccurred</span><span class="sxs-lookup"><span data-stu-id="cd86a-633">IPartnerActivityCallback::EventOccurred</span></span>

<span data-ttu-id="cd86a-634">Se trata de una función de devolución de llamada en el objeto dado al objeto COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="cd86a-634">This is a callback function on the object given to the CsiSyncClient COM object.</span></span> <span data-ttu-id="cd86a-635">Se espera que cuando se produzca un evento (vea [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) para tipos de eventos válidos), el objeto COM CsiSyncClient llamará a este método y señalizará al consumidor.</span><span class="sxs-lookup"><span data-stu-id="cd86a-635">It's expected that when an Event occurs (see [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid event types), the CsiSyncClient COM object will call this method, signalling the consumer.</span></span> 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a><span data-ttu-id="cd86a-636">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd86a-636">Parameters</span></span>

 <span data-ttu-id="cd86a-637">_eEventTypeOccurred_</span><span class="sxs-lookup"><span data-stu-id="cd86a-637">_eEventTypeOccurred_</span></span>
  
<span data-ttu-id="cd86a-638">El tipo de evento de este evento.</span><span class="sxs-lookup"><span data-stu-id="cd86a-638">The event type of this event.</span></span> <span data-ttu-id="cd86a-639">Vea [Enum LSCEventTypeOccurred para](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) obtener valores válidos.</span><span class="sxs-lookup"><span data-stu-id="cd86a-639">See [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid values.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="cd86a-640">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="cd86a-640">Return values</span></span>

<span data-ttu-id="cd86a-641">Siempre devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="cd86a-641">Always returns S_OK.</span></span>
  
## <a name="enumerations"></a><span data-ttu-id="cd86a-642">Enumeraciones</span><span class="sxs-lookup"><span data-stu-id="cd86a-642">Enumerations</span></span>

<span data-ttu-id="cd86a-643">CSISyncClient usa las enumeraciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="cd86a-643">CSISyncClient uses the following enumerations.</span></span>
  
### <a name="enum-lsceventsyncerrortype"></a><span data-ttu-id="cd86a-644">Enum LSCEventSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="cd86a-644">Enum LSCEventSyncErrorType</span></span>
<span data-ttu-id="cd86a-645"><a name="Enum_LSCEventSyncErrorType"> </a></span><span class="sxs-lookup"><span data-stu-id="cd86a-645"><a name="Enum_LSCEventSyncErrorType"> </a></span></span>

<span data-ttu-id="cd86a-646">Esta enumeración especifica las categorías de errores que pueden producirse al sincronizar un archivo.</span><span class="sxs-lookup"><span data-stu-id="cd86a-646">This enumeration specifies the categories of errors that can occur while synchronizing a file.</span></span>
  
|<span data-ttu-id="cd86a-647">Enumerator</span><span class="sxs-lookup"><span data-stu-id="cd86a-647">Enumerator</span></span>|<span data-ttu-id="cd86a-648">Description</span><span class="sxs-lookup"><span data-stu-id="cd86a-648">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd86a-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span><span class="sxs-lookup"><span data-stu-id="cd86a-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span></span>  <br/> |<span data-ttu-id="cd86a-650">El error de sincronización de este evento fue inesperado y puede requerir una consideración especial.</span><span class="sxs-lookup"><span data-stu-id="cd86a-650">The synchronizing error of this event was unexpected, and may require special consideration.</span></span> <span data-ttu-id="cd86a-651">De forma predeterminada, es posible que el usuario tenga que intervenir.</span><span class="sxs-lookup"><span data-stu-id="cd86a-651">By default, the user may have to intervene.</span></span>  <br/> |
|<span data-ttu-id="cd86a-652">LSCEventSyncErrorType_NoInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="cd86a-652">LSCEventSyncErrorType_NoInterventionRequired</span></span>  <br/> |<span data-ttu-id="cd86a-653">El error de sincronización de este evento no necesita una consideración especial.</span><span class="sxs-lookup"><span data-stu-id="cd86a-653">The synchronizing error of this event does not need special consideration.</span></span> <span data-ttu-id="cd86a-654">Office lo controlará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="cd86a-654">Office will handle it automatically.</span></span>  <br/> |
|<span data-ttu-id="cd86a-655">LSCEventSyncErrorType_UserInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="cd86a-655">LSCEventSyncErrorType_UserInterventionRequired</span></span>  <br/> |<span data-ttu-id="cd86a-656">El error de sincronización de este evento requiere que un usuario lo resuelva.</span><span class="sxs-lookup"><span data-stu-id="cd86a-656">The synchronizing error of this event requires a user to resolve it.</span></span> <span data-ttu-id="cd86a-657">Por ejemplo, el error de conflicto de combinación requiere que un usuario abra el documento y lo combine.</span><span class="sxs-lookup"><span data-stu-id="cd86a-657">For example, merge conflict error requires a user to open the document and merge it.</span></span>  <br/> |
|<span data-ttu-id="cd86a-658">LSCEventSyncErrorType_WaitingOnClient</span><span class="sxs-lookup"><span data-stu-id="cd86a-658">LSCEventSyncErrorType_WaitingOnClient</span></span>  <br/> |<span data-ttu-id="cd86a-659">El error de sincronización de este evento requiere que el consumidor intervenga, pero no debe requerir una consideración especial por parte del usuario.</span><span class="sxs-lookup"><span data-stu-id="cd86a-659">The synchronizing error of this event requires the consumer to intervene, but should not require special consideration by the user.</span></span>  <br/> |
|<span data-ttu-id="cd86a-660">LSCEventSyncErrorType_ClientInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="cd86a-660">LSCEventSyncErrorType_ClientInterventionRequired</span></span>  <br/> |<span data-ttu-id="cd86a-661">El error de sincronización de este evento requiere que el consumidor intervenga como caso especial.</span><span class="sxs-lookup"><span data-stu-id="cd86a-661">The synchronizing error of this event requires the consumer to intervene as a special case.</span></span>  <br/> |
|<span data-ttu-id="cd86a-662">LSCEventSyncErrorType_Max</span><span class="sxs-lookup"><span data-stu-id="cd86a-662">LSCEventSyncErrorType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtype"></a><span data-ttu-id="cd86a-663">Enum LSCEventType</span><span class="sxs-lookup"><span data-stu-id="cd86a-663">Enum LSCEventType</span></span>
<span data-ttu-id="cd86a-664"><a name="Enum_LSCEventType"> </a></span><span class="sxs-lookup"><span data-stu-id="cd86a-664"><a name="Enum_LSCEventType"> </a></span></span>

<span data-ttu-id="cd86a-665">Esta enumeración especifica el tipo de eventos que pueden producirse para un archivo determinado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-665">This enumeration specifies the type of events that can occur for a particular file.</span></span>
  
|<span data-ttu-id="cd86a-666">Enumerator</span><span class="sxs-lookup"><span data-stu-id="cd86a-666">Enumerator</span></span>|<span data-ttu-id="cd86a-667">Description</span><span class="sxs-lookup"><span data-stu-id="cd86a-667">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd86a-668">LSCEventType_None</span><span class="sxs-lookup"><span data-stu-id="cd86a-668">LSCEventType_None</span></span>  <br/> ||
|<span data-ttu-id="cd86a-669">LSCEventType_OnLocalChanges</span><span class="sxs-lookup"><span data-stu-id="cd86a-669">LSCEventType_OnLocalChanges</span></span>  <br/> |<span data-ttu-id="cd86a-670">Se realizaron cambios en un archivo local.</span><span class="sxs-lookup"><span data-stu-id="cd86a-670">Changes were made to a local file.</span></span>  <br/> |
|<span data-ttu-id="cd86a-671">LSCEventType_OnOpenedByUser</span><span class="sxs-lookup"><span data-stu-id="cd86a-671">LSCEventType_OnOpenedByUser</span></span>  <br/> |<span data-ttu-id="cd86a-672">Un usuario abrió un archivo.</span><span class="sxs-lookup"><span data-stu-id="cd86a-672">A user opened a file.</span></span>  <br/> |
|<span data-ttu-id="cd86a-673">LSCEventType_OnServerChangesDownloaded</span><span class="sxs-lookup"><span data-stu-id="cd86a-673">LSCEventType_OnServerChangesDownloaded</span></span>  <br/> |<span data-ttu-id="cd86a-674">Ha terminado de descargar los cambios de archivo del servidor.</span><span class="sxs-lookup"><span data-stu-id="cd86a-674">Finished downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="cd86a-675">LSCEventType_OnLocalChangesUploaded</span><span class="sxs-lookup"><span data-stu-id="cd86a-675">LSCEventType_OnLocalChangesUploaded</span></span>  <br/> |<span data-ttu-id="cd86a-676">Se terminaron de cargar los cambios de archivo en el servidor.</span><span class="sxs-lookup"><span data-stu-id="cd86a-676">Finished uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="cd86a-677">LSCEventType_OnLocalConflictStateChanged</span><span class="sxs-lookup"><span data-stu-id="cd86a-677">LSCEventType_OnLocalConflictStateChanged</span></span>  <br/> |<span data-ttu-id="cd86a-678">El estado de conflicto de combinación de un archivo ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-678">The merge conflict state of a file has changed.</span></span>  <br/> |
|<span data-ttu-id="cd86a-679">LSCEventType_OnFileAdded</span><span class="sxs-lookup"><span data-stu-id="cd86a-679">LSCEventType_OnFileAdded</span></span>  <br/> |<span data-ttu-id="cd86a-680">Se agregó un archivo.</span><span class="sxs-lookup"><span data-stu-id="cd86a-680">A file was added.</span></span>  <br/> |
|<span data-ttu-id="cd86a-681">LSCEventType_OnFileDeleted</span><span class="sxs-lookup"><span data-stu-id="cd86a-681">LSCEventType_OnFileDeleted</span></span>  <br/> |<span data-ttu-id="cd86a-682">Se eliminó un archivo.</span><span class="sxs-lookup"><span data-stu-id="cd86a-682">A file was deleted.</span></span>  <br/> |
|<span data-ttu-id="cd86a-683">LSCEventType_OnSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="cd86a-683">LSCEventType_OnSyncEnabled</span></span>  <br/> |<span data-ttu-id="cd86a-684">La sincronización se ha habilitado para los archivos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="cd86a-684">Synchronizing was enabled for a user's files.</span></span>  <br/> |
|<span data-ttu-id="cd86a-685">LSCEventType_OnServerChangesDownloadStarted</span><span class="sxs-lookup"><span data-stu-id="cd86a-685">LSCEventType_OnServerChangesDownloadStarted</span></span>  <br/> |<span data-ttu-id="cd86a-686">Empezó a descargar los cambios de archivos desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="cd86a-686">Started downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="cd86a-687">LSCEventType_OnLocalChangesUploadStarted</span><span class="sxs-lookup"><span data-stu-id="cd86a-687">LSCEventType_OnLocalChangesUploadStarted</span></span>  <br/> |<span data-ttu-id="cd86a-688">Empezó a cargar los cambios de archivo en el servidor.</span><span class="sxs-lookup"><span data-stu-id="cd86a-688">Started uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="cd86a-689">LSCEventType_OnFilePathConflict</span><span class="sxs-lookup"><span data-stu-id="cd86a-689">LSCEventType_OnFilePathConflict</span></span>  <br/> |<span data-ttu-id="cd86a-690">Este evento se genera cuando una llamada a [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)o [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) provoca una colisión de ruta de acceso web o ruta de acceso local con otro archivo en la memoria caché de archivos de Office.</span><span class="sxs-lookup"><span data-stu-id="cd86a-690">This event is generated when a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) causes a Web Path or Local Path collision with another file in the Office file cache.</span></span>  <br/> |
|<span data-ttu-id="cd86a-691">LSCEventType_OnFileForked</span><span class="sxs-lookup"><span data-stu-id="cd86a-691">LSCEventType_OnFileForked</span></span>  <br/> ||
|<span data-ttu-id="cd86a-692">LSCEventType_Max</span><span class="sxs-lookup"><span data-stu-id="cd86a-692">LSCEventType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a><span data-ttu-id="cd86a-693">Enum LSCEventTypeOccurred</span><span class="sxs-lookup"><span data-stu-id="cd86a-693">Enum LSCEventTypeOccurred</span></span>
<span data-ttu-id="cd86a-694"><a name="Enum_LSCEventTypeOccurred"> </a></span><span class="sxs-lookup"><span data-stu-id="cd86a-694"><a name="Enum_LSCEventTypeOccurred"> </a></span></span>

<span data-ttu-id="cd86a-695">Esta enumeración especifica el tipo de eventos que pueden producirse.</span><span class="sxs-lookup"><span data-stu-id="cd86a-695">This enumeration specifies the type of events that can occur.</span></span> <span data-ttu-id="cd86a-696">El consumidor debe llamar a funciones específicas de ILSCLocalSyncClient en función del tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="cd86a-696">The consumer needs to call specific ILSCLocalSyncClient functions based on the event type.</span></span>
  
|<span data-ttu-id="cd86a-697">Enumerator</span><span class="sxs-lookup"><span data-stu-id="cd86a-697">Enumerator</span></span>|<span data-ttu-id="cd86a-698">Description</span><span class="sxs-lookup"><span data-stu-id="cd86a-698">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd86a-699">LSCEventTypeOccurred_GetChanges</span><span class="sxs-lookup"><span data-stu-id="cd86a-699">LSCEventTypeOccurred_GetChanges</span></span>  <br/> |<span data-ttu-id="cd86a-700">Se ha producido un EVENTO ILSC.</span><span class="sxs-lookup"><span data-stu-id="cd86a-700">An ILSCEvent has occurred.</span></span> <span data-ttu-id="cd86a-701">El consumidor debe llamar a [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) para recuperar los datos.</span><span class="sxs-lookup"><span data-stu-id="cd86a-701">The consumer should call [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) to retrieve the data.</span></span>  <br/> |
|<span data-ttu-id="cd86a-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="cd86a-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span></span>  <br/> |<span data-ttu-id="cd86a-703">Las extensiones de archivo compatibles han cambiado.</span><span class="sxs-lookup"><span data-stu-id="cd86a-703">The supported file extensions have changed.</span></span> <span data-ttu-id="cd86a-704">El consumidor debe llamar a [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) para recuperar la nueva lista de extensiones admitidas.</span><span class="sxs-lookup"><span data-stu-id="cd86a-704">The consumer should call [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) to retrieve the new list of supported extensions.</span></span>  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a><span data-ttu-id="cd86a-705">Enum LSCNetworkSyncPermissionType</span><span class="sxs-lookup"><span data-stu-id="cd86a-705">Enum LSCNetworkSyncPermissionType</span></span>
<span data-ttu-id="cd86a-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span><span class="sxs-lookup"><span data-stu-id="cd86a-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span></span>

<span data-ttu-id="cd86a-707">Esta enumeración especifica las marcas usadas para un costo de red heurístico.</span><span class="sxs-lookup"><span data-stu-id="cd86a-707">This enumeration specifies the flags used for a network cost heuristic.</span></span> 

|<span data-ttu-id="cd86a-708">Enumerator</span><span class="sxs-lookup"><span data-stu-id="cd86a-708">Enumerator</span></span>|<span data-ttu-id="cd86a-709">Description</span><span class="sxs-lookup"><span data-stu-id="cd86a-709">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd86a-710">LSCNetworkSyncPermissionType_HighCost</span><span class="sxs-lookup"><span data-stu-id="cd86a-710">LSCNetworkSyncPermissionType_HighCost</span></span>  <br/> |<span data-ttu-id="cd86a-711">True si se invalida el costo heurístico de las redes costosas (como 3G).</span><span class="sxs-lookup"><span data-stu-id="cd86a-711">True if the cost heuristic for expensive networks (such as 3G) is overridden.</span></span>  <br/> |
|<span data-ttu-id="cd86a-712">LSCNetworkSyncPermissionType_HighPowerUsage</span><span class="sxs-lookup"><span data-stu-id="cd86a-712">LSCNetworkSyncPermissionType_HighPowerUsage</span></span>  <br/> |<span data-ttu-id="cd86a-713">True si se invalida el costo heurístico para el uso de energía (como una batería).</span><span class="sxs-lookup"><span data-stu-id="cd86a-713">True if the cost heuristic for power usage (such as a battery) is overridden.</span></span>  <br/> |
   
### <a name="enum-lscstatusflag"></a><span data-ttu-id="cd86a-714">Enum LSCStatusFlag</span><span class="sxs-lookup"><span data-stu-id="cd86a-714">Enum LSCStatusFlag</span></span>
<span data-ttu-id="cd86a-715"><a name="Enum_LSCStatusFlag"> </a></span><span class="sxs-lookup"><span data-stu-id="cd86a-715"><a name="Enum_LSCStatusFlag"> </a></span></span>

<span data-ttu-id="cd86a-716">Esta enumeración se usa para representar el estado de sincronización de un archivo.</span><span class="sxs-lookup"><span data-stu-id="cd86a-716">This enumeration is used to represent the synchronize status of a file.</span></span> 
  
|<span data-ttu-id="cd86a-717">Enumerator</span><span class="sxs-lookup"><span data-stu-id="cd86a-717">Enumerator</span></span>|<span data-ttu-id="cd86a-718">Description</span><span class="sxs-lookup"><span data-stu-id="cd86a-718">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd86a-719">LCSStatusFlag_None</span><span class="sxs-lookup"><span data-stu-id="cd86a-719">LCSStatusFlag_None</span></span>  <br/> ||
|<span data-ttu-id="cd86a-720">LSCStatusFlag_UploadPending</span><span class="sxs-lookup"><span data-stu-id="cd86a-720">LSCStatusFlag_UploadPending</span></span>  <br/> |<span data-ttu-id="cd86a-721">True si hay datos pendientes para enviar al archivo del servidor.</span><span class="sxs-lookup"><span data-stu-id="cd86a-721">True if there is pending data to send to the server file.</span></span>  <br/> |
|<span data-ttu-id="cd86a-722">LSCStatusFlag_DownloadPending</span><span class="sxs-lookup"><span data-stu-id="cd86a-722">LSCStatusFlag_DownloadPending</span></span>  <br/> |<span data-ttu-id="cd86a-723">True si hay datos pendientes para descargar desde el archivo del servidor.</span><span class="sxs-lookup"><span data-stu-id="cd86a-723">True if there is pending data to download from the server file.</span></span>  <br/> |
|<span data-ttu-id="cd86a-724">LSCStatusFlag_LocalFileUnchanged</span><span class="sxs-lookup"><span data-stu-id="cd86a-724">LSCStatusFlag_LocalFileUnchanged</span></span>  <br/> |<span data-ttu-id="cd86a-725">True si los datos que Office tiene en el archivo en su memoria caché es la copia más reciente de los datos en el disco.</span><span class="sxs-lookup"><span data-stu-id="cd86a-725">True if the data Office has on the file in its cache is the most recent copy of the data on disk.</span></span>  <br/> |
   

