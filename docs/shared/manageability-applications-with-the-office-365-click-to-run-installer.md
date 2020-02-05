---
title: Integración de aplicaciones de administración con Office 365 Installer de hacer clic y ejecutar
manager: lindalu
ms.date: 10/22/2017
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Obtenga información sobre cómo integrar el instalador de hacer clic y ejecutar de Office 365 con una solución de administración de software.
ms.openlocfilehash: 0c695d538a0a906bce19719c2735cb39740ff6a2
ms.sourcegitcommit: 31b0a7373ff74fe1d6383c30bc67d7675b73d283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2020
ms.locfileid: "41773739"
---
# <a name="integrating-manageability-applications-with-office-365-click-to-run-installer"></a><span data-ttu-id="8acbe-103">Integración de aplicaciones de administración con Office 365 Installer de hacer clic y ejecutar</span><span class="sxs-lookup"><span data-stu-id="8acbe-103">Integrating manageability applications with Office 365 click-to-run installer</span></span>

<span data-ttu-id="8acbe-104">Obtenga información sobre cómo integrar el instalador de hacer clic y ejecutar de Office 365 con una solución de administración de software.</span><span class="sxs-lookup"><span data-stu-id="8acbe-104">Learn how to integrate the Office 365 Click-to-Run installer with a software management solution.</span></span>
  
<span data-ttu-id="8acbe-105">El instalador de hacer clic y ejecutar de Office 365 proporciona una interfaz COM que permite a los profesionales de ti y a las soluciones de administración de software controlar mediante programación la administración de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="8acbe-105">The Office 365 Click-to-Run installer provides a COM interface that allows IT Professionals and software management solutions programmatic control over update management.</span></span> <span data-ttu-id="8acbe-106">Esta interfaz proporciona funciones de administración adicionales más allá de lo que proporciona la herramienta de implementación de Office.</span><span class="sxs-lookup"><span data-stu-id="8acbe-106">This interface provides additional management capabilities beyond what is provided by the Office Deployment Tool.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8acbe-107">Este artículo se aplica a Office 2016 y versiones posteriores, Office 365.</span><span class="sxs-lookup"><span data-stu-id="8acbe-107">This article applies to Office 2016 and later, Office 365.</span></span> 
  
## <a name="integrating-with-the-click-to-run"></a><span data-ttu-id="8acbe-108">Integración con hacer clic y ejecutar</span><span class="sxs-lookup"><span data-stu-id="8acbe-108">Integrating with the Click-to-Run</span></span>

<span data-ttu-id="8acbe-109">Para usar esta interfaz, una aplicación de administración invoca la interfaz COM y llama a las API expuestas que se comunican directamente con el servicio de instalación de hacer clic y ejecutar.</span><span class="sxs-lookup"><span data-stu-id="8acbe-109">To use this interface, a manageability application invokes the COM interface and calls exposed APIs that communicate directly with the Click-to-Run installation service.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8acbe-110">El instalador de hacer clic y ejecutar de Office puede ejecutarse desde la línea de comandos con parámetros que pueden controlar el comportamiento, tal como se documenta en la [herramienta de implementación de Office para hacer clic y ejecutar](https://www.microsoft.com/download/details.aspx?id=49117).</span><span class="sxs-lookup"><span data-stu-id="8acbe-110">The Office Click-to-Run installer can be run from the command-line with parameters that can control the behavior, as documented in [Office Deployment Tool for Click-to-Run](https://www.microsoft.com/download/details.aspx?id=49117).</span></span> 
  
<span data-ttu-id="8acbe-111">**A continuación se encuentra un diagrama conceptual de la interfaz COM**</span><span class="sxs-lookup"><span data-stu-id="8acbe-111">**Following is a conceptual diagram of the COM interface**</span></span>

