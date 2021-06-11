---
title: Elegir una versión específica de MAPI para cargar
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d353eba55e33b8ab48b3c47d2f31f1b5e0973b58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344523"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a><span data-ttu-id="5e626-103">Elegir una versión específica de MAPI para cargar</span><span class="sxs-lookup"><span data-stu-id="5e626-103">Choose a specific version of MAPI to load</span></span>

<span data-ttu-id="5e626-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e626-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e626-105">Al vincular explícitamente a una implementación de MAPI, debe seleccionar cuidadosamente qué implementación cargar.</span><span class="sxs-lookup"><span data-stu-id="5e626-105">When linking explicitly to an implementation of MAPI, you must carefully select which implementation to load.</span></span> 
  
<span data-ttu-id="5e626-106">Hay dos métodos para vincular explícitamente a una implementación de MAPI.</span><span class="sxs-lookup"><span data-stu-id="5e626-106">There are two methods to link explicitly to an implementation of MAPI.</span></span> 
  
1. <span data-ttu-id="5e626-107">Puede cargar la biblioteca de código auxiliar MAPI y especificar en el Registro una DLL personalizada a la que cargar y enviar llamadas MAPI.</span><span class="sxs-lookup"><span data-stu-id="5e626-107">You can load the MAPI stub library, and specify in the registry a custom DLL to load and dispatch MAPI calls to.</span></span>
    
2. <span data-ttu-id="5e626-108">Puede implementar el algoritmo de búsqueda de cliente MAPI para buscar la versión de MAPI usada por el cliente de correo predeterminado y cargarla.</span><span class="sxs-lookup"><span data-stu-id="5e626-108">You can implement the MAPI client lookup algorithm to look up the version of MAPI used by the default mail client and load it.</span></span>
    
<span data-ttu-id="5e626-109">Dado que puede [](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) cambiar elMapi32.dll registro de código auxiliar Configuración para que la aplicación use cualquier implementación de MAPI, le recomendamos que dirija a la aplicación a usar una implementación de MAPI con la que haya probado.</span><span class="sxs-lookup"><span data-stu-id="5e626-109">Because you can change the [Mapi32.dll Stub Registry Settings](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) to direct your application to use any implementation of MAPI, we recommend that you direct your application to use an implementation of MAPI that you have tested with.</span></span> <span data-ttu-id="5e626-110">A continuación se describen ambos métodos de vinculación explícitamente.</span><span class="sxs-lookup"><span data-stu-id="5e626-110">The following describes both methods of linking explicitly.</span></span> 
  
## <a name="reading-from-the-registry"></a><span data-ttu-id="5e626-111">Lectura desde el Registro</span><span class="sxs-lookup"><span data-stu-id="5e626-111">Reading from the registry</span></span>

### <a name="to-read-mapi-implementation-information-from-the-registry"></a><span data-ttu-id="5e626-112">Para leer la información de implementación mapi desde el Registro</span><span class="sxs-lookup"><span data-stu-id="5e626-112">To read MAPI implementation information from the registry</span></span>

