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
ms.openlocfilehash: 7f32145e0947411c48e1e6c3a941c9913a08709c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565847"
---
# <a name="tablenotification"></a><span data-ttu-id="d93fb-103">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d93fb-103">TABLE_NOTIFICATION</span></span>

<span data-ttu-id="d93fb-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d93fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d93fb-105">Describe una fila en una tabla que se ha visto afectada por algún tipo de evento, como un cambio o un error.</span><span class="sxs-lookup"><span data-stu-id="d93fb-105">Describes a row in a table that has been affected by some type of event, such as a change or an error.</span></span> <span data-ttu-id="d93fb-106">Esto hace que una notificación de la tabla que se genere.</span><span class="sxs-lookup"><span data-stu-id="d93fb-106">This causes a table notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d93fb-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d93fb-107">Header file:</span></span>  <br/> |<span data-ttu-id="d93fb-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d93fb-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="d93fb-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="d93fb-109">Members</span></span>

<span data-ttu-id="d93fb-110">**ulTableEvent**</span><span class="sxs-lookup"><span data-stu-id="d93fb-110">**ulTableEvent**</span></span>
  
> <span data-ttu-id="d93fb-111">Máscara de bits de indicadores que se utilizan para representar el tipo de evento de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d93fb-111">Bitmask of flags used to represent the table event type.</span></span> <span data-ttu-id="d93fb-112">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="d93fb-112">The following flags can be set:</span></span>
    
<span data-ttu-id="d93fb-113">TABLE_CHANGED</span><span class="sxs-lookup"><span data-stu-id="d93fb-113">TABLE_CHANGED</span></span> 
  
> <span data-ttu-id="d93fb-114">Indica a un nivel alto, que ha cambiado algo acerca de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d93fb-114">Indicates at a high level that something about the table has changed.</span></span> <span data-ttu-id="d93fb-115">Estado de la tabla es tal como estaba antes del evento.</span><span class="sxs-lookup"><span data-stu-id="d93fb-115">The table's state is as it was before the event.</span></span> <span data-ttu-id="d93fb-116">Esto significa que todas las propiedades **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), marcadores, la posición actual y las selecciones de interfaz de usuario siguen siendo válidas.</span><span class="sxs-lookup"><span data-stu-id="d93fb-116">This means that all **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) properties, bookmarks, current positioning, and user interface selections are still valid.</span></span> <span data-ttu-id="d93fb-117">Controlar este evento por volver a leer la tabla.</span><span class="sxs-lookup"><span data-stu-id="d93fb-117">Handle this event by rereading the table.</span></span> <span data-ttu-id="d93fb-118">Proveedores de servicios que no desea implementar notificaciones de tabla enriquecido envían eventos TABLE_CHANGED en lugar de eventos más detallados para indicar un determinado tipo de cambio.</span><span class="sxs-lookup"><span data-stu-id="d93fb-118">Service providers that do not want to implement rich table notifications send TABLE_CHANGED events instead of more detailed events to indicate a particular type of change.</span></span> 
    
<span data-ttu-id="d93fb-119">TABLE_ERROR</span><span class="sxs-lookup"><span data-stu-id="d93fb-119">TABLE_ERROR</span></span> 
  
