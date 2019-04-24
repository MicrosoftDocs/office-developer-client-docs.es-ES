---
title: Vínculo a funciones MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be72a893-a3bc-4dea-8234-47f3e1db4515
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 71108da8bb9914bb7ed0ad0b3adacc24e1d69e63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346889"
---
# <a name="link-to-mapi-functions"></a><span data-ttu-id="bf73d-103">Vínculo a funciones MAPI</span><span class="sxs-lookup"><span data-stu-id="bf73d-103">Link to MAPI functions</span></span>

<span data-ttu-id="bf73d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf73d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf73d-105">Hay tres métodos de vinculación: vinculación implícita, vinculación explícita y un nuevo modelo híbrido mediante la biblioteca de código auxiliar de MAPI.</span><span class="sxs-lookup"><span data-stu-id="bf73d-105">There are three methods of linking: implicit linking, explicit linking, and a new hybrid model using the MAPI Stub Library.</span></span>
  
## <a name="implicit-linking"></a><span data-ttu-id="bf73d-106">Vinculación implícita</span><span class="sxs-lookup"><span data-stu-id="bf73d-106">Implicit linking</span></span>

<span data-ttu-id="bf73d-107">Históricamente, llamar a funciones MAPI en una aplicación de mensajería siempre implicaba vinculación a la biblioteca Mapi32. lib.</span><span class="sxs-lookup"><span data-stu-id="bf73d-107">Historically, calling MAPI functions in a messaging application always involved linking to the Mapi32.lib library.</span></span> <span data-ttu-id="bf73d-108">Esto incluyó las llamadas MAPI de enrutamiento a la biblioteca de código auxiliar MAPI de Windows, Mapi32. dll, que, a continuación, reenvía las llamadas a la implementación del cliente MAPI predeterminada en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="bf73d-108">This included routing MAPI calls to the Windows MAPI stub library, Mapi32.dll, which then forwarded the calls to the default MAPI client implementation at run time.</span></span> <span data-ttu-id="bf73d-109">Este proceso de llamada se conoce como vinculación implícita.</span><span class="sxs-lookup"><span data-stu-id="bf73d-109">This call process is known as implicit linking.</span></span> <span data-ttu-id="bf73d-110">En la parte izquierda de la figura siguiente se muestra un ejemplo de vinculación implícita usada en un proceso de llamada a una función MAPI.</span><span class="sxs-lookup"><span data-stu-id="bf73d-110">The left side of the following figure shows an example of implicit linking used in a MAPI function call process.</span></span> <span data-ttu-id="bf73d-111">El proceso se inicia mediante una aplicación MAPI e incluye la biblioteca MAPI (Mapi32. lib) y el código auxiliar MAPI de Windows (Mapi32. dll) y se completa mediante la implementación del cliente MAPI de Outlook del código auxiliar MAPI (Msmapi32. dll).</span><span class="sxs-lookup"><span data-stu-id="bf73d-111">The process is initiated by a MAPI application and involves the MAPI library (Mapi32.lib) and the Windows MAPI stub (Mapi32.dll) and is completed by the Outlook MAPI client implementation of the MAPI stub (Msmapi32.dll).</span></span>
  
<span data-ttu-id="bf73d-112">**Comparación de vínculos implícitos y explícitos.**</span><span class="sxs-lookup"><span data-stu-id="bf73d-112">**Comparison of implicit and explicit linking.**</span></span>

<span data-ttu-id="bf73d-113">![Comparación de vínculos implícitos y explícitos] (media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparación de vínculos implícitos y explícitos")</span><span class="sxs-lookup"><span data-stu-id="bf73d-113">![Comparison of implicit and explicit linking](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparison of implicit and explicit linking")</span></span>
  
## <a name="explicit-linking"></a><span data-ttu-id="bf73d-114">Vinculación explícita</span><span class="sxs-lookup"><span data-stu-id="bf73d-114">Explicit linking</span></span>

