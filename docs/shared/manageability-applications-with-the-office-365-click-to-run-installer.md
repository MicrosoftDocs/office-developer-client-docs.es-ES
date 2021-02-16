---
title: Integración de aplicaciones de administración con el instalador de Hacer clic y ejecutar de Aplicaciones de Microsoft 365
manager: lindalu
ms.date: 09/28/2020
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Obtenga información sobre cómo integrar el instalador de Hacer clic y ejecutar de Aplicaciones de Microsoft 365 con una solución de administración de software.
ms.openlocfilehash: eccd634f7906acf25b521ed2deb456ca914f37da
ms.sourcegitcommit: c8c51bd3f51c0a59fe44c014c8e56f1ba7c7aa03
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "48297317"
---
# <a name="integrating-manageability-applications-with-microsoft-365-apps-click-to-run-installer"></a><span data-ttu-id="52a47-103">Integración de aplicaciones de administración con el instalador de Hacer clic y ejecutar de Aplicaciones de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="52a47-103">Integrating manageability applications with Microsoft 365 Apps Click-to-Run installer</span></span>

<span data-ttu-id="52a47-104">Obtenga información sobre cómo integrar el instalador de Hacer clic y ejecutar de Aplicaciones de Microsoft 365 con una solución de administración de software.</span><span class="sxs-lookup"><span data-stu-id="52a47-104">Learn how to integrate the Microsoft 365 Apps Click-to-Run installer with a software management solution.</span></span>
  
<span data-ttu-id="52a47-105">El instalador hacer clic y ejecutar de aplicaciones de Microsoft 365 proporciona una interfaz COM que permite a los profesionales de IT y a las soluciones de administración de software controlar mediante programación la administración de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="52a47-105">The Microsoft 365 Apps Click-to-Run installer provides a COM interface that allows IT Professionals and software management solutions programmatic control over update management.</span></span> <span data-ttu-id="52a47-106">Esta interfaz proporciona capacidades de administración adicionales más allá de lo que proporciona la Herramienta de implementación de Office.</span><span class="sxs-lookup"><span data-stu-id="52a47-106">This interface provides additional management capabilities beyond what is provided by the Office Deployment Tool.</span></span>
  
> [!NOTE]
> <span data-ttu-id="52a47-107">Este artículo se aplica a las aplicaciones de Office que usan el instalador Hacer clic y ejecutar.</span><span class="sxs-lookup"><span data-stu-id="52a47-107">This article applies to Office apps that use the Click-to-Run installer.</span></span> 
  
## <a name="integrating-with-the-click-to-run"></a><span data-ttu-id="52a47-108">Integración con Hacer clic y ejecutar</span><span class="sxs-lookup"><span data-stu-id="52a47-108">Integrating with the Click-to-Run</span></span>

<span data-ttu-id="52a47-109">Para usar esta interfaz, una aplicación de facilidad de uso invoca la interfaz COM y llama a las API expuestas que se comunican directamente con el servicio de instalación de Hacer clic y ejecutar.</span><span class="sxs-lookup"><span data-stu-id="52a47-109">To use this interface, a manageability application invokes the COM interface and calls exposed APIs that communicate directly with the Click-to-Run installation service.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="52a47-110">El instalador de Hacer clic y ejecutar de Office se puede ejecutar desde la línea de comandos con parámetros que puedan controlar el comportamiento, como se documenta en la Herramienta de implementación de Office para Hacer clic [y ejecutar.](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool)</span><span class="sxs-lookup"><span data-stu-id="52a47-110">The Office Click-to-Run installer can be run from the command-line with parameters that can control the behavior, as documented in [Office Deployment Tool for Click-to-Run](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool).</span></span> 
  
<span data-ttu-id="52a47-111">**A continuación se muestra un diagrama conceptual de la interfaz COM**</span><span class="sxs-lookup"><span data-stu-id="52a47-111">**Following is a conceptual diagram of the COM interface**</span></span>

<span data-ttu-id="52a47-112">![Diagrama del uso de la interfaz COM en el programa de instalación de Hacer clic y ejecutar de Office.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Diagrama de uso de la interfaz COM en el instalador de Hacer clic y ejecutar de Office")</span><span class="sxs-lookup"><span data-stu-id="52a47-112">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on  the Office Click-To-Run installer")</span></span>
  
<span data-ttu-id="52a47-113">El instalador de Hacer clic y ejecutar de Aplicaciones de Microsoft 365 implementa una interfaz basada en COM, **IUpdateNotify** registrada en CLSID **CLSID_UpdateNotifyObject**.</span><span class="sxs-lookup"><span data-stu-id="52a47-113">The Microsoft 365 Apps Click-to-Run installer implements a COM-based interface, **IUpdateNotify** registered to CLSID **CLSID_UpdateNotifyObject**.</span></span>
  
<span data-ttu-id="52a47-114">Esta interfaz se puede invocar de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="52a47-114">This interface can be invoked as follows:</span></span>
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

<span data-ttu-id="52a47-115">La llamada solo se realizará correctamente si el autor de la llamada se ejecuta con privilegios elevados, ya que el programa de instalación Hacer clic y ejecutar debe ejecutarse con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="52a47-115">The call will only succeed if the caller is running under elevated privileges, as the Click-to-Run installation program must be run with elevated privileges.</span></span>
  
<span data-ttu-id="52a47-116">La interfaz COM **IUpdateNotify** expone tres funciones asincrónicas responsables de validar los comandos y parámetros, así como de programar la ejecución con el servicio de instalación hacer clic y ejecutar.</span><span class="sxs-lookup"><span data-stu-id="52a47-116">The **IUpdateNotify** COM interface exposes three asynchronous functions responsible for validating the commands and parameters and scheduling execution with the Click-to-Run installation service.</span></span> 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

<span data-ttu-id="52a47-117">Un método forth, **Status**, puede usarse para obtener información sobre el estado del último comando ejecutado o el estado del comando que se está ejecutando actualmente (es decir, correcto, error, códigos de error detallados).</span><span class="sxs-lookup"><span data-stu-id="52a47-117">A forth method, **Status**, can be used to get information about the status of the last executed command or the status of the currently executing command (i.e. success, failure, detailed error codes).</span></span>
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

<span data-ttu-id="52a47-118">Hay cuatro estados en los que el servicio de instalación hacer clic y ejecutar puede estar durante su ciclo de vida, durante el cual se puede llamar a los métodos **IUpdateNotify;** Reinicio, inactividad, descarga y aplicación.</span><span class="sxs-lookup"><span data-stu-id="52a47-118">There are four states that the Click-to-Run installation service may be in during its lifecycle, during which **IUpdateNotify** methods may be called; Rebooting, Idle, Downloading and Applying.</span></span> 
  
<span data-ttu-id="52a47-119">**A continuación se muestra el diagrama máquina de estado de interfaz COM**</span><span class="sxs-lookup"><span data-stu-id="52a47-119">**Following is the COM Interface State Machine diagram**</span></span>

