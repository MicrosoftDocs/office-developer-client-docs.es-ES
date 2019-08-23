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
# <a name="disconnecting-an-offline-state-add-in"></a><span data-ttu-id="9ae48-103">Desconectar un complemento de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="9ae48-103">Disconnecting an Offline State Add-in</span></span>

<span data-ttu-id="9ae48-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ae48-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ae48-105">Cuando el complemento de estado sin conexión está desconectado, deberá implementar funciones para finalizar correctamente y limpiar el complemento.</span><span class="sxs-lookup"><span data-stu-id="9ae48-105">When the offline state add-in is disconnected, you must implement functions to properly terminate and clean up the add-in.</span></span> <span data-ttu-id="9ae48-106">Para obtener más información sobre cómo configurar y usar el complemento de estado sin conexión para supervisar los cambios de estado de conexión, vea [Configurar un complemento de estado sin conexión](setting-up-an-offline-state-add-in.md) y [Supervisar los cambios de estado de conexión con un complemento de estado sin conexión](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="9ae48-106">For more information on setting up and using the offline state add-in to monitor connection state changes, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md) and [Monitoring Connection State Changes Using an Offline State Add-in](monitoring-connection-state-changes-using-an-offline-state-add-in.md).</span></span>
  
<span data-ttu-id="9ae48-107">En este artículo, se muestran estas funciones de desconexión, finalización y limpieza mediante ejemplos de código desde el complemento de estado sin conexión de muestra.</span><span class="sxs-lookup"><span data-stu-id="9ae48-107">In this topic, these disconnection, terminate, and clean-up functions are demonstrated by using code examples from the Sample Offline State Add-in.</span></span> <span data-ttu-id="9ae48-108">El complemento estado sin conexión de muestra es un complemento COM que agrega un menú **Estado sin conexión** a Outlook y usa la API de estado sin conexión.</span><span class="sxs-lookup"><span data-stu-id="9ae48-108">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and uses the Offline State API.</span></span> <span data-ttu-id="9ae48-109">Mediante el menú estado sin conexión, se puede habilitar o deshabilitar la supervisión del estado, comprobar el estado actual y cambiar el estado actual.</span><span class="sxs-lookup"><span data-stu-id="9ae48-109">Through the Offline State menu, you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="9ae48-110">Para obtener más información sobre cómo descargar e instalar el complemento estado sin conexión de muestra, vea [Instalar el complemento de estado sin conexión de muestra](installing-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="9ae48-110">For more information about downloading and installing the Sample Offline State Add-in, see [Installing the Sample Offline State Add-in](installing-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="9ae48-111">Para obtener más información acerca de la API de estado sin conexión, vea [Información sobre la API de estado sin conexión](about-the-offline-state-api.md).</span><span class="sxs-lookup"><span data-stu-id="9ae48-111">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
## <a name="on-disconnection-routine"></a><span data-ttu-id="9ae48-112">Rutina En desconexión</span><span class="sxs-lookup"><span data-stu-id="9ae48-112">On Disconnection Routine</span></span>

<span data-ttu-id="9ae48-113">Se llama al método **IDTExtensibility2.OnDisconnection** cuando el complemento de estado sin conexión se descarga.</span><span class="sxs-lookup"><span data-stu-id="9ae48-113">The **IDTExtensibility2.OnDisconnection** method is called when the Offline State Add-in is unloaded.</span></span> <span data-ttu-id="9ae48-114">Es recomendable implementar el código de limpieza en esta función.</span><span class="sxs-lookup"><span data-stu-id="9ae48-114">You should implement clean up code in this function.</span></span> <span data-ttu-id="9ae48-115">En el ejemplo siguiente, la función **IDTExtensibility2.OnDisconnection** llama a la función `HrTermAddin`.</span><span class="sxs-lookup"><span data-stu-id="9ae48-115">In the following example, the **IDTExtensibility2.OnDisconnection** function calls the  `HrTermAddin` function.</span></span> 
  
### <a name="cmyaddinondisconnection-example"></a><span data-ttu-id="9ae48-116">Ejemplo CMyAddin::OnDisconnection()</span><span class="sxs-lookup"><span data-stu-id="9ae48-116">CMyAddin::OnDisconnection() example</span></span>

```cpp
STDMETHODIMP CMyAddin::OnDisconnection(ext_DisconnectMode /*RemoveMode*/, SAFEARRAY * * /*custom*/) 
{ 
    Log(true,"OnDisconnection\n"); 
    HRESULT hRes = S_OK; 
    hRes = HrTermAddin(); 
     return hRes; 
}
```

## <a name="terminate-add-in-function"></a><span data-ttu-id="9ae48-117">Finalizar la función de complemento</span><span class="sxs-lookup"><span data-stu-id="9ae48-117">Terminate Add-in Function</span></span>

<span data-ttu-id="9ae48-118">La función `HrTermAddin` llama a las funciones `inDeInitMonitor`, `HrRemoveMenuItems`, y `UnloadLibraries` para terminar de limpiar el complemento de estado sin conexión.</span><span class="sxs-lookup"><span data-stu-id="9ae48-118">The  `HrTermAddin` function calls the  `inDeInitMonitor`,  `HrRemoveMenuItems`, and  `UnloadLibraries` functions to finish cleaning up the Offline State Add-in.</span></span> 
  
### <a name="cmyaddinhrtermaddin-example"></a><span data-ttu-id="9ae48-119">Ejemplo CMyAddin::HrTermAddin()</span><span class="sxs-lookup"><span data-stu-id="9ae48-119">CMyAddin::HrTermAddin() example</span></span>

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

## <a name="deinitialize-monitor-routine"></a><span data-ttu-id="9ae48-120">Rutina Desinicializar supervisión</span><span class="sxs-lookup"><span data-stu-id="9ae48-120">Deinitialize Monitor Routine</span></span>

<span data-ttu-id="9ae48-121">La función `inDeInitMonitor` llama a la función [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) para cancelar las retrollamadas del objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="9ae48-121">The  `inDeInitMonitor` function calls the [IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md) function to cancel the callbacks for the offline object.</span></span> 
  
### <a name="deinitmonitor-example"></a><span data-ttu-id="9ae48-122">Ejemplo DeInitMonitor()</span><span class="sxs-lookup"><span data-stu-id="9ae48-122">DeInitMonitor() example</span></span>

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

## <a name="remove-menu-items-routine"></a><span data-ttu-id="9ae48-123">Rutina Quitar elementos de menú</span><span class="sxs-lookup"><span data-stu-id="9ae48-123">Remove Menu Items Routine</span></span>

<span data-ttu-id="9ae48-124">La función `HrRemoveMenuItems` llama a `DispEventUnadvise` para cada elemento del menú en el menú **Estado sin conexión** y después elimina el menú **Estado sin conexión**.</span><span class="sxs-lookup"><span data-stu-id="9ae48-124">The  `HrRemoveMenuItems` function calls  `DispEventUnadvise` for each menu item under the **Offline State** menu, and then deletes the **Offline State** menu.</span></span> 
  
### <a name="cmyaddinhrremovemenuitems-example"></a><span data-ttu-id="9ae48-125">Ejemplo CMyAddin::HrRemoveMenuItems() </span><span class="sxs-lookup"><span data-stu-id="9ae48-125">CMyAddin::HrRemoveMenuItems() example</span></span>

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

## <a name="unload-libraries-routine"></a><span data-ttu-id="9ae48-126">Rutina Descargar bibliotecas</span><span class="sxs-lookup"><span data-stu-id="9ae48-126">Unload Libraries Routine</span></span>

<span data-ttu-id="9ae48-127">Cuando el complemento se descarga desde Outlook, la función `UnloadLibraries` descarga las bibliotecas de vínculos dinámicos (DLL) que el complemento necesita.</span><span class="sxs-lookup"><span data-stu-id="9ae48-127">When the add-in is unloaded from Outlook, the  `UnloadLibraries` function unloads the dynamic-link libraries (DLLs) that the add-in required.</span></span> 
  
### <a name="unloadlibraries-example"></a><span data-ttu-id="9ae48-128">Ejemplo UnloadLibraries()</span><span class="sxs-lookup"><span data-stu-id="9ae48-128">UnloadLibraries() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="9ae48-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ae48-129">See also</span></span>

- [<span data-ttu-id="9ae48-130">Información sobre la API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="9ae48-130">About the Offline State API</span></span>](about-the-offline-state-api.md)
- [<span data-ttu-id="9ae48-131">Instalar el complemento de estado sin conexión de muestra</span><span class="sxs-lookup"><span data-stu-id="9ae48-131">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="9ae48-132">Información sobre el complemento de estado sin conexión de muestra</span><span class="sxs-lookup"><span data-stu-id="9ae48-132">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="9ae48-133">Configurar un complemento de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="9ae48-133">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
- [<span data-ttu-id="9ae48-134">Supervisar los cambios de estado de conexión con un complemento de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="9ae48-134">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)

