---
title: MAPIInitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIInitialize
api_type:
- HeaderDef
ms.assetid: b9584226-79d2-4d83-8f31-dbfbc50f16c5
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: d22c24088960debcd18ccd818dad23656f6a01f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818267"
---
# <a name="mapiinitialize"></a><span data-ttu-id="b0c54-103">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="b0c54-103">MAPIInitialize</span></span>

  
  
<span data-ttu-id="b0c54-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b0c54-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b0c54-105">Incrementa el recuento de referencia del subsistema MAPI e inicializa datos globales para la DLL de MAPI.</span><span class="sxs-lookup"><span data-stu-id="b0c54-105">Increments the MAPI subsystem reference count and initializes global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b0c54-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b0c54-106">Header file:</span></span>  <br/> |<span data-ttu-id="b0c54-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="b0c54-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="b0c54-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="b0c54-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b0c54-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b0c54-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b0c54-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="b0c54-110">Called by:</span></span>  <br/> |<span data-ttu-id="b0c54-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="b0c54-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a><span data-ttu-id="b0c54-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0c54-112">Parameters</span></span>

 <span data-ttu-id="b0c54-113">_lpMapiInit_</span><span class="sxs-lookup"><span data-stu-id="b0c54-113">_lpMapiInit_</span></span>
  
> <span data-ttu-id="b0c54-114">[entrada] Puntero a una estructura [MAPIINIT_0](mapiinit_0.md) .</span><span class="sxs-lookup"><span data-stu-id="b0c54-114">[in] Pointer to a [MAPIINIT_0](mapiinit_0.md) structure.</span></span> <span data-ttu-id="b0c54-115">El parámetro _lpMapiInit_ se puede establecer en NULL.</span><span class="sxs-lookup"><span data-stu-id="b0c54-115">The  _lpMapiInit_ parameter can be set to NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b0c54-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0c54-116">Return value</span></span>

<span data-ttu-id="b0c54-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="b0c54-117">S_OK</span></span> 
  
> <span data-ttu-id="b0c54-118">El subsistema MAPI se inicializó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b0c54-118">The MAPI subsystem was initialized successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b0c54-119">Notas</span><span class="sxs-lookup"><span data-stu-id="b0c54-119">Remarks</span></span>

<span data-ttu-id="b0c54-120">Los incrementos de función **MAPIInitialize** contar la referencia MAPI para el subsistema MAPI y el disminuye de función [MAPIUninitialize](mapiuninitialize.md) el interno recuento de referencia.</span><span class="sxs-lookup"><span data-stu-id="b0c54-120">The **MAPIInitialize** function increments the MAPI reference count for the MAPI subsystem, and the [MAPIUninitialize](mapiuninitialize.md) function decrements the internal reference count.</span></span> <span data-ttu-id="b0c54-121">Por lo tanto, el número de llamadas a una función debe ser igual que el número de llamadas a otro.</span><span class="sxs-lookup"><span data-stu-id="b0c54-121">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> <span data-ttu-id="b0c54-122">**MAPIInitialize** devuelve S_OK si MAPI no se ha inicializado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b0c54-122">**MAPIInitialize** returns S_OK if MAPI has not been previously initialized.</span></span> 
  
<span data-ttu-id="b0c54-123">Un proveedor de servicio o cliente debe llamar **MAPIInitialize** antes de realizar cualquier otra llamada MAPI.</span><span class="sxs-lookup"><span data-stu-id="b0c54-123">A client or service provider must call **MAPIInitialize** before making any other MAPI call.</span></span> <span data-ttu-id="b0c54-124">Si no lo hace que las llamadas de cliente o servicio proveedor devolver el valor MAPI_E_NOT_INITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="b0c54-124">Failure to do so causes client or service provider calls to return the MAPI_E_NOT_INITIALIZED value.</span></span> 
  
<span data-ttu-id="b0c54-125">Cuando se llama a **MAPIInitialize** desde una aplicación multiproceso, establezca el parámetro _lpMapiInit_ en una estructura [MAPIINIT_0](mapiinit_0.md) que se declara del siguiente modo:</span><span class="sxs-lookup"><span data-stu-id="b0c54-125">When calling **MAPIInitialize** from a multithreaded application, set the  _lpMapiInit_ parameter to a [MAPIINIT_0](mapiinit_0.md) structure that is declared as follows:</span></span> 
  
 <span data-ttu-id="b0c54-126">**MAPIINIT_0** MAPIINIT = {0, MAPI_MULTITHREAD_NOTIFICATIONS}</span><span class="sxs-lookup"><span data-stu-id="b0c54-126">**MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS}</span></span> 
  
<span data-ttu-id="b0c54-127">y la llamada:</span><span class="sxs-lookup"><span data-stu-id="b0c54-127">and call:</span></span> 
  
 <span data-ttu-id="b0c54-128">**MAPIInitialize** (&amp;MAPIINIT);</span><span class="sxs-lookup"><span data-stu-id="b0c54-128">**MAPIInitialize** (&amp;MAPIINIT);</span></span> 
  
