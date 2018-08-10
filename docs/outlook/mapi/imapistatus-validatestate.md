---
title: IMAPIStatusValidateState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.ValidateState
api_type:
- COM
ms.assetid: 036b9b15-86e1-4a37-8e4b-e37b2963d8fb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3ff29ac7e7f9b7876bb678930390ca556351ecf6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817495"
---
# <a name="imapistatusvalidatestate"></a><span data-ttu-id="3a40e-103">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="3a40e-103">IMAPIStatus::ValidateState</span></span>

<span data-ttu-id="3a40e-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3a40e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3a40e-105">Confirma la información de estado externo disponible para el recurso MAPI o el proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="3a40e-105">Confirms the external status information available for the MAPI resource or the service provider.</span></span> <span data-ttu-id="3a40e-106">Este método se admite en todos los objetos de estado.</span><span class="sxs-lookup"><span data-stu-id="3a40e-106">This method is supported in all status objects.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="3a40e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3a40e-107">Parameters</span></span>

<span data-ttu-id="3a40e-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="3a40e-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="3a40e-109">[entrada] Identificador de la ventana principal de los cuadros de diálogo o windows que muestra este método.</span><span class="sxs-lookup"><span data-stu-id="3a40e-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
<span data-ttu-id="3a40e-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3a40e-110">_ulFlags_</span></span>
  
> <span data-ttu-id="3a40e-111">[entrada] Una máscara de bits de indicadores que controla la validación.</span><span class="sxs-lookup"><span data-stu-id="3a40e-111">[in] A bitmask of flags that controls the validation.</span></span> <span data-ttu-id="3a40e-112">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="3a40e-112">The following flags can be set:</span></span>
    
<span data-ttu-id="3a40e-113">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="3a40e-113">ABORT_XP_HEADER_OPERATION</span></span>
  
> <span data-ttu-id="3a40e-114">El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en el cuadro de diálogo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="3a40e-114">The user canceled the operation, typically by clicking the **Cancel** button in the corresponding dialog box.</span></span> <span data-ttu-id="3a40e-115">El objeto de estado tiene dos opciones:</span><span class="sxs-lookup"><span data-stu-id="3a40e-115">The status object has two options:</span></span> 
    
   - <span data-ttu-id="3a40e-116">Continuar trabajando en la operación.</span><span class="sxs-lookup"><span data-stu-id="3a40e-116">Continue working on the operation.</span></span>
    
   - <span data-ttu-id="3a40e-117">Detener la operación y devolver MAPI_E_USER_CANCELED.</span><span class="sxs-lookup"><span data-stu-id="3a40e-117">Stop the operation and return MAPI_E_USER_CANCELED.</span></span>
    
<span data-ttu-id="3a40e-118">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="3a40e-118">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="3a40e-119">Una o varias de las propiedades de configuración del objeto de estado ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="3a40e-119">One or more of the status object's configuration properties changed.</span></span> <span data-ttu-id="3a40e-120">Los clientes pueden establecer esta marca para permitir que la cola MAPI para dinámicamente corregir errores del proveedor de transporte crítico.</span><span class="sxs-lookup"><span data-stu-id="3a40e-120">Clients can set this flag to allow the MAPI spooler to dynamically correct critical transport provider failures.</span></span> 
    
<span data-ttu-id="3a40e-121">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="3a40e-121">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="3a40e-122">Debe realizar una conexión en el objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="3a40e-122">The status object should perform a connection.</span></span> <span data-ttu-id="3a40e-123">Cuando este indicador se utiliza con el indicador REFRESH_XP_HEADER_CACHE o PROCESS_XP_HEADER_CACHE, la conexión se produce sin almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="3a40e-123">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connection occurs without caching.</span></span>
    
<span data-ttu-id="3a40e-124">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="3a40e-124">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="3a40e-125">Debe realizar una operación de desconexión en el objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="3a40e-125">The status object should perform a disconnect operation.</span></span> <span data-ttu-id="3a40e-126">Cuando este indicador se utiliza con el indicador REFRESH_XP_HEADER_CACHE o PROCESS_XP_HEADER_CACHE, se produce la desconexión sin almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="3a40e-126">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the disconnection occurs without caching.</span></span>
    
