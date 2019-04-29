---
title: Información sobre las operaciones de tabla asincrónica
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: eebc04e2263b4a2037e167bd464a31d298b84664
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439572"
---
# <a name="about-asynchronous-table-operations"></a><span data-ttu-id="73b52-103">Información sobre las operaciones de tabla asincrónica</span><span class="sxs-lookup"><span data-stu-id="73b52-103">About asynchronous table operations</span></span>
 
<span data-ttu-id="73b52-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73b52-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73b52-105">La interfaz **IMAPITable** incluye tres métodos que funcionan de forma asincrónica y tres métodos para controlar una operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="73b52-105">The **IMAPITable** interface includes three methods that operate asynchronously and three methods for controlling an asynchronous operation.</span></span> <span data-ttu-id="73b52-106">En la siguiente tabla se enumeran estos métodos:</span><span class="sxs-lookup"><span data-stu-id="73b52-106">The following table lists these methods:</span></span> 
  
|<span data-ttu-id="73b52-107">**Operación asincrónica**</span><span class="sxs-lookup"><span data-stu-id="73b52-107">**Asynchronous operation**</span></span>|<span data-ttu-id="73b52-108">**Método de control asincrónico**</span><span class="sxs-lookup"><span data-stu-id="73b52-108">**Asynchronous control method**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73b52-109">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="73b52-109">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |[<span data-ttu-id="73b52-110">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="73b52-110">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md) <br/> |
|[<span data-ttu-id="73b52-111">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="73b52-111">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |[<span data-ttu-id="73b52-112">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="73b52-112">IMAPITable::Abort</span></span>](imapitable-abort.md) <br/> |
|[<span data-ttu-id="73b52-113">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="73b52-113">IMAPITable::SortTable</span></span>](imapitable-sorttable.md) <br/> |[<span data-ttu-id="73b52-114">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="73b52-114">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md) <br/> |
   
<span data-ttu-id="73b52-115">**Para recuperar información de estado sobre el tipo de una tabla y la operación actual**</span><span class="sxs-lookup"><span data-stu-id="73b52-115">**To retrieve status information about a table's type and current operation**</span></span>
  
- <span data-ttu-id="73b52-116">Llame al [IMAPITable:: getStatus](imapitable-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="73b52-116">Call [IMAPITable::GetStatus](imapitable-getstatus.md).</span></span> <span data-ttu-id="73b52-117">Con **getStatus**, un usuario de tabla puede determinar si la tabla es estática o dinámica, si una operación está en curso o ha finalizado, y si se ha producido un error en una operación completada.</span><span class="sxs-lookup"><span data-stu-id="73b52-117">With **GetStatus**, a table user can determine whether the table is static or dynamic, if an operation is in progress or has completed, and if an error has occurred from a completed operation.</span></span> <span data-ttu-id="73b52-118">Por ejemplo, si un cliente necesita cancelar una operación de ordenación porque está tardando demasiado tiempo, el cliente puede llamar primero a **getStatus** para determinar si, de hecho, se está procesando actualmente una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="73b52-118">For example, if a client needs to cancel a sort operation because it is taking too much time, the client can first call **GetStatus** to determine whether, in fact, a sort operation is presently processing.</span></span> <span data-ttu-id="73b52-119">A continuación, el cliente puede llamar al método [IMAPITable:: ABORT](imapitable-abort.md) para detenerlo.</span><span class="sxs-lookup"><span data-stu-id="73b52-119">Then the client can call [IMAPITable::Abort](imapitable-abort.md) to stop it.</span></span> 
    
<span data-ttu-id="73b52-120">**Para suspender la actividad hasta que se complete una tarea asincrónica**</span><span class="sxs-lookup"><span data-stu-id="73b52-120">**To suspend activity until an asynchronous task has completed**</span></span>
  
- <span data-ttu-id="73b52-121">Llame al [IMAPITable:: WaitForCompletion](imapitable-waitforcompletion.md).</span><span class="sxs-lookup"><span data-stu-id="73b52-121">Call [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md).</span></span> <span data-ttu-id="73b52-122">Llamar a **WaitForCompletion** permite que la tarea se complete sin interrupciones.</span><span class="sxs-lookup"><span data-stu-id="73b52-122">Calling **WaitForCompletion** allows the task to complete without interruption.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="73b52-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="73b52-123">See also</span></span>

- [<span data-ttu-id="73b52-124">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="73b52-124">MAPI Tables</span></span>](mapi-tables.md)

