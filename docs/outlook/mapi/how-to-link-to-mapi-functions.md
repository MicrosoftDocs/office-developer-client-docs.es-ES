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
# <a name="link-to-mapi-functions"></a>Vínculo a funciones MAPI

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Hay tres métodos de vinculación: vinculación implícita, vinculación explícita y un nuevo modelo híbrido mediante la biblioteca de código auxiliar MAPI.
  
## <a name="implicit-linking"></a>Vinculación implícita

Históricamente, llamar a funciones MAPI en una aplicación de mensajería siempre implicaba vincularse a la biblioteca Mapi32.lib. Esto incluía el enrutamiento de llamadas MAPI a la biblioteca Windows código auxiliar MAPI, Mapi32.dll, que luego reenviaba las llamadas a la implementación de cliente MAPI predeterminada en tiempo de ejecución. Este proceso de llamada se conoce como vinculación implícita. El lado izquierdo de la siguiente figura muestra un ejemplo de vinculación implícita usada en un proceso de llamada de función MAPI. El proceso lo inicia una aplicación MAPI e implica la biblioteca MAPI (Mapi32.lib) y el código auxiliar MAPI de Windows (Mapi32.dll) y se completa con la implementación de cliente MAPI de Outlook del código auxiliar MAPI (Msmapi32.dll).
  
**Comparación de vínculos implícitos y explícitos.**

![Comparación de vinculación implícita y explícita](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparación de vínculos implícitos y explícitos")
  
## <a name="explicit-linking"></a>Vinculación explícita

Dado que el cliente MAPI predeterminado admite la instalación a petición mediante el instalador de Windows (MSI), puede desarrollar aplicaciones de mensajería directamente en el código auxiliar MAPI de Outlook en lugar de usar la biblioteca MAPI y Windows código auxiliar MAPI. El lado derecho de la figura anterior muestra un ejemplo de un proceso de llamada de función MAPI, empezando por una aplicación MAPI que busca la ruta de acceso y el nombre dll para el código auxiliar MAPI de Outlook (paso 2 en la sección siguiente) y realiza llamadas de función en el código auxiliar MAPI de Outlook (paso 3 en la sección siguiente). El siguiente procedimiento muestra cómo llamar a funciones MAPI mediante la vinculación explícita. 
  
> [!NOTE]
> Esta información sobre la vinculación explícita puede ser superflua para sus necesidades con la introducción de MAPIStubLibrary.lib que se describe en la sección siguiente. Al igual que el modelo implícito, la nueva biblioteca administra todo e implementa la lógica de vinculación explícita que carga directamente Outlook MAPI de Outlook. 
  
Para obtener más información acerca de la vinculación explícita, vea Vincular explícitamente.
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a>Para llamar a elementos de API MAPI sin la biblioteca MAPI y el código Windows código auxiliar MAPI

1. En el archivo de programa, cree una lista global de punteros de función para cada elemento de API MAPI que está usando. 
    
   En el ejemplo siguiente se muestra este paso.
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. Cree una función que inicialice funciones MAPI para vincular a la DLL MAPI del cliente MAPI predeterminado (por ejemplo, Msmapi32.dll de Microsoft Outlook). En esta función, haga lo siguiente: 
    
    1. Cargue mapi32.dll desde el directorio del sistema adecuado. 
        
       |||
       |:-----|:-----|
       |x64 o x86 de forma nativa  <br/> |**%windir%\system32\mapi32.dll** <br/> |
       |x86 en modo WoW  <br/> |**%windir%\syswow64\mapi32.dll** <br/> |
    
    2. Llame a [la función FGetComponentPath](fgetcomponentpath.md) para obtener la ruta de acceso y el nombre dll que implementa el subsistema MAPI. Para obtener más información, [vea Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).
        
    3. Cargue la DLL llamando a la función LoadLibrary. 
        
    4. Inicialice la matriz de punteros de función MAPI llamando a la función GetProcAddress. 
        
    En el ejemplo siguiente se muestran los pasos anteriores:
        
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

3. Por último, llama a la función que creaste en el paso 2 de la aplicación de mensajería antes de realizar llamadas a elementos de la API MAPI. 
    
   > [!CAUTION]
   > Debe desinicializar el subsistema MAPI antes de cerrar la aplicación. 
  
   En el siguiente ejemplo se muestra este paso: 
    
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

## <a name="mapistublibrarylib"></a>MAPIStubLibrary.lib

La llegada de MICROSOFT OUTLOOK 2010 y MAPI de 64 bits, que ahora se extienden al Microsoft Outlook 2013, requiere más que la API tradicional de 32 bits para la implementación completa. Un nuevo proyecto, la biblioteca auxiliar MAPI, publicado en el sitio web codeplex proporciona un reemplazo de entrega para Mapi32.lib que admite la creación de aplicaciones MAPI de 32 bits y 64 bits. MAPIStubLibrary.lib elimina la necesidad de vincular explícitamente a MAPI y, una vez creado, puede quitar Mapi32.lib de la configuración del vinculador, sustituyéndolo por MAPIStubLibrary.lib; no es necesario realizar más modificaciones en el código. También elimina la necesidad de escribir código **LoadLibrary,** **GetProcAddress** y **FreeLibrary** para controlar las exportaciones más recientes incluidas en este archivo de biblioteca, pero no en Mapi32.lib, que sería necesario si usaste la vinculación explícita. 
  
Algunas de las nuevas funciones vinculadas desde esta biblioteca que no están disponibles en Mapi32.lib incluyen las siguientes:
  
- [GetDefCachedMode](getdefcachedmode.md)    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)   
- [HrOpenOfflineObj](hropenofflineobj.md)    
- [MAPICrashRecovery](mapicrashrecovery.md)   
- [OpenStreamOnFileW](openstreamonfilew.md)    
- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)
    
Un método alternativo para incorporar la biblioteca auxiliar MAPI es copiar los archivos de origen, MapiStubLibrary.cpp y StubUtils.cpp, directamente en el proyecto y quitar cualquier vinculación a Mapi32.lib y cualquier código que se vincule explícitamente a MAPI.
  
Para obtener acceso a los archivos de biblioteca auxiliar MAPI y para obtener información sobre cómo compilarlo e integrarlo en el proyecto, así como preguntas sobre esta biblioteca, como cuándo y por qué usarla, vea la Biblioteca auxiliar [MAPI](https://mapistublibrary.codeplex.com/documentation) en el sitio codeplex. 
  
## <a name="see-also"></a>Vea también

- [Información general sobre programación de MAPI](mapi-programming-overview.md)
- [Instalar el subsistema MAPI](installing-the-mapi-subsystem.md)
- [Instalar archivos de encabezado MAPI](how-to-install-mapi-header-files.md)
- [Elegir una versión específica de MAPI para cargar](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [Determinación del método de vinculación que se va a usar](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [Vincular un archivo ejecutable a un archivo DLL](https://msdn.microsoft.com/library/9yd93633.aspx)
- [Configuración de las claves MSI para su DLL MAPI](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

