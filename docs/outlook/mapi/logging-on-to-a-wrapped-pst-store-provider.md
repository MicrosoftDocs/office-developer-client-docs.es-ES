---
title: Iniciar sesión en un proveedor de almacén de archivos PST ajustado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: 'Última modificación: 2012 de julio de 2002'
ms.openlocfilehash: 96f472d67f144a451046ff61a3ed6c6ff2ff9acf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408989"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a>Iniciar sesión en un proveedor de almacén de archivos PST ajustado

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Antes de poder iniciar la sesión MAPI en un proveedor de almacén de archivos PST ajustado, debe inicializar y configurar el proveedor de almacenamiento de archivos de carpetas personales (PST) ajustado. Para obtener más información, vea [inicializar un proveedor de almacén de archivos PST ajustado](initializing-a-wrapped-pst-store-provider.md).
  
Una vez que haya inicializado y configurado un proveedor de almacén de archivos PST ajustado, debe implementar dos rutinas de inicio de sesión. La función **[IMSProvider:: Logon](imsprovider-logon.md)** registra el MAPI en el proveedor del almacén de archivos PST ajustado. La función **[IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md)** registra los registros de la cola MAPI en el proveedor de almacén de archivos PST ajustado. 
  
En este tema, la función **IMSProvider:: Logon** y la función **IMSProvider:: SpoolerLogon** se demuestran mediante ejemplos de código del proveedor de almacén de archivos PST ajustado de ejemplo. El ejemplo implementa un proveedor de archivos PST ajustado que está pensado para usarse junto con la API de replicación. Para obtener más información sobre cómo descargar e instalar el proveedor de almacén de archivos PST ajustado de ejemplo, vea [Installing the Sample wrapped PST Store Provider](installing-the-sample-wrapped-pst-store-provider.md). Para obtener más información acerca de la API de replicación, consulte [About the replicaTION API](about-the-replication-api.md).
  
Una vez que MAPI y la cola MAPI hayan iniciado sesión en el proveedor de almacén de archivos PST ajustado, estará listo para su uso. Para obtener más información, vea [usar un proveedor de almacén de archivos PST ajustado](using-a-wrapped-pst-store-provider.md).
  
## <a name="mapi-logon-routine"></a>Rutina de inicio de sesión MAPI

Una vez inicializado el proveedor de almacén de archivos PST ajustado, debe implementar la función **[IMSProvider:: Logon](imsprovider-logon.md)** para iniciar sesión MAPI en el almacén de archivos PST ajustado. Esta función valida las credenciales de usuario y obtiene las propiedades de configuración del proveedor. También debe implementar la `SetOLFIInOST` función para establecer la información de archivo sin conexión (**[OLFI](olfi.md)** ). **OLFI** es una cola de estructuras de identificador a largo plazo que usa el proveedor de almacén de archivos PST ajustado para asignar un identificador de entrada para un mensaje o una carpeta nuevos en el modo sin conexión. Por último, la función **IMSProvider:: Logon** devuelve un objeto de almacén de mensajes en el que la cola MAPI y las aplicaciones cliente pueden `ppMDB` iniciar sesión en el parámetro. 
  
### <a name="cmsproviderlogon-example"></a>Ejemplo de CMSProvider:: Logon ()

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

## <a name="mapi-spooler-logon-routine"></a>Rutina de inicio de sesión de la cola MAPI

De forma similar a **IMSProvider:: Logon**, debe implementar la función **[IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md)** para registrar la cola MAPI en el almacén de archivos PST ajustado. Se devuelve en el `ppMDB` parámetro un objeto de almacén de mensajes en el que la cola MAPI y las aplicaciones cliente pueden iniciar sesión. 
  
### <a name="cmsproviderspoolerlogon-example"></a>Ejemplo de CMSProvider:: SpoolerLogon ()

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

## <a name="see-also"></a>Ver también

- [Información sobre el proveedor de almacén de archivos PST ajustado de ejemplo](about-the-sample-wrapped-pst-store-provider.md) 
- [Instalación del proveedor de almacén de archivos PST ajustado de ejemplo](installing-the-sample-wrapped-pst-store-provider.md) 
- [Inicializar un proveedor de almacén de archivos PST ajustado](initializing-a-wrapped-pst-store-provider.md)
- [Usar un proveedor de almacén de archivos PST ajustado](using-a-wrapped-pst-store-provider.md)
- [Apagar un proveedor de almacén de archivos PST ajustado](shutting-down-a-wrapped-pst-store-provider.md)