1. <span data-ttu-id="5e626-113">Las claves del Registro que indican una DLL personalizada para un cliente de correo se encuentran bajo  `HKLM\Software\Clients\Mail` la clave del cliente de correo.</span><span class="sxs-lookup"><span data-stu-id="5e626-113">The registry keys that indicate a custom DLL for a mail client are located under the  `HKLM\Software\Clients\Mail` key of the mail client.</span></span> 
    
   <span data-ttu-id="5e626-114">En la tabla siguiente se describen estas claves:</span><span class="sxs-lookup"><span data-stu-id="5e626-114">The following table describes these keys:</span></span>
    
   |<span data-ttu-id="5e626-115">**Tecla**</span><span class="sxs-lookup"><span data-stu-id="5e626-115">**Key**</span></span>|<span data-ttu-id="5e626-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5e626-116">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="5e626-117">MSIComponentID</span><span class="sxs-lookup"><span data-stu-id="5e626-117">MSIComponentID</span></span>  <br/> |<span data-ttu-id="5e626-118">Un Windows de categoría PublishComponent (GUID) del instalador que identifica el DLL que exporta llamadas MAPI o MAPI sencillas.</span><span class="sxs-lookup"><span data-stu-id="5e626-118">A Windows Installer PublishComponent category ID (GUID) that identifies the DLL that exports simple MAPI or MAPI calls.</span></span> <span data-ttu-id="5e626-119">Si se establece, esta clave tiene prioridad sobre **la clave DLLPath** o **DLLPathEx.**</span><span class="sxs-lookup"><span data-stu-id="5e626-119">If set, this key takes precedence over the **DLLPath** or **DLLPathEx** key.</span></span>  <br/> |
   |<span data-ttu-id="5e626-120">MSIApplicationLCID</span><span class="sxs-lookup"><span data-stu-id="5e626-120">MSIApplicationLCID</span></span>  <br/> |<span data-ttu-id="5e626-121">Identificador de configuración regional (LCID) para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5e626-121">Locale identifier (LCID) for your application.</span></span> <span data-ttu-id="5e626-122">El primer valor de cadena identifica una subclave desde y los valores de cadena subsiguientes identifican los valores del Registro debajo de  `HKLM\Software` esta clave que contienen información de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="5e626-122">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key that contain locale information.</span></span>  <br/> |
   |<span data-ttu-id="5e626-123">MSIOfficeLCID</span><span class="sxs-lookup"><span data-stu-id="5e626-123">MSIOfficeLCID</span></span>  <br/> |<span data-ttu-id="5e626-124">LCID para Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="5e626-124">LCIDs for Microsoft Office.</span></span> <span data-ttu-id="5e626-125">El primer valor de cadena identifica una subclave desde y los valores de cadena subsiguientes identifican los valores  `HKLM\Software` del Registro debajo de esta clave.</span><span class="sxs-lookup"><span data-stu-id="5e626-125">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key.</span></span>  <br/> |
   
   <span data-ttu-id="5e626-126">Obtenga la información de estas claves.</span><span class="sxs-lookup"><span data-stu-id="5e626-126">Obtain the information from these keys.</span></span>
    
2. <span data-ttu-id="5e626-127">Pase los valores obtenidos del paso anterior a la [función FGetComponentPath.](fgetcomponentpath.md)</span><span class="sxs-lookup"><span data-stu-id="5e626-127">Pass the values that you obtained from the previous step to the [FGetComponentPath](fgetcomponentpath.md) function.</span></span> <span data-ttu-id="5e626-128">**FGetComponentPath es** una función exportada por la biblioteca de códigos auxiliares MAPI Mapistub.dll.</span><span class="sxs-lookup"><span data-stu-id="5e626-128">**FGetComponentPath** is a function that is exported by the MAPI stub library Mapistub.dll.</span></span> <span data-ttu-id="5e626-129">Devuelve la ruta de acceso de la versión personalizada de MAPI.</span><span class="sxs-lookup"><span data-stu-id="5e626-129">It returns the path of the custom version of MAPI.</span></span> 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a><span data-ttu-id="5e626-130">Para cargar la implementación de MAPI marcada como predeterminada</span><span class="sxs-lookup"><span data-stu-id="5e626-130">To load the implementation of MAPI marked as default</span></span>

1. <span data-ttu-id="5e626-131">Lea el  `HKLM\Software\Clients\Mail::(default)` valor del Registro.</span><span class="sxs-lookup"><span data-stu-id="5e626-131">Read the  `HKLM\Software\Clients\Mail::(default)` registry value.</span></span> 
    
2. <span data-ttu-id="5e626-132">Busque la información del cliente indicado como se describió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="5e626-132">Look up the information for the indicated client as described earlier.</span></span>
    
> [!NOTE]
> <span data-ttu-id="5e626-133">Tenga en cuenta que es posible que el cliente de correo predeterminado no implemente MAPI extendido.</span><span class="sxs-lookup"><span data-stu-id="5e626-133">Note that the default mail client might not implement Extended MAPI.</span></span> 
  
#### <a name="example"></a><span data-ttu-id="5e626-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5e626-134">Example</span></span>

