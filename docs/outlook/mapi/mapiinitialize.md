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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6464f16d9ad73b332ff20dc007ef162b9525c6d5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411179"
---
# <a name="mapiinitialize"></a><span data-ttu-id="93111-103">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="93111-103">MAPIInitialize</span></span>

  
  
<span data-ttu-id="93111-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93111-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93111-105">Incrementa el recuento de referencia del subsistema MAPI e inicializa datos globales para el archivo DLL de MAPI.</span><span class="sxs-lookup"><span data-stu-id="93111-105">Increments the MAPI subsystem reference count and initializes global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="93111-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="93111-106">Header file:</span></span>  <br/> |<span data-ttu-id="93111-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="93111-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="93111-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="93111-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="93111-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="93111-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="93111-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="93111-110">Called by:</span></span>  <br/> |<span data-ttu-id="93111-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="93111-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a><span data-ttu-id="93111-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="93111-112">Parameters</span></span>

 <span data-ttu-id="93111-113">_lpMapiInit_</span><span class="sxs-lookup"><span data-stu-id="93111-113">_lpMapiInit_</span></span>
  
> <span data-ttu-id="93111-114">a Puntero a una estructura [MAPIINIT_0](mapiinit_0.md) .</span><span class="sxs-lookup"><span data-stu-id="93111-114">[in] Pointer to a [MAPIINIT_0](mapiinit_0.md) structure.</span></span> <span data-ttu-id="93111-115">El parámetro _lpMapiInit_ puede establecerse en NULL.</span><span class="sxs-lookup"><span data-stu-id="93111-115">The  _lpMapiInit_ parameter can be set to NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="93111-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93111-116">Return value</span></span>

<span data-ttu-id="93111-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="93111-117">S_OK</span></span> 
  
> <span data-ttu-id="93111-118">El subsistema MAPI se ha inicializado correctamente.</span><span class="sxs-lookup"><span data-stu-id="93111-118">The MAPI subsystem was initialized successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="93111-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="93111-119">Remarks</span></span>

<span data-ttu-id="93111-120">La función **MAPIInitialize** incrementa el número de referencias MAPI para el subsistema MAPI y la función [MAPIUninitialize](mapiuninitialize.md) reduce el recuento de referencia interna.</span><span class="sxs-lookup"><span data-stu-id="93111-120">The **MAPIInitialize** function increments the MAPI reference count for the MAPI subsystem, and the [MAPIUninitialize](mapiuninitialize.md) function decrements the internal reference count.</span></span> <span data-ttu-id="93111-121">Por lo tanto, el número de llamadas a una función debe ser igual al número de llamadas al otro.</span><span class="sxs-lookup"><span data-stu-id="93111-121">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> <span data-ttu-id="93111-122">**MAPIInitialize** Devuelve S_OK si MAPI no se ha inicializado previamente.</span><span class="sxs-lookup"><span data-stu-id="93111-122">**MAPIInitialize** returns S_OK if MAPI has not been previously initialized.</span></span> 
  
<span data-ttu-id="93111-123">Un cliente o proveedor de servicios debe llamar a **MAPIInitialize** antes de realizar cualquier otra llamada MAPI.</span><span class="sxs-lookup"><span data-stu-id="93111-123">A client or service provider must call **MAPIInitialize** before making any other MAPI call.</span></span> <span data-ttu-id="93111-124">Si no lo hace, las llamadas del cliente o del proveedor de servicios devuelven el valor MAPI_E_NOT_INITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="93111-124">Failure to do so causes client or service provider calls to return the MAPI_E_NOT_INITIALIZED value.</span></span> 
  
<span data-ttu-id="93111-125">Al llamar a **MAPIInitialize** desde una aplicación multiproceso, establezca el parámetro _lpMapiInit_ en una estructura [MAPIINIT_0](mapiinit_0.md) declarada de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="93111-125">When calling **MAPIInitialize** from a multithreaded application, set the  _lpMapiInit_ parameter to a [MAPIINIT_0](mapiinit_0.md) structure that is declared as follows:</span></span> 
  
 <span data-ttu-id="93111-126">**MAPIINIT_0** MAPIINIT = {0, MAPI_MULTITHREAD_NOTIFICATIONS}</span><span class="sxs-lookup"><span data-stu-id="93111-126">**MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS}</span></span> 
  
<span data-ttu-id="93111-127">y llame a:</span><span class="sxs-lookup"><span data-stu-id="93111-127">and call:</span></span> 
  
 <span data-ttu-id="93111-128">**MAPIInitialize** (&amp;MAPIINIT);</span><span class="sxs-lookup"><span data-stu-id="93111-128">**MAPIInitialize** (&amp;MAPIINIT);</span></span> 
  
