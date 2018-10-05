---
title: Elija una versión específica de MAPI para cargar
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d353eba55e33b8ab48b3c47d2f31f1b5e0973b58
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399735"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a><span data-ttu-id="0f781-103">Elija una versión específica de MAPI para cargar</span><span class="sxs-lookup"><span data-stu-id="0f781-103">Choose a specific version of MAPI to load</span></span>

<span data-ttu-id="0f781-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f781-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f781-105">Cuando se vincula explícitamente a una implementación de MAPI, debe seleccionar cuidadosamente qué implementación a cargar.</span><span class="sxs-lookup"><span data-stu-id="0f781-105">When linking explicitly to an implementation of MAPI, you must carefully select which implementation to load.</span></span> 
  
<span data-ttu-id="0f781-106">Existen dos métodos para vincular explícitamente a una implementación de MAPI.</span><span class="sxs-lookup"><span data-stu-id="0f781-106">There are two methods to link explicitly to an implementation of MAPI.</span></span> 
  
1. <span data-ttu-id="0f781-107">Puede cargar la biblioteca de código auxiliar MAPI y especificar en el registro de un archivo DLL personalizado para cargar y distribuir MAPI llamadas a.</span><span class="sxs-lookup"><span data-stu-id="0f781-107">You can load the MAPI stub library, and specify in the registry a custom DLL to load and dispatch MAPI calls to.</span></span>
    
2. <span data-ttu-id="0f781-108">Puede implementar el algoritmo de búsqueda de cliente MAPI para buscar la versión de MAPI utilizado por el cliente de correo predeterminado y lo carga.</span><span class="sxs-lookup"><span data-stu-id="0f781-108">You can implement the MAPI client lookup algorithm to look up the version of MAPI used by the default mail client and load it.</span></span>
    
<span data-ttu-id="0f781-109">Debido a que puede cambiar la [Configuración del registro de Mapi32.dll código auxiliar](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) para dirigir la aplicación para usar cualquier implementación de MAPI, se recomienda que dirigir la aplicación para usar una implementación de MAPI que se han probado con.</span><span class="sxs-lookup"><span data-stu-id="0f781-109">Because you can change the [Mapi32.dll Stub Registry Settings](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) to direct your application to use any implementation of MAPI, we recommend that you direct your application to use an implementation of MAPI that you have tested with.</span></span> <span data-ttu-id="0f781-110">El siguiente, describe ambos métodos de vinculación de forma explícita.</span><span class="sxs-lookup"><span data-stu-id="0f781-110">The following describes both methods of linking explicitly.</span></span> 
  
## <a name="reading-from-the-registry"></a><span data-ttu-id="0f781-111">Lectura del registro</span><span class="sxs-lookup"><span data-stu-id="0f781-111">Reading from the registry</span></span>

### <a name="to-read-mapi-implementation-information-from-the-registry"></a><span data-ttu-id="0f781-112">Para leer información de implementación de MAPI desde el registro</span><span class="sxs-lookup"><span data-stu-id="0f781-112">To read MAPI implementation information from the registry</span></span>