<span data-ttu-id="3a40e-127">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="3a40e-127">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="3a40e-128">Se deben procesar las entradas de la tabla de la memoria caché de encabezado, que deben descargarse todos los mensajes marcados con la marca MSGSTATUS_REMOTE_DOWNLOAD y se deben eliminar todos los mensajes marcados con la marca MSGSTATUS_REMOTE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="3a40e-128">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="3a40e-129">Los mensajes que tienen MSGSTATUS_REMOTE_DOWNLOAD y MSGSTATUS_REMOTE_DELETE establecer se va a mover.</span><span class="sxs-lookup"><span data-stu-id="3a40e-129">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="3a40e-130">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="3a40e-130">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="3a40e-131">Para un proveedor remoto de transporte, que debe descargarse una nueva lista de encabezados de mensaje y se deben borrar todos los marcadores que marca el estado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="3a40e-131">For a remote transport provider, a new list of message headers should be downloaded and all flags that mark message status should be cleared.</span></span>
    
<span data-ttu-id="3a40e-132">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="3a40e-132">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="3a40e-133">Impide que el objeto de estado muestre una interfaz de usuario como parte de la operación.</span><span class="sxs-lookup"><span data-stu-id="3a40e-133">Prevents the status object from displaying a user interface as part of the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3a40e-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3a40e-134">Return value</span></span>

<span data-ttu-id="3a40e-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="3a40e-135">S_OK</span></span> 
  
> <span data-ttu-id="3a40e-136">La validación fue correcta.</span><span class="sxs-lookup"><span data-stu-id="3a40e-136">The validation was successful.</span></span>
    
<span data-ttu-id="3a40e-137">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="3a40e-137">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="3a40e-138">Otra operación está en curso; se debe permitir para llevar a cabo o se debe detener, antes de inicia esta operación.</span><span class="sxs-lookup"><span data-stu-id="3a40e-138">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation is initiated.</span></span>
    
<span data-ttu-id="3a40e-139">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="3a40e-139">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="3a40e-140">El objeto de estado no es compatible con el método de validación, como se indica por la ausencia de la marca STATUS_VALIDATE_STATE en la propiedad **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3a40e-140">The status object does not support the validation method, as indicated by the absence of the STATUS_VALIDATE_STATE flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="3a40e-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="3a40e-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="3a40e-142">El usuario canceló la operación de validación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3a40e-142">The user canceled the validation operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="3a40e-143">Este valor se devuelve sólo por los proveedores de transporte remoto.</span><span class="sxs-lookup"><span data-stu-id="3a40e-143">This value is returned only by remote transport providers.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3a40e-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3a40e-144">Remarks</span></span>

<span data-ttu-id="3a40e-145">El método **IMAPIStatus::ValidateState** comprueba el estado de un recurso que esté asociado a un objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="3a40e-145">The **IMAPIStatus::ValidateState** method checks the state of a resource that is associated with a status object.</span></span> <span data-ttu-id="3a40e-146">**ValidateState** es el único método en la interfaz de [IMAPIStatus](imapistatusimapiprop.md) que es necesario para todos los objetos de estado.</span><span class="sxs-lookup"><span data-stu-id="3a40e-146">**ValidateState** is the only method in the [IMAPIStatus](imapistatusimapiprop.md) interface that is required for all status objects.</span></span> <span data-ttu-id="3a40e-147">El comportamiento exacto de este método depende de la implementación.</span><span class="sxs-lookup"><span data-stu-id="3a40e-147">The exact behavior of this method depends on the implementation.</span></span> <span data-ttu-id="3a40e-148">En la siguiente tabla se describe la implementación de cada uno de los distintos tipos de objetos de estado.</span><span class="sxs-lookup"><span data-stu-id="3a40e-148">The following table describes the implementation of each of the different types of status objects.</span></span> 
  
