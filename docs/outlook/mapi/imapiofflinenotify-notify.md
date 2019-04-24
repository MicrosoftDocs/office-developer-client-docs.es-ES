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
ms.openlocfilehash: 4440df4b8e4a46e13748cf47d599e16599aaf858
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270087"
---
# <a name="imapiofflinenotifynotify"></a><span data-ttu-id="6d099-103">IMAPIOfflineNotify::Notify</span><span class="sxs-lookup"><span data-stu-id="6d099-103">IMAPIOfflineNotify::Notify</span></span>

  
  
<span data-ttu-id="6d099-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d099-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d099-105">Envía notificaciones al cliente sobre los cambios en el estado de conexión.</span><span class="sxs-lookup"><span data-stu-id="6d099-105">Sends notifications to the client about changes in connection state.</span></span>
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a><span data-ttu-id="6d099-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6d099-106">Parameters</span></span>

 <span data-ttu-id="6d099-107">_pNotifyInfo_</span><span class="sxs-lookup"><span data-stu-id="6d099-107">_pNotifyInfo_</span></span>
  
> <span data-ttu-id="6d099-108">a La notificación que Outlook envía al cliente.</span><span class="sxs-lookup"><span data-stu-id="6d099-108">[in] The notification that Outlook sends to the client.</span></span> <span data-ttu-id="6d099-109">La notificación indica la parte del estado de conexión que ha cambiado, el estado de conexión anterior y el nuevo estado de conexión.</span><span class="sxs-lookup"><span data-stu-id="6d099-109">The notification indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6d099-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6d099-110">Remarks</span></span>

<span data-ttu-id="6d099-111">Outlook usa este método para enviar devoluciones de llamada de notificación a un cliente.</span><span class="sxs-lookup"><span data-stu-id="6d099-111">Outlook uses this method to send notification callbacks to a client.</span></span> <span data-ttu-id="6d099-112">Para hacer que esta interfaz esté disponible para Microsoft Outlook 2010 o Microsoft Outlook 2013, el cliente debe implementar esta interfaz y pasar un puntero a ella como miembro en **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** al configurar las devoluciones de llamada mediante **[IMAPIOfflineMgr:: Advise ](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="6d099-112">To make this interface available to Microsoft Outlook 2010 or Microsoft Outlook 2013, the client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
  
<span data-ttu-id="6d099-113">El cliente también pasa a **MAPIOFFLINE_ADVISEINFO** un token de cliente que Outlook 2010 o Outlook 2013 usa en **IMAPIOfflineNotify:: Notify** para identificar al cliente registrado para la devolución de llamada de notificación.</span><span class="sxs-lookup"><span data-stu-id="6d099-113">The client also passes to **MAPIOFFLINE_ADVISEINFO** a client token that Outlook 2010 or Outlook 2013 uses in **IMAPIOfflineNotify::Notify** to identify the client registered for the notification callback.</span></span> 
  
<span data-ttu-id="6d099-114">En general, Outlook 2010 y Outlook 2013 pueden notificar a un cliente los cambios en línea/sin conexión y otros cambios en el estado de conexión, pero la API de estado sin conexión solo admite notificaciones para los cambios en línea o sin conexión.</span><span class="sxs-lookup"><span data-stu-id="6d099-114">In general, Outlook 2010 and Outlook 2013 can notify a client of online/offline changes and other connection state changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="6d099-115">El cliente debe omitir el resto de las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="6d099-115">The client must ignore all other notifications.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6d099-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d099-116">See also</span></span>



[<span data-ttu-id="6d099-117">Información sobre la API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="6d099-117">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="6d099-118">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="6d099-118">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