1. <span data-ttu-id="0f781-113">Las claves del registro que indican un archivo DLL personalizado para un cliente de correo se encuentran en la `HKLM\Software\Clients\Mail` clave del cliente de correo.</span><span class="sxs-lookup"><span data-stu-id="0f781-113">The registry keys that indicate a custom DLL for a mail client are located under the  `HKLM\Software\Clients\Mail` key of the mail client.</span></span> 
    
   <span data-ttu-id="0f781-114">En la siguiente tabla se describe estas claves:</span><span class="sxs-lookup"><span data-stu-id="0f781-114">The following table describes these keys:</span></span>
    
   |<span data-ttu-id="0f781-115">**Clave**</span><span class="sxs-lookup"><span data-stu-id="0f781-115">**Key**</span></span>|<span data-ttu-id="0f781-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0f781-116">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="0f781-117">MSIComponentID</span><span class="sxs-lookup"><span data-stu-id="0f781-117">MSIComponentID</span></span>  <br/> |<span data-ttu-id="0f781-118">Llama una categoría de Windows Installer PublishComponent identificador (GUID) que identifica el archivo DLL que se exporta simple MAPI o MAPI.</span><span class="sxs-lookup"><span data-stu-id="0f781-118">A Windows Installer PublishComponent category ID (GUID) that identifies the DLL that exports simple MAPI or MAPI calls.</span></span> <span data-ttu-id="0f781-119">Si esta clave, set tiene prioridad sobre la clave **DLLPath** o **DLLPathEx** .</span><span class="sxs-lookup"><span data-stu-id="0f781-119">If set, this key takes precedence over the **DLLPath** or **DLLPathEx** key.</span></span>  <br/> |
   |<span data-ttu-id="0f781-120">MSIApplicationLCID</span><span class="sxs-lookup"><span data-stu-id="0f781-120">MSIApplicationLCID</span></span>  <br/> |<span data-ttu-id="0f781-121">Identificador de configuración regional (LCID) para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0f781-121">Locale identifier (LCID) for your application.</span></span> <span data-ttu-id="0f781-122">La primera cadena de valor identifica una subclave de `HKLM\Software` y valores de cadena subsiguientes identifican los valores del Registro debajo de esta clave que contienen información de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="0f781-122">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key that contain locale information.</span></span>  <br/> |
   |<span data-ttu-id="0f781-123">MSIOfficeLCID</span><span class="sxs-lookup"><span data-stu-id="0f781-123">MSIOfficeLCID</span></span>  <br/> |<span data-ttu-id="0f781-124">LCID para Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="0f781-124">LCIDs for Microsoft Office.</span></span> <span data-ttu-id="0f781-125">La primera cadena de valor identifica una subclave de `HKLM\Software` y valores de cadena subsiguientes identifican los valores del Registro debajo de esta clave.</span><span class="sxs-lookup"><span data-stu-id="0f781-125">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key.</span></span>  <br/> |
   
   <span data-ttu-id="0f781-126">Obtener la información de estas claves.</span><span class="sxs-lookup"><span data-stu-id="0f781-126">Obtain the information from these keys.</span></span>
    
2. <span data-ttu-id="0f781-127">Pase los valores que obtuvo en el paso anterior a la función [FGetComponentPath](fgetcomponentpath.md) .</span><span class="sxs-lookup"><span data-stu-id="0f781-127">Pass the values that you obtained from the previous step to the [FGetComponentPath](fgetcomponentpath.md) function.</span></span> <span data-ttu-id="0f781-128">**FGetComponentPath** es una función que se exporta en la biblioteca de código auxiliar MAPI Mapistub.dll.</span><span class="sxs-lookup"><span data-stu-id="0f781-128">**FGetComponentPath** is a function that is exported by the MAPI stub library Mapistub.dll.</span></span> <span data-ttu-id="0f781-129">Devuelve la ruta de acceso de la versión personalizada de MAPI.</span><span class="sxs-lookup"><span data-stu-id="0f781-129">It returns the path of the custom version of MAPI.</span></span> 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a><span data-ttu-id="0f781-130">Para cargar la implementación de MAPI marcada como predeterminada</span><span class="sxs-lookup"><span data-stu-id="0f781-130">To load the implementation of MAPI marked as default</span></span>

1. <span data-ttu-id="0f781-131">Leer la `HKLM\Software\Clients\Mail::(default)` valor del registro.</span><span class="sxs-lookup"><span data-stu-id="0f781-131">Read the  `HKLM\Software\Clients\Mail::(default)` registry value.</span></span> 
    
2. <span data-ttu-id="0f781-132">Buscar la información para el cliente indicado tal y como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="0f781-132">Look up the information for the indicated client as described earlier.</span></span>
    
> [!NOTE]
> <span data-ttu-id="0f781-133">Tenga en cuenta que el cliente de correo predeterminado podría implementar MAPI extendida.</span><span class="sxs-lookup"><span data-stu-id="0f781-133">Note that the default mail client might not implement Extended MAPI.</span></span> 
  
#### <a name="example"></a><span data-ttu-id="0f781-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0f781-134">Example</span></span>

