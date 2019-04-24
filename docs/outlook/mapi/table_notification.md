---
title: TABLE_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.TABLE_NOTIFICATION
api_type:
- COM
ms.assetid: 48e478c4-6e9a-40ab-a7bb-e6219b743b08
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6c35220529fb88b470c563a0b004bfcf7e63ef76
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345650"
---
# <a name="tablenotification"></a><span data-ttu-id="b243a-103">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="b243a-103">TABLE_NOTIFICATION</span></span>

<span data-ttu-id="b243a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b243a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b243a-105">Describe una fila de una tabla que se ha visto afectada por algún tipo de evento, como un cambio o un error.</span><span class="sxs-lookup"><span data-stu-id="b243a-105">Describes a row in a table that has been affected by some type of event, such as a change or an error.</span></span> <span data-ttu-id="b243a-106">Esto hace que se genere una notificación de tabla.</span><span class="sxs-lookup"><span data-stu-id="b243a-106">This causes a table notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b243a-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b243a-107">Header file:</span></span>  <br/> |<span data-ttu-id="b243a-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b243a-108">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _TABLE_NOTIFICATION
{
  ULONG ulTableEvent;
  HRESULT hResult;
  SPropValue propIndex;
  SPropValue propPrior;
  SRow row;
} TABLE_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="b243a-109">Members</span><span class="sxs-lookup"><span data-stu-id="b243a-109">Members</span></span>

<span data-ttu-id="b243a-110">**ulTableEvent**</span><span class="sxs-lookup"><span data-stu-id="b243a-110">**ulTableEvent**</span></span>
  
> <span data-ttu-id="b243a-111">Máscara de las marcas usadas para representar el tipo de evento de tabla.</span><span class="sxs-lookup"><span data-stu-id="b243a-111">Bitmask of flags used to represent the table event type.</span></span> <span data-ttu-id="b243a-112">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="b243a-112">The following flags can be set:</span></span>
    
<span data-ttu-id="b243a-113">TABLE_CHANGED</span><span class="sxs-lookup"><span data-stu-id="b243a-113">TABLE_CHANGED</span></span> 
  
> <span data-ttu-id="b243a-114">Indica en un nivel alto que algo sobre la tabla ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="b243a-114">Indicates at a high level that something about the table has changed.</span></span> <span data-ttu-id="b243a-115">El estado de la tabla es como estaba antes del evento.</span><span class="sxs-lookup"><span data-stu-id="b243a-115">The table's state is as it was before the event.</span></span> <span data-ttu-id="b243a-116">Esto significa que todas las propiedades, marcadores, posicionamiento actual y selecciones de la interfaz de usuario de **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) siguen siendo válidos.</span><span class="sxs-lookup"><span data-stu-id="b243a-116">This means that all **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) properties, bookmarks, current positioning, and user interface selections are still valid.</span></span> <span data-ttu-id="b243a-117">Controle este evento volviendo a leer la tabla.</span><span class="sxs-lookup"><span data-stu-id="b243a-117">Handle this event by rereading the table.</span></span> <span data-ttu-id="b243a-118">Los proveedores de servicios que no desean implementar notificaciones de tablas enriquecidas envían eventos de TABLE_CHANGED en lugar de eventos más detallados para indicar un tipo de cambio determinado.</span><span class="sxs-lookup"><span data-stu-id="b243a-118">Service providers that do not want to implement rich table notifications send TABLE_CHANGED events instead of more detailed events to indicate a particular type of change.</span></span> 
    
<span data-ttu-id="b243a-119">TABLE_ERROR</span><span class="sxs-lookup"><span data-stu-id="b243a-119">TABLE_ERROR</span></span> 
  
