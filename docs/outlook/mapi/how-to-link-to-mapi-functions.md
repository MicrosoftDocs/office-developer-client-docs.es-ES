---
title: Vínculo a funciones de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be72a893-a3bc-4dea-8234-47f3e1db4515
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5cb791d0d350a04864191a0a9d35a2f1c8b165d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577719"
---
# <a name="link-to-mapi-functions"></a>Vínculo a funciones de MAPI

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Hay tres métodos de vinculación: vinculación implícita, vinculación explícita y un nuevo modelo híbrido mediante la biblioteca de código auxiliar de MAPI.
  
## <a name="implicit-linking"></a>Vinculación implícita

Tradicionalmente, llamar a funciones de MAPI en una aplicación de mensajería siempre había involucrado vinculación a la biblioteca de Mapi32.lib. Esto incluye enrutar las llamadas MAPI a la biblioteca de código auxiliar de Windows MAPI, Mapi32.dll, que, a continuación, reenvía las llamadas a la implementación del cliente MAPI predeterminada en tiempo de ejecución. Este proceso de llamada se conoce como la vinculación implícita. El lado izquierdo de la siguiente ilustración muestra un ejemplo de vinculación implícita utiliza en un proceso de llamada de función MAPI. El proceso se inicia una aplicación de MAPI e implica la biblioteca MAPI (Mapi32.lib) y el código auxiliar de MAPI de Windows (Mapi32.dll) y se haya completado la implementación del cliente MAPI de Outlook del código auxiliar MAPI (Msmapi32.dll).
  
**Comparación de Vinculaciones implícitas y explícitas.**

![Comparación de Vinculaciones implícitas y explícitas] (media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "Comparación de Vinculaciones implícitas y explícitas")
  
## <a name="explicit-linking"></a>Vinculación explícita

Debido a que el cliente MAPI predeterminado es compatible con la instalación a petición mediante Windows Installer (MSI), puede desarrollar aplicaciones de mensajería directamente en el código auxiliar de MAPI de Outlook en lugar de usar la biblioteca MAPI y el código auxiliar de MAPI de Windows. El lado derecho de la ilustración anterior muestra un ejemplo de un proceso de llamada de función MAPI, empezando por una aplicación MAPI busca la ruta de acceso y el nombre de archivo DLL para el código auxiliar de MAPI de Outlook (paso 2 en la siguiente sección) y realizar llamadas de función en el código auxiliar de MAPI de Outlook) paso 3 en la siguiente sección). El procedimiento siguiente muestra cómo llamar a funciones de MAPI mediante vinculación explícita. 
  
> [!NOTE]
> Esta información acerca de la vinculación explícita puede ser superflua para sus necesidades con la introducción de la MAPIStubLibrary.lib descrita en la sección siguiente. Al igual que el modelo implícito, la nueva biblioteca de administra todo el contenido e implementa la lógica de vinculación explícita que se carga de Outlook MAPI directamente. 
  
Para obtener más información acerca de la vinculación explícita, vea vinculación de forma explícita.
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a>Para llamar a los elementos de la API de MAPI sin la biblioteca MAPI y el código auxiliar de MAPI de Windows

1. En el archivo de programa, cree una lista global de punteros a función para cada elemento de la API de MAPI que va a usar. 
    
   En el ejemplo siguiente se muestra este paso.
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. Crear una función que inicializa las funciones MAPI para vincular a la DLL de MAPI del cliente MAPI predeterminado (por ejemplo, Msmapi32.dll de Microsoft Outlook). En esta función, haga lo siguiente: 
    
    1. Cargar mapi32.dll desde el directorio de sistema adecuado. 
        
       |||
       |:-----|:-----|
       |x64 o x86 forma nativa  <br/> |**%windir%\system32\mapi32.dll** <br/> |
       |x86 en modo WoW  <br/> |**%windir%\syswow64\mapi32.dll** <br/> |
    
    2. Llame a la función [FGetComponentPath](fgetcomponentpath.md) para obtener la ruta de acceso y el nombre de archivo DLL que implementa el subsistema MAPI. Para obtener más información, vea [Elegir una versión específica de MAPI para carga](how-to-choose-a-specific-version-of-mapi-to-load.md).
        
    3. Cargar el archivo DLL mediante una llamada a la función LoadLibrary. 
        
    4. Inicializar la matriz de puntero de función MAPI mediante una llamada a la función de GetProcAddress. 
        
    El ejemplo siguiente muestra los pasos anteriores:
        
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

