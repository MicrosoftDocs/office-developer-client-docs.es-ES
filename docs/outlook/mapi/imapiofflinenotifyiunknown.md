---
title: IMAPIOfflineNotify IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineNotify
api_type:
- COM
ms.assetid: a593d2a1-29f8-7e23-85bf-02fa3cfebe1b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: adcb8e78d4e85e19d4102795aa4d43f06a7f86ba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568150"
---
# <a name="imapiofflinenotify--iunknown"></a><span data-ttu-id="56b1f-103">IMAPIOfflineNotify : IUnknown</span><span class="sxs-lookup"><span data-stu-id="56b1f-103">IMAPIOfflineNotify : IUnknown</span></span>

  
  
<span data-ttu-id="56b1f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56b1f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56b1f-105">Es compatible con Microsoft Outlook 2010 y Microsoft Outlook 2013 en el envío de las devoluciones de llamada de notificación a un cliente.</span><span class="sxs-lookup"><span data-stu-id="56b1f-105">Supports Microsoft Outlook 2010 and Microsoft Outlook 2013 in sending notification callbacks to a client.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="56b1f-106">Suministrado por:</span><span class="sxs-lookup"><span data-stu-id="56b1f-106">Provided by:</span></span>  <br/> |<span data-ttu-id="56b1f-107">Cliente</span><span class="sxs-lookup"><span data-stu-id="56b1f-107">Client</span></span>  <br/> |
|<span data-ttu-id="56b1f-108">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="56b1f-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="56b1f-109">IID_IMAPIOfflineNotify</span><span class="sxs-lookup"><span data-stu-id="56b1f-109">IID_IMAPIOfflineNotify</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="56b1f-110">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="56b1f-110">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="56b1f-111">Notify</span><span class="sxs-lookup"><span data-stu-id="56b1f-111">Notify</span></span>](imapiofflinenotify-notify.md) <br/> |<span data-ttu-id="56b1f-112">Envía notificaciones a un cliente acerca de los cambios en el estado de conexión.</span><span class="sxs-lookup"><span data-stu-id="56b1f-112">Sends notifications to a client about changes in connection state.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56b1f-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="56b1f-113">Remarks</span></span>

<span data-ttu-id="56b1f-114">El cliente debe implementar esta interfaz y pasar un puntero a él como un miembro en **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** al configurar las devoluciones de llamada con **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="56b1f-114">The client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="56b1f-115">Posteriormente, Outlook 2010 o Outlook 2013 podrán utilizar esta interfaz para enviar las devoluciones de llamada de notificación al cliente.</span><span class="sxs-lookup"><span data-stu-id="56b1f-115">Subsequently, Outlook 2010 or Outlook 2013 will be able to use this interface to send notification callbacks to the client.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="56b1f-116">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="56b1f-116">See also</span></span>



[<span data-ttu-id="56b1f-117">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="56b1f-117">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="56b1f-118">Información sobre la API de estado sin conexión</span><span class="sxs-lookup"><span data-stu-id="56b1f-118">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="56b1f-119">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="56b1f-119">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="56b1f-120">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="56b1f-120">MAPIOFFLINE_ADVISEINFO</span></span>](mapioffline_adviseinfo.md)

