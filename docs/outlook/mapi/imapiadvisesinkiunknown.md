---
title: IUnknown IMAPIAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink
api_type:
- COM
ms.assetid: f598fc57-75d3-473b-8eb0-9d8a3b92e9f2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d537184f427b2ef240dd2a9a59ab2f624f8f75d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409569"
---
# <a name="imapiadvisesink--iunknown"></a><span data-ttu-id="556ac-103">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="556ac-103">IMAPIAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="556ac-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="556ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="556ac-105">Implementa un objeto de receptor de notificaciones para controlar la notificación.</span><span class="sxs-lookup"><span data-stu-id="556ac-105">Implements an advise sink object for handling notification.</span></span> <span data-ttu-id="556ac-106">Un puntero a un objeto receptor de notificaciones se pasa en una llamada a un método **Advise** de un proveedor de servicios, el mecanismo que se usa para registrarse en la notificación.</span><span class="sxs-lookup"><span data-stu-id="556ac-106">A pointer to an advise sink object is passed in a call to a service provider's **Advise** method, the mechanism used to register for notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="556ac-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="556ac-107">Header file:</span></span>  <br/> |<span data-ttu-id="556ac-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="556ac-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="556ac-109">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="556ac-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="556ac-110">Notificar a los objetos de receptor</span><span class="sxs-lookup"><span data-stu-id="556ac-110">Advise sink objects</span></span>  <br/> |
|<span data-ttu-id="556ac-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="556ac-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="556ac-112">Aplicaciones cliente y MAPI</span><span class="sxs-lookup"><span data-stu-id="556ac-112">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="556ac-113">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="556ac-113">Called by:</span></span>  <br/> |<span data-ttu-id="556ac-114">Proveedores de servicios y MAPI</span><span class="sxs-lookup"><span data-stu-id="556ac-114">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="556ac-115">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="556ac-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="556ac-116">IID_IMAPIAdviseSink</span><span class="sxs-lookup"><span data-stu-id="556ac-116">IID_IMAPIAdviseSink</span></span>  <br/> |
|<span data-ttu-id="556ac-117">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="556ac-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="556ac-118">LPMAPIADVISESINK</span><span class="sxs-lookup"><span data-stu-id="556ac-118">LPMAPIADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="556ac-119">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="556ac-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="556ac-120">Notify</span><span class="sxs-lookup"><span data-stu-id="556ac-120">OnNotify</span></span>](imapiadvisesink-onnotify.md) <br/> |<span data-ttu-id="556ac-121">Responde a una notificación realizando una o más tareas.</span><span class="sxs-lookup"><span data-stu-id="556ac-121">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="556ac-122">Las tareas realizadas dependen del tipo de evento y del objeto que genera la notificación.</span><span class="sxs-lookup"><span data-stu-id="556ac-122">The tasks performed depend on the type of event and the object that generates the notification.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="556ac-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="556ac-123">See also</span></span>



[<span data-ttu-id="556ac-124">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="556ac-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