|<span data-ttu-id="3a40e-149">**Objeto de estado**</span><span class="sxs-lookup"><span data-stu-id="3a40e-149">**Status object**</span></span>|<span data-ttu-id="3a40e-150">ValidateState ** implementación **</span><span class="sxs-lookup"><span data-stu-id="3a40e-150">****ValidateState** implementation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3a40e-151">Subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="3a40e-151">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="3a40e-152">Valida el estado de todos los recursos que poseen los proveedores de servicios activo actualmente y el subsistema de sí mismo.</span><span class="sxs-lookup"><span data-stu-id="3a40e-152">Validates the state of all the resources that the currently active service providers and the subsystem itself own.</span></span>  <br/> |
|<span data-ttu-id="3a40e-153">Cola MAPI</span><span class="sxs-lookup"><span data-stu-id="3a40e-153">MAPI spooler</span></span>  <br/> |<span data-ttu-id="3a40e-154">Realiza un inicio de sesión de todos los proveedores de transporte, independientemente de si ya han iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="3a40e-154">Performs a logon of all transport providers, regardless of whether they are already logged on.</span></span>  <br/> |
|<span data-ttu-id="3a40e-155">Libreta de direcciones MAPI</span><span class="sxs-lookup"><span data-stu-id="3a40e-155">MAPI address book</span></span>  <br/> |<span data-ttu-id="3a40e-156">Comprobaciones de las entradas en la sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="3a40e-156">Checks the entries in its profile section.</span></span>  <br/> |
|<span data-ttu-id="3a40e-157">Proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="3a40e-157">Service provider</span></span>  <br/> |<span data-ttu-id="3a40e-158">Implementación depende del tipo de proveedor y los indicadores establecidos en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="3a40e-158">Implementation depends on the type of provider and the flags set in the  _ulFlags_ parameter.</span></span>  <br/> |
   
## <a name="notes-to-implementers"></a><span data-ttu-id="3a40e-159">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="3a40e-159">Notes to implementers</span></span>

<span data-ttu-id="3a40e-160">Las aplicaciones cliente remoto llaman al método **ValidateState** para iniciar el proceso remoto para varias acciones.</span><span class="sxs-lookup"><span data-stu-id="3a40e-160">Remote client applications call the **ValidateState** method to start remote processing for various actions.</span></span> <span data-ttu-id="3a40e-161">Este método existe principalmente para establecer los bits de estado para comunicarse con la cola MAPI, en lugar de hacerlo realmente realizar cualquier trabajo.</span><span class="sxs-lookup"><span data-stu-id="3a40e-161">This method exists primarily to set status bits to communicate with the MAPI spooler, instead of to actually do any work.</span></span> <span data-ttu-id="3a40e-162">Normalmente, el proveedor de transporte establece marcas en su fila de estado que se indican a la cola MAPI qué acciones deben iniciarse para completar la solicitud del cliente.</span><span class="sxs-lookup"><span data-stu-id="3a40e-162">Typically, the transport provider sets flags in its status row that indicate to the MAPI spooler what actions need to be initiated to complete the client's request.</span></span> 

<span data-ttu-id="3a40e-163">En este modelo de interacción de cliente y transporte de cola de impresión, las acciones solicitadas por el cliente son asincrónicas, en que **ValidateState** devuelve antes de que las acciones requeridas se completa.</span><span class="sxs-lookup"><span data-stu-id="3a40e-163">In this model of client-transport-spooler interaction, the actions requested by the client are asynchronous, in that **ValidateState** returns before the requested actions are complete.</span></span> <span data-ttu-id="3a40e-164">Sin embargo, las acciones que implican necesariamente el sistema de mensajería subyacente o que implican una interfaz específica de transporte, pueden ser sincrónicas.</span><span class="sxs-lookup"><span data-stu-id="3a40e-164">However, actions that do not necessarily involve the underlying messaging system, or that involve a transport-specific interface, can be synchronous.</span></span> <span data-ttu-id="3a40e-165">La aplicación cliente pasa una máscara de bits de los siguientes indicadores para especificar las acciones que debe realizar el proveedor de transporte remoto.</span><span class="sxs-lookup"><span data-stu-id="3a40e-165">The client application passes in a bitmask of the following flags to specify which actions the remote transport provider should take.</span></span> 
  