> <span data-ttu-id="d93fb-120">Se ha producido un error normalmente durante el procesamiento de una operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="d93fb-120">An error has occurred, usually during the processing of an asynchronous operation.</span></span> <span data-ttu-id="d93fb-121">Errores durante el procesamiento de los métodos siguientes pueden generar este evento:</span><span class="sxs-lookup"><span data-stu-id="d93fb-121">Errors during the processing of the following methods can generate this event:</span></span> 
    
   - [<span data-ttu-id="d93fb-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="d93fb-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
   - [<span data-ttu-id="d93fb-123">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="d93fb-123">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
   - [<span data-ttu-id="d93fb-124">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="d93fb-124">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
   <span data-ttu-id="d93fb-125">Después de recibir un evento TABLE_ERROR, un cliente no puede confiar en la precisión de la tabla de contenido.</span><span class="sxs-lookup"><span data-stu-id="d93fb-125">After receiving a TABLE_ERROR event, a client cannot rely on the accuracy of the table contents.</span></span> <span data-ttu-id="d93fb-126">Además, las notificaciones sobre otros cambios pendientes se pueden perder.</span><span class="sxs-lookup"><span data-stu-id="d93fb-126">Also, pending notifications about other changes might be lost.</span></span> <span data-ttu-id="d93fb-127">El método [IMAPITable::GetLastError](imapitable-getlasterror.md) no es posible que proporciona información adicional sobre el error ya que se generó en algún momento anterior, no necesariamente desde la última llamada al método.</span><span class="sxs-lookup"><span data-stu-id="d93fb-127">The [IMAPITable::GetLastError](imapitable-getlasterror.md) method might not provide any additional information about the error because it was generated at some previous point, not necessarily from the last method call.</span></span> 
    
<span data-ttu-id="d93fb-128">TABLE_RELOAD</span><span class="sxs-lookup"><span data-stu-id="d93fb-128">TABLE_RELOAD</span></span> 
  
> <span data-ttu-id="d93fb-129">Deben volver a cargar los datos en la tabla.</span><span class="sxs-lookup"><span data-stu-id="d93fb-129">The data in the table should be reloaded.</span></span> <span data-ttu-id="d93fb-130">Proveedores de servicios de envían TABLE_RELOAD cuando, por ejemplo, los datos subyacentes se almacenan en una base de datos y la base de datos se ha reemplazado.</span><span class="sxs-lookup"><span data-stu-id="d93fb-130">Service providers send TABLE_RELOAD when, for example, the underlying data is stored in a database and the database is replaced.</span></span> <span data-ttu-id="d93fb-131">Controlar este evento por suponiendo que nada acerca de la tabla todavía es válido y volviendo a leerlo en la tabla.</span><span class="sxs-lookup"><span data-stu-id="d93fb-131">Handle this event by assuming that nothing about the table is still valid and by rereading the table.</span></span> <span data-ttu-id="d93fb-132">Todos los marcadores, las claves de la instancia, estado e información de posición no son válidos.</span><span class="sxs-lookup"><span data-stu-id="d93fb-132">All bookmarks, instance keys, status and positioning information are invalid.</span></span>
    
<span data-ttu-id="d93fb-133">TABLE_RESTRICT_DONE</span><span class="sxs-lookup"><span data-stu-id="d93fb-133">TABLE_RESTRICT_DONE</span></span> 
  
> <span data-ttu-id="d93fb-134">Ha finalizado una operación de restricción que se inició con una llamada al método **IMAPITable:: Restrict** .</span><span class="sxs-lookup"><span data-stu-id="d93fb-134">A restriction operation initiated with an **IMAPITable::Restrict** method call has completed.</span></span> 
    
<span data-ttu-id="d93fb-135">TABLE_ROW_ADDED</span><span class="sxs-lookup"><span data-stu-id="d93fb-135">TABLE_ROW_ADDED</span></span> 
  
> <span data-ttu-id="d93fb-136">Se agregó una nueva fila a la tabla y el correspondiente objeto guardado.</span><span class="sxs-lookup"><span data-stu-id="d93fb-136">A new row has been added to the table and the corresponding object saved.</span></span> <span data-ttu-id="d93fb-137">Eventos TABLE_ROW_ADDED se generan después de una llamada al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="d93fb-137">TABLE_ROW_ADDED events are generated after a call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
<span data-ttu-id="d93fb-138">TABLE_ROW_DELETED</span><span class="sxs-lookup"><span data-stu-id="d93fb-138">TABLE_ROW_DELETED</span></span> 
  
> <span data-ttu-id="d93fb-139">Se ha quitado una fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d93fb-139">A row has been removed from the table.</span></span> <span data-ttu-id="d93fb-140">El miembro **propPrior** se establece en NULL.</span><span class="sxs-lookup"><span data-stu-id="d93fb-140">The **propPrior** member is set to NULL.</span></span> 
    
<span data-ttu-id="d93fb-141">TABLE_ROW_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="d93fb-141">TABLE_ROW_MODIFIED</span></span> 
  
> <span data-ttu-id="d93fb-142">Se ha modificado una fila.</span><span class="sxs-lookup"><span data-stu-id="d93fb-142">A row has been changed.</span></span> <span data-ttu-id="d93fb-143">El miembro de **fila** contiene las propiedades afectadas para la fila.</span><span class="sxs-lookup"><span data-stu-id="d93fb-143">The **row** member contains the affected properties for the row.</span></span> <span data-ttu-id="d93fb-144">Varios eventos TABLE_ROW_MODIFIED se envían en el orden en que aparecen en la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="d93fb-144">Multiple TABLE_ROW_MODIFIED events are sent in the order that they appear in the table view.</span></span> 
    
  <span data-ttu-id="d93fb-145">Eventos TABLE_ROW_MODIFIED se envían después de los cambios realizados en el objeto correspondiente se han confirmado con una llamada al método **IMAPIProp::SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="d93fb-145">TABLE_ROW_MODIFIED events are sent after changes to the corresponding object have been committed with a call to the **IMAPIProp::SaveChanges** method.</span></span> <span data-ttu-id="d93fb-146">Si la fila modificada ahora es la primera fila en la tabla, el valor de la etiqueta de propiedad en el miembro **propPrior** es **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d93fb-146">If the modified row is now the first row in the table, the value of the property tag in the **propPrior** member is **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
    
<span data-ttu-id="d93fb-147">TABLE_SETCOL_DONE</span><span class="sxs-lookup"><span data-stu-id="d93fb-147">TABLE_SETCOL_DONE</span></span> 
  
> <span data-ttu-id="d93fb-148">Ha finalizado una operación de configuración de columna iniciada con una llamada al método **IMAPITable::SetColumns** .</span><span class="sxs-lookup"><span data-stu-id="d93fb-148">A column setting operation initiated with an **IMAPITable::SetColumns** method call has completed.</span></span> 
    
<span data-ttu-id="d93fb-149">TABLE_SORT_DONE</span><span class="sxs-lookup"><span data-stu-id="d93fb-149">TABLE_SORT_DONE</span></span> 
  
> <span data-ttu-id="d93fb-150">Se ha completado una operación iniciada con una llamada al método **SortTable** de ordenación de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d93fb-150">A table sorting operation initiated with an **IMAPITable::SortTable** method call has completed.</span></span> 
    
<span data-ttu-id="d93fb-151">**hResult**</span><span class="sxs-lookup"><span data-stu-id="d93fb-151">**hResult**</span></span>
  
> <span data-ttu-id="d93fb-152">Valor HRESULT del error que se ha producido, si se establece el miembro **ulTableEvent** en TABLE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="d93fb-152">HRESULT value for the error that has occurred, if the **ulTableEvent** member is set to TABLE_ERROR.</span></span> 
    
<span data-ttu-id="d93fb-153">**propIndex**</span><span class="sxs-lookup"><span data-stu-id="d93fb-153">**propIndex**</span></span>
  
> <span data-ttu-id="d93fb-154">Estructura de [SPropValue](spropvalue.md) para la propiedad **PR_INSTANCE_KEY** de la fila afectada.</span><span class="sxs-lookup"><span data-stu-id="d93fb-154">[SPropValue](spropvalue.md) structure for the **PR_INSTANCE_KEY** property of the affected row.</span></span> 
    
<span data-ttu-id="d93fb-155">**propPrior**</span><span class="sxs-lookup"><span data-stu-id="d93fb-155">**propPrior**</span></span>
  
> <span data-ttu-id="d93fb-156">Estructura de **SPropValue** para la propiedad **PR_INSTANCE_KEY** de la fila antes de la afectados.</span><span class="sxs-lookup"><span data-stu-id="d93fb-156">**SPropValue** structure for the **PR_INSTANCE_KEY** property of the row before the affected one.</span></span> <span data-ttu-id="d93fb-157">Si la fila afectada es la primera fila en la tabla, se debe establecer **propPrior** a **PR_NULL** y no cero.</span><span class="sxs-lookup"><span data-stu-id="d93fb-157">If the affected row is the first row in the table, **propPrior** must be set to **PR_NULL** and not zero.</span></span> <span data-ttu-id="d93fb-158">Cero no es una etiqueta de propiedad válido.</span><span class="sxs-lookup"><span data-stu-id="d93fb-158">Zero is not a valid property tag.</span></span> 
    
<span data-ttu-id="d93fb-159">**row**</span><span class="sxs-lookup"><span data-stu-id="d93fb-159">**row**</span></span>
  
> <span data-ttu-id="d93fb-160">Estructura de [SRow](srow.md) que describe la fila afectada.</span><span class="sxs-lookup"><span data-stu-id="d93fb-160">[SRow](srow.md) structure describing the affected row.</span></span> <span data-ttu-id="d93fb-161">Esta estructura se rellena para todos los eventos de notificación de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d93fb-161">This structure is filled for all table notification events.</span></span> <span data-ttu-id="d93fb-162">Para los eventos de notificación de tabla que no pasan la fila de datos, el miembro **cValues** de la estructura **SRow** se establece en cero y el miembro **lpProps** se establece en NULL.</span><span class="sxs-lookup"><span data-stu-id="d93fb-162">For table notification events that do not pass row data, the **cValues** member of the **SRow** structure is set to zero and the **lpProps** member is set to NULL.</span></span> <span data-ttu-id="d93fb-163">Debido a que esta estructura **SRow** es de sólo lectura; los clientes deben realizar una copia de la misma si desean hacer modificaciones.</span><span class="sxs-lookup"><span data-stu-id="d93fb-163">Because this **SRow** structure is read-only; clients must make a copy of it if they want to make modifications.</span></span> <span data-ttu-id="d93fb-164">La función [ScDupPropset](scduppropset.md) puede utilizarse para realizar la copia.</span><span class="sxs-lookup"><span data-stu-id="d93fb-164">The [ScDupPropset](scduppropset.md) function can be used to make the copy.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d93fb-165">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d93fb-165">Remarks</span></span>

<span data-ttu-id="d93fb-166">El **tabla\_notificación** estructura es uno de los miembros de la unión de estructuras incluidos en el miembro de la **información** de la estructura de [notificación](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="d93fb-166">The **TABLE\_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="d93fb-167">El miembro **info** incluye un **tabla\_notificación** estructurar cuando el miembro **ulEventType** de la estructura está establecido en _fnevTableModified_.</span><span class="sxs-lookup"><span data-stu-id="d93fb-167">The **info** member includes a **TABLE\_NOTIFICATION** structure when the **ulEventType** member of the structure is set to  _fnevTableModified_.</span></span>
  
<span data-ttu-id="d93fb-168">El orden y el tipo de columnas en el miembro de fila que refleje el orden y el tipo que estaba en efecto en el momento en que se generó la notificación.</span><span class="sxs-lookup"><span data-stu-id="d93fb-168">The order and type of columns in the row member reflect the order and type that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="d93fb-169">El orden y el tipo en el momento en que se generó la notificación no es necesariamente el mismo que cuando se entregó la notificación.</span><span class="sxs-lookup"><span data-stu-id="d93fb-169">The order and type at the time that the notification was generated is not necessarily the same as when the notification was delivered.</span></span> 
  
<span data-ttu-id="d93fb-170">Para obtener más información acerca de las notificaciones, vea los temas que se describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="d93fb-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="d93fb-171">**Tema**</span><span class="sxs-lookup"><span data-stu-id="d93fb-171">**Topic**</span></span>|<span data-ttu-id="d93fb-172">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d93fb-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d93fb-173">Notificación de eventos en MAPI</span><span class="sxs-lookup"><span data-stu-id="d93fb-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="d93fb-174">Descripción general de notificación y eventos de notificación.</span><span class="sxs-lookup"><span data-stu-id="d93fb-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="d93fb-175">Administrar notificaciones</span><span class="sxs-lookup"><span data-stu-id="d93fb-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="d93fb-176">Explicación de cómo los clientes deben controlar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="d93fb-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="d93fb-177">Compatibilidad con la notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="d93fb-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="d93fb-178">Explicación de cómo los proveedores de servicios pueden usar el método **IMAPISupport** para generar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="d93fb-178">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
<span data-ttu-id="d93fb-179">Debido a que las notificaciones de tabla son asincrónicas, los clientes pueden recibir notificaciones de una fila se ha agregado después de aprendizaje acerca de la adición a través de otro medio.</span><span class="sxs-lookup"><span data-stu-id="d93fb-179">Because table notifications are asynchronous, clients can receive notification of an added row after learning about the addition through another means.</span></span> <span data-ttu-id="d93fb-180">Es posible recibir un evento TABLE_ERROR cuando se ha producido un error en un método **IMAPITable::Sort**, **IMAPITable:: Restrict**o **IMAPITable::SetColumns** o cuando subyacentes de un proceso intenta actualizar una tabla con, por ejemplo, la nueva funcionalidad o las filas modificadas.</span><span class="sxs-lookup"><span data-stu-id="d93fb-180">It is possible to receive a TABLE_ERROR event when there is an error in an **IMAPITable::Sort**, **IMAPITable::Restrict**, or **IMAPITable::SetColumns** method or when an underlying process attempts to update a table with, for example, new or modified rows.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d93fb-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="d93fb-181">See also</span></span>

- [<span data-ttu-id="d93fb-182">Notificaci�n</span><span class="sxs-lookup"><span data-stu-id="d93fb-182">NOTIFICATION</span></span>](notification.md) 
- [<span data-ttu-id="d93fb-183">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="d93fb-183">ScDupPropset</span></span>](scduppropset.md)
- [<span data-ttu-id="d93fb-184">SRow</span><span class="sxs-lookup"><span data-stu-id="d93fb-184">SRow</span></span>](srow.md)
- [<span data-ttu-id="d93fb-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d93fb-185">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="d93fb-186">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="d93fb-186">MAPI Structures</span></span>](mapi-structures.md)

