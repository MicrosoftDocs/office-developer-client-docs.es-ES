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
ms.openlocfilehash: d537184f427b2ef240dd2a9a59ab2f624f8f75d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409569"
---
# <a name="imapiadvisesink--iunknown"></a><span data-ttu-id="e7158-103">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e7158-103">IMAPIAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="e7158-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7158-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7158-105">Implementa un objeto receptor de avisos para controlar la notificación.</span><span class="sxs-lookup"><span data-stu-id="e7158-105">Implements an advise sink object for handling notification.</span></span> <span data-ttu-id="e7158-106">Un puntero a un objeto receptor de aviso se pasa en una llamada al método **Advise** de un proveedor de servicios, el mecanismo usado para registrar la notificación.</span><span class="sxs-lookup"><span data-stu-id="e7158-106">A pointer to an advise sink object is passed in a call to a service provider's **Advise** method, the mechanism used to register for notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e7158-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e7158-107">Header file:</span></span>  <br/> |<span data-ttu-id="e7158-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e7158-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e7158-109">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="e7158-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="e7158-110">Avisar a los objetos receptores</span><span class="sxs-lookup"><span data-stu-id="e7158-110">Advise sink objects</span></span>  <br/> |
|<span data-ttu-id="e7158-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="e7158-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="e7158-112">Aplicaciones cliente y MAPI</span><span class="sxs-lookup"><span data-stu-id="e7158-112">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="e7158-113">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="e7158-113">Called by:</span></span>  <br/> |<span data-ttu-id="e7158-114">Proveedores de servicios y MAPI</span><span class="sxs-lookup"><span data-stu-id="e7158-114">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="e7158-115">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="e7158-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e7158-116">IID_IMAPIAdviseSink</span><span class="sxs-lookup"><span data-stu-id="e7158-116">IID_IMAPIAdviseSink</span></span>  <br/> |
|<span data-ttu-id="e7158-117">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="e7158-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="e7158-118">LPMAPIADVISESINK</span><span class="sxs-lookup"><span data-stu-id="e7158-118">LPMAPIADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e7158-119">Orden de tabla virtual</span><span class="sxs-lookup"><span data-stu-id="e7158-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e7158-120">OnNotify</span><span class="sxs-lookup"><span data-stu-id="e7158-120">OnNotify</span></span>](imapiadvisesink-onnotify.md) <br/> |<span data-ttu-id="e7158-121">Responde a una notificación realizando una o varias tareas.</span><span class="sxs-lookup"><span data-stu-id="e7158-121">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="e7158-122">Las tareas realizadas dependen del tipo de evento y del objeto que genera la notificación.</span><span class="sxs-lookup"><span data-stu-id="e7158-122">The tasks performed depend on the type of event and the object that generates the notification.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e7158-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e7158-123">See also</span></span>



[<span data-ttu-id="e7158-124">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="e7158-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

