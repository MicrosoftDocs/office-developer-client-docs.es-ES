---
title: Desconectar un complemento de estado sin conexión
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
# <a name="disconnecting-an-offline-state-add-in"></a><span data-ttu-id="b6ae6-103">Desconectar un complemento de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="b6ae6-103">Disconnecting an Offline State Add-in</span></span>

<span data-ttu-id="b6ae6-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b6ae6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b6ae6-105">Cuando el estado sin conexión complemento está desconectado, debe implementar las funciones para terminar y limpiar el complemento correctamente.</span><span class="sxs-lookup"><span data-stu-id="b6ae6-105">When the offline state add-in is disconnected, you must implement functions to properly terminate and clean up the add-in.</span></span> <span data-ttu-id="b6ae6-106">Para obtener más información sobre la configuración y el uso sin conexión de estado complemento para supervisar los cambios de estado de conexión, vea [Agregar en configuración de seguridad de un estado sin conexión](setting-up-an-offline-state-add-in.md) y [Supervisión conexión el estado de los cambios utilizando un complemento de estado sin conexión](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="b6ae6-106">For more information on setting up and using the offline state add-in to monitor connection state changes, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md) and [Monitoring Connection State Changes Using an Offline State Add-in](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span></span>
  
<span data-ttu-id="b6ae6-107">En este tema, estos desconexión, terminar y se muestran las funciones de limpieza mediante el uso de los ejemplos de código desde el complemento de estado sin conexión de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b6ae6-107">In this topic, these disconnection, terminate, and clean-up functions are demonstrated by using code examples from the Sample Offline State Add-in.</span></span> <span data-ttu-id="b6ae6-108">El complemento de estado sin conexión de ejemplo es un complemento COM que se agrega un menú de **Estado desconectado** a Outlook y usa la API de estado sin conexión.</span><span class="sxs-lookup"><span data-stu-id="b6ae6-108">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and uses the Offline State API.</span></span> <span data-ttu-id="b6ae6-109">A través del menú de estado desconectado, puede habilitar o deshabilitar la supervisión de estado, compruebe el estado actual y cambiar el estado actual.</span><span class="sxs-lookup"><span data-stu-id="b6ae6-109">Through the Offline State menu, you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="b6ae6-110">Para obtener más información sobre cómo descargar e instalar el complemento de ejemplo desconectado estado, vea [instalar el complemento de estado sin conexión de ejemplo](installing-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="b6ae6-110">For more information about downloading and installing the Sample Offline State Add-in, see [Installing the Sample Offline State Add-in](installing-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="b6ae6-111">Para obtener más información acerca de la API de estado sin conexión, vea [Acerca de la sin conexión estado API](about-the-offline-state-api.md).</span><span class="sxs-lookup"><span data-stu-id="b6ae6-111">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
## <a name="on-disconnection-routine"></a><span data-ttu-id="b6ae6-112">En la rutina de desconexión</span><span class="sxs-lookup"><span data-stu-id="b6ae6-112">On Disconnection Routine</span></span>

<span data-ttu-id="b6ae6-113">Se llama al método de **IDTExtensibility2.OnDisconnection** cuando el estado sin conexión complemento se descarga.</span><span class="sxs-lookup"><span data-stu-id="b6ae6-113">The **IDTExtensibility2.OnDisconnection** method is called when the Offline State Add-in is unloaded.</span></span> <span data-ttu-id="b6ae6-114">Debe implementar una limpieza de código en esta función.</span><span class="sxs-lookup"><span data-stu-id="b6ae6-114">You should implement clean up code in this function.</span></span> <span data-ttu-id="b6ae6-115">En el siguiente ejemplo, llama la función **IDTExtensibility2.OnDisconnection** el `HrTermAddin` (función).</span><span class="sxs-lookup"><span data-stu-id="b6ae6-115">In the following example, the **IDTExtensibility2.OnDisconnection** function calls the  `HrTermAddin` function.</span></span> 
  
### <a name="cmyaddinondisconnection-example"></a><span data-ttu-id="b6ae6-116">Ejemplo de CMyAddin::OnDisconnection()</span><span class="sxs-lookup"><span data-stu-id="b6ae6-116">CMyAddin::OnDisconnection() example</span></span>

```cpp
STDMETHODIMP CMyAddin::OnDisconnection(ext_DisconnectMode /*RemoveMode*/, SAFEARRAY * * /*custom*/) 
{ 
    Log(true,"OnDisconnection\n"); 
    HRESULT hRes = S_OK; 
    hRes = HrTermAddin(); 
     return hRes; 
}
```

## <a name="terminate-add-in-function"></a><span data-ttu-id="b6ae6-117">Terminar complemento (función)</span><span class="sxs-lookup"><span data-stu-id="b6ae6-117">Terminate Add-in Function</span></span>

<span data-ttu-id="b6ae6-118">El `HrTermAddin` llamadas a función el `inDeInitMonitor`, `HrRemoveMenuItems`, y `UnloadLibraries` funciones para terminar de limpiar el complemento estado sin conexión.</span><span class="sxs-lookup"><span data-stu-id="b6ae6-118">The  `HrTermAddin` function calls the  `inDeInitMonitor`,  `HrRemoveMenuItems`, and  `UnloadLibraries` functions to finish cleaning up the Offline State Add-in.</span></span> 
  
### <a name="cmyaddinhrtermaddin-example"></a><span data-ttu-id="b6ae6-119">Ejemplo de CMyAddin::HrTermAddin()</span><span class="sxs-lookup"><span data-stu-id="b6ae6-119">CMyAddin::HrTermAddin() example</span></span>

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

## <a name="deinitialize-monitor-routine"></a><span data-ttu-id="b6ae6-120">Deinitialize rutina de Monitor</span><span class="sxs-lookup"><span data-stu-id="b6ae6-120">Deinitialize Monitor Routine</span></span>

<span data-ttu-id="b6ae6-121">El `inDeInitMonitor` función llama a la función [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) para cancelar las devoluciones de llamada para el objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="b6ae6-121">The  `inDeInitMonitor` function calls the [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) function to cancel the callbacks for the offline object.</span></span> 
  
### <a name="deinitmonitor-example"></a><span data-ttu-id="b6ae6-122">Ejemplo de DeInitMonitor()</span><span class="sxs-lookup"><span data-stu-id="b6ae6-122">DeInitMonitor() example</span></span>

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

## <a name="remove-menu-items-routine"></a><span data-ttu-id="b6ae6-123">Quitar la rutina de los elementos de menú</span><span class="sxs-lookup"><span data-stu-id="b6ae6-123">Remove Menu Items Routine</span></span>

<span data-ttu-id="b6ae6-124">El `HrRemoveMenuItems` llamadas a función `DispEventUnadvise` para cada elemento de menú en el menú de **Estado sin conexión** y, a continuación, elimina el menú de **Estado sin conexión** .</span><span class="sxs-lookup"><span data-stu-id="b6ae6-124">The  `HrRemoveMenuItems` function calls  `DispEventUnadvise` for each menu item under the **Offline State** menu, and then deletes the **Offline State** menu.</span></span> 
  
### <a name="cmyaddinhrremovemenuitems-example"></a><span data-ttu-id="b6ae6-125">Ejemplo de CMyAddin::HrRemoveMenuItems()</span><span class="sxs-lookup"><span data-stu-id="b6ae6-125">CMyAddin::HrRemoveMenuItems() example</span></span>

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

## <a name="unload-libraries-routine"></a><span data-ttu-id="b6ae6-126">Descargar la rutina de bibliotecas</span><span class="sxs-lookup"><span data-stu-id="b6ae6-126">Unload Libraries Routine</span></span>

<span data-ttu-id="b6ae6-127">Cuando el complemento se descarga desde Outlook, el `UnloadLibraries` función descarga las bibliotecas de vínculos dinámicos (DLL) que el complemento necesario.</span><span class="sxs-lookup"><span data-stu-id="b6ae6-127">When the add-in is unloaded from Outlook, the  `UnloadLibraries` function unloads the dynamic-link libraries (DLLs) that the add-in required.</span></span> 
  
### <a name="unloadlibraries-example"></a><span data-ttu-id="b6ae6-128">Ejemplo de UnloadLibraries()</span><span class="sxs-lookup"><span data-stu-id="b6ae6-128">UnloadLibraries() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="b6ae6-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6ae6-129">See also</span></span>

- [<span data-ttu-id="b6ae6-130">Información sobre la API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="b6ae6-130">About the Offline State API</span></span>](about-the-offline-state-api.md)
- [<span data-ttu-id="b6ae6-131">Instalar el complemento de estado sin conexión de muestra</span><span class="sxs-lookup"><span data-stu-id="b6ae6-131">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="b6ae6-132">Información sobre el complemento de estado sin conexión de muestra</span><span class="sxs-lookup"><span data-stu-id="b6ae6-132">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="b6ae6-133">Configurar un complemento de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="b6ae6-133">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
- [<span data-ttu-id="b6ae6-134">Supervisar los cambios estado de conexión con un complemento de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="b6ae6-134">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)

