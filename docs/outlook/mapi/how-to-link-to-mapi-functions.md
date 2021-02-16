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
# <a name="link-to-mapi-functions"></a><span data-ttu-id="e39e8-103">Vínculo a funciones MAPI</span><span class="sxs-lookup"><span data-stu-id="e39e8-103">Link to MAPI functions</span></span>

<span data-ttu-id="e39e8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e39e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e39e8-105">Hay tres métodos de vinculación: vinculación implícita, vinculación explícita y un nuevo modelo híbrido mediante la biblioteca de códigos auxiliares MAPI.</span><span class="sxs-lookup"><span data-stu-id="e39e8-105">There are three methods of linking: implicit linking, explicit linking, and a new hybrid model using the MAPI Stub Library.</span></span>
  
## <a name="implicit-linking"></a><span data-ttu-id="e39e8-106">Vinculación implícita</span><span class="sxs-lookup"><span data-stu-id="e39e8-106">Implicit linking</span></span>

<span data-ttu-id="e39e8-107">Históricamente, llamar a funciones MAPI en una aplicación de mensajería siempre implicaba vincularse a la biblioteca Mapi32.lib.</span><span class="sxs-lookup"><span data-stu-id="e39e8-107">Historically, calling MAPI functions in a messaging application always involved linking to the Mapi32.lib library.</span></span> <span data-ttu-id="e39e8-108">Esto incluía el enrutamiento de llamadas MAPI a la biblioteca de códigos auxiliares mapi de Windows, Mapi32.dll, que luego reenviaba las llamadas a la implementación de cliente MAPI predeterminada en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="e39e8-108">This included routing MAPI calls to the Windows MAPI stub library, Mapi32.dll, which then forwarded the calls to the default MAPI client implementation at run time.</span></span> <span data-ttu-id="e39e8-109">Este proceso de llamada se conoce como vinculación implícita.</span><span class="sxs-lookup"><span data-stu-id="e39e8-109">This call process is known as implicit linking.</span></span> <span data-ttu-id="e39e8-110">En el lado izquierdo de la figura siguiente se muestra un ejemplo de vinculación implícita usada en un proceso de llamada de función MAPI.</span><span class="sxs-lookup"><span data-stu-id="e39e8-110">The left side of the following figure shows an example of implicit linking used in a MAPI function call process.</span></span> <span data-ttu-id="e39e8-111">El proceso se inicia mediante una aplicación MAPI e implica la biblioteca MAPI (Mapi32.lib) y el código auxiliar MAPI de Windows (Mapi32.dll) y se completa mediante la implementación del cliente MAPI de Outlook del código auxiliar MAPI (Msmapi32.dll).</span><span class="sxs-lookup"><span data-stu-id="e39e8-111">The process is initiated by a MAPI application and involves the MAPI library (Mapi32.lib) and the Windows MAPI stub (Mapi32.dll) and is completed by the Outlook MAPI client implementation of the MAPI stub (Msmapi32.dll).</span></span>
  
<span data-ttu-id="e39e8-112">**Comparación de vinculación implícita y explícita.**</span><span class="sxs-lookup"><span data-stu-id="e39e8-112">**Comparison of implicit and explicit linking.**</span></span>

