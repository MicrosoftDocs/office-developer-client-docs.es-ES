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
ms.openlocfilehash: 443644b66ba9c961992e22dbfc260fe8c48fe1b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818257"
---
# <a name="mapiofflineadviseinfo"></a><span data-ttu-id="0071a-103">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="0071a-103">MAPIOFFLINE_ADVISEINFO</span></span>
 
<span data-ttu-id="0071a-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0071a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0071a-105">Proporciona información a **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** para registrar la devolución de llamada para un objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="0071a-105">Provides information to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** to register callback for an offline object.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="0071a-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="0071a-106">Quick info</span></span>

<span data-ttu-id="0071a-107">Vea **IMAPIOfflineMgr::Advise**.</span><span class="sxs-lookup"><span data-stu-id="0071a-107">See **IMAPIOfflineMgr::Advise**.</span></span> 
  
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

## <a name="members"></a><span data-ttu-id="0071a-108">Members</span><span class="sxs-lookup"><span data-stu-id="0071a-108">Members</span></span>

<span data-ttu-id="0071a-109">_ulSize_: el tamaño de **MAPIOFFLINE_ADVISEINFO**.</span><span class="sxs-lookup"><span data-stu-id="0071a-109">_ulSize_: The size of **MAPIOFFLINE_ADVISEINFO**.</span></span> 
    
<span data-ttu-id="0071a-110">_ulClientToken_: un símbolo (token) definido por el cliente sobre una devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="0071a-110">_ulClientToken_: A token defined by the client about a callback.</span></span> <span data-ttu-id="0071a-111">Es el miembro *ulClientToken* de la estructura **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** pasado a **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)**.</span><span class="sxs-lookup"><span data-stu-id="0071a-111">It is the *ulClientToken* member of the **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** structure passed to **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)**.</span></span> 
    
<span data-ttu-id="0071a-112">_CallbackType_: tipo de devolución de llamada para realizar.</span><span class="sxs-lookup"><span data-stu-id="0071a-112">_CallbackType_: Type of callback to make.</span></span>
    
   -  <span data-ttu-id="0071a-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="0071a-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span></span> 
    
   - <span data-ttu-id="0071a-114">El tipo de devolución de llamada es por notificación.</span><span class="sxs-lookup"><span data-stu-id="0071a-114">The type of callback is by notification.</span></span> <span data-ttu-id="0071a-115">Esto es el único tipo admitido de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="0071a-115">This is the only supported type of callback.</span></span>  <span data-ttu-id="0071a-116">*pCallback* debe indicar la interfaz **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="0071a-116">*pCallback*  must indicate the interface **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="0071a-117">_pCallback_: interfaz que se usará para la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="0071a-117">_pCallback_: Interface to use for callback.</span></span> <span data-ttu-id="0071a-118">Esto es la implementación del cliente de **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="0071a-118">This is the client's implementation of **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="0071a-119">_ulAdviseTypes_: los tipos de advise, identificado por la condición para que advierte.</span><span class="sxs-lookup"><span data-stu-id="0071a-119">_ulAdviseTypes_: The types of advise, as identified by the condition for advising.</span></span> <span data-ttu-id="0071a-120">El único tipo admitido es MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.</span><span class="sxs-lookup"><span data-stu-id="0071a-120">The only supported type is MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.</span></span>
    
<span data-ttu-id="0071a-121">_ulStateMask_: el estado compatible sólo es MAPIOFFLINE_STATE_ALL.</span><span class="sxs-lookup"><span data-stu-id="0071a-121">_ulStateMask_: The only supported state is MAPIOFFLINE_STATE_ALL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0071a-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="0071a-122">See also</span></span>

- [<span data-ttu-id="0071a-123">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="0071a-123">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)
- [<span data-ttu-id="0071a-124">Información sobre la API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="0071a-124">About the Offline State API</span></span>](about-the-offline-state-api.md) 
- [<span data-ttu-id="0071a-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="0071a-125">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="0071a-126">MAPIOFFLINE_CALLBACK_TYPE</span><span class="sxs-lookup"><span data-stu-id="0071a-126">MAPIOFFLINE_CALLBACK_TYPE</span></span>](mapioffline_callback_type.md)