<span data-ttu-id="5e626-135">Para cargar MAPI según lo implementado por Outlook, busque las claves del Registro en y pásenlas `HKLM\Software\Clients\Mail\Microsoft Outlook` a **FGetComponentPath**.</span><span class="sxs-lookup"><span data-stu-id="5e626-135">To load MAPI as implemented by Outlook, look up the registry keys under  `HKLM\Software\Clients\Mail\Microsoft Outlook` and pass them to **FGetComponentPath**.</span></span> <span data-ttu-id="5e626-136">**FGetComponentPath** devolverá la ruta de acceso para Outlook implementación de MAPI.</span><span class="sxs-lookup"><span data-stu-id="5e626-136">**FGetComponentPath** will return the path for Outlook's implementation of MAPI.</span></span> 
  
<span data-ttu-id="5e626-137">Si las claves **MSIComponentID,** **MSIApplicationLCID** y **MSIOfficeLCID** no están establecidas, compruebe el valor del Registro **DLLPathEx.**</span><span class="sxs-lookup"><span data-stu-id="5e626-137">If the keys **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID** are not set, check the **DLLPathEx** registry value.</span></span> <span data-ttu-id="5e626-138">Si se establecen las claves, **FGetComponentPath** proporciona la ruta de acceso de la implementación del cliente de MAPI.</span><span class="sxs-lookup"><span data-stu-id="5e626-138">If the keys are set, **FGetComponentPath** gives the path of the client's implementation of MAPI.</span></span> 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a><span data-ttu-id="5e626-139">Implementación del algoritmo de búsqueda de cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="5e626-139">Implementing the MAPI Client Lookup algorithm</span></span>

<span data-ttu-id="5e626-140">En la tabla siguiente se enumeran las cuatro funciones de MFCMAPI que se usan para buscar la ruta de acceso de una implementación personalizada de MAPI:</span><span class="sxs-lookup"><span data-stu-id="5e626-140">The following table lists the four functions from MFCMAPI that are used to look up the path for a custom implementation of MAPI:</span></span>
  
|<span data-ttu-id="5e626-141">**Función**</span><span class="sxs-lookup"><span data-stu-id="5e626-141">**Function**</span></span>|<span data-ttu-id="5e626-142">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5e626-142">**Description**</span></span>|
|:-----|:-----|
| `GetMAPIPath` <br/> |<span data-ttu-id="5e626-143">Obtiene la ruta de acceso de la biblioteca MAPI.</span><span class="sxs-lookup"><span data-stu-id="5e626-143">Gets the MAPI library path.</span></span>  <br/> |
| `GetMailKey` <br/> |<span data-ttu-id="5e626-144">Obtiene la clave del Registro de correo MAPI.</span><span class="sxs-lookup"><span data-stu-id="5e626-144">Gets the MAPI mail registry key.</span></span>  <br/> |
| `GetMapiMsiIds` <br/> |<span data-ttu-id="5e626-145">Obtiene el identificador Windows installer.</span><span class="sxs-lookup"><span data-stu-id="5e626-145">Gets the Windows Installer identifier.</span></span>  <br/> |
| `GetComponentPath` <br/> |<span data-ttu-id="5e626-146">Obtiene la ruta de acceso del componente [mediante FGetComponentPath](fgetcomponentpath.md).</span><span class="sxs-lookup"><span data-stu-id="5e626-146">Gets the component path using [FGetComponentPath](fgetcomponentpath.md).</span></span>  <br/> |
   
<span data-ttu-id="5e626-147">Dado que MFCMAPI carga la implementación predeterminada de MAPI de forma predeterminada, si desea usar una implementación diferente de MAPI, debe dirigirla explícitamente para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="5e626-147">Because MFCMAPI loads the default implementation of MAPI by default, if you want to use a different implementation of MAPI, you must explicitly direct it to do so.</span></span> <span data-ttu-id="5e626-148">Esto se realiza mediante la **rutina Session\Load MAPI.**</span><span class="sxs-lookup"><span data-stu-id="5e626-148">This is performed by using the **Session\Load MAPI** routine.</span></span> 
  