3. Por último, llame a la función que ha creado en el paso 2 en su aplicación de mensajería antes de realizar llamadas a los elementos de la API de MAPI. 
    
   > [!CAUTION]
   > Debe cancelar la inicialización del subsistema MAPI antes de cerrar la aplicación. 
  
   En el ejemplo siguiente se muestra este paso: 
    
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

La llegada de Microsoft Outlook 2010 y MAPI de 64 bits, ahora extender en Microsoft Outlook 2013, se requiere más que la API de 32 bits tradicional para la implementación completa. Un nuevo proyecto, la biblioteca de código auxiliar de MAPI, registrado en el sitio Web de CodePlex proporciona un reemplazo de orden para Mapi32.lib que admita la generación de aplicaciones de MAPI de 32 bits y 64 bits. MAPIStubLibrary.lib elimina la necesidad de vincularse explícitamente a MAPI y tener creado, puede quitar Mapi32.lib de la configuración del vinculador, reemplazando con MAPIStubLibrary.lib; debe ser necesaria ninguna modificación adicional al código. También se elimina la necesidad de escribir código **LoadLibrary**, **GetProcAddress**y **FreeLibrary** para controlar las exportaciones más reciente incluidas en este archivo de la biblioteca, pero no en Mapi32.lib, que se necesitaría si usó la vinculación explícita. 
  
Algunas de las nuevas funciones vinculadas desde esta biblioteca que no están disponibles en Mapi32.lib incluyen lo siguiente:
  
- [GetDefCachedMode](getdefcachedmode.md)    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)   
- [HrOpenOfflineObj](hropenofflineobj.md)    
- [MAPICrashRecovery](mapicrashrecovery.md)   
- [OpenStreamOnFileW](openstreamonfilew.md)    
- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)
    
Es un método alternativo de la incorporación de la biblioteca de código auxiliar de MAPI copiar los archivos de origen, MapiStubLibrary.cpp y StubUtils.cpp, directamente en el proyecto y quitar cualquier vinculaciones a Mapi32.lib y cualquier código que se vincula explícitamente a MAPI.
  
Para obtener acceso a los archivos de biblioteca de código auxiliar de MAPI y para obtener información acerca de cómo crear e integrarla en su proyecto, así como preguntas acerca de esta biblioteca, como cuándo y por qué usarla, consulte la [Biblioteca de código auxiliar de MAPI](http://mapistublibrary.codeplex.com/documentation) en el sitio de CodePlex. 
  
## <a name="see-also"></a>Recursos adicionales

- [Informaci�n general sobre programaci�n de MAPI](mapi-programming-overview.md)
- [Instalar el subsistema MAPI](installing-the-mapi-subsystem.md)
- [Instalar los archivos de encabezado MAPI](how-to-install-mapi-header-files.md)
- [Elegir una versión específica de MAPI para cargar](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [Determinar qué método de vinculación de uso](http://msdn.microsoft.com/en-us/library/253b8k2c.aspx)
- [Vincular un ejecutable a un archivo DLL](http://msdn.microsoft.com/en-us/library/9yd93633.aspx)
- [Configuración de las claves MSI para el archivo DLL de MAPI](http://msdn.microsoft.com/en-us/library/ee909494%28v=VS.85%29.aspx)

