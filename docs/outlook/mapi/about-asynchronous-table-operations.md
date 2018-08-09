---
title: Acerca de las operaciones asincrónicas de tabla
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 99bff153d4ce4bac3f85e0ed0feeaffafa6bf3f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816349"
---
# <a name="about-asynchronous-table-operations"></a><span data-ttu-id="1aa2f-103">Acerca de las operaciones asincrónicas de tabla</span><span class="sxs-lookup"><span data-stu-id="1aa2f-103">About asynchronous table operations</span></span>
 
<span data-ttu-id="1aa2f-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1aa2f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1aa2f-105">La interfaz **IMAPITable** incluye tres métodos que operan de forma asincrónica y tres métodos para controlar una operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="1aa2f-105">The **IMAPITable** interface includes three methods that operate asynchronously and three methods for controlling an asynchronous operation.</span></span> <span data-ttu-id="1aa2f-106">En la siguiente tabla se enumera estos métodos:</span><span class="sxs-lookup"><span data-stu-id="1aa2f-106">The following table lists these methods:</span></span> 
  
|<span data-ttu-id="1aa2f-107">**Operación asincrónica**</span><span class="sxs-lookup"><span data-stu-id="1aa2f-107">**Asynchronous operation**</span></span>|<span data-ttu-id="1aa2f-108">**Método de control asincrónico**</span><span class="sxs-lookup"><span data-stu-id="1aa2f-108">**Asynchronous control method**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1aa2f-109">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="1aa2f-109">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |[<span data-ttu-id="1aa2f-110">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="1aa2f-110">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md) <br/> |
|[<span data-ttu-id="1aa2f-111">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="1aa2f-111">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |[<span data-ttu-id="1aa2f-112">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="1aa2f-112">IMAPITable::Abort</span></span>](imapitable-abort.md) <br/> |
|[<span data-ttu-id="1aa2f-113">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="1aa2f-113">IMAPITable::SortTable</span></span>](imapitable-sorttable.md) <br/> |[<span data-ttu-id="1aa2f-114">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="1aa2f-114">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |
   
<span data-ttu-id="1aa2f-115">**Para recuperar información de estado sobre el tipo y la operación actual de una tabla**</span><span class="sxs-lookup"><span data-stu-id="1aa2f-115">**To retrieve status information about a table's type and current operation**</span></span>
  
- <span data-ttu-id="1aa2f-116">Llame a [IMAPITable::GetStatus](imapitable-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="1aa2f-116">Call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span> <span data-ttu-id="1aa2f-117">Con **GetStatus**, un usuario de la tabla puede determinar si la tabla es estático o dinámico, si una operación está en curso o ha finalizado y si se ha producido un error de una operación completada.</span><span class="sxs-lookup"><span data-stu-id="1aa2f-117">With **GetStatus**, a table user can determine whether the table is static or dynamic, if an operation is in progress or has completed, and if an error has occurred from a completed operation.</span></span> <span data-ttu-id="1aa2f-118">Por ejemplo, si un cliente necesita cancelar una operación de ordenación porque se está tardando demasiado tiempo, el cliente puede llamar primero **GetStatus** para determinar si, en realidad, una operación de ordenación es actualmente el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="1aa2f-118">For example, if a client needs to cancel a sort operation because it is taking too much time, the client can first call **GetStatus** to determine whether, in fact, a sort operation is presently processing.</span></span> <span data-ttu-id="1aa2f-119">A continuación, el cliente puede llamar a [IMAPITable::Abort](imapitable-abort.md) para que deje.</span><span class="sxs-lookup"><span data-stu-id="1aa2f-119">Then the client can call [IMAPITable::Abort](imapitable-abort.md) to stop it.</span></span> 
    
<span data-ttu-id="1aa2f-120">**Para suspender la actividad hasta que haya finalizado una tarea asincrónica**</span><span class="sxs-lookup"><span data-stu-id="1aa2f-120">**To suspend activity until an asynchronous task has completed**</span></span>
  
- <span data-ttu-id="1aa2f-121">Llame a [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span><span class="sxs-lookup"><span data-stu-id="1aa2f-121">Call [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span></span> <span data-ttu-id="1aa2f-122">Una llamada a **WaitForCompletion** permite la tarea se complete sin interrupciones.</span><span class="sxs-lookup"><span data-stu-id="1aa2f-122">Calling **WaitForCompletion** allows the task to complete without interruption.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="1aa2f-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="1aa2f-123">See also</span></span>

- [<span data-ttu-id="1aa2f-124">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="1aa2f-124">MAPI Tables</span></span>](mapi-tables.md)