### <a name="how-these-functions-work"></a><span data-ttu-id="5e626-149">Cómo funcionan estas funciones</span><span class="sxs-lookup"><span data-stu-id="5e626-149">How these functions work</span></span>

1. <span data-ttu-id="5e626-150">MFCMAPI llama  `GetMAPIPath` , pasando NULL para el parámetro de cliente, para cargar la implementación MAPI predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5e626-150">MFCMAPI calls  `GetMAPIPath`, passing NULL for the client parameter, to load the default MAPI implementation.</span></span>
    
2.  <span data-ttu-id="5e626-151">`GetMAPIPath` llamadas  `GetMapiMsiIds` para leer los valores de **MSIComponentID,** **MSIApplicationLCID** y **MSIOfficeLCID**.</span><span class="sxs-lookup"><span data-stu-id="5e626-151">`GetMAPIPath` calls  `GetMapiMsiIds` to read the values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
3.  <span data-ttu-id="5e626-152">`GetMapiMsiIds` llamadas  `GetMailKey` para abrir la clave del Registro para el cliente de correo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5e626-152">`GetMapiMsiIds` calls  `GetMailKey` to open the registry key for the default mail client.</span></span> 
    
4.  <span data-ttu-id="5e626-153">`GetMapiMsiIds` usa el controlador del Registro devuelto por para buscar valores  `GetMailKey` para **MSIComponentID,** **MSIApplicationLCID** y **MSIOfficeLCID**.</span><span class="sxs-lookup"><span data-stu-id="5e626-153">`GetMapiMsiIds` uses the registry handle returned by  `GetMailKey` to look up values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
5. <span data-ttu-id="5e626-154">Los valores de **MSIComponentID,** **MSIApplicationLCID** y **MSIOfficeLCID**, se devuelven a  `GetMAPIPath` .</span><span class="sxs-lookup"><span data-stu-id="5e626-154">The values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**, are returned to  `GetMAPIPath`.</span></span>  <span data-ttu-id="5e626-155">`GetMAPIPath` a continuación, los pasa a  `GetComponentPath` .</span><span class="sxs-lookup"><span data-stu-id="5e626-155">`GetMAPIPath` then passes them to  `GetComponentPath`.</span></span>
    
6.  <span data-ttu-id="5e626-156">`GetComponentPath` carga la biblioteca de código auxiliar MAPI, Mapi32.dll, desde el directorio del sistema.</span><span class="sxs-lookup"><span data-stu-id="5e626-156">`GetComponentPath` loads the MAPI stub library, Mapi32.dll, from the system directory.</span></span> 
    
7.  <span data-ttu-id="5e626-157">`GetComponentPath` a continuación, recupera la dirección de la función **FGetComponentPath** desde Mapi32.dll, suponiendo que Mapi32.dll exporta **FGetComponentPath**.</span><span class="sxs-lookup"><span data-stu-id="5e626-157">`GetComponentPath` then retrieves the address of the **FGetComponentPath** function from Mapi32.dll, assuming that Mapi32.dll exports **FGetComponentPath**.</span></span>
    
8. <span data-ttu-id="5e626-158">Si se produce un error al obtener la dirección de **FGetComponentPath** Mapi32.dll, recupera  `GetComponentPath` la dirección de Mapistub.dll.</span><span class="sxs-lookup"><span data-stu-id="5e626-158">If getting the address of **FGetComponentPath** from Mapi32.dll fails,  `GetComponentPath` retrieves the address from Mapistub.dll.</span></span> 
    
9.  <span data-ttu-id="5e626-159">`GetComponentPath` a continuación, **llama a FGetComponentPath**, obteniendo la ruta de acceso de la versión predeterminada de MAPI.</span><span class="sxs-lookup"><span data-stu-id="5e626-159">`GetComponentPath` then calls **FGetComponentPath**, obtaining the path of the default version of MAPI.</span></span>
    
