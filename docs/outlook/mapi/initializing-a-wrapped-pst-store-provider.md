---
title: Inicializar un proveedor de almacén de archivos PST ajustado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 07633717-ba4c-b146-ad65-60b37ab98ab6
description: 'Última modificación: 05 de octubre de 2012'
ms.openlocfilehash: a332c63814163579d5fe8ab365145e9583fa6c97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817834"
---
# <a name="initializing-a-wrapped-pst-store-provider"></a>Inicializar un proveedor de almacén de archivos PST ajustado

**Se aplica a**: Outlook 
  
Para implementar un proveedor de almacén de archivo (.pst) de carpetas personales ajustado, deben inicializar el proveedor de almacén de archivos PST ajustado mediante el uso de la función **[MSProviderInit](msproviderinit.md)** como un punto de entrada. Después de que se inicialice la DLL del proveedor, la función **[MSGSERVICEENTRY](msgserviceentry.md)** configura el proveedor de almacén de archivos PST ajustado. 
  
En este tema, se muestran la función **MSProviderInit** y la función **MSGSERVICEENTRY** mediante el uso de los ejemplos de código desde el proveedor de almacén de archivos PST ajustado de ejemplo. En el ejemplo se implementa un proveedor de PST ajustado que está pensado para usarse junto con la API de replicación. Para obtener más información sobre cómo descargar e instalar al proveedor de almacén de archivos PST ajustado de ejemplo, vea [instalar el proveedor de almacén de archivos PST ajustado de ejemplo](installing-the-sample-wrapped-pst-store-provider.md). Para obtener más información acerca de la API de replicación, vea [Acerca de la API de replicación](about-the-replication-api.md).
  
Después de inicializar un proveedor de almacén de archivos PST ajustado, debe implementar funciones de modo que pueden iniciar sesión en el proveedor de almacén de mensajes MAPI y la cola de MAPI. Para obtener más información, vea [Registro en a un proveedor de almacén de archivos PST ajustado](logging-on-to-a-wrapped-pst-store-provider.md).
  
## <a name="initialization-routine"></a>Rutina de inicialización

Todos los proveedores de almacén de archivos PST ajustados deben implementar la función **[MSProviderInit](msproviderinit.md)** como un punto de entrada para inicializar la DLL del proveedor. **MSProviderInit** comprueba si el número de versión de la interfaz de proveedor de servicio, `ulMAPIVer`, es compatible con el número de versión actual, `CURRENT_SPI_VERSION`. La función guarda la memoria MAPI de rutinas de administración en el `g_lpAllocateBuffer`, `g_lpAllocateMore`, y `g_lpFreeBuffer` parámetros. Estas rutinas de administración de memoria se deben usar durante la implementación de almacén de archivos PST ajustada para la asignación y cancelación de asignación de memoria. 
  
### <a name="msproviderinit-example"></a>Ejemplo de MSProviderInit()

```cpp
STDINITMETHODIMP MSProviderInit ( 
    HINSTANCE /*hInstance*/, 
    LPMALLOC lpMalloc, 
    LPALLOCATEBUFFER lpAllocateBuffer, 
    LPALLOCATEMORE lpAllocateMore, 
    LPFREEBUFFER lpFreeBuffer, 
    ULONG ulFlags, 
    ULONG ulMAPIVer, 
    ULONG FAR * lpulProviderVer, 
    LPMSPROVIDER FAR * lppMSProvider) 
{ 
    Log(true,"MSProviderInit function called\n"); 
    if (!lppMSProvider || !lpulProviderVer) return MAPI_E_INVALID_PARAMETER; 
    HRESULT hRes = S_OK; 
 
    *lppMSProvider = NULL; 
    *lpulProviderVer = CURRENT_SPI_VERSION; 
    if (ulMAPIVer < CURRENT_SPI_VERSION) 
    { 
        Log(true,"MSProviderInit: The version of the subsystem cannot handle this" 
            + "version of the provider\n"); 
        return MAPI_E_VERSION; 
    } 
 
    Log(true,"MSProviderInit: saving off memory management routines\n"); 
    g_lpAllocateBuffer = lpAllocateBuffer; 
    g_lpAllocateMore = lpAllocateMore; 
    g_lpFreeBuffer = lpFreeBuffer; 
    HMODULE hm = LoadLibrary("C:\\Program Files\\Common Files\\System" + 
        "\\MSMAPI\\1033\\MSPST32.dll" ); 
    if (!hm) hm = LoadLibrary("C:\\Program Files\\Microsoft Office\\Office12" + 
        "\\MSPST32.dll" ); 
    Log(true,"LoadLibrary returned 0x%08X\n", hm); 
 
    LPMSPROVIDERINIT pMsProviderInit = NULL; 
    if (hm) 
    { 
        pMsProviderInit = (LPMSPROVIDERINIT)GetProcAddress(hm, "MSProviderInit"); 
        Log(true,"GetProcAddress returned 0x%08X\n", pMsProviderInit); 
    } 
    else hRes = E_OUTOFMEMORY; 
    if (pMsProviderInit) 
    { 
        Log(true,"Calling pMsProviderInit\n"); 
        CMSProvider* pWrappedProvider = NULL; 
        LPMSPROVIDER pSyncProviderObj = NULL; 
        hRes = pMsProviderInit( 
            hm,// not hInstance: first param is handle of module in which the function lives 
            lpMalloc, 
            lpAllocateBuffer, 
            lpAllocateMore, 
            lpFreeBuffer, 
            ulFlags, 
            ulMAPIVer, 
            lpulProviderVer, 
            &pSyncProviderObj                         
            ); 
        Log(true,"pMsProviderInit returned 0x%08X\n", hRes); 
        if (SUCCEEDED(hRes)) 
        { 
            pWrappedProvider = new CMSProvider (pSyncProviderObj); 
            if (NULL == pWrappedProvider) 
            { 
                Log(true,"MSProviderInit: Failed to allocate new CMSProvider object\n"); 
                hRes = E_OUTOFMEMORY; 
            } 
            // Copy pointer to the allocated object back into the  
            //return IMSProvider object pointer 
            *lppMSProvider = pWrappedProvider; 
        } 
    } 
    else hRes = E_OUTOFMEMORY; 
    return hRes; 
}
```

