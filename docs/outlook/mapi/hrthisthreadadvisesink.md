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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346840"
---
# <a name="hrthisthreadadvisesink"></a><span data-ttu-id="81e9c-103">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="81e9c-103">HrThisThreadAdviseSink</span></span>

  
  
<span data-ttu-id="81e9c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81e9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81e9c-105">Crea un receptor de notificaciones que encapsula un receptor de notificaciones existente para la seguridad de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="81e9c-105">Creates an advise sink that wraps an existing advise sink for thread safety.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="81e9c-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="81e9c-106">Header file:</span></span>  <br/> |<span data-ttu-id="81e9c-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="81e9c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="81e9c-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="81e9c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="81e9c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="81e9c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="81e9c-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="81e9c-110">Called by:</span></span>  <br/> |<span data-ttu-id="81e9c-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="81e9c-111">Client applications</span></span>  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="81e9c-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="81e9c-112">Parameters</span></span>

 <span data-ttu-id="81e9c-113">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="81e9c-113">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="81e9c-114">a Puntero al receptor de notificaciones que se va a ajustar.</span><span class="sxs-lookup"><span data-stu-id="81e9c-114">[in] Pointer to the advise sink to be wrapped.</span></span> 
    
 <span data-ttu-id="81e9c-115">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="81e9c-115">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="81e9c-116">contempla Puntero a un puntero a un nuevo receptor de notificaciones que encapsula el receptor de notificaciones al que apunta el parámetro _lpAdviseSink_ .</span><span class="sxs-lookup"><span data-stu-id="81e9c-116">[out] Pointer to a pointer to a new advise sink that wraps the advise sink pointed to by the  _lpAdviseSink_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="81e9c-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81e9c-117">Return value</span></span>

<span data-ttu-id="81e9c-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="81e9c-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="81e9c-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="81e9c-119">Remarks</span></span>

<span data-ttu-id="81e9c-120">El propósito del contenedor es asegurarse de que se llama a la notificación en el mismo subproceso que llamó a la función **HrThisThreadAdviseSink** .</span><span class="sxs-lookup"><span data-stu-id="81e9c-120">The purpose of the wrapper is to make sure that notification is called on the same thread that called the **HrThisThreadAdviseSink** function.</span></span> <span data-ttu-id="81e9c-121">Esta función se usa para proteger las devoluciones de llamada de notificaciones que se deben ejecutar en un subproceso en particular.</span><span class="sxs-lookup"><span data-stu-id="81e9c-121">This function is used to protect notification callbacks that must run on a particular thread.</span></span> 
  
<span data-ttu-id="81e9c-122">Las aplicaciones cliente deben usar **HrThisThreadAdviseSink** para restringir Cuándo se generan las notificaciones, es decir, cuando se realizan llamadas al método [IMAPIAdviseSink:: método Notify](imapiadvisesink-onnotify.md) del objeto de notificación de notificaciones que pasa el cliente en una \*\*notificación anterior \*\*llamar.</span><span class="sxs-lookup"><span data-stu-id="81e9c-122">Client applications should use **HrThisThreadAdviseSink** to restrict when notifications are generated, that is, when calls are made to the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method of the advise sink object passed by the client in a previous **Advise** call.</span></span> <span data-ttu-id="81e9c-123">Si se permite generar arbitrariamente las notificaciones, una implementación de notificaciones puede forzar a un cliente en una operación multiproceso cuando no sería adecuada.</span><span class="sxs-lookup"><span data-stu-id="81e9c-123">If notifications are allowed to be generated arbitrarily, a notification implementation might force a client into multithreaded operation when that would not be appropriate.</span></span> <span data-ttu-id="81e9c-124">Por ejemplo, un cliente podría usar una biblioteca, como una de las bibliotecas de Microsoft Foundation Class, que no es compatible con llamadas multiproceso.</span><span class="sxs-lookup"><span data-stu-id="81e9c-124">For example, a client might use a library, such as one of the Microsoft Foundation Class Libraries, that does not support multithreaded calls.</span></span> <span data-ttu-id="81e9c-125">La notificación en un subproceso diferente haría que un cliente de este tipo sería difícil de probar y propenso a errores.</span><span class="sxs-lookup"><span data-stu-id="81e9c-125">Notification on a different thread would make such a client difficult to test and prone to error.</span></span> 
  
 <span data-ttu-id="81e9c-126">**HrThisThreadAdviseSink** asegura que las llamadas a **Notify** solo se producen en las siguientes horas adecuadas:</span><span class="sxs-lookup"><span data-stu-id="81e9c-126">**HrThisThreadAdviseSink** makes sure that **OnNotify** calls occur only at these appropriate times:</span></span> 
  
- <span data-ttu-id="81e9c-127">Durante el procesamiento de una llamada a cualquier método de MAPI.</span><span class="sxs-lookup"><span data-stu-id="81e9c-127">During processing of a call to any MAPI method.</span></span> 
    
- <span data-ttu-id="81e9c-128">Durante el procesamiento de los mensajes de Windows.</span><span class="sxs-lookup"><span data-stu-id="81e9c-128">During processing of Windows messages.</span></span> 
    
<span data-ttu-id="81e9c-129">Cuando se implementa **HrThisThreadAdviseSink** , cualquier llamada al método de **Notify** del receptor de notificación nuevo en cualquier subproceso causa el método de notificación original que se ejecuta en el subproceso en el que se llamó a **HrThisThreadAdviseSink** .</span><span class="sxs-lookup"><span data-stu-id="81e9c-129">When **HrThisThreadAdviseSink** is implemented, any calls to the new advise sink's **OnNotify** method on any thread cause the original notification method to be executed on the thread on which **HrThisThreadAdviseSink** was called.</span></span> 
  
<span data-ttu-id="81e9c-130">Para obtener más información acerca de los receptores de notificaciones y avisos, vea [notificación de eventos en MAPI](event-notification-in-mapi.md) e [implementación de un objeto](implementing-an-advise-sink-object.md)de notificación de aviso.</span><span class="sxs-lookup"><span data-stu-id="81e9c-130">For more information about notification and advise sinks, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Implementing an Advise Sink Object](implementing-an-advise-sink-object.md).</span></span> 
  

