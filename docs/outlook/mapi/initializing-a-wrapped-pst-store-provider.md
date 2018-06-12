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
# <a name="initializing-a-wrapped-pst-store-provider"></a><span data-ttu-id="60164-103">Inicializar un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="60164-103">Initializing a wrapped PST store provider</span></span>

<span data-ttu-id="60164-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="60164-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="60164-105">Para implementar un proveedor de almacén de archivo (.pst) de carpetas personales ajustado, deben inicializar el proveedor de almacén de archivos PST ajustado mediante el uso de la función **[MSProviderInit](msproviderinit.md)** como un punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="60164-105">To implement a wrapped Personal Folders file (PST) store provider, you must initialize the wrapped PST store provider by using the **[MSProviderInit](msproviderinit.md)** function as an entry point.</span></span> <span data-ttu-id="60164-106">Después de que se inicialice la DLL del proveedor, la función **[MSGSERVICEENTRY](msgserviceentry.md)** configura el proveedor de almacén de archivos PST ajustado.</span><span class="sxs-lookup"><span data-stu-id="60164-106">After the provider's DLL is initialized, the **[MSGSERVICEENTRY](msgserviceentry.md)** function configures the wrapped PST store provider.</span></span> 
  
<span data-ttu-id="60164-107">En este tema, se muestran la función **MSProviderInit** y la función **MSGSERVICEENTRY** mediante el uso de los ejemplos de código desde el proveedor de almacén de archivos PST ajustado de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="60164-107">In this topic, the **MSProviderInit** function and the **MSGSERVICEENTRY** function are demonstrated by using code examples from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="60164-108">En el ejemplo se implementa un proveedor de PST ajustado que está pensado para usarse junto con la API de replicación.</span><span class="sxs-lookup"><span data-stu-id="60164-108">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="60164-109">Para obtener más información sobre cómo descargar e instalar al proveedor de almacén de archivos PST ajustado de ejemplo, vea [instalar el proveedor de almacén de archivos PST ajustado de ejemplo](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="60164-109">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="60164-110">Para obtener más información acerca de la API de replicación, vea [Acerca de la API de replicación](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="60164-110">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="60164-111">Después de inicializar un proveedor de almacén de archivos PST ajustado, debe implementar funciones de modo que pueden iniciar sesión en el proveedor de almacén de mensajes MAPI y la cola de MAPI.</span><span class="sxs-lookup"><span data-stu-id="60164-111">After you have initialized a wrapped PST store provider, you must implement functions so that MAPI and the MAPI spooler can log onto the message store provider.</span></span> <span data-ttu-id="60164-112">Para obtener más información, vea [Registro en a un proveedor de almacén de archivos PST ajustado](logging-on-to-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="60164-112">For more information, see [Logging On to a Wrapped PST Store Provider](logging-on-to-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="initialization-routine"></a><span data-ttu-id="60164-113">Rutina de inicialización</span><span class="sxs-lookup"><span data-stu-id="60164-113">Initialization routine</span></span>

<span data-ttu-id="60164-114">Todos los proveedores de almacén de archivos PST ajustados deben implementar la función **[MSProviderInit](msproviderinit.md)** como un punto de entrada para inicializar la DLL del proveedor.</span><span class="sxs-lookup"><span data-stu-id="60164-114">All wrapped PST store providers must implement the **[MSProviderInit](msproviderinit.md)** function as an entry point to initialize the provider's DLL.</span></span> <span data-ttu-id="60164-115">**MSProviderInit** comprueba si el número de versión de la interfaz de proveedor de servicio, `ulMAPIVer`, es compatible con el número de versión actual, `CURRENT_SPI_VERSION`.</span><span class="sxs-lookup"><span data-stu-id="60164-115">**MSProviderInit** checks to see if the version number of the service provider interface,  `ulMAPIVer`, is compatible with the current version number,  `CURRENT_SPI_VERSION`.</span></span> <span data-ttu-id="60164-116">La función guarda la memoria MAPI de rutinas de administración en el `g_lpAllocateBuffer`, `g_lpAllocateMore`, y `g_lpFreeBuffer` parámetros.</span><span class="sxs-lookup"><span data-stu-id="60164-116">The function saves the MAPI memory management routines into the  `g_lpAllocateBuffer`,  `g_lpAllocateMore`, and  `g_lpFreeBuffer` parameters.</span></span> <span data-ttu-id="60164-117">Estas rutinas de administración de memoria se deben usar durante la implementación de almacén de archivos PST ajustada para la asignación y cancelación de asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="60164-117">These memory management routines should be used throughout the wrapped PST store implementation for memory allocation and deallocation.</span></span> 
  
### <a name="msproviderinit-example"></a><span data-ttu-id="60164-118">Ejemplo de MSProviderInit()</span><span class="sxs-lookup"><span data-stu-id="60164-118">MSProviderInit() example</span></span>

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

### <a name="wrapped-pst-and-unicode-paths"></a><span data-ttu-id="60164-119">Rutas de acceso de Unicode y PST ajustados</span><span class="sxs-lookup"><span data-stu-id="60164-119">Wrapped PST and Unicode paths</span></span>

<span data-ttu-id="60164-120">Para plantear el ejemplo original preparado en Microsoft Visual Studio 2008 para usar rutas de acceso de Unicode a NST para su uso en Microsoft Outlook 2010 está habilitado para Unicode y Outlook 2013, debe usar la rutina **CreateStoreEntryID** , que genera el identificador de entrada, un formato para las rutas de acceso de ASCII y otra para las rutas de acceso Unicode.</span><span class="sxs-lookup"><span data-stu-id="60164-120">To retrofit the original sample prepared in Microsoft Visual Studio 2008 to use Unicode paths to the NST for use in Unicode-enabled Microsoft Outlook 2010 and Outlook 2013, the **CreateStoreEntryID** routine, which produces the entry identifier, should use one format for ASCII paths, and another for Unicode paths.</span></span> <span data-ttu-id="60164-121">Estos se representan como estructuras en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="60164-121">These are represented as structures in the following example.</span></span> 
  
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
> <span data-ttu-id="60164-122">Las diferencias en estas estructuras son dos bytes NULL antes de una ruta de acceso de Unicode.</span><span class="sxs-lookup"><span data-stu-id="60164-122">The differences in these structures are two NULL bytes prior to a Unicode path.</span></span> <span data-ttu-id="60164-123">Si necesita interpretar el identificador de entrada en el "servicio de entrada rutina" que sigue, una forma de determinar si ese es el caso o no sería convertir como EIDMS en primer lugar, a continuación, compruebe si la szPath [0] es NULL.</span><span class="sxs-lookup"><span data-stu-id="60164-123">If you need to interpret the entry identifier in the "Service Entry Routine" that follows, one way to determine whether that is the case or not would be to cast as EIDMS first, then check whether the szPath[0] is NULL.</span></span> <span data-ttu-id="60164-124">Si es así, convertir como EIDMSW.</span><span class="sxs-lookup"><span data-stu-id="60164-124">If it is, cast it as EIDMSW instead.</span></span> 
  
## <a name="service-entry-routine"></a><span data-ttu-id="60164-125">Rutina de entrada de servicio</span><span class="sxs-lookup"><span data-stu-id="60164-125">Service Entry routine</span></span>

<span data-ttu-id="60164-126">La función **[MSGSERVICEENTRY](msgserviceentry.md)** es el punto de entrada del servicio de mensaje donde se configura el proveedor de almacén de archivos PST ajustado.</span><span class="sxs-lookup"><span data-stu-id="60164-126">The **[MSGSERVICEENTRY](msgserviceentry.md)** function is the message service entry point where the wrapped PST store provider is configured.</span></span> <span data-ttu-id="60164-127">Las llamadas de función `GetMemAllocRoutines()` para obtener las rutinas de administración de la memoria MAPI.</span><span class="sxs-lookup"><span data-stu-id="60164-127">The function calls  `GetMemAllocRoutines()` to get the MAPI memory management routines.</span></span> <span data-ttu-id="60164-128">La función utiliza la `lpProviderAdmin` parámetro para buscar la sección de perfil para el proveedor y se establecen las propiedades en el perfil.</span><span class="sxs-lookup"><span data-stu-id="60164-128">The function uses the  `lpProviderAdmin` parameter to locate the profile section for the provider and sets the properties in the profile.</span></span> 
  
### <a name="serviceentry-example"></a><span data-ttu-id="60164-129">Ejemplo de ServiceEntry()</span><span class="sxs-lookup"><span data-stu-id="60164-129">ServiceEntry() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="60164-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="60164-130">See also</span></span>

- [<span data-ttu-id="60164-131">Acerca del ejemplo ajusta el proveedor de almacén de archivos PST</span><span class="sxs-lookup"><span data-stu-id="60164-131">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="60164-132">Instalar el ejemplo ajusta el proveedor de almacén de archivos PST</span><span class="sxs-lookup"><span data-stu-id="60164-132">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md)
- [<span data-ttu-id="60164-133">Inicie sesión en un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="60164-133">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="60164-134">Uso de un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="60164-134">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="60164-135">Cerrando un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="60164-135">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

