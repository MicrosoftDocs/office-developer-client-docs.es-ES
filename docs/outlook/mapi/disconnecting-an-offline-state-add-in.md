---
title: Desconectar un sin conexión estado Add-in
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6922cb38-a9e3-e4a9-d4a3-e11b81fc77e2
description: '�ltima modificaci�n: lunes, 7 de diciembre de 2015'
ms.openlocfilehash: 82f529f58a62f412ed8b25d1ceaf508463491612
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19816673"
---
# <a name="disconnecting-an-offline-state-add-in"></a>Desconectar un sin conexión estado Add-in

**Se aplica a**: Outlook 
  
Cuando el estado sin conexión complemento está desconectado, debe implementar las funciones para terminar y limpiar el complemento correctamente. Para obtener más información sobre la configuración y el uso sin conexión de estado complemento para supervisar los cambios de estado de conexión, vea [Agregar en configuración de seguridad de un estado sin conexión](setting-up-an-offline-state-add-in.md) y [Supervisión conexión el estado de los cambios utilizando un complemento de estado sin conexión](monitoring-connection-state-changes-using-an-offline-state-add-in.md).
  
En este tema, estos desconexión, terminar y se muestran las funciones de limpieza mediante el uso de los ejemplos de código desde el complemento de estado sin conexión de ejemplo. El complemento de estado sin conexión de ejemplo es un complemento COM que se agrega un menú de **Estado desconectado** a Outlook y usa la API de estado sin conexión. A través del menú de estado desconectado, puede habilitar o deshabilitar la supervisión de estado, compruebe el estado actual y cambiar el estado actual. Para obtener más información sobre cómo descargar e instalar el complemento de ejemplo desconectado estado, vea [instalar el complemento de estado sin conexión de ejemplo](installing-the-sample-offline-state-add-in.md). Para obtener más información acerca de la API de estado sin conexión, vea [Acerca de la sin conexión estado API](about-the-offline-state-api.md).
  
## <a name="on-disconnection-routine"></a>En la rutina de desconexión

Se llama al método de **IDTExtensibility2.OnDisconnection** cuando el estado sin conexión complemento se descarga. Debe implementar una limpieza de código en esta función. En el siguiente ejemplo, llama la función **IDTExtensibility2.OnDisconnection** el `HrTermAddin` (función). 
  
### <a name="cmyaddinondisconnection-example"></a>Ejemplo de CMyAddin::OnDisconnection()

```cpp
STDMETHODIMP CMyAddin::OnDisconnection(ext_DisconnectMode /*RemoveMode*/, SAFEARRAY * * /*custom*/) 
{ 
    Log(true,"OnDisconnection\n"); 
    HRESULT hRes = S_OK; 
    hRes = HrTermAddin(); 
     return hRes; 
}
```

## <a name="terminate-add-in-function"></a>Terminar complemento (función)

El `HrTermAddin` llamadas a función el `inDeInitMonitor`, `HrRemoveMenuItems`, y `UnloadLibraries` funciones para terminar de limpiar el complemento estado sin conexión. 
  
### <a name="cmyaddinhrtermaddin-example"></a>Ejemplo de CMyAddin::HrTermAddin()

```cpp
HRESULT CMyAddin::HrTermAddin() 
{ 
    HRESULT hRes = S_OK; 
    DeInitMonitor(); 
    hRes =  HrRemoveMenuItems(); 
    UnloadLibraries(); 
    return hRes; 
}
```

## <a name="deinitialize-monitor-routine"></a>Deinitialize rutina de Monitor

El `inDeInitMonitor` función llama a la función [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) para cancelar las devoluciones de llamada para el objeto sin conexión. 
  
### <a name="deinitmonitor-example"></a>Ejemplo de DeInitMonitor()

```cpp
void DeInitMonitor() 
{ 
Log(true,_T("Deinitializing Outlook Offline State Monitor\n")); 
HRESULT hRes = S_OK; 
if (g_lpOfflineMgr) 
{ 
hRes = g_lpOfflineMgr->Unadvise(MAPIOFFLINE_UNADVISE_DEFAULT, g_ulAdviseToken); 
g_lpOfflineMgr->Release(); 
g_lpOfflineMgr = NULL; 
g_ulAdviseToken = NULL; 
} 
}
```

## <a name="remove-menu-items-routine"></a>Quitar la rutina de los elementos de menú

El `HrRemoveMenuItems` llamadas a función `DispEventUnadvise` para cada elemento de menú en el menú de **Estado sin conexión** y, a continuación, elimina el menú de **Estado sin conexión** . 
  
### <a name="cmyaddinhrremovemenuitems-example"></a>Ejemplo de CMyAddin::HrRemoveMenuItems()

```cpp
HRESULT CMyAddin::HrRemoveMenuItems() 
{     
    Log(true,"HrRemoveMenuItems\n"); 
    HRESULT hRes = S_OK; 
    if (m_fMenuItemsAdded) 
    { 
        try 
        { 
            if (m_spInitButton) 
            { 
                m_InitButtonHandler.DispEventUnadvise(m_spInitButton); 
            } 
            if (m_spDeinitButton) 
            { 
                m_DeinitButtonHandler.DispEventUnadvise(m_spDeinitButton); 
            } 
            if (m_spGetStateButton) 
            { 
                m_GetStateButtonHandler.DispEventUnadvise(m_spGetStateButton); 
            } 
            if (m_spSetStateButton) 
            { 
                m_SetStateButtonHandler.DispEventUnadvise(m_spSetStateButton); 
            } 
 
            m_spMyMenu->Delete(); 
        } 
        catch(_com_error) 
        { 
            hRes = E_FAIL; 
        } 
        if (SUCCEEDED(hRes)) 
        { 
            m_fMenuItemsAdded = false; 
        } 
    } 
    return hRes; 
}
```

## <a name="unload-libraries-routine"></a>Descargar la rutina de bibliotecas

Cuando el complemento se descarga desde Outlook, el `UnloadLibraries` función descarga las bibliotecas de vínculos dinámicos (DLL) que el complemento necesario. 
  
### <a name="unloadlibraries-example"></a>Ejemplo de UnloadLibraries()

```cpp
void UnloadLibraries() 
{ 
    Log(true,_T("UnloadLibraries - freeing modules\n")); 
    pfnHrOpenOfflineObj = NULL; 
    pfnMAPIFreeBuffer = NULL; 
    if (hModMSMAPI) FreeLibrary(hModMSMAPI); 
    hModMSMAPI = NULL; 
    if (hModMAPI) FreeLibrary(hModMAPI); 
    hModMAPI = NULL; 
    if (hModMAPIStub) FreeLibrary(hModMAPIStub); 
    hModMAPIStub = NULL; 
}
```

## <a name="see-also"></a>Ver también

- [Acerca de la API de estado sin conexión](about-the-offline-state-api.md)
- [Instalar el ejemplo sin conexión estado Add-in](installing-the-sample-offline-state-add-in.md)
- [Acerca del ejemplo sin conexión de estado complemento:](about-the-sample-offline-state-add-in.md)
- [Configurar un sin conexión estado Add-in](setting-up-an-offline-state-add-in.md)
- [Supervisión de estado de conexión cambia mediante un sin conexión estado Add-in](monitoring-connection-state-changes-using-an-offline-state-add-in.md)

