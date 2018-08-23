---
title: Supervisión de los cambios de estado de conexión con un complemento en el estado sin conexión
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c482ddce-f2b6-222b-aa30-824b1c6f3b14
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d8385b2379f2fde8689ae2c7fc5d177af696f22e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579882"
---
# <a name="monitoring-connection-state-changes-using-an-offline-state-add-in"></a><span data-ttu-id="54ee3-103">Supervisión de los cambios de estado de conexión con un complemento en el estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="54ee3-103">Monitoring connection state changes using an offline state add-in</span></span>

<span data-ttu-id="54ee3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54ee3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54ee3-105">Antes de que puede usar un complemento de estado sin conexión para supervisar los cambios de estado de conexión, debe implementar las funciones para configurar e inicializar el complemento.</span><span class="sxs-lookup"><span data-stu-id="54ee3-105">Before you can use an offline state add-in to monitor connection state changes, you must implement functions to set up and initialize the add-in.</span></span> <span data-ttu-id="54ee3-106">Para obtener más información, vea [Agregar en configuración de seguridad de un estado no conectado](setting-up-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="54ee3-106">For more information, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
<span data-ttu-id="54ee3-107">Después de configurar el complemento en el estado sin conexión, debe usar la función **[HrOpenOfflineObj](hropenofflineobj.md)** para obtener un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="54ee3-107">After you set up the offline state add-in, you must use the **[HrOpenOfflineObj](hropenofflineobj.md)** function to obtain an offline object.</span></span> <span data-ttu-id="54ee3-108">Con este objeto sin conexión, puede inicializar al monitor de estado y, a continuación, obtener y establecer el estado actual.</span><span class="sxs-lookup"><span data-stu-id="54ee3-108">Using this offline object, you can initialize your state monitor, and then get and set the current state.</span></span> 
  
<span data-ttu-id="54ee3-109">En este tema, se muestran estas funciones de supervisión de estado mediante el uso de los ejemplos de código desde el complemento de estado sin conexión de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="54ee3-109">In this topic, these state monitoring functions are demonstrated by using code examples from the Sample Offline State Add-in.</span></span> <span data-ttu-id="54ee3-110">El complemento de estado sin conexión de ejemplo es un complemento COM que se agrega un menú de **Estado desconectado** a Outlook y utiliza la API de estado sin conexión.</span><span class="sxs-lookup"><span data-stu-id="54ee3-110">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="54ee3-111">A través del menú de **Estado desconectado** , puede habilitar o deshabilitar la supervisión de estado, compruebe el estado actual y cambiar el estado actual.</span><span class="sxs-lookup"><span data-stu-id="54ee3-111">Through the **Offline State** menu, you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="54ee3-112">Para obtener más información sobre cómo descargar e instalar el complemento de ejemplo desconectado estado, vea [instalar el complemento de estado sin conexión de ejemplo](installing-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="54ee3-112">For more information about downloading and installing the Sample Offline State Add-in, see [Installing the Sample Offline State Add-in](installing-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="54ee3-113">Para obtener más información acerca de la API de estado sin conexión, vea [Acerca de la sin conexión estado API](about-the-offline-state-api.md).</span><span class="sxs-lookup"><span data-stu-id="54ee3-113">For more information about the Offline State API, see [About the Offline State API](about-the-offline-state-api.md).</span></span>
  
<span data-ttu-id="54ee3-114">Cuando el estado sin conexión complemento está desconectado, debe implementar las funciones para terminar y limpiar el complemento correctamente.</span><span class="sxs-lookup"><span data-stu-id="54ee3-114">When the offline state add-in is disconnected, you must implement functions to properly terminate and clean up the add-in.</span></span> <span data-ttu-id="54ee3-115">Para obtener más información, vea [desconectar un complemento estado sin conexión](disconnecting-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="54ee3-115">For more information, see [Disconnecting an Offline State Add-in](disconnecting-an-offline-state-add-in.md).</span></span>
  
## <a name="open-offline-object-routine"></a><span data-ttu-id="54ee3-116">Rutina de apertura objeto sin conexión</span><span class="sxs-lookup"><span data-stu-id="54ee3-116">Open Offline Object routine</span></span>

<span data-ttu-id="54ee3-117">Para que el cliente recibir una notificación cuando se produce un cambio de estado de conexión, debe llamar a la función **[HrOpenOfflineObj](hropenofflineobj.md)** .</span><span class="sxs-lookup"><span data-stu-id="54ee3-117">For the client to be notified when a connection state change occurs, you must call the **[HrOpenOfflineObj](hropenofflineobj.md)** function.</span></span> <span data-ttu-id="54ee3-118">Esta función abre un objeto sin conexión que admite **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span><span class="sxs-lookup"><span data-stu-id="54ee3-118">This function opens an offline object that supports **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span></span> <span data-ttu-id="54ee3-119">La función **HrOpenOfflineObj** se define en el archivo de encabezado ConnectionState.h.</span><span class="sxs-lookup"><span data-stu-id="54ee3-119">The **HrOpenOfflineObj** function is defined in the ConnectionState.h header file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="54ee3-120">La función **HrOpenOfflineObj** se declara en el archivo de encabezado ImportProcs.h como se indica a continuación: `extern HROPENOFFLINEOBJ* pfnHrOpenOfflineObj;`.</span><span class="sxs-lookup"><span data-stu-id="54ee3-120">The **HrOpenOfflineObj** function is declared in the ImportProcs.h header file as follows:  `extern HROPENOFFLINEOBJ* pfnHrOpenOfflineObj;`.</span></span> 
  
### <a name="hropenofflineobj-example"></a><span data-ttu-id="54ee3-121">Ejemplo de HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="54ee3-121">HrOpenOfflineObj example</span></span>

```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
    ULONG ulFlags, 
    LPCWSTR pwszProfileName, 
    const GUID* pGUID, 
    const GUID* pInstance, 
    IMAPIOfflineMgr** ppOffline 
);
```

## <a name="initialize-monitor-routine"></a><span data-ttu-id="54ee3-122">Inicializar la rutina de Monitor</span><span class="sxs-lookup"><span data-stu-id="54ee3-122">Initialize Monitor routine</span></span>

<span data-ttu-id="54ee3-123">El `InitMonitor` función llama a la función **HrOpenOfflineObj** .</span><span class="sxs-lookup"><span data-stu-id="54ee3-123">The  `InitMonitor` function calls the **HrOpenOfflineObj** function.</span></span> <span data-ttu-id="54ee3-124">El `InitMonitor` función llama a **CMyOfflineNotify** , por lo que Outlook puede enviar notificaciones de devolución de llamada al cliente y registra la devolución de llamada a través de la variable **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** `AdviseInfo`.</span><span class="sxs-lookup"><span data-stu-id="54ee3-124">The  `InitMonitor` function calls **CMyOfflineNotify** so that Outlook can send callback notifications to the client, and registers the callback through the **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** variable  `AdviseInfo`.</span></span>
  
### <a name="initmonitor-example"></a><span data-ttu-id="54ee3-125">Ejemplo de InitMonitor()</span><span class="sxs-lookup"><span data-stu-id="54ee3-125">InitMonitor() example</span></span>

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

## <a name="get-current-state-routine"></a><span data-ttu-id="54ee3-126">Rutina de estado actual de Get</span><span class="sxs-lookup"><span data-stu-id="54ee3-126">Get Current State routine</span></span>

<span data-ttu-id="54ee3-127">El `GetCurrentState` función llama a la función **HrOpenOfflineObj** y, a continuación, se utiliza el objeto sin conexión para obtener el estado de conexión actual.</span><span class="sxs-lookup"><span data-stu-id="54ee3-127">The  `GetCurrentState` function calls the **HrOpenOfflineObj** function, and then uses the offline object to get the current connection state.</span></span> <span data-ttu-id="54ee3-128">Se devuelve el estado actual de la `ulCurState` variable, que se usa en el `CButtonEventHandler::Click` función para mostrar el estado actual para el usuario.</span><span class="sxs-lookup"><span data-stu-id="54ee3-128">The current state is returned in the  `ulCurState` variable, which is used in the  `CButtonEventHandler::Click` function to display the current state to the user.</span></span> 
  
### <a name="getcurrentstate-example"></a><span data-ttu-id="54ee3-129">Ejemplo de GetCurrentState()</span><span class="sxs-lookup"><span data-stu-id="54ee3-129">GetCurrentState() example</span></span>

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

## <a name="set-current-state-routine"></a><span data-ttu-id="54ee3-130">Rutina de establecer el estado actual</span><span class="sxs-lookup"><span data-stu-id="54ee3-130">Set Current State routine</span></span>

<span data-ttu-id="54ee3-131">El `SetCurrentState` función llama a la función **HrOpenOfflineObj** y, a continuación, se utiliza el objeto sin conexión para establecer el estado de conexión actual.</span><span class="sxs-lookup"><span data-stu-id="54ee3-131">The  `SetCurrentState` function calls the **HrOpenOfflineObj** function, and then uses the offline object to set the current connection state.</span></span> <span data-ttu-id="54ee3-132">El `CButtonEventHandler::Click` llamadas a función el `SetCurrentState` (función) y el nuevo estado se pasa a través del `ulState` variable.</span><span class="sxs-lookup"><span data-stu-id="54ee3-132">The  `CButtonEventHandler::Click` function calls the  `SetCurrentState` function and the new state is passed in through the  `ulState` variable.</span></span> 
  
### <a name="setcurrentstate-example"></a><span data-ttu-id="54ee3-133">Ejemplo de SetCurrentState()</span><span class="sxs-lookup"><span data-stu-id="54ee3-133">SetCurrentState() example</span></span>

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

## <a name="notification-routine"></a><span data-ttu-id="54ee3-134">Rutina de notificación</span><span class="sxs-lookup"><span data-stu-id="54ee3-134">Notification routine</span></span>

<span data-ttu-id="54ee3-135">La función **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** se usa en Outlook para enviar notificaciones a un cliente cuando hay cambios en el estado de conexión.</span><span class="sxs-lookup"><span data-stu-id="54ee3-135">The **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** function is used by Outlook to send notifications to a client when there are changes in the connection state.</span></span> 
  
### <a name="cmyofflinenotifynotify-example"></a><span data-ttu-id="54ee3-136">Ejemplo de CMyOfflineNotify::Notify()</span><span class="sxs-lookup"><span data-stu-id="54ee3-136">CMyOfflineNotify::Notify() example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="54ee3-137">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="54ee3-137">See also</span></span>

- [<span data-ttu-id="54ee3-138">Información sobre la API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="54ee3-138">About the Offline State API</span></span>](about-the-offline-state-api.md)
- [<span data-ttu-id="54ee3-139">Instalar el complemento de estado sin conexión de muestra</span><span class="sxs-lookup"><span data-stu-id="54ee3-139">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="54ee3-140">Información sobre el complemento de estado sin conexión de muestra</span><span class="sxs-lookup"><span data-stu-id="54ee3-140">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
- [<span data-ttu-id="54ee3-141">Configurar un complemento de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="54ee3-141">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
- [<span data-ttu-id="54ee3-142">Desconectar un complemento de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="54ee3-142">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