<span data-ttu-id="b0c54-129">Cuando se declara esta estructura, MAPI crea un subproceso independiente para controlar la ventana de notificación, que continúa hasta que el recuento de referencia initialize entra en cero.</span><span class="sxs-lookup"><span data-stu-id="b0c54-129">When this structure is declared, MAPI creates a separate thread to handle the notification window, which continues until the initialize reference count falls to zero.</span></span> <span data-ttu-id="b0c54-130">Un servicio de Windows debe establecer al miembro **ulflags** de la estructura **MAPIINIT_0** que señala _lpMapiInit_ a MAPI_NT_SERVICE.</span><span class="sxs-lookup"><span data-stu-id="b0c54-130">A Windows service must set the **ulflags** member of the **MAPIINIT_0** structure pointed to by  _lpMapiInit_ to MAPI_NT_SERVICE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b0c54-131">No se puede llamar a **MAPIInitialize** o **MAPIUninitialize** desde dentro de una función de Win32 **DllMain** o cualquier otra función que crea o termina subprocesos.</span><span class="sxs-lookup"><span data-stu-id="b0c54-131">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="b0c54-132">Para obtener más información, vea [Uso de objetos de subprocesos](using-thread-safe-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b0c54-132">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  
 <span data-ttu-id="b0c54-133">**MAPIInitialize** no devuelve ninguna información de error extendido.</span><span class="sxs-lookup"><span data-stu-id="b0c54-133">**MAPIInitialize** does not return any extended error information.</span></span> <span data-ttu-id="b0c54-134">A diferencia de la mayoría de llamadas MAPI, el significado de sus valores devueltos se define estrictamente para que se correspondan con el paso concreto de la inicialización con errores:</span><span class="sxs-lookup"><span data-stu-id="b0c54-134">Unlike most other MAPI calls, the meanings of its return values are strictly defined to correspond to the particular step of the initialization that failed:</span></span> 
  
1. <span data-ttu-id="b0c54-135">Comprueba los parámetros y los indicadores.</span><span class="sxs-lookup"><span data-stu-id="b0c54-135">Checks parameters and flags.</span></span>
    
    <span data-ttu-id="b0c54-136">MAPI_E_INVALID_PARAMETER o MAPI_E_UNKNOWN_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="b0c54-136">MAPI_E_INVALID_PARAMETER or MAPI_E_UNKNOWN_FLAGS.</span></span> <span data-ttu-id="b0c54-137">Se pasó un parámetro no válido o marca.</span><span class="sxs-lookup"><span data-stu-id="b0c54-137">Caller passed invalid parameter or flag.</span></span>
    
2. <span data-ttu-id="b0c54-138">Inicializa las claves del registro necesarias para MAPI y confirma el tipo de sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b0c54-138">Initializes registry keys required by MAPI and confirms the type of operating system.</span></span> <span data-ttu-id="b0c54-139">Este paso sólo ocurre si el proceso de cliente se ejecuta como un servicio en Windows y establece la marca de servicio de MAPI_NT en la estructura **MAPIINIT_0** .</span><span class="sxs-lookup"><span data-stu-id="b0c54-139">This step only happens if the client process is running as a service under Windows and sets the MAPI_NT SERVICE flag in the **MAPIINIT_0** structure.</span></span> 
    
    <span data-ttu-id="b0c54-140">MAPI_E_TOO_COMPLEX.</span><span class="sxs-lookup"><span data-stu-id="b0c54-140">MAPI_E_TOO_COMPLEX.</span></span> <span data-ttu-id="b0c54-141">El proceso de llamada es un servicio de Windows y no se podrían inicializar las claves del registro necesarias para MAPI.</span><span class="sxs-lookup"><span data-stu-id="b0c54-141">The calling process is a Windows service and registry keys required by MAPI could not be initialized.</span></span> 
    
    <span data-ttu-id="b0c54-142">Información adicional puede estar disponible en el registro de eventos de aplicación.</span><span class="sxs-lookup"><span data-stu-id="b0c54-142">Additional information may be available in the application event log.</span></span>
    
3. <span data-ttu-id="b0c54-143">Comprobar la compatibilidad de MAPI con OLE y, a continuación, inicializar OLE.</span><span class="sxs-lookup"><span data-stu-id="b0c54-143">Check for the compatibility of MAPI with OLE, then initialize OLE.</span></span>
    
1. <span data-ttu-id="b0c54-144">Comprobaciones para la compatibilidad entre las versiones actuales de OLE y MAPI.</span><span class="sxs-lookup"><span data-stu-id="b0c54-144">Checks for compatibility between the current versions of OLE and MAPI.</span></span> 
    
    <span data-ttu-id="b0c54-145">MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="b0c54-145">MAPI_E_VERSION.</span></span> <span data-ttu-id="b0c54-146">La versión de OLE instalada en la estación de trabajo no es compatible con esta versión de MAPI.</span><span class="sxs-lookup"><span data-stu-id="b0c54-146">The version of OLE installed on the workstation is not compatible with this version of MAPI.</span></span>
    