<span data-ttu-id="bf73d-115">Dado que el cliente MAPI predeterminado admite la instalación a petición mediante Windows Installer (MSI), puede desarrollar aplicaciones de mensajería directamente en el código auxiliar MAPI de Outlook, en lugar de usar la biblioteca MAPI y el código auxiliar MAPI de Windows.</span><span class="sxs-lookup"><span data-stu-id="bf73d-115">Because the default MAPI client supports on-demand installation using the Windows Installer (MSI), you can develop messaging applications directly on the Outlook MAPI stub instead of using the MAPI library and Windows MAPI stub.</span></span> <span data-ttu-id="bf73d-116">En el lado derecho de la figura anterior se muestra un ejemplo de un proceso de llamada a una función MAPI, comenzando con una aplicación MAPI que busca la ruta de acceso y el nombre de la DLL para el código auxiliar MAPI de Outlook (paso 2 de la siguiente sección) y realiza llamadas de función en el código auxiliar MAPI de Outlook ( Paso 3 de la sección siguiente).</span><span class="sxs-lookup"><span data-stu-id="bf73d-116">The right side of the previous figure shows an example of a MAPI function call process, starting with a MAPI application looking for the path and DLL name for the Outlook MAPI stub (step 2 in the following section), and making function calls into the Outlook MAPI stub (step 3 in the following section).</span></span> <span data-ttu-id="bf73d-117">El siguiente procedimiento muestra cómo llamar a las funciones MAPI mediante la vinculación explícita.</span><span class="sxs-lookup"><span data-stu-id="bf73d-117">The following procedure shows how to call MAPI functions by using explicit linking.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="bf73d-118">Esta información sobre la vinculación explícita puede ser superflua para sus necesidades con la introducción de MAPIStubLibrary. lib que se describe en la siguiente sección.</span><span class="sxs-lookup"><span data-stu-id="bf73d-118">This information about explicit linking may be superfluous to your needs with the introduction of the MAPIStubLibrary.lib discussed in the following section.</span></span> <span data-ttu-id="bf73d-119">Al igual que el modelo implícito, la nueva biblioteca administra todo e implementa la lógica de vinculación explícita que carga MAPI de Outlook directamente.</span><span class="sxs-lookup"><span data-stu-id="bf73d-119">Like the implicit model, the new library manages everything and implements the explicit linking logic that loads Outlook's MAPI directly.</span></span> 
  
<span data-ttu-id="bf73d-120">Para obtener más información sobre la vinculación explícita, vea vincular explícitamente.</span><span class="sxs-lookup"><span data-stu-id="bf73d-120">For more information about explicit linking, see Linking Explicitly.</span></span>
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a><span data-ttu-id="bf73d-121">Para llamar a elementos de la API MAPI sin la biblioteca MAPI y el código auxiliar MAPI de Windows</span><span class="sxs-lookup"><span data-stu-id="bf73d-121">To call MAPI API elements without the MAPI library and the Windows MAPI stub</span></span>

