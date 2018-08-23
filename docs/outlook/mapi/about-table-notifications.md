---
title: Información sobre las notificaciones de tabla
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00c9c6c2-fc21-4b9c-91fa-629450a22d37
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d6fd49e1a004202e0de02e262f6977ca8a07019d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571944"
---
# <a name="about-table-notifications"></a><span data-ttu-id="006f8-103">Información sobre las notificaciones de tabla</span><span class="sxs-lookup"><span data-stu-id="006f8-103">About Table Notifications</span></span>

  
  
<span data-ttu-id="006f8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="006f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="006f8-105">Los clientes a menudo se basan en las notificaciones de tabla para obtener más información de los cambios a objetos en lugar de registrar para recibir notificaciones directamente desde los objetos.</span><span class="sxs-lookup"><span data-stu-id="006f8-105">Clients often rely on table notifications to learn of changes to objects instead of registering to receive notifications directly from the objects.</span></span> <span data-ttu-id="006f8-106">Los cambios más frecuentes que impedir que se envíen notificaciones incluyen la adición, eliminación o modificación de una fila y cualquier error crítico.</span><span class="sxs-lookup"><span data-stu-id="006f8-106">Typical changes that cause notifications to be sent include the addition, deletion, or modification of a row and any critical error.</span></span> <span data-ttu-id="006f8-107">Cuando se reciben las notificaciones, los clientes pueden determinar si debe realizar otra llamada a volver a cargar en la tabla.</span><span class="sxs-lookup"><span data-stu-id="006f8-107">When notifications arrive, clients can determine whether to make another call to reload the table.</span></span> 
  
<span data-ttu-id="006f8-108">Debido a que las notificaciones de tabla son asincrónicas, hay algunos problemas que pueden hacer que las notificaciones de tratamiento de menos de un proceso sencillo:</span><span class="sxs-lookup"><span data-stu-id="006f8-108">Because table notifications are asynchronous, there are a few issues that can make handling notifications less than straightforward:</span></span>
  
- <span data-ttu-id="006f8-109">Los datos que se pasan en la estructura [TABLE_NOTIFICATION](table_notification.md) no es posible que representan el estado más reciente de la tabla.</span><span class="sxs-lookup"><span data-stu-id="006f8-109">The data passed in the [TABLE_NOTIFICATION](table_notification.md) structure might not represent the table's most current state.</span></span> <span data-ttu-id="006f8-110">Por ejemplo, un cliente podría realizar un cambio en un mensaje y, a continuación, decida eliminarla.</span><span class="sxs-lookup"><span data-stu-id="006f8-110">For example, a client might make a change to a message and then decide to delete it.</span></span> <span data-ttu-id="006f8-111">El proveedor de almacenamiento de mensaje implementación de la tabla de contenido que incluye el mensaje envía dos notificaciones: un evento TABLE_ROW_MODIFIED seguido de un evento TABLE_ROW_DELETED.</span><span class="sxs-lookup"><span data-stu-id="006f8-111">The message store provider implementing the contents table that included the message sends two notifications: a TABLE_ROW_MODIFIED event followed by a TABLE_ROW_DELETED event.</span></span> <span data-ttu-id="006f8-112">Dependiendo de cómo el proveedor de almacenamiento de mensaje veces las notificaciones, el cliente podría recibir la notificación TABLE_ROW_MODIFIED después de la eliminación de la fila.</span><span class="sxs-lookup"><span data-stu-id="006f8-112">Depending on how the message store provider times notifications, the client might receive the TABLE_ROW_MODIFIED notification after the deletion of the row.</span></span> 
    
- <span data-ttu-id="006f8-113">El conjunto incluye con una notificación de columnas pueden ser diferente del conjunto actual de columna de la tabla.</span><span class="sxs-lookup"><span data-stu-id="006f8-113">The column set included with a notification might be different from the table's current column set.</span></span> <span data-ttu-id="006f8-114">MAPI requiere que el conjunto de columnas de notificación coinciden con el conjunto de columnas que estaba en efecto en el momento en que se generó la notificación.</span><span class="sxs-lookup"><span data-stu-id="006f8-114">MAPI requires that the notification column set match the column set that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="006f8-115">Debido a que es posible que un cliente pueda llamar a [IMAPITable::SetColumns](imapitable-setcolumns.md) para modificar la columna establecer en cualquier momento, incluso después de una notificación: no se pueden sincronizar los conjuntos de dos columnas.</span><span class="sxs-lookup"><span data-stu-id="006f8-115">Because it is possible for a client to call [IMAPITable::SetColumns](imapitable-setcolumns.md) to alter the column set at any time — including after a notification — the two column sets may not be synchronized.</span></span> 
    
- <span data-ttu-id="006f8-116">Tabla solo se envían para las filas que forman parte de la vista.</span><span class="sxs-lookup"><span data-stu-id="006f8-116">Table notifications are only sent for rows that are part of the view.</span></span> <span data-ttu-id="006f8-117">Es decir, si una fila se excluye de la vista debido a una restricción o porque la tabla está en un estado contraído, no se enviarán ninguna notificación si cambia de esa fila.</span><span class="sxs-lookup"><span data-stu-id="006f8-117">That is, if a row is excluded from the view due to a restriction or because the table is in a collapsed state, no notification will be sent if that row changes.</span></span> <span data-ttu-id="006f8-118">Además, no se envían a informar a un cliente sobre un cambio en el estado de la categoría.</span><span class="sxs-lookup"><span data-stu-id="006f8-118">Also, no notifications are sent to inform a client about a change in category state.</span></span>
    
<span data-ttu-id="006f8-119">Los clientes deben tener en cuenta que no todas las tablas admiten la notificación TABLE_SORT_DONE y deben estar preparadas para controlar esta condición por:</span><span class="sxs-lookup"><span data-stu-id="006f8-119">Clients should be aware that not all tables support the TABLE_SORT_DONE notification and should be prepared to handle this condition by:</span></span>
  
1. <span data-ttu-id="006f8-120">Forzar la ordenación ser sincrónico.</span><span class="sxs-lookup"><span data-stu-id="006f8-120">Forcing the sort to be synchronous.</span></span>
    
2. <span data-ttu-id="006f8-121">Volver a cargar las filas de la tabla cuando [SortTable](imapitable-sorttable.md) devuelve.</span><span class="sxs-lookup"><span data-stu-id="006f8-121">Reloading the rows of the table when [IMAPITable::SortTable](imapitable-sorttable.md) returns.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="006f8-122">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="006f8-122">See also</span></span>



[<span data-ttu-id="006f8-123">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="006f8-123">MAPI Tables</span></span>](mapi-tables.md)

