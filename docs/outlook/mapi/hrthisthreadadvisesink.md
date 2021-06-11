---
title: HrThisThreadAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrThisThreadAdviseSink
api_type:
- COM
ms.assetid: 12c07302-472f-4e4f-8087-1bdf0dc09a5a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0fb867d662064dfe5ff7759dba4b36a4635a2914
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427733"
---
# <a name="hrthisthreadadvisesink"></a><span data-ttu-id="5e7f7-103">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="5e7f7-103">HrThisThreadAdviseSink</span></span>

  
  
<span data-ttu-id="5e7f7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e7f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e7f7-105">Crea un receptor de avisos que encapsula un receptor de avisos existente para la seguridad de los subprocesos.</span><span class="sxs-lookup"><span data-stu-id="5e7f7-105">Creates an advise sink that wraps an existing advise sink for thread safety.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5e7f7-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="5e7f7-106">Header file:</span></span>  <br/> |<span data-ttu-id="5e7f7-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="5e7f7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5e7f7-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="5e7f7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5e7f7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5e7f7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5e7f7-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="5e7f7-110">Called by:</span></span>  <br/> |<span data-ttu-id="5e7f7-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="5e7f7-111">Client applications</span></span>  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="5e7f7-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="5e7f7-112">Parameters</span></span>

 <span data-ttu-id="5e7f7-113">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="5e7f7-113">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="5e7f7-114">[in] Puntero al receptor de aviso que se va a ajustar.</span><span class="sxs-lookup"><span data-stu-id="5e7f7-114">[in] Pointer to the advise sink to be wrapped.</span></span> 
    
 <span data-ttu-id="5e7f7-115">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="5e7f7-115">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="5e7f7-116">[salida] Puntero a un puntero a un nuevo receptor de avisos que ajusta el receptor de avisos al que apunta el _parámetro lpAdviseSink._</span><span class="sxs-lookup"><span data-stu-id="5e7f7-116">[out] Pointer to a pointer to a new advise sink that wraps the advise sink pointed to by the  _lpAdviseSink_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5e7f7-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e7f7-117">Return value</span></span>

<span data-ttu-id="5e7f7-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5e7f7-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5e7f7-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5e7f7-119">Remarks</span></span>

<span data-ttu-id="5e7f7-120">El propósito del contenedor es asegurarse de que se llama a la notificación en el mismo subproceso que llamó a la función **HrThisThreadAdviseSink.**</span><span class="sxs-lookup"><span data-stu-id="5e7f7-120">The purpose of the wrapper is to make sure that notification is called on the same thread that called the **HrThisThreadAdviseSink** function.</span></span> <span data-ttu-id="5e7f7-121">Esta función se usa para proteger las devoluciones de llamada de notificación que deben ejecutarse en un subproceso determinado.</span><span class="sxs-lookup"><span data-stu-id="5e7f7-121">This function is used to protect notification callbacks that must run on a particular thread.</span></span> 
  
<span data-ttu-id="5e7f7-122">Las aplicaciones cliente deben usar **HrThisThreadAdviseSink** para restringir cuando se generan notificaciones, es decir, cuando se realizan llamadas al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) del objeto receptor de notificaciones pasado por el cliente en una llamada **advise** anterior.</span><span class="sxs-lookup"><span data-stu-id="5e7f7-122">Client applications should use **HrThisThreadAdviseSink** to restrict when notifications are generated, that is, when calls are made to the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method of the advise sink object passed by the client in a previous **Advise** call.</span></span> <span data-ttu-id="5e7f7-123">Si las notificaciones se pueden generar de forma arbitraria, una implementación de notificación podría forzar a un cliente a una operación multiproceso cuando eso no fuera apropiado.</span><span class="sxs-lookup"><span data-stu-id="5e7f7-123">If notifications are allowed to be generated arbitrarily, a notification implementation might force a client into multithreaded operation when that would not be appropriate.</span></span> <span data-ttu-id="5e7f7-124">Por ejemplo, un cliente puede usar una biblioteca, como una de las bibliotecas de Microsoft Foundation Class, que no admite llamadas multiproceso.</span><span class="sxs-lookup"><span data-stu-id="5e7f7-124">For example, a client might use a library, such as one of the Microsoft Foundation Class Libraries, that does not support multithreaded calls.</span></span> <span data-ttu-id="5e7f7-125">La notificación en un subproceso diferente haría que un cliente de este tipo sea difícil de probar y propenso a errores.</span><span class="sxs-lookup"><span data-stu-id="5e7f7-125">Notification on a different thread would make such a client difficult to test and prone to error.</span></span> 
  
 <span data-ttu-id="5e7f7-126">**HrThisThreadAdviseSink** se asegura de que las llamadas **a OnNotify** se produzcan solo en estos momentos adecuados:</span><span class="sxs-lookup"><span data-stu-id="5e7f7-126">**HrThisThreadAdviseSink** makes sure that **OnNotify** calls occur only at these appropriate times:</span></span> 
  
- <span data-ttu-id="5e7f7-127">Durante el procesamiento de una llamada a cualquier método MAPI.</span><span class="sxs-lookup"><span data-stu-id="5e7f7-127">During processing of a call to any MAPI method.</span></span> 
    
- <span data-ttu-id="5e7f7-128">Durante el procesamiento de Windows mensajes.</span><span class="sxs-lookup"><span data-stu-id="5e7f7-128">During processing of Windows messages.</span></span> 
    
<span data-ttu-id="5e7f7-129">Cuando se implementa **HrThisThreadAdviseSink,** cualquier llamada al método **OnNotify** del nuevo receptor de notificaciones en cualquier subproceso hace que el método de notificación original se ejecute en el subproceso en el que se llamó a **HrThisThreadAdviseSink.**</span><span class="sxs-lookup"><span data-stu-id="5e7f7-129">When **HrThisThreadAdviseSink** is implemented, any calls to the new advise sink's **OnNotify** method on any thread cause the original notification method to be executed on the thread on which **HrThisThreadAdviseSink** was called.</span></span> 
  
<span data-ttu-id="5e7f7-130">Para obtener más información acerca de los receptores de notificaciones y avisos, vea [Event Notification in MAPI](event-notification-in-mapi.md) e [Implementing an Advise Sink Object](implementing-an-advise-sink-object.md).</span><span class="sxs-lookup"><span data-stu-id="5e7f7-130">For more information about notification and advise sinks, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Implementing an Advise Sink Object](implementing-an-advise-sink-object.md).</span></span> 
  

