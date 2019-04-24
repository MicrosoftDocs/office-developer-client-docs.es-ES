---
title: Acerca de las notificaciones de tabla
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00c9c6c2-fc21-4b9c-91fa-629450a22d37
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9a42ed1e196e8ac498ab5889b4419ff407db4748
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321843"
---
# <a name="about-table-notifications"></a><span data-ttu-id="e1f39-103">Acerca de las notificaciones de tabla</span><span class="sxs-lookup"><span data-stu-id="e1f39-103">About Table Notifications</span></span>

  
  
<span data-ttu-id="e1f39-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1f39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1f39-105">Los clientes suelen basarse en las notificaciones de tabla para obtener información sobre los cambios en los objetos en lugar de registrarse para recibir notificaciones directamente de los objetos.</span><span class="sxs-lookup"><span data-stu-id="e1f39-105">Clients often rely on table notifications to learn of changes to objects instead of registering to receive notifications directly from the objects.</span></span> <span data-ttu-id="e1f39-106">Los cambios típicos que provocan que se envíen las notificaciones son la adición, la eliminación o la modificación de una fila y cualquier error crítico.</span><span class="sxs-lookup"><span data-stu-id="e1f39-106">Typical changes that cause notifications to be sent include the addition, deletion, or modification of a row and any critical error.</span></span> <span data-ttu-id="e1f39-107">Cuando llegan las notificaciones, los clientes pueden determinar si hacen otra llamada para volver a cargar la tabla.</span><span class="sxs-lookup"><span data-stu-id="e1f39-107">When notifications arrive, clients can determine whether to make another call to reload the table.</span></span> 
  
<span data-ttu-id="e1f39-108">Como las notificaciones de tabla son asincrónicas, hay algunos problemas que pueden hacer que las notificaciones de control sean menos que sencillas:</span><span class="sxs-lookup"><span data-stu-id="e1f39-108">Because table notifications are asynchronous, there are a few issues that can make handling notifications less than straightforward:</span></span>
  
- <span data-ttu-id="e1f39-109">Es posible que los datos pasados en la estructura [TABLE_NOTIFICATION](table_notification.md) no representen el estado más actual de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e1f39-109">The data passed in the [TABLE_NOTIFICATION](table_notification.md) structure might not represent the table's most current state.</span></span> <span data-ttu-id="e1f39-110">Por ejemplo, es posible que un cliente realice un cambio en un mensaje y, a continuación, decida eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="e1f39-110">For example, a client might make a change to a message and then decide to delete it.</span></span> <span data-ttu-id="e1f39-111">El proveedor de almacenamiento de mensajes que implementa la tabla de contenido que incluye el mensaje envía dos notificaciones: un evento TABLE_ROW_MODIFIED seguido de un evento TABLE_ROW_DELETED.</span><span class="sxs-lookup"><span data-stu-id="e1f39-111">The message store provider implementing the contents table that included the message sends two notifications: a TABLE_ROW_MODIFIED event followed by a TABLE_ROW_DELETED event.</span></span> <span data-ttu-id="e1f39-112">Según el modo en que el proveedor de almacenamiento de mensajes multiplica las notificaciones, es posible que el cliente reciba la notificación TABLE_ROW_MODIFIED después de eliminar la fila.</span><span class="sxs-lookup"><span data-stu-id="e1f39-112">Depending on how the message store provider times notifications, the client might receive the TABLE_ROW_MODIFIED notification after the deletion of the row.</span></span> 
    
- <span data-ttu-id="e1f39-113">El conjunto de columnas incluido en una notificación podría ser diferente al conjunto de columnas actual de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e1f39-113">The column set included with a notification might be different from the table's current column set.</span></span> <span data-ttu-id="e1f39-114">MAPI requiere que el conjunto de columnas de notificación se ajuste a la columna que estaba en vigor en el momento en que se generó la notificación.</span><span class="sxs-lookup"><span data-stu-id="e1f39-114">MAPI requires that the notification column set match the column set that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="e1f39-115">Debido a que es posible que un cliente llame a [IMAPITable:: SetColumns](imapitable-setcolumns.md) para alterar el conjunto de columnas en cualquier momento, incluso después de una notificación, es posible que los dos conjuntos de columnas no se sincronicen.</span><span class="sxs-lookup"><span data-stu-id="e1f39-115">Because it is possible for a client to call [IMAPITable::SetColumns](imapitable-setcolumns.md) to alter the column set at any time — including after a notification — the two column sets may not be synchronized.</span></span> 
    
- <span data-ttu-id="e1f39-116">Las notificaciones de tabla solo se envían para las filas que forman parte de la vista.</span><span class="sxs-lookup"><span data-stu-id="e1f39-116">Table notifications are only sent for rows that are part of the view.</span></span> <span data-ttu-id="e1f39-117">Es decir, si una fila se excluye de la vista debido a una restricción o porque la tabla está en estado contraído, no se enviará ninguna notificación si la fila cambia.</span><span class="sxs-lookup"><span data-stu-id="e1f39-117">That is, if a row is excluded from the view due to a restriction or because the table is in a collapsed state, no notification will be sent if that row changes.</span></span> <span data-ttu-id="e1f39-118">Además, no se envía ninguna notificación para informar a un cliente sobre un cambio en el estado de la categoría.</span><span class="sxs-lookup"><span data-stu-id="e1f39-118">Also, no notifications are sent to inform a client about a change in category state.</span></span>
    
<span data-ttu-id="e1f39-119">Los clientes deben tener en cuenta que no todas las tablas admiten la notificación TABLE_SORT_DONE y deben estar preparadas para controlar esta condición:</span><span class="sxs-lookup"><span data-stu-id="e1f39-119">Clients should be aware that not all tables support the TABLE_SORT_DONE notification and should be prepared to handle this condition by:</span></span>
  
1. <span data-ttu-id="e1f39-120">Obligar a la ordenación a ser sincrónica.</span><span class="sxs-lookup"><span data-stu-id="e1f39-120">Forcing the sort to be synchronous.</span></span>
    
2. <span data-ttu-id="e1f39-121">Volver a cargar las filas de la tabla cuando se devuelve [IMAPITable:: SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="e1f39-121">Reloading the rows of the table when [IMAPITable::SortTable](imapitable-sorttable.md) returns.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e1f39-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1f39-122">See also</span></span>



[<span data-ttu-id="e1f39-123">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="e1f39-123">MAPI Tables</span></span>](mapi-tables.md)