<span data-ttu-id="93111-129">Cuando se declara esta estructura, MAPI crea un subproceso independiente para controlar la ventana de notificación, que sigue hasta que el recuento de referencia inicializado caiga en cero.</span><span class="sxs-lookup"><span data-stu-id="93111-129">When this structure is declared, MAPI creates a separate thread to handle the notification window, which continues until the initialize reference count falls to zero.</span></span> <span data-ttu-id="93111-130">Un servicio de Windows debe establecer el miembro **ulflags** de la estructura **MAPIINIT_0** a la que apunta _lpMapiInit_ a MAPI_NT_SERVICE.</span><span class="sxs-lookup"><span data-stu-id="93111-130">A Windows service must set the **ulflags** member of the **MAPIINIT_0** structure pointed to by  _lpMapiInit_ to MAPI_NT_SERVICE.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="93111-131">No se puede llamar a **MAPIInitialize** o **MAPIUninitialize** desde dentro de una función **DllMain** de Win32 o cualquier otra función que cree o finalice subprocesos.</span><span class="sxs-lookup"><span data-stu-id="93111-131">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="93111-132">Para obtener más información, vea el [tema sobre cómo usar objetos seguros para](using-thread-safe-objects.md)subprocesos.</span><span class="sxs-lookup"><span data-stu-id="93111-132">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  
 <span data-ttu-id="93111-133">**MAPIInitialize** no devuelve ninguna información de error extendida.</span><span class="sxs-lookup"><span data-stu-id="93111-133">**MAPIInitialize** does not return any extended error information.</span></span> <span data-ttu-id="93111-134">A diferencia de la mayoría de las llamadas MAPI, el significado de los valores devueltos se define estrictamente para corresponderse con el paso concreto de la inicialización que produjo el error:</span><span class="sxs-lookup"><span data-stu-id="93111-134">Unlike most other MAPI calls, the meanings of its return values are strictly defined to correspond to the particular step of the initialization that failed:</span></span> 
  
1. <span data-ttu-id="93111-135">Comprueba los parámetros y las marcas.</span><span class="sxs-lookup"><span data-stu-id="93111-135">Checks parameters and flags.</span></span>
    
    <span data-ttu-id="93111-136">MAPI_E_INVALID_PARAMETER o MAPI_E_UNKNOWN_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="93111-136">MAPI_E_INVALID_PARAMETER or MAPI_E_UNKNOWN_FLAGS.</span></span> <span data-ttu-id="93111-137">El autor de la llamada pasó un parámetro o marca no válido.</span><span class="sxs-lookup"><span data-stu-id="93111-137">Caller passed invalid parameter or flag.</span></span>
    
2. <span data-ttu-id="93111-138">Inicializa las claves del registro requeridas por MAPI y confirma el tipo de sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="93111-138">Initializes registry keys required by MAPI and confirms the type of operating system.</span></span> <span data-ttu-id="93111-139">Este paso solo se produce si el proceso de cliente se ejecuta como un servicio en Windows y establece la marca de servicio MAPI_NT en la estructura **MAPIINIT_0** .</span><span class="sxs-lookup"><span data-stu-id="93111-139">This step only happens if the client process is running as a service under Windows and sets the MAPI_NT SERVICE flag in the **MAPIINIT_0** structure.</span></span> 
    
    <span data-ttu-id="93111-140">MAPI_E_TOO_COMPLEX.</span><span class="sxs-lookup"><span data-stu-id="93111-140">MAPI_E_TOO_COMPLEX.</span></span> <span data-ttu-id="93111-141">El proceso de llamada es un servicio de Windows y claves del registro que MAPI no pudo inicializar.</span><span class="sxs-lookup"><span data-stu-id="93111-141">The calling process is a Windows service and registry keys required by MAPI could not be initialized.</span></span> 
    
    <span data-ttu-id="93111-142">Puede que haya información adicional disponible en el registro de eventos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="93111-142">Additional information may be available in the application event log.</span></span>
    
3. <span data-ttu-id="93111-143">Compruebe la compatibilidad de MAPI con OLE y, a continuación, inicialice OLE.</span><span class="sxs-lookup"><span data-stu-id="93111-143">Check for the compatibility of MAPI with OLE, then initialize OLE.</span></span>
    
1. <span data-ttu-id="93111-144">Comprueba la compatibilidad entre las versiones actuales de OLE y MAPI.</span><span class="sxs-lookup"><span data-stu-id="93111-144">Checks for compatibility between the current versions of OLE and MAPI.</span></span> 
    
    <span data-ttu-id="93111-145">MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="93111-145">MAPI_E_VERSION.</span></span> <span data-ttu-id="93111-146">La versión de OLE instalada en la estación de trabajo no es compatible con esta versión de MAPI.</span><span class="sxs-lookup"><span data-stu-id="93111-146">The version of OLE installed on the workstation is not compatible with this version of MAPI.</span></span>
    
