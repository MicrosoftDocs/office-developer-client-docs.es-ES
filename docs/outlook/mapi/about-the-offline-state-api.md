---
title: Información sobre la API de estado sin conexión
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: 'Última modificación: 25 de junio de 2012'
ms.openlocfilehash: aa30a173251193d74d6560c8dce2663463a18e36
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565987"
---
# <a name="about-the-offline-state-api"></a><span data-ttu-id="c38cf-103">Información sobre la API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="c38cf-103">About the Offline State API</span></span>

  
  
<span data-ttu-id="c38cf-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c38cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c38cf-105">La API de estado sin conexión admite las devoluciones de llamada que indica los cambios en el estado de conexión de un usuario en Microsoft Outlook 2013 y Microsoft Outlook 2010: por ejemplo, desde la que se está en línea en Outlook 2013 o Outlook 2010 para que se está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="c38cf-105">The Offline State API supports callbacks indicating changes in a user's connection state in Microsoft Outlook 2013 and Microsoft Outlook 2010—for example, from being online in Outlook 2013 or Outlook 2010 to being offline.</span></span> <span data-ttu-id="c38cf-106">La API usa un objeto global sin conexión en Outlook 2013 o Outlook 2010 para realizar un seguimiento de dichos cambios para un perfil de cuenta de usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="c38cf-106">The API uses a global offline object in Outlook 2013 or Outlook 2010 to track such changes for a given user account profile.</span></span> <span data-ttu-id="c38cf-107">Notificación es la única forma compatible de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="c38cf-107">Notification is the only supported form of callback.</span></span> <span data-ttu-id="c38cf-108">Como los clientes de esta API, los proveedores de correo que desean recibir una notificación de estos cambios de estado de conexión, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c38cf-108">As clients of this API, mail providers who want to be notified of such connection state changes do the following:</span></span>
  
1. <span data-ttu-id="c38cf-109">Implemente **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="c38cf-109">Implement **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
2. <span data-ttu-id="c38cf-110">Abrir un objeto sin conexión existente para un perfil específico mediante **[HrOpenOfflineObj](hropenofflineobj.md)**.</span><span class="sxs-lookup"><span data-stu-id="c38cf-110">Open an existing offline object for a specific profile using **[HrOpenOfflineObj](hropenofflineobj.md)**.</span></span> 
    
3. <span data-ttu-id="c38cf-111">Determinar si el objeto tiene la capacidad de proporcionar notificaciones en línea o sin conexión con **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span><span class="sxs-lookup"><span data-stu-id="c38cf-111">Determine if the object has the capability of providing online or offline notifications using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> 
    
4. <span data-ttu-id="c38cf-112">Registre el objeto para las notificaciones en línea o sin conexión con **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="c38cf-112">Register the object for online or offline notifications using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="c38cf-113">Proveedores de correo ahora pueden recibir notificaciones de que Outlook 2013 o Outlook 2010 enviar utilizando **IMAPIOfflineNotify**.</span><span class="sxs-lookup"><span data-stu-id="c38cf-113">Mail providers can now receive notifications that Outlook 2013 or Outlook 2010 send using **IMAPIOfflineNotify**.</span></span> 
    
5. <span data-ttu-id="c38cf-114">En el cierre, quite el registro para las notificaciones de en línea y sin conexión mediante **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span><span class="sxs-lookup"><span data-stu-id="c38cf-114">On shutdown, remove registration for online and offline notifications using **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="c38cf-115">En general, Outlook 2013 y Outlook 2010 pueden notificar a un cliente de los cambios en línea o sin conexión, así como otros cambios, pero la API de estado sin conexión admite solamente las notificaciones de cambios en línea o sin conexión.</span><span class="sxs-lookup"><span data-stu-id="c38cf-115">In general, Outlook 2013 and Outlook 2010 can notify a client of online/offline changes as well as other changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="c38cf-116">El cliente debe omitir todas las notificaciones de otras.</span><span class="sxs-lookup"><span data-stu-id="c38cf-116">The client should ignore all other notifications.</span></span> <span data-ttu-id="c38cf-117">Para obtener más información, vea **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** y **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span><span class="sxs-lookup"><span data-stu-id="c38cf-117">For more information, see **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span></span> 
  
 <span data-ttu-id="c38cf-118">Para obtener un ejemplo de un cliente que usa la API de estado sin conexión, vea [Agregar en sobre el ejemplo de estado no conectado](about-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="c38cf-118">For an example of a client that uses the Offline State API, see [About the Sample Offline State Add-in](about-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="c38cf-119">El complemento de estado sin conexión de ejemplo es un complemento COM que usa la API de estado sin conexión para supervisar y cambiar el estado de conexión.</span><span class="sxs-lookup"><span data-stu-id="c38cf-119">The Sample Offline State Add-in is a COM add-in that uses the Offline State API to monitor and change the connection state.</span></span>
  
<span data-ttu-id="c38cf-120">Esta API ofrece lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c38cf-120">This API provides the following:</span></span>
  
<span data-ttu-id="c38cf-121">Definiciones:</span><span class="sxs-lookup"><span data-stu-id="c38cf-121">Definitions:</span></span>
  
- [<span data-ttu-id="c38cf-122">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="c38cf-122">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="c38cf-123">Tipos de datos:</span><span class="sxs-lookup"><span data-stu-id="c38cf-123">Data types:</span></span>
  
- <span data-ttu-id="c38cf-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span><span class="sxs-lookup"><span data-stu-id="c38cf-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span></span>
    
- <span data-ttu-id="c38cf-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span><span class="sxs-lookup"><span data-stu-id="c38cf-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span></span>
    
- <span data-ttu-id="c38cf-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span><span class="sxs-lookup"><span data-stu-id="c38cf-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span></span>
    
<span data-ttu-id="c38cf-127">Funciones:</span><span class="sxs-lookup"><span data-stu-id="c38cf-127">Functions:</span></span>
  
- <span data-ttu-id="c38cf-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span><span class="sxs-lookup"><span data-stu-id="c38cf-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span></span>
    
<span data-ttu-id="c38cf-129">Interfaces:</span><span class="sxs-lookup"><span data-stu-id="c38cf-129">Interfaces:</span></span>
  
- <span data-ttu-id="c38cf-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="c38cf-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span></span>
    
- <span data-ttu-id="c38cf-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span><span class="sxs-lookup"><span data-stu-id="c38cf-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span></span>
    
- <span data-ttu-id="c38cf-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="c38cf-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span></span>
    