<span data-ttu-id="0f781-135">Para cargar MAPI tal como se implementa mediante Outlook, busque las claves del registro bajo `HKLM\Software\Clients\Mail\Microsoft Outlook` y páselos a **FGetComponentPath**.</span><span class="sxs-lookup"><span data-stu-id="0f781-135">To load MAPI as implemented by Outlook, look up the registry keys under  `HKLM\Software\Clients\Mail\Microsoft Outlook` and pass them to **FGetComponentPath**.</span></span> <span data-ttu-id="0f781-136">**FGetComponentPath** devolverá la ruta de acceso para la implementación de MAPI de Outlook.</span><span class="sxs-lookup"><span data-stu-id="0f781-136">**FGetComponentPath** will return the path for Outlook's implementation of MAPI.</span></span> 
  
<span data-ttu-id="0f781-137">Si no se establecen las claves **MSIComponentID**, **MSIApplicationLCID**y **MSIOfficeLCID** , compruebe el valor de registro **DLLPathEx** .</span><span class="sxs-lookup"><span data-stu-id="0f781-137">If the keys **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID** are not set, check the **DLLPathEx** registry value.</span></span> <span data-ttu-id="0f781-138">Si se establecen las claves, **FGetComponentPath** proporciona la ruta de acceso de implementación del cliente de MAPI.</span><span class="sxs-lookup"><span data-stu-id="0f781-138">If the keys are set, **FGetComponentPath** gives the path of the client's implementation of MAPI.</span></span> 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a><span data-ttu-id="0f781-139">Implementar el algoritmo de búsqueda de cliente de MAPI</span><span class="sxs-lookup"><span data-stu-id="0f781-139">Implementing the MAPI Client Lookup algorithm</span></span>

<span data-ttu-id="0f781-140">En la siguiente tabla se enumera las cuatro funciones de MFCMAPI que se usan para buscar la ruta de acceso para una implementación personalizada de MAPI:</span><span class="sxs-lookup"><span data-stu-id="0f781-140">The following table lists the four functions from MFCMAPI that are used to look up the path for a custom implementation of MAPI:</span></span>
  
|<span data-ttu-id="0f781-141">**Función**</span><span class="sxs-lookup"><span data-stu-id="0f781-141">**Function**</span></span>|<span data-ttu-id="0f781-142">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0f781-142">**Description**</span></span>|
|:-----|:-----|
| `GetMAPIPath` <br/> |<span data-ttu-id="0f781-143">Obtiene la ruta de acceso de la biblioteca MAPI.</span><span class="sxs-lookup"><span data-stu-id="0f781-143">Gets the MAPI library path.</span></span>  <br/> |
| `GetMailKey` <br/> |<span data-ttu-id="0f781-144">Obtiene la clave del registro de correo MAPI.</span><span class="sxs-lookup"><span data-stu-id="0f781-144">Gets the MAPI mail registry key.</span></span>  <br/> |
| `GetMapiMsiIds` <br/> |<span data-ttu-id="0f781-145">Obtiene el identificador de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="0f781-145">Gets the Windows Installer identifier.</span></span>  <br/> |
| `GetComponentPath` <br/> |<span data-ttu-id="0f781-146">Obtiene la ruta de acceso de componente con [FGetComponentPath](fgetcomponentpath.md).</span><span class="sxs-lookup"><span data-stu-id="0f781-146">Gets the component path using [FGetComponentPath](fgetcomponentpath.md).</span></span>  <br/> |
   
<span data-ttu-id="0f781-147">Debido a que MFCMAPI carga la implementación predeterminada de MAPI de forma predeterminada, si va a usar una implementación diferente de MAPI, debe dirigir explícitamente que lo haga.</span><span class="sxs-lookup"><span data-stu-id="0f781-147">Because MFCMAPI loads the default implementation of MAPI by default, if you want to use a different implementation of MAPI, you must explicitly direct it to do so.</span></span> <span data-ttu-id="0f781-148">Esto se realiza mediante el uso de la rutina de **MAPI Session\Load** .</span><span class="sxs-lookup"><span data-stu-id="0f781-148">This is performed by using the **Session\Load MAPI** routine.</span></span> 
  