2. <span data-ttu-id="b0c54-147">Inicializa OLE.</span><span class="sxs-lookup"><span data-stu-id="b0c54-147">Initializes OLE.</span></span> 
    
    <span data-ttu-id="b0c54-148">Durante este paso solo, esta función puede devolver un código de error no se muestran aquí.</span><span class="sxs-lookup"><span data-stu-id="b0c54-148">During this step only, this function can return an error code not listed here.</span></span> <span data-ttu-id="b0c54-149">Cualquier error _no_ aparece aquí se supone que debe proceder de la función OLE **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="b0c54-149">Any error  _not_ listed here should be assumed to come from the OLE function **CoInitialize**.</span></span>
    
4. <span data-ttu-id="b0c54-150">Inicializa las variables globales por proceso.</span><span class="sxs-lookup"><span data-stu-id="b0c54-150">Initializes per-process global variables.</span></span>
    
    <span data-ttu-id="b0c54-151">MAPI_E_SESSION_LIMIT.</span><span class="sxs-lookup"><span data-stu-id="b0c54-151">MAPI_E_SESSION_LIMIT.</span></span> <span data-ttu-id="b0c54-152">MAPI configura contexto específica para el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="b0c54-152">MAPI sets up context specific to the current process.</span></span> <span data-ttu-id="b0c54-153">Es posible que se producen errores en Win16 si el número de procesos supera un cierto número, o en cualquier sistema si se ha agotado la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="b0c54-153">Failures may occur on Win16 if the number of processes exceeds a certain number, or on any system if available memory is exhausted.</span></span>
    
5. <span data-ttu-id="b0c54-154">Inicializa shared variables globales de todos los procesos.</span><span class="sxs-lookup"><span data-stu-id="b0c54-154">Initializes shared global variables of all processes.</span></span>
    
    <span data-ttu-id="b0c54-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span><span class="sxs-lookup"><span data-stu-id="b0c54-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span></span> <span data-ttu-id="b0c54-156">No hay suficientes recursos del sistema estaban disponibles para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="b0c54-156">Not enough system resources were available to complete the operation.</span></span>
    
6. <span data-ttu-id="b0c54-157">Inicializa el motor de notificación, crea su ventana y su subproceso si solicitado por el indicador MAPI_MULTITHREAD_NOTIFICATIONS.</span><span class="sxs-lookup"><span data-stu-id="b0c54-157">Initializes the notification engine, creates its window and its thread if requested by the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
    
    <span data-ttu-id="b0c54-158">MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="b0c54-158">MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="b0c54-159">Puede producirse un error si se agotan los recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="b0c54-159">May fail if system resources are exhausted.</span></span> 
    
7. <span data-ttu-id="b0c54-160">Carga e inicializa el proveedor de perfiles.</span><span class="sxs-lookup"><span data-stu-id="b0c54-160">Loads and initializes the profile provider.</span></span> <span data-ttu-id="b0c54-161">Comprueba que **MAPIInitialize** puede obtener acceso a la clave del registro donde se almacenan los datos de perfil.</span><span class="sxs-lookup"><span data-stu-id="b0c54-161">Verifies that **MAPIInitialize** can access the registry key where profile data are stored.</span></span> 
    
    <span data-ttu-id="b0c54-162">MAPI_E_NOT_INITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="b0c54-162">MAPI_E_NOT_INITIALIZED.</span></span> <span data-ttu-id="b0c54-163">El proveedor de perfiles detectó un error.</span><span class="sxs-lookup"><span data-stu-id="b0c54-163">The profile provider has encountered an error.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="b0c54-164">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b0c54-164">MFCMAPI reference</span></span>

<span data-ttu-id="b0c54-165">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="b0c54-165">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b0c54-166">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="b0c54-166">**File**</span></span>|<span data-ttu-id="b0c54-167">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="b0c54-167">**Function**</span></span>|<span data-ttu-id="b0c54-168">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="b0c54-168">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b0c54-169">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="b0c54-169">ContentsTableListCtrl.cpp</span></span>  <br/> ||<span data-ttu-id="b0c54-170">MFCMAPI, utiliza el método **MAPIInitialize** para inicializar MAPI en un subproceso en segundo plano para realizar algún procesamiento de tabla.</span><span class="sxs-lookup"><span data-stu-id="b0c54-170">MFCMAPI uses the **MAPIInitialize** method to initialize MAPI on a background thread to do some table processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b0c54-171">Ver también</span><span class="sxs-lookup"><span data-stu-id="b0c54-171">See also</span></span>



[<span data-ttu-id="b0c54-172">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="b0c54-172">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