<span data-ttu-id="3a40e-166">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="3a40e-166">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="3a40e-167">Si es posible, el proveedor de transporte remoto debe cancelar las operaciones que implican descargar encabezados.</span><span class="sxs-lookup"><span data-stu-id="3a40e-167">If possible, the remote transport provider should cancel any operations that involve downloading headers.</span></span> <span data-ttu-id="3a40e-168">Para ello, el proveedor de transporte debe establecer los siguientes valores de propiedad en la fila de estado del objeto de inicio de sesión:</span><span class="sxs-lookup"><span data-stu-id="3a40e-168">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="3a40e-169">Desactive los bits STATUS_INBOUND_ENABLED y STATUS_INBOUND_ACTIVE en la propiedad **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) para indicar a la cola MAPI para detener el proceso de vaciado entrante para este proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="3a40e-169">Clear the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property to tell the MAPI spooler to halt the incoming flush process for this transport provider.</span></span>
    
   - <span data-ttu-id="3a40e-170">Establecer el bit en la propiedad **PR_STATUS_CODE** de STATUS_OFFLINE.</span><span class="sxs-lookup"><span data-stu-id="3a40e-170">Set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="3a40e-171">Establezca la propiedad **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) en TRUE.</span><span class="sxs-lookup"><span data-stu-id="3a40e-171">Set the **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) property to TRUE.</span></span>
    
   - <span data-ttu-id="3a40e-172">Establezca la propiedad **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) en una cadena que indica el estado del proveedor de transporte para el usuario.</span><span class="sxs-lookup"><span data-stu-id="3a40e-172">Set the **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) property to a string that indicates the transport provider's status to the user.</span></span>
    
   - <span data-ttu-id="3a40e-173">Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="3a40e-173">Return S_OK.</span></span> <span data-ttu-id="3a40e-174">Sin embargo, si no se puede cancelar la operación en curso, **ValidateState** debe devolver MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="3a40e-174">However, if the operation in progress cannot be canceled, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
<span data-ttu-id="3a40e-175">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="3a40e-175">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="3a40e-176">Un proveedor de transporte remoto nunca debe establecer una conexión a un recurso compartido (por ejemplo, un módem o un puerto COM) fuera del contexto de la interacción de transporte de la cola de impresión MAPI implica en el método [IXPLogon::FlushQueues](ixplogon-flushqueues.md) .</span><span class="sxs-lookup"><span data-stu-id="3a40e-176">A remote transport provider should never establish a connection to a shared resource (for example, a modem or COM port) outside the context of the MAPI spooler-transport interaction involved in the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) method.</span></span> <span data-ttu-id="3a40e-177">Si se llama a **ValidateState** con este indicador, el proveedor de transporte debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3a40e-177">If **ValidateState** is called with this flag, your transport provider should do the following:</span></span> 
    
   - <span data-ttu-id="3a40e-178">Establecer un indicador de estado interno para indicar que se debe establecer la conexión remota cuando se llama al método **IXPLogon::FlushQueues** .</span><span class="sxs-lookup"><span data-stu-id="3a40e-178">Set an internal status flag to indicate that the remote connection must be established when the **IXPLogon::FlushQueues** method is called.</span></span> 
    
   - <span data-ttu-id="3a40e-179">Establecer los valores correctos en la tabla de estado para hacer que la cola MAPI iniciar la cola de proceso de vaciado.</span><span class="sxs-lookup"><span data-stu-id="3a40e-179">Set the correct values in the status table to cause the MAPI spooler to initiate the queue flushing process.</span></span>
    
   - <span data-ttu-id="3a40e-180">Cuando se haya completado el vaciado de colas, el recurso compartido de la versión.</span><span class="sxs-lookup"><span data-stu-id="3a40e-180">When flushing of queues is complete, release the shared resource.</span></span>
    
   - <span data-ttu-id="3a40e-181">Desactive el STATUS_OFFLINE de bit en la propiedad **PR_STATUS_CODE** .</span><span class="sxs-lookup"><span data-stu-id="3a40e-181">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="3a40e-182">Devuelve S_OK.</span><span class="sxs-lookup"><span data-stu-id="3a40e-182">Return S_OK.</span></span>
    
<span data-ttu-id="3a40e-183">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="3a40e-183">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="3a40e-184">El proveedor de transporte remoto debe liberar su conexión con los recursos del sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="3a40e-184">The remote transport provider should release its connection to the messaging system resources.</span></span> <span data-ttu-id="3a40e-185">Después de hacer esto, se debe establecer el bit STATUS_OFFLINE en la propiedad **PR_STATUS_CODE** y devolver S_OK.</span><span class="sxs-lookup"><span data-stu-id="3a40e-185">After doing this, it should set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property and return S_OK.</span></span> 
    