> <span data-ttu-id="b243a-120">Se ha producido un error, normalmente durante el procesamiento de una operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b243a-120">An error has occurred, usually during the processing of an asynchronous operation.</span></span> <span data-ttu-id="b243a-121">Los errores producidos durante el procesamiento de los métodos siguientes pueden generar este evento:</span><span class="sxs-lookup"><span data-stu-id="b243a-121">Errors during the processing of the following methods can generate this event:</span></span> 
    
   - [<span data-ttu-id="b243a-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="b243a-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
   - [<span data-ttu-id="b243a-123">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="b243a-123">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
   - [<span data-ttu-id="b243a-124">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="b243a-124">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
   <span data-ttu-id="b243a-125">Después de recibir un evento TABLE_ERROR, un cliente no puede depender de la exactitud del contenido de la tabla.</span><span class="sxs-lookup"><span data-stu-id="b243a-125">After receiving a TABLE_ERROR event, a client cannot rely on the accuracy of the table contents.</span></span> <span data-ttu-id="b243a-126">Además, es posible que se pierdan las notificaciones pendientes sobre otros cambios.</span><span class="sxs-lookup"><span data-stu-id="b243a-126">Also, pending notifications about other changes might be lost.</span></span> <span data-ttu-id="b243a-127">Es posible que el método [IMAPITable:: GetLastError](imapitable-getlasterror.md) no proporcione información adicional sobre el error porque se generó en algún punto anterior, no necesariamente desde la última llamada al método.</span><span class="sxs-lookup"><span data-stu-id="b243a-127">The [IMAPITable::GetLastError](imapitable-getlasterror.md) method might not provide any additional information about the error because it was generated at some previous point, not necessarily from the last method call.</span></span> 
    
<span data-ttu-id="b243a-128">TABLE_RELOAD</span><span class="sxs-lookup"><span data-stu-id="b243a-128">TABLE_RELOAD</span></span> 
  
> <span data-ttu-id="b243a-129">Los datos de la tabla se deben volver a cargar.</span><span class="sxs-lookup"><span data-stu-id="b243a-129">The data in the table should be reloaded.</span></span> <span data-ttu-id="b243a-130">Los proveedores de servicios envían TABLE_RELOAD cuando, por ejemplo, los datos subyacentes se almacenan en una base de datos y se reemplaza la base de datos.</span><span class="sxs-lookup"><span data-stu-id="b243a-130">Service providers send TABLE_RELOAD when, for example, the underlying data is stored in a database and the database is replaced.</span></span> <span data-ttu-id="b243a-131">Para controlar este evento, supongamos que no hay nada de la tabla que siga siendo válido y que relea la tabla.</span><span class="sxs-lookup"><span data-stu-id="b243a-131">Handle this event by assuming that nothing about the table is still valid and by rereading the table.</span></span> <span data-ttu-id="b243a-132">Todos los marcadores, claves de instancia, estado e información de posicionamiento no son válidos.</span><span class="sxs-lookup"><span data-stu-id="b243a-132">All bookmarks, instance keys, status and positioning information are invalid.</span></span>
    
<span data-ttu-id="b243a-133">TABLE_RESTRICT_DONE</span><span class="sxs-lookup"><span data-stu-id="b243a-133">TABLE_RESTRICT_DONE</span></span> 
  
> <span data-ttu-id="b243a-134">Se ha completado una operación de restricción iniciada con una llamada al método **IMAPITable:: Restrict** .</span><span class="sxs-lookup"><span data-stu-id="b243a-134">A restriction operation initiated with an **IMAPITable::Restrict** method call has completed.</span></span> 
    
<span data-ttu-id="b243a-135">TABLE_ROW_ADDED</span><span class="sxs-lookup"><span data-stu-id="b243a-135">TABLE_ROW_ADDED</span></span> 
  
> <span data-ttu-id="b243a-136">Se ha agregado una fila nueva a la tabla y se ha guardado el objeto correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b243a-136">A new row has been added to the table and the corresponding object saved.</span></span> <span data-ttu-id="b243a-137">Los eventos TABLE_ROW_ADDED se generan después de una llamada al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="b243a-137">TABLE_ROW_ADDED events are generated after a call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
<span data-ttu-id="b243a-138">TABLE_ROW_DELETED</span><span class="sxs-lookup"><span data-stu-id="b243a-138">TABLE_ROW_DELETED</span></span> 
  
> <span data-ttu-id="b243a-139">Se ha quitado una fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="b243a-139">A row has been removed from the table.</span></span> <span data-ttu-id="b243a-140">El miembro **propPrior** se establece en NULL.</span><span class="sxs-lookup"><span data-stu-id="b243a-140">The **propPrior** member is set to NULL.</span></span> 
    
<span data-ttu-id="b243a-141">TABLE_ROW_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="b243a-141">TABLE_ROW_MODIFIED</span></span> 
  
> <span data-ttu-id="b243a-142">Se ha cambiado una fila.</span><span class="sxs-lookup"><span data-stu-id="b243a-142">A row has been changed.</span></span> <span data-ttu-id="b243a-143">El miembro **Row** contiene las propiedades afectadas de la fila.</span><span class="sxs-lookup"><span data-stu-id="b243a-143">The **row** member contains the affected properties for the row.</span></span> <span data-ttu-id="b243a-144">Se envían varios eventos TABLE_ROW_MODIFIED en el orden en que aparecen en la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="b243a-144">Multiple TABLE_ROW_MODIFIED events are sent in the order that they appear in the table view.</span></span> 
    
  <span data-ttu-id="b243a-145">Los eventos TABLE_ROW_MODIFIED se envían después de que los cambios realizados en el objeto correspondiente se hayan confirmado con una llamada al método **IMAPIProp:: SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="b243a-145">TABLE_ROW_MODIFIED events are sent after changes to the corresponding object have been committed with a call to the **IMAPIProp::SaveChanges** method.</span></span> <span data-ttu-id="b243a-146">Si la fila modificada es ahora la primera fila de la tabla, el valor de la etiqueta de propiedad en el miembro **propPrior** es **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b243a-146">If the modified row is now the first row in the table, the value of the property tag in the **propPrior** member is **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
    
<span data-ttu-id="b243a-147">TABLE_SETCOL_DONE</span><span class="sxs-lookup"><span data-stu-id="b243a-147">TABLE_SETCOL_DONE</span></span> 
  
> <span data-ttu-id="b243a-148">Se ha completado una operación de configuración de columna iniciada con una llamada al método **IMAPITable:: SetColumns** .</span><span class="sxs-lookup"><span data-stu-id="b243a-148">A column setting operation initiated with an **IMAPITable::SetColumns** method call has completed.</span></span> 
    
<span data-ttu-id="b243a-149">TABLE_SORT_DONE</span><span class="sxs-lookup"><span data-stu-id="b243a-149">TABLE_SORT_DONE</span></span> 
  
> <span data-ttu-id="b243a-150">Se ha completado una operación de ordenación de tabla iniciada con una llamada al método **IMAPITable:: SortTable** .</span><span class="sxs-lookup"><span data-stu-id="b243a-150">A table sorting operation initiated with an **IMAPITable::SortTable** method call has completed.</span></span> 
    
<span data-ttu-id="b243a-151">**Valores**</span><span class="sxs-lookup"><span data-stu-id="b243a-151">**hResult**</span></span>
  
> <span data-ttu-id="b243a-152">Valor HRESULT del error que se ha producido, si el miembro **ulTableEvent** está establecido en TABLE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="b243a-152">HRESULT value for the error that has occurred, if the **ulTableEvent** member is set to TABLE_ERROR.</span></span> 
    
<span data-ttu-id="b243a-153">**propIndex**</span><span class="sxs-lookup"><span data-stu-id="b243a-153">**propIndex**</span></span>
  
> <span data-ttu-id="b243a-154">Estructura [SPropValue](spropvalue.md) de la propiedad **PR_INSTANCE_KEY** de la fila afectada.</span><span class="sxs-lookup"><span data-stu-id="b243a-154">[SPropValue](spropvalue.md) structure for the **PR_INSTANCE_KEY** property of the affected row.</span></span> 
    
<span data-ttu-id="b243a-155">**propPrior**</span><span class="sxs-lookup"><span data-stu-id="b243a-155">**propPrior**</span></span>
  
> <span data-ttu-id="b243a-156">Estructura **SPropValue** de la propiedad **PR_INSTANCE_KEY** de la fila antes de la afectada.</span><span class="sxs-lookup"><span data-stu-id="b243a-156">**SPropValue** structure for the **PR_INSTANCE_KEY** property of the row before the affected one.</span></span> <span data-ttu-id="b243a-157">Si la fila afectada es la primera fila de la tabla, **propPrior** debe establecerse en **PR_NULL** y no en cero.</span><span class="sxs-lookup"><span data-stu-id="b243a-157">If the affected row is the first row in the table, **propPrior** must be set to **PR_NULL** and not zero.</span></span> <span data-ttu-id="b243a-158">Cero no es una etiqueta de propiedad válida.</span><span class="sxs-lookup"><span data-stu-id="b243a-158">Zero is not a valid property tag.</span></span> 
    
<span data-ttu-id="b243a-159">**columna**</span><span class="sxs-lookup"><span data-stu-id="b243a-159">**row**</span></span>
  
> <span data-ttu-id="b243a-160">Estructura [SRow](srow.md) que describe la fila afectada.</span><span class="sxs-lookup"><span data-stu-id="b243a-160">[SRow](srow.md) structure describing the affected row.</span></span> <span data-ttu-id="b243a-161">Esta estructura se rellena para todos los eventos de notificación de tabla.</span><span class="sxs-lookup"><span data-stu-id="b243a-161">This structure is filled for all table notification events.</span></span> <span data-ttu-id="b243a-162">Para los eventos de notificación de tabla que no pasan datos de fila, el miembro **cValues** de la estructura **SRow** se establece en cero y el miembro **lpProps** se establece en NULL.</span><span class="sxs-lookup"><span data-stu-id="b243a-162">For table notification events that do not pass row data, the **cValues** member of the **SRow** structure is set to zero and the **lpProps** member is set to NULL.</span></span> <span data-ttu-id="b243a-163">Porque esta estructura **SRow** es de solo lectura; los clientes deben realizar una copia de la misma si quieren realizar modificaciones.</span><span class="sxs-lookup"><span data-stu-id="b243a-163">Because this **SRow** structure is read-only; clients must make a copy of it if they want to make modifications.</span></span> <span data-ttu-id="b243a-164">La función [ScDupPropset](scduppropset.md) se puede usar para realizar la copia.</span><span class="sxs-lookup"><span data-stu-id="b243a-164">The [ScDupPropset](scduppropset.md) function can be used to make the copy.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b243a-165">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b243a-165">Remarks</span></span>

<span data-ttu-id="b243a-166">La estructura de **notificación de\_tabla** es uno de los miembros de la Unión de estructuras incluidas en el miembro de **información** de la estructura de [notificación](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="b243a-166">The **TABLE\_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="b243a-167">El miembro **info** incluye una estructura de **notificación de\_tabla** cuando el miembro **UlEventType** de la estructura se establece en _fnevTableModified_.</span><span class="sxs-lookup"><span data-stu-id="b243a-167">The **info** member includes a **TABLE\_NOTIFICATION** structure when the **ulEventType** member of the structure is set to  _fnevTableModified_.</span></span>
  
<span data-ttu-id="b243a-168">El orden y el tipo de las columnas del miembro de fila reflejan el orden y el tipo que estaban en vigor en el momento en que se generó la notificación.</span><span class="sxs-lookup"><span data-stu-id="b243a-168">The order and type of columns in the row member reflect the order and type that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="b243a-169">El orden y el tipo en el momento en que se generó la notificación no es necesariamente el mismo que cuando se entregó la notificación.</span><span class="sxs-lookup"><span data-stu-id="b243a-169">The order and type at the time that the notification was generated is not necessarily the same as when the notification was delivered.</span></span> 
  
<span data-ttu-id="b243a-170">Para obtener más información acerca de las notificaciones, vea los temas que se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="b243a-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="b243a-171">**Tema**</span><span class="sxs-lookup"><span data-stu-id="b243a-171">**Topic**</span></span>|<span data-ttu-id="b243a-172">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b243a-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b243a-173">Notificación de eventos en MAPI</span><span class="sxs-lookup"><span data-stu-id="b243a-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="b243a-174">Información general sobre los eventos de notificación y notificación.</span><span class="sxs-lookup"><span data-stu-id="b243a-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="b243a-175">Control de notificaciones</span><span class="sxs-lookup"><span data-stu-id="b243a-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="b243a-176">Descripción de cómo deben administrar los clientes las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="b243a-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="b243a-177">Admitir notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="b243a-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="b243a-178">Explicación de cómo los proveedores de servicios pueden usar el método **IMAPISupport** para generar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="b243a-178">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
<span data-ttu-id="b243a-179">Como las notificaciones de tabla son asincrónicas, los clientes pueden recibir una notificación de una fila agregada después de aprender sobre la adición a través de otros medios.</span><span class="sxs-lookup"><span data-stu-id="b243a-179">Because table notifications are asynchronous, clients can receive notification of an added row after learning about the addition through another means.</span></span> <span data-ttu-id="b243a-180">Es posible recibir un evento TABLE_ERROR cuando hay un error en un método **IMAPITable:: Sort**, **IMAPITable:: Restrict**o **IMAPITable:: SetColumns** o cuando un proceso subyacente intenta actualizar una tabla con, por ejemplo, New o filas modificadas.</span><span class="sxs-lookup"><span data-stu-id="b243a-180">It is possible to receive a TABLE_ERROR event when there is an error in an **IMAPITable::Sort**, **IMAPITable::Restrict**, or **IMAPITable::SetColumns** method or when an underlying process attempts to update a table with, for example, new or modified rows.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b243a-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="b243a-181">See also</span></span>

- [<span data-ttu-id="b243a-182">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="b243a-182">NOTIFICATION</span></span>](notification.md) 
- [<span data-ttu-id="b243a-183">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="b243a-183">ScDupPropset</span></span>](scduppropset.md)
- [<span data-ttu-id="b243a-184">SRow</span><span class="sxs-lookup"><span data-stu-id="b243a-184">SRow</span></span>](srow.md)
- [<span data-ttu-id="b243a-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b243a-185">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="b243a-186">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="b243a-186">MAPI Structures</span></span>](mapi-structures.md)