2. <span data-ttu-id="93111-147">Inicializa OLE.</span><span class="sxs-lookup"><span data-stu-id="93111-147">Initializes OLE.</span></span> 
    
    <span data-ttu-id="93111-148">Durante este paso, esta función puede devolver un código de error que no se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="93111-148">During this step only, this function can return an error code not listed here.</span></span> <span data-ttu-id="93111-149">Se debe suponer que cualquier error que _no_ se muestra aquí proviene de la función OLE **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="93111-149">Any error  _not_ listed here should be assumed to come from the OLE function **CoInitialize**.</span></span>
    
4. <span data-ttu-id="93111-150">Inicializa variables globales por proceso.</span><span class="sxs-lookup"><span data-stu-id="93111-150">Initializes per-process global variables.</span></span>
    
    <span data-ttu-id="93111-151">MAPI_E_SESSION_LIMIT.</span><span class="sxs-lookup"><span data-stu-id="93111-151">MAPI_E_SESSION_LIMIT.</span></span> <span data-ttu-id="93111-152">MAPI configura el contexto específico del proceso actual.</span><span class="sxs-lookup"><span data-stu-id="93111-152">MAPI sets up context specific to the current process.</span></span> <span data-ttu-id="93111-153">Pueden producirse errores en Win16 si el número de procesos supera un número determinado o en cualquier sistema si se agota la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="93111-153">Failures may occur on Win16 if the number of processes exceeds a certain number, or on any system if available memory is exhausted.</span></span>
    
5. <span data-ttu-id="93111-154">Inicializa variables globales compartidas de todos los procesos.</span><span class="sxs-lookup"><span data-stu-id="93111-154">Initializes shared global variables of all processes.</span></span>
    
    <span data-ttu-id="93111-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span><span class="sxs-lookup"><span data-stu-id="93111-155">MAPI_E_NOT_ENOUGH_RESOURCES.</span></span> <span data-ttu-id="93111-156">No hay suficientes recursos del sistema disponibles para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="93111-156">Not enough system resources were available to complete the operation.</span></span>
    
6. <span data-ttu-id="93111-157">Inicializa el motor de notificación, crea su ventana y su subproceso si lo solicita la marca MAPI_MULTITHREAD_NOTIFICATIONS.</span><span class="sxs-lookup"><span data-stu-id="93111-157">Initializes the notification engine, creates its window and its thread if requested by the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
    
    <span data-ttu-id="93111-158">MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="93111-158">MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="93111-159">Puede producirse un error si se agotan los recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="93111-159">May fail if system resources are exhausted.</span></span> 
    
7. <span data-ttu-id="93111-160">Carga e inicializa el proveedor de perfiles.</span><span class="sxs-lookup"><span data-stu-id="93111-160">Loads and initializes the profile provider.</span></span> <span data-ttu-id="93111-161">Comprueba que **MAPIInitialize** puede tener acceso a la clave del registro donde se almacenan los datos del perfil.</span><span class="sxs-lookup"><span data-stu-id="93111-161">Verifies that **MAPIInitialize** can access the registry key where profile data are stored.</span></span> 
    
    <span data-ttu-id="93111-162">MAPI_E_NOT_INITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="93111-162">MAPI_E_NOT_INITIALIZED.</span></span> <span data-ttu-id="93111-163">El proveedor de perfiles detectó un error.</span><span class="sxs-lookup"><span data-stu-id="93111-163">The profile provider has encountered an error.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="93111-164">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="93111-164">MFCMAPI reference</span></span>

<span data-ttu-id="93111-165">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="93111-165">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="93111-166">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="93111-166">**File**</span></span>|<span data-ttu-id="93111-167">**Función**</span><span class="sxs-lookup"><span data-stu-id="93111-167">**Function**</span></span>|<span data-ttu-id="93111-168">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="93111-168">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="93111-169">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="93111-169">ContentsTableListCtrl.cpp</span></span>  <br/> ||<span data-ttu-id="93111-170">MFCMAPI usa el método **MAPIInitialize** para inicializar MAPI en un subproceso en segundo plano para realizar algún procesamiento de tabla.</span><span class="sxs-lookup"><span data-stu-id="93111-170">MFCMAPI uses the **MAPIInitialize** method to initialize MAPI on a background thread to do some table processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="93111-171">Ver también</span><span class="sxs-lookup"><span data-stu-id="93111-171">See also</span></span>



[<span data-ttu-id="93111-172">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="93111-172">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

