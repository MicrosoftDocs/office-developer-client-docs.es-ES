---
title: Procesamiento diferido
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 8f26fc6a51c3abdb4d4d009183fa8263ce97b261
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816635"
---
# <a name="deferring-processing"></a><span data-ttu-id="0631f-103">Procesamiento diferido</span><span class="sxs-lookup"><span data-stu-id="0631f-103">Deferring Processing</span></span>

  
  
<span data-ttu-id="0631f-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0631f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0631f-105">Pase el indicador MAPI_DEFERRED_ERRORS a las llamadas de método medida de lo posible.</span><span class="sxs-lookup"><span data-stu-id="0631f-105">Pass the MAPI_DEFERRED_ERRORS flag to method calls as much as possible.</span></span> <span data-ttu-id="0631f-106">Muchas de las llamadas al método MAPI se han optimizado para que acepte esta marca, lo que provoca que el proveedor ya sea posponer la tarea solicitada hasta que se pueden realizar varias tareas a la vez o puede esperar a que los resultados ya no.</span><span class="sxs-lookup"><span data-stu-id="0631f-106">Many of the MAPI method calls have been optimized to accept this flag, causing the provider to either postpone the requested task until multiple tasks can be performed at once or you can wait no longer for the results.</span></span>
  
<span data-ttu-id="0631f-107">Por ejemplo, si se pasa MAPI_DEFERRED_ERRORS a [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir una carpeta, la apertura de la carpeta y un posible remoto de llamadas se puede posponer hasta que se realiza otra llamada, como una llamada a la carpeta **GetHierarchyTable** o ** GetProps** métodos.</span><span class="sxs-lookup"><span data-stu-id="0631f-107">For example, if you pass MAPI_DEFERRED_ERRORS to [IMsgStore::OpenEntry](imsgstore-openentry.md) to open a folder, the opening of the folder and a possible remote call can be postponed until you make another call such as a call to the folder's **GetHierarchyTable** or **GetProps** methods.</span></span> <span data-ttu-id="0631f-108">**GetHierarchyTable** y **GetProps** requieren la devolución de datos del proveedor de servicios, una tarea que se debe realizar inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="0631f-108">Both **GetHierarchyTable** and **GetProps** require the return of data from the service provider, a task that must be performed immediately.</span></span> 
  
<span data-ttu-id="0631f-109">Otra forma de procesarla es simplemente no realizar una llamada.</span><span class="sxs-lookup"><span data-stu-id="0631f-109">Another way to defer processing is simply not to make a call.</span></span> <span data-ttu-id="0631f-110">Al que se va a tener en cuenta del usuario y cuando el usuario puede perciben un consumo de recursos o el tiempo de procesamiento, puede determinar cuando tenga sentido para realizar llamadas.</span><span class="sxs-lookup"><span data-stu-id="0631f-110">By being aware of the user and when the user can perceive a drain on resources or processing time, you can determine when it makes sense to make calls.</span></span> <span data-ttu-id="0631f-111">No hay una oportunidad para mejorar el rendimiento mediante la realización de llamadas, ya sea a la vez cuando el usuario no observará o por no realizarlos.</span><span class="sxs-lookup"><span data-stu-id="0631f-111">There is an opportunity to improve performance by making calls either at a time when the user will not notice or by not making them at all.</span></span>
  
<span data-ttu-id="0631f-112">Por ejemplo, considere la situación cuando recibe más de una notificación por segundo desde un almacén de mensajes que está moviendo un gran número de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0631f-112">For example, consider the situation when you are receiving more than one notification per second from a message store that is moving a great number of messages.</span></span> <span data-ttu-id="0631f-113">Se muestra un indicador de progreso para indicar el porcentaje de finalización de la operación.</span><span class="sxs-lookup"><span data-stu-id="0631f-113">A progress indicator is displayed to indicate the percentage of the operation's completion.</span></span> <span data-ttu-id="0631f-114">Normalmente, los usuarios no notarán esta operación para ser lenta, hasta que se han pasado unos segundos.</span><span class="sxs-lookup"><span data-stu-id="0631f-114">Users typically will not perceive this operation to be slow until a few seconds have passed.</span></span> <span data-ttu-id="0631f-115">Por lo tanto, si va a actualizar el indicador de progreso, no realice ningún cambio hasta que al menos cuatro segundos después de la iniciación de la operación de movimiento.</span><span class="sxs-lookup"><span data-stu-id="0631f-115">Therefore, if you are updating the progress indicator, do not make any changes until at least four seconds after the initiation of the move operation.</span></span> <span data-ttu-id="0631f-116">Esto va a ahorrar tiempo en los casos comunes cuando la operación es rápida e informar a los usuarios de manera oportuna cuando la operación es lenta.</span><span class="sxs-lookup"><span data-stu-id="0631f-116">This will save time in the common cases when the operation is fast and inform users in a timely manner when the operation is slow.</span></span>
  