### <a name="how-these-functions-work"></a><span data-ttu-id="0f781-149">Cómo funcionan estas funciones</span><span class="sxs-lookup"><span data-stu-id="0f781-149">How these functions work</span></span>

1. <span data-ttu-id="0f781-150">Las llamadas MFCMAPI `GetMAPIPath`, pasando NULL para el parámetro de cliente, para cargar la implementación de MAPI predeterminada.</span><span class="sxs-lookup"><span data-stu-id="0f781-150">MFCMAPI calls  `GetMAPIPath`, passing NULL for the client parameter, to load the default MAPI implementation.</span></span>
    
2.  <span data-ttu-id="0f781-151">`GetMAPIPath`las llamadas `GetMapiMsiIds` para leer los valores para **MSIComponentID**, **MSIApplicationLCID**y **MSIOfficeLCID**.</span><span class="sxs-lookup"><span data-stu-id="0f781-151">`GetMAPIPath` calls  `GetMapiMsiIds` to read the values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
3.  <span data-ttu-id="0f781-152">`GetMapiMsiIds`las llamadas `GetMailKey` para abrir la clave del registro para el cliente de correo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0f781-152">`GetMapiMsiIds` calls  `GetMailKey` to open the registry key for the default mail client.</span></span> 
    
4.  <span data-ttu-id="0f781-153">`GetMapiMsiIds`usa el identificador del registro devuelto por `GetMailKey` para buscar valores de **MSIComponentID**, **MSIApplicationLCID**y **MSIOfficeLCID**.</span><span class="sxs-lookup"><span data-stu-id="0f781-153">`GetMapiMsiIds` uses the registry handle returned by  `GetMailKey` to look up values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
5. <span data-ttu-id="0f781-154">Los valores para **MSIComponentID**, **MSIApplicationLCID**y **MSIOfficeLCID**, se devuelven a `GetMAPIPath`.</span><span class="sxs-lookup"><span data-stu-id="0f781-154">The values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**, are returned to  `GetMAPIPath`.</span></span>  <span data-ttu-id="0f781-155">`GetMAPIPath`a continuación, pasa a `GetComponentPath`.</span><span class="sxs-lookup"><span data-stu-id="0f781-155">`GetMAPIPath` then passes them to  `GetComponentPath`.</span></span>
    
6.  <span data-ttu-id="0f781-156">`GetComponentPath`carga la biblioteca de código auxiliar MAPI, Mapi32.dll, desde el directorio del sistema.</span><span class="sxs-lookup"><span data-stu-id="0f781-156">`GetComponentPath` loads the MAPI stub library, Mapi32.dll, from the system directory.</span></span> 
    
7.  <span data-ttu-id="0f781-157">`GetComponentPath`a continuación, se recupera la dirección de la función **FGetComponentPath** de Mapi32.dll, suponiendo que Mapi32.dll exporta **FGetComponentPath**.</span><span class="sxs-lookup"><span data-stu-id="0f781-157">`GetComponentPath` then retrieves the address of the **FGetComponentPath** function from Mapi32.dll, assuming that Mapi32.dll exports **FGetComponentPath**.</span></span>
    
8. <span data-ttu-id="0f781-158">Si obtiene la dirección de **FGetComponentPath** de Mapi32.dll se produce un error, `GetComponentPath` recupera la dirección de Mapistub.dll.</span><span class="sxs-lookup"><span data-stu-id="0f781-158">If getting the address of **FGetComponentPath** from Mapi32.dll fails,  `GetComponentPath` retrieves the address from Mapistub.dll.</span></span> 
    
9.  <span data-ttu-id="0f781-159">`GetComponentPath`a continuación, llama a **FGetComponentPath**, obtener la ruta de acceso de la versión predeterminada de MAPI.</span><span class="sxs-lookup"><span data-stu-id="0f781-159">`GetComponentPath` then calls **FGetComponentPath**, obtaining the path of the default version of MAPI.</span></span>
    
