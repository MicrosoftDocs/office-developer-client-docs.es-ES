---
title: IMAPIAdviseSink IUnknown
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
ms.openlocfilehash: c6e352288f0bf5b0a3f284441bffc522bf00b9f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19817186"
---
# <a name="imapiadvisesink--iunknown"></a><span data-ttu-id="26114-103">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="26114-103">IMAPIAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="26114-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="26114-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="26114-105">Implementa un objeto de receptor advise para controlar la notificación.</span><span class="sxs-lookup"><span data-stu-id="26114-105">Implements an advise sink object for handling notification.</span></span> <span data-ttu-id="26114-106">Un puntero a un objeto de receptor advise se pasa en la llamada al método **Advise** de un proveedor de servicios, el mecanismo utilizado para registrar la notificación.</span><span class="sxs-lookup"><span data-stu-id="26114-106">A pointer to an advise sink object is passed in a call to a service provider's **Advise** method, the mechanism used to register for notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="26114-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="26114-107">Header file:</span></span>  <br/> |<span data-ttu-id="26114-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="26114-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="26114-109">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="26114-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="26114-110">Objetos del receptor de aviso</span><span class="sxs-lookup"><span data-stu-id="26114-110">Advise sink objects</span></span>  <br/> |
|<span data-ttu-id="26114-111">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="26114-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="26114-112">Las aplicaciones cliente y MAPI</span><span class="sxs-lookup"><span data-stu-id="26114-112">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="26114-113">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="26114-113">Called by:</span></span>  <br/> |<span data-ttu-id="26114-114">Proveedores de servicios y MAPI</span><span class="sxs-lookup"><span data-stu-id="26114-114">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="26114-115">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="26114-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="26114-116">IID_IMAPIAdviseSink</span><span class="sxs-lookup"><span data-stu-id="26114-116">IID_IMAPIAdviseSink</span></span>  <br/> |
|<span data-ttu-id="26114-117">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="26114-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="26114-118">LPMAPIADVISESINK</span><span class="sxs-lookup"><span data-stu-id="26114-118">LPMAPIADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="26114-119">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="26114-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="26114-120">OnNotify</span><span class="sxs-lookup"><span data-stu-id="26114-120">OnNotify</span></span>](imapiadvisesink-onnotify.md) <br/> |<span data-ttu-id="26114-121">Responde a una notificación mediante la realización de una o varias tareas.</span><span class="sxs-lookup"><span data-stu-id="26114-121">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="26114-122">Las tareas que realiza dependen del tipo de evento y el objeto que genera la notificación.</span><span class="sxs-lookup"><span data-stu-id="26114-122">The tasks performed depend on the type of event and the object that generates the notification.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="26114-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="26114-123">See also</span></span>



[<span data-ttu-id="26114-124">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="26114-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