<span data-ttu-id="52a47-120">![Un diagrama de estado de la interfaz COM.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Un diagrama de estado para la interfaz COM")</span><span class="sxs-lookup"><span data-stu-id="52a47-120">![A state diagram for the COM interface.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "A state diagram for the COM interface")</span></span>
  
> [!NOTE]
> <span data-ttu-id="52a47-121">**Reinicio:** cuando la máquina arranca, hay un período de tiempo en el que el servicio del instalador de Hacer clic y ejecutar no está disponible.</span><span class="sxs-lookup"><span data-stu-id="52a47-121">**Rebooting**: When the machine is booting there is a period of time when the Click-to-Run installer service is not available.</span></span> <span data-ttu-id="52a47-122">Una llamada correcta al método Status después de un reinicio devolverá eUPDATE_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="52a47-122">A successful call to the Status method after a reboot will return eUPDATE_UNKNOWN.</span></span> 
  
<span data-ttu-id="52a47-123">**Inactivo:** Cuando el instalador de Hacer clic y ejecutar está en estado inactivo, puede llamar a:</span><span class="sxs-lookup"><span data-stu-id="52a47-123">**Idle:** When the Click-to-Run installer is in the idle state, you can call:</span></span> 
  
- <span data-ttu-id="52a47-124">**Aplicar:** instalar el contenido descargado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="52a47-124">**Apply**: Install previously downloaded content.</span></span>
    
- <span data-ttu-id="52a47-125">**Cancel**: Devuelve , "Se llamó a un método  `0x800000e` en un momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="52a47-125">**Cancel**: Returns  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="52a47-126">**Descargar:** descarga contenido nuevo en el cliente para su instalación posterior.</span><span class="sxs-lookup"><span data-stu-id="52a47-126">**Download**: Downloads new content to the client for later installation.</span></span>
    
- <span data-ttu-id="52a47-127">**Estado:** devuelve el resultado de la última acción completada o un mensaje de error si la acción finalizó en error.</span><span class="sxs-lookup"><span data-stu-id="52a47-127">**Status**: Returns the result of the last completed action, or an error message if the action ended in failure.</span></span> <span data-ttu-id="52a47-128">Si no hay ninguna acción anterior, **El estado** devuelve  `eUPDATE_UNKNOWN` .</span><span class="sxs-lookup"><span data-stu-id="52a47-128">If there is no previous action, **Status** returns  `eUPDATE_UNKNOWN`.</span></span>
    
<span data-ttu-id="52a47-129">**Descarga:** Cuando el instalador de Hacer clic y ejecutar está en el estado de descarga, puede llamar a:</span><span class="sxs-lookup"><span data-stu-id="52a47-129">**Downloading:** When the Click-to-Run installer is in the downloading state, you can call:</span></span> 
  
- <span data-ttu-id="52a47-130">**Apply**: devuelve un **valor HRESULT** con el valor "Se llamó a un método  `0x800000e` en un momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="52a47-130">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="52a47-131">**Cancelar:** detiene la descarga y quita el contenido descargado parcialmente.</span><span class="sxs-lookup"><span data-stu-id="52a47-131">**Cancel**: Stops the download and removes the partially downloaded content.</span></span>
    
- <span data-ttu-id="52a47-132">**Download**: Devuelve un **valor HRESULT** con el valor "Se llamó a un método  `0x800000e` en un momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="52a47-132">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="52a47-133">**Estado:** devuelve **DOWNLOAD_WIP** para indicar que el trabajo de descarga está en curso.</span><span class="sxs-lookup"><span data-stu-id="52a47-133">**Status**: Returns **DOWNLOAD_WIP** to indicate that download work is in progress.</span></span> 
    
<span data-ttu-id="52a47-134">**Aplicar:** Cuando el instalador de Hacer clic y ejecutar está en proceso de instalar contenido descargado previamente:</span><span class="sxs-lookup"><span data-stu-id="52a47-134">**Applying:** When the Click-to-Run installer is in the process of installing previously download content:</span></span> 
  
- <span data-ttu-id="52a47-135">**Apply**: devuelve un **valor HRESULT** con el valor "Se llamó a un método  `0x800000e` en un momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="52a47-135">**Apply**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span>
    
- <span data-ttu-id="52a47-136">**Cancel**: Devuelve  `0x800000e` , la acción Aplicar no se puede cancelar.</span><span class="sxs-lookup"><span data-stu-id="52a47-136">**Cancel**: Returns  `0x800000e`, the Apply action cannot be canceled.</span></span>
    
- <span data-ttu-id="52a47-137">**Download**: Devuelve un **valor HRESULT** con el valor "Se llamó a un método  `0x800000e` en un momento inesperado".</span><span class="sxs-lookup"><span data-stu-id="52a47-137">**Download**: Returns an **HRESULT** with the value  `0x800000e`, "A method was called at an unexpected time."</span></span> 
    
- <span data-ttu-id="52a47-138">**Estado:** devuelve **APPLY_WIP** para indicar que el trabajo de aplicación está en curso.</span><span class="sxs-lookup"><span data-stu-id="52a47-138">**Status**: Returns **APPLY_WIP** to indicate that apply work is in progress.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="52a47-139">Dado que OfficeC2RCOM es un servicio COM+ y se carga dinámicamente, debe llamar a **CoCreateInstance** cada vez que llame a un método en esta clase para asegurarse de que obtiene el resultado esperado.</span><span class="sxs-lookup"><span data-stu-id="52a47-139">Since OfficeC2RCOM is a COM+ service and is dynamically loaded, you need to call **CoCreateInstance** every time you call a method on this class to ensure that you get the expected result.</span></span> <span data-ttu-id="52a47-140">El servicio COM+ controlará la creación de una nueva instancia si es necesario.</span><span class="sxs-lookup"><span data-stu-id="52a47-140">The COM+ service will handle creating a new instance if necessary.</span></span> <span data-ttu-id="52a47-141">Cuando se llama a uno de los métodos por primera vez, COM+ cargará el objeto **IUpdateNotify** y lo ejecutará dentro de una de las dllhost.exe predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="52a47-141">When one of the methods is called for the first time, COM+ will load the **IUpdateNotify** object and run it within one of the dllhost.exe instances.</span></span> <span data-ttu-id="52a47-142">El nuevo objeto permanecerá activo durante unos 3 minutos en modo inactivo.</span><span class="sxs-lookup"><span data-stu-id="52a47-142">The new object will stay active for about 3 minutes in idle.</span></span> <span data-ttu-id="52a47-143">Si se realiza una llamada posterior en los tres minutos siguientes a la última llamada, el objeto **IUpdateNotify** permanecerá cargado y no se creará una nueva instancia.</span><span class="sxs-lookup"><span data-stu-id="52a47-143">If a subsequent call is made within three minutes of the last call, the **IUpdateNotify** object will remain loaded and a new instance is not created.</span></span> <span data-ttu-id="52a47-144">Si no se realiza ninguna llamada en un plazo de tres minutos, el objeto IUpdateNotify se descargará y se creará un nuevo objeto **IUpdateNotify** cuando se haga la siguiente llamada.</span><span class="sxs-lookup"><span data-stu-id="52a47-144">If no call is made within three minutes, the IUpdateNotify object will be unloaded and a new **IUpdateNotify** object will be created when the next call is made.</span></span> 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a><span data-ttu-id="52a47-145">Guía de referencia de API COM del instalador hacer clic y ejecutar</span><span class="sxs-lookup"><span data-stu-id="52a47-145">Click-to-Run installer COM API reference guide</span></span>

<span data-ttu-id="52a47-146">En la siguiente documentación de referencia de API:</span><span class="sxs-lookup"><span data-stu-id="52a47-146">In the following API reference documentation:</span></span>
  
- <span data-ttu-id="52a47-147">Los parámetros están en un formato de par clave/valor separados por un espacio.</span><span class="sxs-lookup"><span data-stu-id="52a47-147">Parameters are in a key/value pair format separated by a space.</span></span>
    
- <span data-ttu-id="52a47-148">Los parámetros no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="52a47-148">The parameters are not case-sensitive.</span></span>
    
- <span data-ttu-id="52a47-149">Hay una lista [de parámetros con](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) documentación disponible.</span><span class="sxs-lookup"><span data-stu-id="52a47-149">There is a [list of parameters](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) with documentation available.</span></span> 
    
- <span data-ttu-id="52a47-150">Ahora se incluye un resumen de la interfaz IUpdateNotify2.</span><span class="sxs-lookup"><span data-stu-id="52a47-150">Summary of IUpdateNotify2 interface is now included.</span></span>
    
### <a name="apply"></a><span data-ttu-id="52a47-151">Apply</span><span class="sxs-lookup"><span data-stu-id="52a47-151">Apply</span></span>

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a><span data-ttu-id="52a47-152">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52a47-152">Parameters</span></span>

-  <span data-ttu-id="52a47-153">_displaylevel:_ **true** para mostrar el estado de instalación, incluidos los errores, durante el proceso de actualización; **false** para ocultar el estado de instalación, incluidos los errores, durante el proceso de actualización.</span><span class="sxs-lookup"><span data-stu-id="52a47-153">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="52a47-154">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="52a47-154">The default is **false**.</span></span>
    
-  <span data-ttu-id="52a47-155">_forceappshutdown:_ **true** para forzar que las aplicaciones de Office se cierren inmediatamente cuando **se** desencadena la acción Aplicar; **false** para producir un error si se está ejecutando alguna aplicación de Office.</span><span class="sxs-lookup"><span data-stu-id="52a47-155">_forceappshutdown_: **true** to force Office applications to shut down immediately when the **Apply** action is triggered; **false** to fail if any Office applications are running.</span></span> <span data-ttu-id="52a47-156">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="52a47-156">The default is **false**.</span></span> <span data-ttu-id="52a47-157">Vea [los comentarios para](#bk_ApplyRemark) obtener más información.</span><span class="sxs-lookup"><span data-stu-id="52a47-157">See [Remarks](#bk_ApplyRemark) for more information.</span></span> 
    
  <span data-ttu-id="52a47-158">Si alguna aplicación de Office se ejecuta cuando **se** desencadena la acción Aplicar, **normalmente** se producirá un error en la acción Aplicar.</span><span class="sxs-lookup"><span data-stu-id="52a47-158">If any Office application is running when the **Apply** action is triggered, the **Apply** action will usually fail.</span></span> <span data-ttu-id="52a47-159">Pasar al método Apply hará que el `forceappshutdown=true` **servicio OfficeClickToRun** cierre inmediatamente las aplicaciones y aplique la actualización. </span><span class="sxs-lookup"><span data-stu-id="52a47-159">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down the applications and apply the update.</span></span> <span data-ttu-id="52a47-160">El usuario puede experimentar la pérdida de datos en este caso.</span><span class="sxs-lookup"><span data-stu-id="52a47-160">The user may experience data loss in this case.</span></span> 
    
#### <a name="return-results"></a><span data-ttu-id="52a47-161">Resultados devueltos</span><span class="sxs-lookup"><span data-stu-id="52a47-161">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52a47-162">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="52a47-162">**S_OK**</span></span> <br/> |<span data-ttu-id="52a47-163">La acción se envió correctamente al servicio Hacer clic y ejecutar para su ejecución.</span><span class="sxs-lookup"><span data-stu-id="52a47-163">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="52a47-164">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="52a47-164">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="52a47-165">El autor de la llamada no se está ejecutando con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="52a47-165">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="52a47-166">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="52a47-166">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="52a47-167">Se han pasado parámetros no válidos.</span><span class="sxs-lookup"><span data-stu-id="52a47-167">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="52a47-168">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="52a47-168">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="52a47-169">La acción no está permitida en este momento.</span><span class="sxs-lookup"><span data-stu-id="52a47-169">Action is not allowed at this time.</span></span> <span data-ttu-id="52a47-170">Vea [los comentarios para](#bk_ApplyRemark) obtener más información.</span><span class="sxs-lookup"><span data-stu-id="52a47-170">See [Remarks](#bk_ApplyRemark) for more information.</span></span>  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="52a47-171">Comentarios</span><span class="sxs-lookup"><span data-stu-id="52a47-171">Remarks</span></span>

- <span data-ttu-id="52a47-172">Si alguna aplicación de Office se ejecuta cuando **se** desencadena la acción Aplicar, se **producirá** un error en la acción Aplicar.</span><span class="sxs-lookup"><span data-stu-id="52a47-172">If any Office application is running when the **Apply** action is triggered, the **Apply** action will fail.</span></span> <span data-ttu-id="52a47-173">Pasar al método Apply hará que el servicio `forceappshutdown=true` **OfficeClickToRun** cierre inmediatamente cualquier aplicación de Office que se esté ejecutando y aplique la actualización. </span><span class="sxs-lookup"><span data-stu-id="52a47-173">Passing  `forceappshutdown=true` to the **Apply** method will cause the **OfficeClickToRun** service to immediately shut down any Office applications that are running and apply the update.</span></span> <span data-ttu-id="52a47-174">Es posible que el usuario experimente datos, ya que no se le pide que guarde los cambios en los documentos abiertos.</span><span class="sxs-lookup"><span data-stu-id="52a47-174">The user may experience data as they are not prompted to save changes to open documents..</span></span> 
    
- <span data-ttu-id="52a47-175">Esta acción solo se puede desencadenar cuando el estado COM es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="52a47-175">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="52a47-176">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="52a47-176">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="52a47-177">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="52a47-177">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="52a47-178">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="52a47-178">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="52a47-179">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="52a47-179">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="52a47-180">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="52a47-180">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="52a47-181">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="52a47-181">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="52a47-182">Si llama al **método Apply** sin descargar previamente el  contenido, el método **Apply** informará correctamente, ya que no detectó nada que aplicar y completó el proceso **aplicar** correctamente.</span><span class="sxs-lookup"><span data-stu-id="52a47-182">If you call the **Apply** method without previously downloading content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
### <a name="cancel"></a><span data-ttu-id="52a47-183">Cancelar</span><span class="sxs-lookup"><span data-stu-id="52a47-183">Cancel</span></span>

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a><span data-ttu-id="52a47-184">Resultados devueltos</span><span class="sxs-lookup"><span data-stu-id="52a47-184">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52a47-185">S_OK</span><span class="sxs-lookup"><span data-stu-id="52a47-185">S_OK</span></span>  <br/> |<span data-ttu-id="52a47-186">La acción se envió correctamente al servicio Hacer clic y ejecutar para su ejecución.</span><span class="sxs-lookup"><span data-stu-id="52a47-186">Action was successfully submitted to the Click-to-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="52a47-187">E_ILLEGAL_METHOD_CALL</span><span class="sxs-lookup"><span data-stu-id="52a47-187">E_ILLEGAL_METHOD_CALL</span></span>  <br/> |<span data-ttu-id="52a47-188">La acción no está permitida en este momento.</span><span class="sxs-lookup"><span data-stu-id="52a47-188">Action is not allowed at this time.</span></span> <span data-ttu-id="52a47-189">Vea la [sección Comentarios](#bk_CancelRemarks) para obtener más información</span><span class="sxs-lookup"><span data-stu-id="52a47-189">See the [Remarks](#bk_CancelRemarks) section for more information</span></span>  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a><span data-ttu-id="52a47-190">Comentarios</span><span class="sxs-lookup"><span data-stu-id="52a47-190">Remarks</span></span>

- <span data-ttu-id="52a47-191">Este método solo se puede desencadenar cuando el identificador de estado COM **eDOWNLOAD_WIP**.</span><span class="sxs-lookup"><span data-stu-id="52a47-191">This method can only be triggered when the COM status id **eDOWNLOAD_WIP**.</span></span> <span data-ttu-id="52a47-192">Intentará cancelar la acción de descarga actual.</span><span class="sxs-lookup"><span data-stu-id="52a47-192">It will attempt to cancel the current download action.</span></span> <span data-ttu-id="52a47-193">El estado COM cambiará a **eDOWNLOAD_CANCELLING** y, finalmente, cambiará **a eDOWNLOAD_CANCELED**.</span><span class="sxs-lookup"><span data-stu-id="52a47-193">The COM status will change to **eDOWNLOAD_CANCELLING** and eventually change to **eDOWNLOAD_CANCELED**.</span></span> <span data-ttu-id="52a47-194">El estado COM **devolverá** E_ILLEGAL_METHOD_CALL si se desencadena en cualquier otro momento.</span><span class="sxs-lookup"><span data-stu-id="52a47-194">The COM status will return **E_ILLEGAL_METHOD_CALL** if triggered at any other time.</span></span> 
    
### <a name="download"></a><span data-ttu-id="52a47-195">Descargar</span><span class="sxs-lookup"><span data-stu-id="52a47-195">Download</span></span>

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a><span data-ttu-id="52a47-196">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52a47-196">Parameters</span></span>

-  <span data-ttu-id="52a47-197">_displaylevel:_ **true** para mostrar el estado de instalación, incluidos los errores, durante el proceso de actualización; **false** para ocultar el estado de instalación, incluidos los errores, durante el proceso de actualización.</span><span class="sxs-lookup"><span data-stu-id="52a47-197">_displaylevel_: **true** to show the installation status, including errors, during the update process; **false** to hide the installation status, including errors, during the update process.</span></span> <span data-ttu-id="52a47-198">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="52a47-198">The default is **false**.</span></span>
    
-  <span data-ttu-id="52a47-199">_updatebaseurl:_ dirección URL del origen de descarga alternativo.</span><span class="sxs-lookup"><span data-stu-id="52a47-199">_updatebaseurl_: URL to the alternate download source.</span></span>
    
-  <span data-ttu-id="52a47-200">_updatetoversion:_ la versión a la que se actualizará Office.</span><span class="sxs-lookup"><span data-stu-id="52a47-200">_updatetoversion_: The version to update Office to.</span></span> <span data-ttu-id="52a47-201">Defina este parámetro si desea actualizar a una versión anterior a la versión instalada actualmente.</span><span class="sxs-lookup"><span data-stu-id="52a47-201">Define this parameter if you want to update to an older version than the version that is currently installed.</span></span>
    
-  <span data-ttu-id="52a47-202">_downloadsource:_ CLSID de la implementación personalizada de **IBackgroundCopyManager** (administrador de BITS).</span><span class="sxs-lookup"><span data-stu-id="52a47-202">_downloadsource_: CLSID of the customized **IBackgroundCopyManager** implementation (BITS manager).</span></span> 
    
-  <span data-ttu-id="52a47-203">_contentid:_ identifica el contenido que se debe descargar desde el servidor de contenido a través del administrador de BITS personalizado.</span><span class="sxs-lookup"><span data-stu-id="52a47-203">_contentid_: Identifies the content to download from the content server through the customized BITS manager.</span></span> <span data-ttu-id="52a47-204">Este valor se pasa a través de la interfaz bits para su interpretación.</span><span class="sxs-lookup"><span data-stu-id="52a47-204">This value is passed through the BITS interface for interpretation.</span></span>
    
#### <a name="return-results"></a><span data-ttu-id="52a47-205">Resultados devueltos</span><span class="sxs-lookup"><span data-stu-id="52a47-205">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52a47-206">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="52a47-206">**S_OK**</span></span> <br/> |<span data-ttu-id="52a47-207">La acción se envió correctamente al servicio Hacer clic y ejecutar para su ejecución.</span><span class="sxs-lookup"><span data-stu-id="52a47-207">Action was successfully submitted to the Click-To-Run service for execution.</span></span>  <br/> |
|<span data-ttu-id="52a47-208">**E_ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="52a47-208">**E_ACCESSDENIED**</span></span> <br/> |<span data-ttu-id="52a47-209">El autor de la llamada no se está ejecutando con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="52a47-209">The caller is not running with elevated privileges.</span></span>  <br/> |
|<span data-ttu-id="52a47-210">**E_INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="52a47-210">**E_INVALIDARG**</span></span> <br/> |<span data-ttu-id="52a47-211">Se han pasado parámetros no válidos.</span><span class="sxs-lookup"><span data-stu-id="52a47-211">Invalid parameters were passed.</span></span>  <br/> |
|<span data-ttu-id="52a47-212">**E_ILLEGAL_METHOD_CALL**</span><span class="sxs-lookup"><span data-stu-id="52a47-212">**E_ILLEGAL_METHOD_CALL**</span></span> <br/> |<span data-ttu-id="52a47-213">La acción no está permitida en este momento.</span><span class="sxs-lookup"><span data-stu-id="52a47-213">Action is not allowed at this time.</span></span> <span data-ttu-id="52a47-214">Vea [los comentarios para](#bk_DownloadRemark) obtener más información.</span><span class="sxs-lookup"><span data-stu-id="52a47-214">See [Remarks](#bk_DownloadRemark) for more information.</span></span>  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a><span data-ttu-id="52a47-215">Comentarios</span><span class="sxs-lookup"><span data-stu-id="52a47-215">Remarks</span></span>

- <span data-ttu-id="52a47-216">Debe especificar  _downloadsource y_  _contentid_ como un par.</span><span class="sxs-lookup"><span data-stu-id="52a47-216">You must specify  _downloadsource_ and  _contentid_ as a pair.</span></span> <span data-ttu-id="52a47-217">Si no es así, **el método Download** devolverá un **E_INVALIDARG** error.</span><span class="sxs-lookup"><span data-stu-id="52a47-217">If not, the **Download** method will return an **E_INVALIDARG** error.</span></span> 
    
- <span data-ttu-id="52a47-218">Si _se proporcionan downloadsource_, _contentid_ y _updatebaseurl,_ se omitirá _updatebaseurl._</span><span class="sxs-lookup"><span data-stu-id="52a47-218">If  _downloadsource_,  _contentid_, and  _updatebaseurl_ are provided,  _updatebaseurl_ will be ignored.</span></span> 
    
- <span data-ttu-id="52a47-219">Esta acción solo se puede desencadenar cuando el estado COM es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="52a47-219">This action can only be triggered when the COM status is one of the following:</span></span> 
    
  - <span data-ttu-id="52a47-220">**eUPDATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="52a47-220">**eUPDATE_UNKNOWN**</span></span>
    
  - <span data-ttu-id="52a47-221">**eDOWNLOAD_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="52a47-221">**eDOWNLOAD_CANCELLED**</span></span>
    
  - <span data-ttu-id="52a47-222">**eDOWNLOAD_FAILED**</span><span class="sxs-lookup"><span data-stu-id="52a47-222">**eDOWNLOAD_FAILED**</span></span>
    
  - <span data-ttu-id="52a47-223">**eDOWNLOAD_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="52a47-223">**eDOWNLOAD_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="52a47-224">**eAPPLY_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="52a47-224">**eAPPLY_SUCCEEDED**</span></span>
    
  - <span data-ttu-id="52a47-225">**eAPPLY_FAILED**</span><span class="sxs-lookup"><span data-stu-id="52a47-225">**eAPPLY_FAILED**</span></span>
    
- <span data-ttu-id="52a47-226">Si llama al método **Apply** sin contenido descargado previamente, el método **Apply** informará correctamente, ya que no detectó nada que aplicar y completó el proceso **aplicar** correctamente. </span><span class="sxs-lookup"><span data-stu-id="52a47-226">If you call the **Apply** method without previously downloaded content, the **Apply** method will report **Succeeded** as it detected nothing to apply and completed the **Apply** process successfully.</span></span> 
    
#### <a name="examples"></a><span data-ttu-id="52a47-227">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="52a47-227">Examples</span></span>

- <span data-ttu-id="52a47-228">Para descargar el contenido desde el administrador de BITS personalizado: llame a la **función download()** pasando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="52a47-228">To download the content from the customized BITS manager: Call the **download()** function passing the following parameters:</span></span> 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- <span data-ttu-id="52a47-229">Para descargar el contenido de la red de entrega de contenido (CDN) de Office: llame a la función **download()** sin especificar los parámetros _downloadsource_, _contentid_ o _updatebaseurl._</span><span class="sxs-lookup"><span data-stu-id="52a47-229">To download the content from the Office Content Delivery Network (CDN): Call the **download()** function without specifying the  _downloadsource_,  _contentid_, or  _updatebaseurl_ parameters.</span></span> 
    
- <span data-ttu-id="52a47-230">Para descargar el contenido desde una ubicación personalizada: llame a la **función download()** pasando el siguiente parámetro:</span><span class="sxs-lookup"><span data-stu-id="52a47-230">To download the content from a customized location: Call the **download()** function passing the following parameter:</span></span> 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a><span data-ttu-id="52a47-231">Estado</span><span class="sxs-lookup"><span data-stu-id="52a47-231">Status</span></span>

```cpp
typdef struct _UPDATE_STATUS_REPORT
{
    UPDATE_STATUS status;
    UINT error;
    LPCWSTR contentid;
}UPDATE_STATUS_REPORT;
HRESULT status([out] _UPDATE_STATUS_REPORT& pUpdateStatusReport) // Get status of current action
```

#### <a name="parameters"></a><span data-ttu-id="52a47-232">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52a47-232">Parameters</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="52a47-233">_pUpdateStatusReport_</span><span class="sxs-lookup"><span data-stu-id="52a47-233">_pUpdateStatusReport_</span></span> <br/> |<span data-ttu-id="52a47-234">Puntero a una UPDATE_STATUS_REPORT de datos.</span><span class="sxs-lookup"><span data-stu-id="52a47-234">Pointer to an UPDATE_STATUS_REPORT structure.</span></span>  <br/> |
   
#### <a name="return-results"></a><span data-ttu-id="52a47-235">Resultados devueltos</span><span class="sxs-lookup"><span data-stu-id="52a47-235">Return results</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52a47-236">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="52a47-236">**S_OK**</span></span> <br/> |<span data-ttu-id="52a47-237">El **método Status** siempre devuelve este resultado.</span><span class="sxs-lookup"><span data-stu-id="52a47-237">The **Status** method always returns this result.</span></span> <span data-ttu-id="52a47-238">Inspeccione la  `UPDATE_STATUS_RESULT` estructura para ver el estado de la acción actual.</span><span class="sxs-lookup"><span data-stu-id="52a47-238">Inspect the  `UPDATE_STATUS_RESULT` structure for the status of the current action.</span></span>  <br/> |
   
#### <a name="remarks"></a><span data-ttu-id="52a47-239">Comentarios</span><span class="sxs-lookup"><span data-stu-id="52a47-239">Remarks</span></span>

- <span data-ttu-id="52a47-240">El campo de estado del  `UPDATE_STATUS_REPORT` objeto contiene el estado de la acción actual.</span><span class="sxs-lookup"><span data-stu-id="52a47-240">The status field of the  `UPDATE_STATUS_REPORT` contains the status of the current action.</span></span> <span data-ttu-id="52a47-241">Se devuelve uno de los siguientes valores de estado:</span><span class="sxs-lookup"><span data-stu-id="52a47-241">One of the following status values is returned:</span></span> 
    
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

- <span data-ttu-id="52a47-242">Si el último comando produjo un error, el campo de error contiene información  `UPDATE_STATUS_REPORT` detallada sobre el error.</span><span class="sxs-lookup"><span data-stu-id="52a47-242">If the last command resulted in an error, the error field of the  `UPDATE_STATUS_REPORT` contains detailed information about the error.</span></span> <span data-ttu-id="52a47-243">Se devuelven dos tipos de códigos de error desde el **método Status.**</span><span class="sxs-lookup"><span data-stu-id="52a47-243">Two types of error codes are returned from the **Status** method.</span></span> 
    
- <span data-ttu-id="52a47-244">Si el error es menor que , el error es uno de los siguientes códigos de  `UPDATE_ERROR_CODE::eUNKNOWN` error predefinidos:</span><span class="sxs-lookup"><span data-stu-id="52a47-244">If the error less than  `UPDATE_ERROR_CODE::eUNKNOWN`, the error is one of the following pre-defined error codes:</span></span>
    
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

  <span data-ttu-id="52a47-245">Si el código de error devuelto es mayor que  `UPDATE_ERROR_CODE::eUNKNOWN` el **HRESULT** de una llamada de función con error.</span><span class="sxs-lookup"><span data-stu-id="52a47-245">If the return error code is larger than  `UPDATE_ERROR_CODE::eUNKNOWN` it is the **HRESULT** of a failed function call.</span></span> <span data-ttu-id="52a47-246">Para extraer el valor HRESULT  `UPDATE_ERROR_CODE::eUNKNOWN` restar del valor devuelto en el campo de error de  `UPDATE_STATUS_REPORT` la .</span><span class="sxs-lookup"><span data-stu-id="52a47-246">To extract the HRESULT subtract  `UPDATE_ERROR_CODE::eUNKNOWN` from the value returned in the error field of the  `UPDATE_STATUS_REPORT`.</span></span>
    
  <span data-ttu-id="52a47-247">La lista completa de valores de estado y error se puede ver inspeccionando la biblioteca de tipos **IUpdateNotify** incrustada en OfficeC2RCom.dll.</span><span class="sxs-lookup"><span data-stu-id="52a47-247">The complete list of status and error values can be viewed by inspecting the **IUpdateNotify** type library embedded in OfficeC2RCom.dll.</span></span> 
    
- <span data-ttu-id="52a47-248">El campo contentid se  usa  para las llamadas al estado después de iniciar la descarga y devuelve el contentid que se pasó a la **llamada de** descarga.</span><span class="sxs-lookup"><span data-stu-id="52a47-248">The contentid field is used for calls to **Status** after **Download** has initiated and returns the contentid that was passed in to the **Download** call.</span></span> <span data-ttu-id="52a47-249">Es un procedimiento recomendado inicializar este campo en **null** antes de llamar al método **Status** y, a continuación, comprobar el valor después de **que** se haya devuelto Status.</span><span class="sxs-lookup"><span data-stu-id="52a47-249">It is a best practice to initialize this field to **null** before you call the **Status** method and then check the value after **Status** has been returned.</span></span> <span data-ttu-id="52a47-250">Si el valor sigue siendo **nulo,** significa que no hay contentid que devolver.</span><span class="sxs-lookup"><span data-stu-id="52a47-250">If the value is still **null**, that means there is no contentid to return.</span></span> <span data-ttu-id="52a47-251">Si el valor no es **nulo,** debe liberarlo con una llamada a **SysFreeString()**.</span><span class="sxs-lookup"><span data-stu-id="52a47-251">If the value is not **null**, you need to free it with a call to **SysFreeString()**.</span></span> <span data-ttu-id="52a47-252">Este es un fragmento de código de cómo llamar al **estado después** de **descargar**.</span><span class="sxs-lookup"><span data-stu-id="52a47-252">Here is a code snippet of how to call **Status** after **Download**.</span></span>
    
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

### <a name="summary-of-iupdatenotify2-interface"></a><span data-ttu-id="52a47-253">Resumen de la interfaz IUpdateNotify2</span><span class="sxs-lookup"><span data-stu-id="52a47-253">Summary of IUpdateNotify2 interface</span></span>

<span data-ttu-id="52a47-254">Desde la versión [16.0.8208.6352] hemos agregado una nueva interfaz **IUpdateNotify2.**</span><span class="sxs-lookup"><span data-stu-id="52a47-254">From version [16.0.8208.6352] we have added a new **IUpdateNotify2** interface.</span></span> 
  
- <span data-ttu-id="52a47-255">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span><span class="sxs-lookup"><span data-stu-id="52a47-255">CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}</span></span>
    
- <span data-ttu-id="52a47-256">Esta interfaz también hospedaba la interfaz IUpdateNotify original para proporcionar compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="52a47-256">This interface also hosted the original IUpdateNotify interface to provide backward compatibility.</span></span> <span data-ttu-id="52a47-257">Lo que significa que si usa esta interfaz, tendrá acceso a todos los métodos proporcionados en la interfaz **UpdateNotifyObject.**</span><span class="sxs-lookup"><span data-stu-id="52a47-257">Which means if you use this interface, you have access to all the methods provided in **UpdateNotifyObject** interface.</span></span> 
    
- <span data-ttu-id="52a47-258">Nuevos métodos agregados a IUpdateNotify2:</span><span class="sxs-lookup"><span data-stu-id="52a47-258">New methods added to IUpdateNotify2:</span></span>
    
  - <span data-ttu-id="52a47-259">**HRESULT** GetBlockingApps([out] BSTR \* AppsList).</span><span class="sxs-lookup"><span data-stu-id="52a47-259">**HRESULT** GetBlockingApps([out] BSTR \* AppsList).</span></span> <span data-ttu-id="52a47-260">Obtener la lista de aplicaciones de bloqueo de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="52a47-260">Get updates blocking apps list.</span></span> <span data-ttu-id="52a47-261">Esta llamada devolverá la ejecución de aplicaciones de Office que bloquearán el proceso de actualización para que no se ejecute.</span><span class="sxs-lookup"><span data-stu-id="52a47-261">This call will return running Office apps which will block the update process from proceeding.</span></span> 
    
  - <span data-ttu-id="52a47-262">**HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span><span class="sxs-lookup"><span data-stu-id="52a47-262">**HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR \* OfficeData).</span></span> <span data-ttu-id="52a47-263">Obtener datos de implementación de Office.</span><span class="sxs-lookup"><span data-stu-id="52a47-263">Get Office deployment Data.</span></span> 
    
- <span data-ttu-id="52a47-264">Si desea usar los nuevos métodos, debe asegurarse de:</span><span class="sxs-lookup"><span data-stu-id="52a47-264">If you want to use the new methods, you need to make sure:</span></span>
    
  - <span data-ttu-id="52a47-265">La versión C2R es más reciente que la compilación anterior ( \> = compilación de bifurcación de junio).</span><span class="sxs-lookup"><span data-stu-id="52a47-265">Your C2R version is newer than the above build (\>= June fork build).</span></span>
    
  - <span data-ttu-id="52a47-266">Use UpdateNotifyObject2, en lugar **de UpdateNotifyObject** para llamar **a CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="52a47-266">Use UpdateNotifyObject2, instead of **UpdateNotifyObject** to call **CoCreateInstance**.</span></span>
    
<span data-ttu-id="52a47-267">Si no usa ninguno de los nuevos métodos, no es necesario cambiar nada.</span><span class="sxs-lookup"><span data-stu-id="52a47-267">If you don't use any of the new methods, you don't need to change anything.</span></span> <span data-ttu-id="52a47-268">Todos los métodos existentes funcionarán exactamente del mismo modo que antes.</span><span class="sxs-lookup"><span data-stu-id="52a47-268">All the existing methods will work as exact the same way as before.</span></span>
  
## <a name="implementing-the-bits-interface"></a><span data-ttu-id="52a47-269">Implementación de la interfaz bits</span><span class="sxs-lookup"><span data-stu-id="52a47-269">Implementing the BITS interface</span></span>

<span data-ttu-id="52a47-270">El [Servicio de transferencia inteligente en](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) segundo plano (BITS) es un servicio proporcionado por Microsoft para transferir archivos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="52a47-270">The [Background Intelligent Transfer Service](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (BITS) is a service provided by Microsoft to transfer files between a client and server.</span></span> <span data-ttu-id="52a47-271">BITS es uno de los canales que el instalador de Hacer clic y ejecutar de Office puede usar para descargar contenido.</span><span class="sxs-lookup"><span data-stu-id="52a47-271">BITS is one of the channels that Office Click-To-Run installer can use to download content.</span></span> <span data-ttu-id="52a47-272">De forma predeterminada, el instalador de Hacer clic y ejecutar de Aplicaciones de Microsoft 365 usa la implementación integrada de BITS de Windows para descargar el contenido de la red CDN.</span><span class="sxs-lookup"><span data-stu-id="52a47-272">By default, the Microsoft 365 Apps Click-To-Run installer uses the Windows' built in implementation of BITS to download the content from the CDN.</span></span> 
  
<span data-ttu-id="52a47-273">Al proporcionar una implementación de BITS personalizada al método **download()** de la interfaz **IUpdateNotify,** el software de administración puede controlar dónde y cómo el cliente descarga el contenido.</span><span class="sxs-lookup"><span data-stu-id="52a47-273">By providing a customized BITS implementation to the **download()** method of the **IUpdateNotify** interface, your manageability software can control where and how the client downloads the content.</span></span> <span data-ttu-id="52a47-274">Una interfaz BITS personalizada es útil al proporcionar un canal de distribución de contenido personalizado que no sea los canales integrados hacer clic y ejecutar, como la red CDN, los servidores IIS o los recursos compartidos de archivos.</span><span class="sxs-lookup"><span data-stu-id="52a47-274">A customized BITS interface is useful when providing a custom content distribution channel other than the Click-to-Run built-in channels, such as the CDN, IIS servers, or file shares.</span></span> 
  
<span data-ttu-id="52a47-275">El requisito mínimo para que una interfaz BITS personalizada funcione con el servicio C2R de Office es:</span><span class="sxs-lookup"><span data-stu-id="52a47-275">The minimum requirement for a customized BITS interface to work with Office C2R service is:</span></span>
  
- <span data-ttu-id="52a47-276">Para **IBackgroundCopyManager:**</span><span class="sxs-lookup"><span data-stu-id="52a47-276">For **IBackgroundCopyManager**:</span></span>
    
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

- <span data-ttu-id="52a47-277">Para **IBackgroundCopyJob:**</span><span class="sxs-lookup"><span data-stu-id="52a47-277">For **IBackgroundCopyJob**:</span></span>
    
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

- <span data-ttu-id="52a47-278">Para **IBackgroundCopyJob3:**</span><span class="sxs-lookup"><span data-stu-id="52a47-278">For **IBackgroundCopyJob3**:</span></span>
    
  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- <span data-ttu-id="52a47-279">Para las  `Addfile` funciones  `AddFileWithRanges` y, la dirección URL remota tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="52a47-279">For the  `Addfile` and  `AddFileWithRanges` functions, the remote URL is in the following format:</span></span> 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - <span data-ttu-id="52a47-280">cmbits está codificado de forma hard y significa BITS personalizados.</span><span class="sxs-lookup"><span data-stu-id="52a47-280">cmbits is hard coded, and stands for customized BITS.</span></span>
    
  -  <span data-ttu-id="52a47-281">_\<contentid\>_ es el _parámetro contentid_ del **método Download().**</span><span class="sxs-lookup"><span data-stu-id="52a47-281">_\<contentid\>_ is the  _contentid_ parameter for the **Download()** method.</span></span> 
    
  -  <span data-ttu-id="52a47-282">_\<relative path to target file\>_ proporciona la ubicación y el nombre de archivo del archivo que se debe descargar.</span><span class="sxs-lookup"><span data-stu-id="52a47-282">_\<relative path to target file\>_ provides the location and file name of the file to download.</span></span> 
    
    <span data-ttu-id="52a47-283">Por ejemplo, si ha proporcionado un _contentid_ del método Download() y Office C2R desea descargar el archivo #A0 de la versión, como el archivo, llamará a `f732af58-5d86-4299-abe9-7595c35136ef`  `v32.cab` **AddFile()** con lo `RemoteUrl` siguiente:</span><span class="sxs-lookup"><span data-stu-id="52a47-283">For example, if you have provided a  _contentid_ of  `f732af58-5d86-4299-abe9-7595c35136ef` to the **Download()** method, and Office C2R wants to download the version cab file, such as  `v32.cab` file, it will call **AddFile()** with the following  `RemoteUrl`:</span></span>
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- <span data-ttu-id="52a47-284">Para **IBackgroundCopyError:**</span><span class="sxs-lookup"><span data-stu-id="52a47-284">For **IBackgroundCopyError**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- <span data-ttu-id="52a47-285">Para **IBackgroundCopyFile:**</span><span class="sxs-lookup"><span data-stu-id="52a47-285">For **IBackgroundCopyFile**:</span></span>
    
  ```cpp
  HRESULT _stdcall GetLocalName([out] LPWSTR *ppName); 
  HRESULT _stdcall GetRemoteName([out] LPWSTR *ppName);
  
  ```
## <a name="automating-content-staging"></a><span data-ttu-id="52a47-286">Automatización del almacenamiento provisional de contenido</span><span class="sxs-lookup"><span data-stu-id="52a47-286">Automating content staging</span></span>

<span data-ttu-id="52a47-287">Los administradores de TI pueden elegir que los clientes de escritorio estén habilitados para recibir actualizaciones automáticamente cuando estén disponibles directamente desde la red CDN o pueden elegir controlar la implementación de actualizaciones disponibles desde los canales de actualización mediante la Herramienta de implementación de Office o Microsoft Endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="52a47-287">IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the CDN or they can choose to control the deployment of updates available from the update channels using the Office Deployment Tool or Microsoft Endpoint Configuration Manager.</span></span>
  
<span data-ttu-id="52a47-288">El servicio admite la capacidad de las herramientas de administración para reconocer y automatizar la descarga del contenido cuando hay actualizaciones disponibles.</span><span class="sxs-lookup"><span data-stu-id="52a47-288">The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.</span></span>
  
<span data-ttu-id="52a47-289">**La siguiente imagen es una introducción a la descarga de una imagen personalizada**</span><span class="sxs-lookup"><span data-stu-id="52a47-289">**The following image is an overview of downloading a custom image**</span></span>

<span data-ttu-id="52a47-290">![Diagrama del uso de la interfaz COM en el programa de instalación de Hacer clic y ejecutar de Office.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Diagrama de uso de la interfaz COM en el instalador de Hacer clic y ejecutar de Office")</span><span class="sxs-lookup"><span data-stu-id="52a47-290">![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "A diagram of using the COM interface on the Office Click-To-Run installer")</span></span>
  
### <a name="overview-of-downloading-a-custom-image"></a><span data-ttu-id="52a47-291">Información general sobre la descarga de una imagen personalizada</span><span class="sxs-lookup"><span data-stu-id="52a47-291">Overview of downloading a custom image</span></span>
  
<span data-ttu-id="52a47-292">En el diagrama anterior, verá que hay disponible una nueva imagen de Aplicaciones de Microsoft 365 en la red CDN.</span><span class="sxs-lookup"><span data-stu-id="52a47-292">In the previous diagram, you see that a new Microsoft 365 Apps image is available on the CDN.</span></span> <span data-ttu-id="52a47-293">Junto con la imagen aplicaciones de Microsoft 365, hay disponible una API que tiene la información necesaria para permitir que el software de administración cree imágenes personalizadas directamente reemplazando la necesidad de usar la Herramienta de implementación de Office.</span><span class="sxs-lookup"><span data-stu-id="52a47-293">Along with the Microsoft 365 Apps image, an API is available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.</span></span>

<span data-ttu-id="52a47-294">Una empresa configura su WSUS para sincronizar las actualizaciones de Aplicaciones de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="52a47-294">An enterprise configures their WSUS to sync the Microsoft 365 Apps updates.</span></span> <span data-ttu-id="52a47-295">Estas actualizaciones no contienen la carga real de la imagen, pero permiten que el software de administración reconozca cuándo hay contenido nuevo disponible.</span><span class="sxs-lookup"><span data-stu-id="52a47-295">These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available.</span></span> <span data-ttu-id="52a47-296">A continuación, el software de administración puede leer los metadatos de La actualización de aplicaciones de Microsoft 365 para comprender a qué versión de Office se aplica la actualización.</span><span class="sxs-lookup"><span data-stu-id="52a47-296">The manageability software can then read the Microsoft 365 Apps Update metadata to understand what version of Office the update applies to.</span></span>

<span data-ttu-id="52a47-297">Si la actualización es aplicable, el software de facilidad de uso puede usar el contenido de la red CDN y la lista de archivos para crear la imagen personalizada y almacenarla en la ubicación del recurso compartido de archivos que está configurada para usar.</span><span class="sxs-lookup"><span data-stu-id="52a47-297">If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.</span></span>
  
### <a name="using-the-microsoft-365-apps-file-list-api"></a><span data-ttu-id="52a47-298">Uso de la API de lista de archivos de Aplicaciones de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="52a47-298">Using the Microsoft 365 Apps file list API</span></span>

<span data-ttu-id="52a47-299">La API de lista de archivos de Aplicaciones de Microsoft 365 se usa para recuperar los nombres de los archivos necesarios para una actualización concreta de Aplicaciones de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="52a47-299">The Microsoft 365 Apps file list API is used to retrieve the names of the files needed for a particular Microsoft 365 Apps update.</span></span>

<span data-ttu-id="52a47-300">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="52a47-300">HTTP Request</span></span>

<span data-ttu-id="52a47-301">GET https://config.office.com/api/filelist</span><span class="sxs-lookup"><span data-stu-id="52a47-301">GET https://config.office.com/api/filelist</span></span>

<span data-ttu-id="52a47-302">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="52a47-302">Do not supply a request body for this method.</span></span>

<span data-ttu-id="52a47-303">No se requieren permisos para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="52a47-303">No permissions are required to call this API.</span></span>

<span data-ttu-id="52a47-304">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="52a47-304">Optional query parameters</span></span>

|<span data-ttu-id="52a47-305">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="52a47-305">**Name**</span></span>|<span data-ttu-id="52a47-306">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="52a47-306">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="52a47-307">channel</span><span class="sxs-lookup"><span data-stu-id="52a47-307">channel</span></span> <br/>| <span data-ttu-id="52a47-308">Especifica el nombre del canal</span><span class="sxs-lookup"><span data-stu-id="52a47-308">Specifies the channel name</span></span>  <br/> <span data-ttu-id="52a47-309">Opcional: valor predeterminado en 'SemiAnnual'</span><span class="sxs-lookup"><span data-stu-id="52a47-309">Optional – default to ‘SemiAnnual’</span></span> <br/> <span data-ttu-id="52a47-310">Valores admitidos https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element</span><span class="sxs-lookup"><span data-stu-id="52a47-310">Supported values https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element</span></span> |
| <span data-ttu-id="52a47-311">version</span><span class="sxs-lookup"><span data-stu-id="52a47-311">version</span></span> <br/>| <span data-ttu-id="52a47-312">Especifica la versión de actualización</span><span class="sxs-lookup"><span data-stu-id="52a47-312">Specifies the update version</span></span> <br/> <span data-ttu-id="52a47-313">Opcional: el valor predeterminado es la versión más reciente disponible para el canal especificado.</span><span class="sxs-lookup"><span data-stu-id="52a47-313">Optional – defaults to the latest version available for the specified channel</span></span> |
| <span data-ttu-id="52a47-314">arch</span><span class="sxs-lookup"><span data-stu-id="52a47-314">arch</span></span> <br/>| <span data-ttu-id="52a47-315">Especifica la arquitectura de cliente</span><span class="sxs-lookup"><span data-stu-id="52a47-315">Specifies client architecture</span></span> <br/> <span data-ttu-id="52a47-316">Opcional: el valor predeterminado es "x64"</span><span class="sxs-lookup"><span data-stu-id="52a47-316">Optional – defaults to ‘x64’</span></span> <br/> <span data-ttu-id="52a47-317">Valores admitidos: x64, x86</span><span class="sxs-lookup"><span data-stu-id="52a47-317">Supported values: x64, x86</span></span> |
| <span data-ttu-id="52a47-318">lid</span><span class="sxs-lookup"><span data-stu-id="52a47-318">lid</span></span> <br/>| <span data-ttu-id="52a47-319">Especifica los archivos de idioma que se incluirán</span><span class="sxs-lookup"><span data-stu-id="52a47-319">Specifies the language files to include</span></span> <br/> <span data-ttu-id="52a47-320">Opcional: el valor predeterminado es none</span><span class="sxs-lookup"><span data-stu-id="52a47-320">Optional – defaults to none</span></span> <br/> <span data-ttu-id="52a47-321">Para especificar varios idiomas, incluya un parámetro de consulta de tapa para cada idioma</span><span class="sxs-lookup"><span data-stu-id="52a47-321">To specify multiple languages, include an lid query parameter for each language</span></span> <br/> <span data-ttu-id="52a47-322">Use el formato de identificador de idioma, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="52a47-322">Use the language identifier format, ex.</span></span> <span data-ttu-id="52a47-323">'en-us', 'fr-fr'</span><span class="sxs-lookup"><span data-stu-id="52a47-323">‘en-us’, ‘fr-fr’</span></span> |
| <span data-ttu-id="52a47-324">alllanguages</span><span class="sxs-lookup"><span data-stu-id="52a47-324">alllanguages</span></span> <br/>| <span data-ttu-id="52a47-325">Especifica que se incluyan todos los archivos de idioma</span><span class="sxs-lookup"><span data-stu-id="52a47-325">Specifies to include all language files</span></span> <br/> <span data-ttu-id="52a47-326">Opcional: el valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="52a47-326">Optional – defaults to false</span></span> |

<span data-ttu-id="52a47-327">Respuesta HTTP</span><span class="sxs-lookup"><span data-stu-id="52a47-327">HTTP Response</span></span>

<span data-ttu-id="52a47-328">Si se realiza correctamente, este método devuelve un código de respuesta 200 OK y la colección de objetos de archivo en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="52a47-328">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>

<span data-ttu-id="52a47-329">Para crear una imagen, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="52a47-329">To create an image, follow these steps:</span></span>
1.  <span data-ttu-id="52a47-330">Llame a la API y proporcione los parámetros de consulta adecuados para el canal, la versión y la arquitectura de la actualización que le interesa.</span><span class="sxs-lookup"><span data-stu-id="52a47-330">Call the API, providing the appropriate query parameters for the channel, version and architecture of the update you are interested in.</span></span>
<span data-ttu-id="52a47-331">Nota: Los objetos de archivo con el atributo "lcid": "0" son archivos de idioma neutro y deben incluirse en la imagen.</span><span class="sxs-lookup"><span data-stu-id="52a47-331">Note: File objects with the attribute "lcid": "0" are language neutral files and must be included in the image.</span></span>
2.  <span data-ttu-id="52a47-332">Construya una imagen local de la red CDN mediante la iteración de los objetos de archivo y la copia de los archivos de la red CDN, al mismo tiempo que crea la estructura de carpetas especificada por el atributo "relativePath" definido para cada uno de los objetos de archivo.</span><span class="sxs-lookup"><span data-stu-id="52a47-332">Construct a local image of the CDN by iterating through the file objects and copying the CDN files, while creating the folder structure as specified by the “relativePath” attribute defined for each of the file objects.</span></span>

<span data-ttu-id="52a47-333">En el siguiente ejemplo se recupera la lista de archivos del Canal actual y la versión 16.0.4229.1004 para 64 bits e incluye los archivos en francés e inglés:</span><span class="sxs-lookup"><span data-stu-id="52a47-333">The following example retrieves the file list for the Current Channel and version 16.0.4229.1004 for 64bit and includes the French and English language files:</span></span>

```http
Get https://config.office.com/api/filelist?Channel=Current&Version=16.0.4229.1004&Arch=x64&Lid=fr-fr&Lid=en-US
```

### <a name="hash-verification-of-dat-files"></a><span data-ttu-id="52a47-334">Comprobación de hash de archivos .dat</span><span class="sxs-lookup"><span data-stu-id="52a47-334">Hash verification of .dat files</span></span>

<span data-ttu-id="52a47-335">Las herramientas de creación de imágenes pueden comprobar la integridad de los archivos .dat descargados comparando un valor hash calculado con el valor hash proporcionado asociado a cada uno de los archivos .dat.</span><span class="sxs-lookup"><span data-stu-id="52a47-335">Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed hash value with the supplied hash value associated with each of the .dat files.</span></span> <span data-ttu-id="52a47-336">A continuación se muestra un ejemplo de un objeto de archivo que especifica valores hashLocation y hashAlgorithm:</span><span class="sxs-lookup"><span data-stu-id="52a47-336">Following is an example of a file object that specifies hashLocation and hashAlgorithm values:</span></span>
  
```xml
{
  "url": "https://officecdn.microsoft.com/pr/7ffbc6bf-bc32-4f92-8982-f9dd17fd3114/office/data/16.0.1234.1001/stream.x64.x-none.dat",
  "name": "stream.x64.x-none.dat",
  "relativePath": "/office/data/16.0.1234.1001/",
  "hashLocation": "s640.cab/stream.x64.x-none.hash",
  "hashAlgorithm": "Sha256",
  "lcid": "0"
},
```

- <span data-ttu-id="52a47-337">El **atributo hashLocation** especifica la ubicación de ruta de acceso relativa del archivo .cab que contiene el valor hash.</span><span class="sxs-lookup"><span data-stu-id="52a47-337">The **hashLocation** attribute specifies the relative path location of .cab file that contains the hash value.</span></span> <span data-ttu-id="52a47-338">Construya la ubicación del archivo hash concatenando URL + relativePath + hashLocation.</span><span class="sxs-lookup"><span data-stu-id="52a47-338">Construct the hash file location by concatenating URL + relativePath + hashLocation.</span></span> <span data-ttu-id="52a47-339">En el siguiente ejemplo, la stream.x64.bg-bg.hash sería:</span><span class="sxs-lookup"><span data-stu-id="52a47-339">In the following example, the stream.x64.bg-bg.hash location would be:</span></span> 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- <span data-ttu-id="52a47-340">El **atributo hashAlgorithm** especifica qué algoritmo hash se usó.</span><span class="sxs-lookup"><span data-stu-id="52a47-340">The **hashAlgorithm** attribute specifies what hashing algorithm was used.</span></span> 
    
  <span data-ttu-id="52a47-341">Para validar la integridad del archivo stream.x64.bg-bg.dat, abra el archivo stream.x64.bg-bg.hash y lea el valor HASH, que es la primera línea de texto del archivo hash.</span><span class="sxs-lookup"><span data-stu-id="52a47-341">To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the HASH value which is the first line of text in the hash file.</span></span> <span data-ttu-id="52a47-342">Compare esto con el valor hash calculado (mediante el algoritmo hash especificado) para comprobar la integridad del archivo .dat descargado.</span><span class="sxs-lookup"><span data-stu-id="52a47-342">Compare this to the computed hash value (using the specified hashing algorithm) to verify the integrity of the downloaded .dat file.</span></span>
    
  <span data-ttu-id="52a47-343">En el siguiente ejemplo se muestra el código C# para leer el hash.</span><span class="sxs-lookup"><span data-stu-id="52a47-343">The following example shows the C# code to read the hash.</span></span>
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="microsoft-365-apps-updates"></a><span data-ttu-id="52a47-344">Actualizaciones de aplicaciones de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="52a47-344">Microsoft 365 Apps Updates</span></span>

<span data-ttu-id="52a47-345">Todas las actualizaciones de aplicaciones de Microsoft 365 se publican en el Catálogo [de Microsoft Update](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span><span class="sxs-lookup"><span data-stu-id="52a47-345">All Microsoft 365 Apps Updates are published to the [Microsoft Update Catalog](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).</span></span>
  
<span data-ttu-id="52a47-346">Las actualizaciones de aplicaciones de Microsoft 365 permiten que el software de administración trate las actualizaciones de aplicaciones de Microsoft 365 de una manera muy similar a cualquier otra actualización de WU con una excepción; las actualizaciones de cliente no contienen una carga real.</span><span class="sxs-lookup"><span data-stu-id="52a47-346">Microsoft 365 Apps Updates enable manageability software to treat Microsoft 365 Apps Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload.</span></span> <span data-ttu-id="52a47-347">Las actualizaciones de aplicaciones de Microsoft 365 no deben instalarse en ningún cliente, sino que se deben usar para desencadenar los flujos de trabajo con el software de facilidad de uso que reemplaza el comando de instalación por el mecanismo de instalación basado en COM mostrado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="52a47-347">The Microsoft 365 Apps Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.</span></span>

<span data-ttu-id="52a47-348">**En la figura siguiente se muestra un diagrama del flujo de trabajo de actualización de cliente de Office 365.**</span><span class="sxs-lookup"><span data-stu-id="52a47-348">**The following figure shows a diagram of the Office 365 Client Update workflow.**</span></span>

<span data-ttu-id="52a47-349">![Diagrama de flujo de trabajo para las actualizaciones de cliente de O365PP.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Diagrama de flujo de trabajo para actualizaciones de cliente de O365PP")</span><span class="sxs-lookup"><span data-stu-id="52a47-349">![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")</span></span>
  
<span data-ttu-id="52a47-350">Cada actualización de aplicaciones de Microsoft 365 que se publica incluye metadatos sobre la actualización.</span><span class="sxs-lookup"><span data-stu-id="52a47-350">Each Microsoft 365 Apps Update that is published includes metadata about the update.</span></span> <span data-ttu-id="52a47-351">Estos metadatos incluyen un parámetro denominado MoreInfoUrl que se puede usar para derivar la llamada API a la API de lista de archivos para esa actualización específica.</span><span class="sxs-lookup"><span data-stu-id="52a47-351">This metadata includes a parameter called MoreInfoUrl which can be used to derive the API call to the file list API for that specific update.</span></span>

<span data-ttu-id="52a47-352">En el siguiente ejemplo, la API de lista de archivos está incrustada en MoreInfoURL y comienza por "ServicePath="</span><span class="sxs-lookup"><span data-stu-id="52a47-352">In the following example, the file list API is embedded in the MoreInfoURL and starts with “ServicePath=”</span></span>

<span data-ttu-id="52a47-353"> http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath=https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True</span><span class="sxs-lookup"><span data-stu-id="52a47-353">http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath=https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True</span></span>
  
### <a name="additional-metadata-for-automating-content-staging"></a><span data-ttu-id="52a47-354">Metadatos adicionales para automatizar el almacenamiento provisional de contenido</span><span class="sxs-lookup"><span data-stu-id="52a47-354">Additional metadata for automating content staging</span></span>

<span data-ttu-id="52a47-355">**API de historial de versiones**</span><span class="sxs-lookup"><span data-stu-id="52a47-355">**Release History API**</span></span>
  
<span data-ttu-id="52a47-356">La API del historial de versiones de Aplicaciones de Microsoft 365 se usa para recuperar detalles de cada una de las actualizaciones publicadas en la red CDN junto con los nombres de canal y otros atributos de canal.</span><span class="sxs-lookup"><span data-stu-id="52a47-356">The Microsoft 365 Apps release history API is used to retrieve details for each of the updates published to the CDN along with the channel names and other channel attributes.</span></span>

<span data-ttu-id="52a47-357">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="52a47-357">HTTP Request</span></span>

```http
GET https://config.office.com/api/filelist/channels 
```

<span data-ttu-id="52a47-358">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="52a47-358">Do not supply a request body for this method.</span></span>

<span data-ttu-id="52a47-359">No se requieren permisos para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="52a47-359">No permissions are required to call this API.</span></span>

<span data-ttu-id="52a47-360">Respuesta HTTP</span><span class="sxs-lookup"><span data-stu-id="52a47-360">HTTP Response</span></span>

<span data-ttu-id="52a47-361">Si se realiza correctamente, este método devuelve un código de respuesta 200 OK y la colección de objetos de archivo en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="52a47-361">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>

<span data-ttu-id="52a47-362">**API de SKU**</span><span class="sxs-lookup"><span data-stu-id="52a47-362">**SKUs API**</span></span>
  
<span data-ttu-id="52a47-363">La API de SKU devuelve información útil para determinar qué productos están disponibles para la implementación y el mantenimiento desde la red CDN de Office junto con varias opciones para cada uno.</span><span class="sxs-lookup"><span data-stu-id="52a47-363">The SKUs API returns information that is useful for determining which products are available for deployment and servicing from the Office CDN along with various options for each.</span></span>

<span data-ttu-id="52a47-364">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="52a47-364">HTTP Request</span></span>

```http
GET https://config.office.com/api/filelist/skus 
```

<span data-ttu-id="52a47-365">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="52a47-365">Do not supply a request body for this method.</span></span>

<span data-ttu-id="52a47-366">No se requieren permisos para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="52a47-366">No permissions are required to call this API.</span></span>

<span data-ttu-id="52a47-367">Respuesta HTTP</span><span class="sxs-lookup"><span data-stu-id="52a47-367">HTTP Response</span></span>

<span data-ttu-id="52a47-368">Si se realiza correctamente, este método devuelve un código de respuesta 200 OK y la colección de objetos de archivo en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="52a47-368">If successful, this method returns a 200 OK response code and collection of file objects in the response body.</span></span>
