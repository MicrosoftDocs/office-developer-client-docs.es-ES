---
title: Aplazamiento del procesamiento
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2d3fbf8f7a725f121579066001715fb0bc6beba0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430934"
---
# <a name="deferring-processing"></a><span data-ttu-id="bca86-103">Aplazamiento del procesamiento</span><span class="sxs-lookup"><span data-stu-id="bca86-103">Deferring Processing</span></span>

  
  
<span data-ttu-id="bca86-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bca86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bca86-105">Pase la marca MAPI_DEFERRED_ERRORS a las llamadas de método tanto como sea posible.</span><span class="sxs-lookup"><span data-stu-id="bca86-105">Pass the MAPI_DEFERRED_ERRORS flag to method calls as much as possible.</span></span> <span data-ttu-id="bca86-106">Muchas de las llamadas al método MAPI se han optimizado para aceptar esta marca, lo que hace que el proveedor posponga la tarea solicitada hasta que se puedan realizar varias tareas a la vez o no puede esperar más a los resultados.</span><span class="sxs-lookup"><span data-stu-id="bca86-106">Many of the MAPI method calls have been optimized to accept this flag, causing the provider to either postpone the requested task until multiple tasks can be performed at once or you can wait no longer for the results.</span></span>
  
<span data-ttu-id="bca86-107">Por ejemplo, si pasa MAPI_DEFERRED_ERRORS a [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir una carpeta, la apertura de la carpeta y una posible llamada remota se pueden posponer hasta que realice otra llamada, como una llamada a los métodos **GetHierarchyTable** o **GetProps** de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="bca86-107">For example, if you pass MAPI_DEFERRED_ERRORS to [IMsgStore::OpenEntry](imsgstore-openentry.md) to open a folder, the opening of the folder and a possible remote call can be postponed until you make another call such as a call to the folder's **GetHierarchyTable** or **GetProps** methods.</span></span> <span data-ttu-id="bca86-108">Tanto **GetHierarchyTable** como **GetProps** requieren la devolución de datos del proveedor de servicios, una tarea que debe realizarse inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="bca86-108">Both **GetHierarchyTable** and **GetProps** require the return of data from the service provider, a task that must be performed immediately.</span></span> 
  
<span data-ttu-id="bca86-109">Otra forma de aplazar el procesamiento es simplemente no realizar una llamada.</span><span class="sxs-lookup"><span data-stu-id="bca86-109">Another way to defer processing is simply not to make a call.</span></span> <span data-ttu-id="bca86-110">Al ser consciente del usuario y cuando el usuario puede percibir un vaciado de recursos o tiempo de procesamiento, puede determinar cuándo tiene sentido realizar llamadas.</span><span class="sxs-lookup"><span data-stu-id="bca86-110">By being aware of the user and when the user can perceive a drain on resources or processing time, you can determine when it makes sense to make calls.</span></span> <span data-ttu-id="bca86-111">Existe la oportunidad de mejorar el rendimiento realizando llamadas en un momento en el que el usuario no se dará cuenta o al no realizarlas en absoluto.</span><span class="sxs-lookup"><span data-stu-id="bca86-111">There is an opportunity to improve performance by making calls either at a time when the user will not notice or by not making them at all.</span></span>
  
<span data-ttu-id="bca86-112">Por ejemplo, considere la situación cuando recibe más de una notificación por segundo desde un almacén de mensajes que mueve un gran número de mensajes.</span><span class="sxs-lookup"><span data-stu-id="bca86-112">For example, consider the situation when you are receiving more than one notification per second from a message store that is moving a great number of messages.</span></span> <span data-ttu-id="bca86-113">Se muestra un indicador de progreso para indicar el porcentaje de finalización de la operación.</span><span class="sxs-lookup"><span data-stu-id="bca86-113">A progress indicator is displayed to indicate the percentage of the operation's completion.</span></span> <span data-ttu-id="bca86-114">Por lo general, los usuarios no perciben que esta operación sea lenta hasta que transcurran unos segundos.</span><span class="sxs-lookup"><span data-stu-id="bca86-114">Users typically will not perceive this operation to be slow until a few seconds have passed.</span></span> <span data-ttu-id="bca86-115">Por lo tanto, si va a actualizar el indicador de progreso, no realice ningún cambio hasta al menos cuatro segundos después del inicio de la operación de movimiento.</span><span class="sxs-lookup"><span data-stu-id="bca86-115">Therefore, if you are updating the progress indicator, do not make any changes until at least four seconds after the initiation of the move operation.</span></span> <span data-ttu-id="bca86-116">Esto ahorrará tiempo en los casos comunes cuando la operación es rápida e informará a los usuarios de forma oportuna cuando la operación es lenta.</span><span class="sxs-lookup"><span data-stu-id="bca86-116">This will save time in the common cases when the operation is fast and inform users in a timely manner when the operation is slow.</span></span>
  

