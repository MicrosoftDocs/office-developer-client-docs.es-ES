---
title: Supervisión de los cambios de estado de conexión con un complemento de estado sin conexión
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c482ddce-f2b6-222b-aa30-824b1c6f3b14
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d24a6d93943883a5503b57ef223d9be777af13d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338818"
---
# <a name="monitoring-connection-state-changes-using-an-offline-state-add-in"></a><span data-ttu-id="bb88e-103">Supervisión de los cambios de estado de conexión con un complemento de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="bb88e-103">Monitoring connection state changes using an offline state add-in</span></span>

<span data-ttu-id="bb88e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb88e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb88e-105">Antes de poder usar un complemento de estado sin conexión para supervisar los cambios en el estado de conexión, debe implementar funciones para configurar e inicializar el complemento.</span><span class="sxs-lookup"><span data-stu-id="bb88e-105">Before you can use an offline state add-in to monitor connection state changes, you must implement functions to set up and initialize the add-in.</span></span> <span data-ttu-id="bb88e-106">Para obtener más información, consulte [configurar un complemento de estado sin conexión](setting-up-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="bb88e-106">For more information, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
<span data-ttu-id="bb88e-107">Después de configurar el complemento de estado sin conexión, debe usar la función **[HrOpenOfflineObj](hropenofflineobj.md)** para obtener un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="bb88e-107">After you set up the offline state add-in, you must use the **[HrOpenOfflineObj](hropenofflineobj.md)** function to obtain an offline object.</span></span> <span data-ttu-id="bb88e-108">Con este objeto sin conexión, puede inicializar el monitor de estado y, a continuación, obtener y establecer el estado actual.</span><span class="sxs-lookup"><span data-stu-id="bb88e-108">Using this offline object, you can initialize your state monitor, and then get and set the current state.</span></span> 
  
<span data-ttu-id="bb88e-109">En este tema, estas funciones de supervisión de estado se muestran mediante ejemplos de código del complemento de estado sin conexión de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="bb88e-109">In this topic, these state monitoring functions are demonstrated by using code examples from the Sample Offline State Add-in.</span></span> <span data-ttu-id="bb88e-110">El complemento de estado sin conexión de muestra es un complemento COM que agrega un menú de **estado sin conexión** a Outlook y usa la API de estado sin conexión.</span><span class="sxs-lookup"><span data-stu-id="bb88e-110">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="bb88e-111">Mediante el menú **estado sin conexión** , puede habilitar o deshabilitar la supervisión de estado, comprobar el estado actual y cambiar el estado actual.</span><span class="sxs-lookup"><span data-stu-id="bb88e-111">Through the **Offline State** menu, you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="bb88e-112">Para obtener más información sobre cómo descargar e instalar el complemento estado sin conexión de muestra, vea [Instalar el complemento de estado sin conexión de muestra](installing-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="bb88e-112">For more information about downloading and installing the Sample Offline State Add-in, see [Installing the Sample Offline State Add-in](installing-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="bb88e-113">Para obtener más información acerca de la API de estado sin conexión, vea [Información sobre la API de estado sin conexión](about-the-offline-state-api.md).</span><span class="sxs-lookup"><span data-stu-id="bb88e-113">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
<span data-ttu-id="bb88e-114">Cuando el complemento de estado sin conexión está desconectado, deberá implementar funciones para finalizar correctamente y limpiar el complemento.</span><span class="sxs-lookup"><span data-stu-id="bb88e-114">When the offline state add-in is disconnected, you must implement functions to properly terminate and clean up the add-in.</span></span> <span data-ttu-id="bb88e-115">Para obtener más información, vea [desconectar un complemento de estado sin conexión](disconnecting-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="bb88e-115">For more information, see [Disconnecting an Offline State Add-in](disconnecting-an-offline-state-add-in.md).</span></span>
  
## <a name="open-offline-object-routine"></a><span data-ttu-id="bb88e-116">Abrir rutina de objeto sin conexión</span><span class="sxs-lookup"><span data-stu-id="bb88e-116">Open Offline Object routine</span></span>

<span data-ttu-id="bb88e-117">Para que el cliente reciba una notificación cuando se produzca un cambio de estado de la conexión, debe llamar a la función **[HrOpenOfflineObj](hropenofflineobj.md)** .</span><span class="sxs-lookup"><span data-stu-id="bb88e-117">For the client to be notified when a connection state change occurs, you must call the **[HrOpenOfflineObj](hropenofflineobj.md)** function.</span></span> <span data-ttu-id="bb88e-118">Esta función abre un objeto sin conexión que admite **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span><span class="sxs-lookup"><span data-stu-id="bb88e-118">This function opens an offline object that supports **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span></span> <span data-ttu-id="bb88e-119">La función **HrOpenOfflineObj** se define en el archivo de encabezado ConnectionState. h.</span><span class="sxs-lookup"><span data-stu-id="bb88e-119">The **HrOpenOfflineObj** function is defined in the ConnectionState.h header file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="bb88e-120">La función **HrOpenOfflineObj** se declara en el archivo de encabezado ImportProcs. h de la `extern HROPENOFFLINEOBJ* pfnHrOpenOfflineObj;`siguiente manera:.</span><span class="sxs-lookup"><span data-stu-id="bb88e-120">The **HrOpenOfflineObj** function is declared in the ImportProcs.h header file as follows:  `extern HROPENOFFLINEOBJ* pfnHrOpenOfflineObj;`.</span></span> 
  
### <a name="hropenofflineobj-example"></a><span data-ttu-id="bb88e-121">Ejemplo de HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="bb88e-121">HrOpenOfflineObj example</span></span>

```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
    ULONG ulFlags, 
    LPCWSTR pwszProfileName, 
    const GUID* pGUID, 
    const GUID* pInstance, 
    IMAPIOfflineMgr** ppOffline 
);
```

## <a name="initialize-monitor-routine"></a><span data-ttu-id="bb88e-122">Rutina de inicialización de monitor</span><span class="sxs-lookup"><span data-stu-id="bb88e-122">Initialize Monitor routine</span></span>

<span data-ttu-id="bb88e-123">La `InitMonitor` función llama a la función **HrOpenOfflineObj** .</span><span class="sxs-lookup"><span data-stu-id="bb88e-123">The  `InitMonitor` function calls the **HrOpenOfflineObj** function.</span></span> <span data-ttu-id="bb88e-124">La `InitMonitor` función llama a **CMyOfflineNotify** para que Outlook pueda enviar notificaciones de devolución de llamada al cliente y registra la devolución de llamada a `AdviseInfo`través de la variable **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** .</span><span class="sxs-lookup"><span data-stu-id="bb88e-124">The  `InitMonitor` function calls **CMyOfflineNotify** so that Outlook can send callback notifications to the client, and registers the callback through the **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** variable  `AdviseInfo`.</span></span>
  
### <a name="initmonitor-example"></a><span data-ttu-id="bb88e-125">Ejemplo de InitMonitor ()</span><span class="sxs-lookup"><span data-stu-id="bb88e-125">InitMonitor() example</span></span>

```cpp
void InitMonitor(LPCWSTR szProfile) 
{ 
    if (!szProfile) return; 
    Log(true,_T("Initializing Outlook Offline State Monitor\n")); 
    HRESULT hRes = S_OK; 
 
    if (g_lpOfflineMgr) 
    { 
        Log(true,_T("Already initialized\n")); 
        return; 
    } 
     
    if (pfnHrOpenOfflineObj) 
    { 
        if (g_lpOfflineMgr) DeInitMonitor(); 
        Log(true,_T("Calling HrOpenOfflineObj for \"%ws\"\n"),szProfile); 
        hRes = pfnHrOpenOfflineObj( 
            NULL, 
            szProfile, 
            &GUID_GlobalState, 
            NULL, 
            &g_lpOfflineMgr); 
        if (FAILED(hRes))  
        { 
            Log(true,_T("HrOpenOfflineObj failed: 0x%08X\n"),hRes); 
        } 
        if (g_lpOfflineMgr) 
        { 
            IMAPIOffline* lpOffline = NULL; 
            hRes = g_lpOfflineMgr->QueryInterface(IID_IMAPIOffline,(LPVOID*)&lpOffline); 
             
            if (lpOffline) 
            { 
                ULONG ulCap = NULL; 
                hRes = lpOffline->GetCapabilities(&ulCap); 
                 
                if (ulCap & MAPIOFFLINE_CAPABILITY_OFFLINE) Log(true,_T("MAPIOFFLINE_CAPABILITY_OFFLINE supported\n")); 
                if (ulCap & MAPIOFFLINE_CAPABILITY_ONLINE) Log(true,_T("MAPIOFFLINE_CAPABILITY_ONLINE supported\n")); 
                 
                if (ulCap & (MAPIOFFLINE_CAPABILITY_OFFLINE | MAPIOFFLINE_CAPABILITY_ONLINE)) 
                { 
                    CMyOfflineNotify* lpImplNotify = new CMyOfflineNotify(); 
                     
                    if (lpImplNotify) 
                    { 
                        MAPIOFFLINE_ADVISEINFO AdviseInfo = {0}; 
                        AdviseInfo.ulSize = sizeof(MAPIOFFLINE_ADVISEINFO); 
                        AdviseInfo.ulClientToken = 0;// something you want to get handed back when you get the notification 
                        AdviseInfo.CallbackType = MAPIOFFLINE_CALLBACK_TYPE_NOTIFY; 
                        AdviseInfo.pCallback = lpImplNotify; 
                        AdviseInfo.ulAdviseTypes = MAPIOFFLINE_ADVISE_TYPE_STATECHANGE; 
                        AdviseInfo.ulStateMask = MAPIOFFLINE_STATE_ALL; 
                         
                        hRes = g_lpOfflineMgr->Advise(MAPIOFFLINE_ADVISE_DEFAULT, &AdviseInfo, &g_ulAdviseToken); 
                        Log(true,"ulAdviseToken = 0x%08X\n",g_ulAdviseToken); 
                    } 
                } 
                lpOffline->Release(); 
            }                 
        } 
    } 
}
```

## <a name="get-current-state-routine"></a><span data-ttu-id="bb88e-126">Obtener rutina de estado actual</span><span class="sxs-lookup"><span data-stu-id="bb88e-126">Get Current State routine</span></span>

<span data-ttu-id="bb88e-127">La `GetCurrentState` función llama a la función **HrOpenOfflineObj** y, a continuación, usa el objeto sin conexión para obtener el estado de conexión actual.</span><span class="sxs-lookup"><span data-stu-id="bb88e-127">The  `GetCurrentState` function calls the **HrOpenOfflineObj** function, and then uses the offline object to get the current connection state.</span></span> <span data-ttu-id="bb88e-128">El estado actual se devuelve en la `ulCurState` variable, que se usa en la `CButtonEventHandler::Click` función para mostrar el estado actual al usuario.</span><span class="sxs-lookup"><span data-stu-id="bb88e-128">The current state is returned in the  `ulCurState` variable, which is used in the  `CButtonEventHandler::Click` function to display the current state to the user.</span></span> 
  
### <a name="getcurrentstate-example"></a><span data-ttu-id="bb88e-129">Ejemplo de GetCurrentState ()</span><span class="sxs-lookup"><span data-stu-id="bb88e-129">GetCurrentState() example</span></span>

```cpp
ULONG (LPCWSTR szProfile) 
{ 
    if (!szProfile) return 0; 
    Log(true,_T("Getting Current Offline State\n")); 
    HRESULT hRes = S_OK; 
    ULONG ulCurState = NULL; 
 
    if (pfnHrOpenOfflineObj) 
    { 
        if (g_lpOfflineMgr) DeInitMonitor(); 
        Log(true,_T("Calling HrOpenOfflineObj for \"%ws\"\n"),szProfile); 
        hRes = pfnHrOpenOfflineObj( 
            NULL, 
            szProfile, 
            &GUID_GlobalState, 
            NULL, 
            &g_lpOfflineMgr); 
        if (FAILED(hRes))  
        { 
            Log(true,_T("HrOpenOfflineObj failed: 0x%08X\n"),hRes); 
        } 
        if (g_lpOfflineMgr) 
        { 
            IMAPIOffline* lpOffline = NULL; 
            hRes = g_lpOfflineMgr->QueryInterface(IID_IMAPIOffline,(LPVOID*)&lpOffline); 
             
            if (lpOffline) 
            { 
                hRes = lpOffline->GetCurrentState(&ulCurState); 
                Log(true,_T("GetCurrentState returned 0x%08X\n"),hRes); 
 
                switch(ulCurState) 
                { 
                case MAPIOFFLINE_STATE_ONLINE: 
                    Log(true,_T("Current state is MAPIOFFLINE_STATE_ONLINE\n")); 
                    break; 
                case MAPIOFFLINE_STATE_OFFLINE: 
                    Log(true,_T("Current state is MAPIOFFLINE_STATE_OFFLINE\n")); 
                    break; 
                default: 
                    Log(true,_T("Current state is 0x%0X\n"),ulCurState); 
                } 
                lpOffline->Release(); 
            } 
        } 
    } 
    return ulCurState; 
}
```

## <a name="set-current-state-routine"></a><span data-ttu-id="bb88e-130">Establecer la rutina de estado actual</span><span class="sxs-lookup"><span data-stu-id="bb88e-130">Set Current State routine</span></span>

<span data-ttu-id="bb88e-131">La `SetCurrentState` función llama a la función **HrOpenOfflineObj** y, a continuación, usa el objeto sin conexión para establecer el estado de conexión actual.</span><span class="sxs-lookup"><span data-stu-id="bb88e-131">The  `SetCurrentState` function calls the **HrOpenOfflineObj** function, and then uses the offline object to set the current connection state.</span></span> <span data-ttu-id="bb88e-132">La `CButtonEventHandler::Click` función llama a `SetCurrentState` la función y el nuevo estado se pasa a través `ulState` de la variable.</span><span class="sxs-lookup"><span data-stu-id="bb88e-132">The  `CButtonEventHandler::Click` function calls the  `SetCurrentState` function and the new state is passed in through the  `ulState` variable.</span></span> 
  
### <a name="setcurrentstate-example"></a><span data-ttu-id="bb88e-133">Ejemplo de SetCurrentState ()</span><span class="sxs-lookup"><span data-stu-id="bb88e-133">SetCurrentState() example</span></span>

```cpp
HRESULT SetCurrentState(LPCWSTR szProfile, ULONG ulFlags, ULONG ulState) 
{ 
    if (!szProfile) return 0; 
    Log(true,_T("Setting Current Offline State\n")); 
    HRESULT hRes = S_OK; 
 
    if (pfnHrOpenOfflineObj) 
    { 
        if (g_lpOfflineMgr) DeInitMonitor(); 
        Log(true,_T("Calling HrOpenOfflineObj for \"%ws\"\n"),szProfile); 
        hRes = pfnHrOpenOfflineObj( 
            NULL, 
            szProfile, 
            &GUID_GlobalState, 
            NULL, 
            &g_lpOfflineMgr); 
        if (FAILED(hRes))  
        { 
            Log(true,_T("HrOpenOfflineObj failed: 0x%08X\n"),hRes); 
        } 
        if (g_lpOfflineMgr) 
        { 
            IMAPIOffline* lpOffline = NULL; 
            hRes = g_lpOfflineMgr->QueryInterface(IID_IMAPIOffline,(LPVOID*)&lpOffline); 
             
            if (lpOffline) 
            { 
                switch(ulFlags) 
                { 
                case MAPIOFFLINE_FLAG_BLOCK: 
                    Log(true,_T("Flag used: MAPIOFFLINE_FLAG_BLOCK\n")); 
                    break; 
                case MAPIOFFLINE_FLAG_DEFAULT: 
                    Log(true,_T("Flag used: MAPIOFFLINE_FLAG_DEFAULT\n")); 
                    break; 
                default: 
                    Log(true,_T("Flag used: 0x%0X\n"),ulFlags); 
                } 
                switch(ulState) 
                { 
                case MAPIOFFLINE_STATE_ONLINE: 
                    Log(true,_T("New state will be MAPIOFFLINE_STATE_ONLINE\n")); 
                    break; 
                case MAPIOFFLINE_STATE_OFFLINE: 
                    Log(true,_T("New state will be MAPIOFFLINE_STATE_OFFLINE\n")); 
                    break; 
                default: 
                    Log(true,_T("New state will be 0x%0X\n"),ulState); 
                } 
                hRes = lpOffline->SetCurrentState(ulFlags, MAPIOFFLINE_STATE_OFFLINE_MASK,ulState,NULL); 
                Log(true,_T("SetCurrentState returned 0x%08X\n"),hRes); 
                 
                lpOffline->Release(); 
            } 
        } 
    } 
    return hRes; 
}
```

## <a name="notification-routine"></a><span data-ttu-id="bb88e-134">Rutina de notificación</span><span class="sxs-lookup"><span data-stu-id="bb88e-134">Notification routine</span></span>

<span data-ttu-id="bb88e-135">La función **[IMAPIOfflineNotify:: Notify](imapiofflinenotify-notify.md)** se usa en Outlook para enviar notificaciones a un cliente cuando hay cambios en el estado de conexión.</span><span class="sxs-lookup"><span data-stu-id="bb88e-135">The **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** function is used by Outlook to send notifications to a client when there are changes in the connection state.</span></span> 
  
### <a name="cmyofflinenotifynotify-example"></a><span data-ttu-id="bb88e-136">Ejemplo de CMyOfflineNotify:: NOTIFY ()</span><span class="sxs-lookup"><span data-stu-id="bb88e-136">CMyOfflineNotify::Notify() example</span></span>

```cpp
void CMyOfflineNotify::Notify(const MAPIOFFLINE_NOTIFY *pNotifyInfo) 
{ 
    Log(true,_T("CMyOfflineNotify::Notify\n")); 
    if    (pNotifyInfo == NULL) 
    {     
        Log(true,_T("pNotifyInfo is NULL\n")); 
    } 
    else 
    { 
        Log(true,_T("pNotifyInfo->ulSize == 0x%0X\n"),pNotifyInfo->ulSize); 
        switch(pNotifyInfo->NotifyType) 
        { 
            case    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE: 
                Log(true,_T("pNotifyInfo->NotifyType == MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE\n")); 
                break; 
            case    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START: 
                Log(true,_T("pNotifyInfo->NotifyType == MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START\n")); 
                break; 
            case    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE: 
                Log(true,_T("pNotifyInfo->NotifyType == MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE\n")); 
                break; 
            default: 
                Log(true,_T("pNotifyInfo->NotifyType == 0x%08X\n"),pNotifyInfo->NotifyType); 
        } 
        Log(true,_T("pNotifyInfo->ulClientToken == 0x%0X\n"),pNotifyInfo->ulClientToken); 
        switch(pNotifyInfo->Info.StateChange.ulMask) 
        { 
            case    MAPIOFFLINE_STATE_OFFLINE_MASK: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulMask == MAPIOFFLINE_STATE_OFFLINE_MASK\n")); 
                break; 
            default: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulMask == 0x%0X\n"),pNotifyInfo->Info.StateChange.ulMask); 
        } 
        switch(pNotifyInfo->Info.StateChange.ulStateOld) 
        { 
            case    MAPIOFFLINE_STATE_ONLINE: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateOld == MAPIOFFLINE_STATE_ONLINE\n")); 
                break; 
            case    MAPIOFFLINE_STATE_OFFLINE: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateOld == MAPIOFFLINE_STATE_OFFLINE\n")); 
                break; 
            default: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateOld == 0x%0X\n"),pNotifyInfo->Info.StateChange.ulStateOld); 
        } 
        switch(pNotifyInfo->Info.StateChange.ulStateNew) 
        { 
            case    MAPIOFFLINE_STATE_ONLINE: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateNew == MAPIOFFLINE_STATE_ONLINE\n")); 
                break; 
            case    MAPIOFFLINE_STATE_OFFLINE: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateNew == MAPIOFFLINE_STATE_OFFLINE\n")); 
                break; 
            default: 
                Log(true,_T("pNotifyInfo->Info.StateChange.ulStateNew == 0x%0X\n"),pNotifyInfo->Info.StateChange.ulStateNew); 
        } 
    } 
    return; 
}
```

## <a name="see-also"></a><span data-ttu-id="bb88e-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb88e-137">See also</span></span>

- [<span data-ttu-id="bb88e-138">Información sobre la API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="bb88e-138">About the Offline State API</span></span>](about-the-offline-state-api.md)
- [<span data-ttu-id="bb88e-139">Instalar el complemento de estado sin conexión de muestra</span><span class="sxs-lookup"><span data-stu-id="bb88e-139">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="bb88e-140">Información sobre el complemento de estado sin conexión de muestra</span><span class="sxs-lookup"><span data-stu-id="bb88e-140">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="bb88e-141">Configurar un complemento de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="bb88e-141">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
- [<span data-ttu-id="bb88e-142">Desconexión de un complemento de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="bb88e-142">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