<span data-ttu-id="3a40e-186">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="3a40e-186">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="3a40e-187">El proveedor de transporte remoto debe procesar los mensajes remotos y cargar todos los mensajes que se han aplazado.</span><span class="sxs-lookup"><span data-stu-id="3a40e-187">The remote transport provider should process remote messages and upload any messages that have been deferred.</span></span> <span data-ttu-id="3a40e-188">Para ello, el proveedor de transporte debe establecer los siguientes valores de propiedad en la fila de estado del objeto de inicio de sesión:</span><span class="sxs-lookup"><span data-stu-id="3a40e-188">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="3a40e-189">Establezca la propiedad **PR_STATUS_STRING** en una cadena que indica el estado del proveedor de transporte para el usuario.</span><span class="sxs-lookup"><span data-stu-id="3a40e-189">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="3a40e-190">Establecer los bits STATUS_OUTBOUND_ENABLED y STATUS_OUTBOUND_ACTIVE en la propiedad **PR_STATUS_CODE** .</span><span class="sxs-lookup"><span data-stu-id="3a40e-190">Set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="3a40e-191">Establezca la propiedad **PR_REMOTE_VALIDATE_OK** en la fila de estado del proveedor de transporte en FALSE.</span><span class="sxs-lookup"><span data-stu-id="3a40e-191">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
   - <span data-ttu-id="3a40e-192">Si hay otra operación en curso (por ejemplo, descargar encabezados) cuando se llama a **ValidateState** , **ValidateState** debe devolver MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="3a40e-192">If another operation is in progress (such as downloading headers) when **ValidateState** is called, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
   - <span data-ttu-id="3a40e-193">Ejecutar el código para procesar la marca REFRESH_XP_HEADER_CACHE, también, para satisfacer los requisitos del cliente de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="3a40e-193">Execute the code for processing the REFRESH_XP_HEADER_CACHE flag, as well, to satisfy requirements of the Microsoft Exchange client.</span></span>
    
<span data-ttu-id="3a40e-194">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="3a40e-194">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="3a40e-195">El proveedor de transporte remoto debe recuperar los encabezados de mensaje nuevo desde el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="3a40e-195">The remote transport provider should retrieve any new message headers from the messaging system.</span></span> <span data-ttu-id="3a40e-196">Para ello, el proveedor de transporte debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3a40e-196">To do this, the transport provider must do the following:</span></span>
    
   - <span data-ttu-id="3a40e-197">Establezca la propiedad **PR_STATUS_STRING** en una cadena que indica el estado del proveedor de transporte para el usuario.</span><span class="sxs-lookup"><span data-stu-id="3a40e-197">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="3a40e-198">Establecer los bits STATUS_INBOUND_ENABLED y STATUS_INBOUND_ACTIVE en la propiedad **PR_STATUS_CODE** .</span><span class="sxs-lookup"><span data-stu-id="3a40e-198">Set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="3a40e-199">Desactive el STATUS_OFFLINE de bit en la propiedad **PR_STATUS_CODE** .</span><span class="sxs-lookup"><span data-stu-id="3a40e-199">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="3a40e-200">Establecer el bit en la propiedad **PR_STATUS_CODE** de STATUS_ONLINE.</span><span class="sxs-lookup"><span data-stu-id="3a40e-200">Set the STATUS_ONLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="3a40e-201">Establezca la propiedad **PR_REMOTE_VALIDATE_OK** en la fila de estado del proveedor de transporte en FALSE.</span><span class="sxs-lookup"><span data-stu-id="3a40e-201">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
<span data-ttu-id="3a40e-202">SHOW_XP_SESSION_UI</span><span class="sxs-lookup"><span data-stu-id="3a40e-202">SHOW_XP_SESSION_UI</span></span> 
  
> <span data-ttu-id="3a40e-203">Si su proveedor de transporte tiene cualquier partes de la interfaz de usuario para procesar los encabezados del mensaje (por ejemplo, un cuadro de diálogo que confirma la descarga de mensajes), se debe mostrar ese cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3a40e-203">If your transport provider has any pieces of user interface for processing the message headers (such as a dialog box that confirms the downloading of messages), that dialog box should be displayed.</span></span> <span data-ttu-id="3a40e-204">De lo contrario, **ValidateState** puede devolver MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="3a40e-204">Otherwise, **ValidateState** can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="3a40e-205">Si se pasan los indicadores distintos de estos, **ValidateState** debe devolver MAPI_E_UNKNOWN_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="3a40e-205">If any flags other than these are passed in, **ValidateState** should return MAPI_E_UNKNOWN_FLAGS.</span></span> 
  
