---
title: IMAPIOfflineNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineNotify.Notify
api_type:
- COM
ms.assetid: 10c7cb9d-2e9d-72eb-6b07-31eed892e646
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: a84114a3363f9cbcd9455bce12d3171843bd18a4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571118"
---
# <a name="imapiofflinenotifynotify"></a><span data-ttu-id="4b52e-103">IMAPIOfflineNotify::Notify</span><span class="sxs-lookup"><span data-stu-id="4b52e-103">IMAPIOfflineNotify::Notify</span></span>

  
  
<span data-ttu-id="4b52e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b52e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b52e-105">Envía notificaciones al cliente acerca de los cambios en el estado de conexión.</span><span class="sxs-lookup"><span data-stu-id="4b52e-105">Sends notifications to the client about changes in connection state.</span></span>
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a><span data-ttu-id="4b52e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b52e-106">Parameters</span></span>

 <span data-ttu-id="4b52e-107">_pNotifyInfo_</span><span class="sxs-lookup"><span data-stu-id="4b52e-107">_pNotifyInfo_</span></span>
  
> <span data-ttu-id="4b52e-108">[entrada] La notificación de que Outlook envíe al cliente.</span><span class="sxs-lookup"><span data-stu-id="4b52e-108">[in] The notification that Outlook sends to the client.</span></span> <span data-ttu-id="4b52e-109">La notificación indica la parte del estado de conexión que ha cambiado, el estado de conexión anterior y el nuevo estado de conexión.</span><span class="sxs-lookup"><span data-stu-id="4b52e-109">The notification indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4b52e-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4b52e-110">Remarks</span></span>

<span data-ttu-id="4b52e-111">Outlook utiliza este método para enviar las devoluciones de llamada de notificación a un cliente.</span><span class="sxs-lookup"><span data-stu-id="4b52e-111">Outlook uses this method to send notification callbacks to a client.</span></span> <span data-ttu-id="4b52e-112">Para realizar esta interfaz disponible en Microsoft Outlook 2010 o Microsoft Outlook 2013, el cliente debe implementar esta interfaz y pasar un puntero a él como un miembro en **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** al configurar las devoluciones de llamada con **[IMAPIOfflineMgr::Advise ](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="4b52e-112">To make this interface available to Microsoft Outlook 2010 or Microsoft Outlook 2013, the client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
  
<span data-ttu-id="4b52e-113">El cliente también pasa al **MAPIOFFLINE_ADVISEINFO** un símbolo (token) de cliente que Outlook 2010 o 2013 de Outlook se usa en **IMAPIOfflineNotify::Notify** para identificar el cliente registrado para la devolución de llamada de notificación.</span><span class="sxs-lookup"><span data-stu-id="4b52e-113">The client also passes to **MAPIOFFLINE_ADVISEINFO** a client token that Outlook 2010 or Outlook 2013 uses in **IMAPIOfflineNotify::Notify** to identify the client registered for the notification callback.</span></span> 
  
<span data-ttu-id="4b52e-114">En general, Outlook 2010 y Outlook 2013 pueden notificar a un cliente de cambios en línea o sin conexión y otros cambios de estado de conexión, pero la API de estado sin conexión admite solamente las notificaciones de cambios en línea o sin conexión.</span><span class="sxs-lookup"><span data-stu-id="4b52e-114">In general, Outlook 2010 and Outlook 2013 can notify a client of online/offline changes and other connection state changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="4b52e-115">El cliente debe omitir todas las notificaciones de otras.</span><span class="sxs-lookup"><span data-stu-id="4b52e-115">The client must ignore all other notifications.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4b52e-116">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="4b52e-116">See also</span></span>



[<span data-ttu-id="4b52e-117">Información sobre la API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="4b52e-117">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="4b52e-118">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="4b52e-118">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