### <a name="wrapped-pst-and-unicode-paths"></a>Rutas de acceso de Unicode y PST ajustados

Para plantear el ejemplo original preparado en Microsoft Visual Studio 2008 para usar rutas de acceso de Unicode a NST para su uso en Microsoft Outlook 2010 está habilitado para Unicode y Outlook 2013, debe usar la rutina **CreateStoreEntryID** , que genera el identificador de entrada, un formato para las rutas de acceso de ASCII y otra para las rutas de acceso Unicode. Estos se representan como estructuras en el siguiente ejemplo. 
  
```cpp
typedef struct                              // short format
{
         BYTE             rgbFlags[4];     // MAPI-defined flags
         MAPIUID          uid;             // PST provider MUID
         BYTE             bReserved;       // Reserved (must be zero)
         CHAR             szPath[1];       // Full path to store (ASCII)
 } EIDMS;
// Unicode version of EIDMSW is an extension of EIDMS
// and szPath is always NULL
typedef struct                              // Long format to support Unicode path and name
{
         BYTE             rgbFlags[4];     // MAPI-defined flags
         MAPIUID          uid;             // PST provider MUID
         BYTE             bReserved;       // Reserved (must be zero)
         CHAR             szPath[1];       // ASCII path to store is always NULL
         WCHAR            wzPath[1];       // Full path to store (Unicode)
} EIDMSW;
```

> [!IMPORTANT]
> Las diferencias en estas estructuras son dos bytes NULL antes de una ruta de acceso de Unicode. Si necesita interpretar el identificador de entrada en el "servicio de entrada rutina" que sigue, una forma de determinar si ese es el caso o no sería convertir como EIDMS en primer lugar, a continuación, compruebe si la szPath [0] es NULL. Si es así, convertir como EIDMSW. 
  
## <a name="service-entry-routine"></a>Rutina de entrada de servicio

La función **[MSGSERVICEENTRY](msgserviceentry.md)** es el punto de entrada del servicio de mensaje donde se configura el proveedor de almacén de archivos PST ajustado. Las llamadas de función `GetMemAllocRoutines()` para obtener las rutinas de administración de la memoria MAPI. La función utiliza la `lpProviderAdmin` parámetro para buscar la sección de perfil para el proveedor y se establecen las propiedades en el perfil. 
  
### <a name="serviceentry-example"></a>Ejemplo de ServiceEntry()