<span data-ttu-id="3a40e-206">El método **IMAPIStatus::ValidateState** a menudo será la llamada del cliente para el proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="3a40e-206">The client's call to the transport provider will often be to the **IMAPIStatus::ValidateState** method.</span></span> <span data-ttu-id="3a40e-207">Durante el procesamiento de **ValidateState**, el proveedor de transporte no debe realizar todas las acciones que asignan recursos escaso del sistema, como un módem o el puerto COM.</span><span class="sxs-lookup"><span data-stu-id="3a40e-207">During the processing of **ValidateState**, the transport provider should not perform any actions that allocate scarce system resources, such as a modem or COM port.</span></span> <span data-ttu-id="3a40e-208">Esto es debido a que la cola MAPI en ocasiones, necesite vaciar las colas en más de un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="3a40e-208">This is because the MAPI spooler will sometimes need to flush queues on more than one transport provider.</span></span> <span data-ttu-id="3a40e-209">Sin embargo, el cliente puede llamar a método **ValidateState** del cualquier proveedor transporte en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="3a40e-209">However, the client can call any transport provider's **ValidateState** method at any time.</span></span> <span data-ttu-id="3a40e-210">Si su proveedor de transporte intenta asignar un recurso escaso durante el procesamiento de **ValidateState**, puede producir un error debido a conflictos con otro proveedor de transporte que se ha indicado la cola MAPI a que vacíen sus colas.</span><span class="sxs-lookup"><span data-stu-id="3a40e-210">If your transport provider attempts to allocate a scarce resource during the processing of **ValidateState**, an error can result due to conflict with another transport provider that the MAPI spooler has instructed to flush its queues.</span></span> <span data-ttu-id="3a40e-211">Si permite que todas las asignaciones de recurso escaso se producen bajo la dirección de la cola MAPI, puede evitar estos conflictos.</span><span class="sxs-lookup"><span data-stu-id="3a40e-211">If you allow all scarce resource allocations to occur under the direction of the MAPI spooler, you can avoid such conflicts.</span></span> <span data-ttu-id="3a40e-212">El proveedor de transporte debe admitir la propiedad **PR_REMOTE_VALIDATE_OK** para que pueden detectar las aplicaciones cliente cuando el proveedor de transporte está ocupado o tener que esperar la cola MAPI iniciar una acción.</span><span class="sxs-lookup"><span data-stu-id="3a40e-212">Your transport provider should support the **PR_REMOTE_VALIDATE_OK** property so client applications can detect when your transport provider is busy or waiting for the MAPI spooler to initiate an action.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3a40e-213">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="3a40e-213">Notes to callers</span></span>

<span data-ttu-id="3a40e-214">Debido a que este método puede causar que otras llamadas potencialmente prolongados efectuarán, **ValidateState** puede devolver MAPI_E_BUSY para informarle de que este método está esperando la finalización de otra operación.</span><span class="sxs-lookup"><span data-stu-id="3a40e-214">Because this method can cause other potentially lengthy calls to be made, **ValidateState** can return MAPI_E_BUSY to inform you that this method is waiting for the completion of another operation.</span></span> <span data-ttu-id="3a40e-215">Debe esperar hasta que se complete la operación pendiente antes de intentar otra tarea.</span><span class="sxs-lookup"><span data-stu-id="3a40e-215">You should wait until the pending operation is complete before attempting another task.</span></span> 
  
<span data-ttu-id="3a40e-216">Tener el máximo control sobre las llamadas a objetos de estado de proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="3a40e-216">You have the most control over your calls to transport provider status objects.</span></span> <span data-ttu-id="3a40e-217">Puede pasar uno o más indicadores a **ValidateState** que afectan a las operaciones del proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="3a40e-217">You can pass one or more flags to **ValidateState** that affect the transport provider's operations.</span></span> <span data-ttu-id="3a40e-218">Por ejemplo, el indicador ABORT_XP_HEADER_OPERATION indica que el usuario canceló la validación.</span><span class="sxs-lookup"><span data-stu-id="3a40e-218">For example, the ABORT_XP_HEADER_OPERATION flag indicates that the user canceled the validation.</span></span> <span data-ttu-id="3a40e-219">Los proveedores de transporte pueden optar por anular, devolver MAPI_E_USER_CANCELED, o pueden continuar.</span><span class="sxs-lookup"><span data-stu-id="3a40e-219">Transport providers can decide to abort, returning MAPI_E_USER_CANCELED, or can continue.</span></span> 
  
