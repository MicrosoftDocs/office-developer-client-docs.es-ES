---
title: MAPIOFFLINE_ADVISEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20a46c69-d6ae-7d17-f8af-12952867d342
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 82869fa479ebe8a4d7b1881cec5d5c243b7d7957
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565098"
---
# <a name="mapiofflineadviseinfo"></a><span data-ttu-id="0584e-103">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="0584e-103">MAPIOFFLINE_ADVISEINFO</span></span>
 
<span data-ttu-id="0584e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0584e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0584e-105">Proporciona información a **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** para registrar la devolución de llamada para un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="0584e-105">Provides information to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** to register callback for an offline object.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="0584e-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="0584e-106">Quick info</span></span>

<span data-ttu-id="0584e-107">Vea **IMAPIOfflineMgr::Advise**.</span><span class="sxs-lookup"><span data-stu-id="0584e-107">See **IMAPIOfflineMgr::Advise**.</span></span> 
  
```cpp
typedef struct 
{ 
      ULONG                   ulSize; 
      ULONG                   ulClientToken; 
      MAPIOFFLINE_CALLBACK_TYPE     CallbackType; 
      IUnknown*               pCallback; 
      ULONG                   ulAdviseTypes; 
      ULONG                   ulStateMask; 
} MAPIOFFLINE_ADVISEINFO;
```

## <a name="members"></a><span data-ttu-id="0584e-108">Members</span><span class="sxs-lookup"><span data-stu-id="0584e-108">Members</span></span>

<span data-ttu-id="0584e-109">_ulSize_: el tamaño de **MAPIOFFLINE_ADVISEINFO**.</span><span class="sxs-lookup"><span data-stu-id="0584e-109">_ulSize_: The size of **MAPIOFFLINE_ADVISEINFO**.</span></span> 
    
<span data-ttu-id="0584e-110">_ulClientToken_: un símbolo (token) definido por el cliente sobre una devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="0584e-110">_ulClientToken_: A token defined by the client about a callback.</span></span> <span data-ttu-id="0584e-111">Es el miembro *ulClientToken* de la estructura **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** pasado a **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)**.</span><span class="sxs-lookup"><span data-stu-id="0584e-111">It is the *ulClientToken* member of the **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** structure passed to **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)**.</span></span> 
    
<span data-ttu-id="0584e-112">_CallbackType_: tipo de devolución de llamada para realizar.</span><span class="sxs-lookup"><span data-stu-id="0584e-112">_CallbackType_: Type of callback to make.</span></span>
    
   -  <span data-ttu-id="0584e-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="0584e-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span></span> 
    
   - <span data-ttu-id="0584e-114">El tipo de devolución de llamada es por notificación.</span><span class="sxs-lookup"><span data-stu-id="0584e-114">The type of callback is by notification.</span></span> <span data-ttu-id="0584e-115">Esto es el único tipo admitido de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="0584e-115">This is the only supported type of callback.</span></span>  <span data-ttu-id="0584e-116">*pCallback* debe indicar la interfaz **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="0584e-116">*pCallback*  must indicate the interface **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="0584e-117">_pCallback_: interfaz que se usará para la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="0584e-117">_pCallback_: Interface to use for callback.</span></span> <span data-ttu-id="0584e-118">Esto es la implementación del cliente de **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="0584e-118">This is the client's implementation of **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="0584e-119">_ulAdviseTypes_: los tipos de advise, identificado por la condición para que advierte.</span><span class="sxs-lookup"><span data-stu-id="0584e-119">_ulAdviseTypes_: The types of advise, as identified by the condition for advising.</span></span> <span data-ttu-id="0584e-120">El único tipo admitido es MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.</span><span class="sxs-lookup"><span data-stu-id="0584e-120">The only supported type is MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.</span></span>
    
<span data-ttu-id="0584e-121">_ulStateMask_: el estado compatible sólo es MAPIOFFLINE_STATE_ALL.</span><span class="sxs-lookup"><span data-stu-id="0584e-121">_ulStateMask_: The only supported state is MAPIOFFLINE_STATE_ALL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0584e-122">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="0584e-122">See also</span></span>

- [<span data-ttu-id="0584e-123">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="0584e-123">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)
- [<span data-ttu-id="0584e-124">Información sobre la API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="0584e-124">About the Offline State API</span></span>](about-the-offline-state-api.md) 
- [<span data-ttu-id="0584e-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="0584e-125">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="0584e-126">MAPIOFFLINE_CALLBACK_TYPE</span><span class="sxs-lookup"><span data-stu-id="0584e-126">MAPIOFFLINE_CALLBACK_TYPE</span></span>](mapioffline_callback_type.md)

