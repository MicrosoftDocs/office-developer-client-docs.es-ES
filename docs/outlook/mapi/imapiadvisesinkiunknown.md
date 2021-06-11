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
# <a name="imapiadvisesink--iunknown"></a><span data-ttu-id="a59fe-103">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a59fe-103">IMAPIAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="a59fe-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a59fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a59fe-105">Implementa un objeto de receptor de aviso para controlar la notificación.</span><span class="sxs-lookup"><span data-stu-id="a59fe-105">Implements an advise sink object for handling notification.</span></span> <span data-ttu-id="a59fe-106">Un puntero a un objeto receptor de aviso se pasa en una llamada al método **Advise** de un proveedor de servicios, el mecanismo usado para registrarse para la notificación.</span><span class="sxs-lookup"><span data-stu-id="a59fe-106">A pointer to an advise sink object is passed in a call to a service provider's **Advise** method, the mechanism used to register for notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a59fe-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a59fe-107">Header file:</span></span>  <br/> |<span data-ttu-id="a59fe-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a59fe-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a59fe-109">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="a59fe-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="a59fe-110">Aconsejar objetos de receptor</span><span class="sxs-lookup"><span data-stu-id="a59fe-110">Advise sink objects</span></span>  <br/> |
|<span data-ttu-id="a59fe-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="a59fe-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="a59fe-112">Aplicaciones cliente y MAPI</span><span class="sxs-lookup"><span data-stu-id="a59fe-112">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="a59fe-113">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="a59fe-113">Called by:</span></span>  <br/> |<span data-ttu-id="a59fe-114">Proveedores de servicios y MAPI</span><span class="sxs-lookup"><span data-stu-id="a59fe-114">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="a59fe-115">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="a59fe-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a59fe-116">IID_IMAPIAdviseSink</span><span class="sxs-lookup"><span data-stu-id="a59fe-116">IID_IMAPIAdviseSink</span></span>  <br/> |
|<span data-ttu-id="a59fe-117">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="a59fe-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="a59fe-118">LPMAPIADVISESINK</span><span class="sxs-lookup"><span data-stu-id="a59fe-118">LPMAPIADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a59fe-119">Orden de Vtable</span><span class="sxs-lookup"><span data-stu-id="a59fe-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a59fe-120">OnNotify</span><span class="sxs-lookup"><span data-stu-id="a59fe-120">OnNotify</span></span>](imapiadvisesink-onnotify.md) <br/> |<span data-ttu-id="a59fe-121">Responde a una notificación realizando una o varias tareas.</span><span class="sxs-lookup"><span data-stu-id="a59fe-121">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="a59fe-122">Las tareas realizadas dependen del tipo de evento y del objeto que genera la notificación.</span><span class="sxs-lookup"><span data-stu-id="a59fe-122">The tasks performed depend on the type of event and the object that generates the notification.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a59fe-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="a59fe-123">See also</span></span>



[<span data-ttu-id="a59fe-124">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="a59fe-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