<span data-ttu-id="3a40e-220">Puede establecer la marca CONFIG_CHANGED en una llamada para el objeto de estado de un proveedor de servicios o la cola MAPI para indicar que se ha cambiado una opción de configuración.</span><span class="sxs-lookup"><span data-stu-id="3a40e-220">You can set the CONFIG_CHANGED flag on a call to either the status object of a service provider or the MAPI spooler to indicate that a configuration option has been changed.</span></span> <span data-ttu-id="3a40e-221">Puede usar CONFIG_CHANGED para dinámicamente volver a configurar un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="3a40e-221">You can use CONFIG_CHANGED to dynamically reconfigure a transport provider.</span></span> <span data-ttu-id="3a40e-222">Cuando se establece CONFIG_CHANGED en una llamada al objeto de estado de un proveedor de servicios, el proveedor responde con una llamada a [SpoolerNotify](imapisupport-spoolernotify.md) a la cola MAPI del cambio de la alerta.</span><span class="sxs-lookup"><span data-stu-id="3a40e-222">When you set CONFIG_CHANGED on a call to a service provider's status object, the provider responds with a call to [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) to alert the MAPI spooler of the change.</span></span> <span data-ttu-id="3a40e-223">Cuando se establece CONFIG_CHANGED en una llamada al objeto de estado de la cola MAPI, la cola de impresión llama a [IXPLogon::AddressTypes](ixplogon-addresstypes.md) para cada proveedor de transporte activa.</span><span class="sxs-lookup"><span data-stu-id="3a40e-223">When you set CONFIG_CHANGED on a call to the MAPI spooler's status object, the spooler calls [IXPLogon::AddressTypes](ixplogon-addresstypes.md) for each active transport provider.</span></span> <span data-ttu-id="3a40e-224">**AddressTypes** informa a la cola MAPI de tipos de direcciones compatibles de un transporte.</span><span class="sxs-lookup"><span data-stu-id="3a40e-224">**AddressTypes** informs the MAPI spooler of a transport's supported address types.</span></span> <span data-ttu-id="3a40e-225">Algunos proveedores de servicios también mostrar un indicador de progreso si la validación se espera a tardar mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="3a40e-225">Some service providers also display a progress indicator if the validation is expected to take a long time.</span></span> <span data-ttu-id="3a40e-226">Mostrar un indicador de progreso es útil, pero no se requiere.</span><span class="sxs-lookup"><span data-stu-id="3a40e-226">Displaying a progress indicator is helpful, but not required.</span></span> 
  
<span data-ttu-id="3a40e-227">Cuando se establece la marca SUPPRESS_UI, se pueden mostrar ninguna de las hojas de propiedades de configuración o cuadros de diálogo de progreso.</span><span class="sxs-lookup"><span data-stu-id="3a40e-227">When the SUPPRESS_UI flag is set, none of the configuration property sheets or progress dialog boxes can be displayed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3a40e-228">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a40e-228">See also</span></span>

- [<span data-ttu-id="3a40e-229">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="3a40e-229">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
- [<span data-ttu-id="3a40e-230">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="3a40e-230">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
- [<span data-ttu-id="3a40e-231">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="3a40e-231">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
- [<span data-ttu-id="3a40e-232">Propiedad canónica PidTagRemoteValidateOk</span><span class="sxs-lookup"><span data-stu-id="3a40e-232">PidTagRemoteValidateOk Canonical Property</span></span>](pidtagremotevalidateok-canonical-property.md)
- [<span data-ttu-id="3a40e-233">Propiedad canónica PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="3a40e-233">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
- [<span data-ttu-id="3a40e-234">Propiedad canónica PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="3a40e-234">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
- [<span data-ttu-id="3a40e-235">Propiedad canónica PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="3a40e-235">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)
- [<span data-ttu-id="3a40e-236">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3a40e-236">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)
