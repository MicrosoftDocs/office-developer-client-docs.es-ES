---
title: Iniciar sesión en un proveedor de almacén de archivos PST ajustado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: 'Last modified: July 02, 2012'
ms.openlocfilehash: 96f472d67f144a451046ff61a3ed6c6ff2ff9acf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408989"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a><span data-ttu-id="0c6dd-103">Iniciar sesión en un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="0c6dd-103">Logging on to a wrapped PST store provider</span></span>

<span data-ttu-id="0c6dd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c6dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c6dd-105">Para poder iniciar sesión en MAPI en un proveedor de almacenamiento PST ajustado, debe inicializar y configurar el proveedor de almacén de archivos de carpetas personales (PST) ajustado.</span><span class="sxs-lookup"><span data-stu-id="0c6dd-105">Before you can log on MAPI to a wrapped PST store provider, you must initialize and configure the wrapped Personal Folders file (PST) store provider.</span></span> <span data-ttu-id="0c6dd-106">Para obtener más información, vea [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0c6dd-106">For more information, see [Initializing a Wrapped PST Store Provider](initializing-a-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="0c6dd-107">Después de inicializar y configurar un proveedor de almacenamiento PST ajustado, debe implementar dos rutinas de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="0c6dd-107">After you have initialized and configured a wrapped PST store provider, you must implement two logon routines.</span></span> <span data-ttu-id="0c6dd-108">La **[función IMSProvider::Logon](imsprovider-logon.md)** inicia sesión en MAPI en el proveedor del almacén PST ajustado.</span><span class="sxs-lookup"><span data-stu-id="0c6dd-108">The **[IMSProvider::Logon](imsprovider-logon.md)** function logs on MAPI to the wrapped PST store provider.</span></span> <span data-ttu-id="0c6dd-109">La **[función IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** inicia sesión en la cola MAPI en el proveedor de almacenamiento PST ajustado.</span><span class="sxs-lookup"><span data-stu-id="0c6dd-109">The **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function logs on the MAPI spooler to the wrapped PST store provider.</span></span> 
  
<span data-ttu-id="0c6dd-110">En este tema, la función **IMSProvider::Logon** y la función **IMSProvider::SpoolerLogon** se muestran mediante ejemplos de código del proveedor de almacén PST ajustado de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0c6dd-110">In this topic, the **IMSProvider::Logon** function and the **IMSProvider::SpoolerLogon** function are demonstrated by using code examples from the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="0c6dd-111">El ejemplo implementa un proveedor de PST ajustado que está pensado para usarse junto con la API de replicación.</span><span class="sxs-lookup"><span data-stu-id="0c6dd-111">The sample implements a wrapped PST provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="0c6dd-112">Para obtener más información acerca de cómo descargar e instalar el proveedor de la tienda PST encapsulada de muestra, consulte [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0c6dd-112">For more information about downloading and installing the Sample Wrapped PST Store Provider, see [Installing the Sample Wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md).</span></span> <span data-ttu-id="0c6dd-113">Para obtener más información acerca de la API de replicación, vea [Acerca de la API de replicación](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="0c6dd-113">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="0c6dd-114">Después de que MAPI y la cola MAPI hayan iniciado sesión en el proveedor de almacenamiento PST ajustado, está listo para usarse.</span><span class="sxs-lookup"><span data-stu-id="0c6dd-114">After MAPI and the MAPI spooler are logged on to the wrapped PST store provider, it is ready to be used.</span></span> <span data-ttu-id="0c6dd-115">Para obtener más información, vea [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0c6dd-115">For more information, see [Using a Wrapped PST Store Provider](using-a-wrapped-pst-store-provider.md).</span></span>
  
## <a name="mapi-logon-routine"></a><span data-ttu-id="0c6dd-116">Rutina de inicio de sesión MAPI</span><span class="sxs-lookup"><span data-stu-id="0c6dd-116">MAPI Logon routine</span></span>

<span data-ttu-id="0c6dd-117">Después de inicializar el proveedor del almacén PST ajustado, debe implementar la función **[IMSProvider::Logon](imsprovider-logon.md)** para iniciar sesión en MAPI en el almacén PST ajustado.</span><span class="sxs-lookup"><span data-stu-id="0c6dd-117">After the wrapped PST store provider is initialized, you must implement the **[IMSProvider::Logon](imsprovider-logon.md)** function to log on MAPI to the wrapped PST store.</span></span> <span data-ttu-id="0c6dd-118">Esta función valida las credenciales de usuario y obtiene las propiedades de configuración del proveedor.</span><span class="sxs-lookup"><span data-stu-id="0c6dd-118">This function validates user credentials and gets the configuration properties for the provider.</span></span> <span data-ttu-id="0c6dd-119">También debe implementar la función para establecer la información de archivo sin  `SetOLFIInOST` conexión (**[OLFI](olfi.md)** ).</span><span class="sxs-lookup"><span data-stu-id="0c6dd-119">You must also implement the  `SetOLFIInOST` function to set the Offline File Info (**[OLFI](olfi.md)** ).</span></span> <span data-ttu-id="0c6dd-120">**OLFI** es una cola de estructuras de id. a largo plazo que usa el proveedor de almacenamiento PST ajustado para asignar un identificador de entrada para un nuevo mensaje o carpeta en modo sin conexión.</span><span class="sxs-lookup"><span data-stu-id="0c6dd-120">**OLFI** is a queue of long-term ID structures that is used by the wrapped PST store provider to assign an Entry ID for a new message or folder in offline mode.</span></span> <span data-ttu-id="0c6dd-121">Por último, la función **IMSProvider::Logon** devuelve un objeto de almacén de mensajes al que la cola MAPI y las aplicaciones cliente pueden iniciar sesión en el  `ppMDB` parámetro.</span><span class="sxs-lookup"><span data-stu-id="0c6dd-121">Finally, the **IMSProvider::Logon** function returns a message store object that the MAPI spooler and client applications can log on to in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderlogon-example"></a><span data-ttu-id="0c6dd-122">Ejemplo de CMSProvider::Logon()</span><span class="sxs-lookup"><span data-stu-id="0c6dd-122">CMSProvider::Logon() example</span></span>

```cpp
STDMETHODIMP CMSProvider::Logon( 
    LPMAPISUP pSupObj, 
    ULONG ulUIParam, 
    LPTSTR pszProfileName, 
    ULONG cbEntryID, 
    LPENTRYID pEntryID, 
    ULONG ulFlags, 
    LPCIID pInterface, 
    ULONG * pcbSpoolSecurity, 
    LPBYTE * ppbSpoolSecurity, 
    LPMAPIERROR * ppMAPIError, 
    LPMSLOGON * ppMSLogon, 
    LPMDB * ppMDB) 
{ 
    HRESULT hRes = S_OK; 
    LPMDB lpPSTMDB = NULL; 
    CMsgStore* pWrappedMDB = NULL; 
 
    Log(true,"CMSProvider::Logon Pst logon Called\n"); 
 
    LPPROFSECT lpProfSect = NULL; 
    CSupport * pMySup = NULL; 
    hRes = GetGlobalProfileObject(pSupObj,&lpProfSect); 
    pMySup = new CSupport(pSupObj, lpProfSect); 
    if (!pMySup) 
    { 
        Log(true,"CMSProvider::Logon: Failed to allocate new CSupport object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    if (SUCCEEDED(hRes)) 
    { 
        ulFlags = (ulFlags & ~MDB_OST_LOGON_ANSI) | MDB_OST_LOGON_UNICODE; 
        hRes = m_pPSTMS->Logon( 
            pMySup, 
            ulUIParam,  
            pszProfileName,  
            cbEntryID, 
            pEntryID,  
            ulFlags,  
            pInterface,  
            pcbSpoolSecurity, 
            ppbSpoolSecurity,  
            ppMAPIError,  
            ppMSLogon,  
            &lpPSTMDB); 
    } 
    Log(true,"CMSProvider::Logon returned 0x%08X\n", hRes); 
 
    // Set up the MDB to allow synchronization 
    if (SUCCEEDED(hRes)) 
    { 
        hRes = SetOLFIInOST(lpPSTMDB); 
        Log(true,"SetOLFIInOST returned 0x%08X\n", hRes); 
    } 
    // Wrap the outgoing MDB 
    pWrappedMDB = new CMsgStore (lpPSTMDB); 
    if (NULL == pWrappedMDB) 
    { 
        Log(true,"CMSProvider::Logon: Failed to allocate new CMsgStore object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    // Copy pointer to the allocated object back into the return LPMDB object pointer 
    *ppMDB = pWrappedMDB; 
    if (lpProfSect) lpProfSect->Release(); 
 
    return hRes; 
}
```

## <a name="mapi-spooler-logon-routine"></a><span data-ttu-id="0c6dd-123">Rutina de inicio de sesión de cola MAPI</span><span class="sxs-lookup"><span data-stu-id="0c6dd-123">MAPI Spooler Logon routine</span></span>

<span data-ttu-id="0c6dd-124">De forma similar a **IMSProvider::Logon**, debe implementar la función **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** para iniciar sesión en la cola MAPI en el almacén DE PST ajustado.</span><span class="sxs-lookup"><span data-stu-id="0c6dd-124">Similar to **IMSProvider::Logon**, you must implement the **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** function to log the MAPI spooler on to the wrapped PST store.</span></span> <span data-ttu-id="0c6dd-125">Se devuelve un objeto de almacén de mensajes en el que la cola MAPI y las aplicaciones cliente pueden iniciar sesión en el  `ppMDB` parámetro.</span><span class="sxs-lookup"><span data-stu-id="0c6dd-125">A message store object that the MAPI spooler and client applications can log on to is returned in the  `ppMDB` parameter.</span></span> 
  
### <a name="cmsproviderspoolerlogon-example"></a><span data-ttu-id="0c6dd-126">Ejemplo de CMSProvider::SpoolerLogon()</span><span class="sxs-lookup"><span data-stu-id="0c6dd-126">CMSProvider::SpoolerLogon() example</span></span>

```cpp
STDMETHODIMP CMSProvider::SpoolerLogon ( 
    LPMAPISUP pSupObj, 
    ULONG ulUIParam, 
    LPTSTR pszProfileName, 
    ULONG cbEntryID, 
    LPENTRYID pEntryID, 
    ULONG ulFlags, 
    LPCIID pInterface, 
    ULONG cbSpoolSecurity, 
    LPBYTE pbSpoolSecurity, 
    LPMAPIERROR * ppMAPIError, 
    LPMSLOGON * ppMSLogon, 
    LPMDB * ppMDB) 
{ 
    HRESULT hRes = S_OK; 
     
    Log(true,"CMSProvider::SpoolerLogon\n"); 
    LPPROFSECT lpProfSect = NULL; 
    CSupport * pMySup = NULL; 
    hRes = GetGlobalProfileObject(pSupObj,&lpProfSect); 
    pMySup = new CSupport(pSupObj, lpProfSect); 
    if (!pMySup) 
    { 
        Log(true,"CMSProvider::SpoolerLogon: " + 
            "Failed to allocate new CSupport object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    if (SUCCEEDED(hRes)) 
    { 
        hRes = m_pPSTMS->SpoolerLogon(  
            pMySup,//pSupObj, 
            ulUIParam, 
            pszProfileName, 
            cbEntryID, 
            pEntryID, 
            ulFlags, 
            pInterface, 
            cbSpoolSecurity, 
            pbSpoolSecurity, 
            ppMAPIError, 
            ppMSLogon, 
            ppMDB); 
    } 
    Log(true,"CMSProvider::SpoolerLogon returned 0x%08X\n", hRes); 
 
    return hRes; 
}
```

## <a name="see-also"></a><span data-ttu-id="0c6dd-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c6dd-127">See also</span></span>

- [<span data-ttu-id="0c6dd-128">Acerca del proveedor de almacén PST ajustado de ejemplo</span><span class="sxs-lookup"><span data-stu-id="0c6dd-128">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="0c6dd-129">Instalación del proveedor de almacén PST ajustado de muestra</span><span class="sxs-lookup"><span data-stu-id="0c6dd-129">Installing the Sample Wrapped PST Store Provider</span></span>](installing-the-sample-wrapped-pst-store-provider.md) 
- [<span data-ttu-id="0c6dd-130">Inicializar un proveedor de almacenamiento PST ajustado</span><span class="sxs-lookup"><span data-stu-id="0c6dd-130">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="0c6dd-131">Uso de un proveedor de almacenamiento PST ajustado</span><span class="sxs-lookup"><span data-stu-id="0c6dd-131">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
- [<span data-ttu-id="0c6dd-132">Apagar un proveedor de almacenamiento PST ajustado</span><span class="sxs-lookup"><span data-stu-id="0c6dd-132">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

