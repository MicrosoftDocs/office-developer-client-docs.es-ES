---
title: Acerca de la API de estado sin conexión
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: df225a0852b09e048656e817c54ea28b0de59888
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816377"
---
# <a name="about-the-offline-state-api"></a><span data-ttu-id="a2383-103">Acerca de la API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="a2383-103">About the Offline State API</span></span>

  
  
<span data-ttu-id="a2383-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a2383-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a2383-105">La API de estado sin conexión admite las devoluciones de llamada que indica los cambios en el estado de conexión de un usuario en Microsoft Outlook 2013 y Microsoft Outlook 2010: por ejemplo, desde la que se está en línea en Outlook 2013 o Outlook 2010 para que se está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="a2383-105">The Offline State API supports callbacks indicating changes in a user's connection state in Microsoft Outlook 2013 and Microsoft Outlook 2010—for example, from being online in Outlook 2013 or Outlook 2010 to being offline.</span></span> <span data-ttu-id="a2383-106">La API usa un objeto global sin conexión en Outlook 2013 o Outlook 2010 para realizar un seguimiento de dichos cambios para un perfil de cuenta de usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="a2383-106">The API uses a global offline object in Outlook 2013 or Outlook 2010 to track such changes for a given user account profile.</span></span> <span data-ttu-id="a2383-107">Notificación es la única forma compatible de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="a2383-107">Notification is the only supported form of callback.</span></span> <span data-ttu-id="a2383-108">Como los clientes de esta API, los proveedores de correo que desean recibir una notificación de estos cambios de estado de conexión, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a2383-108">As clients of this API, mail providers who want to be notified of such connection state changes do the following:</span></span>
  
1. <span data-ttu-id="a2383-109">Implemente **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="a2383-109">Implement **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
2. <span data-ttu-id="a2383-110">Abrir un objeto sin conexión existente para un perfil específico mediante **[HrOpenOfflineObj](hropenofflineobj.md)**.</span><span class="sxs-lookup"><span data-stu-id="a2383-110">Open an existing offline object for a specific profile using **[HrOpenOfflineObj](hropenofflineobj.md)**.</span></span> 
    
3. <span data-ttu-id="a2383-111">Determinar si el objeto tiene la capacidad de proporcionar notificaciones en línea o sin conexión con **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span><span class="sxs-lookup"><span data-stu-id="a2383-111">Determine if the object has the capability of providing online or offline notifications using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> 
    
4. <span data-ttu-id="a2383-112">Registre el objeto para las notificaciones en línea o sin conexión con **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="a2383-112">Register the object for online or offline notifications using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="a2383-113">Proveedores de correo ahora pueden recibir notificaciones de que Outlook 2013 o Outlook 2010 enviar utilizando **IMAPIOfflineNotify**.</span><span class="sxs-lookup"><span data-stu-id="a2383-113">Mail providers can now receive notifications that Outlook 2013 or Outlook 2010 send using **IMAPIOfflineNotify**.</span></span> 
    
5. <span data-ttu-id="a2383-114">En el cierre, quite el registro para las notificaciones de en línea y sin conexión mediante **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span><span class="sxs-lookup"><span data-stu-id="a2383-114">On shutdown, remove registration for online and offline notifications using **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="a2383-115">En general, Outlook 2013 y Outlook 2010 pueden notificar a un cliente de los cambios en línea o sin conexión, así como otros cambios, pero la API de estado sin conexión admite solamente las notificaciones de cambios en línea o sin conexión.</span><span class="sxs-lookup"><span data-stu-id="a2383-115">In general, Outlook 2013 and Outlook 2010 can notify a client of online/offline changes as well as other changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="a2383-116">El cliente debe omitir todas las notificaciones de otras.</span><span class="sxs-lookup"><span data-stu-id="a2383-116">The client should ignore all other notifications.</span></span> <span data-ttu-id="a2383-117">Para obtener más información, vea **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** y **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span><span class="sxs-lookup"><span data-stu-id="a2383-117">For more information, see **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span></span> 
  
 <span data-ttu-id="a2383-118">Para obtener un ejemplo de un cliente que usa la API de estado sin conexión, vea [Agregar en sobre el ejemplo de estado no conectado](about-the-sample-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="a2383-118">For an example of a client that uses the Offline State API, see [About the Sample Offline State Add-in](about-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="a2383-119">El complemento de estado sin conexión de ejemplo es un complemento COM que usa la API de estado sin conexión para supervisar y cambiar el estado de conexión.</span><span class="sxs-lookup"><span data-stu-id="a2383-119">The Sample Offline State Add-in is a COM add-in that uses the Offline State API to monitor and change the connection state.</span></span>
  
<span data-ttu-id="a2383-120">Esta API ofrece lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a2383-120">This API provides the following:</span></span>
  
<span data-ttu-id="a2383-121">Definiciones:</span><span class="sxs-lookup"><span data-stu-id="a2383-121">Definitions:</span></span>
  
- [<span data-ttu-id="a2383-122">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="a2383-122">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="a2383-123">Tipos de datos:</span><span class="sxs-lookup"><span data-stu-id="a2383-123">Data types:</span></span>
  
- <span data-ttu-id="a2383-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span><span class="sxs-lookup"><span data-stu-id="a2383-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span></span>
    
- <span data-ttu-id="a2383-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span><span class="sxs-lookup"><span data-stu-id="a2383-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span></span>
    
- <span data-ttu-id="a2383-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span><span class="sxs-lookup"><span data-stu-id="a2383-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span></span>
    
<span data-ttu-id="a2383-127">Funciones:</span><span class="sxs-lookup"><span data-stu-id="a2383-127">Functions:</span></span>
  
- <span data-ttu-id="a2383-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span><span class="sxs-lookup"><span data-stu-id="a2383-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span></span>
    
<span data-ttu-id="a2383-129">Interfaces:</span><span class="sxs-lookup"><span data-stu-id="a2383-129">Interfaces:</span></span>
  
- <span data-ttu-id="a2383-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="a2383-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span></span>
    
- <span data-ttu-id="a2383-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span><span class="sxs-lookup"><span data-stu-id="a2383-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span></span>
    
- <span data-ttu-id="a2383-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="a2383-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span></span>
    