<span data-ttu-id="8acbe-112">![Diagrama del uso de la interfaz COM en el programa de instalación de Hacer clic y ejecutar de Office.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Diagrama de uso de la interfaz COM en el instalador de hacer clic y ejecutar de Office")</span><span class="sxs-lookup"><span data-stu-id="8acbe-112">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
<span data-ttu-id="8acbe-113">El instalador de hacer clic y ejecutar de Office 365 implementa una interfaz basada en COM, **IUpdateNotify** registrada en CLSID **CLSID_UpdateNotifyObject**.</span><span class="sxs-lookup"><span data-stu-id="8acbe-113">The Office 365 Click-to-Run installer implements a COM-based interface, **IUpdateNotify** registered to CLSID **CLSID_UpdateNotifyObject**.</span></span>
  
<span data-ttu-id="8acbe-114">Esta interfaz se puede invocar de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8acbe-114">This interface can be invoked as follows:</span></span>
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

<span data-ttu-id="8acbe-115">La llamada solo se realizará correctamente si el autor de la llamada se ejecuta con privilegios elevados, ya que el programa de instalación de hacer clic y ejecutar debe ejecutarse con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="8acbe-115">The call will only succeed if the caller is running under elevated privileges, as the Click-to-Run installation program must be run with elevated privileges.</span></span>
  
<span data-ttu-id="8acbe-116">La interfaz com **IUpdateNotify** expone tres funciones asincrónicas que son responsables de validar los comandos y los parámetros, y de programar la ejecución con el servicio de instalación de hacer clic y ejecutar.</span><span class="sxs-lookup"><span data-stu-id="8acbe-116">The **IUpdateNotify** COM interface exposes three asynchronous functions responsible for validating the commands and parameters and scheduling execution with the Click-to-Run installation service.</span></span> 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

<span data-ttu-id="8acbe-117">El método, **status**, se puede usar para obtener información sobre el estado del último comando ejecutado o el estado del comando que se está ejecutando actualmente (es decir, correcto, error, códigos de error detallados).</span><span class="sxs-lookup"><span data-stu-id="8acbe-117">A forth method, **Status**, can be used to get information about the status of the last executed command or the status of the currently executing command (i.e. success, failure, detailed error codes).</span></span>
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

<span data-ttu-id="8acbe-118">Hay cuatro Estados en los que el servicio de instalación de hacer clic y ejecutar puede encontrarse durante su ciclo de vida, durante el cual se puede llamar a los métodos de **IUpdateNotify** ; Reiniciar, inactivo, descargar y aplicar.</span><span class="sxs-lookup"><span data-stu-id="8acbe-118">There are four states that the Click-to-Run installation service may be in during its lifecycle, during which **IUpdateNotify** methods may be called; Rebooting, Idle, Downloading and Applying.</span></span> 
  
<span data-ttu-id="8acbe-119">**A continuación se encuentra el diagrama de máquina de estado de interfaz COM**</span><span class="sxs-lookup"><span data-stu-id="8acbe-119">**Following is the COM Interface State Machine diagram**</span></span>

<span data-ttu-id="8acbe-120">![Un diagrama de estado de la interfaz COM.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Un diagrama de estado para la interfaz COM")</span><span class="sxs-lookup"><span data-stu-id="8acbe-120">![A state diagram for the COM interface.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "A state diagram for the COM interface")</span></span>
  
> [!NOTE]
> <span data-ttu-id="8acbe-121">**Reiniciar**: cuando el equipo arranca, hay un período de tiempo en el que el servicio de instalación de hacer clic y ejecutar no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8acbe-121">**Rebooting**: When the machine is booting there is a period of time when the Click-to-Run installer service is not available.</span></span> <span data-ttu-id="8acbe-122">Una llamada correcta al método de estado después de un reinicio, devolverá eUPDATE_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="8acbe-122">A successful call to the Status method after a reboot will return eUPDATE_UNKNOWN.</span></span> 
  
<span data-ttu-id="8acbe-123">**Inactivo:** Cuando el programa de instalación de hacer clic y ejecutar se encuentra en estado inactivo, puede llamar a:</span><span class="sxs-lookup"><span data-stu-id="8acbe-123">**Idle:** When the Click-to-Run installer is in the idle state, you can call:</span></span> 
  
- <span data-ttu-id="8acbe-124">**Aplicar**: instalar contenido descargado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="8acbe-124">**Apply**: Install previously downloaded content.</span></span>
    
- <span data-ttu-id="8acbe-125">**Cancel**: devuelve `0x800000e`"se llamó a un método en un momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="8acbe-125">**Cancel**: Returns  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="8acbe-126">**Descargar**: descarga nuevo contenido en el cliente para su instalación posterior.</span><span class="sxs-lookup"><span data-stu-id="8acbe-126">**Download**: Downloads new content to the client for later installation.</span></span>
    
- <span data-ttu-id="8acbe-127">**Status**: devuelve el resultado de la última acción completada o un mensaje de error si la acción finalizó por error.</span><span class="sxs-lookup"><span data-stu-id="8acbe-127">**Status**: Returns the result of the last completed action, or an error message if the action ended in failure.</span></span> <span data-ttu-id="8acbe-128">Si no hay ninguna acción anterior, **status** devuelve `eUPDATE_UNKNOWN`.</span><span class="sxs-lookup"><span data-stu-id="8acbe-128">If there is no previous action, **Status** returns  `eUPDATE_UNKNOWN`.</span></span>
    
<span data-ttu-id="8acbe-129">**Descargar:** Cuando el programa de instalación de hacer clic y ejecutar se encuentra en estado de descarga, puede llamar a:</span><span class="sxs-lookup"><span data-stu-id="8acbe-129">**Downloading:** When the Click-to-Run installer is in the downloading state, you can call:</span></span> 
  
- <span data-ttu-id="8acbe-130">**Apply**: devuelve un **HRESULT** con el valor `0x800000e`, "se llamó a un método en un momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="8acbe-130">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="8acbe-131">**Cancelar**: detiene la descarga y quita el contenido parcialmente descargado.</span><span class="sxs-lookup"><span data-stu-id="8acbe-131">**Cancel**: Stops the download and removes the partially downloaded content.</span></span>
    
- <span data-ttu-id="8acbe-132">**Download**: devuelve un **HRESULT** con el valor `0x800000e`"se llamó a un método en un momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="8acbe-132">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="8acbe-133">**Status**: devuelve **DOWNLOAD_WIP** para indicar que el trabajo de descarga está en curso.</span><span class="sxs-lookup"><span data-stu-id="8acbe-133">**Status**: Returns **DOWNLOAD_WIP** to indicate that download work is in progress.</span></span> 
    
<span data-ttu-id="8acbe-134">**Aplicar:** Cuando el programa de instalación de hacer clic y ejecutar está en proceso de instalar contenido de descarga anterior:</span><span class="sxs-lookup"><span data-stu-id="8acbe-134">**Applying:** When the Click-to-Run installer is in the process of installing previously download content:</span></span> 
  
- <span data-ttu-id="8acbe-135">**Apply**: devuelve un **HRESULT** con el valor `0x800000e`, "se llamó a un método en un momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="8acbe-135">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="8acbe-136">**Cancelar**: devuelve `0x800000e`, la acción Apply no se puede cancelar.</span><span class="sxs-lookup"><span data-stu-id="8acbe-136">**Cancel**: Returns  `0x800000e`, the Apply action cannot be canceled.</span></span>
    
- <span data-ttu-id="8acbe-137">**Download**: devuelve un **HRESULT** con el valor `0x800000e`"se llamó a un método en un momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="8acbe-137">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="8acbe-138">**Status**: devuelve **APPLY_WIP** para indicar que el trabajo de aplicación está en curso.</span><span class="sxs-lookup"><span data-stu-id="8acbe-138">**Status**: Returns **APPLY_WIP** to indicate that apply work is in progress.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="8acbe-139">Dado que OfficeC2RCOM es un servicio COM+ y se carga dinámicamente, es necesario llamar a **CoCreateInstance** cada vez que se llama a un método en esta clase para garantizar que se obtiene el resultado esperado.</span><span class="sxs-lookup"><span data-stu-id="8acbe-139">Since OfficeC2RCOM is a COM+ service and is dynamically loaded, you need to call **CoCreateInstance** every time you call a method on this class to ensure that you get the expected result.</span></span> <span data-ttu-id="8acbe-140">El servicio COM+ administrará la creación de una nueva instancia si es necesario.</span><span class="sxs-lookup"><span data-stu-id="8acbe-140">The COM+ service will handle creating a new instance if necessary.</span></span> <span data-ttu-id="8acbe-141">Cuando se llama a uno de los métodos por primera vez, COM+ cargará el objeto **IUpdateNotify** y lo ejecutará dentro de una de las instancias de dllhost. exe.</span><span class="sxs-lookup"><span data-stu-id="8acbe-141">When one of the methods is called for the first time, COM+ will load the **IUpdateNotify** object and run it within one of the dllhost.exe instances.</span></span> <span data-ttu-id="8acbe-142">El nuevo objeto permanecerá activo durante unos 3 minutos de inactividad.</span><span class="sxs-lookup"><span data-stu-id="8acbe-142">The new object will stay active for about 3 minutes in idle.</span></span> <span data-ttu-id="8acbe-143">Si se realiza una llamada subsiguiente en tres minutos después de la última llamada, el objeto **IUpdateNotify** permanecerá cargado y no se creará una nueva instancia.</span><span class="sxs-lookup"><span data-stu-id="8acbe-143">If a subsequent call is made within three minutes of the last call, the **IUpdateNotify** object will remain loaded and a new instance is not created.</span></span> <span data-ttu-id="8acbe-144">Si no se realiza ninguna llamada en un plazo de tres minutos, el objeto IUpdateNotify se descargará y se creará un nuevo objeto **IUpdateNotify** cuando se realice la siguiente llamada.</span><span class="sxs-lookup"><span data-stu-id="8acbe-144">If no call is made within three minutes, the IUpdateNotify object will be unloaded and a new **IUpdateNotify** object will be created when the next call is made.</span></span> 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a><span data-ttu-id="8acbe-145">Guía de referencia de la API de COM del instalador de hacer clic y ejecutar</span><span class="sxs-lookup"><span data-stu-id="8acbe-145">Click-to-Run installer COM API reference guide</span></span>

<span data-ttu-id="8acbe-146">En la siguiente documentación de referencia de la API:</span><span class="sxs-lookup"><span data-stu-id="8acbe-146">In the following API reference documentation:</span></span>
  
- <span data-ttu-id="8acbe-147">Los parámetros se encuentran en un formato de par clave-valor separados por un espacio.</span><span class="sxs-lookup"><span data-stu-id="8acbe-147">Parameters are in a key/value pair format separated by a space.</span></span>
    
- <span data-ttu-id="8acbe-148">Los parámetros no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8acbe-148">The parameters are not case-sensitive.</span></span>
    
- <span data-ttu-id="8acbe-149">Hay una [lista de parámetros](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) con documentación disponible.</span><span class="sxs-lookup"><span data-stu-id="8acbe-149">There is a [list of parameters](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) with documentation available.</span></span> 
    
- <span data-ttu-id="8acbe-150">Ahora se incluye un resumen de la interfaz de IUpdateNotify2.</span><span class="sxs-lookup"><span data-stu-id="8acbe-150">Summary of IUpdateNotify2 interface is now included.</span></span>
    
### <a name="apply"></a><span data-ttu-id="8acbe-151">Apply</span><span class="sxs-lookup"><span data-stu-id="8acbe-151">Apply</span></span>

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a><span data-ttu-id="8acbe-152">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8acbe-152">Parameters</span></span>

-  <span data-ttu-id="8acbe-153">_displaylevel_: **true** para mostrar el estado de la instalación, incluidos los errores, durante el proceso de actualización; **false** para ocultar el estado de la instalación, incluidos los errores, durante el proceso de actualización.</span><span class="sxs-lookup"><span data-stu-id="8acbe-153">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="8acbe-154">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="8acbe-154">The default is **false**.</span></span>
    
-  <span data-ttu-id="8acbe-155">_forceappshutdown_: **true** para forzar que las aplicaciones de Office se cierren inmediatamente cuando se desencadena la acción **Apply** ; **false** se producirá un error si se ejecuta cualquier aplicación de Office.</span><span class="sxs-lookup"><span data-stu-id="8acbe-155">_forceappshutdown_: **true** to force Office applications to shut down immediately when the **Apply** action is triggered; **false** to fail if any Office applications are running.</span></span> <span data-ttu-id="8acbe-156">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="8acbe-156">The default is **false**.</span></span> <span data-ttu-id="8acbe-157">Vea los [comentarios](#bk_ApplyRemark) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8acbe-157">See [Remarks](#bk_ApplyRemark) for more information.</span></span> 
    
  <span data-ttu-id="8acbe-158">Si se está ejecutando cualquier aplicación de Office cuando se desencadena la acción **Apply** , la acción **Apply** producirá un error.</span><span class="sxs-lookup"><span data-stu-id="8acbe-158">If any Office application is running when the **Apply** action is triggered, the **Apply** action will usually fail.</span></span> <span data-ttu-id="8acbe-159">Pasar `forceappshutdown=true` al método **Apply** hará que el servicio **OfficeClickToRun** cierre inmediatamente las aplicaciones y aplique la actualización.</span><span class="sxs-lookup"><span data-stu-id="8acbe-159">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down the applications and apply the update.</span></span> <span data-ttu-id="8acbe-160">En este caso, el usuario puede experimentar pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="8acbe-160">The user may experience data loss in this case.</span></span> 
    
#### <a name="return-results"></a><span data-ttu-id="8acbe-161">Resultados devueltos</span><span class="sxs-lookup"><span data-stu-id="8acbe-161">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8acbe-162">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="8acbe-162">**S_OK**</span></span> <br/> |<span data-ttu-id="8acbe-163">La acción se ha enviado correctamente al servicio de hacer clic y ejecutar para su ejecución.</span><span class="sxs-lookup"><span data-stu-id="8acbe-163">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="8acbe-164">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="8acbe-164">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="8acbe-165">El autor de la llamada no se está ejecutando con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="8acbe-165">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="8acbe-166">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="8acbe-166">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="8acbe-167">Se pasaron parámetros no válidos.</span><span class="sxs-lookup"><span data-stu-id="8acbe-167">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="8acbe-168">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="8acbe-168">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="8acbe-169">La acción no está permitida en este momento.</span><span class="sxs-lookup"><span data-stu-id="8acbe-169">Action is not allowed at this time.</span></span> <span data-ttu-id="8acbe-170">Vea los [comentarios](#bk_ApplyRemark) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8acbe-170">See [Remarks](#bk_ApplyRemark) for more information.</span></span>  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="8acbe-171">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8acbe-171">Remarks</span></span>

- <span data-ttu-id="8acbe-172">Si se está ejecutando cualquier aplicación de Office cuando se desencadena la acción **Apply** , se producirá un error en la acción **Apply** .</span><span class="sxs-lookup"><span data-stu-id="8acbe-172">If any Office application is running when the **Apply** action is triggered, the **Apply** action will fail.</span></span> <span data-ttu-id="8acbe-173">Pasar `forceappshutdown=true` al método **Apply** hará que el servicio **OfficeClickToRun** cierre inmediatamente todas las aplicaciones de Office que se estén ejecutando y aplique la actualización.</span><span class="sxs-lookup"><span data-stu-id="8acbe-173">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down any Office applications that are running and apply the update.</span></span> <span data-ttu-id="8acbe-174">El usuario puede experimentar datos porque no se le pide que guarde los cambios realizados en los documentos abiertos.</span><span class="sxs-lookup"><span data-stu-id="8acbe-174">The user may experience data as they are not prompted to save changes to open documents..</span></span> 
    
- <span data-ttu-id="8acbe-175">Esta acción solo se puede desencadenar cuando el estado de COM es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="8acbe-175">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="8acbe-176">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="8acbe-176">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="8acbe-177">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="8acbe-177">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="8acbe-178">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="8acbe-178">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="8acbe-179">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="8acbe-179">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="8acbe-180">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="8acbe-180">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="8acbe-181">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="8acbe-181">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="8acbe-182">Si se llama al método **Apply** sin descargar previamente el contenido, el método **Apply** notificará que el proceso se ha **realizado** correctamente, ya que se ha detectado que no se ha aplicado nada y que se ha completado el proceso de **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="8acbe-182">If you call the **Apply** method without previously downloading content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
### <a name="cancel"></a><span data-ttu-id="8acbe-183">Cancel</span><span class="sxs-lookup"><span data-stu-id="8acbe-183">Cancel</span></span>

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a><span data-ttu-id="8acbe-184">Resultados devueltos</span><span class="sxs-lookup"><span data-stu-id="8acbe-184">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8acbe-185">S_OK</span><span class="sxs-lookup"><span data-stu-id="8acbe-185">S_OK</span></span>  <br/> |<span data-ttu-id="8acbe-186">La acción se ha enviado correctamente al servicio de hacer clic y ejecutar para su ejecución.</span><span class="sxs-lookup"><span data-stu-id="8acbe-186">Action was successfully submitted to the Click-to-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="8acbe-187">E_ILLEGAL_METHOD_CALL</span><span class="sxs-lookup"><span data-stu-id="8acbe-187">E_ILLEGAL_METHOD_CALL</span></span>  <br/> |<span data-ttu-id="8acbe-188">La acción no está permitida en este momento.</span><span class="sxs-lookup"><span data-stu-id="8acbe-188">Action is not allowed at this time.</span></span> <span data-ttu-id="8acbe-189">Vea la sección [comentarios](#bk_CancelRemarks) para obtener más información</span><span class="sxs-lookup"><span data-stu-id="8acbe-189">See the [Remarks](#bk_CancelRemarks) section for more information</span></span>  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a><span data-ttu-id="8acbe-190">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8acbe-190">Remarks</span></span>

- <span data-ttu-id="8acbe-191">Este método sólo se puede desencadenar cuando el identificador de estado COM **eDOWNLOAD_WIP**.</span><span class="sxs-lookup"><span data-stu-id="8acbe-191">This method can only be triggered when the COM status id **eDOWNLOAD_WIP**.</span></span> <span data-ttu-id="8acbe-192">Se intentará cancelar la acción de descarga actual.</span><span class="sxs-lookup"><span data-stu-id="8acbe-192">It will attempt to cancel the current download action.</span></span> <span data-ttu-id="8acbe-193">El estado de COM cambiará a **eDOWNLOAD_CANCELLING** y, finalmente, cambiará a **eDOWNLOAD_CANCELED**.</span><span class="sxs-lookup"><span data-stu-id="8acbe-193">The COM status will change to **eDOWNLOAD_CANCELLING** and eventually change to **eDOWNLOAD_CANCELED**.</span></span> <span data-ttu-id="8acbe-194">El estado COM devolverá **E_ILLEGAL_METHOD_CALL** si se desencadena en cualquier otro momento.</span><span class="sxs-lookup"><span data-stu-id="8acbe-194">The COM status will return **E_ILLEGAL_METHOD_CALL** if triggered at any other time.</span></span> 
    
### <a name="download"></a><span data-ttu-id="8acbe-195">Descargar</span><span class="sxs-lookup"><span data-stu-id="8acbe-195">Download</span></span>

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a><span data-ttu-id="8acbe-196">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8acbe-196">Parameters</span></span>

-  <span data-ttu-id="8acbe-197">_displaylevel_: **true** para mostrar el estado de la instalación, incluidos los errores, durante el proceso de actualización; **false** para ocultar el estado de la instalación, incluidos los errores, durante el proceso de actualización.</span><span class="sxs-lookup"><span data-stu-id="8acbe-197">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="8acbe-198">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="8acbe-198">The default is **false**.</span></span>
    
-  <span data-ttu-id="8acbe-199">_updatebaseurl_: dirección URL al origen de descarga alternativo.</span><span class="sxs-lookup"><span data-stu-id="8acbe-199">_updatebaseurl_: URL to the alternate download source.</span></span>
    
-  <span data-ttu-id="8acbe-200">_updatetoversion_: versión en la que se va a actualizar Office.</span><span class="sxs-lookup"><span data-stu-id="8acbe-200">_updatetoversion_: The version to update Office to.</span></span> <span data-ttu-id="8acbe-201">Defina este parámetro si desea actualizar a una versión anterior a la versión instalada actualmente.</span><span class="sxs-lookup"><span data-stu-id="8acbe-201">Define this parameter if you want to update to an older version than the version that is currently installed.</span></span>
    
-  <span data-ttu-id="8acbe-202">_downloadsource_: CLSID de la implementación de **IBackgroundCopyManager** personalizada (Administrador de bits).</span><span class="sxs-lookup"><span data-stu-id="8acbe-202">_downloadsource_: CLSID of the customized **IBackgroundCopyManager** implementation (BITS manager).</span></span> 
    
-  <span data-ttu-id="8acbe-203">_contentid_: identifica el contenido que se va a descargar desde el servidor de contenido mediante el administrador de bits personalizado.</span><span class="sxs-lookup"><span data-stu-id="8acbe-203">_contentid_: Identifies the content to download from the content server through the customized BITS manager.</span></span> <span data-ttu-id="8acbe-204">Este valor se pasa a través de la interfaz de BITS para la interpretación.</span><span class="sxs-lookup"><span data-stu-id="8acbe-204">This value is passed through the BITS interface for interpretation.</span></span>
    
#### <a name="return-results"></a><span data-ttu-id="8acbe-205">Resultados devueltos</span><span class="sxs-lookup"><span data-stu-id="8acbe-205">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8acbe-206">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="8acbe-206">**S_OK**</span></span> <br/> |<span data-ttu-id="8acbe-207">La acción se ha enviado correctamente al servicio de hacer clic y ejecutar para su ejecución.</span><span class="sxs-lookup"><span data-stu-id="8acbe-207">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="8acbe-208">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="8acbe-208">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="8acbe-209">El autor de la llamada no se está ejecutando con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="8acbe-209">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="8acbe-210">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="8acbe-210">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="8acbe-211">Se pasaron parámetros no válidos.</span><span class="sxs-lookup"><span data-stu-id="8acbe-211">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="8acbe-212">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="8acbe-212">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="8acbe-213">La acción no está permitida en este momento.</span><span class="sxs-lookup"><span data-stu-id="8acbe-213">Action is not allowed at this time.</span></span> <span data-ttu-id="8acbe-214">Vea los [comentarios](#bk_DownloadRemark) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8acbe-214">See [Remarks](#bk_DownloadRemark) for more information.</span></span>  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="8acbe-215">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8acbe-215">Remarks</span></span>

- <span data-ttu-id="8acbe-216">Debe especificar _downloadsource_ y _contentid_ como un par.</span><span class="sxs-lookup"><span data-stu-id="8acbe-216">You must specify  _downloadsource_ and  _contentid_ as a pair.</span></span> <span data-ttu-id="8acbe-217">De lo contrario, el método de **descarga** devolverá un error de **E_INVALIDARG** .</span><span class="sxs-lookup"><span data-stu-id="8acbe-217">If not, the **Download** method will return an **E_INVALIDARG** error.</span></span> 
    
- <span data-ttu-id="8acbe-218">Si se proporciona _downloadsource_, _contentid_y _updatebaseurl_ , se omitirá _updatebaseurl_ .</span><span class="sxs-lookup"><span data-stu-id="8acbe-218">If  _downloadsource_,  _contentid_, and  _updatebaseurl_ are provided,  _updatebaseurl_ will be ignored.</span></span> 
    
- <span data-ttu-id="8acbe-219">Esta acción solo se puede desencadenar cuando el estado de COM es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="8acbe-219">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="8acbe-220">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="8acbe-220">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="8acbe-221">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="8acbe-221">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="8acbe-222">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="8acbe-222">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="8acbe-223">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="8acbe-223">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="8acbe-224">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="8acbe-224">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="8acbe-225">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="8acbe-225">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="8acbe-226">Si se llama al método **Apply** sin descargar previamente el contenido, el método **Apply** informará de que el proceso se ha detectado correctamente **, ya que** se ha detectado que no se ha aplicado nada y se ha completado el proceso de **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="8acbe-226">If you call the **Apply** method without previously downloaded content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
#### <a name="examples"></a><span data-ttu-id="8acbe-227">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8acbe-227">Examples</span></span>

- <span data-ttu-id="8acbe-228">Para descargar el contenido del administrador de BITS personalizado: llame a la función **download ()** y pase los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="8acbe-228">To download the content from the customized BITS manager: Call the **download()** function passing the following parameters:</span></span> 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- <span data-ttu-id="8acbe-229">Para descargar el contenido de la red CDN de Microsoft: llame a la función **download ()** sin especificar los parámetros _downloadsource_, _contentid_o _updatebaseurl_ .</span><span class="sxs-lookup"><span data-stu-id="8acbe-229">To download the content from the Microsoft CDN: Call the **download()** function without specifying the  _downloadsource_,  _contentid_, or  _updatebaseurl_ parameters.</span></span> 
    
- <span data-ttu-id="8acbe-230">Para descargar el contenido desde una ubicación personalizada: llame a la función **download ()** y pase el parámetro siguiente:</span><span class="sxs-lookup"><span data-stu-id="8acbe-230">To download the content from a customized location: Call the **download()** function passing the following parameter:</span></span> 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a><span data-ttu-id="8acbe-231">Estado</span><span class="sxs-lookup"><span data-stu-id="8acbe-231">Status</span></span>

```cpp
typdef struct _UPDATE_STATUS_REPORT
{
    UPDATE_STATUS status;
    UINT error;
    LPCWSTR contentid;
}UPDATE_STATUS_REPORT;
HRESULT status([out] _UPDATE_STATUS_REPORT& pUpdateStatusReport) // Get status of current action
```

#### <a name="parameters"></a><span data-ttu-id="8acbe-232">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8acbe-232">Parameters</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="8acbe-233">_pUpdateStatusReport_</span><span class="sxs-lookup"><span data-stu-id="8acbe-233">_pUpdateStatusReport_</span></span> <br/> |<span data-ttu-id="8acbe-234">Puntero a una estructura UPDATE_STATUS_REPORT.</span><span class="sxs-lookup"><span data-stu-id="8acbe-234">Pointer to an UPDATE_STATUS_REPORT structure.</span></span>  <br/> |
   
#### <a name="return-results"></a><span data-ttu-id="8acbe-235">Resultados devueltos</span><span class="sxs-lookup"><span data-stu-id="8acbe-235">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8acbe-236">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="8acbe-236">**S_OK**</span></span> <br/> |<span data-ttu-id="8acbe-237">El método **status** siempre devuelve este resultado.</span><span class="sxs-lookup"><span data-stu-id="8acbe-237">The **Status** method always returns this result.</span></span> <span data-ttu-id="8acbe-238">Inspeccione `UPDATE_STATUS_RESULT` la estructura del estado de la acción actual.</span><span class="sxs-lookup"><span data-stu-id="8acbe-238">Inspect the  `UPDATE_STATUS_RESULT` structure for the status of the current action.</span></span>  <br/> |
   
#### <a name="remarks"></a><span data-ttu-id="8acbe-239">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8acbe-239">Remarks</span></span>

- <span data-ttu-id="8acbe-240">El campo Estado de `UPDATE_STATUS_REPORT` contiene el estado de la acción actual.</span><span class="sxs-lookup"><span data-stu-id="8acbe-240">The status field of the  `UPDATE_STATUS_REPORT` contains the status of the current action.</span></span> <span data-ttu-id="8acbe-241">Se devuelve uno de los siguientes valores de estado:</span><span class="sxs-lookup"><span data-stu-id="8acbe-241">One of the following status values is returned:</span></span> 
    
  ```cpp
  typedef enum _UPDATE_STATUS
  {
  eUPDATE_UNKNOWN = 0,
  eDOWNLOAD_PENDING,
  eDOWNLOAD_WIP,
  eDOWNLOAD_CANCELLING,
  eDOWNLOAD_CANCELLED,
  eDOWNLOAD_FAILED,
  eDOWNLOAD_SUCCEEDED,
  eAPPLY_PENDING,
  eAPPLY_WIP,
  eAPPLY_SUCCEEDED,
  eAPPLY_FAILED,
  } UPDATE_STATUS;
  
  ```

- <span data-ttu-id="8acbe-242">Si se produce un error en el último comando, el campo de error `UPDATE_STATUS_REPORT` del contiene información detallada sobre el error.</span><span class="sxs-lookup"><span data-stu-id="8acbe-242">If the last command resulted in an error, the error field of the  `UPDATE_STATUS_REPORT` contains detailed information about the error.</span></span> <span data-ttu-id="8acbe-243">Se devuelven dos tipos de códigos de error del método **status** .</span><span class="sxs-lookup"><span data-stu-id="8acbe-243">Two types of error codes are returned from the **Status** method.</span></span> 
    
- <span data-ttu-id="8acbe-244">Si el error es menor `UPDATE_ERROR_CODE::eUNKNOWN`que, el error es uno de los siguientes códigos de error predefinidos:</span><span class="sxs-lookup"><span data-stu-id="8acbe-244">If the error less than  `UPDATE_ERROR_CODE::eUNKNOWN`, the error is one of the following pre-defined error codes:</span></span>
    
  ```cpp
  typedef enum _UPDATE_ERROR_CODE
  {
  eOK = 0,
  eFAILED_UNEXPECTED,
  eTRIGGER_DISABLED,
  ePIPELINE_IN_USE,
  eFAILED_STOP_C2RSERVICE,
  eFAILED_GET_CLIENTUPDATEFOLDER,
  eFAILED_LOCK_PACKAGE_TO_UPDATE,
  eFAILED_CREATE_STREAM_SESSION,
  eFAILED_PUBLISH_WORKING_CONFIGURATION,
  eFAILED_DOWNLOAD_UPGRADE_PACKAGE,
  eFAILED_APPLY_UPGRADE_PACKAGE,
  eFAILED_INITIALIZE_RSOD,
  eFAILED_PUBLISH_RSOD,
  // Keep this one as the last
  eUNKNOWN
  } UPDATE_ERROR_CODE;
  
  ```

  <span data-ttu-id="8acbe-245">Si el código de error devuelto es `UPDATE_ERROR_CODE::eUNKNOWN` mayor que el **valor HRESULT** de una llamada a una función fallida.</span><span class="sxs-lookup"><span data-stu-id="8acbe-245">If the return error code is larger than  `UPDATE_ERROR_CODE::eUNKNOWN` it is the **HRESULT** of a failed function call.</span></span> <span data-ttu-id="8acbe-246">Para extraer el valor de `UPDATE_ERROR_CODE::eUNKNOWN` resta de HRESULT del valor devuelto en el campo `UPDATE_STATUS_REPORT`de error del.</span><span class="sxs-lookup"><span data-stu-id="8acbe-246">To extract the HRESULT subtract  `UPDATE_ERROR_CODE::eUNKNOWN` from the value returned in the error field of the  `UPDATE_STATUS_REPORT`.</span></span>
    
  <span data-ttu-id="8acbe-247">Para ver la lista completa de valores de estado y error, inspeccione la biblioteca de tipos de **IUpdateNotify** incrustada en OfficeC2RCom. dll.</span><span class="sxs-lookup"><span data-stu-id="8acbe-247">The complete list of status and error values can be viewed by inspecting the **IUpdateNotify** type library embedded in OfficeC2RCom.dll.</span></span> 
    
- <span data-ttu-id="8acbe-248">El campo contentid se usa para las llamadas al **Estado** una vez iniciada la **descarga** y devuelve el elemento contentid que se pasó a la llamada a **download** .</span><span class="sxs-lookup"><span data-stu-id="8acbe-248">The contentid field is used for calls to **Status** after **Download** has initiated and returns the contentid that was passed in to the **Download** call.</span></span> <span data-ttu-id="8acbe-249">Se recomienda inicializar este campo en **null** antes de llamar al método **status** y, a continuación, comprobar el valor una vez que se ha devuelto el **Estado** .</span><span class="sxs-lookup"><span data-stu-id="8acbe-249">It is a best practice to initialize this field to **null** before you call the **Status** method and then check the value after **Status** has been returned.</span></span> <span data-ttu-id="8acbe-250">Si el valor todavía es **null**, significa que no hay contentid para devolver.</span><span class="sxs-lookup"><span data-stu-id="8acbe-250">If the value is still **null**, that means there is no contentid to return.</span></span> <span data-ttu-id="8acbe-251">Si el valor no es **null**, debe liberarlo con una llamada a **SysFreeString ()**.</span><span class="sxs-lookup"><span data-stu-id="8acbe-251">If the value is not **null**, you need to free it with a call to **SysFreeString()**.</span></span> <span data-ttu-id="8acbe-252">A continuación, se muestra un fragmento de código sobre cómo llamar al **Estado** después de la **descarga**.</span><span class="sxs-lookup"><span data-stu-id="8acbe-252">Here is a code snippet of how to call **Status** after **Download**.</span></span>
    
  ```cpp
  std::wstring contentID;
  UPDATE_STATUS_REPORT statusReport;
  statusReport.status = eUPDATE_UNKNOWN;
  statusReport.error = eOK;
  statusReport.contentid = NULL;
  hr = p->Status(&statusReport);
  if (statusReport.contentid != NULL)
  {
  contentID = statusReport.contentid;
  SysFreeString(statusReport.contentid);
  }
  wprintf(L"ContentID: %s, Status: %d, LastError: %d", contentID.c_str(), statusReport.status, statusReport.error);
  
  ```

### <a name="summary-of-iupdatenotify2-interface"></a><span data-ttu-id="8acbe-253">Resumen de la interfaz de IUpdateNotify2</span><span class="sxs-lookup"><span data-stu-id="8acbe-253">Summary of IUpdateNotify2 interface</span></span>

> [!NOTE]
> <span data-ttu-id="8acbe-254">Este resumen se proporciona como una información de complementos para [la integración de aplicaciones de administración con el instalador de hacer clic y ejecutar de Office 365](https://docs.microsoft.com/office/client-developer/shared/manageability-applications-with-the-office-365-click-to-run-installer).</span><span class="sxs-lookup"><span data-stu-id="8acbe-254">This summary is provided as a compliment info to [Integrating manageability applications with the Office 365 click-to-run installer](https://docs.microsoft.com/office/client-developer/shared/manageability-applications-with-the-office-365-click-to-run-installer).</span></span> <span data-ttu-id="8acbe-255">Una vez que se actualiza el documento público, este documento puede considerarse obsoleto.</span><span class="sxs-lookup"><span data-stu-id="8acbe-255">Once the public doc is updated, this doc can be considered as obsolete.</span></span> 
  
<span data-ttu-id="8acbe-256">De C2RTenant [16.0.8208.6352](https://oloop/BuildGroup/Details/tenantc2rclient#3519/1255278) (la primera compilación disponible públicamente debe ser la compilación de la horquilla de junio--8326. \*) se ha agregado una nueva interfaz de **IUpdateNotify2** .</span><span class="sxs-lookup"><span data-stu-id="8acbe-256">From C2RTenant [16.0.8208.6352](https://oloop/BuildGroup/Details/tenantc2rclient#3519/1255278) (First publicly available build should be June fork build -- 8326.\*) we have added a new **IUpdateNotify2** interface.</span></span> <span data-ttu-id="8acbe-257">A continuación se muestra información básica sobre esta interfaz:</span><span class="sxs-lookup"><span data-stu-id="8acbe-257">Here is some basic info about this interface:</span></span> 
  
- <span data-ttu-id="8acbe-258">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span><span class="sxs-lookup"><span data-stu-id="8acbe-258">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span></span>
    
- <span data-ttu-id="8acbe-259">Esta interfaz también hospedaba la interfaz IUpdateNotify original para proporcionar compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="8acbe-259">This interface also hosted the original IUpdateNotify interface to provide backward compatibility.</span></span> <span data-ttu-id="8acbe-260">Lo que significa que si usa esta interfaz, tiene acceso a todos los métodos proporcionados en la interfaz **UpdateNotifyObject** .</span><span class="sxs-lookup"><span data-stu-id="8acbe-260">Which means if you use this interface, you have access to all the methods provided in **UpdateNotifyObject** interface.</span></span> 
    
- <span data-ttu-id="8acbe-261">Nuevos métodos agregados a IUpdateNotify2:</span><span class="sxs-lookup"><span data-stu-id="8acbe-261">New methods added to IUpdateNotify2:</span></span>
    
  - <span data-ttu-id="8acbe-262">**HRESULT** GetBlockingApps ([salida] BSTR \* AppsList).</span><span class="sxs-lookup"><span data-stu-id="8acbe-262">**HRESULT** GetBlockingApps([out] BSTR \* AppsList).</span></span> <span data-ttu-id="8acbe-263">Obtener actualizaciones bloqueo de la lista de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8acbe-263">Get updates blocking apps list.</span></span> <span data-ttu-id="8acbe-264">Esta llamada devolverá la ejecución de aplicaciones de Office que impedirán que el proceso de actualización continúe.</span><span class="sxs-lookup"><span data-stu-id="8acbe-264">This call will return running Office apps which will block the update process from proceeding.</span></span> 
    
  - <span data-ttu-id="8acbe-265">**HRESULT** GetOfficeDeploymentData ([in] int DataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span><span class="sxs-lookup"><span data-stu-id="8acbe-265">**HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span></span> <span data-ttu-id="8acbe-266">Obtener datos de implementación de Office.</span><span class="sxs-lookup"><span data-stu-id="8acbe-266">Get Office deployment Data.</span></span> 
    
- <span data-ttu-id="8acbe-267">Si desea usar los nuevos métodos, debe asegurarse de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8acbe-267">If you want to use the new methods, you need to make sure:</span></span>
    
  - <span data-ttu-id="8acbe-268">La versión de C2R es más reciente que la compilación\>anterior (= compilación de la bifurcación de junio).</span><span class="sxs-lookup"><span data-stu-id="8acbe-268">Your C2R version is newer than the above build (\>= June fork build).</span></span>
    
  - <span data-ttu-id="8acbe-269">Use UpdateNotifyObject2, en lugar de **UpdateNotifyObject** para llamar a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="8acbe-269">Use UpdateNotifyObject2, instead of **UpdateNotifyObject** to call **CoCreateInstance**.</span></span>
    
<span data-ttu-id="8acbe-270">Si no usa ninguno de los métodos nuevos, no es necesario cambiar nada.</span><span class="sxs-lookup"><span data-stu-id="8acbe-270">If you don't use any of the new methods, you don't need to change anything.</span></span> <span data-ttu-id="8acbe-271">Todos los métodos existentes funcionarán exactamente del mismo modo que antes.</span><span class="sxs-lookup"><span data-stu-id="8acbe-271">All the existing methods will work as exact the same way as before.</span></span>
  
## <a name="implementing-the-bits-interface"></a><span data-ttu-id="8acbe-272">Implementación de la interfaz de BITS</span><span class="sxs-lookup"><span data-stu-id="8acbe-272">Implementing the BITS interface</span></span>

<span data-ttu-id="8acbe-273">El [servicio de transferencia inteligente en segundo plano](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (bits) es un servicio proporcionado por Microsoft para transferir archivos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="8acbe-273">The [Background Intelligent Transfer Service](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (BITS) is a service provided by Microsoft to transfer files between a client and server.</span></span> <span data-ttu-id="8acbe-274">BITS es uno de los canales que puede usar el instalador de hacer clic y ejecutar de Office para descargar contenido.</span><span class="sxs-lookup"><span data-stu-id="8acbe-274">BITS is one of the channels that Office Click-To-Run installer can use to download content.</span></span> <span data-ttu-id="8acbe-275">De forma predeterminada, el instalador de hacer clic y ejecutar de Office usa la implementación de BITS de Windows integrada para descargar el contenido de la red CDN.</span><span class="sxs-lookup"><span data-stu-id="8acbe-275">By default, the Office Click-To-Run installer uses the Windows' built in implementation of BITS to download the content from the CDN.</span></span> 
  
<span data-ttu-id="8acbe-276">Al suministrar una implementación BITS personalizada al método **download ()** de la interfaz **IUpdateNotify** , el software de administración puede controlar dónde y cómo descarga el contenido el cliente.</span><span class="sxs-lookup"><span data-stu-id="8acbe-276">By providing a customized BITS implementation to the **download()** method of the **IUpdateNotify** interface, your manageability software can control where and how the client downloads the content.</span></span> <span data-ttu-id="8acbe-277">Una interfaz de BITS personalizada es útil cuando se proporciona un canal de distribución de contenido personalizado distinto de los canales integrados de hacer clic y ejecutar, como la red CDN de Office, los servidores IIS o los recursos compartidos de archivos.</span><span class="sxs-lookup"><span data-stu-id="8acbe-277">A customized BITS interface is useful when providing a custom content distribution channel other than the Click-to-Run built-in channels, such as the Office CDN, IIS servers, or file shares.</span></span> 
  
<span data-ttu-id="8acbe-278">El requisito mínimo para que una interfaz de BITS personalizada funcione con Office C2R Service es:</span><span class="sxs-lookup"><span data-stu-id="8acbe-278">The minimum requirement for a customized BITS interface to work with Office C2R service is:</span></span>
  
- <span data-ttu-id="8acbe-279">Para **IBackgroundCopyManager**:</span><span class="sxs-lookup"><span data-stu-id="8acbe-279">For **IBackgroundCopyManager**:</span></span>
    
  ```cpp
  HRESULT _stdcall CreateJob(
                      [in] LPWSTR DisplayName, 
                      [in] BG_JOB_TYPE Type, 
                      [out] GUID* pJobId, 
                      [out] IBackgroundCopyJob** ppJob)
  HRESULT _stdcall GetJob(
                      [in] GUID* jobID, 
                      [out] IBackgroundCopyJob** ppJob)
  HRESULT _stdcall EnumJobs(
                      [in] unsigned long dwFlags, 
                      [out] IEnumBackgroundCopyJobs** ppenum)
  
  ```

- <span data-ttu-id="8acbe-280">Para **IBackgroundCopyJob**:</span><span class="sxs-lookup"><span data-stu-id="8acbe-280">For **IBackgroundCopyJob**:</span></span>
    
  ```cpp
  HRESULT _stdcall AddFile(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName)
  HRESULT _stdcall Resume()
  HRESULT _stdcall Complete()
  HRESULT _stdcall Cancel();
  HRESULT _stdcall GetState([out] BG_JOB_STATE* pVal);
  HRESULT GetProgress( [out] BG_JOB_PROGRESS *pProgress);
  
  ```

- <span data-ttu-id="8acbe-281">Para **IBackgroundCopyJob3**:</span><span class="sxs-lookup"><span data-stu-id="8acbe-281">For **IBackgroundCopyJob3**:</span></span>
    
  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- <span data-ttu-id="8acbe-282">Para las `Addfile` funciones `AddFileWithRanges` y, la dirección URL remota tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="8acbe-282">For the  `Addfile` and  `AddFileWithRanges` functions, the remote URL is in the following format:</span></span> 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - <span data-ttu-id="8acbe-283">cmbits está codificado de forma rígida y representa BITS personalizados.</span><span class="sxs-lookup"><span data-stu-id="8acbe-283">cmbits is hard coded, and stands for customized BITS.</span></span>
    
  -  <span data-ttu-id="8acbe-284">__ \*\*\*\* _\> contentid es el parámetro contentid del método \<_ download ().</span><span class="sxs-lookup"><span data-stu-id="8acbe-284">_\<contentid\>_ is the  _contentid_ parameter for the **Download()** method.</span></span> 
    
  -  <span data-ttu-id="8acbe-285">_ruta de acceso relativa al\> archivo de destino proporciona la ubicación y el nombre del archivo que se va a descargar. \<_</span><span class="sxs-lookup"><span data-stu-id="8acbe-285">_\<relative path to target file\>_ provides the location and file name of the file to download.</span></span> 
    
    <span data-ttu-id="8acbe-286">Por ejemplo, si ha proporcionado un _contentid_ del al `f732af58-5d86-4299-abe9-7595c35136ef` método **download ()** y Office C2R desea descargar el archivo CAB de la versión, `v32.cab` como File, llamará a **AddFile ()** con lo siguiente `RemoteUrl`:</span><span class="sxs-lookup"><span data-stu-id="8acbe-286">For example, if you have provided a  _contentid_ of  `f732af58-5d86-4299-abe9-7595c35136ef` to the **Download()** method, and Office C2R wants to download the version cab file, such as  `v32.cab` file, it will call **AddFile()** with the following  `RemoteUrl`:</span></span>
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- <span data-ttu-id="8acbe-287">Para **IBackgroundCopyError**:</span><span class="sxs-lookup"><span data-stu-id="8acbe-287">For **IBackgroundCopyError**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- <span data-ttu-id="8acbe-288">Para **IBackgroundCopyFile**:</span><span class="sxs-lookup"><span data-stu-id="8acbe-288">For **IBackgroundCopyFile**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetLocalName([out] LPWSTR *ppName); 
  HRESULT _stdcall GetRemoteName([out] LPWSTR *ppName);
  
  ```

<!--## Automating content staging

IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the Microsoft Content Delivery Network (CDN) or they can choose to control the deployment of updates available from the [update channels](https://docs.microsoft.com/DeployOffice/overview-of-update-channels-for-office-365-proplus) using the [Office 2016 Deployment Tool](https://www.microsoft.com/download/details.aspx?id=49117) or [System Center Configuration Manager](https://docs.microsoft.com/deployoffice/manage-office-365-proplus-updates-with-configuration-manager).
  
The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.
  
**Following is a diagram showing the overview of downloading a custom image**

![An overview of downloading Office updates from the CDN.](media/9afac230-6b22-4526-a800-0562708cc436.png "An overview of downloading Office updates from the CDN")
  
In the above diagram you see that a new Office 365 ProPlus image is available on the Office Content Distribution Network (CDN). Along with the Office 365 ProPlus image, an XML-formatted file list is also available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.
  
An enterprise configures their WSUS to sync the Office 365 Client Updates. These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available. The manageability software can then read the Client Update metadata to understand what version of Office the update applies to.
  
If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.
  
### Format of the XML file list

There are two file lists available in a cab file on the CDN. One lists the files for the 32-bit version of Office and one for the 64-bit version of Office. The URL of the location of the Office File List (OFL.CAB) file is [https://officecdn.microsoft.com/pr/wsus/ofl.cab](https://officecdn.microsoft.com/pr/wsus/ofl.cab). The two file lists are called:
  
- O365Client_32bit.xml
    
- O365Client_64bit.xml
    
Within the XML for each of the file lists is an  `UpdateFiles` node which contains a version attribute.  `UpdateFiles version="1.4"`.
  
This version is incremented if changes are made to the file lists.
  
There are two parameters that need to be combined with the XML to make a custom image: 
  
- Replace  _%version%_ with the build version of Office. This can be derived from the Client Update metadata  `MoreInfoURL` field, see below. 
    
- Define  _baseURL_ by using the URL value associated with the branch the image is being created for. This can be derived from the Client Update metadata, see below. 
    
The steps for creating an image are:
  
1. Open the XML file list.
    
2. Replace occurrences of  _%version%_ with the applicable Office build version. The build version can be acquired from releasehistory.xml as described later in this article. 
    
3. Read the URL attribute for the target branch.
    
4. Remove language nodes for any languages not required in the custom image.
    
   > [!NOTE]
   > Nodes with language='0' are language neutral and must be included in the image. 
  
5. Construct a local image of the CDN by iterating through the XML file list and copying the CDN files, while creating the folder structure as needed. 
    
   - If the  _rename_ attribute is provided, then rename the copied file to the value provided in the  _rename_ attribute. This used to create the top-level default v64.cab and v32.cab files. These are the renamed versions of the top-level build cab file and are used as the default installation version if the version is not specified. 
    
   - Use URL + relativePath + filename to construct the CDN location.
    
The following examples use the Monthly channel (as defined by the  `baseURL` node) and build version 16.0.4229.1004 from releasehistory.xml. 
  
```cpp
baseURL branch="Monthly" URL="https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" /
```

- The following is a language neutral file needed for all languages. The name of the file is v64_16.0.4229.1004.cab and it should be copied from https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab and renamed to …/office/data/v64.cab.
    
  ```cpp
  baseURL branch="Business" URL="https://officecdn.microsoft.com/pr/7ffbc6bf-bc32-4f92-8982-f9dd17fd3114" /
  File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/
  
  ```

- The following is a file to be included in the en-US image as designated by the language LCID=1033. The name of the file is s641033.cab and it should be copied from https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab and not renamed.
    
  ```cpp
  File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" /
  ```

### Hash verification of data files

Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed HASH value with the supplied HASH value associated with each of the .dat files. Below is an example of a .dat file from the Monthly channel with build version 16.0.4229.1004 and language set to Bulgarian.
  
```cpp
File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"
```

- The  _hashLocation_ attribute specifies the relative path location of the stream.x64.bg-bg.hash for the stream.x64.bg-bg.dat file. Construct the hash file location by concatenating URL + relativePath + hashLocation. In this example the stream.x64.bg-bg.hash location would be https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
    
- The  _hashAlgo_ attribute specifies what hashing algorithm was used. In this case the Sha256 algorithm was used. 
    
To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the hash value from the first line of text in the hash file. Compare this to the has value that you computed using the specified hashing algorithm to verify that the values match. Use the following C# code to read the hash.
  
```cs
string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
string readHash = readHashes.First();

```

### Office 365 Client Updates

Office 365 Client Updates enable manageability software to treat the Office 365 Client Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload. The Office 365 Client Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.
  
**Office 365 Client Update workflow**

![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")
  
Each Office 365 Client Update that is published includes metadata about the update. This metadata includes a parameter called  _MoreInfoUrl_ which can be used to derive the following information: 
  
-  _Ver_: Identifies the Office version associated with this update. For example 16.0.4229.1004.
    
-  _Branch_: Identifies the Update Channel for this update. Values include InsiderFast, Insiders, Monthly, Targeted, Broad. Additional values may be added in the future.
    
-  _Arch_: Identifies the processor architecture associated with this update.
    
-  _xmlVer_: Identifies the version of the XML file lists to use to construct the base image for this update.
    
-  _xmlPath_: Path to the OFL.CAB file that contains the XML file lists.
    
-  _xmlFile_: The name of the file list that should be used for this update. The value will be  `O365Client_32bit` or  `O365Client_64bit` and will match the value in  _Arch_.
    
The following is an example of the  _MoreInfoURL_ parameter which refers to the Office 365 Client Update for the 32-bit version of Office with build version of 16.0.2342.2343 on the Current channel. 
  
```http
https://officecdn.microsoft.com/pr/wsus/ofl.cab is the location of the XML file lists for this update, specifically the O365Client_32bit.xml from within the OFL.CAB.
https://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=https://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml 

```
THE ABOVE SECTION APPEARS TO BE A DUPLICATE OF THE FOLLOWING SECTION; TEMPORARILY COMMENTING IT OUT.-->

## <a name="automating-content-staging"></a><span data-ttu-id="8acbe-289">Automatizar el almacenamiento provisional del contenido</span><span class="sxs-lookup"><span data-stu-id="8acbe-289">Automating content staging</span></span>

<span data-ttu-id="8acbe-290">Los administradores de TI pueden elegir que los clientes de escritorio reciban automáticamente actualizaciones cuando están disponibles directamente desde la red de entrega de contenido (CDN) de Microsoft o pueden elegir controlar la implementación de las actualizaciones disponibles en la actualización. canales con la herramienta de implementación de Office o System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8acbe-290">IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the Microsoft Content Delivery Network (CDN) or they can choose to control the deployment of updates available from the update channels using the Office Deployment Tool or System Center Configuration Manager.</span></span>
  
<span data-ttu-id="8acbe-291">El servicio admite la capacidad de las herramientas de administración para reconocer y automatizar la descarga del contenido cuando las actualizaciones estén disponibles.</span><span class="sxs-lookup"><span data-stu-id="8acbe-291">The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.</span></span>
  
<span data-ttu-id="8acbe-292">**La siguiente imagen es una introducción a la descarga de una imagen personalizada**</span><span class="sxs-lookup"><span data-stu-id="8acbe-292">**The following image is an overview of downloading a custom image**</span></span>

<span data-ttu-id="8acbe-293">![Diagrama del uso de la interfaz COM en el programa de instalación de Hacer clic y ejecutar de Office.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Diagrama de uso de la interfaz COM en el instalador de hacer clic y ejecutar de Office")</span><span class="sxs-lookup"><span data-stu-id="8acbe-293">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
### <a name="overview-of-downloading-a-custom-image"></a><span data-ttu-id="8acbe-294">Información general sobre la descarga de una imagen personalizada</span><span class="sxs-lookup"><span data-stu-id="8acbe-294">Overview of downloading a custom image</span></span>
  
<span data-ttu-id="8acbe-295">En el diagrama anterior, verá que una imagen nueva de Office 365 ProPlus está disponible en la red de distribución de contenido (CDN) de Office.</span><span class="sxs-lookup"><span data-stu-id="8acbe-295">In the previous diagram, you see that a new Office 365 ProPlus image is available on the Office Content Distribution Network (CDN).</span></span> <span data-ttu-id="8acbe-296">Junto con la imagen de Office 365 ProPlus, también hay disponible una lista de archivos con formato XML que contiene la información necesaria para que el software de administración pueda crear imágenes personalizadas directamente, lo que reemplaza la necesidad de usar la herramienta de implementación de Office.</span><span class="sxs-lookup"><span data-stu-id="8acbe-296">Along with the Office 365 ProPlus image, an XML-formatted file list is also available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.</span></span>
  
<span data-ttu-id="8acbe-297">Una empresa configura su WSUS para que sincronice las actualizaciones de cliente de Office 365.</span><span class="sxs-lookup"><span data-stu-id="8acbe-297">An enterprise configures their WSUS to sync the Office 365 Client Updates.</span></span> <span data-ttu-id="8acbe-298">Estas actualizaciones no contienen la carga real de la imagen, pero sí permiten que el software de administración reconozca cuando hay contenido nuevo disponible.</span><span class="sxs-lookup"><span data-stu-id="8acbe-298">These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available.</span></span> <span data-ttu-id="8acbe-299">El software de administración puede leer los metadatos de actualización del cliente para comprender a qué versión de Office se aplica la actualización.</span><span class="sxs-lookup"><span data-stu-id="8acbe-299">The manageability software can then read the Client Update metadata to understand what version of Office the update applies to.</span></span>
  
<span data-ttu-id="8acbe-300">Si la actualización es aplicable, el software de administración puede usar el contenido de la red CDN y la lista de archivos para crear la imagen personalizada y almacenarla en la ubicación del recurso compartido de archivos que está configurada para usar.</span><span class="sxs-lookup"><span data-stu-id="8acbe-300">If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.</span></span>
  
### <a name="format-of-the-xml-file-list"></a><span data-ttu-id="8acbe-301">Formato de la lista de archivos XML</span><span class="sxs-lookup"><span data-stu-id="8acbe-301">Format of the XML file list</span></span>

<span data-ttu-id="8acbe-302">Hay dos listas de archivos disponibles en un archivo CAB en la red CDN.</span><span class="sxs-lookup"><span data-stu-id="8acbe-302">There are two file lists available in a cab file on the CDN.</span></span> <span data-ttu-id="8acbe-303">Uno enumera los archivos de la versión de 32 bits de Office y otro para la versión de 64 bits de Office.</span><span class="sxs-lookup"><span data-stu-id="8acbe-303">One lists the files for the 32-bit version of Office and one for the 64-bit version of Office.</span></span> <span data-ttu-id="8acbe-304">La dirección URL de la ubicación de la lista de archivos de Office (OFL. CAB) es [https://officecdn.microsoft.com/pr/wsus/ofl.cab](https://officecdn.microsoft.com/pr/wsus/ofl.cab).</span><span class="sxs-lookup"><span data-stu-id="8acbe-304">The URL of the location of the Office File List (OFL.CAB) file is [https://officecdn.microsoft.com/pr/wsus/ofl.cab](https://officecdn.microsoft.com/pr/wsus/ofl.cab).</span></span> <span data-ttu-id="8acbe-305">Se llama a las dos listas de archivos:</span><span class="sxs-lookup"><span data-stu-id="8acbe-305">The two file lists are called:</span></span>
  
- <span data-ttu-id="8acbe-306">O365Client_32bit. XML</span><span class="sxs-lookup"><span data-stu-id="8acbe-306">O365Client_32bit.xml</span></span>
    
- <span data-ttu-id="8acbe-307">O365Client_64bit. XML</span><span class="sxs-lookup"><span data-stu-id="8acbe-307">O365Client_64bit.xml</span></span>
    
<span data-ttu-id="8acbe-308">Dentro del código XML para cada una de las listas de <UpdateFiles> archivos se encuentra un nodo que contiene un atributo version.</span><span class="sxs-lookup"><span data-stu-id="8acbe-308">Within the XML for each of the file lists is an <UpdateFiles> node which contains a version attribute.</span></span>  <span data-ttu-id="8acbe-309">`<UpdateFiles version="1.4">`.</span><span class="sxs-lookup"><span data-stu-id="8acbe-309">`<UpdateFiles version="1.4">`.</span></span> <span data-ttu-id="8acbe-310">Esta versión se incrementa si se realizan cambios en las listas de archivos.</span><span class="sxs-lookup"><span data-stu-id="8acbe-310">This version is incremented if changes are made to the file lists.</span></span>
  
<span data-ttu-id="8acbe-311">Hay dos parámetros que deben combinarse con el XML para crear una imagen personalizada:</span><span class="sxs-lookup"><span data-stu-id="8acbe-311">There are two parameters that need to be combined with the XML to make a custom image:</span></span> 
  
- <span data-ttu-id="8acbe-312">Reemplace *% versión%* por la versión de compilación de Office.</span><span class="sxs-lookup"><span data-stu-id="8acbe-312">Replace  *%version%*  with the build version of Office.</span></span> <span data-ttu-id="8acbe-313">Esto puede derivarse de los metadatos de actualización de cliente (que se explican en la sección siguiente).</span><span class="sxs-lookup"><span data-stu-id="8acbe-313">This can be derived from the Client Update metadata (explained in the next section).</span></span> 
    
- <span data-ttu-id="8acbe-314">Defina *baseurl* mediante el valor de dirección URL asociado a la rama para la que se está creando la imagen.</span><span class="sxs-lookup"><span data-stu-id="8acbe-314">Define  *baseURL*  by using the URL value associated with the branch the image is being created for.</span></span> <span data-ttu-id="8acbe-315">Esto se deriva de los metadatos de actualización del cliente, que se explican en la siguiente sección.</span><span class="sxs-lookup"><span data-stu-id="8acbe-315">This is derived from the Client Update metadata, explained in the following section.</span></span> 
    
<span data-ttu-id="8acbe-316">Los pasos para crear una imagen son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="8acbe-316">The steps for creating an image are:</span></span>
  
1. <span data-ttu-id="8acbe-317">Abra la lista de archivos XML.</span><span class="sxs-lookup"><span data-stu-id="8acbe-317">Open the XML file list.</span></span>
    
2. <span data-ttu-id="8acbe-318">Reemplace las repeticiones de *% version%* por la versión de compilación de Office aplicable.</span><span class="sxs-lookup"><span data-stu-id="8acbe-318">Replace occurrences of  *%version%*  with the applicable Office build version.</span></span> <span data-ttu-id="8acbe-319">La versión de compilación puede adquirirse de releasehistory. XML, como se describe más adelante en este artículo.</span><span class="sxs-lookup"><span data-stu-id="8acbe-319">The build version can be acquired from releasehistory.xml as described later in this article.</span></span> 
    
3. <span data-ttu-id="8acbe-320">Lea el atributo de dirección URL de la rama de destino.</span><span class="sxs-lookup"><span data-stu-id="8acbe-320">Read the URL attribute for the target branch.</span></span>
    
4. <span data-ttu-id="8acbe-321">Quita los nodos de idioma de los idiomas que no se necesitan en la imagen personalizada.</span><span class="sxs-lookup"><span data-stu-id="8acbe-321">Remove language nodes for any languages not required in the custom image.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="8acbe-322">Los nodos con Language = ' 0 ' son independientes del idioma y deben incluirse en la imagen.</span><span class="sxs-lookup"><span data-stu-id="8acbe-322">Nodes with language='0' are language neutral and must be included in the image.</span></span> 
  
5. <span data-ttu-id="8acbe-323">Construya una imagen local de la red CDN iterando por la lista de archivos XML y copiando los archivos de la red CDN, a la vez que crea la estructura de carpetas según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="8acbe-323">Construct a local image of the CDN by iterating through the XML file list and copying the CDN files, while creating the folder structure as needed.</span></span> 
    
   - <span data-ttu-id="8acbe-324">Si se proporciona el atributo *Rename* , cambie el *nombre* del archivo copiado al valor proporcionado en el atributo Rename.</span><span class="sxs-lookup"><span data-stu-id="8acbe-324">If the  *rename*  attribute is provided, then  *rename*  the copied file to the value provided in the rename attribute.</span></span> <span data-ttu-id="8acbe-325">Se usa para crear los archivos V64. cab y V32. cab predeterminados de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="8acbe-325">This is used to create the top-level default v64.cab and v32.cab files.</span></span> <span data-ttu-id="8acbe-326">Estas son las versiones a las que se ha cambiado el nombre del archivo CAB de compilación de nivel superior y se usan como la versión de instalación predeterminada si no se especifica la versión.</span><span class="sxs-lookup"><span data-stu-id="8acbe-326">These are the renamed versions of the top-level build cab file and are used as the default installation version if the version is not specified.</span></span> 
    
   - <span data-ttu-id="8acbe-327">Use URL + relativePath + FILENAME para construir la ubicación de la red CDN.</span><span class="sxs-lookup"><span data-stu-id="8acbe-327">Use URL + relativePath + filename to construct the CDN location.</span></span>
    
<span data-ttu-id="8acbe-328">Los siguientes son ejemplos que usan el canal mensual (definido por el `<baseURL>` nodo) y la versión de compilación 16.0.4229.1004 desde releasehistory. Xml.</span><span class="sxs-lookup"><span data-stu-id="8acbe-328">The following are examples that use the Monthly channel (as defined by the  `<baseURL>` node) and build version 16.0.4229.1004 from releasehistory.xml.</span></span> 
  
```xml
<baseURL branch="Monthly" URL="https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" />
```

- <span data-ttu-id="8acbe-329">A continuación se encuentra un archivo independiente del idioma necesario para todos los idiomas.</span><span class="sxs-lookup"><span data-stu-id="8acbe-329">The following is a language neutral file needed for all languages.</span></span> <span data-ttu-id="8acbe-330">El nombre del archivo es v64_16.0.4229.1004. cab y debe copiarse `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab` y cambiar su nombre a. `…/office/data/v64.cab`</span><span class="sxs-lookup"><span data-stu-id="8acbe-330">The name of the file is v64_16.0.4229.1004.cab and it should be copied from `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab` and renamed to `…/office/data/v64.cab`.</span></span> 
    
  ```xml
  <File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/>
  
  ```

- <span data-ttu-id="8acbe-331">A continuación se incluye un archivo que se incluirá en la imagen en-US, tal como lo designe el LCID del idioma = 1033.</span><span class="sxs-lookup"><span data-stu-id="8acbe-331">The following is a file to be included in the en-US image as designated by the language LCID=1033.</span></span> <span data-ttu-id="8acbe-332">El nombre del archivo es s641033. cab y debe copiarse y no cambiarse de `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab` nombre.</span><span class="sxs-lookup"><span data-stu-id="8acbe-332">The name of the file is s641033.cab and it should be copied from `https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab` and not renamed.</span></span>
    
  ```xml
  <File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" />
  ```

### <a name="hash-verification-of-dat-files"></a><span data-ttu-id="8acbe-333">Comprobación de hash de los archivos. dat</span><span class="sxs-lookup"><span data-stu-id="8acbe-333">Hash verification of .dat files</span></span>

<span data-ttu-id="8acbe-334">Las herramientas de creación de imágenes pueden comprobar la integridad de los archivos. dat descargados mediante la comparación de un valor HASH calculado con el valor HASH proporcionado asociado con cada uno de los archivos. dat.</span><span class="sxs-lookup"><span data-stu-id="8acbe-334">Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed HASH value with the supplied HASH value associated with each of the .dat files.</span></span> <span data-ttu-id="8acbe-335">A continuación se proporciona un ejemplo de un archivo. dat desde el canal mensual con la versión de compilación 16.0.4229.1004 y el idioma configurado en búlgaro:</span><span class="sxs-lookup"><span data-stu-id="8acbe-335">Following is an example of a .dat file from the Monthly channel with build version 16.0.4229.1004 and language set to Bulgarian:</span></span>
  
```xml
<File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"/>
```

- <span data-ttu-id="8acbe-336">El atributo **hashLocation** especifica la ubicación de la ruta de acceso relativa del Stream.x64.BG-BG. hash para el archivo Stream.x64.BG-BG. dat.</span><span class="sxs-lookup"><span data-stu-id="8acbe-336">The **hashLocation** attribute specifies the relative path location of the stream.x64.bg-bg.hash for the stream.x64.bg-bg.dat file.</span></span> <span data-ttu-id="8acbe-337">Construya la ubicación del archivo hash concatenando la dirección URL + relativePath + hashLocation.</span><span class="sxs-lookup"><span data-stu-id="8acbe-337">Construct the hash file location by concatenating URL + relativePath + hashLocation.</span></span> <span data-ttu-id="8acbe-338">En el siguiente ejemplo, la ubicación de stream.x64.bg-BG. hash sería:</span><span class="sxs-lookup"><span data-stu-id="8acbe-338">In the following example, the stream.x64.bg-bg.hash location would be:</span></span> 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- <span data-ttu-id="8acbe-339">El atributo **hashAlgo** especifica el algoritmo hash que se usó.</span><span class="sxs-lookup"><span data-stu-id="8acbe-339">The **hashAlgo** attribute specifies what hashing algorithm was used.</span></span> <span data-ttu-id="8acbe-340">En este caso, se utilizó Sha256.</span><span class="sxs-lookup"><span data-stu-id="8acbe-340">In this case Sha256 was used.</span></span> 
    
  <span data-ttu-id="8acbe-341">Para validar la integridad del archivo stream.x64.bg-BG. dat, abra el stream.x64.bg-BG. hash y lea el valor de HASH, que es la primera línea de texto del archivo hash.</span><span class="sxs-lookup"><span data-stu-id="8acbe-341">To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the HASH value which is the first line of text in the hash file.</span></span> <span data-ttu-id="8acbe-342">Compare esto con el valor hash calculado (con el algoritmo hash especificado) para comprobar la integridad del archivo. dat descargado.</span><span class="sxs-lookup"><span data-stu-id="8acbe-342">Compare this to the computed hash value (using the specified hashing algorithm) to verify the integrity of the downloaded .dat file.</span></span>
    
  <span data-ttu-id="8acbe-343">En el ejemplo siguiente se muestra el código de C# para leer el hash.</span><span class="sxs-lookup"><span data-stu-id="8acbe-343">The following example shows the C# code to read the hash.</span></span>
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="office-365-client-updates"></a><span data-ttu-id="8acbe-344">Actualizaciones de cliente de Office 365</span><span class="sxs-lookup"><span data-stu-id="8acbe-344">Office 365 Client Updates</span></span>

<span data-ttu-id="8acbe-345">Todas las actualizaciones de cliente de Office 365 se publican en el [Catálogo de Microsoft Update](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span><span class="sxs-lookup"><span data-stu-id="8acbe-345">All Office 365 Client Updates are published to the [Microsoft Update Catalog](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span></span>
  
<span data-ttu-id="8acbe-346">Las actualizaciones de cliente de Office 365 permiten que el software de administración trate las actualizaciones de cliente de Office 365 de forma muy similar a cualquier otra actualización de WU con una excepción; las actualizaciones de cliente no contienen una carga real.</span><span class="sxs-lookup"><span data-stu-id="8acbe-346">Office 365 Client Updates enable manageability software to treat the Office 365 Client Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload.</span></span> <span data-ttu-id="8acbe-347">Las actualizaciones de cliente de Office 365 no deben instalarse en ningún cliente, sino que se usan para desencadenar flujos de trabajo con el software de administración que reemplaza el comando de instalación por el mecanismo de instalación basado en COM mostrado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="8acbe-347">The Office 365 Client Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.</span></span> 
  
<span data-ttu-id="8acbe-348">**En la siguiente figura se muestra un diagrama del flujo de trabajo de actualización de cliente de Office 365.**</span><span class="sxs-lookup"><span data-stu-id="8acbe-348">**The following figure shows a diagram of the Office 365 Client Update workflow.**</span></span>

<span data-ttu-id="8acbe-349">![Diagrama de flujo de trabajo para las actualizaciones de cliente de O365PP.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Diagrama de flujo de trabajo para actualizaciones de cliente de O365PP")</span><span class="sxs-lookup"><span data-stu-id="8acbe-349">![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")</span></span>
  
<span data-ttu-id="8acbe-350">Cada actualización de cliente de Office 365 que está publicada incluye metadatos sobre la actualización.</span><span class="sxs-lookup"><span data-stu-id="8acbe-350">Each Office 365 Client Update that is published includes metadata about the update.</span></span> <span data-ttu-id="8acbe-351">Estos metadatos incluyen un parámetro denominado *MoreInfoUrl* que se puede usar para derivar la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="8acbe-351">This metadata includes a parameter called  *MoreInfoUrl*  which can be used to derive the following information:</span></span> 
  
-  <span data-ttu-id="8acbe-352">*Ver*: identifica la versión de Office asociada a esta actualización.</span><span class="sxs-lookup"><span data-stu-id="8acbe-352">*Ver*: Identifies the Office version associated with this update.</span></span> 
    
-  <span data-ttu-id="8acbe-353">*Branch*: identifica el canal de actualización para esta actualización.</span><span class="sxs-lookup"><span data-stu-id="8acbe-353">*Branch*: Identifies the Update Channel for this update.</span></span> <span data-ttu-id="8acbe-354">Los valores incluyen InsiderFast, Insider, mensual, dirigido, general.</span><span class="sxs-lookup"><span data-stu-id="8acbe-354">Values include InsiderFast, Insiders, Monthly, Targeted, Broad.</span></span> <span data-ttu-id="8acbe-355">Es posible que se agreguen valores adicionales en el futuro.</span><span class="sxs-lookup"><span data-stu-id="8acbe-355">Additional values may be added in the future.</span></span> 
    
-  <span data-ttu-id="8acbe-356">*Arch*: identifica la arquitectura del procesador asociada con esta actualización.</span><span class="sxs-lookup"><span data-stu-id="8acbe-356">*Arch*: Identifies the processor architecture associated with this update.</span></span> 
    
-  <span data-ttu-id="8acbe-357">*xmlVer*: la versión de las listas de archivos XML que se deben usar para construir la imagen base para esta actualización.</span><span class="sxs-lookup"><span data-stu-id="8acbe-357">*xmlVer*: The version of the XML file lists that should be used to construct the base image for this update.</span></span> 
    
-  <span data-ttu-id="8acbe-358">*xmlPath*: ruta de acceso al OFL. Archivo CAB que contiene las listas de archivos XML.</span><span class="sxs-lookup"><span data-stu-id="8acbe-358">*xmlPath*: Path to the OFL.CAB file which contains the XML file lists.</span></span> 
    
-  <span data-ttu-id="8acbe-359">*mlFile*: nombre de la lista de archivos que se debe usar para esta actualización.</span><span class="sxs-lookup"><span data-stu-id="8acbe-359">*mlFile*: The name of the file list that should be used for this update.</span></span> <span data-ttu-id="8acbe-360">El valor será O365Client_32bit o O365Client_64bit, y coincidirá con el arco.</span><span class="sxs-lookup"><span data-stu-id="8acbe-360">The value will be O365Client_32bit or O365Client_64bit and will match the Arch.</span></span> 
    
<span data-ttu-id="8acbe-361">La siguiente dirección URL es un ejemplo del parámetro *MoreInfoURL* que hace referencia a las versiones de actualización de cliente de Office 365 para la versión de 32 bits de Office con la versión de compilación de 16.0.2342.2343 en el canal actual.</span><span class="sxs-lookup"><span data-stu-id="8acbe-361">The following URL is an example of the  *MoreInfoURL*  parameter which refers to the Office 365 client update releases for the 32-bit version of Office with build version of 16.0.2342.2343 on the Current channel.</span></span> 
  
<span data-ttu-id="8acbe-362">https://officecdn.microsoft.com/pr/wsus/ofl.cabes la ubicación de las listas de archivos XML para esta actualización, concretamente la O365Client_32bit. XML desde dentro del OFL. Gabinete.</span><span class="sxs-lookup"><span data-stu-id="8acbe-362">https://officecdn.microsoft.com/pr/wsus/ofl.cab is the location of the XML file lists for this update, specifically the O365Client_32bit.xml from within the OFL.CAB.</span></span>
  
[<span data-ttu-id="8acbe-363">Versiones de canal de actualización de cliente de Office 365</span><span class="sxs-lookup"><span data-stu-id="8acbe-363">Office 365 client update channel releases</span></span>](https://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=https://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml)
  
### <a name="additional-metadata-for-automating-content-staging"></a><span data-ttu-id="8acbe-364">Metadatos adicionales para automatizar el contenido provisional</span><span class="sxs-lookup"><span data-stu-id="8acbe-364">Additional metadata for automating content staging</span></span>

<span data-ttu-id="8acbe-365">Además de los metadatos publicados que definen, hay también archivos XML adicionales publicados en la red CDN que pueden ayudar a proporcionar información adicional sobre los clientes de Office 365 que están disponibles en la red CDN de Office.</span><span class="sxs-lookup"><span data-stu-id="8acbe-365">In addition to the metadata that is published which defines there are also additional XML files published to the CDN that can help provide additional information about the Office 365 clients that are available from the Office CDN.</span></span>
  
<span data-ttu-id="8acbe-366">**SKU. XML**</span><span class="sxs-lookup"><span data-stu-id="8acbe-366">**SKUS.XML**</span></span>
  
<span data-ttu-id="8acbe-367">Este archivo XML está contenido en un archivo CAB firmado y se publica en la red CDN de Office en [https://officecdn.microsoft.com/pr/wsus/skus.cab](https://officecdn.microsoft.com/pr/wsus/skus.cab)la siguiente dirección URL:.</span><span class="sxs-lookup"><span data-stu-id="8acbe-367">This XML file is contained within a signed CAB and published to the Office CDN at the following URL: [https://officecdn.microsoft.com/pr/wsus/skus.cab](https://officecdn.microsoft.com/pr/wsus/skus.cab).</span></span>
  
<span data-ttu-id="8acbe-368">Los metadatos publicados en este archivo XML son útiles para determinar qué productos están disponibles para la implementación y el servicio desde la red CDN de Office junto con varias opciones para cada uno.</span><span class="sxs-lookup"><span data-stu-id="8acbe-368">The metadata published in this XML file is useful for determining which products are available for deployment and servicing from the Office CDN along with various options for each.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<ReleaseInfo PublishedDate="08/07/2017 16:34">
  <!-- Suite / App catalog -->
  <Suite>
    <SKU Name="Office 365 ProPlus" ProductID="O365ProPlusRetail" Default="True">
      <Apps>
        <App Name="Access" AppID="Access" />
        <App Name="Excel" AppID="Excel" />
        <App Name="OneDrive for Business (Groove)" AppID="Groove" />
        <App Name="OneDrive for Business (Next Gen Sync Client)" AppID="OneDrive" />
        <App Name="OneNote" AppID="OneNote" />
        <App Name="Outlook" AppID="Outlook" />
        <App Name="PowerPoint" AppID="PowerPoint" />
        <App Name="Publisher" AppID="Publisher" />
        <App Name="Skype for Business" AppID="Lync" />
        <App Name="Word" AppID="Word" />
      </Apps>
      <Channels>
        <Channel ID="Monthly"/>
        <Channel ID="Insiders"/>
        <Channel ID="Targeted"/>
        <Channel ID="Broad"/>
      </Channels>
    </SKU>
```

<span data-ttu-id="8acbe-369">ReleaseInfo nodo raíz contiene el atributo PublishedDate que identifica la fecha en que se publicó este archivo. \*\* \<\> \*\*</span><span class="sxs-lookup"><span data-stu-id="8acbe-369">**\<ReleaseInfo\>** root node contains the PublishedDate attribute which identifies the date which this file was published.</span></span> 
  
<span data-ttu-id="8acbe-370">El nodo **SKU\> identifica una SKU individual. \<**</span><span class="sxs-lookup"><span data-stu-id="8acbe-370">**\<SKU\>** node identifies an individual SKU.</span></span> 
  
- <span data-ttu-id="8acbe-371">El atributo *ProductID* identifica el identificador que se pasa como el atributo ID en Configuration. xml si se usa la ODT.</span><span class="sxs-lookup"><span data-stu-id="8acbe-371">The  *ProductID*  attribute identifies the ID that is passed as the ID attribute in the configuration.xml if using the ODT.</span></span> <span data-ttu-id="8acbe-372">Por ejemplo, `<Product ID="O365ProPlusRetail">`.</span><span class="sxs-lookup"><span data-stu-id="8acbe-372">For example, `<Product ID="O365ProPlusRetail">`.</span></span> 
    
- <span data-ttu-id="8acbe-373">El atributo *default* , si se establece en true, identifica el SKU recomendado.</span><span class="sxs-lookup"><span data-stu-id="8acbe-373">The  *Default*  attribute, if set to True, identifies the recommended SKU.</span></span> 
    
<span data-ttu-id="8acbe-374">Los nodos de la **aplicación\> se usan para definir las aplicaciones de Office individuales que admite cada SKU. \<**</span><span class="sxs-lookup"><span data-stu-id="8acbe-374">**\<App\>** nodes are used to define the individual Office apps that each SKU supports.</span></span> 
  
- <span data-ttu-id="8acbe-375">El atributo *Name* es el nombre de la aplicación que se muestra.</span><span class="sxs-lookup"><span data-stu-id="8acbe-375">The  *Name*  attribute is the displayed application name.</span></span> 
    
- <span data-ttu-id="8acbe-376">El atributo *AppID* es el atributo ID que se pasa en Configuration. XML para \*\* \<el\> nodo ExcludeApp\*\* si se usa la ODT.</span><span class="sxs-lookup"><span data-stu-id="8acbe-376">The  *AppID*  attribute is the ID attribute passed in the configuration.xml for the **\<ExcludeApp\>** node if using the ODT.</span></span> <span data-ttu-id="8acbe-377">Por ejemplo, `<ExcludeApp ID="Publisher" />`.</span><span class="sxs-lookup"><span data-stu-id="8acbe-377">For example, `<ExcludeApp ID="Publisher" />`.</span></span> 
    
<span data-ttu-id="8acbe-378">**RELEASEHISTORY. XML**</span><span class="sxs-lookup"><span data-stu-id="8acbe-378">**RELEASEHISTORY.XML**</span></span>
  
<span data-ttu-id="8acbe-379">Este archivo XML está contenido en un archivo CAB firmado y se publica en la red CDN de Office en [https://officecdn.microsoft.com/pr/wsus/releasehistory.cab](https://officecdn.microsoft.com/pr/wsus/releasehistory.cab)la siguiente ubicación:.</span><span class="sxs-lookup"><span data-stu-id="8acbe-379">This XML file is contained within a signed CAB and published to the Office CDN at the following location: [https://officecdn.microsoft.com/pr/wsus/releasehistory.cab](https://officecdn.microsoft.com/pr/wsus/releasehistory.cab).</span></span> 
  
<span data-ttu-id="8acbe-380">Los metadatos publicados en este archivo XML son útiles para determinar qué canales se admiten para el servicio de actualizaciones desde la red CDN de Office junto con información sobre el historial de la compilación para cada uno de los canales admitidos.</span><span class="sxs-lookup"><span data-stu-id="8acbe-380">The metadata published in this XML file is useful for determining which channels are supported for servicing updates from the Office CDN along with information about the build history for each of the supported channels.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<ReleaseHistory PublishedDate="10/22/2017 00:48">
  <UpdateChannel Name="Current" ID="Monthly" DisplayName="Monthly Channel">
    <Update Latest="True" Version="1709" LegacyVersion="16.0.8528.2139" Build="8528.2139" PubTime="2017-10-16T19:45:50.743Z" />
    <Update Latest="False" Version="1708" LegacyVersion="16.0.8431.2107" Build="8431.2107" PubTime="2017-10-11T01:52:33.793Z" />
    <Update Latest="False" Version="1708" LegacyVersion="16.0.8431.2079" Build="8431.2079" PubTime="2017-09-18T22:26:13.673Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2107" Build="8326.2107" PubTime="2017-09-12T18:56:53.657Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2096" Build="8326.2096" PubTime="2017-08-30T00:10:25.253Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2076" Build="8326.2076" PubTime="2017-08-19T00:13:01.787Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2073" Build="8326.2073" PubTime="2017-08-11T19:35:42.173Z" />
  </UpdateChannel>
```

<span data-ttu-id="8acbe-381">El nodo raíz \*\* \<ReleaseHistory\> \*\* contiene el atributo PublishedDate, que identifica la fecha en que se publicó el archivo.</span><span class="sxs-lookup"><span data-stu-id="8acbe-381">The **\<ReleaseHistory\>** root node contains the PublishedDate attribute which identifies the date which this file was published.</span></span> 
  
<span data-ttu-id="8acbe-382">El \*\* \<nodo\> UpdateChannel\*\* define un canal admitido.</span><span class="sxs-lookup"><span data-stu-id="8acbe-382">The **\<UpdateChannel\>** node defines a supported channel.</span></span> 
  
- <span data-ttu-id="8acbe-383">El atributo *Name* define el identificador de canal que se usa para pasar a la ODT en Configuration. XML como el atributo de canal.</span><span class="sxs-lookup"><span data-stu-id="8acbe-383">The  *Name*  attribute defines the channel ID which is used to pass to the ODT in the configuration.xml as the Channel attribute.</span></span> 
    
  <span data-ttu-id="8acbe-384">Ejemplo: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Current">`</span><span class="sxs-lookup"><span data-stu-id="8acbe-384">Example: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Current">`</span></span> 
    
  > [!NOTE] 
  > <span data-ttu-id="8acbe-385">Este atributo se ha dejado de usar y solo se usa para compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="8acbe-385">This attribute has been deprecated and is used for backward compatibility only.</span></span> <span data-ttu-id="8acbe-386">Use el atributo ID en vez del atributo name.</span><span class="sxs-lookup"><span data-stu-id="8acbe-386">Use the ID attribute in place of the Name attribute.</span></span> 
    
- <span data-ttu-id="8acbe-387">El atributo *ID* define el identificador de canal que se usa para pasar a la ODT en Configuration. XML como el atributo de canal.</span><span class="sxs-lookup"><span data-stu-id="8acbe-387">The  *ID*  attribute defines the channel ID which is used to pass to the ODT in the configuration.xml as the Channel attribute.</span></span> 
    
  <span data-ttu-id="8acbe-388">Ejemplo: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Deferred">`</span><span class="sxs-lookup"><span data-stu-id="8acbe-388">Example: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Deferred">`</span></span> 
    
- <span data-ttu-id="8acbe-389">El atributo **displayName** se usa como el nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="8acbe-389">The **DisplayName**  attribute is used as the display name.</span></span> 
    
<span data-ttu-id="8acbe-390">El \*\* \<nodo\> actualizar\*\* se usa para definir cada actualización que se ha publicado para ese canal en particular.</span><span class="sxs-lookup"><span data-stu-id="8acbe-390">The **\<Update\>** node is used to define each update that has been published for that particular channel.</span></span> 
  
- <span data-ttu-id="8acbe-391">El atributo **último** , si se establece en true, define la versión más reciente de ese canal.</span><span class="sxs-lookup"><span data-stu-id="8acbe-391">The **Latest**  attribute, if set to True, defines the release that is the latest release for that channel.</span></span> 
    
- <span data-ttu-id="8acbe-392">El atributo **version** define el número de versión para esta actualización en particular.</span><span class="sxs-lookup"><span data-stu-id="8acbe-392">The **Version** attribute defines the version number for this particular update.</span></span> 
    
- <span data-ttu-id="8acbe-393">El atributo **LegacyVersion** define el número de versión completo de esta actualización en particular.</span><span class="sxs-lookup"><span data-stu-id="8acbe-393">The **LegacyVersion** attribute defines the full version number for this particular update.</span></span> 
    
- <span data-ttu-id="8acbe-394">El atributo **Build** define el número de compilación de esta actualización en particular.</span><span class="sxs-lookup"><span data-stu-id="8acbe-394">The **Build** attribute defines the build number for this particular update.</span></span> 
    
- <span data-ttu-id="8acbe-395">El atributo **PubTime** define la fecha y la hora en la que se publicó la actualización en la red CDN de Office.</span><span class="sxs-lookup"><span data-stu-id="8acbe-395">The **PubTime** attribute defines the date and time at which this update was published to the Office CDN.</span></span> 
    