10.  <span data-ttu-id="0f781-160">`GetMAPIPath`a continuación, devuelve esta ruta de acceso para el autor de la llamada, que, a continuación, carga MAPI y se vincula explícitamente a él tal como se describe en el [vínculo a las funciones de MAPI](how-to-link-to-mapi-functions.md).</span><span class="sxs-lookup"><span data-stu-id="0f781-160">`GetMAPIPath` then returns this path to the caller, which then loads MAPI and explicitly links to it as described in [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="0f781-161">Para admitir copias localizados de MAPI para inglés y configuraciones regionales que no sean inglés, `GetMAPIPath` lee los valores de las subclaves de **MSIApplicationLCID** y **MSIOfficeLCID** .</span><span class="sxs-lookup"><span data-stu-id="0f781-161">To support localized copies of MAPI for English and non-English locales,  `GetMAPIPath` reads the values for the **MSIApplicationLCID** and **MSIOfficeLCID** subkeys.</span></span>  <span data-ttu-id="0f781-162">`GetMAPIPath`a continuación, llama a **FGetComponentPath**, especificando primero **MSIApplicationLCID** como **szQualifier**y vuelva a especificar **MSIOfficeLCID** como **szQualifier**.</span><span class="sxs-lookup"><span data-stu-id="0f781-162">`GetMAPIPath` then calls **FGetComponentPath**, first specifying **MSIApplicationLCID** as **szQualifier**, and again specifying **MSIOfficeLCID** as **szQualifier**.</span></span> <span data-ttu-id="0f781-163">Para obtener más información acerca de las claves del registro para los clientes de correo que admiten idiomas distintos del inglés, consulte [Configuración de las teclas de MSI para una DLL de MAPI](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="0f781-163">For more information about registry keys for mail clients that support non-English languages, see [Setting Up the MSI Keys for Your MAPI DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).</span></span>   
> - <span data-ttu-id="0f781-164">Si MFCMAPI no recibe una ruta de acceso para el uso de MAPI `GetMAPIPath`, que carga la biblioteca de código auxiliar MAPI desde el directorio del sistema.</span><span class="sxs-lookup"><span data-stu-id="0f781-164">If MFCMAPI does not receive a path for MAPI using  `GetMAPIPath`, it loads the MAPI stub library from the system directory.</span></span>
> - <span data-ttu-id="0f781-165">El valor de registro **MSMapiApps** tratado en [Explícitamente asignación de las llamadas MAPI a los archivos DLL de MAPI](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) sólo se aplica cuando se usa la biblioteca de código auxiliar de MAPI.</span><span class="sxs-lookup"><span data-stu-id="0f781-165">The **MSMapiApps** registry value discussed in [Explicitly Mapping MAPI Calls to MAPI DLLs](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) only applies when the MAPI Stub library is used.</span></span> <span data-ttu-id="0f781-166">Las aplicaciones que carga una implementación específica de MAPI o de carga de la implementación predeterminada no es necesario establecer la clave del registro **MSMapiApps** .</span><span class="sxs-lookup"><span data-stu-id="0f781-166">Applications that load a specific implementation of MAPI or load the default implementation do not have to set the **MSMapiApps** registry key.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="0f781-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f781-167">See also</span></span>

- [<span data-ttu-id="0f781-168">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="0f781-168">FGetComponentPath</span></span>](fgetcomponentpath.md)
- [<span data-ttu-id="0f781-169">Informaci�n general sobre programaci�n de MAPI</span><span class="sxs-lookup"><span data-stu-id="0f781-169">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="0f781-170">Vínculo a funciones MAPI</span><span class="sxs-lookup"><span data-stu-id="0f781-170">Link to MAPI Functions</span></span>](how-to-link-to-mapi-functions.md)
- [<span data-ttu-id="0f781-171">Configuración de Mapi32.dll código auxiliar del registro</span><span class="sxs-lookup"><span data-stu-id="0f781-171">Mapi32.dll Stub Registry Settings</span></span>](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [<span data-ttu-id="0f781-172">Configuración de las claves MSI para el archivo DLL de MAPI</span><span class="sxs-lookup"><span data-stu-id="0f781-172">Setting Up the MSI Keys for Your MAPI DLL</span></span>](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [<span data-ttu-id="0f781-173">Asignación explícitamente las llamadas MAPI a los archivos DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="0f781-173">Explicitly Mapping MAPI Calls to MAPI DLLs</span></span>](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)

