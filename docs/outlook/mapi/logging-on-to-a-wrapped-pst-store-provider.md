---
title: Inicio de sesión a un proveedor de almacén de archivos PST ajustado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: 'Última modificación: 02 de julio de 2012'
ms.openlocfilehash: 2dfa3820d8d2ab57f278e90bef5d5a40164da6fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/21/2018
ms.locfileid: "19818024"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a>Inicio de sesión a un proveedor de almacén de archivos PST ajustado

**Hace referencia a**: Outlook 
  
Antes de que puede iniciar sesión MAPI a un proveedor de almacén de archivos PST ajustado, debe inicializar y configurar el proveedor de almacenamiento de archivo (.pst) de carpetas personales ajustado. Para obtener más información, vea [inicializar un proveedor de almacén de archivos PST ajustado](initializing-a-wrapped-pst-store-provider.md).
  
Después de haber inicializado y configurado un proveedor de almacén de archivos PST ajustado, debe implementar dos rutinas de inicio de sesión. La función **[IMSProvider::Logon](imsprovider-logon.md)** inicia sesión MAPI en el proveedor de almacén de archivos PST ajustado. Los registros de la función **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** en la cola MAPI para el proveedor de almacén de archivos PST ajustado. 
  
En este tema, se muestran la función **IMSProvider::Logon** y la función **IMSProvider::SpoolerLogon** mediante el uso de los ejemplos de código desde el proveedor de almacén de archivos PST ajustado de ejemplo. En el ejemplo se implementa un proveedor de PST ajustado que está pensado para usarse junto con la API de replicación. Para obtener más información sobre cómo descargar e instalar al proveedor de almacén de archivos PST ajustado de ejemplo, vea [instalar el proveedor de almacén de archivos PST ajustado de ejemplo](installing-the-sample-wrapped-pst-store-provider.md). Para obtener más información acerca de la API de replicación, vea [Acerca de la API de replicación](about-the-replication-api.md).
  
Una vez iniciados sesión MAPI y la cola MAPI proveedor de almacén de sesión en el archivo PST ajustado, está listo para usarse. Para obtener más información, vea [uso de un proveedor de almacén de archivos PST ajustado](using-a-wrapped-pst-store-provider.md).
  
## <a name="mapi-logon-routine"></a>Rutina de inicio de sesión MAPI

Después de que se inicialice el proveedor de almacén de archivos PST ajustado, debe implementar la función **[IMSProvider::Logon](imsprovider-logon.md)** para iniciar sesión MAPI en el almacén de archivos PST ajustado. Esta función valida las credenciales de usuario y obtiene las propiedades de configuración para el proveedor. También debe implementar la `SetOLFIInOST` (función) para establecer la información del archivo sin conexión (**[OLFI](olfi.md)** ). **OLFI** es una cola de estructuras a largo plazo de identificador que se usa por el proveedor de almacén de archivos PST ajustado para asignar un identificador de entrada para un nuevo mensaje o una carpeta en modo sin conexión. Por último, la función **IMSProvider::Logon** devuelve un objeto de almacén de mensajes que las aplicaciones de cliente y de la cola de impresión MAPI pueden iniciar sesión en el `ppMDB` parámetro. 
  
### <a name="cmsproviderlogon-example"></a>Ejemplo de CMSProvider::Logon()

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

## <a name="mapi-spooler-logon-routine"></a>Rutina de inicio de sesión de cola de impresión de MAPI

Al igual que **IMSProvider::Logon**, debe implementar la función **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** para iniciar sesión en el almacén de archivos PST ajustado en la cola de MAPI. Se devuelve un objeto de almacén de mensajes que pueden iniciar una sesión en las aplicaciones de cliente y de la cola de impresión MAPI en el `ppMDB` parámetro. 
  
### <a name="cmsproviderspoolerlogon-example"></a>Ejemplo de CMSProvider::SpoolerLogon()

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

## <a name="see-also"></a>Vea también

- [Información sobre el proveedor de almacén de archivos PST ajustado de muestra](about-the-sample-wrapped-pst-store-provider.md) 
- [Instalar la muestra de proveedor de almacén de archivos PST ajustado](installing-the-sample-wrapped-pst-store-provider.md) 
- [Inicializar un proveedor de almacén de archivos PST ajustado](initializing-a-wrapped-pst-store-provider.md)
- [Usar un proveedor de almacén de archivos PST ajustado](using-a-wrapped-pst-store-provider.md)
- [Apagar un proveedor de almacén de archivos PST ajustado](shutting-down-a-wrapped-pst-store-provider.md)

