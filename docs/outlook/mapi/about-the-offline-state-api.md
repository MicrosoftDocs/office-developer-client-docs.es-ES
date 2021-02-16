---
title: Información sobre la API de estado sin conexión
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: 56793ae0d2c2ce76c89c7cda4985618e3a40ccfd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410486"
---
# <a name="about-the-offline-state-api"></a><span data-ttu-id="56974-103">Información sobre la API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="56974-103">About the Offline State API</span></span>

  
  
<span data-ttu-id="56974-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56974-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56974-105">La API de estado sin conexión admite devoluciones de llamada que indican cambios en el estado de conexión de un usuario en Microsoft Outlook 2013 y Microsoft Outlook 2010, por ejemplo, desde estar en línea en Outlook 2013 o Outlook 2010 hasta estar sin conexión.</span><span class="sxs-lookup"><span data-stu-id="56974-105">The Offline State API supports callbacks indicating changes in a user's connection state in Microsoft Outlook 2013 and Microsoft Outlook 2010—for example, from being online in Outlook 2013 or Outlook 2010 to being offline.</span></span> <span data-ttu-id="56974-106">La API usa un objeto sin conexión global en Outlook 2013 o Outlook 2010 para realizar un seguimiento de estos cambios para un perfil de cuenta de usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="56974-106">The API uses a global offline object in Outlook 2013 or Outlook 2010 to track such changes for a given user account profile.</span></span> <span data-ttu-id="56974-107">La notificación es la única forma compatible de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="56974-107">Notification is the only supported form of callback.</span></span> <span data-ttu-id="56974-108">Como clientes de esta API, los proveedores de correo que desean recibir una notificación de estos cambios de estado de conexión hacen lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="56974-108">As clients of this API, mail providers who want to be notified of such connection state changes do the following:</span></span>
  
1. <span data-ttu-id="56974-109">Implementar **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="56974-109">Implement **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
2. <span data-ttu-id="56974-110">Abra un objeto sin conexión existente para un perfil específico mediante **[HrOpenOfflineObj](hropenofflineobj.md)**.</span><span class="sxs-lookup"><span data-stu-id="56974-110">Open an existing offline object for a specific profile using **[HrOpenOfflineObj](hropenofflineobj.md)**.</span></span> 
    
3. <span data-ttu-id="56974-111">Determinar si el objeto tiene la capacidad de proporcionar notificaciones en línea o sin conexión mediante **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span><span class="sxs-lookup"><span data-stu-id="56974-111">Determine if the object has the capability of providing online or offline notifications using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> 
    
4. <span data-ttu-id="56974-112">Registre el objeto para notificaciones en línea o sin conexión **[con IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="56974-112">Register the object for online or offline notifications using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="56974-113">Los proveedores de correo ahora pueden recibir notificaciones que Outlook 2013 o Outlook 2010 envían **mediante IMAPIOfflineNotify**.</span><span class="sxs-lookup"><span data-stu-id="56974-113">Mail providers can now receive notifications that Outlook 2013 or Outlook 2010 send using **IMAPIOfflineNotify**.</span></span> 
    
5. <span data-ttu-id="56974-114">Al cerrar, quite el registro de las notificaciones en línea y sin conexión con **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span><span class="sxs-lookup"><span data-stu-id="56974-114">On shutdown, remove registration for online and offline notifications using **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="56974-115">En general, Outlook 2013 y Outlook 2010 pueden notificar a un cliente los cambios en línea o sin conexión, así como otros cambios, pero la API de estado sin conexión solo admite notificaciones para cambios en línea o sin conexión.</span><span class="sxs-lookup"><span data-stu-id="56974-115">In general, Outlook 2013 and Outlook 2010 can notify a client of online/offline changes as well as other changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="56974-116">El cliente debe omitir todas las demás notificaciones.</span><span class="sxs-lookup"><span data-stu-id="56974-116">The client should ignore all other notifications.</span></span> <span data-ttu-id="56974-117">Para obtener más información, **[vea IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** y **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span><span class="sxs-lookup"><span data-stu-id="56974-117">For more information, see **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span></span> 
  
 <span data-ttu-id="56974-118">Para obtener un ejemplo de un cliente que usa la API de estado sin conexión, vea Acerca del [complemento de estado sin conexión de ejemplo.](about-the-sample-offline-state-add-in.md)</span><span class="sxs-lookup"><span data-stu-id="56974-118">For an example of a client that uses the Offline State API, see [About the Sample Offline State Add-in](about-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="56974-119">El complemento de estado sin conexión de ejemplo es un complemento COM que usa la API de estado sin conexión para supervisar y cambiar el estado de conexión.</span><span class="sxs-lookup"><span data-stu-id="56974-119">The Sample Offline State Add-in is a COM add-in that uses the Offline State API to monitor and change the connection state.</span></span>
  
<span data-ttu-id="56974-120">Esta API proporciona lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="56974-120">This API provides the following:</span></span>
  
<span data-ttu-id="56974-121">Definiciones:</span><span class="sxs-lookup"><span data-stu-id="56974-121">Definitions:</span></span>
  
- [<span data-ttu-id="56974-122">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="56974-122">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="56974-123">Tipos de datos:</span><span class="sxs-lookup"><span data-stu-id="56974-123">Data types:</span></span>
  
- <span data-ttu-id="56974-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span><span class="sxs-lookup"><span data-stu-id="56974-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span></span>
    
- <span data-ttu-id="56974-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span><span class="sxs-lookup"><span data-stu-id="56974-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span></span>
    
- <span data-ttu-id="56974-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span><span class="sxs-lookup"><span data-stu-id="56974-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span></span>
    
<span data-ttu-id="56974-127">Funciones:</span><span class="sxs-lookup"><span data-stu-id="56974-127">Functions:</span></span>
  
- <span data-ttu-id="56974-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span><span class="sxs-lookup"><span data-stu-id="56974-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span></span>
    
<span data-ttu-id="56974-129">Interfaces:</span><span class="sxs-lookup"><span data-stu-id="56974-129">Interfaces:</span></span>
  
- <span data-ttu-id="56974-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="56974-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span></span>
    
- <span data-ttu-id="56974-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span><span class="sxs-lookup"><span data-stu-id="56974-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span></span>
    
- <span data-ttu-id="56974-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="56974-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span></span>
    