<span data-ttu-id="e39e8-113">![Comparación de la comparación de vinculación]implícita y explícita(media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "de vinculación implícita y explícita")</span><span class="sxs-lookup"><span data-stu-id="e39e8-113">![Comparison of implicit and explicit linking](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparison of implicit and explicit linking")</span></span>
  
## <a name="explicit-linking"></a><span data-ttu-id="e39e8-114">Vinculación explícita</span><span class="sxs-lookup"><span data-stu-id="e39e8-114">Explicit linking</span></span>

<span data-ttu-id="e39e8-115">Dado que el cliente MAPI predeterminado admite la instalación a petición mediante Windows Installer (MSI), puede desarrollar aplicaciones de mensajería directamente en el código auxiliar MAPI de Outlook en lugar de usar la biblioteca MAPI y el código auxiliar MAPI de Windows.</span><span class="sxs-lookup"><span data-stu-id="e39e8-115">Because the default MAPI client supports on-demand installation using the Windows Installer (MSI), you can develop messaging applications directly on the Outlook MAPI stub instead of using the MAPI library and Windows MAPI stub.</span></span> <span data-ttu-id="e39e8-116">En el lado derecho de la figura anterior se muestra un ejemplo de un proceso de llamada de función MAPI, empezando por una aplicación MAPI que busca la ruta de acceso y el nombre dll para el código auxiliar MAPI de Outlook (paso 2 en la sección siguiente) y realiza llamadas de función en el código auxiliar MAPI de Outlook (paso 3 en la siguiente sección).</span><span class="sxs-lookup"><span data-stu-id="e39e8-116">The right side of the previous figure shows an example of a MAPI function call process, starting with a MAPI application looking for the path and DLL name for the Outlook MAPI stub (step 2 in the following section), and making function calls into the Outlook MAPI stub (step 3 in the following section).</span></span> <span data-ttu-id="e39e8-117">El siguiente procedimiento muestra cómo llamar a funciones MAPI mediante la vinculación explícita.</span><span class="sxs-lookup"><span data-stu-id="e39e8-117">The following procedure shows how to call MAPI functions by using explicit linking.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e39e8-118">Esta información sobre la vinculación explícita puede ser superflua para sus necesidades con la introducción de MAPIStubLibrary.lib que se describe en la siguiente sección.</span><span class="sxs-lookup"><span data-stu-id="e39e8-118">This information about explicit linking may be superfluous to your needs with the introduction of the MAPIStubLibrary.lib discussed in the following section.</span></span> <span data-ttu-id="e39e8-119">Al igual que el modelo implícito, la nueva biblioteca administra todo e implementa la lógica de vinculación explícita que carga mapi de Outlook directamente.</span><span class="sxs-lookup"><span data-stu-id="e39e8-119">Like the implicit model, the new library manages everything and implements the explicit linking logic that loads Outlook's MAPI directly.</span></span> 
  
<span data-ttu-id="e39e8-120">Para obtener más información acerca de la vinculación explícita, vea Vincular explícitamente.</span><span class="sxs-lookup"><span data-stu-id="e39e8-120">For more information about explicit linking, see Linking Explicitly.</span></span>
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a><span data-ttu-id="e39e8-121">Para llamar a elementos de la API de MAPI sin la biblioteca MAPI y el código auxiliar MAPI de Windows</span><span class="sxs-lookup"><span data-stu-id="e39e8-121">To call MAPI API elements without the MAPI library and the Windows MAPI stub</span></span>

1. <span data-ttu-id="e39e8-122">En el archivo de programa, cree una lista global de punteros de función para cada elemento de LA API MAPI que use.</span><span class="sxs-lookup"><span data-stu-id="e39e8-122">In your program file, create a global list of function pointers for each MAPI API element that you are using.</span></span> 
    
   <span data-ttu-id="e39e8-123">En el siguiente ejemplo se muestra este paso.</span><span class="sxs-lookup"><span data-stu-id="e39e8-123">The following example shows this step.</span></span>
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. <span data-ttu-id="e39e8-124">Cree una función que inicialice las funciones MAPI para vincular a la DLL de MAPI del cliente MAPI predeterminado (por ejemplo, Msmapi32.dll de Microsoft Outlook).</span><span class="sxs-lookup"><span data-stu-id="e39e8-124">Create a function that initializes MAPI functions to link to the MAPI DLL of the default MAPI client (for example, Msmapi32.dll of Microsoft Outlook).</span></span> <span data-ttu-id="e39e8-125">En esta función, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e39e8-125">In this function, do the following:</span></span> 
    
    1. <span data-ttu-id="e39e8-126">Cargue mapi32.dll desde el directorio del sistema adecuado.</span><span class="sxs-lookup"><span data-stu-id="e39e8-126">Load mapi32.dll from the appropriate system directory.</span></span> 
        
       |||
       |:-----|:-----|
       |<span data-ttu-id="e39e8-127">x64 o x86 de forma nativa</span><span class="sxs-lookup"><span data-stu-id="e39e8-127">x64 or x86 natively</span></span>  <br/> |<span data-ttu-id="e39e8-128">**%windir%\system32\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="e39e8-128">**%windir%\system32\mapi32.dll**</span></span> <br/> |
       |<span data-ttu-id="e39e8-129">x86 en modo WoW</span><span class="sxs-lookup"><span data-stu-id="e39e8-129">x86 on WoW mode</span></span>  <br/> |<span data-ttu-id="e39e8-130">**%windir%\syswow64\mapi32.dll**</span><span class="sxs-lookup"><span data-stu-id="e39e8-130">**%windir%\syswow64\mapi32.dll**</span></span> <br/> |
    
    2. <span data-ttu-id="e39e8-131">Llame a [la función FGetComponentPath](fgetcomponentpath.md) para obtener la ruta de acceso y el nombre de DLL que implementa el subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="e39e8-131">Call the [FGetComponentPath](fgetcomponentpath.md) function to get the path and DLL name that implements the MAPI subsystem.</span></span> <span data-ttu-id="e39e8-132">Para obtener más información, [vea Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span><span class="sxs-lookup"><span data-stu-id="e39e8-132">For more information, see [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span>
        
    3. <span data-ttu-id="e39e8-133">Cargue la DLL llamando a la función LoadLibrary.</span><span class="sxs-lookup"><span data-stu-id="e39e8-133">Load the DLL by calling the LoadLibrary function.</span></span> 
        
    4. <span data-ttu-id="e39e8-134">Inicialice la matriz de punteros de función MAPI llamando a la función GetProcAddress.</span><span class="sxs-lookup"><span data-stu-id="e39e8-134">Initialize the MAPI function pointer array by calling the GetProcAddress function.</span></span> 
        
    <span data-ttu-id="e39e8-135">En el siguiente ejemplo se muestran los pasos anteriores:</span><span class="sxs-lookup"><span data-stu-id="e39e8-135">The following example shows the previous steps:</span></span>
        
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

3. <span data-ttu-id="e39e8-136">Por último, llame a la función que creó en el paso 2 de la aplicación de mensajería antes de realizar llamadas a los elementos de la API mapi.</span><span class="sxs-lookup"><span data-stu-id="e39e8-136">Finally, call the function that you created in step 2 in your messaging application before you make calls to MAPI API elements.</span></span> 
    
   > [!CAUTION]
   > <span data-ttu-id="e39e8-137">Debe cancelar la inicialización del subsistema MAPI antes de cerrar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e39e8-137">You must uninitialize the MAPI subsystem before closing your application.</span></span> 
  
   <span data-ttu-id="e39e8-138">En el siguiente ejemplo se muestra este paso:</span><span class="sxs-lookup"><span data-stu-id="e39e8-138">The following example shows this step:</span></span> 
    
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

## <a name="mapistublibrarylib"></a><span data-ttu-id="e39e8-139">MAPIStubLibrary.lib</span><span class="sxs-lookup"><span data-stu-id="e39e8-139">MAPIStubLibrary.lib</span></span>

<span data-ttu-id="e39e8-140">La llegada de Microsoft Outlook 2010 y MAPI de 64 bits, que ahora se extiende a Microsoft Outlook 2013, requiere algo más que la API tradicional de 32 bits para la implementación completa.</span><span class="sxs-lookup"><span data-stu-id="e39e8-140">The advent of Microsoft Outlook 2010 and 64-bit MAPI, now extending to the Microsoft Outlook 2013, requires more than the traditional 32-bit API for full implementation.</span></span> <span data-ttu-id="e39e8-141">Un nuevo proyecto, la biblioteca de códigos auxiliares MAPI, publicado en el sitio web de CodePlex proporciona un reemplazo de lista desplegable para Mapi32.lib que admite la creación de aplicaciones MAPI de 32 bits y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e39e8-141">A new project, the MAPI Stub Library, posted on the CodePlex website provides a drop-in replacement for Mapi32.lib that supports building both 32-bit and 64-bit MAPI applications.</span></span> <span data-ttu-id="e39e8-142">MAPIStubLibrary.lib elimina la necesidad de vincular explícitamente a MAPI y, una vez creado, puede quitar Mapi32.lib de la configuración del vinculador, reemplazándose por MAPIStubLibrary.lib; no es necesario realizar más modificaciones en el código.</span><span class="sxs-lookup"><span data-stu-id="e39e8-142">MAPIStubLibrary.lib eliminates the need to explicitly link to MAPI, and having built it, you can remove Mapi32.lib from your linker settings, replacing it with MAPIStubLibrary.lib; no further modifications to your code should be needed.</span></span> <span data-ttu-id="e39e8-143">También elimina la necesidad de escribir código **LoadLibrary**, **GetProcAddress** y **FreeLibrary** para controlar las exportaciones más recientes incluidas en este archivo de biblioteca, pero no en Mapi32.lib, lo que sería necesario si usaste la vinculación explícita.</span><span class="sxs-lookup"><span data-stu-id="e39e8-143">It also eliminates the need to write **LoadLibrary**, **GetProcAddress**, and **FreeLibrary** code to handle newer exports included in this library file but not in Mapi32.lib, which would be needed if you used explicit linking.</span></span> 
  
<span data-ttu-id="e39e8-144">Algunas de las nuevas funciones vinculadas desde esta biblioteca que no están disponibles en Mapi32.lib incluyen lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e39e8-144">Some of the new functions linked from this library that are not available in Mapi32.lib include the following:</span></span>
  
- [<span data-ttu-id="e39e8-145">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="e39e8-145">GetDefCachedMode</span></span>](getdefcachedmode.md)    
- [<span data-ttu-id="e39e8-146">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="e39e8-146">HrGetGALFromEmsmdbUID</span></span>](hrgetgalfromemsmdbuid.md)   
- [<span data-ttu-id="e39e8-147">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="e39e8-147">HrOpenOfflineObj</span></span>](hropenofflineobj.md)    
- [<span data-ttu-id="e39e8-148">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="e39e8-148">MAPICrashRecovery</span></span>](mapicrashrecovery.md)   
- [<span data-ttu-id="e39e8-149">OpenStreamOnFileW</span><span class="sxs-lookup"><span data-stu-id="e39e8-149">OpenStreamOnFileW</span></span>](openstreamonfilew.md)    
- [<span data-ttu-id="e39e8-150">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="e39e8-150">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)
    
<span data-ttu-id="e39e8-151">Un método alternativo para incorporar la biblioteca de códigos auxiliares MAPI es copiar los archivos de origen, MapiStubLibrary.cpp y StubUtils.cpp, directamente en el proyecto y quitar cualquier vinculación a Mapi32.lib y cualquier código que se vincule explícitamente a MAPI.</span><span class="sxs-lookup"><span data-stu-id="e39e8-151">An alternate method of incorporating the MAPI Stub Library is to copy the source files, MapiStubLibrary.cpp and StubUtils.cpp, directly into your project and remove any linkage to Mapi32.lib and any code that explicitly links to MAPI.</span></span>
  
<span data-ttu-id="e39e8-152">Para obtener acceso a los archivos de la biblioteca de códigos auxiliares MAPI y para obtener información sobre cómo compilarlo e integrarlo en el proyecto, así como preguntas sobre esta biblioteca, como cuándo y por qué usarla, vea la biblioteca de códigos auxiliares [mapi](https://mapistublibrary.codeplex.com/documentation) en el sitio codeplex.</span><span class="sxs-lookup"><span data-stu-id="e39e8-152">To access the MAPI Stub Library files and for information about how to build and integrate it into your project, as well as questions about this library such as when and why to use it, see the [MAPI Stub Library](https://mapistublibrary.codeplex.com/documentation) on the CodePlex site.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e39e8-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="e39e8-153">See also</span></span>

- [<span data-ttu-id="e39e8-154">Información general sobre programación de MAPI</span><span class="sxs-lookup"><span data-stu-id="e39e8-154">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="e39e8-155">Instalar el subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="e39e8-155">Installing the MAPI Subsystem</span></span>](installing-the-mapi-subsystem.md)
- [<span data-ttu-id="e39e8-156">Instalar archivos de encabezado MAPI</span><span class="sxs-lookup"><span data-stu-id="e39e8-156">Install MAPI Header Files</span></span>](how-to-install-mapi-header-files.md)
- [<span data-ttu-id="e39e8-157">Elegir una versión específica de MAPI para cargar</span><span class="sxs-lookup"><span data-stu-id="e39e8-157">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [<span data-ttu-id="e39e8-158">Determinación del método de vinculación que se va a usar</span><span class="sxs-lookup"><span data-stu-id="e39e8-158">Determining Which Linking Method to Use</span></span>](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [<span data-ttu-id="e39e8-159">Vincular un archivo ejecutable a una DLL</span><span class="sxs-lookup"><span data-stu-id="e39e8-159">Linking an Executable to a DLL</span></span>](https://msdn.microsoft.com/library/9yd93633.aspx)
- [<span data-ttu-id="e39e8-160">Configuración de las claves MSI para la DLL de MAPI</span><span class="sxs-lookup"><span data-stu-id="e39e8-160">Setting Up the MSI Keys for Your MAPI DLL</span></span>](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

