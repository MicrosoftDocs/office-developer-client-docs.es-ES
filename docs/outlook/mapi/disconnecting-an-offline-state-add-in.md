---
title: Desconectar un complemento de estado sin conexión
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6922cb38-a9e3-e4a9-d4a3-e11b81fc77e2
description: 'Última modificación: 07 de diciembre de 2015'
ms.openlocfilehash: c665bae57a72428df7acd92e080f7c31b131253b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316656"
---
# <a name="disconnecting-an-offline-state-add-in"></a>Desconectar un complemento de estado sin conexión

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Cuando el complemento de estado sin conexión está desconectado, deberá implementar funciones para finalizar correctamente y limpiar el complemento. Para obtener más información sobre cómo configurar y usar el complemento de estado sin conexión para supervisar los cambios de estado de conexión, vea [Configurar un complemento de estado sin conexión](setting-up-an-offline-state-add-in.md) y [Supervisar los cambios de estado de conexión con un complemento de estado sin conexión](monitoring-connection-state-changes-using-an-offline-state-add-in.md).
  
En este artículo, se muestran estas funciones de desconexión, finalización y limpieza mediante ejemplos de código desde el complemento de estado sin conexión de muestra. El complemento estado sin conexión de muestra es un complemento COM que agrega un menú **Estado sin conexión** a Outlook y usa la API de estado sin conexión. Mediante el menú estado sin conexión, se puede habilitar o deshabilitar la supervisión del estado, comprobar el estado actual y cambiar el estado actual. Para obtener más información sobre cómo descargar e instalar el complemento estado sin conexión de muestra, vea [Instalar el complemento de estado sin conexión de muestra](installing-the-sample-offline-state-add-in.md). Para obtener más información acerca de la API de estado sin conexión, vea [Información sobre la API de estado sin conexión](about-the-offline-state-api.md).
  
## <a name="on-disconnection-routine"></a>Rutina En desconexión

Se llama al método **IDTExtensibility2.OnDisconnection** cuando el complemento de estado sin conexión se descarga. Es recomendable implementar el código de limpieza en esta función. En el ejemplo siguiente, la función **IDTExtensibility2.OnDisconnection** llama a la función `HrTermAddin`. 
  
### <a name="cmyaddinondisconnection-example"></a>Ejemplo CMyAddin::OnDisconnection()

```cpp
STDMETHODIMP CMyAddin::OnDisconnection(ext_DisconnectMode /*RemoveMode*/, SAFEARRAY * * /*custom*/) 
{ 
    Log(true,"OnDisconnection\n"); 
    HRESULT hRes = S_OK; 
    hRes = HrTermAddin(); 
     return hRes; 
}
```

## <a name="terminate-add-in-function"></a>Finalizar la función de complemento

La función `HrTermAddin` llama a las funciones `inDeInitMonitor`, `HrRemoveMenuItems`, y `UnloadLibraries` para terminar de limpiar el complemento de estado sin conexión. 
  
### <a name="cmyaddinhrtermaddin-example"></a>Ejemplo CMyAddin::HrTermAddin()

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

## <a name="deinitialize-monitor-routine"></a>Rutina Desinicializar supervisión

La función `inDeInitMonitor` llama a la función [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) para cancelar las retrollamadas del objeto sin conexión. 
  
### <a name="deinitmonitor-example"></a>Ejemplo DeInitMonitor()

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

## <a name="remove-menu-items-routine"></a>Rutina Quitar elementos de menú

La función `HrRemoveMenuItems` llama a `DispEventUnadvise` para cada elemento del menú en el menú **Estado sin conexión** y después elimina el menú **Estado sin conexión**. 
  
### <a name="cmyaddinhrremovemenuitems-example"></a>Ejemplo CMyAddin::HrRemoveMenuItems() 

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

## <a name="unload-libraries-routine"></a>Rutina Descargar bibliotecas

Cuando el complemento se descarga desde Outlook, la función `UnloadLibraries` descarga las bibliotecas de vínculos dinámicos (DLL) que el complemento necesita. 
  
### <a name="unloadlibraries-example"></a>Ejemplo UnloadLibraries()

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

## <a name="see-also"></a>Vea también

- [Información sobre la API de estado sin conexión](about-the-offline-state-api.md)
- [Instalar el complemento de estado sin conexión de muestra](installing-the-sample-offline-state-add-in.md)
- [Información sobre el complemento de estado sin conexión de muestra](about-the-sample-offline-state-add-in.md)
- [Configurar un complemento de estado sin conexión](setting-up-an-offline-state-add-in.md)
- [Supervisar los cambios de estado de conexión con un complemento de estado sin conexión](monitoring-connection-state-changes-using-an-offline-state-add-in.md)

