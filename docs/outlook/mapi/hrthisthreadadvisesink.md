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
ms.openlocfilehash: 744d9a7588bff89e9d306e516a24da2db3038d4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817098"
---
# <a name="hrthisthreadadvisesink"></a><span data-ttu-id="4a5c0-103">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="4a5c0-103">HrThisThreadAdviseSink</span></span>

  
  
<span data-ttu-id="4a5c0-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4a5c0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4a5c0-105">Crea un receptor de notificaciones que se ajusta un receptor de notificaciones existentes seguridad para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="4a5c0-105">Creates an advise sink that wraps an existing advise sink for thread safety.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4a5c0-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="4a5c0-106">Header file:</span></span>  <br/> |<span data-ttu-id="4a5c0-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="4a5c0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="4a5c0-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="4a5c0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4a5c0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4a5c0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4a5c0-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="4a5c0-110">Called by:</span></span>  <br/> |<span data-ttu-id="4a5c0-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="4a5c0-111">Client applications</span></span>  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="4a5c0-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a5c0-112">Parameters</span></span>

 <span data-ttu-id="4a5c0-113">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="4a5c0-113">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="4a5c0-114">[entrada] Puntero para el receptor de notificaciones que se ajustarán.</span><span class="sxs-lookup"><span data-stu-id="4a5c0-114">[in] Pointer to the advise sink to be wrapped.</span></span> 
    
 <span data-ttu-id="4a5c0-115">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="4a5c0-115">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="4a5c0-116">[out] Puntero a un puntero a un nuevo receptor de notificaciones que se ajusta el receptor de notificaciones que señala el parámetro _lpAdviseSink_ .</span><span class="sxs-lookup"><span data-stu-id="4a5c0-116">[out] Pointer to a pointer to a new advise sink that wraps the advise sink pointed to by the  _lpAdviseSink_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4a5c0-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a5c0-117">Return value</span></span>

<span data-ttu-id="4a5c0-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4a5c0-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4a5c0-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4a5c0-119">Remarks</span></span>

<span data-ttu-id="4a5c0-120">El propósito del contenedor es asegurarse de que la notificación se denomina en el mismo subproceso que llamó a la función **HrThisThreadAdviseSink** .</span><span class="sxs-lookup"><span data-stu-id="4a5c0-120">The purpose of the wrapper is to make sure that notification is called on the same thread that called the **HrThisThreadAdviseSink** function.</span></span> <span data-ttu-id="4a5c0-121">Esta función se usa para proteger las devoluciones de llamada de notificación que se deben ejecutar en un subproceso concreto.</span><span class="sxs-lookup"><span data-stu-id="4a5c0-121">This function is used to protect notification callbacks that must run on a particular thread.</span></span> 
  
<span data-ttu-id="4a5c0-122">Aplicaciones cliente deben usar **HrThisThreadAdviseSink** para restringir cuando se generan notificaciones, es decir, cuando se realizan llamadas al método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) del objeto receptor advise que se pasan por el cliente en un **anterior Advise **de llamadas.</span><span class="sxs-lookup"><span data-stu-id="4a5c0-122">Client applications should use **HrThisThreadAdviseSink** to restrict when notifications are generated, that is, when calls are made to the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method of the advise sink object passed by the client in a previous **Advise** call.</span></span> <span data-ttu-id="4a5c0-123">Si se permiten las notificaciones que se genere arbitrariamente, una implementación de notificación podría forzar a un cliente en funcionamiento multiproceso cuando que no sería adecuado.</span><span class="sxs-lookup"><span data-stu-id="4a5c0-123">If notifications are allowed to be generated arbitrarily, a notification implementation might force a client into multithreaded operation when that would not be appropriate.</span></span> <span data-ttu-id="4a5c0-124">Por ejemplo, un cliente puede usar una biblioteca, como una de las bibliotecas de clases de Microsoft Foundation, que no admite llamadas multiproceso.</span><span class="sxs-lookup"><span data-stu-id="4a5c0-124">For example, a client might use a library, such as one of the Microsoft Foundation Class Libraries, that does not support multithreaded calls.</span></span> <span data-ttu-id="4a5c0-125">Notificación en un subproceso diferente haría que este tipo de cliente difícil probar y propensas a errores.</span><span class="sxs-lookup"><span data-stu-id="4a5c0-125">Notification on a different thread would make such a client difficult to test and prone to error.</span></span> 
  
 <span data-ttu-id="4a5c0-126">**HrThisThreadAdviseSink** se asegura de que las llamadas de **OnNotify** se producen sólo en estos momentos adecuados:</span><span class="sxs-lookup"><span data-stu-id="4a5c0-126">**HrThisThreadAdviseSink** makes sure that **OnNotify** calls occur only at these appropriate times:</span></span> 
  
- <span data-ttu-id="4a5c0-127">Durante el procesamiento de una llamada a cualquier método de MAPI.</span><span class="sxs-lookup"><span data-stu-id="4a5c0-127">During processing of a call to any MAPI method.</span></span> 
    
- <span data-ttu-id="4a5c0-128">Durante el procesamiento de los mensajes de Windows.</span><span class="sxs-lookup"><span data-stu-id="4a5c0-128">During processing of Windows messages.</span></span> 
    
<span data-ttu-id="4a5c0-129">Cuando se implementa **HrThisThreadAdviseSink** , las llamadas al método de **OnNotify** del receptor de notificaciones nuevas en cualquier subproceso que el método de notificación original que se debe ejecutar en el subproceso en el que se llamó a **HrThisThreadAdviseSink** .</span><span class="sxs-lookup"><span data-stu-id="4a5c0-129">When **HrThisThreadAdviseSink** is implemented, any calls to the new advise sink's **OnNotify** method on any thread cause the original notification method to be executed on the thread on which **HrThisThreadAdviseSink** was called.</span></span> 
  
<span data-ttu-id="4a5c0-130">Para obtener más información acerca de la notificación y receptores de notificaciones, vea la [Notificación de eventos en MAPI](event-notification-in-mapi.md) y la [implementación de un objeto de receptor de aviso](implementing-an-advise-sink-object.md).</span><span class="sxs-lookup"><span data-stu-id="4a5c0-130">For more information about notification and advise sinks, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Implementing an Advise Sink Object](implementing-an-advise-sink-object.md).</span></span> 
  