10.  <span data-ttu-id="5e626-160">`GetMAPIPath` a continuación, devuelve esta ruta de acceso al autor de la llamada, que luego carga MAPI y se vincula explícitamente a ella como se describe [en Vínculo a funciones MAPI](how-to-link-to-mapi-functions.md).</span><span class="sxs-lookup"><span data-stu-id="5e626-160">`GetMAPIPath` then returns this path to the caller, which then loads MAPI and explicitly links to it as described in [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="5e626-161">Para admitir copias localizadas de MAPI para configuraciones regionales en inglés y no inglesas, lee los valores de las `GetMAPIPath` subclaves **MSIApplicationLCID** y **MSIOfficeLCID.**</span><span class="sxs-lookup"><span data-stu-id="5e626-161">To support localized copies of MAPI for English and non-English locales,  `GetMAPIPath` reads the values for the **MSIApplicationLCID** and **MSIOfficeLCID** subkeys.</span></span>  <span data-ttu-id="5e626-162">`GetMAPIPath` a continuación, llama **a FGetComponentPath**, primero especifica **MSIApplicationLCID** como **szQualifier** y, de nuevo, especifica **MSIOfficeLCID** **como szQualifier**.</span><span class="sxs-lookup"><span data-stu-id="5e626-162">`GetMAPIPath` then calls **FGetComponentPath**, first specifying **MSIApplicationLCID** as **szQualifier**, and again specifying **MSIOfficeLCID** as **szQualifier**.</span></span> <span data-ttu-id="5e626-163">Para obtener más información acerca de las claves del Registro para clientes de correo que admiten idiomas que no son inglés, vea [Setting Up the MSI Keys for Your MAPI DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5e626-163">For more information about registry keys for mail clients that support non-English languages, see [Setting Up the MSI Keys for Your MAPI DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).</span></span>   
> - <span data-ttu-id="5e626-164">Si MFCMAPI no recibe una ruta de acceso para MAPI mediante , carga la biblioteca de código  `GetMAPIPath` auxiliar MAPI desde el directorio del sistema.</span><span class="sxs-lookup"><span data-stu-id="5e626-164">If MFCMAPI does not receive a path for MAPI using  `GetMAPIPath`, it loads the MAPI stub library from the system directory.</span></span>
> - <span data-ttu-id="5e626-165">El valor del Registro **MSMapiApps** que se describe en [Asignación](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) explícita de llamadas MAPI a DLL MAPI solo se aplica cuando se usa la biblioteca auxiliar MAPI.</span><span class="sxs-lookup"><span data-stu-id="5e626-165">The **MSMapiApps** registry value discussed in [Explicitly Mapping MAPI Calls to MAPI DLLs](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) only applies when the MAPI Stub library is used.</span></span> <span data-ttu-id="5e626-166">Las aplicaciones que cargan una implementación específica de MAPI o cargan la implementación predeterminada no tienen que establecer la clave del Registro **MSMapiApps.**</span><span class="sxs-lookup"><span data-stu-id="5e626-166">Applications that load a specific implementation of MAPI or load the default implementation do not have to set the **MSMapiApps** registry key.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="5e626-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e626-167">See also</span></span>

- [<span data-ttu-id="5e626-168">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="5e626-168">FGetComponentPath</span></span>](fgetcomponentpath.md)
- [<span data-ttu-id="5e626-169">Información general sobre programación de MAPI</span><span class="sxs-lookup"><span data-stu-id="5e626-169">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="5e626-170">Vínculo a funciones MAPI</span><span class="sxs-lookup"><span data-stu-id="5e626-170">Link to MAPI Functions</span></span>](how-to-link-to-mapi-functions.md)
- [<span data-ttu-id="5e626-171">Mapi32.dll registro de código auxiliar Configuración</span><span class="sxs-lookup"><span data-stu-id="5e626-171">Mapi32.dll Stub Registry Settings</span></span>](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [<span data-ttu-id="5e626-172">Configuración de las claves MSI para su DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="5e626-172">Setting Up the MSI Keys for Your MAPI DLL</span></span>](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [<span data-ttu-id="5e626-173">Asignación explícita de llamadas MAPI a DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="5e626-173">Explicitly Mapping MAPI Calls to MAPI DLLs</span></span>](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)