1. <span data-ttu-id="bf73d-122">En el archivo de programa, cree una lista global de punteros a funciones para cada elemento de la API de MAPI que use.</span><span class="sxs-lookup"><span data-stu-id="bf73d-122">In your program file, create a global list of function pointers for each MAPI API element that you are using.</span></span> 
    
   <span data-ttu-id="bf73d-123">En el ejemplo siguiente se muestra este paso.</span><span class="sxs-lookup"><span data-stu-id="bf73d-123">The following example shows this step.</span></span>
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. <span data-ttu-id="bf73d-124">Cree una función que inicialice las funciones MAPI para vincularlas a la DLL MAPI del cliente MAPI predeterminado (por ejemplo, Msmapi32. dll de Microsoft Outlook).</span><span class="sxs-lookup"><span data-stu-id="bf73d-124">Create a function that initializes MAPI functions to link to the MAPI DLL of the default MAPI client (for example, Msmapi32.dll of Microsoft Outlook).</span></span> <span data-ttu-id="bf73d-125">En esta función, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="bf73d-125">In this function, do the following:</span></span> 
    
    1. <span data-ttu-id="bf73d-126">Cargue Mapi32. dll desde el directorio del sistema adecuado.</span><span class="sxs-lookup"><span data-stu-id="bf73d-126">Load mapi32.dll from the appropriate system directory.</span></span> 
        
       |||
       |:-----|:-----|
       |<span data-ttu-id="bf73d-127">x64 o x86 de forma nativa</span><span class="sxs-lookup"><span data-stu-id="bf73d-127">x64 or x86 natively</span></span>  <br/> |<span data-ttu-id="bf73d-128">**%WINDIR%\system32\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="bf73d-128">**%windir%\system32\mapi32.dll**</span></span> <br/> |
       |<span data-ttu-id="bf73d-129">x86 en modo WoW</span><span class="sxs-lookup"><span data-stu-id="bf73d-129">x86 on WoW mode</span></span>  <br/> |<span data-ttu-id="bf73d-130">**%WINDIR%\syswow64\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="bf73d-130">**%windir%\syswow64\mapi32.dll**</span></span> <br/> |
    
    2. <span data-ttu-id="bf73d-131">Llame a la función [FGetComponentPath](fgetcomponentpath.md) para obtener la ruta de acceso y el nombre de dll que implementa el subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="bf73d-131">Call the [FGetComponentPath](fgetcomponentpath.md) function to get the path and DLL name that implements the MAPI subsystem.</span></span> <span data-ttu-id="bf73d-132">Para obtener más información, vea [elegir una versión específica de MAPI para cargar](how-to-choose-a-specific-version-of-mapi-to-load.md).</span><span class="sxs-lookup"><span data-stu-id="bf73d-132">For more information, see [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span>
        
    3. <span data-ttu-id="bf73d-133">Cargue el archivo DLL llamando a la función LoadLibrary.</span><span class="sxs-lookup"><span data-stu-id="bf73d-133">Load the DLL by calling the LoadLibrary function.</span></span> 
        
    4. <span data-ttu-id="bf73d-134">Para inicializar la matriz de punteros de función MAPI, llame a la función GetProcAddress.</span><span class="sxs-lookup"><span data-stu-id="bf73d-134">Initialize the MAPI function pointer array by calling the GetProcAddress function.</span></span> 
        
    <span data-ttu-id="bf73d-135">En el ejemplo siguiente se muestran los pasos anteriores:</span><span class="sxs-lookup"><span data-stu-id="bf73d-135">The following example shows the previous steps:</span></span>
        
   ```cpp
    void InitializeMapiFunctions()
    {
    {
        // Get the DLL path and name of the actual MAPI implementation.
        FGetComponentPath(g_szMapiComponentGUID, NULL, szMAPIDLL, MAX_PATH);
        // Load the DLL.
        hMod = LoadLibrary(szMAPIDLL);
        // Initialize MAPI functions.
        pfnMAPIInitialize = GetProcAddress(hMod, "MAPIInitialize");
        pfnMAPIUninitialize = GetProcAddress(hMod, "MAPIUninitialize");
    }
   ```

3. <span data-ttu-id="bf73d-136">Por último, llame a la función que creó en el paso 2 de la aplicación de mensajería antes de realizar llamadas a los elementos de la API de MAPI.</span><span class="sxs-lookup"><span data-stu-id="bf73d-136">Finally, call the function that you created in step 2 in your messaging application before you make calls to MAPI API elements.</span></span> 
    
   > [!CAUTION]
   > <span data-ttu-id="bf73d-137">Debe desinicializar el subsistema MAPI antes de cerrar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bf73d-137">You must uninitialize the MAPI subsystem before closing your application.</span></span> 
  
   <span data-ttu-id="bf73d-138">En el ejemplo siguiente se muestra este paso:</span><span class="sxs-lookup"><span data-stu-id="bf73d-138">The following example shows this step:</span></span> 
    
   ```cpp
    int main()
    {
        HRESULT hr;
        InitializeMapiFunctions();
        // Initialize the MAPI subsystem.
        hr = (*pfnMAPIInitialize)(NULL);
        if (hr!= S_OK)
        {
            // Handle the error case.
        }
        // Here is where you make calls to other MAPI interfaces.
        // Uninitialize the MAPI subsystem.
        (*pfnMAPIUninitialize)();
    return (0);
    }
   ```

## <a name="mapistublibrarylib"></a><span data-ttu-id="bf73d-139">MAPIStubLibrary. lib</span><span class="sxs-lookup"><span data-stu-id="bf73d-139">MAPIStubLibrary.lib</span></span>

<span data-ttu-id="bf73d-140">La llegada de Microsoft Outlook 2010 y 64 bits MAPI, que ahora se extiende a Microsoft Outlook 2013, requiere más que la API tradicional de 32 bits para una implementación completa.</span><span class="sxs-lookup"><span data-stu-id="bf73d-140">The advent of Microsoft Outlook 2010 and 64-bit MAPI, now extending to the Microsoft Outlook 2013, requires more than the traditional 32-bit API for full implementation.</span></span> <span data-ttu-id="bf73d-141">Un nuevo proyecto, la biblioteca de código auxiliar MAPI, que se publica en el sitio web de CodePlex, proporciona un reemplazo de buzón para Mapi32. lib que admite la creación de aplicaciones MAPI de 32-bit y de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="bf73d-141">A new project, the MAPI Stub Library, posted on the CodePlex website provides a drop-in replacement for Mapi32.lib that supports building both 32-bit and 64-bit MAPI applications.</span></span> <span data-ttu-id="bf73d-142">MAPIStubLibrary. lib elimina la necesidad de vincularse explícitamente a MAPI y, después de crearlo, puede quitar Mapi32. lib de la configuración del vinculador, reemplazándolo por MAPIStubLibrary. lib; no es necesario realizar más modificaciones en el código.</span><span class="sxs-lookup"><span data-stu-id="bf73d-142">MAPIStubLibrary.lib eliminates the need to explicitly link to MAPI, and having built it, you can remove Mapi32.lib from your linker settings, replacing it with MAPIStubLibrary.lib; no further modifications to your code should be needed.</span></span> <span data-ttu-id="bf73d-143">También elimina la necesidad de escribir código **LoadLibrary**, **GetProcAddress**y **FreeLibrary** para controlar las exportaciones más recientes incluidas en este archivo de biblioteca, pero no en Mapi32. lib, que serían necesarias si se usaba la vinculación explícita.</span><span class="sxs-lookup"><span data-stu-id="bf73d-143">It also eliminates the need to write **LoadLibrary**, **GetProcAddress**, and **FreeLibrary** code to handle newer exports included in this library file but not in Mapi32.lib, which would be needed if you used explicit linking.</span></span> 
  
<span data-ttu-id="bf73d-144">Entre las nuevas funciones vinculadas desde esta biblioteca que no están disponibles en Mapi32. lib se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="bf73d-144">Some of the new functions linked from this library that are not available in Mapi32.lib include the following:</span></span>
  
- [<span data-ttu-id="bf73d-145">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="bf73d-145">GetDefCachedMode</span></span>](getdefcachedmode.md)    
- [<span data-ttu-id="bf73d-146">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="bf73d-146">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)   
- [<span data-ttu-id="bf73d-147">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="bf73d-147">HrOpenOfflineObj</span></span>](hropenofflineobj.md)    
- [<span data-ttu-id="bf73d-148">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="bf73d-148">MAPICrashRecovery</span></span>](mapicrashrecovery.md)   
- [<span data-ttu-id="bf73d-149">OpenStreamOnFileW</span><span class="sxs-lookup"><span data-stu-id="bf73d-149">OpenStreamOnFileW</span></span>](openstreamonfilew.md)    
- [<span data-ttu-id="bf73d-150">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="bf73d-150">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)
    
<span data-ttu-id="bf73d-151">Un método alternativo para incorporar la biblioteca de código auxiliar de MAPI es copiar los archivos de origen, MapiStubLibrary. cpp y StubUtils. cpp, directamente en el proyecto y quitar cualquier vinculación a Mapi32. lib y cualquier código que se vincule explícitamente a MAPI.</span><span class="sxs-lookup"><span data-stu-id="bf73d-151">An alternate method of incorporating the MAPI Stub Library is to copy the source files, MapiStubLibrary.cpp and StubUtils.cpp, directly into your project and remove any linkage to Mapi32.lib and any code that explicitly links to MAPI.</span></span>
  
<span data-ttu-id="bf73d-152">Para obtener acceso a los archivos de la biblioteca de código auxiliar MAPI y obtener información sobre cómo compilarlo e integrarlo en el proyecto, así como preguntas sobre esta biblioteca, como Cuándo y por qué usarla, vea la [biblioteca de código auxiliar MAPI](https://mapistublibrary.codeplex.com/documentation) en el sitio codeplex.</span><span class="sxs-lookup"><span data-stu-id="bf73d-152">To access the MAPI Stub Library files and for information about how to build and integrate it into your project, as well as questions about this library such as when and why to use it, see the [MAPI Stub Library](https://mapistublibrary.codeplex.com/documentation) on the CodePlex site.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bf73d-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf73d-153">See also</span></span>

- [<span data-ttu-id="bf73d-154">Información general sobre programación de MAPI</span><span class="sxs-lookup"><span data-stu-id="bf73d-154">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="bf73d-155">Instalar el subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="bf73d-155">Installing the MAPI Subsystem</span></span>](installing-the-mapi-subsystem.md)
- [<span data-ttu-id="bf73d-156">Instalar los archivos de encabezado MAPI</span><span class="sxs-lookup"><span data-stu-id="bf73d-156">Install MAPI Header Files</span></span>](how-to-install-mapi-header-files.md)
- [<span data-ttu-id="bf73d-157">Elegir una versión específica de MAPI para cargar</span><span class="sxs-lookup"><span data-stu-id="bf73d-157">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [<span data-ttu-id="bf73d-158">Determinación del método de vinculación que se va a usar</span><span class="sxs-lookup"><span data-stu-id="bf73d-158">Determining Which Linking Method to Use</span></span>](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [<span data-ttu-id="bf73d-159">Vincular un ejecutable a un archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bf73d-159">Linking an Executable to a DLL</span></span>](https://msdn.microsoft.com/library/9yd93633.aspx)
- [<span data-ttu-id="bf73d-160">Configuración de las claves MSI para la DLL de MAPI</span><span class="sxs-lookup"><span data-stu-id="bf73d-160">Setting Up the MSI Keys for Your MAPI DLL</span></span>](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