```cpp
HRESULT STDAPICALLTYPE ServiceEntry ( 
    HINSTANCE /*hInstance*/, 
    LPMALLOC lpMalloc, 
    LPMAPISUP lpMAPISup, 
    ULONG ulUIParam, 
    ULONG ulFlags, 
    ULONG ulContext, 
    ULONG cValues, 
    LPSPropValue lpProps, 
    LPPROVIDERADMIN lpProviderAdmin, 
    LPMAPIERROR FAR *lppMapiError) 
{ 
    if (!lpMAPISup || !lpProviderAdmin) return MAPI_E_INVALID_PARAMETER; 
    HRESULT         hRes = S_OK; 
    Log(true,"ServiceEntry function called\n"); 
    Log(true,"About to call NSTServiceEntry\n"); 
 
    if (MSG_SERVICE_INSTALL         == ulContext || 
        MSG_SERVICE_DELETE            == ulContext || 
        MSG_SERVICE_UNINSTALL        == ulContext || 
        MSG_SERVICE_PROVIDER_CREATE == ulContext || 
        MSG_SERVICE_PROVIDER_DELETE == ulContext) 
    { 
        // These contexts are not supported 
        return MAPI_E_NO_SUPPORT; 
    } 
 
    // Get memory routines 
    hRes = lpMAPISup-> 
        GetMemAllocRoutines(&g_lpAllocateBuffer,&g_lpAllocateMore,&g_lpFreeBuffer); 
    HMODULE hm = LoadLibrary("C:\\Program Files\\Common Files\\System" + 
        "\\MSMAPI\\1033\\MSPST32.dll" ); 
    if (!hm) hm = LoadLibrary("C:\\Program Files\\Microsoft Office\\Office12" + 
        "\\MSPST32.dll" ); 
    Log(true, "Got module 0x%08X\n", hm); 
    if (!hm) return E_OUTOFMEMORY; 
    LPMSGSERVICEENTRY pNSTServiceEntry =  
        (LPMSGSERVICEENTRY)GetProcAddress(hm, "NSTServiceEntry"); 
    Log(true, "Got procaddress  0x%08X\n", pNSTServiceEntry); 
    if (!pNSTServiceEntry) return E_OUTOFMEMORY; 
 
    // Get profile section 
    LPPROFSECT lpProfSect = NULL; 
    hRes = lpProviderAdmin-> 
        OpenProfileSection((LPMAPIUID) NULL, NULL, MAPI_MODIFY, &lpProfSect); 
    // Set passed in props into the profile 
    if (lpProps && cValues) 
    { 
        hRes = lpProfSect->SetProps(cValues,lpProps,NULL); 
    } 
    // Make sure there is a store path set 
    if (SUCCEEDED(hRes)) hRes = SetOfflineStoreProps(lpProfSect,ulUIParam); 
    ULONG            ulProfProps = 0; 
    LPSPropValue    lpProfProps = NULL; 
 
    // Evaluate props 
    hRes = lpProfSect->GetProps((LPSPropTagArray)&sptClientProps, 
                                fMapiUnicode, 
                                &ulProfProps, 
                                &lpProfProps); 
    if (SUCCEEDED(hRes)) 
    { 
        CSupport * pMySup = NULL; 
        pMySup = new CSupport(lpMAPISup, lpProfSect); 
        if (!pMySup) 
        { 
            Log(true,"MSProviderInit: Failed to allocate new CSupport object\n"); 
            hRes = E_OUTOFMEMORY; 
        } 
        if (SUCCEEDED(hRes)) 
        { 
            hRes = pNSTServiceEntry( 
                hm,  
                lpMalloc, 
                pMySup, 
                ulUIParam, 
                ulFlags, 
                ulContext, 
                ulProfProps, 
                lpProfProps, 
                NULL,//pAdminProvObj, //Don't pass this when creating an NST 
                lppMapiError); 
            if (SUCCEEDED(hRes)) 
            { 
                // Finish setting up the profile 
                hRes = InitStoreProps( 
                    lpMAPISup,  
                    lpProfSect,  
                    lpProviderAdmin); 
                hRes = lpProfSect->SaveChanges(KEEP_OPEN_READWRITE); 
            } 
        } 
    } 
    Log(true, "Ran pNSTServiceEntry 0x%08X\n", hRes); 
    MyFreeBuffer(lpProfProps); 
    if (lpProfSect) lpProfSect->Release(); 
 
    return hRes; 
}
```

## <a name="see-also"></a>Ver también

- [Acerca del ejemplo ajusta el proveedor de almacén de archivos PST](about-the-sample-wrapped-pst-store-provider.md)
- [Instalar el ejemplo ajusta el proveedor de almacén de archivos PST](installing-the-sample-wrapped-pst-store-provider.md)
- [Inicie sesión en un proveedor de almacén de archivos PST ajustado](logging-on-to-a-wrapped-pst-store-provider.md)
- [Uso de un proveedor de almacén de archivos PST ajustado](using-a-wrapped-pst-store-provider.md)
- [Cerrando un proveedor de almacén de archivos PST ajustado](shutting-down-a-wrapped-pst-store-provider.md)

